# Troubleshooting

Although launching *binjr* should idealy be as simple as double-clicking an icon, sometimes things go wrong... 

Here you'll find here answers to some issues commonly encountered when trying to run binjr.

### JavaFX

binjr relies on JavaFX for its user interface if is not present, it will fail to start.

As of version 8, JavaFX is distributed by default in Oracle's JRE on all supported platforms. Unfortunately, it is not the case with the OpenJDK runtime environment provided with most Linux distributions.

In this case, you can either:

* Install the Oracle JRE for your platform.
* Build or install a prebuilt package for OpenJFX.

For instance, if you're running Ubuntu 16.04, OpenJFX can be installed via:

    sudo apt-get install openjfx

### Java 9

The compiled versions of binjr found on the [Release](https://github.com/binjr/binjr/releases) page, both JAR and native bundles, are built against Java 8 and are *not* compatible with Java 9.

In order to successfully run binjr under a Java 9 Runtime Environment, you'll need to checkout and build the [java9](https://github.com/binjr/binjr/tree/java9) branch.

Also, because JAXB, alongside the rest of the J2EE modules, is no longer implicitly declared in the JRE's classpath,  it is necessary to explicitly add the java.xml.bind module as a VM option:

    java --add-modules java.xml.bind -jar binjr.jar

### SSL/TLS and Certificates issues

If a certificate validation fails because a root CA certificate cannot be found in the certification path, you may need to import it into the JVM's trusted CA store (of course, ___only do that if you trust that CA___) :


      keytool -importcert -alias startssl -keystore $JAVA_HOME/jre/lib/security/cacerts -storepass changeit -file [myCaCert.der]


### Kerberos authentication

*binjr* supports Kerberos authentication to http based sources via SPNEGO. If you're having troubles, please check the following:

* Enable kerberos debug information for easier troubleshooting:

  `-Dsun.security.krb5.debug=true`

* Make sure the information in krb5.ini/krb5.conf is correct. To override the default location for the krb5 configuration file, use:

  `-Djava.security.krb5.conf=[PathTo]/krb5.conf`

  Refer to http://web.mit.edu/kerberos/krb5-1.4/krb5-1.4.1/doc/krb5-admin/krb5.conf.html for more info on how to configure Kerberos.

* If you need to override the JAAS login configuration, use the following propoerty to target the new config file:
        
  `-Djava.security.auth.login.config=[PathTo]/jaas_login.conf`

* If configuration is correct and a TGT (Ticket granting Ticket) is present in Kerberos credential cache but Single Sign On still fails (e.g. you are prompted with request for credentials), you may need to refresh the cache's ticket using `kinit`.

  If you're facing that issue under Windows, you may want to clear Java's specific ticket cache if it exists (by default `%USERPROFILE%\krb5cc_[username]`) to ensure TGT is retrieve from the LSA (Local Security Authority) instead.

* If running on Windows, you will likely need to modify the following registry key to allow the app to establish a session using the TGT recovered from the LSA (Reference: http://web.mit.edu/kerberos/kfw-3.2/kfw-3.2/relnotes.html#mslsa):
```
  HKLM\SYSTEM\CurrentControlSet\Control\Lsa\Kerberos\Parameters

  AllowTGTSessionKey = 0x01 (DWORD)
```

* Again, if you are running binjr on Windows and it fails to authenticate using the TGT retrieved from the Local Security Authority (LSA), but you *can* log if entering the same set of credentials when prompted, check whether the account you're using belong the local group `Administrators`.

  If it is the case, you may need to run the application with elevated UAC privileges to allow proper operation of Single Sign On, as Microsoft introduced further restriction on accessing the LSA's ticket cache for members of that group in Windows Vista and later (Reference: http://web.mit.edu/kerberos/kfw-3.2/kfw-3.2/relnotes.html#mslsa).

* If authentication still fails, including after you've provided a set a valid credentials and you're sure the configuration is correct, it might be because you're current JVM is not capable of handling the encryption type requested by the KDC. 
  
  In this case you may need to install the JCE (Java Cryptographic Extensions) Unlimited Strength Jurisdiction Policy Files from your JVM's vendor.

