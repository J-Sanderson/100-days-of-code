# 100 Days Of Code - Log

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
