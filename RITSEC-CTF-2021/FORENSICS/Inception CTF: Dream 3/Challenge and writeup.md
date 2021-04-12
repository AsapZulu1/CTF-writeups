# Challenge

Note: This challenge builds on Inception CTF: Dream 2.

While the first two steps were easy it’s all hard from here on out, ThePointMan is the most crucial role of the mission he has to be presentable but without giving away our intentions. Use Alternate Dream State to find the flag before the kick.

# Solution

TheHotel.7z opened with the password genereted in [Inception CTF: Dream 3] () contained the following files:
* SnowFortress.7z
* ThePointMan.txt
* A file with no name

The file with no name could be opened in a text editor, and contained the following line: 
`You mean, a dream within a dream? NTIgNDkgNTQgNTMgNDUgNDMgN2IgNDYgNDAgMjEgMjEgNjkgNmUgNjcgNDUgNmMgNjUgNzYgNDAgNzQgNmYgNzIgN2Q= `

Used the hURL command to decode Base64 first, then HEX:
<pre><font color="#5EBDAB">┌──(</font><font color="#277FFF"><b>asapzulu㉿kali</b></font><font color="#5EBDAB">)-[</font><b>~</b><font color="#5EBDAB">]</font>
<font color="#5EBDAB">└─</font><font color="#277FFF"><b>$</b></font> <font color="#5EBDAB">hURL</font> <font color="#9755B3">-b</font> NTIgNDkgNTQgNTMgNDUgNDMgN2IgNDYgNDAgMjEgMjEgNjkgNmUgNjcgNDUgNmMgNjUgNzYgNDAgNzQgNmYgNzIgN2Q=

<font color="#277FFF"><b>Original string       :: </b></font><b>NTIgNDkgNTQgNTMgNDUgNDMgN2IgNDYgNDAgMjEgMjEgNjkgNmUgNjcgNDUgNmMgNjUgNzYgNDAgNzQgNmYgNzIgN2Q=</b>
<font color="#05A1F7"><b>base64 DEcoded string :: </b></font><b>52 49 54 53 45 43 7b 46 40 21 21 69 6e 67 45 6c 65 76 40 74 6f 72 7d</b>
                                                                                                  
<font color="#5EBDAB">┌──(</font><font color="#277FFF"><b>asapzulu㉿kali</b></font><font color="#5EBDAB">)-[</font><b>~</b><font color="#5EBDAB">]</font>
<font color="#5EBDAB">└─</font><font color="#277FFF"><b>$</b></font> <font color="#5EBDAB">hURL</font> <font color="#9755B3">-x</font> <font color="#FEA44C">&quot;52 49 54 53 45 43 7b 46 40 21 21 69 6e 67 45 6c 65 76 40 74 6f 72 7d&quot;</font>            

<font color="#277FFF"><b>Original HEX      :: </b></font><b>5249545345437b46402121696e67456c657640746f727d</b>
<font color="#05A1F7"><b>ASCII/RAW DEcoded :: </b></font><b>RITSEC{F@!!ingElev@tor}</b>
</pre>

ThePointMan.txt contained several codes but turned out to be a "fake rabbithole" with strings like "Create a maze in two minutes that takes me one munite to solve. " and " You're waiting for a train, a train that will take you far away. You know where you hope this train will take you, but you can&apos;t be sure. but it doesn't matter - because we'll be together." when decoded. 

Flag:
`RITSEC{F@!!ingElev@tor}`

To be continued in [Inception CTF: Dream 4](), now in the STEGO category.
