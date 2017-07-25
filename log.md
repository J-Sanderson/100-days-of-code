# 100 Days Of Code - Log

### Day 42: July 25, 2017

**Today's Progress**: More tweaks to the Simon game - a mobile layout, an 'about box'. Small things, mostly. I will need to create some more graphics and sounds before I can do anything big.

**Thoughts:** Slow, calm, relaxing. I got this.

**Link to work:** [Copycat! A  Simon clone!](https://codepen.io/jsanderson/pen/vZwYOx)

### Day 41: July 24, 2017

**Today's Progress**: Fixed the broken 'play again' button in the Simon game. Still need sounds, but focusing for now on the layout, colour scheme etc. Got the layout set to roughly how I want it, still using some placeholders so will need to draw appropriate graphics as needed. Need to make a mobile version too, as it stands the layout is extremely mobile unfriendly.

**Thoughts:** Everything feels so sedate now! It's weird to think of this last challenge almost being done. I'm wondering what I'll do next.

**Link to work:** [Copycat! A  Simon clone!](https://codepen.io/jsanderson/pen/vZwYOx)

### Day 40: July 23, 2017

**Today's Progress**: Some tweaks to the Simon game - nothing major today, mainly layout/color/graphics changes. Still got a few bugs but as right now I'm in a position to be able to make graphics I want to focus on that while I can. Will return to the bugs tomorrow. Looking for sounds - not yet found anything satisfactory, may record my own.

**Thoughts:** Small things, but I like seeing the game get a theme.

**Link to work:** [Copycat! A  Simon clone!](https://codepen.io/jsanderson/pen/vZwYOx)

### Day 39: July 22, 2017

**Today's Progress**: Last day of family visit, so no work done today...

### Day 38: July 21, 2017

**Today's Progress**: Continuing to work on the Simon game. Now that the main functionality is down, I'm working on smaller things. Worked mostly on adding some messages - the win condition, a lose message for strict mode. They pop up okay, but I'm having trouble gettig the button clicks on those messages to start a new game. They don't seem to be registering yet, need to work out why. Planning what I want the game to look like too - I think I will make some images to add flavour.

**Thoughts:** Things feel slower today, but I think that's because I've moved on from solving the big things. Still lots to do, but it's all different now.

**Link to work:** [Copycat! A  Simon clone!](https://codepen.io/jsanderson/pen/vZwYOx)

### Day 37: July 20, 2017

**Today's Progress**: Playtested the Simon game - it works and the win condition triggers at the right point! There is of course still lots to do, but the basic game will now play as required.

Next up, I want to enable strict mode since that's one of the still missing core aspects. Added a checkbox to turn it on and off and a variable to keep track. Tested it again - the wrong click branch now handles this and will exit the play function (though at the moment it doesn't restart - I will probably add in a 'you lost, do you want to try again?' message later). 

In the same vein, the game needs a reset button so the user can choose to start again. Added one in, set it to reset everything and restart. In the future I want to add a 'do you want to restart?' message but that can come later.

The next user story that needs to be covered is speeding the game up on the 5th, 9th, and 13th steps to mimic the original game and add more of a challenge - as it stands each light stays on for a second, which is pretty slow (and rather dull when play-testing, I found). Set the interval to vary depending on the current round, tested it out and it feels nice and challenging.

The only user story left to fulfil is the sounds - I think I will do those later. FCC has the original game sounds but I have an idea that I want to do instead (it'll play like the original, but won't look or sound like it), and it will involve finding the sounds I need, so that will have to come later.

Apart from that, I have a very plain looking but fully functional Simon game!

**Thoughts:** A relaxing day, probably for the best since I have family over, but I would have pushed on regardless - I'm all the more excited to be doing this as the project grows more and more into what it should be. I've noticed a pattern when creating/making in other areas - there is always a point where everything seems irreversibly broken, but it gets better. This is the getting better bit.

**Link to work:** [Simon game](https://codepen.io/jsanderson/pen/vZwYOx)

### Day 36: July 19, 2017

**Today's Progress**: Reconstructed the Simon game. The sequence display and lights are still working. I now need to focus on the logic for the user's clicks. At the moment it is set to move on to the next step in the sequence when the user presses any light regardless of how far along the sequence is, or whether the click was even correct.

First of all, added code to just say if the user's click was right or wrong. Now it needs to handle the two situations differently:

If wrong: re-display the sequence all over again (or restart everything if in strict mode)
If right: check if the user has finished inputting the sequence, and start the next round if so.

First added in the wrong branch - that was easy enough for now, just re-call play() without iterating the user's click counter or the round counter, and the sequence displays again (I'm planning to add strict mode and some sort of 'wrong click' message later - want to get the basic functionality right first). The code for the right branch is a little more complex as it needs to do a few more things: iterate the user click counter, test if the counter is equal to the current round, then call play() for the next round if so.

At last, the game is starting to run as it should! But it's still missing a win functionality. Put in a quick test to see if the round is equal to the maximum steps (20). Need to trial it to see if it works, so time to play the game...

**Thoughts:** I don't want to say anything too soon, but this feels like the monent where it starts to come together again...

It runs properly. I don't know if I can say how great that feels. It's the moment where you think yes, this is what I love to do, and I'm glad I'm doing it. Code isn't just something I'm doing because it's a big thing, but because making things and seeing them work is something I love, and this is a great medium for it.

### Day 35: July 18, 2017

**Today's Progress**: Another go at the Simon game and getting the round variable to behave. It seems to be iterating over and over until it hits double its previous value - still unsure why. I keep thinking it's still a scope error because it's so similar to the word counter issues I had, but it's not behaving as that did. Tried creating a local variable with let, still no luck. 

Some more testing and it does seem that the doubling is due to the play function calling itself over and over until the round value has doubled. Very puzzled now, as the function should only be called on a user's click. Even commenting out all the light switches/timing and just having the current sequence display in the console still causes doubling.

Stripped everything down even further - now all that happens is the console logs the current round. A little more testing with alerts and it seems that it's the click handler excecuting multiple times? Tried moving the click handler outside of play(). Finally the stripped down function counts properly! Now to rebuild. But finally, I found the weak spot.

Now to rebuild - I have an earlier version but I think I will be rebuilding the stripped down one using that as a reference. I feel the code was getting a bit convoluted and I was losing track, so this will hopefully help me grasp it better. Recreated the light switch function, can definitely see improvements I can make on what variables I pass to it.

**Thoughts:** At the lowest point of the tic-tac-toe challenge, it was much like this - I felt like I had to rebuild everything all over again, and I didn't know how or why things happened as they did. I stalled for a long time because of it. I don't want to do that again.

I'm not admitting defeat but I am admitting that this is an issue I don't fully understand. I know I can learn but things do seem pretty low at the moment. But if the tic-tac-toe challenge is any indication, this is where things start looking up...

And I suppose they did. But again, I'm pretty sad that I don't understand why it happened. I want to understand more. 'It works somehow if I do this' isn't satisfying!

### Day 34: July 17, 2017

**Today's Progress**: Back to the Simon game. Need to work out what's causing the play function to call itself at the wrong time. After some poking around there seem to be yet more issues with the light timing.

I think I may need to step back and think some more about getting the display right without worrying about the user's clicks so much. Probably need to roll back and look at that more in depth. Made a new fork and stripped out the code relating to counting and testing the user's clicks. Focusing just on having the user click any light, then the sequence displaying the next iteration. That should help weed out any time errors.

So far the sequence is working but it does seem to be having some issues with counting the current round. I'm testing by having the console display the current round, and it's doing so twice once I get past round one. Double checked for duplicate code but there doesn't appear to be any. There also seems to be an error in timing for when the lights become active each round. It seems to occur in rounds three and up - the delay in making the lights active seems to be capping somehow at two or three seconds. Tried to log the delay to take a look at it, and it seems to be called twice or more, just as with the current round variable - and the first delay is 3 seconds, as I observed. It then gets called an increasing number of times as the rounds go on. The final iteration for each round is correct but obviously can't function properly.

So again, it's all back to the round numbers. Not much progress but at least I think I've hit the major source of the problem...

**Thoughts:** Very nitpicky work. That said, I like hunting down problems like this. Not so fond of facing the prospect of dismantling so much code after so much effort. But if it doesn't work, it can't stay. Sometimes dismantling and rebuilding helps me find what's wrong.

Feels like yet another day for the 'things will get better if you keep at it' reassurances. But that's ok. If I knew everything, I wouldn't be doing this.

### Day 34: July 16, 2017

**Today's Progress**: Little bit more work on the event bubbling demo. I got it working, it's quick and easy but I now know something I didn't before! I think I'd like to expand it a bit later but I'm mainly just happy to have taken a rather embarassing phone call and turned into into a learning opportunity!

**Thoughts:** That was a lot easier than I thought it'd be! Feels almost too easy. But it works and that's what's important. I think I'd like to do some more demos to teach myself - I still want to get a better understanding of promises and closures. They at least seem a lot less scary than they did only a week ago!

**Link to work:** [Event Bubbling Demo](https://codepen.io/jsanderson/full/gREyob/)

### Day 33: July 15, 2017

**Today's Progress**: Need a new weekend project now that the word counter is done. My thought was to try teaching myself some of the concepts that I wanted to brush up on, so I started putting together a simple event bubbling demo. So far I have the basic setup done, but no actual bubbling - I still need to do some more reading into how to set that up.

**Thoughts:** Working with pure vanilla JS feels so strange. There's so much I don't know because I've done all my DOM handling with JQuery. That's fine, that's what JQuery is for, but I do feel like I need to know the basics too. Maybe I should challenge myself to put JQuery to one side a bit more just so I know more of what the vanilla JS is actually doing.

### Day 32: July 14, 2017

**Today's Progress**: Finishing off the word counter. Added in a popup box to explain the challenge, then added some styling and tidied the CSS. I'm going to call this one done for now!

**Thoughts:**  Small, relaxing, but very fulfilling. I made something useful!

**Link to work:** [A Word Crawl for the Motivationally Challenged!](https://codepen.io/jsanderson/pen/EXdPey)

### Day 31: July 13, 2017

**Today's Progress**: While reading through You Don't Know JS' chapter on [closures](https://github.com/getify/You-Dont-Know-JS/blob/master/scope%20%26%20closures/ch5.md), I found some interesting details in the section regarding closures and loops. I think this might go some way toward explaining some of the sequence display issues I had in the Simon game, and possibly the scope errors in the word counter. Interesting reading.

Now back to the game. The user clicks are working but the game needs to stop them once the user is done with the current sequence (or makes a mistake, when I get to implimenting strict mode). Set it up to remove the active class from the lights once the sequence length is reached - works just fine. No code yet to handle restarting/strict mode on errors, but that can come later.

I now have a reasonably working game, but it only runs with a set sequence of three presses. Next big step - get it working as a proper game, one sequence at a time. Moved the whole playing code, apart from generating the sequence at the start, to its own function. I still only have a hazy idea of what is to happen, but I'm imagining it working similar to the word counter, calling itself again when done. Created a counter to show what round of the game the player is on, and got it to display in the on screen counter.

Thinking about getting the function to call itself again. I can't easily put in a delay as I have no means of knowing how long the current round is going to take. But I do have code to handle finishing the user's inputs, which is dependent on the user's click - I can just re-call the function there. This seems to work, though now I have to make sure the code inside the play function isn't so static. As expected the biggest issue is the timing for making the lights active. They need to be set to active as soon as the page is done demonstrating the sequence, so I need to determine the number sequence to use to calculate the delay. Wrote down the round number/delay sequence and paper which helped me to work it out. Tested it, but the timing still isn't right.

Looked around at the program flow with the console - I think it's somewhere in the user click, or re-calling the play function. It seems to be re-calling play() even when the user counter isn't done. I think this may be similar to the issue I had with the word counter, but globally declaring the current round variable didn't help. I'm just going to have to keep looking and breaking things down until I find the answer...

**Thoughts:** I'm over a quarter of the way done now and honestly I feel like it's going too fast! The end is going to come sooner than I thought. Maybe I'll try a round two afterwards... 200 days of code?

Starting to worry about how tangled the Simon code is - feels like it's bouncing around and passing things all over the place. Trying not to worry about it until I have the whole game functional, though. I'm still only on the basics - I don't know what it'll be like later. (Later note - already feels somewhat improved by putting the light switch/click functions inside the main play function?)

Moving on to getting the game working as a proper game is intimidating - it means taking what I have now and adding a whole new layer onto it. Things will likely break. That's ok. I can handle this.

And really, it went better than I thought. Sure there's a few confusing bits and some very broken parts, but the game is starting to act more and more as it should do. It's a very satisfying feeling.

### Day 30: July 12, 2017

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
