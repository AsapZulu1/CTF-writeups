# Challenge
Robots are taking over. Find out more.

34.69.61.54:5247

# Writeup
The challenge name is obviously a hint. Entered this in a browser:
> http://34.69.61.54:5247/robots.txt
> 

The file had no protection. Did a quick search in the given document and found the line:
> Allow: /flag/UlN7UjBib3RzX2FyM19iNGR9
> 

Decoded the string with Base64:
> <pre><font color="#5EBDAB">┌──(</font><font color="#277FFF"><b>asapzulu㉿kali</b></font><font color="#5EBDAB">)-[</font><b>~</b><font color="#5EBDAB">]</font>
> <font color="#5EBDAB">└─</font><font color="#277FFF"><b>$</b></font> <font color="#5EBDAB">hURL</font> <font color="#9755B3">-b</font> UlN7UjBib3RzX2FyM19iNGR9                                      127 <font color="#EC0101"><b>⨯</b></font>
>
> <font color="#277FFF"><b>Original string       :: </b></font><b>UlN7UjBib3RzX2FyM19iNGR9</b>
> <font color="#05A1F7"><b>base64 DEcoded string :: </b></font><b>RS{R0bots_ar3_b4d}</b>
> </pre>
> 

Flag:
> RS{R0bots_ar3_b4d}
> 

