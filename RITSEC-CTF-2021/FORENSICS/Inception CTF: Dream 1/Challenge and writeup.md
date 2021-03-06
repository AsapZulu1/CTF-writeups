# Challenge

The purpose of this CTF challenge is to identify common methods of hiding malicious files and code. In most cases adversaries will attempt to evade defenses in many cases by masquerading, hiding files, and more. There are five directories like the five levels in the movie Inception, Reality -> Van Chase -> The Hotel -> Snow Fortress -> Limbo. You will find one flag in each of the levels, that flag will also be the password to extract the next directory. Requirements: • You must have 7zip installed • Drop the InceptionCTF.7z on the Desktop as “InceptionCTF” • Use the option “Extract to "<name of directory>\\” for the CTF to function properly Missing either of the above may result in complications which may cause issues when attempting to find flags.

NOTE: These challenges have a flag format of RITSEC{}

Dream 1: We have to get to their subconscious first, look for a hidden text file within the directory “Reality” this flag will unlock the next directory.

# Solution

The provided InceptionCTFRITSEC.7z contained Reality.7z

The first flag was in the Subconcious.txt file extracted from the provided Reality.7z. 

The textfile only contained this:

> Wait a minute, whose subconscious are we going into, exactly? {dnalmaerD}CESTIR
> 
Revering the last section revealed the flag.

Flag: 
> RITSEC{Dreamland}
> 

As the challenge instructs, the flag is also the password for the VanChase.7z that was also extracted from Reality.7z


...to be continued in [Inception CTF: Dream 2](https://github.com/AsapZulu1/CTF-writeups/blob/main/RITSEC-CTF-2021/FORENSICS/Inception%20CTF:%20Dream%202/Challenge%20and%20writeup.md)
