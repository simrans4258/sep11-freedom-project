# Entry 2
##### 12/9/24

## Continuing Learning Tool
It's been around 2-3 months of learning my tool, Earsketch. I ended up learning *a lot* about the tool, especially since I had to use the javascript skills we had learned in class. So, here's some of the things I did/learned, and what my plans are for the upcoming winter break.

### Learning more elements
One of the main things I did while learning about my tool is just learning new things that are in Earsketch, and testing it out on other code editors, mainly [jsbin](https://jsbin.com/yayubolaze/edit?html,css,output). I did two jsbins for this actually, the one I linked before, and [this one](https://jsbin.com/woxajunela/1/edit?html,output). It took me a bit to figure out how to connect it to other code editors, but Earsketch was nice enough to provide a code block that not only connects Earsketch to other code editors, but it can also save future changes so you don't need to code on a new code editor, just sticking to Earsketch. How fun!

Anyways, one of the most important things I learned while using Earsketch is that the `fitMedia()` element is the **most** important thing to use if you want to input any sound into the music editor in the first place. I've been using it constantly to input many different sounds into Earsketch, and honestly, it works like a charm. You just have to assign them into different places so that the different tracks don't overtake one another, and it looks like this when you run the code for the music editor to show up. I also used the `setEffect()` element to put certain effects on tracks, like making it louder for example.
![image](https://github.com/user-attachments/assets/1ae608e7-5c6f-426a-a114-0213e27009cc)

One of the most prominent projects on Earsketch I did was some sort of recreation of Alicia Key's Underdog, as I thought it would be interesting to recreate that in Earsketch, since one, the sounds of it were free on Earsketch, since there's this collaboration going on between the company and other musicians, and two, I actually never heard of the song before, so why not do it blind? I just used the `fitMedia()` elements and `setEffect()` elements for it, since it was the first ever project I did on Earsketch, and to be honest it works well on it's own. Here's the [code](https://earsketch.gatech.edu/earsketch2/?sharing=MiQYCfFVzS1eXFgGYppkFg) below:
```js
// tempo: 
setTempo(90);

//808
fitMedia(AK_UNDOG_808_1, 1, 1, 43)
fitMedia(AK_UNDOG_808_2, 2, 1, 43)
fitMedia(AK_UNDOG_808_3, 3, 1, 43)
//bass
fitMedia(AK_UNDOG_BASS_1, 4, 1, 43)
fitMedia(AK_UNDOG_BASS_2, 5, 1, 43)
fitMedia(AK_UNDOG_BASS_3, 8, 1, 43)
fitMedia(AK_UNDOG_BASS_4, 9, 1, 43)
//guitar
fitMedia(AK_UNDOG_ACOUSTIC_GUITAR_1, 7, 1, 43)
fitMedia(AK_UNDOG_ACOUSTIC_GUITAR_2, 10, 1, 43)
//other instruments
fitMedia(AK_UNDOG_PIANO_1, 11, 1, 43)
fitMedia(AK_UNDOG_STRINGS, 12, 1, 43)
fitMedia(AK_UNDOG_CLAPS_SNAPS_1, 13, 1, 43)
fitMedia(AK_UNDOG_STOMP_1, 14, 1, 43)

// vocals
fitMedia(AK_UNDOG_OOHS_1, 6, 1, 5)
fitMedia(AK_UNDOG_LEAD_VOCALS_VERSE_1, 6, 6, 15)
fitMedia(AK_UNDOG_LEAD_VOCALS_PRE_CHORUS_1, 6, 15, 20)
fitMedia(AK_UNDOG_LEAD_VOCALS_CHORUS, 6, 20, 29)
fitMedia(AK_UNDOG_OOHS_2, 6, 30, 34)
fitMedia(AK_UNDOG_LEAD_VOCALS_VERSE_2, 6, 34, 43)

// effects
setEffect(1, VOLUME, GAIN, -20, 10, 5)
setEffect(1, VOLUME, GAIN, 1, 9, 5)
setEffect(6, VOLUME, GAIN, 3)
```

Of course, I also learned how to use other javascript elements into Earsketch, such as variables and conditionals, as I didn't just want to use the same type of elements for long. I used variables as alternatives for the sound names, as they are quite long, and I have to use them a couple of times sometimes. I used conditionals for sounds and certain beats to play. In fact, I haven't been using this commonly because at first, I thought it would be hard to input conditionals into Earsketch. But after realizing this only applied to certain stuff like to amplfy and analyze tracks, it was actually not that bad. This is [one example](https://earsketch.gatech.edu/earsketch2/?sharing=mMnc0kl_hpBlouIoSmUzQA) of this out of my *many* editors:
```js
// description: 
setTempo(120);

//variables
var synth = TECHNO_SYNTHPLUCK_001
var drumSamples = Y18_DRUM_SAMPLES_2
var drums = Y01_DRUMS_1
var bass = Y11_BASS_1
var guitar = Y11_GUITAR_1
var edm = YG_EDM_PAD_5

//Music Section
fitMedia(synth, 1, 1, 9);
fitMedia(drumSamples, 2, 1, 9);
fitMedia(drums, 3, 1, 9);
fitMedia(bass, 4, 1, 9);
fitMedia(guitar, 5, 1, 9);
fitMedia(edm, 6, 1, 9)

//conditional
var loud1 = analyzeTrack(4, RMS_AMPLITUDE)
var loud2 = analyzeTrack(3, RMS_AMPLITUDE)

if (loud1 > loud2) {
    setEffect(1, VOLUME, GAIN, -10)
} else {
    setEffect(2, VOLUME, GAIN, -20)
}
```

I also used functions in order to divide certain beats and sounds into sections of their own, so I could repeat them with each other without having to write the code again and again, so I'll definetly be using this more often. Making functions into Earsketch was actually more easier than I thought it would be. Here's a [code](https://earsketch.gatech.edu/earsketch2/?sharing=WlIuL5eON1uG6ilE5frDVg) of it below:
```js
// tempo: 
setTempo(120);

// variables:
var percussion = RD_WORLD_PERCUSSION_BASSWOODENTONE_1
var drum = RD_WORLD_PERCUSSION_DRUMPART_1
var mainDrum = RD_WORLD_PERCUSSION_DRUMSMAIN_2
var string = RD_WORLD_PERCUSSION_ETHNICSTRING_4
var glasstone = RD_WORLD_PERCUSSION_GLASSTONE_2
var kalimba = RD_WORLD_PERCUSSION_KALIMBA_PIANO_1
var wooden = RD_WORLD_PERCUSSION_WOODENGLASSDRUM_1

// functions
function sectionA (start, end) {
    fitMedia(percussion, 1, start, end)
    fitMedia(drum, 2, start, end)
    fitMedia(mainDrum, 3, start, end)
    fitMedia(string, 4, start, end)
    fitMedia(glasstone, 5, start, end)
    fitMedia(kalimba, 6, start, end)
    fitMedia(wooden, 7, start, end)
}

function sectionB (start, end){
    fitMedia(RD_WORLD_PERCUSSION_BASSWOODENTONE_4, 1, start, end)
    fitMedia(RD_WORLD_PERCUSSION_DRUMPART_13, 2, start, end)
    fitMedia(RD_WORLD_PERCUSSION_DRUMSMAIN_5, 3, start, end)
    fitMedia(RD_WORLD_PERCUSSION_ETHNICSTRING_1, 4, start, end)
    fitMedia(RD_WORLD_PERCUSSION_GLASSTONE_1, 5, start, end)
    fitMedia(RD_WORLD_PERCUSSION_KALIMBA_PIANO_7, 6, start, end)
    fitMedia(RD_WORLD_PERCUSSION_WOODENDRUM_1, 7, start, end)
}

sectionA(1, 5)
sectionB(5, 9)
sectionA(9, 13)
sectionB(13, 17)
```
Overall, it's been actually quite fun learning Earsketch and making a bunch of songs on it. And, I got to learn more about how music works, which is a very nice bonus! I definetly will learn more about Earsketch as time goes onto the Freedom Project.

### Plan for the Winter Break
So, what do I have to do during winter break, since we don't have school that time? Well, I plan to continue working on my tool, even if I'm not assigned it, and overall reviewing skills I learned, so that I won't forget during the break. I also plan to learn more javascript skills outside of Earsketch, more notably functions, conditionals, and loops, so I can input those skills onto Earsketch itself. Overall, I just have to learn more, take notes, and review my tool for the winter break. Not too much of course, because I want a break during the break, obviously.

## EDP
Currently I'm in steps 3 and 4 of the Engineering Design Process, brainstorming possible solutions and plan the most promising solution. Basically, I have solve my problem, which is making a music game, by learning more about my tool, which helps with music, and that leads me to learn the more complicated things about Earsketch since that seems like the most promising solution.

## Skills
I learned **a lot** of skills while learning about my tool. Here's just a few of them.

### Trying out new things
One skill I learned was to try out new things when it comes to something you are familiar with, my tool Earsketch in this case. At first, I was hesistant to try out the things we learned in Javascript into Earsketch because it seemed to work perfectly fine with only exclusive Earsketch elements. But after actually trying it out onto my code, I came to realize how much they actually matter when you want to make certain sounds, certain patterns, and much more. So I'll definetly keep testing out and trying all the things Earsketch has to offer.

### Trial and Error
Another skill I learned was to going through multiple trials and errors is a good thing to do in order to learn about your tool. When I was testing out conditionals, functions, and other new things, I was a bit confused, as at first those elements didn't work on Earsketch. I didn't know what I was doing wrong. But after reviewing my code and looking at the error messages Earsketch has, I came to realize not everything is compatable with each other in Earsketch. Some things in Earsketch, such as `analyzeTrack()` and `RMS_AMPLITUDE`, just belong to each other, and **only** to each other, at least what I know so far. I wouldn't know if I ignored it, so expect me to keep on making trials and errors along the way when learning about my tool.

[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
