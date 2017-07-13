# 100 Days Of Code - Log

### Day 29: July 11, 2017

**Today's Progress**: While reading through You Don't Know JS' chapter on [closures](https://github.com/getify/You-Dont-Know-JS/blob/master/scope%20%26%20closures/ch5.md), I found some interesting details in the section regarding closures and loops. I think this might go some way toward explainaing some of the sequence display issues I had in the Simon game, and possibly the scope errors in the word counter. Interesting reading.

Now back to the game. The user clicks are working but the game needs to stop them once the user is done with the current sequence (or makes a mistake, when I get to implimenting strict mode). Set it up to remove the active class from the lights once the sequence length is reached - works just fine. No code yet to handle restarting/strict mode on errors, but that can come later.

I now have a reasonably working game, but it only runs with a set sequence of three presses. Next big step - get it working as a proper game, one sequence at a time. Moved the whole playing code, apart from generating the sequence at the start, to its own function. I still only have a hazy idea of what is to happen, but I'm imagining it working similar to the word counter, calling itself again when done. Created a counter to show what round of the game the player is on, and got it to display in the on screen counter.

Thinking about getting the function to call itself again. I can't easily put in a delay as I have no means of knowing how long the current round is going to take. But I do have code to handle finishing the user's inputs, which is dependent on the user's click - I can just re-call the function there. This seems to work, though now I have to make sure the code inside the play function isn't so static. As expected the biggest issue is the timing for making the lights active. They need to be set to active as soon as the page is done demonstrating the sequence, so I need to determine the number sequence to use to calculate the delay. Wrote down the round number/delay sequence and paper which helped me to work it out. Tested it, but the timing still isn't right.

Looked around at the program flow with the console - I think it's somewhere in the user click, or re-calling the play function. It seems to be re-calling play() even when the user counter isn't done. I think this may be similar to the issue I had with the word counter, but globally declaring the current round variable didn't help. I'm just going to have to keep looking and breaking things down until I find the answer...

**Thoughts:** I'm over a quarter of the way done now and honestly I feel like it's going too fast! The end is going to come sooner than I thought. Maybe I'll try a round two afterwards... 200 days of code?

Starting to worry about how tangled the Simon code is - feels like it's bouncing around and passing things all over the place. Trying not to worry about it until I have the whole game functional, though. I'm still only on the basics - I don't know what it'll be like later. (Later note - already feels somewhat improved by putting the light switch/click functions inside the main play function?)

Moving on to getting the game working as a proper game is intimidating - it means taking what I have now and adding a whole new layer onto it. Things will likely break. That's ok. I can handle this.

And really, it went better than I thought. Sure there's a few confusing bits and some very broken parts, but the game is starting to act more and more as it should do. It's a very satisfying feeling.

### Day 29: July 11, 2017

**Today's Progress**: I had planned to work on the Simon game but couldn't get a chance to sit down with it, so I worked on the word counter challenge. Added a progress bar to track how far the user is through the challenge - it animates every time the user finishes a section. Also added a toggle to switch the bar on or off so the user can choose whether or not to see it.

**Thoughts:** Maybe it was a good thing to take a break on the Simon game - I don't want to stop working on it, but sometimes you gotta step back.

The word couter is feeling very simple and relaxing in comparison, but that's no bad thing. I'm glad to be doing some personal work on this scale as well. FCC's challenges are excellent for learning, but there is a lot to be said for seeing somethig in your own life that you can solve with code, and then going out and doing it!

