# Entry 3
##### 2/3/25

## What I learned over the Break

### More elements
Text

I did all of this for the `house.js` code:
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

And I did all of this for the code of `random.js`:
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
    setEffect(1, DISTORTION, DISTO_GAIN, 20)
} else {
    setEffect(2, DISTORTION, MIX, 1)
}

var crash = Y01_CRASH_1
var crash_beat = "0-0-000-0-0-000"

for (var measure = 1; measure < 9; measure++){
    fitMedia(EIGHT_BIT_ANALOG_DRUM_LOOP_001, 7, measure, measure + 1)
    fitMedia(EIGHT_BIT_ATARI_PAD_004, 8, measure +.5, measure + 1)
    makeBeat(crash, 9, measure, crash_beat)
}
```

### Did I do enough?
So, after reviewing the editing I did in Earsketch and what I actually inputed in my learning log, I have to say that I didn't do as much as I thought I would, but I feel like I learned enough 

## EDP

## Skills
Of course, I ended up learning a lot of skills along the way of learning about my tool. Here are two skills I learned while learning my tool over the break. 

### Keeping track of what I learned


### Trying out new things


[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
