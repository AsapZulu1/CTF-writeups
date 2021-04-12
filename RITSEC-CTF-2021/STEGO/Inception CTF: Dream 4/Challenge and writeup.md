# Challenge

Note: This challenge builds off of [Inception CTF: Dream 3]().

Don’t lose yourself within the dreams, it’s critical to have your totem. Take a close look at the facts of the file presented to you. Please note the flag is marked with an “RITSEC=” rather than {} due to encoding limitations.

The flag will need to be converted to RITSEC{}

# Solution

The password from the flag in [InceptionCTF: Dream 3]() was used to extract files from SnowFortress.7z.
Extracted files:
* Limbo.7z
* PasswordPath.exe

I noticed that there were something strange with the name of the .exe. 
I extracted strings in terminal using the strings command. The last part of the output was:
<pre>Wait a minute, whose subconscious are we going into, exactly? {dnalmaerD}CESTIR
</pre>
This string is known from [Inception CTF: Dream 1](). So that would likely not be the flag fort this challenge. 
This was in the output over the mentioned line:

<pre>&lt;script language=&quot;javascript&quot;&gt;document.write(unescape(&apos;3c%68%74%6d%6c%3e%0a%3c%62%6f%64%79%3e%0a%0a%3c%21%44%4f%43%54%59%50%45%20%68%74%6d%6c%3e%0a%3c%68%74%6d%6c%3e%0a%3c%68%65%61%64%3e%0a%20%20%20%20%3c%74%69%74%6c%65%3e%4e%6f%6e%2c%20%6a%65%20%6e%65%20%72%65%67%72%65%74%74%65%20%72%69%65%6e%3c%2f%74%69%74%6c%65%3e%0a%3c%48%54%41%3a%41%50%50%4c%49%43%41%54%49%4f%4e%0a%20%20%41%50%50%4c%49%43%41%54%49%4f%4e%4e%41%4d%45%3d%22%4e%6f%6e%2c%20%6a%65%20%6e%65%20%72%65%67%72%65%74%74%65%20%72%69%65%6e%22%0a%20%20%49%44%3d%22%49%6e%63%65%70%74%69%6f%6e%22%0a%20%20%56%45%52%53%49%4f%4e%3d%22%31%2e%30%22%0a%20%20%53%43%52%4f%4c%4c%3d%22%6e%6f%22%2f%3e%0a%20%0a%3c%73%74%79%6c%65%20%74%79%70%65%3d%22%74%65%78%74%2f%63%73%73%22%3e%0a%3c%2f%68%65%61%64%3e%0a%20%20%20%20%3c%64%69%76%20%69%64%3d%22%66%65%61%74%75%72%65%22%3e%0a%20%20%20%20%20%20%20%20%20%20%20%20%3c%64%69%76%20%69%64%3d%22%63%6f%6e%74%65%6e%74%0a%09%09%09%09%3c%2f%73%74%79%6c%65%3e%0a%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%3c%68%31%20%69%64%3d%22%75%6e%61%76%61%69%6c%61%62%6c%65%22%20%63%6c%61%73%73%3d%22%6c%6f%61%64%69%6e%67%22%3e%42%75%69%6c%64%69%6e%67%20%44%72%65%61%6d%73%2e%2e%2e%2e%3c%2f%68%31%3e%0a%09%09%09%09%3c%73%63%72%69%70%74%20%74%79%70%65%3d%22%74%65%78%74%2f%6a%61%76%61%73%63%72%69%70%74%22%20%6c%61%6e%67%75%61%67%65%3d%22%6a%61%76%61%73%63%72%69%70%74%22%3e%0a%09%09%09%09%09%66%75%6e%63%74%69%6f%6e%20%52%75%6e%46%69%6c%65%28%29%20%7b%0a%09%09%09%09%09%57%73%68%53%68%65%6c%6c%20%3d%20%6e%65%77%20%41%63%74%69%76%65%58%4f%62%6a%65%63%74%28%22%57%53%63%72%69%70%74%2e%53%68%65%6c%6c%22%29%3b%0a%09%09%09%09%09%57%73%68%53%68%65%6c%6c%2e%52%75%6e%28%22%6e%6f%74%65%70%61%64%20%25%55%53%45%52%50%52%4f%46%49%4c%45%25%2f%44%65%73%6b%74%6f%70%2f%49%6e%63%65%70%74%69%6f%6e%43%54%46%2f%52%65%61%6c%69%74%79%2f%56%61%6e%43%68%61%73%65%2f%54%68%65%48%6f%74%65%6c%2f%54%68%65%50%6f%69%6e%74%4d%61%6e%2e%74%78%74%22%2c%20%31%2c%20%66%61%6c%73%65%29%3b%0a%09%09%09%09%09%7d%0a%09%09%09%09%3c%2f%73%63%72%69%70%74%3e%0a%20%20%20%20%20%20%20%20%3c%2f%64%69%76%3e%0a%20%20%20%20%3c%2f%64%69%76%3e%0a%3c%62%6f%64%79%3e%0a%09%3c%69%6e%70%75%74%20%74%79%70%65%3d%22%62%75%74%74%6f%6e%22%20%76%61%6c%75%65%3d%22%49%6d%70%6c%61%6e%74%20%49%6e%63%65%70%74%69%6f%6e%20%48%65%72%65%22%20%6f%6e%63%6c%69%63%6b%3d%22%52%75%6e%46%69%6c%65%28%29%3b%22%2f%3e%0a%09%3c%70%20%73%74%79%6c%65%3d%22%63%6f%6c%6f%72%3a%77%68%69%74%65%3b%22%3e%0a%2d%2e%2e%20%2e%2d%2e%20%2e%20%2e%2d%20%2d%2d%20%2e%2e%2e%0a%2e%2e%2d%2e%20%2e%20%2e%20%2e%2d%2e%2e%0a%2e%2d%2e%20%2e%20%2e%2d%20%2e%2d%2e%2e%0a%2e%2d%2d%20%2e%2e%2e%2e%20%2e%20%2d%2e%0a%2e%2d%2d%20%2e%20%2e%2d%2d%2d%2d%2e%20%2e%2d%2e%20%2e%0a%2e%2e%20%2d%2e%0a%2d%20%2e%2e%2e%2e%20%2e%20%2d%2d%20%2e%2d%2e%2d%2e%2d%0a%2e%2e%20%2d%20%2e%2d%2d%2d%2d%2e%20%2e%2e%2e%0a%2d%2d%2d%20%2d%2e%20%2e%2d%2e%2e%20%2d%2e%2d%2d%0a%2e%2d%2d%20%2e%2e%2e%2e%20%2e%20%2d%2e%0a%2e%2d%2d%20%2e%0a%2e%2d%2d%20%2e%2d%20%2d%2e%2d%20%2e%0a%2e%2e%2d%20%2e%2d%2d%2e%0a%2d%20%2e%2e%2e%2e%20%2e%2d%20%2d%0a%2e%2d%2d%20%2e%0a%2e%2d%2e%20%2e%20%2e%2d%20%2e%2d%2e%2e%20%2e%2e%20%2d%2d%2e%2e%20%2e%0a%2e%2e%2e%20%2d%2d%2d%20%2d%2d%20%2e%20%2d%20%2e%2e%2e%2e%20%2e%2e%20%2d%2e%20%2d%2d%2e%0a%2e%2d%2d%20%2e%2d%20%2e%2e%2e%0a%2e%2d%20%2d%2e%2d%2e%20%2d%20%2e%2e%2d%20%2e%2d%20%2e%2d%2e%2e%20%2e%2d%2e%2e%20%2d%2e%2d%2d%0a%2e%2e%2e%20%2d%20%2e%2d%2e%20%2e%2d%20%2d%2e%20%2d%2d%2e%20%2e%20%2e%2d%2e%2d%2e%2d%0a%2e%2d%2e%20%2e%2e%20%2d%20%2e%2e%2e%20%2e%20%2d%2e%2d%2e%20%2d%2e%2e%2e%2d%20%2d%2e%2e%20%2e%2e%20%2e%2e%2e%2d%20%2e%20%2e%2d%2e%20%2e%2e%2e%20%2e%2e%20%2d%2d%2d%20%2d%2e%20%0a%3c%2f%70%3e%0a%3c%2f%62%6f%64%79%3e%0a%3c%2f%62%6f%64%79%3e%0a%20%20%3c%2f%68%74%6d%6c%3e&apos;));&lt;/script&gt;
</pre>

