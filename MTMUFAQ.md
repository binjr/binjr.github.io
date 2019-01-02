---
title: MTMUFAQ
layout: default
---

# MTMUFAQ[\*](#-mandatory-totally-made-up-faq)



_**binjr ??!? How the hell do you say that?**_

Well, I say "binger", as in ginger, but you're welcome to say it however you want.

***

_**binjr ??!? What the hell does it mean?**_

It is, sadly, Yet Another Oh-So-Clever Recursive Acronym (YAOSCRA??), and it stands for "**B**injr **I**s **N**ot a **J**RDS **R**ewrite". 

[JRDS](http://jrds.fr) is a monitoring application which was the first compatible source of data for binjr. As a matter of fact, using JRDS extensively and getting frustrated with the limitations of its user interface was the main inspiration for writing this tool.
	
***

_**Well in that case you should have called it "ginjr"; it's even more worthy of nerdy street cred, isn't it?**_

Yay, I know, you're right. But I realized that too late and couldn't be bothered refactoring everything at that stage. Plus I'd already bought the domain name, and I'm far too cheap to buy another one.
	
***

_**Anyways... You really seem to have a thing for acronyms, don't you?**_

I actually hate acronyms. Having been in the software industry for a while now, I've come to literally cringe every time I hear someone drowning his/her audience in sea of those. And then I realize that person is me...
	
***

_**Riiiiight... Moving on; so, binjr, what's that anyway?**_

In a nutshell, binjr is a tool that plots time series. It doesn't produce any data to speak off, it only displays data produced by other applications. It is a client application, written in Java, packaged as a single executable JAR file and has no other requirement than a compatible Java Runtime Environment. 

 As explained above, it was originally developed as an alternative front end to the monitoring application called [JRDS](http://jrds.fr).
	
***

_**Why on earth did you write it as a thick client in Java? Why not a webapp using some spiffy new frontend framework?**_

One main reason for that: I am *NOT* touching Javascript with a 10 foot pole. Period. So there's that, and also the fact that a I'm quite keen on small, self-contained and portable tools, therefore I find having something that can be run by simply launching a single executable/JAR appealing. Plus, JavaFX (Java's new UI framework) is actually quite nice to work with, and it's fairly easy to produce decent looking UI with it.
	
***

_**I am using Cacti, Munin, some other tool base on RRDTool or RRD4J, etc... It already presents time series as charts but it does so by producing static images that you can't zoom in or out using the mouse, so the overall experience isn't all that great. Can I use binjr to present that data in a more flexible way?**_

This is precisely what binjr was made for, so yes it can probably help. But... before that can happen, the code needed to specifically retrieve the raw data from the source will likely need to be written. Feel free to propose support for a specific data source as an enhancement [here](https://github.com/binjr/binjr/issues), but be aware that the available bandwidth of the contributors is limited, so unless extra help is provided, any significant enhancement proposal is unlikely to come to fruition.
	
***

_**Ok, so I'm developer and I'd be glad to help; can I contribute that code to the project?**_

Why yes, absolutely! The best way to contribute code is to fork the project on github and send a pull request with your changes. If you have question about the API, or if you find something broken, you can get in touch by opening an issue [here](https://github.com/binjr/binjr/issues).

***
	
_**I have a use case that is completely different from what you just describe, but I feel that all or part of the binjr code base could help me. Can I use it?**_

The source code of binjr is released under the terms of the Apache Software license version 2.0, so you're free to use it in accordance with those terms. In any case, I'd love to hear about what you have in mind so feel free to get in touch by email to binjr_AT_free_DOT_fr.

***
	
_**Nice logo, by the way. I quite like the colour scheme.**_

It's nice, isn't? My wife picked it, actually. She says "bleu canard" is definitely this season's colour!
	
***

_**Hey! That last one wasn't really a question, was it?**_

Well this isn't really a FAQ, so...
	
***

_**This is getting silly: where can I can some proper technical help to my very real technical issue?**_

You should try you luck at the [binjr wiki](https://github.com/binjr/binjr/wiki), starting with the [troubleshooting section](https://github.com/binjr/binjr/wiki/troubleshooting).

If all else fails, please open an issue [here](https://github.com/binjr/binjr/issues).
	
***


##### * Mandatory Totally Made Up FAQ
