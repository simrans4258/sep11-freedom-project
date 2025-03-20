# Entry 4
##### 3/10/25

## Learning Earsketch
During the time of this blog, I learned a lot about Earsketch, and I ended up working on the Freedom Project for a bit. Here are some things I worked on.

### Actually making good songs
I decided to keep on doing what I was doing before, and just continue on working on the same songs as before. But this time, I took longer than usual on Earsketch to make them sound good, like they were actual nicely produced songs. When I was reviewing my songs, I realized that while I made a couple of them, I still have a long way to go when it comes to actual production of music. No wonder why artists take so long to drop songs. This takes some time.

Anyways, I knew I had to do something with my tool to make it work for the freedom project, so I went straight to it. First, I decided to edit some songs I already made so they could be better than before. In order to do that, I decided to add more diverse effects to my songs, so that it could have better sounds and nicer flows to them. One such song is for my `world.js` song, which is the song with the highest amount of lines I believe. I made the song have change tracks so it would be more nicer to the ear, as I learned that having too much tracks can be overwhelming. Plus, I changed some of the measures in the for loop so that the tracks inside it can sound more smooth.

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
Speaking of adjusting songs, I decided to make a new song, `pop.js`, with a new genre to experiment to, which is pop, said in the title. Anyways, I ended up experimenting a lot with breaks in between tracks, as I learned from a youtube video [here](https://youtu.be/0MW6gJ_G1xk?si=dl7zBdmG0sDVsUMA), that adding breaks to your songs, and even deleting some tracks, can help improve the song greatly, and it really did. I applied that to most of my songs, but this one especially, since it was new.

I also added a new thing I haven't done before, for fun; asking the user what tempo they want in the song. Tempo is basically the beats per minute in a composition and is essentially the speed of a song. So, the more higher the number is, the more faster the song gets. It was really fun to experiment what different tempos do to the song, and how different tempos effect different genres of music. So, here is the code for the [`pop.js`](https://earsketch.gatech.edu/earsketch2/?sharing=sJofaPkVAFacF9qah6U0sw) song (so far).
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
Overall, I liked working on these songs, and I will continue to do so for our freedom project. I ended up enjoying myself while doing these songs a lot more than I expected, and I ended up learning a lot more about music composition as a result of being on Earsketch, which is pretty cool.

## Freedom Project Progress
Now, its time to discuss what me and my partner, Nancy, had done for our freedom project so far, as we started to work on it a bit.

### What we had done so far
For the freedom project, we decided to make our own repo so it would be easier to git commit and push our changes together, and I decided to name it [music game](https://github.com/simrans4258/music-game), because that's what we were doing.

We ended up communicating with each other more about what to do for our freedom project, as we needed to get started on this soon with the year passing by. However, the most convienient part about working together is that we ended up having different tools while working on the freedom project together. I have Earsketch, while she has Phaser. Essentially, we realized that our tools were actually coming along together just fine for the type of game we were working on, so our game will be find. 

So far, me and Nancy had begun making our freedom project, with me providing the songs for it (so far) and her coding buttons (so far). We ended up making a bit more than what I expected, but that was pretty good in the context of what time we had left. According to our plan, we ended up achieving our first steps. Making the start page, an alert, some songs we can use, instructions, and a few other things. While it is definetly not in the best shape for now, we are getting somewhere for sure. Its better than doing nothing at least.

### What's Next?
Considering during the time of writing this blog, we are learning p5js, we are going to continue making our freedom project according to our plan as well as implementing things we learned in our course to our game. It'll definetly benefit us in the long run. For me, I'm planning to make the songs I already have to be longer, the plan is about 3 minutes or a bit less. Once I finish with that, then I could possibly make more songs for the game, which would be pretty cool, if we have enough time. Overall, it'll be fun to work on this project, especially when we will be done.

## EDP
Currently, I'd say that we are on step 5 of the Engineering Design Process, which is creating a prototype, which is basically making the game itself. Since me and Nancy are literally working on the game right now, I'd say that we are on the beginning of step 5. It may be little, but at least we are getting somewhere with this project, especially with the year passing by so fast. I feel like step 5 will take a while to complete, but it'll be worth it at the end of the day.

## Skills
Of course, while learning a lot about my tool and working on the freedom project, I learned a lot of things along the way. Here are some skills I learned.

### Communication
One skill I learned while working on my tool and the freedom project for a bit is to communicate more, especially with people you have to work with. When me and Nancy had to start working on the Freedom Project, one downside is that we have no classes together this entire year, so we had no other choice but to communicate online in our free time outside of school. At first, it was hard, since we had to figure out times when we are both free, especially since we had other work from other classes to do, but we ended up making it work for some times, and so far, I'd say we are doing good thanks to communicating with each other. We just have to keep on doing that and it'll be good.

### Literally listening attentively
Another skill I learned while working on my tool is to actually listen to the songs very closely, to make sure if they sound good. When I listen to the song only on the first try, I first thought that that was good. But after I actually listened to it a couple of times, I realized that there was some tuning and adjusting needed to do for a lot of these songs. So, I ended up experimenting a bit until they became just right (for now). Considering how these songs are going to be used for the game, I need to make them as best as I can. Overall, it is very beneficial for me to learn these skills along the way of coding, and I'll continue to work hard on the freedom project so it can be really good for the final result.

[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