The output was a html-code with an incorporated morse-code:
<pre><b>-.. .-. . .- -- ...</b>
<b>..-. . . .-..</b>
<b>.-. . .- .-..</b>
<b>.-- .... . -.</b>
<b>.-- . .----. .-. .</b>
<b>.. -.</b>
<b>- .... . -- .-.-.-</b>
<b>.. - .----. ...</b>
<b>--- -. .-.. -.--</b>
<b>.-- .... . -.</b>
<b>.-- .</b>
<b>.-- .- -.- .</b>
<b>..- .--.</b>
<b>- .... .- -</b>
<b>.-- .</b>
<b>.-. . .- .-.. .. --.. .</b>
<b>... --- -- . - .... .. -. --.</b>
<b>.-- .- ...</b>
<b>.- -.-. - ..- .- .-.. .-.. -.--</b>
<b>... - .-. .- -. --. . .-.-.-</b>
<b>.-. .. - ... . -.-. -...- -.. .. ...- . .-. ... .. --- -. </b></pre>

Decoded using [CyberChef](https://gchq.github.io/CyberChef/) and got this as output:
> DREAMS FEEL REAL WHEN WE'RE IN THEM. IT'S ONLY WHEN WE WAKE UP THAT WE REALIZE SOMETHING WAS ACTUALLY STRANGE. RITSEC=DIVERSION
> 
I converted the flag from RITSEC=DIVERSION to RITSEC{DIVERSION} as instructed in the challenge.

Flag:
>RITSEC{DIVERSION}
>

...to be continued in [Inception CTF: Dream 5]()
