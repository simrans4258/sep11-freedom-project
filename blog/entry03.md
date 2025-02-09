# Entry 3
##### 2/3/25

## What I learned over the Winter Break
Ever since the few weeks that winter break was over, I've learned a lot about my tool during that time, and while it's been some time, here are some of things I learned about Earsketch during Winter Break, and even more.

### More elements
First, I ended up learning **a lot** about what Earsketch has to offer and other things I haven't learned before while trying to figure out my tool. I especially learned more about how to adjust sounds and tracks in Earsketch, so that the songs don't just have to rely on the tracks alone to make things sound nice, I could add *more* to it.

When I was discovering new things about Earsketch, I stumbled upon the `setEffect()` element of Earsketch, which basically lets you put effects on the tracks to make it sound more better, depending on what you choose. It's pretty self-explanatory, the more you think about it. At first, I only used like 1 or 2 effects because I was comfortable with those effects, but after seeing the list on Earsketch, I decided to give out more a try. Here are some I used: 
* EQ3BAND, which basically helps adjust the volume for the tracks and amplifies it more
* TREMOLO, which makes a wobbly sound effect for the tracks
* CHORUS, which makes vocals and other sounds have some sort of ensemble to it, by repeating and amplifying vocals
* DISTORTION, which is self-explanatory
* DELAY, which is also self-explanatory
* and much more!

