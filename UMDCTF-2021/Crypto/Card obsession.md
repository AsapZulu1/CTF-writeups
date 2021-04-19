### Challenge
This relaxing card gif I found started making noise all of the sudden. What is going on?

Flag format: UMDCTF-{words\_go\_here}

`https://drive.google.com/drive/folders/1mQR9YrsiM4ZhZ8iof5XRzM3ukoneuccr?usp=sharing`

### Løsning
The given file was a .mp4-video with the sound of someone dialing numbers on a phone. 
I figured I had to extract the numbers being dialed. I used `dtmf`as a tool to extract the numbers.

But first I had to extract the audio from the video, using `ffmpeg`.

`$ ffmpeg -i card\ obsession.mp4 card\ obsession.wav`

Then I could run the `dtmf`-command.
Da kunne jeg bruke `dtmf`.

```
$ dtmf card\ obsession.wav
88632222833345444366666668855544B4452553332222777377777
```
I immediately suspected that the tool wasn´t 100% spot on since it extracted the letter B.

I runned the numbers on the multi-tap phone (sms) tool fram dcode.fr. 
I got `UMDCATFGJIDOOMULH HJAKFCARDSP`on the first run, wich was imprecise as expected, but I knew I was on the right track since I could read `UMDCTF`.

I did some manual listening and adjustments that gave me the numberes `8863222833344436666685554445533222277737777`
Wich gave me `ÙMDCTFidontlikecards`when decoded on dcode.fr.

Then I adjusted it to the described flag format in the description, and got the flag:
>UMDCTF-{i_dont_like_cards}
