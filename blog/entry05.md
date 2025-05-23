# Entry 5
##### 4/21/25

## Final Touches on Earsketch
Durnig the time of this blog, all of us are basically done with our Freedom Projects, and so when the time was nearing, it was also time for me to learn the final bits of my tool for the project, and to touch up on things.

### Making Songs Longer
One of the first, and honestly only things I did was to make the songs I made *longer*, as they needed to be at least 30 seconds to a minute long for the game to be finished. The plan was to make the music some sort of reward for the player after completing a level, since the game was kind of a platformer game combined with music happening. **So,** I decided to use the five songs I currenly had and make them longer, at least 30 seconds each, and a minute or more as the "Beyond MVP" for those songs. Due to all the skills I learned from working with Earsketch, making them longer was no problem, I just extended the lengths of the songs with repetition and longer time frames, plus I added some other effects to them as well.

*However*, making the songs longer **and** making it all sound well put together and nice was the hardest part of finishing the songs. It took a *long* time in order to make all the songs sound nice. I had to try out so many different sounds, combinations, effects, and even more additions to the songs in order for them to be coherently listenable. It took a rather *long* time to actually complete it for all of the songs, and at the end of the day, I managed to complete it all in time, which was great progress for the project. As a result, the codes for the songs turned out to be extremely long, but they were doable at the end of the day. Here is the code for [`random.js`](https://earsketch.gatech.edu/earsketch2/?sharing=6RUq-vYFHsDSki1kbHMugw) and [`house.js`](https://earsketch.gatech.edu/earsketch2/?sharing=6RUq-vYFHsDSki1kbHMugw):

```js
// random.js
setTempo(120);

//variables
var synth = TECHNO_SYNTHPLUCK_001
var drumSamples = Y18_DRUM_SAMPLES_2
var drums = Y01_DRUMS_1
var bass = Y11_BASS_1
var guitar = Y11_GUITAR_1
var edm = YG_EDM_PAD_5

//Music Section
fitMedia(synth, 1, 1, 5);
fitMedia(synth, 1, 8, 12)

fitMedia(drumSamples, 2, 2, 6);
fitMedia(drumSamples, 2, 7, 11);

fitMedia(drums, 3, 1, 5);
fitMedia(drums, 3, 8, 12);

fitMedia(bass, 4, 6, 10);
fitMedia(bass, 4, 12, 16)

fitMedia(guitar, 5, 11, 15);

fitMedia(edm, 6, 1, 5)
fitMedia(edm, 6, 7, 11)

var loud1 = analyzeTrack(4, RMS_AMPLITUDE)
var loud2 = analyzeTrack(3, RMS_AMPLITUDE)

if (loud1 > loud2) {
    setEffect(1, DISTORTION, DISTO_GAIN, 15)
} else {
    setEffect(2, DISTORTION, MIX, 1)
}

for (var measure = 1; measure < 9; measure++){
    fitMedia(EIGHT_BIT_ANALOG_DRUM_LOOP_001, 7, measure, measure + 1)
    fitMedia(EIGHT_BIT_ATARI_PAD_004, 8, measure +.5, measure + 1)
}

// house.js
setTempo(115);

//variables house
var housePiano = HOUSE_BREAK_FILL_001
var houseBreakbeat = HOUSE_BREAKBEAT_004
var houseDeepChord = HOUSE_DEEP_CRYSTALCHORD_003
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
    fitMedia(HOUSE_BREAK_FILL_002, 1, start, end)
    fitMedia(HOUSE_BREAKBEAT_022, 2, start, end)
    fitMedia(HOUSE_DEEP_CHORD_001, 3, start, end)
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
setEffect(1, FILTER, FILTER_RESONANCE, 1);
setEffect(2, DISTORTION, DISTO_GAIN, 5);
setEffect(3, EQ3BAND, EQ3BAND_HIGHGAIN, 15);
setEffect(4, COMPRESSOR, COMPRESSOR_THRESHOLD, -10);
setEffect(5, CHORUS, MIX, 0.5);
setEffect(6, BANDPASS, BANDPASS_RESONANCE, 0.9)
```
While it was a lot, at the end of the day I'm glad that I got to make these songs longer. 

## Finishing Up MVP
After that was done, me and Nancy spent time working together on what to do for the Freedom Project, especially over the break. 

### Adding some finishing touches
We were working on the game throughout the course of the year, so all we needed to do is add the finishing touches to the game, and the main finishing touch was the music. The problem was, Earsketch was more of a music creating/editing platform that uses code, so implementing the actual code from Earsketch is just going to make the game look weird, since it shows the actual editing platform when I tested it out earlier. So, we came up with the solution that the songs needed to be downloaded in order for the game to be completed. So, I ended up downloading the songs and sending them to Nancy, who helped implement the songs into the game, and we were good. I tested out the game, and I'd say it turned out to be pretty nice. The link to the game is [here](https://simrans4258.github.io/music-game), and overall, I'm so happy that I got to work together with Nancy to contribute to this very nice project.

## EDP
Currently we are on steps 5 and 6 of the Engineering Design Process, which is creating the prototype and testing and evaluating it. Since me and Nancy are done with the project, we just need to test out some things and see if we can improve it more, and then thats it really, as we are getting so close to making it Beyond MVP, and we are basically done with the MVP, which is great.

## Skills
Of course, when we were finishing up the freedom project, I learned a couple of skills along the way. Here are some skills I learned.

### Communication
The first skill I learned was that communication was key in order to create the best project you can make. Nearing the end of the date the MVP of our project was due, me and Nancy decided that the time was now to finally finish the project. We ended up communicating during the break as we had the most time available, and so we made sure that everything was on track according to our plan, made a few adjustments so the MVP could be met in time, and overall we worked together to finally finish up the project. Communication was key in finishing this project, and so I'm glad that me and Nancy were able to do it all in time.

### Balancing my work schedule
The second skill I learned was being able to balance my work schedule efficiently so I was able to contribute to the project enough while also being able to complete all my other assignments in time. While for good reason, most of my teachers decided to give me huge amounts of break work to do in order to prepare for things such as the AP Exams, and so it was **very tough** to go through. However, with timing all my tasks carefully, plus making sure to take breaks in the meantime, I was able to finish the project on time, so I was greatful for myself for being able to track all my assignments down rather nicely. At the end of the day, I'm proud of how the project turned out, and I'm looking forward of what's next for us.

[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
