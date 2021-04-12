# Challenge

Note: This challenge builds off Inception CTF: Dream 1,

Unfortunately, the subconscious isn’t enough for this mission, we have to kidnap Fischer we need to go further into the system of the mind. Use the flag found to edit the PowerShell script, entering the Flag in line three in-between the single quotes. Run the PowerShell script and wait for it to complete its actions.

Thanks to SRA for providing this challenge!

# Solution

The VanChase.7z contained the following files:
* TheHotel.7z
* Kicks.ps1
* Kidnap.txt

The txt-file contained this:

``An idea is like a virus, resilient, highly contagious. 
52 49 54 53 45 43 7b 57 61 74 65 72 55 6e 64 65 72 54 68 65 42 72 69 64 67 65 7d``

I used the hURL command to decode the message:

<pre><font color="#5EBDAB">┌──(</font><font color="#277FFF"><b>asapzulu㉿kali</b></font><font color="#5EBDAB">)-[</font><b>~</b><font color="#5EBDAB">]</font>
<font color="#5EBDAB">└─</font><font color="#277FFF"><b>$</b></font> <font color="#5EBDAB">hURL</font> <font color="#9755B3">-x</font> <font color="#FEA44C">&quot;52 49 54 53 45 43 7b 57 61 74 65 72 55 6e 64 65 72 54 68 65 42 72 69 64 67 65 7d&quot;</font>  

<font color="#277FFF"><b>Original HEX      :: </b></font><b>5249545345437b5761746572556e6465725468654272696467657d</b>
<font color="#05A1F7"><b>ASCII/RAW DEcoded :: </b></font><b>RITSEC{WaterUnderTheBridge}</b>
</pre>


Flag:
`RITSEC{WaterUnderTheBridge}`

...to be continued in [Inception CTF: Dream 3](https://github.com/AsapZulu1/CTF-writeups/blob/main/RITSEC-CTF-2021/FORENSICS/Inception%20CTF:%20Dream%203/Challenge%20and%20writeup.md)