**Link to work:** [A Word Crawl for the Motivationally Challenged!](https://codepen.io/jsanderson/pen/EXdPey)

### Day 29: July 11, 2017

**Today's Progress**: Did some reading up on aspects of JS I had been asked about but didn't know much about - event propagation/bubbling, promises, and closures. I have a somewhat better grasp of them now but would like to do some actual work with them before I'd feel comfortable saying I understood them. I'm very much a learn by doing sort of person.

For now, back to the Simon game. I've added another timeout on my test game and set it up so that when it is the user's turn, the lights get an 'active' class in that timeout. The function that register's a user's click then only actives when the light has that class. Now I need to make sure that function will do something.

First of all, the light has to switch back on. Copied over the code from the original light switch - it switches on but the timer isn't quite right for switching it off. Admittedly I'm not fond of repeating the code so I think I'll take a different approach. If I put the clicked light's id into an array (which I was going to do anyway) then I can just call the original light switch function using that, giving it the last item in the user sequence array each time. That seems to work, but it looks like I'll need to restructure how the delays are calculated in the light switch function. Currently they're calculated based on the position of the array - good for the computer, not for a user who doesn't want to wait an increasing number of seconds to see feedback from their click. Added a new parameter to say if the function is being called for the computer or the user, and a couple of ternaries to set the delays accordingly. Running smoothly again.

Next up is to compare the user's inputs to the pregenerated sequence. Set up a comparison - nothing special, just displaying a message in the document to say if the click was right or wrong. But it shows the comparison works - something to build on later. I'll probably end up putting the user click handler in its own function that calls itself until the user is done with the current sequence length, rather as I did with the word counter. I think that will be the next step.

**Thoughts:** "I don't know" is a powerful thing to say sometimes, because admitting you don't know something also means you know what to learn, so that you do.

I'm not sure I'm happy with adding more timeouts to this game - got a feeling somewhere along the line something will collapse. We'll see if I'm right or just worrying over nothing.

I wonder if I go on too much here? Or is that a good thing? It's kind of motivating to record my thoughts as I work...

### Day 28: July 10, 2017

**Today's Progress**: Timing is not going well on the Simon game. It still seems to be only showing the final sequence even when I try to make it go through the steps one at a time. I wonder if what I learnt yesterday on the word counters will help. At the moment I'm not worrying about the DOM, just logging the sequence to the console step by step to check it's working. For some reason putting a timeout on the logging causes it to delay correctly, but with the final sequence each time. Hmmmm.

Maybe I need to look at this from another angle. Instead of generating each step on the fly, why not generate the whole thing and then only show what needs to be shown? That seems like it would solve a lot of timing issues, no need to worry about making the program wait to generate the next part of the sequence.

Done that and it seems a lot tidier. Thinking now about having the game show the sequence. I'm worrying too much about it showing the sequence length of one, then two, then three... all in one go, which the game isn't ever going to do! It's going to wait for the user to input their sequence - so why am I worrying over something that the game won't need to do? Time to stop that and get working on user input.

Of course here is another timing problem - my test user input doesn't wait for the game to stop showing the sequence. And I don't want to assume the user is going to sit and wait for the sequence to finish before they start pressing buttons. That would be lazy, and I've resisted laziness once on this project. Not going to give in now.

**Thoughts:** I think this is another 'I don't know anything' days. But I had one of those last week, and I made it through, so why should this be any different?

Looking at yesterday and the day before, doing the word counter webapp was some good timing. Both setups involve the page waiting for user input, and I think I learnt a lot about each one from the other. I didn't mean for that to come together so well, but it definitely worked out.

Once again, I need to give the brain a rest every once in a while and look for simple solutions.

### Day 27: July 9, 2017

**Today's Progress**: I fixed the problem with the word counter. Another simple solution, just have the counter iterate when the user presses the 'done' button to show they're finished with their chunk, and call the text handler with the new counter value. Added some code to the text handler to break out if the goal list is done, which so far just displays an alert but will get expanded on once I prettify everything.

Testing it out, I ran into problems with the page accepting wordcounts lower than the given goal. Couldn't work out why - the goal variable was exactly what it should be, but the page kept acting as if it was 10 (the first goal) every time. Thought it might be a scope error and declared the goal variable at the top of the script instead. Sure enough, everything started working as it should.

Tested it out again. The code to handle ending the challenge when the last goal is reached isn't quite working - found out it wasn't breaking out of the text handler properly, fixed that.

Everything seems to be holding up! I need to prettify the page now, maybe add an optional progress bar, all that fancy stuff, but the meat of the thing is there.

**Thoughts:** If there's one thing I've learnt over the last few days, it's that I have a bad habit of looking for big, complex solutions where small, simple ones exist. I need to kick that. Not sure how except for distancing myself for a bit. I actually thought of having the text handler call itself while falling asleep last night...

I would like to understand more about why the scope error occured as it did. I knew enough to fix it when I suspected that was what was going on, but I don't feel I really grasp why it acted as it did. That's something I'd like to read up on. I have been flicking through You Don't Know JS lately, I'm wondering if I'll get some understanding there. The why is as important as the how.

**Link to work:** [A Word Crawl for the Motivationally Challenged!](https://codepen.io/jsanderson/pen/EXdPey)

### Day 26: July 8, 2017

**Today's Progress**: Updated one of my gallery sites, but I also want to do something meatier than just personal site work when I'm away from my FCC challenges. So I picked up on a project I wanted to start which was a webapp for a popular NaNoWriMo motivational thread ('A Crawl for the Motivationally Challenged!'). The thread challenges you to write chunks of words, none of which is any more than 200 words at a time, which build up and leave you with just over 3,000 words at the end. For a while now I've wanted to do a webapp that counts your words as you type and shows your progress throughout the challenge. A bit like the web version of [Write or Die](http://writeordie.com) without the timer. (Though I guess I could add a timer if people wanted, but let's not get ahead...)

Thankfully I had some existing [word counters](https://codepen.io/jsanderson/pen/RoxOPM) which I'd already modified for an implimentation of the [50 Headed Hydra](https://codepen.io/jsanderson/pen/pNKrzL0) challenge, so modifying it to work on a new page was easy work. I've gotten a working version but so far it only works on the first step of the challenge (10 words). I'm considering how to make it go through each one of the steps in turn. For any other language I'd just use a loop, but I don't know if I can pause JS to wait for the user to write their words before moving on to the next step. All that work on the Simon game has helped me with JS timing, but I don't know how long it will take for the user to write, so I can't hard code that. I may just have to make the wordcounter its own function and keep calling it for each step, but I'm unsure if that's a satisfactory solution. The timing issue is still there too. Each step needs to follow on from the user's input...

**Thoughts:** Yeah, I admit it, when I'm home my motivation goes waaaay down. This isn't good! I'm glad to be being a bit less lazy. Sure those personal sites had work that needed to be done, but once it's done I can't waffle on them forever.

### Day 25: July 7, 2017

**Today's Progress**: Actually did some coding in work, just a few VBA macros, but it felt very fulfilling anyway. Now back to the Simon game. The code that pushes light values ('red', 'yellow', 'blue' or 'green') is still a bit buggy, sometimes nothing goes into the array. Turns out it was just an issue with the switch statement not being written correctly, nothing big or difficult.

Now that the game can generate random sequences it needs to keep on doing so, adding on to the next step and displaying where it is in the sequence. Moved the 'light switch' (the part that handles the lights turning on and off) to its own function, and the rest into a while loop (it probably won't stay there, but I want to check it can generate new additions to the sequence twenty times, so it will do for now).

After making sure everything's getting passed around correctly, everything seems to work! (I hope...) I've got the sequence displaying in the console as well to test it, but of course the problem with that is it appears instantly (or as close as can be to human eyes). And I want the current length to be visible on the game so the player can see where they are. Added a small div to the page that initially displays 0 and increments each time a new sequence is displayed.

Unfortunately it seems as if the sequence isn't running quite as I thought it would. It looks like instead of displaying each step in the process, it just skips straight to step 20. I'm not sure how or why (suspect it's another timing error) but that's where flowcharts come in again. Suspect the problem is that while the 'light switch' has all its delays set up ok, the for loop that calls it has no delay. So I need to know how long each iteration of the sequence needs to display by and delay the execution of the light switch by that amount.

**Thoughts:** A little exciting and a little bit scary. After all that effort getting the lights to work there's a bit of a 'now what?' moment - having the flowchart again to show me what needs to be done next is a real help.

Words cannot express my love of flowcharts right now. Not only for guidance but for seeing where things go wrong. If I have a visual of the program's flow, everything becomes clear to me. They've already saved me several times on this project, and I don't think this will be the last time.

I'm seriously going to miss this project over the weekend. It's been a whole load of frustrating fun. And I'm quite sure by now that those aren't mutually exclusive.

### Day 24: July 6, 2017

**Today's Progress**: Success - kind of. I've got the lights to blink in sequence using setTimeout, no more queues or delays. Some more wrangling and I got it working in a for loop, though I had to put the actual on/off function outside the loop. Just one problem with the timing, when one light switches off, the next one immediately switches on. This means if the same light blinks twice or more in sucession (something I put in my test array because I specifically wanted to try out that condition) the individual blinks aren't visible. The light appears to stay on.

For a moment I considered making it so that adjoining elements in the array couldn't be the same, but face it, that's being extremely lazy over a fixable problem. The timing has always caught me out, getting the right numbers in sequence is hard, but it shouldn't be impossible! I DO have issues with visualising those numbers, so back to the flowcharts. If I can write out what's going on in flowchart form, I should have a second by second breakdown of what exactly is happening here. Tried that and was better able to visualise the number sequence that would allow me to time the lights properly. Now they flash as they should do! I can also speed up the sequence by adjusting the interval time, which will be useful when I need to speed the game up in later stages.

Now that little bit of core functionality is working, I want to get it going within an actual game rather than repeating a predetermined sequence. The game needs to randomly choose a light to add to the sequence, so I set it to generate random numbers between 1 and 4 within a switch statement. Each number corresponds to a string containing the light div's id ('red', 'yellow', 'blue' or 'green'), that string goes into the array, and the sequencing loop references that array. Still a few bugs in that. Will get to them next time, but overall this was a good day.

**Thoughts:** Still frustrating to run into a problem after most are solved. You start to wonder if it's another thing you can't solve and the whole thing will need rebuilding again. But it's much better going than yesterday. I admit the temptation to decide to just go with the two or more elements flashing in sequence issue is strong, but it would be very bad form to just give up and pretend it was always part of the game when it's not. So, onward, and getting it to WORK rather than working around the issue feels great.

### Day 23: July 5, 2017

**Today's Progress**: Back with the Simon game and timing the light flashes. Attempting to replace delay() with animate() and use stop() to clear it. Slow going. I'm not sure I'm on the right path with this. More looking around, [this seems similar to my problems](https://stackoverflow.com/questions/5324587/jquery-animation-in-sequence), but only acts on each div once - in my case the divs need to animate multiple times within the sequence. Maybe it was queues I needed after all. Tried out some work with them but everything seems even more tangled up. Perhaps I need to name them.

**Thoughts:** Sometimes the amount of options available is frustrating, you spend a while on one only to find it wasn't the best idea. I admit I'm feeling discouraged - I'm looking up everything I can and while it makes sense, I can't seem to apply it to what I need to do. I don't feel very smart right now, although I know I'll get this in the future.

### Day 22: July 4, 2017

**Today's Progress**: Stuck away from my normal work station today so did some personal site work again and some reading on static site generators. I'm interested in learning how to convert my sites to themes, even if I don't end up using them.

**Thoughts:** I wish I had more to say about the personal sites, but honestly it's basic work, formatting and the like. So not very exciting. Got some ideas for more interesting personal projects for when I can't get to my FCC work, though - thinking of the "3K words for the unmotivated" writing webapp I've been considering, or some site themes based on teletext, just for fun and flexing the design site of things.

### Day 21: July 3, 2017

**Today's Progress**: Finally back to the Simon game! Managed to get the lights to switch 'on' in succession using delay(). Next I want to make the lights blink on and off rather than staying on. Set up a test fixed sequence to get the timing right. Next up, linked that to an array which I can then get the game to modify later - each array element shares its name with one of the light divs. Scrapped the fixed sequence and set up a for loop referring to that array.

This worked but problems set in when I added more items to the array - suddenly the timing was wrong again. I think there's a problem in calculating the delay, got to work out the exact sequence. Went back to the hard coded sequence and commented out the loop for now.

I think it has something to do with the delay on subsequent calls to that div being added on to what came before. Today's question - is there a way to clear the preexisting delay? [Answer: Not a simple one...](https://stackoverflow.com/questions/7929266/jquery-delay-how-to-stop-it) but there's some workarounds there that I want to look into next time.

**Thoughts:** Getting back to a challenge feels good. Finding delay()'s timing to be very confusing, but reading is always good. Things are tough - I didn't expect to run up against that issue with delays not being able to cancel - but I feel challenged in a good way, like I know I can solve these problems with a bit of effort. That's great! I haven't felt like this for days now! I love days where I learn something new about the tools I've been using all this time!

### Day 20: July 2, 2017

**Today's Progress**: More personal sites. Hoping to be back to some heavier work tomorrow...

**Thoughts:** I still feel like I'm being lazy working on personal sites and not pushing myself, but at the same time I'm also getting a lot of work done that was sitting around, so it evens itself out?

### Day 19: July 1, 2017

**Today's Progress**: Kept pushing myself to do some work while sick, did some more formatting on one of the personal sites...

### Day 18: June 30, 2017

**Today's Progress**: Still feeling very sick. Wanted to do something even if small so I set up a test Wordpress install. I don't know what I'll do with it, but I want to at least learn to make themes. After that updated some more personal work.

**Thoughts:** I feel so behind only just learning Wordpress now. I've always been a static site person - I learnt HTML in the late Geocities days so static has always been how I work. But even if I don't get much personal use from Wordpress I think it's worth learning. I lost an interview chance for not knowing any back end stuff, I don't want to lose any more.

**Link to work:** None today.

### Day 17: June 29, 2017

**Today's Progress**: Nope, its a full blown sick day...

### Day 16: June 28, 2017

**Today's Progress**: None today. Things piled up too much and I needed a break. Back to work tomorrow!

### Day 15: June 27, 2017

**Today's Progress**: The gallery is working, could use a few minor formatting tweaks but it works...

**Thoughts:** I hope things clear up. It's nice to have some relaxing work, but I want to get back to the big stuff...

**Link to work:** None today.

### Day 14: June 26, 2017

**Today's Progress**: Life suddenly got busy so decided to do something calming and work on the gallery. Decided to do a JQuery version for now since I know I can get it to work. It's not super end user friendly, but I'm the only one who's going to be editing it, so it'll do for now.

**Thoughts:** Lazy days make me feel guilty...

**Link to work:** None today.

### Day 13: June 25, 2017

**Today's Progress**: The gallery popups for the personal/art site I was working on last week are buggy. Switched back to basic image links for now. It's bare bones but it works.

**Thoughts:** I made the popups using CSS - I can easily do them with JQuery but I wanted something a touch more accessible. But I see what I did wrong with the CSS popups. I copied a lot of code without really understanding what I was doing. I'd still like to do CSS popups if at all possible, but I want to understand what I'm doing this time.

Considering setting up a local Wordpress installation too. I work mostly with static pages but I think it may be time to try learning some backend stuff.

**Link to work:** None today.

### Day 12: June 24, 2017

**Today's Progress**: Made some background images for the Simon game and tried some test animations. They flip nicely back and forth now, no complex layering needed. Now to see if I can use queues to get them flashing in order.

Moved back to the personal/writing site I was working on last week. Added some story content, static HTML as usual, and embedded some fonts. Looking good.

**Thoughts:** Lazy day, I admit. But it felt good to go back to the personal projects I'd been neglecting too!

**Link to work:** None today.

### Day 11: June 23, 2017

**Today's Progress**: More on the Simon game and timing the sequence flashing. Taking my own advice and decided to plot out how I think I'll do it on a flowchart rather than touching any actual code. [This may also be of some help](https://stackoverflow.com/questions/7519793/sequencing-events-in-javascript). Thinking Jquery queues are what I'm looking for. Experimenting with delay() - maybe I was doing it wrong by changing classes, maybe animate() is my friend here? It can't do colours but I could have an 'off' div that lays on top of the 'on' div, and can be set to not display. Tried it, found it makes positioning a pain. Maybe background images? I'm thinking of using some anyway. The image itself isn't possible, but maybe the position...? Did a test run with a random wallpaper, and it works. The sequencing is still to come, but I can at least animate the background.

**Thoughts:** Definitely at the point where my least favourite thing about JS is not being able to just tell it to pause and then resume x time later... but I get the feeling this project is meant to get you working on that. I do like FCC's 'throw you in' style even if times like these are frustrating. But having that moment where you feel you've found an answer is worth it.

I'm thinking the animation sequence timing is going to be the difficult part here. But I don't want to speak too soon either.

**Link to work:** None today.

### Day 10: June 22, 2017

**Today's Progress**: Continuing the Simon game, roughed out a flowchart for the basic game logic. Next I want to focus on making the divs (they might not stay divs, it depends on how I lay the game out, but I'm using them right now for simplicity's sake) light up one by one. Managed to use setInterval to make one div light up and turn off, now to get a sequence going without them all going off at once. Doing some more reading on setInterval.

My pomodoro clock (see below) would decrement the time remaining, convert that to a m:s display to put on the page, and complete when the timer ran out. Can I modify that for this game (switch light x on/off when time y reached) or would that be overly complicated overkill?

**Thoughts:** This was the first time I planned a project using a flowchart. Previously I haven't felt the need to, but in this case I felt I needed a map. It was very helpful seeing it laid out before me. Will definitely use this method again in the future. (Not sure why I never felt the need before, I worked a lot with flowcharts in a previous job.)

With the lights, the most frustrating part is getting the program to 'pause' and light things up in sequence. I'm not sure I fully understand setTimeout, though I use it as a seconds counter in a previous project: [FCC Pomodoro Clock](https://codepen.io/jsanderson/pen/qNoXZJ). This time it's a it more difficult. Don't want to do what I did before and stop for ages because I'm discouraged, though... It's okay. I'm in that early stage where everything is a mess, I've made it through before, I'll make it through here.

**Link to work:** None today.

### Day 9: June 21, 2017

**Today's Progress**: Onto the Simon webapp, the last front end development challenge on FCC. Had to research the game some. Set up a test page - nothing fancy, just some clickable coloured divs to try the game logic out on. I think I'm going to try putting my own twist on the way it looks, but I'm not too concerned about layout at this stage.

Decided to step back from the code for now and map out the program's flow.

**Thoughts:** I wonder if I rely too much on JQuery... should I be trying new things?

Kind of interesting to be working on a game I'm unfamiliar with as opposed to one I know like before. I wonder if that makes my approach any different?

**Link to work:** None today.

### Day 8: June 20, 2017

**Today's Progress**: Finishing off the weather app, adding an imageless version for small screens.

Decided to redo my FCC portfolio page once that was done. Minor tweaks again.

**Thoughts:** Keep on feeling the urge to add more to the weather app, but I think it's important to know when to call it done.

**Link to work:** [Local weather](https://codepen.io/jsanderson/pen/VeRmJM)

### Day 7: June 19, 2017

**Today's Progress**: Back to the weather app. It's all functional now, added some new backgrounds and an imperial unit conversion option. Doing some formatting changes to make text more readable against some of the background images.

**Thoughts:** Nothing game changing, but I think I'm settling into a routine of sitting down to code and looking forward to it too. Great flow state too, ended up late home because I was so absorbed in what I was doing!

**Link to work:** [Local weather](https://codepen.io/jsanderson/pen/VeRmJM)

### Day 6: June 18, 2017

**Today's Progress**: Still not feeling too great, did some basic layout work on another personal site (this time, for some writing work).

**Thoughts:** Just low stress stuff for those umotivated sick days. Considering devoting weekends to personal projects and weekdays to FCC/other tutorial projects. Will see how it goes. The best bit - I'm one week in!

**Link to work:** None today.

### Day 5: June 17, 2017

**Today's Progress**: Feeling somewhat unwell today so went back to working on the gallery site from Day 2, getting it all updated. Mostly tidying everythig up and getting it presentable

**Thoughts:** Not feeling very motivated due to illness, but glad I had something low stress to do. It was something I'd been putting off for ages anyway...

**Link to work:** None today.

### Day 4: June 16, 2017

**Today's Progress**: Continung the FCC Twitch streamer status webapp, rebuilding it with the new API. Got it to work and fixed some old code.

Next up is the weather app, another case of having to start again with a new API. Problems with access control first of all - didn't realise had to add "callback=?" to the end of the getJSON url. Easy enough to fix things now. Got the main bulk of the app working again, next up need to offer an imperial units option and get some variable backgrounds in there.

**Thoughts:** I feel a lot better about having to rebuild my old code than I did yesterday. It was frustrating then, but the rewriting has shown me there was a lot of room for improvement - better commenting, getting rid of all those global variables that were floating around.

Moving on to the weather app I feel better too. I know where I am now. The failure to initially complete the API call was frustrating but I need to remember - check the browser console, not just Codepen's.

I'm a little embarassed too - in the last five days I've done more on my FCC courses than I have since the start of the year. But it also shows what accountability does to you. (I should know, I'm a returning NaNoWriMo participant since 2003.)

**Link to work:** [Twitch streamer statuses](https://codepen.io/jsanderson/pen/VeNOpL)

### Day 3: June 15, 2017

**Today's Progress**: Back to the FCC work, some issues have cropped up with subsequent games following the first one not playing correctly. Thought it was a styling error but it seems something isn't getting correctly passed back to the main play function. Fixed it - there was some code lying around relating to a since removed class. Play tested it a bit (managed to beat it once, so the imperfect move possibility is definitely there!) and happy to call this one done.

Decided to go back to some older FCC projects before moving on, specifically the API challenges, as the calls don't all work any more and I'm not entirely happy with some of the styling. Started out with minor tweaks to the Wikipedia viewer, styling the textarea and buttons when clicked.

Next up, Twitch streamer statuses. The API call is no longer working, seems to be due to a change on Twitch's end.

**Thoughts:** Honestly thought I'd be just tidying this one up. Nope. Funny how the problem always ends up being a thing that you didn't suspect. More than anything else, happy to have the biggest challenge I've faced so far all wrapped up!

Less happy about the APIs. Looks like I'm having to rebuild the Twitch status project from the ground up, but it could probably use an update anyway...

**Link to work:** [Tic-Tac-Toe](https://codepen.io/jsanderson/pen/JJPwxQ)
[Wikipedia Viewer](https://codepen.io/jsanderson/pen/xZBmXy)

### Day 2: June 14, 2017

**Today's Progress**: Slight change of plan, away from my usual work area so decided to do some work on a personal/artwork portfolio site of mine that's long due for an update. Most of the work is on giving it a responsive layout and some new menus as well as updating the content (no backend, it's all manual). Set up a rudimentary form with formspring, needs some styling, but a lot better than before.

**Thoughts:** I get a lot of thoughts about design when I'm doing this sort of work. I want to make something professional, but I don't want something dull and sterile. This is an art gallery! (And code is art too!) Does the world want sites that are't big, blank white expanses with giant photos and a bit of blue? I hope so. Because I like purple.

**Link to work:** None today.

### Day 1: June 13, 2017

**Today's Progress**: Continuing the FCC Tic-Tac-Toe challenge, moving on to styling as the base code is now working. Want to include a bit of interactivity - have the intro box offer you your symbol, fade that out to reveal the board, and so on. Some shuffling of the JS to animate things. Mostly done, need to get the rematch function working, but no more boring alert boxes!

**Thoughts:** Lots of positioning and z-index work, which is annoying when it doesn't do what you think it does. But the styling is relaxing after a lot of game coding, all the same. It feels like the big challenges have been overcome, and the finish is in sight. Sometimes worry I'm overengineering some of the styling work, but maybe that's just normal when you have to tweak the game code again...

**Link to work:** [Tic-Tac-Toe](https://codepen.io/jsanderson/pen/JJPwxQ)

### Day 0: June 12, 2017

**Today's Progress**: Working on FCC's [Tic-Tac-Toe](https://www.freecodecamp.com/challenges/build-a-tic-tac-toe-game) Challenge. Most game functionality is already there - working on the game AI right now as too easy to beat. Looks like it doesn't check for winning scenarios correctly, need to fix...

Solved it after carefully logging variables step by step. Turns out it was a simple mistake, easily fixed.

This has also had the effect of solving another problem I had with subsequent games not registering moves correctly!

Felt the computer being unbeatable (the human player can force a draw) was dull, so I added in the possibility (not too large, if Math.random > 0.9) that the computer will skip the game AI and place a random move. Should allow the human player some chance of victory once in a while!

Cleaned up some repetitive code regarding game over/restart game details, put in its own function.

The game is complete and plays well, all that is left to do is style the page.

**Thoughts:** This particular challenge has been a block in my path for a long time. Very frustrating, but with some accountability behind me I feel more empowered to bust through even if I'm frustrated, rather than losing interest and wandering off.

Feeling a lot better now I've found the source of the problem, too! As usual it's a silly mistake, but these things happen, what matters is putting in the effort to track them down.

Feeling -very- happy with having fixed the JS and having a fully working game. For me that's the main challenge, the styling is going to be nice and relaxing after this. I consider it a reward!

Fantastic first day all around!

**Link to work:** [Tic-Tac-Toe](https://codepen.io/jsanderson/pen/JJPwxQ)
