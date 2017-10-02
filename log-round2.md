# 100 Days Of Code Round 2 - Log

### Day 0: October 02/10/17

**Today's Progress:** Back once again for round two!

I'm ready to get started with the camper leaderboard. Started off the day with a read of [Thinking in React](https://reactjs.org/docs/thinking-in-react.html) to get me going. It reccomends starting with a static version of the app you want to create and adding the interactivity to that. As luck would have it, the example app functions a lot like the finished camper leaderboard, in both cases making calls to an API and listing details in a table. I grabbed some static data from the API (the first few items in the array it returns) and put together an app with nested components. This game me some practice with passing props around - there is no state at the moment since this is a static page.

Now that's going I need to think about state. I also want to run a call to FCC's camper API when the page first loads. Judging by the user stories, this default run will show the top 100 users in descending order based upon their 30 day point totals. I want to set the app up so that it calls the camper API rather than running from a static list. I can then toggle it in the header, where I have placed sort buttons to do that.

Set up the initial call (which also gave me a chance to call the API without using JQuery for a change) and got the data back - now I have all 100 top users. While I was at it I noticed I didn't have a ranking number for each user, which the example did.

**Thoughts:** Can I pull this off through NaNoWriMo and holidays? Yes. Yes I can.

**Link to work:** [Camper Leaderboard](https://codepen.io/jsanderson/pen/VMzgRx)
