# Entry 2
##### 12/9/24

## Continuing Learning Tool
It's been around 2-3 months of learning my tool, Earsketch. I ended up learning *a lot* about the tool, especially since I had to use the javascript skills we had learned in class. So, here's some of the things I did/learned, and what my plans are for the upcoming winter break.

### Learning more elements
One of the main things I did while learning about my tool is just learning new things that are in Earsketch, and testing it out on other code editors, mainly [jsbin](https://jsbin.com/yayubolaze/edit?html,css,output). I did two jsbins for this actually, the one I linked before, and [this one](https://jsbin.com/woxajunela/1/edit?html,output). It took me a bit to figure out how to connect it to other code editors, but Earsketch was nice enough to provide a code block that not only connects Earsketch to other code editors, but it can also save future changes so you don't need to code on a new code editor, just sticking to Earsketch. How fun!

Anyways, one of the most important things I learned while using Earsketch is that the `fitMedia()` element is the **most** important thing to use if you want to input any sound into the music editor in the first place. I've been using it constantly to input many different sounds into Earsketch, and honestly, it works like a charm. You just have to assign them into different places so that the different tracks don't overtake one another, and it looks like this when you run the code for the music editor to show up. 
![image](https://github.com/user-attachments/assets/1ae608e7-5c6f-426a-a114-0213e27009cc)

I also learned how to use other javascript elements into Earsketch, such as variables and conditionals. I used variables as alternatives for the sound names, as they are quite long, and I have to use them a couple of times sometimes. I used conditionals for sounds and certain beats to play. This is one example of this out of my *many* editors:
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

var loud1 = analyzeTrack(4, RMS_AMPLITUDE)
var loud2 = analyzeTrack(3, RMS_AMPLITUDE)

if (loud1 > loud2) {
    setEffect(1, VOLUME, GAIN, -10)
} else {
    setEffect(2, VOLUME, GAIN, -20)
}
```

### Plan for the Winter Break
So, what do I have to do during winter break, since we don't have school that time? Well, I plan to continue working on my tool, even if I'm not assigned it, and overall reviewing skills I learned, so that I won't forget during the break. I also plan to learn more javascript skills outside of Earsketch, more notably functions, conditionals, and loops, so I can input those skills onto Earsketch itself. Overall, I just have to learn more, take notes, and review my tool for the winter break. Not too much of course, because I want a break during the break.

## EDP
Currently I'm in steps 3 and 4 of the Engineering Design Process, brainstorming possible solutions and plan the most promising solution. Basically, I have solve my problem, which is making a music game, by learning more about my tool, which helps with music, and that leads me to learn the more complicated things about Earsketch since that seems like the most promising solution.

## Skills
I learned **a lot** of skills while learning about my tool. Here's just a few of them.

### Trying out new things
One skill I learned was to try out new things when it comes to something you are familiar with, my tool Earsketch in this case.

### Trial and Error
Another skill I learned was to going through multiple trials and errors is a good thing.

[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
