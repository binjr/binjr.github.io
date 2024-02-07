# Verifying downloads

Each file on the [download page](/download/latest_release/) is accompanied by an OpenPGP signature (a file with the 
same name as the package and the extension ".asc").   
It allows you to verify the file you've downloaded is exactly the one we intended you to get.

!!! Info  
    ***binjr***'s automatic update feature uses the same signatures to verify the integrity of the package it downloads 
    before installing it. 

## Installing GnuPG

First of all you need to have GnuPG installed before you can verify signatures.

=== "For Windows users"
    If you are using Windows, you can install [Gpg4win](https://gpg4win.org/download.html).  

=== "For macOS users"
    If you are using macOS, you can install [GPGTools](https://gpgtools.org/).

=== "For GNU/Linux users"
    If you are using GNU/Linux, then you probably already have GnuPG in your system, 
    as most GNU/Linux distributions come with it preinstalled.


## Verifying signatures

1. Download the binjr developers signing key
    ```
    curl https://binjr.eu/openpgpkey/binjr_dev_pub_keys.asc > binjr_dev_pub_keys.asc
    ```
  
2. Import the public key:
    ``` 
    gpg --import binjr_dev_pub_keys.asc
    ```

3. Verify the signature for the package you would like to authenticate:
    ``` 
    gpg --verify <package_name.extention>.asc <package_name.extention>
    ```
   
!!! Tip 
    Make sure you have downloaded *both* the package and its signature (.asc). 
    
If the verification is successful, the program should output something along these lines:
```
gpg: Signature made Wed Feb  7 16:29:54 2024 CET
gpg:                using RSA key AF45EEEFB23702CB
gpg: Good signature from "binjr (Package signing key) <signing@binjr.eu>"
```