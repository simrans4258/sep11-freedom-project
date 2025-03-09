# Tool Learning Log

## Tool: **Earsketch**

## Project: **Music Game with Javascript**

---

### 10/4/24:
* Experimented with the website on [Earsketch](https://earsketch.gatech.edu/earsketch2/)
  * found out it uses both python and javascript
* found a beginner [tutorial](https://www.youtube.com/watch?v=NtaGTRA48ms)
  * this uses python but it is really similar
* need to know how to connect it with other things like jsbin and not just on the website

### 10/13/24:
* tested on [Earsketch](https://earsketch.gatech.edu/earsketch2/?sharing=MiQYCfFVzS1eXFgGYppkFg) more
  * experimented with effects more
* watched this video (https://www.youtube.com/watch?v=-pkS95U8zRg)
* found out there is a block mode for earsketch, can make things easier

### 10/20/24:
* decided to create Earsketch account on the website to see what happens
* found the [Earsketch Channel](https://www.youtube.com/channel/UCqtFcjm-0WMCxl0y-m87EuQ)
  * have 7 tutorial videos on their channel, not many views though
* found out they have a [Cirriculum Section](https://earsketch.gatech.edu/earsketch2/?curriculum=/en/v2/unit-1&language=javascript) in the editor so you can learn while doing the code
  * need to learn more about effects and other types of things on Earsketch, not just adding sounds
* How can I be able to use EarSketch outside of it's website?

### 10/26/2024:
* learned how to share code with [Earsketch](https://earsketch.gatech.edu/earsketch2/?sharing=MiQYCfFVzS1eXFgGYppkFg)
  * I learned how to input sounds into the music editor and what a tempo is
  * Also learned how to do effects, such as gaining audio for example
  * learned to input `var` and making beats
  * Am I able to use functions and even more javascript elements in Earsketch, or only a few are applicable here?
 
### 11/4/2024:
* ended up connecting my current Earsketch code to [jsbin](https://jsbin.com/woxajunela/1/edit?html,output)
  * the code shows up on the output of jsbin, which is interesting
  * can't edit the code on jsbin, but it's connected to Earsketch
  * if you edit on Earsketch then reload the jsbin page, then it shows up
* if you hide both the DAW (digital audio workstation) and the code, then it only shows the play button, but it still works
* I want to see if I am able to hide the whole code, but it is still able to produce sounds

### 11/9/24:
* started a new [Earsketch](https://earsketch.gatech.edu/earsketch2/?sharing=mMnc0kl_hpBlouIoSmUzQA) code to match with what the cirriculum says, plus to test out new sounds available in the program
  * learned that conditionals can work well with Earsketch as you can manipulate which tracks you want to be louder or less louder than others easier than manually do it
  * also used variables a lot, which makes writing names for sounds more easy, especially if you have to use them constantly and/or if those names are quite long, which are a lot
    * though the names automatically fill for you in Earsketch, it is convenient to use variable names to make things easier for you, which is how javascript works
* added new code in [jsbin](https://jsbin.com/yayubolaze/edit?html,css,output)
  * added css and divs to make it look more pretty, but can't change the code itself, only what's around it
  * both of them can be played at the same time and the sounds overlap with each other
  * How can I make it not show while still playing the sound? Can it connect to other regular javascript code too?
 
### 11/18/24:
* experimented with new code on [Earsketch](https://earsketch.gatech.edu/earsketch2/?sharing=6RUq-vYFHsDSki1kbHMugw)
  * inplemented functions and for loops in order to make repeated music/code more easy to manage, and it was, as it heavily shortened the code I needed to do, I just needed to call parameters and such
  * also used the `makeBeat` element to make nice beats to a track in the loop
* used conditionals for this [code on Earsketch](https://earsketch.gatech.edu/earsketch2/?sharing=mMnc0kl_hpBlouIoSmUzQA)
  * used `analyzeTrack` as it works best with conditionals on Earsketch
  * works pretty well and sounds nice, but it doesn't work sometimes on other code when I try it, I should try to see the problem later
* updated some code on Earsketch and it shows up on [jsbin](https://jsbin.com/kopusibawu/edit?html,css,output)
* How much can I alter sounds using things such as `makeBeat`, `analyzeTrack`, `setEffect`, and more?

### 11/22/24:
* altered the first [Earsketch project](https://earsketch.gatech.edu/earsketch2/?sharing=MiQYCfFVzS1eXFgGYppkFg)
  * just put `fitMedia`, as it works just fine on that, but I feel like other elements of javascript can be implemented, it just takes a lot of editing to do
* also did new code surrounding [world music](https://earsketch.gatech.edu/earsketch2/?sharing=WlIuL5eON1uG6ilE5frDVg)
  * Used a lot of functions for that one, as it made it sound nicer than before
* the code updated on [jsbin](https://jsbin.com/yayubolaze/edit?html,output)
* I wonder how can I implement more javascript elements without making it too complicated, since Earsketch can hold up on its own

### 12/2/24:
* edited some code for [random Earsketch project](https://earsketch.gatech.edu/earsketch2/?sharing=mMnc0kl_hpBlouIoSmUzQA)
  * added a `for` loop in order to repeat specific tracks/beats, and it works pretty well
  * the repetition works on the track itself, so it repeats a track a certain amount of times on the music editor if it's less than or equal to the track end, since you always have to declare the `var` to 1, since it's equal to the track number
* i also come to understand beats more now, since I listened to them, and you basically put numbers and dashes in a string which all represent steps, the numbers are the sounds, the dashes are the breaks
* it shows up on [jsbin](https://jsbin.com/yayubolaze/edit?html,css,output), as I made sure the jsbin code saves future changes as well
* I plan to use the `for` loops more often now, as it makes code more easy and pretty to look at, especially repetitions, plus I'll use more beats to add flare to the music

### 12/26/24: 
* used more `setEffect()` for my code editors, to make the tracks sound more unique and nice
  * for [the house](https://earsketch.gatech.edu/earsketch2/?sharing=6RUq-vYFHsDSki1kbHMugw) one, I used EQ3BAND, which basically helps adjust the volume for the tracks and amplifies it more
  * for [the world](https://earsketch.gatech.edu/earsketch2/?sharing=WlIuL5eON1uG6ilE5frDVg) one, I used TREMOLO, which makes a wobbly sound effect for the tracks
  * for [the Underdog](https://earsketch.gatech.edu/earsketch2/?sharing=MiQYCfFVzS1eXFgGYppkFg) one, I used CHORUS, which makes vocals and other sounds have some sort of ensemble to it, by repeating and amplifying vocals
  * used DISTORTION for [this one](https://earsketch.gatech.edu/earsketch2/?sharing=mMnc0kl_hpBlouIoSmUzQA)
* added and adjusted the for loop for the world.js one so that it could fit the music better
* will work on how to make the functions and loops more connected with each other, just like we did in regular javascript lessons

### 1/12/25:
* worked on [the world](https://earsketch.gatech.edu/earsketch2/?sharing=WlIuL5eON1uG6ilE5frDVg) one
  * added some more tracks that fit the theme of the song
  * added some more effects (used the TREMOLO and DELAY effects)
* also worked on [the house](https://earsketch.gatech.edu/earsketch2/?sharing=6RUq-vYFHsDSki1kbHMugw) one
  * added one more track
  * adjusted all the effects so it could all be different (used FILTER, DISTORTION, BANDPASS, and more)
* will probably use effects more often, and maybe more variables

### 2/24/25:
* I learned more about beats, and how to use for loops more efficiently
  * learned how beats are made, as you have to put a sequence of numbers/signs, such as `00--000` or `---1----` for example
  * also learned more about for loops and its use for repitition
* will keep these two skills in mind, and will use them more for more songs to make

### 3/2/25:
* changed some things about [`world.js`](https://earsketch.gatech.edu/earsketch2/?sharing=WlIuL5eON1uG6ilE5frDVg)
  * removed some tracks from the song to make it sound better
  * did the same for [`random.js`](https://earsketch.gatech.edu/earsketch2/?sharing=mMnc0kl_hpBlouIoSmUzQA)
* earsketch has now color coded arrows on tracks so you can track down which ones are playing, which is very convienient
* made a new code, [`pop.js`](https://earsketch.gatech.edu/earsketch2/?sharing=sJofaPkVAFacF9qah6U0sw), to experiment with new sounds and genres
  * used `setEffect()` and `fitMedia()`, which are the basics, in order to make it
  * decided to do different type of format to see how it sounds, plus to add more tracks
  * will experiment with this more
* will make the music for the Freedom Project, and will figure out how to input audio only
  * found out that I can download the music I made as not just code script, but as mp3 and wav files
  * will use this to input the audio for the game

### 3/7/25:
* changed many things about [`pop.js`](https://earsketch.gatech.edu/earsketch2/?sharing=sJofaPkVAFacF9qah6U0sw) script
  * removed a lot of unnecessary tracks and replaced them with new ones to free up some space in the song/not overwhelm it
  * used different effects to check different sounds the tracks make with them (not too much though)
  * tried out user input, where theres an alert for the user to change the tempo between a certain range (inspired by the cirriculum)
* edited a bit more for [`random.js`](https://earsketch.gatech.edu/earsketch2/?sharing=mMnc0kl_hpBlouIoSmUzQA)
* made a new song, [`rnb.js`](https://earsketch.gatech.edu/earsketch2/?sharing=_gGHsvc6BDkde-hPHHbgDw)
* will continue to make and experiment with new songs for freedom project

<!-- 
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
