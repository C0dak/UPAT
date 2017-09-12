# UPAT
UPAT (Ultimate Password Awareness Toolkit) is a toolkit to assess passwords strength through local attacks, you can run dictionary attacks, brute-force/mask attacks, analyze wordlists or create new ones, and generate strong passwords. 

A user-friendly interface allows to run through all steps and display the tools results.

Pre-requisites:
- Hashcat >= 3.50
- John the Ripper Bleeding Jumbo Edition
- Hashcat-Utils >= 1.7
- PACK >= 0.0.4
- CeWL >=5.2
- Crunch >= 3.6
- DyMerge >= 0.2
- Wyd >= 0.2
- PassTrust >= 2.1
- Pipal >= 3.1

Tested environments:
- Ubuntu 16.04 LTS
- CentOS

1/ Once dependancies are installed, run ./home.py
2/ Adjust the tools path and dictionary repo under Configure tab
3/ Run the Speed Test to benchmark your hardware
4/ Put some dictionaries under the repo folder, some good ones:
- The 500 Worst Passwords of All Times: https://github.com/danielmiessler/SecLists/blob/master/Passwords/500-worst-passwords.txt
- John's default dictionary: https://github.com/danielmiessler/SecLists/blob/master/Passwords/john.txt
- Crackstation's Human only (64M passwords): https://crackstation.net/buy-crackstation-wordlist-password-cracking-dictionary.htm
- PHPBB leak: https://github.com/danielmiessler/SecLists/blob/master/Passwords/phpbb.txt
- MySpace leak: https://github.com/danielmiessler/SecLists/blob/master/Passwords/myspace.txt
- OpenWall all: https://github.com/danielmiessler/SecLists/blob/master/Passwords/openwall_all.txt
- RockYou leak: https://github.com/danielmiessler/SecLists/blob/master/Passwords/rockyou.txt.tar.gz
- Cupp 3 foreign dictionaries

Now you are good to go.

----
Author: Pierre Jourdan
UPAT has been developed in the context of the Master's project in CyberSecurity proposed by UCLan Cyprus, under the supervision of Dr Eliana Stavrou.



Feel free to contribute.


An indicative roadmap for future improvements:

-	A huge announcement reported in august 2017 was the release of the biggest passwords dictionary from Have I Been Pwned website, consisting of 306 million entries which could be added to the Wordlists repository and used to check instantly if a given password has been leaked online and thus exclude it from use.

-	Integrate Hash Buster, a Python script released in June 2017 that takes as input an encrypted password and asks online services who basically host rainbow tables and known/leaked hashes for the matching plaintext. Ethical concerns however apply as the passwords would then be uploaded online on servers outside of our control.

-	Recommendations on how to create strong passwords are evolving as per NIST 800-63B Digital Identity Guidelines published in June 2017, and it is now preferred to allow long pass phrases which are simple to remember while being very hardly attackable through brute-force, and not impose composition rules with results in complex/unfriendly constructions. A tool such as Abbrase would be good to add in the Generate password tab of UPAT.

-	A tool measuring password strength would be good to add or even implementing a local algorithm

-	The ability to run distributed attacks taking advantage of multiple computers processing units to optimize cracking time. A server/client tool exists named Hashtopussy and allows to run distributed Hashcat jobs.
