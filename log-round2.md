# 100 Days Of Code Round 2 - Log

### Day 23: October 25/10/17

**Today's Progress:** Looking for some resources for random dungeon generation. [This](http://bigbadwofl.me/random-dungeon-generator/) may help, also [this](http://www.roguebasin.com/index.php?title=Dungeon-Building_Algorithm). Tried doing some basic setup, so far I can generate an initial chamber but I'm still unsure which one to go for...

**Thoughts:** I keep on feeling really intimidated. Is too much going on at once? It's okay. I have this. It's okay. (okay admittedly I'm trying to focus through the odd minor panic attack but long story... small progress is progress.)

### Day 22: October 24/10/17

**Today's Progress:** Back to FCC's curriculum. The last of the React/SASS projects is the roguelike dungeon crawler. This seems like a big deal and intimidating. I'm trying to think of it as several smaller problems. Things that come to mind:

* setting up a board - randomly generating rooms etc, will need to look up how to do this. There are probably plenty of well documented examples out there to look up.
* rendering the board - I'm thinking this will be similar to the Game of Life with a grid rendered on canvas, although this time the whole thing will not be shown.
* moving the player character - there's probably going to be an x,y co-ordinate stored in state for them. I think I would like to have them respond to keyboard presses and maybe some on screen buttons too.
* populating the board with enemies, weapons, health items etc - probably will store stats for these in an object somewhere.
* the ability to save progress to local storage? Not vital but nice to have.

It does seem like a natural progression from the Game of Life, when I think of it. As with everything else I've done in React, the first thing will probably be to build a static version. It won't do an awful lot, but it'll hold everything that needs to come later.

Set up a basic page layout with a canvas element to hold the game screen. Next up will be generating the dungeon.

**Thoughts:** I'm feeling intimidated? By this project and by a lot of things. It's ok. Someone told me I need to fly. So get out those wings. Or something.

### Day 21: October 23/10/17

**Today's Progress:** Another personal work day as today was very hectic and people heavy!

### Day 20: October 22/10/17

**Today's Progress:** Took another slow day and did some more personal site work...

### Day 19: October 21/10/17

**Today's Progress:** Tested the Game of Life in Firefox, seems to work ok. Passing it out to some friends to see if they have difficulties. Added some styling to finish it off for now, will call it done.

**Thoughts:** There are definitely things I feel I could have done better. Sometimes I think the game logic was too complex. I think now that I'm done I might see how other people have implemented it. That said I'm happy to be done, this was a complicated piece of work that took a while, and having a finished product is very satisfying.

**Link to work:** [Game of Life](https://codepen.io/jsanderson/pen/xXYMNK)

### Day 18: October 20/10/17

**Today's Progress:** Going through the Game of Life code step by step but still unable to determine why it can't find the reference array. I did find another bug in which changing the canvas size doesn't cause the game to create an entirely new randomised grid, which it should do. Turned out that was another issue with the generator function directly referencing the grid in state - switched things around so that it makes a completely new one, and the problems are solved. Now back to the missing reference...

...Looks like an off by one error. Of course it would be something stupid like that! At least the code is a bit neater now, none of these refBoard.length - 1 statements all over the place.

Filled in the rest of the missing game logic and it runs perfectly! (also altered the game speed settings as even the fast one seemed too slow)

The last user story is the ability to add or remove cells by clicking the grid. I already have a function set up to detect clicks on the canvas element but what I need is to know where on the canvas the click was. I am not sure how to do that so I will have to do some more reading. [This might help.](http://miloq.blogspot.co.uk/2011/05/coordinates-mouse-click-canvas.html)

Using the example I managed to work out the corresponding array position (divide the co-ordinate by ten, then round down) and pass it to the cell click function. From there I managed to use the same board update logic as before - create a copy, modify it according to the row and column position, then pass back to state. The function allows the user to turn a cell on or off depending on its initial state.

The only problem is that the co-ordinate detection does not work in Firefox according to the linked example. Thankfully it includes a workround, but at the moment I don't have access to Firefox so I can't test it. Tomorrow I will, so will try to test it then.

That aside, the gameplay and user stories are fulfilled, and it's time to work on styling, but I think I'll leave most of that until I know the Firefox issue is solved.

**Thoughts:** See, I knew it would be something stupid.

I'm kind of liking some of the emergent behaviour I'm already seing even with the game logic only partially implemented. I'm seeing these little thorn shaped things going from right to left. I'm calling them "fenceposts" for now. Cute little guys.

Kind of fun to watch everything run now I have the full game logic. Makes up for the frustration to have something cool to stare at.

**Link to work:** [Game of Life](https://codepen.io/jsanderson/pen/xXYMNK)

### Day 17: October 19/10/17

**Today's Progress:** Another busy day so taking it off. New end point is day 102.

### Day 16: October 18/10/17

**Today's Progress:** Trying to work out the wrap around function of the game play. Starting to get some animation but running into an error when I try to look up the bottom left cell with a wrap around - somehow it acts as if the rightmost column is undefined? I can tell that the cell is there because the state will log to the console but somehow the code to check if it is set to true or false acts as if it is not there. 

**Thoughts:** This is frustrating because on paper the whole thing makes sense - get the state of all neighbouring cells. 

### Day 15: October 17/10/17

**Today's Progress:** A little more CSS brushing up. Still not feeling so great and some busy days are ahead but doing what I can - there is a reason for the sudden CSS swerve.

Made an attempt at implementing game logic for the Game of Life, however running into trouble with the edge cells not working correctly and the entire thing failing to run. I can see the problem - the function to check on the number of neighbours fails if the cell is on the edge since there is nothing for it to reference - but need to figure out how to overcome this. Ideally I would like the game board to wrap around into a toroidal shape.

### Day 14: October 16/10/17

**Today's Progress:** Still feeling unwell, so went to my usual fallback of personal HTML webpage work (read: pretending it's the 90s). Also did some brushing up on CSS.

**Thoughts:** I was surprised by how little I knew about CSS. I learnt about attribute selectors - mind blown. Also some more interesting selectors: children, nth of type, adjacent, etc - also specificity and how it works with the cascade. Much of what I know about CSS has been patchy, picking things up as needed. I didn't realise just how complex and powerful it could be.

### Day 13: October 15/10/17

**Today's Progress:** Feeling unwell today so took the day off. New end point is day 101.

### Day 12: October 14/10/17

**Today's Progress:** Spontaneous project day! I made an attempt at reverse-engineering the random name generator from the game [Niche](http://niche-game.com/). My guess was that it determined a number of syllables, then pulled that number randomly from a syllable list, one for male creatures, one for females. The generator I made did indeed manage to pull up names consistent with the ones from the game.

**Thoughts:** I didn't plan on doing this, but it was something I'd meant to make for a while and I got inspired by a livestream. It was fun to make something as a one-day project, going from an idea to a full page in a few hours.

### Day 11: October 13/10/17

**Today's Progress:** Looking at the page layout, I felt that the buttons should go in their own component. So I shuffled things around and updated the functions. Worked on changing game speed, again with just the generation counter. Managed to get it set up and going. Added a test into the play() function (currently updates the generation counter but will eventually handle all the game logic) to update the canvas too - so far it just inverts dead and alive cells each generation. This works but it then occured to me that every bit of array code so far was directly accessing and updating the array held in state, not copying it and then updating state once all needed changes are making. After some reading fixed it with a combination of map() for the ounter array and slice() for the inner. Now that's working too.

There's one more thing I need to set up before I do some real game logic, though, and that's the pause and resume buttons. Added that in with a function to clear the current timeout. I also want to be able to clear the board, which will also mean pausing it so that the user can add their own cell pattern. Set up the clear function with the ability to pause the game. Now to clear the board. Set up two nested map() functions to copy the state array and set every cell to false (i.e. dead). Everything working so far.

Next step will be the actual game logic. (There is one more story I need to address, which is the ability to click to add cells, but that's going to involve some more reading up on canvas so I will save it for later).

**Thoughts:** I think this is the point where things start to look up. I'm excited to start tackling the game logic and have the board start to do what it should do. All of this work so far has just been a setup for this point.

**Link to work:** [Game of Life](https://codepen.io/jsanderson/pen/xXYMNK)

### Day 10: October 12/10/17

**Today's Progress:** Busy day! Taking it off - new end point is day 100.

### Day 9: October 11/10/17

**Today's Progress:** Trying to set up the code to iterate the game every interval, but having trouble working out where it should go. Going to go back to the video and double check where everything is. Managed to set up a timer, though so far it only increments the generation count and does nothing to the actual board. I want to get all the things associated with the timer (starting, stopping, changing speed and board size - the latter of which should reset the game as it's a new board) going before I worry about the game logic. So far I have managed to get the counter to reset if the board size changes. The rest is up next.

**Thoughts:** I don't want to copy but I do want a better idea of what state goes where. If I can update the page with a click, I can update it with a timer.

### Day 8: October 10/10/17

**Today's Progress:** Back to the game and working out the canvas. Wrote up the function to change the canvas size to one of three presets (small, medium, and large). That's saved in the state and then passed to the grid component. Also wrote up an initial board setup function that runs when the App component mounts. It creates a 2D array of cell values (true for alive, false for dead) and saves that in the App state - this also gets passed to the board. In the future there will be functionality to update this state. For now it's just generating an initial setup.

Now the grid needs to draw this setup on the canvas. Here's where things get interesting, and by interesting, I mean I am not sure what I'm doing, but will have fun finding out...

A lot of wrangling and I think what I need to do is set the canvas drawing inside of Grid's componentDidUpdate function. So far I managed to get it to render the initial state and fix some bugs with the state not updating right when I tried to change sizes. I now have a starting point and the next thing to do is to update the board every generation.

**Thoughts:** This is not one of the good days. I don't think React and canvas are having a nice time together. I'm not having a nice time with them. I'll get through this, but really starting to wonder if I put the state in the right place. Maybe will rewatch that video again and take a closer look as to how it's put together.

### Day 7: October 09/10/17

**Today's Progress:** Spent some time learning the basics of canvas. I think now that I have an idea where I'm going. I can split up my game screen canvas into squares, which correspond to on or off values inside an array passed to the canvas from the parent App container. That container can then update the array every tick of the game and pass it back to the canvas.

Drew up a diagram of data flow around the app so I now have something to go by. Added the required functions onto the page. None of them do anything yet but everything is laid out and ready.

**Thoughts:** I don't like taking a day to sidetrack, but I think this was one of the ones I needed to do.

The data flow looks strangely simplistic, but maybe that's just because I'm looking at it from a high level point.

### Day 6: October 08/10/17

**Today's Progress:** Stuck to some small personal HTML work today.

**Thoughts:** I shouldn't feel so bad for doing small personal projects every now and again. They're important too.

### Day 5: October 07/10/17

**Today's Progress:** Put together a basic static layout for the Game of Life including a canvas tag. Next up, I need to learn more about canvas...

**Thoughts:** I feel intimidated by choosing to use canvas, which is an element I've barely used, but at the same time I think it's something it's about time I learnt about.

I also want to keep better track of the data flow on this project. I think I let it grow too organically with the recipe box and because of that, it ended up messy. For this project I want to get down what I want the page to do and have it all down from the start. I might not know HOW to do all the things right now, but I will know WHAT needs to be done.

### Day 4: October 06/10/17

**Today's Progress:** Put together some styling for the recipe box (and a cancel edit button I'd forgotten to add yesterday). Tried to expand my use of Sass with some mixins to kill repetitive code. After a morning of styling, I'm calling this one done.

Next up is the Game of Life. [I'm kicking back with a video](https://www.youtube.com/watch?v=PM0_Er3SvFQ) and thinking of [requestAnimationFrame](https://css-tricks.com/using-requestanimationframe/). Seeing a lot of suggestions to use canvas, which is relatively new to me but may be worth a go.

**Thoughts:** I still have my reservations about how much data is going back and forth... there's probably some repetitive code in there. Wishing I could do modules in Codepen, but overall really happy with the end result.

**Link to work:** [Recipe Box](https://codepen.io/jsanderson/pen/rGpYze)

### Day 3: October 05/10/17

**Today's Progress:** Back to the recipe box and adding a new recipe. Seperated out ingredients into their own array by splitting at commas and used trim() to remove any leading and trailing whitespace in the name and ingredients. Then this all gets added to local storage and the app updates. Finally added a cancel button to the add box so it can be closed without adding a recipe.

The last bit of functionality to add is the ability to edit recipes. Added an edit box, which could be toggled to appear and disappear the same as the Add box, though a little more complex as the edit box belongs to App but is triggered further down the hierachy. The edit box has a form that has the same fields as the Add box, however in this case it needs to contain the existing name and ingredients as default text.

Run into a problem with passing the name and ingredients to the Add component when triggering the edit box - the state doesn't update until the second click. I can't tell why. Maybe the edit box shouldn't be a direct child of App, but sit under the ingredients list? That way there's no need to pass state around when it doesn't need to be passed. Edit doesn't really need to interact with App until the user submits the results, and then it can pass them over to App to do all the parsing and storing stuff. Until then, everything can live in Ingredients, including the edit display state.

So I put it under the Ingredients component so it could directly recieve what the user is trying to edit. I'm not happy with how the positioning is now set up, but will worry about the CSS later. With the name and ingredients passed as props I could then set them as default values in the form. Made an onEdit function inside App that takes the old name of the recipe (for search purposes), the new name, and the new ingredient list.

Run into a problem, the edit form doesn't let me change the default value in the box. I don't think this is normal for the value property. Placeholder lets me add in text, but it's overwritten as soon as the user starts typing. I want default text that the user can edit, for example they just want to add or remove one ingredient. Making them type the whole list again isn't user friendly. Reading now about [uncontrolled components](https://reactjs.org/docs/uncontrolled-components.html) to see if they can fix this. Turns out I needed to use defaultValue rather than plain value. Now the onEdit function is taking the data it needs, so it should do something with it. Parsed the input as with add, removing excess whitespace and splitting the ingredients into an array with commas as the seperator, then pulled out the existing recipe list. I don't want to remove the old recipe and put a new one in, I want to find the one I'm editing and update it as needed. Can't use indexOf as it's an array of objects, so going through it with forEach and looking at each object inside. I don't know if this is the best thing to do but not sure I can think of anything better.

Still, it works, and after putting the new list back in local storage and updating the state, all user stories are now fulfilled. Tomorrow I'll work on the styling.

**Thoughts:** I'm just happy with how fast and painless this has been. I hope that wasn't too soon.

One thing that's starting to bug me is how much data flow is going back and forth. I should make a diagram, I'm starting to lose track. I should really have done that before I added in any state and flow, that is something I should remember for the next challenge.

**Link to work:** [Recipe Box](https://codepen.io/jsanderson/pen/rGpYze)

### Day 2: October 04/10/17

**Today's Progress:** Doing some reading on [local storage](http://htmlui.com/blog/2011-08-23-5-obscure-facts-about-html5-localstorage.html) and it looks easy to implement. Going to put that on one side for now and think about the rest of the app. Adding and removing items seems easy enough. But I also need to display the recipe when the name is clicked. I guess we're learning about conditional rendering today!

To start off with I stuck with Thinking in React's suggestion to create a static version of the app. I set up a basic hierachy with everything I would need, using two recipes (stored within the code for now) to test it. For each recipe there is a single Recipe component which contains the name of the recipe, and then an Ingredients component containing the ingredients list, as well as buttons to edit and delete the recipe. I think that each of these Recipe components should have its own state that determines whether or not the Ingredients component should display, and that is toggled by clicking on the recipe name. (the main app component should also have a state that deals with all the recipes in the browser storage, but that is something I'll come to later)

Set up a toggle function that fires upon clicking the header containing the recipe name and switches the Recipe component's 'display' state to either true or false depending on its current state. This is then passed to the child Ingredients component as a prop. Ingredients then displays a div with either a list of ingredients, or a blank none displaying div, depending on that prop's value.

Next up I need to be able to add, edit, and delete the recipes. This means setting them up as a component state. I think I'm going to again let the top component, App, handle the state as it owns the Add button - it can handle talking to the browser storage, then pass the data onto its child, RecipeList, which then renders as many Recipe components as it has to. First of all, I want to put my default recipes into the browser storage. I imagine I'll only want to do this the first time a user visits, as on any subsequent visits I'll want to load any changes they made.

Set up the componentDidMount function inside the App component and set it to store the initial data inside of the local storage. Had trouble with passing through the data as it's an array of objects, found that JSON.stringify and JSON.parse would fix it. The function checks if a 'recipes' property exists in localStorage - if not, it sets it to the default list. Then it takes the recipe list from local storage and sets it as the App component's state.

Now to make changes to it. There are three things we need to be able to do:

* add a recipe
* edit a recipe (change its name, add ingredients, or remove ingredients)
* delete a recipe

I think I will focus on deleting first as this seems like it will be the most basic one of the three, not requing any user input other than a button press. Created a deleteRecipe function in the Ingredients component as this contains the delete button, then an onDelete function in the App component that will handle talking to the local storage and resetting the state. onDelete then gets passed down to Ingredients through the components (App>RecipeList>Recipe(multiple instances)>Ingredients). onDelete then fires when I click any of the delete buttons. So far it just displays an alert with the name of the recipe to delete on it, to prove it was working ok.

Now it needs to go into localStorage and find the recipe that triggered onDelete (passed to it as a parameter named 'recipe'). The 'recipes' key inside localStorage contains an array of objects, each an individual recipe, and each with a 'name' property, one of which should match the triggering recipe. Since the container for all of these is an array, I took the current recipe list from local storage and used filter() on it to make a new array that does not contain the recipe to be deleted. This array then goes back into local storage, then the App component's state updates and the recipe is removed from the page, and stays removed upon refresh.

The add and edit functions are a bit more complicated as they will require working with user input. This will require adding a popup box, prompting the user for a name, parsing a list of ingredients (comma seperated in the example version, I'll probably do the same), then turning all that into a recipe object and passing it to local storage. First off, I need to create the popup. I'm guessing this will be a child component of App that will only render if the "add" button is clicked, in the same way that the ingredients don't display unless you click the parent recipe name. Set up a basic popup box that sits on top of the rest of the app and can be toggled on and off.

Next step is to add a form so the user can add a recipe. I put in a basic form with fields for a name and ingredients and set up an onSubmit function in the component that would take the input. Again, created an function in App (addRecipe) that gets passed to Add and fires from Add's onSubmit. Tested it out (passing variables through and setting the display state to false so the popup doesn't stick around) and the name/ingredients variables are passing through, next step will be to do something with them.

**Thoughts:** Having a process of events to follow (start static, work out data flow) is very helpful. I feel like I'm following a logical order rather than looking at a huge pile of things to do and no idea where to begin.

**Link to work:** [Recipe Box](https://codepen.io/jsanderson/pen/rGpYze)

### Day 1: October 03/10/17

**Today's Progress:** Continuing the camper leaderboard. I need to work out the toggle function, which means passing to a child component (Header) of the main, state owning component (App). The header contains the buttons that toggle whether to sort by last 30 days or all time, which should then trigger a new call in the app component to the API and update its state/re-render. This has tripped me up so far but I think I'm understanding it as such:

* Inside the parent App component, create a function that will handle the new API call (here called onSwitch)
* Pass this function to the child Header as a prop in the parent's render function (onSwitch={this.onSwitch})
* Inside the child Header component, create a function to handle the button clicks (here called onClick)
* Inside onClick, get which of the buttons was clicked, then pass that to onSwitch (this.props.onSwitch(clicked);)

And this should work. It should also sound pretty obvious to anyone who knows React but I'm still wrapping my head around the data flow. Tested it out, then set up toggling, which was very easy, just the same as the componentDidMount function but with a variable URL. The app now has full functionality. Added some styling and it's all ready to go.

Next up is the recipe box challenge which will involve working with the brower's local storage. I haven't dealt with this before so will do some reading.

**Thoughts:** I love it when murky things finally click. This project really helped me make sense of state, props, and data flow back and forth. I now feel comfortable that I know where an app's state should sit, and how to pass data up and down the DOM tree.

**Link to work:** [Camper Leaderboard](https://codepen.io/jsanderson/pen/NavZeb)

### Day 0: October 02/10/17

**Today's Progress:** Back once again for round two!

I'm ready to get started with the camper leaderboard. Started off the day with a read of [Thinking in React](https://reactjs.org/docs/thinking-in-react.html) to get me going. It reccomends starting with a static version of the app you want to create and adding the interactivity to that. As luck would have it, the example app functions a lot like the finished camper leaderboard, in both cases making calls to an API and listing details in a table. I grabbed some static data from the API (the first few items in the array it returns) and put together an app with nested components. This game me some practice with passing props around - there is no state at the moment since this is a static page.

Now that's going I need to think about state. I also want to run a call to FCC's camper API when the page first loads. Judging by the user stories, this default run will show the top 100 users in descending order based upon their 30 day point totals. I want to set the app up so that it calls the camper API rather than running from a static list. I can then toggle it in the header, where I have placed sort buttons to do that.

Set up the initial call (which also gave me a chance to call the API without using JQuery for a change) and got the data back - now I have all 100 top users. While I was at it I noticed I didn't have a ranking number for each user, which the example did. This turned out to be easy to impliment with the forEach method I was using to return the table rows for rendering, so I added it in.

Thinking in React's next step is to identify the minimal state of the app. My guess that would be if we are getting data from the last 30 days or all time (they are different endpoints on FCC's API). The component that renders this state is the leader table (which then renders in turn a row for each person in the state array), while the header component would be in charge of toggling the state between the two endpoints. These are both sibling components and their parent is the main App component. Thus App is presumably where the state lives, according to TiR's guidelines.

The next problem is how to make an API call within the app. Doing some [reading](https://daveceddia.com/ajax-requests-in-react/), may give Axios a try and get into promises. I managed to place a call in componentDidMount, but I can't set the state in the promise function. More reading. Turns out I forgot to bind "this" to the promise ('.bind(this)' after the call, for future reference).

**Thoughts:** Can I pull this off through NaNoWriMo and holidays? Yes. Yes I can.

I'm liking having Thinking in React as a guide. It's tempting to go look up the answers and follow through what someone else does. But the TiR guide takes you through the best practice and gives tips for how to set up your own page based upon the example it gives (such as above where I had to identify which component owns the state). I'm finding that very often getting something to work isn't the hard part, but getting it to work according to best practice is.

I'm surprised and impressed with how fast this is going.

**Link to work:** [Camper Leaderboard](https://codepen.io/jsanderson/pen/NavZeb)
