# Challenge

Note: this challenge builds on [Inception CTF: Dream 4](https://github.com/AsapZulu1/CTF-writeups/blob/main/RITSEC-CTF-2021/STEGO/Inception%20CTF:%20Dream%204/Challenge%20and%20writeup.md).

We’re almost there, we just need Fischer to open the safe! That top looks awfully weird though.

# Solution

The flag from the previous "dream" was the password for Limbo.7z. It contained a single file:
* Inception.jpg

I found nothing using exiftool and several other stego-tools. I then extracted strings from the jpg. One string standed out being longer than the others;
> UklUU0VDezUyODQ5MX0g
> 

I tried to Base64-decoded the string:
<pre><font color="#5EBDAB">┌──(</font><font color="#277FFF"><b>asapzulu㉿kali</b></font><font color="#5EBDAB">)-[</font><b>~/Desktop</b><font color="#5EBDAB">]</font>
<font color="#5EBDAB">└─</font><font color="#277FFF"><b>$</b></font> <font color="#5EBDAB">hURL</font> <font color="#9755B3">-b</font> UklUU0VDezUyODQ5MX0g

<font color="#277FFF"><b>Original string       :: </b></font><b>UklUU0VDezUyODQ5MX0g</b>
<font color="#05A1F7"><b>base64 DEcoded string :: </b></font><b>RITSEC{528491} </b></pre>

Et voilà! 
The last flag of this 5-challenge route:
> RITSEC{528491}
> 
