# Entry 4
##### 3/10/25

## Learning Earsketch
During the time of this blog, I learned a lot about Earsketch, and I ended up working on the Freedom Project for a bit. Here are some things I worked on.

### Actually making good songs
I decided to keep on doing what I was doing before, and just continue on working on the same songs as before. But this time, I took longer than usual on Earsketch to make them sound good, like they were actual nicely produced songs. 

Here is the code for [`world.js`](https://earsketch.gatech.edu/earsketch2/?sharing=WlIuL5eON1uG6ilE5frDVg), which is very long, but is very much worth the effort to make it sound good, in my opinion. 
```js
setTempo(120);

var percussion = RD_WORLD_PERCUSSION_BASSWOODENTONE_1
var drum = RD_WORLD_PERCUSSION_DRUMPART_1
var mainDrum = RD_WORLD_PERCUSSION_DRUMSMAIN_2
var string = RD_WORLD_PERCUSSION_ETHNICSTRING_4
var glasstone = RD_WORLD_PERCUSSION_GLASSTONE_2
var kalimba = RD_WORLD_PERCUSSION_KALIMBA_PIANO_1
var wooden = RD_WORLD_PERCUSSION_WOODENGLASSDRUM_1

function sectionA (start, end) {
    fitMedia(percussion, 1, start, end)
    fitMedia(drum, 2, start, end)
    fitMedia(mainDrum, 3, start, end)
    fitMedia(string, 4, start, end)
    fitMedia(glasstone, 5, start, end)
    fitMedia(kalimba, 6, start, end)
    fitMedia(wooden, 7, start, end)
    fitMedia(RD_WORLD_PERCUSSION_PAN_FLUTE_2, 8, start, end)
}

function sectionB (start, end){
    fitMedia(RD_WORLD_PERCUSSION_BASSWOODENTONE_4, 1, start, end)
    fitMedia(RD_WORLD_PERCUSSION_DRUMPART_13, 2, start, end)
    fitMedia(RD_WORLD_PERCUSSION_DRUMSMAIN_5, 3, start, end)
    fitMedia(RD_WORLD_PERCUSSION_ETHNICSTRING_1, 4, start, end)
    fitMedia(RD_WORLD_PERCUSSION_GLASSTONE_1, 5, start, end)
    fitMedia(RD_WORLD_PERCUSSION_KALIMBA_PIANO_7, 6, start, end)
    fitMedia(RD_WORLD_PERCUSSION_WOODENDRUM_1, 7, start, end)
    fitMedia(RD_WORLD_PERCUSSION_PAN_FLUTE_1, 8, start, end)
}

var crash = RD_WORLD_PERCUSSION_DRUMPART_3
var crash_beat = "0-0-000-0-0-000"

for (var measure = 1; measure < 17; measure++){
    fitMedia(RD_WORLD_PERCUSSION_DRUMSMAIN_9, 9, measure, measure + 1)
    fitMedia(RD_WORLD_PERCUSSION_ETHNICSTRING_5, 10, measure + .5, measure + 1)
    makeBeat(crash, 11, measure + 1, crash_beat)
}

setEffect(1, TREMOLO, MIX, 1)
setEffect(2, TREMOLO, TREMOLO_FREQ, 7.5);
setEffect(3, TREMOLO, TREMOLO_AMOUNT, -10);
setEffect(1, TREMOLO, MIX, 1);
setEffect(4, DELAY, DELAY_TIME, 5)

sectionA(1, 5)
sectionB(5, 9)
sectionA(9, 13)
sectionB(13, 17)
```

Here is the code for the [`pop.js`](https://earsketch.gatech.edu/earsketch2/?sharing=sJofaPkVAFacF9qah6U0sw) song (so far).
```js
fitMedia(RD_POP_SFX_NOISESPIRAL_4, 1, 1, 3)
fitMedia(RD_POP_MAINBEAT_17, 2, 3, 5)
fitMedia(RD_POP_SOLODRUMPART_16, 3, 4, 6)
fitMedia(RD_POP_PADCHORD_2, 4, 1, 5)
fitMedia(RD_POP_SYNTHBASS_3, 5, 2.5, 6.5)
fitMedia(RD_POP_MAINBEAT_4, 3, 7, 11)
fitMedia(RD_POP_SYNTHBASS_9, 5, 8, 10)

setEffect(5, CHORUS, CHORUS_NUMVOICES, 2)
setEffect(3, DISTORTION, DISTO_GAIN, 10)

var question = "What tempo would you like for your music? Choose a number between 45 and 220";
var answer = readInput(question);

// converting to a number
var tempo = Number(answer);

// setting the tempo
setTempo(tempo);
```

## Freedom Project Progress
Now, its time to discuss what me and my partner, Nancy, had done for our freedom project so far, as we started to work on it a bit.

### What we had done so far
For the freedom project, we decided to make our own repo so it would be easier to git commit and push our changes together, and I decided to name it [music game](https://github.com/simrans4258/music-game), because that's what we were doing. So far, me and Nancy had begun making our freedom project, with me providing the songs for it (so far) and her coding buttons (so far).

### What's Next?
Considering during the time of writing this blog, we are learning p5js, we are going to continue making our freedom project as well as 

## EDP
Currently, I'd say that we are on step 5 of the Engineering Design Process, which is creating a prototype. Since me and Nancy are literally working on the game right now, I'd say that we are on the beginning of step 5. It may be little, but at least we are getting somewhere with this project, especially with the year passing by so fast.

## Skills
Of course, while learning a lot about my tool and working on the freedom project, I learned a lot of things along the way. Here are some skills I learned.

### Communication
One skill I learned while working on my tool and the freedom project for a bit is to communicate more, especially with people you have to work with. When me and Nancy had to start working on the Freedom Project, one downside is that we have no classes together this entire year, so we had no other choice but to communicate online in our free time outside of school. At first, it was hard, since we had to figure out times when we are both free, especially since we had other work from other classes to do, but we ended up making it work for some times, and so far, I'd say we are doing good thanks to communicating with each other. We just have to keep on doing that and it'll be good.

### Literally listening attentively
Another skill I learned while working on my tool is to actually listen to the songs very closely, to make sure if they sound good. When I listen to the song only on the first try, I first thought that that was good. But after I actually listened to it a couple of times, I realized that there was some tuning and adjusting needed to do for a lot of these songs. So, I ended up experimenting a bit until they became just right (for now). Considering how these songs are going to be used for the game, I need to make them as best as I can. Overall, it is very beneficial for me to learn these skills along the way of coding, and I'll continue to work hard on the freedom project so it can be really good for the final result.

[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
