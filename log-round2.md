# 100 Days Of Code Round 2 - Log

### Day 2: October 04/10/17

**Today's Progress:** Doing some reading on [local storage](http://htmlui.com/blog/2011-08-23-5-obscure-facts-about-html5-localstorage.html) and it looks easy to implement. Going to put that on one side for now and think about the rest of the app. Adding and removing items seems easy enough. But I also need to display the recipe when the name is clicked. I guess we're learning about conditional rendering today!

To start off with I stuck with Thinking in React's suggestion to create a static version of the app. I set up a basic hierachy with everything I would need, using two recipes (stored within the code for now) to test it. For each recipe there is a single Recipe component which contains the name of the recipe, and then an Ingredients component containing the ingredients list, as well as buttons to edit and delete the recipe. I think that each of these Recipe components should have its own state that determines whether or not the Ingredients component should display, and that is toggled by clicking on the recipe name. (the main app component should also have a state that deals with all the recipes in the browser storage, but that is something I'll come to later)

Set up a toggle function that fires upon clicking the header containing the recipe name and switches the Recipe component's 'display' state to either true or false depending on its current state. This is then passed to the child Ingredients component as a prop. Ingredients then displays a div with either a list of ingredients, or a blank none displaying div, depending on that prop's value.

Next up I need to be able to add, edit, and delete the recipes. This means setting them up as a component state. I think I'm going to again let the top component, App, handle the state as it owns the Add button - it can handle talking to the browser storage, then pass the data onto its child, RecipeList, which then renders as many Recipe components as it has to. First of all, I want to put my default recipes into the browser storage. I imagine I'll only want to do this the first time a user visits, as on any subsequent visits I'll want to load any changes they made.

Set up the componentDidMount function inside the App component and set it to store the initial data inside of the local storage. Had trouble with passing through the data as it's an array of objects, found that JSON.stringify and JSON.parse would fix it. 

**Thoughts:** Having a process of events to follow (start static, work out data flow) is very helpful. I feel like I'm following a logical order rather than looking at a huge pile of things to do and no idea where to begin.

**Link to work:** [Recipe Box](https://codepen.io/jsanderson/pen/WZXERR)

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
