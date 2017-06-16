# 100 Days Of Code - Log

### Day 4: June 16, 2017

**Today's Progress**: Continung the FCC Twitch streamer status webapp, rebuilding it with the new API. Got it to work and fixed some old code.

**Thoughts:** I feel a lot better about having to rebuild my old code than I did yesterday. It was frustrating then, but the rewriting has shown me there was a lot of room for improvement - better commenting, getting rid of all those global variables that were floating around.

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