I used all of those effects across my codes, such as for [`world.js`](https://earsketch.gatech.edu/earsketch2/?sharing=WlIuL5eON1uG6ilE5frDVg), which turned out quite nice I'd have to say. I ended up using only some of the effects I listed above, plus a few others, but for this code, it was enough for me. At least, as of now, I might change it later the more I experiment with both javascript and Earsketch.

However, I did ended up using **a lot** of effects for my `house.js` code, as house music traditionally has a lot of effects added to it to make the music sound nice. So at the end of the day, I did all of **this** for the [`house.js`](https://earsketch.gatech.edu/earsketch2/?sharing=6RUq-vYFHsDSki1kbHMugw) code. It's quite *long*, longer than I thought it would, but it's the effort that counts:
```js
// Setup Section
setTempo(115);

//variables house
var housePiano = HOUSE_ACOUSTIC_PIANO_001
var houseBreakbeat = HOUSE_BREAKBEAT_001
var houseDeepChord = HOUSE_DEEP_AIRYCHORD_001
var houseBass = HOUSE_DEEP_BASS_001

// sectionA
function sectionA(start, end) {
    fitMedia(housePiano, 1, start, end)
    fitMedia(houseBreakbeat, 2, start, end)
    fitMedia(houseDeepChord, 3, start, end)
    fitMedia(houseBass, 4, start, end)
    fitMedia(HOUSE_DEEP_ARPLEAD_001, 5, start, end)
    fitMedia(HOUSE_BREAK_FILL_001, 6, start, end)
}

//section B
function sectionB(start, end) {
    fitMedia(HOUSE_ACOUSTIC_PIANO_002, 1, start, end)
    fitMedia(HOUSE_BREAKBEAT_002, 2, start, end)
    fitMedia(HOUSE_DEEP_AIRYCHORD_002, 3, start, end)
    fitMedia(HOUSE_DEEP_BASS_002, 4, start, end)
    fitMedia(HOUSE_DEEP_MOOGLEAD_008, 5, start, end)
    fitMedia(HOUSE_BREAK_FILL_004, 6, start, end)
}

//calling functions
sectionA(1, 11)
sectionB(11, 21)
sectionA(21, 31)
sectionB(31, 41)

// for loops
var beat = "0-0--00----000--0-0"
for (var measure = 1; measure > 41; measure++){
    makeBeat(HOUSE_DEEP_BASS_001, 5, measure, beat)
}

// effects
setEffect(1, FILTER, FILTER_RESONANCE, 0.5);
setEffect(2, DISTORTION, DISTO_GAIN, 5);
setEffect(3, EQ3BAND, EQ3BAND_HIGHGAIN, 15);
setEffect(4, COMPRESSOR, COMPRESSOR_THRESHOLD, -10);
setEffect(5, CHORUS, MIX, 1);
setEffect(6, BANDPASS, BANDPASS_RESONANCE, 0.9)
```
As you can see, I also used functions and for loops for the code, which leads me to my next point. After experimenting with Earsketch for a while, I came to realize how using functions makes repeating tracks **much more** easier to manage, as I can just put the tracks in a function, set the parameters as the start and the end of tracks, and just repeat that a number of times for the code. Not only did it make cool patterns in the music, but it also can be reminiscient of how music sounds in general, which is pretty cool.

Finally, I learned how to use for loops and conditionals for my code. While admittedly, I haven't used them **as much** as the rest, I still found a use for them in some way. The for lops are pretty self-explanatory, it helps give repetition to your code, and it makes certain sounds easier for you to input without having to repeat them multiple times manually. Conditionals help compare sounds/tracks to each other and play a certain type of beat. Considering how these two skills are *fundamental* in javascript, I plan to use them way more in the future.

However, that doesn't mean I haven't used them at all. I tested out conditionals and for loops for some of my codes, and while it took some trial and error, I *finally* got some to work. I inputed those skills specifically for the code of [`random.js`](https://earsketch.gatech.edu/earsketch2/?sharing=mMnc0kl_hpBlouIoSmUzQA) I used variables, a conditional, and a for loop for this code, but there *could* be more to it coming to the future. But I like what I have so far:
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

// loud
var loud1 = analyzeTrack(4, RMS_AMPLITUDE)
var loud2 = analyzeTrack(3, RMS_AMPLITUDE)

if (loud1 > loud2) {
    setEffect(1, DISTORTION, DISTO_GAIN, 20)
} else {
    setEffect(2, DISTORTION, MIX, 1)
}

// crash
var crash = Y01_CRASH_1
var crash_beat = "0-0-000-0-0-000"

for (var measure = 1; measure < 9; measure++){
    fitMedia(EIGHT_BIT_ANALOG_DRUM_LOOP_001, 7, measure, measure + 1)
    fitMedia(EIGHT_BIT_ATARI_PAD_004, 8, measure +.5, measure + 1)
    makeBeat(crash, 9, measure, crash_beat)
}
```
I figured at the end of the day that the goal of Earsketch is just to make some good music and to vibe with it. I ended up playing this code *multiple* times because of how catch it was (at least in my opinion). I don't want to praise myself **that** much, but I'd say that I did a decently good job with figuring out how sounds and effects work in Earsketch, and managing to make the songs I made in Earsketch sound x10 better than it was before. I'll defintely be learning more later on.

### Did I do enough?
So, after reviewing the editing I did in Earsketch and what I actually inputed in my learning log, I have to say that I didn't do as much as I thought I would, but I feel like I learned enough to move forward. Currently checking on my learning log, I have to be honest here, I literally only written down one day, for whatever reason. 

I feel like due to other assignments and chores I had to do over the winter break, and me just wanting to **finally** have a break in general from school, I didn't write down as much days than I wanted to. But, I did some learning without actually writing it down the learning log, like testing my code for example. So overall, while I didn't write as much as expected, I feel like I learned enough. And I'll definetly do more in the future.

## EDP
Currently, I'd say I'm at step 4 of the Engineering Design Process, which is planning the most promising solution to my problem, which is basically just learning my tool for my game. I feel like I still have a long way to go with just learning, as there's definetly way more components to making a game involving music, but I feel like I'm getting somewhere, as I'm halfway there.

## Skills
Of course, I ended up learning a lot of skills along the way of learning about my tool. Here are two skills I learned while learning my tool over the break. 

### Keeping track of what I learned
One skill I learned was to keep track of what I had learned throughout the course of figuring out Earsketch. While I didn't write **that much** than I figured for the learning log, I did keep track of what I had in my code throughout my learning of Earsketch. I ended up remembering things more out of the top of my head the more I kept doing it, and I spread out those skills throughout my multiple pieces of code to experiment a little, and it all worked out at the end. So that was a pretty good skill to keep in mind, just keep track.

### Trying out new things
Another skill I learned while learning about Earsketch is to try out new things, even if they seem scary to you. At first, I was hestitant to learn more about the things Earsketch has to offer, because I was okay with sticking with the things I know, as Earsketch seems to work fine with it. However, as I started to try out other stuff on Earsketch, I ended up realizing *how much* I was missing out about Earsketch by ignoring it instead of trying it. So I'll definetly keep using this skill in the future.

[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
