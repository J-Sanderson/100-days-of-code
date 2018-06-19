# 100 Days Of Code Round 2 - Log

### Day 70: June 19 2018

**Today's Progress:** Working my way through the Redux portion of FCC's new sections. Threw together another layout, a 24 hour clock with a varying background depending on the hour.

Decided to jump in with the one outstanding FCC frontend project, the drum machine. It turned out to be surprisingly quick, taking only a couple of hours. Decided to implement it in JQuery, anything more complex felt like overkill.

**Thoughts:** Not the most functional thing, but it looks nice and was fun to build as a random challenge.

Redux isn't quite sinking in yet but I think I need to actually use it to grasp the idea behind it.

**Link to work:** [24 Hour Clock](https://codepen.io/jsanderson/full/MXrLbd/) - [drum machine](https://codepen.io/jsanderson/full/QxaRoR/)

### Day 69: June 14 2018

**Today's Progress:** Got the CSS grid cards looking nice. Got started on the new challenges for FCC's frontend certification and worked through the React lesson.

**Thoughts:** Good to get a refresher on React as it's been a few months since I touched it. That's why I keep wanting to make smaller things. I don't want to lose those skills.

**Link to work:** [CSS Grid cards](https://codepen.io/jsanderson/full/oywEGJ/)

### Day 68: June 13 2018

**Today's Progress:** Worked on the new algorithm scripting challenges for FCC. Mainly just catching up to where I was before.

Took a break and did some layout testing with CSS grid to keep myself on track with making things.

**Thoughts:** Not much to say but there's a few interesting new things popping up.

**Link to work:** [CSS Grid cards](https://codepen.io/jsanderson/full/oywEGJ/)

### Day 67: June 08 2018

**Today's Progress:** Finished off the last of the responsive frontend challenges, the technical documentation page. This one went really quickly. That's all for the new responsive frontend certification.

**Thoughts:** That one felt a little anticlimatic, but it was a docs page, so it's not meant to be fancy.

**Link to work:** [Technical documentation page](https://codepen.io/jsanderson/full/wXzNEQ/)

### Day 66: June 07 2018

**Today's Progress:** Added some basic styling for the poll app. It's not exactly nice to look at, but there is some organisation there that wasn't there before, and it'll make a good basis for adding in the charts.

Added in the charts via Chart.js. Technically this fulfils all the user stories but I still want some pagination setting up so the pages don't get overloaded. But I may do that once I have a better handle on what I'm doing here.

Finished off the styling to make it look better. I think I will call this one done. There is still a lot to do (like the abovementioned pagination) but I think I've done as much as I can with my current skillset. I will probably come back to this later and do some overhauling. For now I'll focus on the new challenges.

Finished off the product landing page mockup.

**Thoughts:** I'm happy so far but I think adding in the charts is going to be another complexity leap because one of the hardest parts of this project is learning how the different components "talk" to one another. So I'm going to have to work out how to get the database information to a front end script to generate the chart.

I wrote all of that before deciding to just scrape the DOM. I'm not entirely happy with that solution but it works for something small like this. I suspect once I have a better idea of what I'm doing I'll be fixing a lot, but I'll probably get better at it once I've worked through the updated curriculum. I still don't regret doing it; it was a wobbly start but lots of interesting new ground to tread.

Chart.js is nicely intuitive, I didn't do much more than copy in the sample chart, feed in the correct data, and fiddle with the options, but it was fun to play with it and I found it easy to pick up.

Quite happy with the landing page mockup. I keep trying to strike a balance between what I like and common layouts for this sort of page as I do feel a lot of these sites are very samey. I think I pulled it off here.

**Link to work:** [Voting app](https://jsanderson-voting.glitch.me/) - [product landing page](https://codepen.io/jsanderson/full/zaBeao/)

### Day 65: June 06 2018

**Today's Progress:** Added in the new poll option functionality, and also allowed unathenticated users to vote. This fulfils most of the user stories apart from the visible charts, but this will be added in when styling.

Worked on the landing page project for the new FCC challenges. Got a decent looking layout going on.

**Thoughts:** I'm admittedly surprised that the routes are all set up. I keep thinking there should be something else to do, but the whole thing is functional now.

Although it could do with some pagination for the poll lists. There's not a lot now but it could quickly get out of control.

**Link to work:** [Voting app](https://jsanderson-voting.glitch.me/) - [product landing page](https://codepen.io/jsanderson/full/zaBeao/)

### Day 64: June 05 2018

**Today's Progress:** Set up the voting voutes so that a user can only vote once. There's two checks - the poll page won't display the vote buttons if the user has voted, and the route will check on retreiving the poll if the user's ID is already listed inside it, and only update if it is not.

Next up is the ability to add new options to an existing poll.

**Thoughts:** It works and that's the important thing.

**Link to work:** [Voting app](https://jsanderson-voting.glitch.me/)

### Day 63: June 04 2018

**Today's Progress:** Worked on a voting route for the voting app. Works so far, and this time it redirects properly too. Still needs some checks to make sure that no logged in person can vote more than once, but the basic principle is there and works.

Went back to the new FCC responsive design challenges and finished up the first of the ones I'm missing, the survey form.

**Thoughts:** I suspect this votting app is going to be one huge mess behind the scenes once it's done, but eh, it's my first time working on this scale. It's not going to be elegant. Save that for later.

Going back to the responsive design challenges is interesting. I was worried that it would feel too much like a step backwards, but there's plenty of new things like flexbox and CSS grid to work with, so it still feels fresh.

**Link to work:** [Voting app](https://jsanderson-voting.glitch.me/) - [Survey page](https://codepen.io/jsanderson/full/RJroBm/)

### Day 62: May 31 2018

**Today's Progress:** Attempted to set up a delete function. This turned out to be a major pain. As far as I can tell, the delete route is doing exactly what it's meant to and deleting the poll, but the Ajax request that triggers is still returns an error, and I can't redirect to another page afterwards. I had to settle eventually for putting the redirect request in the Ajax call's error handler. It works at least but even after all this reading I can't work out what the problem is.

**Thoughts:** That was a mess and I hate the solution even if it works. But the only other way I could manage it was to make a GET request, which worked but isn't the right thing to do here. So I'm stuck with whatever works until I can figure out something better...

Also I made a mistake last time, the voting app is still in the curriculum but as part of the take home challenges and not the main certification. That's making it tempting to leave it on the side for now. But I've invested enough frustration in this thing as it is, I can't stop now! Maybe I'll just slow down and work on the existing certifications too.

**Link to work:** [Voting app](https://jsanderson-voting.glitch.me/)

### Day 61: May 31 2018

**Today's Progress:** Polls now display in decending order on a user's profile. There is also an "all polls" page that displays every poll - this will probably need pagination later.

Worked on the redirection after creating a poll. I wanted it to go to the page for that poll, but I'm still having trouble working out how to pass around all the required information so right now it just redirects back to the user's profile.

Next up I want to allow a user to delete a poll they no longer want.

**Thoughts:** Still a bit disjointed but I think things are going to make sense as I keep going.

Whilst checking user stories I noticed that FCC has changed curriculum and no longer has this project as a requirement. I should probably finish it anyway, but I think I would like to explore what's new - there may be something that works as a better introduction to back end work.

**Link to work:** [Voting app](https://jsanderson-voting.glitch.me/)

### Day 60: May 30 2018

**Today's Progress:** Worked on making sure that the polls could be saved with options. Took some fiddling about with converting the initial string into an object with option/votecount pairs, but it works, and polls can now be saved with all the required details. But right now that's all that can be done - we can't even see them without looking at the database. That's not much use at all. Next up I will want to have a user's polls display on their profile, which will mean searching the database for every poll they have created upon loading it.

**Thoughts:** Everything feels like small steps right now but they also feel manageable, a big step up from last time. I think I can do this now.

**Link to work:** [Voting app](https://jsanderson-voting.glitch.me/)

### Day 59: May 26 2018

**Today's Progress:** Trying to set up the ability to create polls - got a schema/model for polls, although right now it only records the title and the person who created it. The rest can wait until it's working ok. Spent some time trying to fire off an ajax request from the create page form. Feels like a mess but I finally got it running and got the post route to fire, and I can now save a copy of the poll to the database. Now the polls need some more detail so they're not just names, but that was a big step.

**Thoughts:** This was a real low point where I felt like giving up. I wasn't going to but it was hard going anyway. I'm still unsure of where I'm going but I have some idea now.

I think the hard part is that I have some idea of how to work all these different technologies but not so much on how to hook them all together. I think that will come in time but right now it still feels like strange magic.

**Link to work:** [Voting app](https://jsanderson-voting.glitch.me/)

### Day 58: May 25 2018

**Today's Progress:** Continued to work through the videos and managed to setup a very bare bones app that you can log in and out of. Great! But you can't do anything yet so here comes the rest. Users need to be able to make polls, which is going to mean setting up another schema and all that fun.

**Thoughts:** I'm worried that I still don't know much about how Passport works, I just coded along with the videos, but I have several more projects to fully understand it. I'll get somewhere.

The next steps of this project are a bit intimidating because I'm back on my own, but this is stuff I should already be able to do. The only thing that was really intimidating me was Passport and the Google authentication because I had never touched it before. The rest is stuff I've already got.

**Link to work:** [Voting app](https://jsanderson-voting.glitch.me/)

### Day 57: May 23 2018

**Today's Progress:** Did some work on the voting app, following on with a playlist from the Net Ninja that I linked the previous day. It isn't totally set up, but now I have a database setup and some authentication from Google, and it appears to be working.

**Thoughts:** I love these videos. Everything is so clear!

### Day 56: May 21 2018

**Today's Progress:** Didn't have time to work on the voting app but did find some time to work on learning how to create Sankey diagrams with D3 for some work stuff, and created a test version to play around with.

I should also watch [these](https://forum.freecodecamp.org/t/good-passport-tutorial-net-ninja-on-youtube/175699).

**Thoughts:** Well hey, it's useful. Now make the thing you're meant to make, self!

**Link to work:** [Sankey diagram test](https://codepen.io/jsanderson/full/yjZdpG/)

### Day 55: May 20 2018

**Today's Progress:** Decided to make a start on the first of the advanced backend challenges, the voting app. This is a big step. So far I just set up some basic routes in Express, similar to the API challenges. There is a lot yet to come. I think first of all I want to look into how to allow someone to log in as an authenticated user. [This](https://scotch.io/tutorials/easy-node-authentication-google) and [this](http://www.passportjs.org/docs/) may be good reading.

**Thoughts:** This one's intimidating enough that I went back to do all the data visualisation challenges as a form of stalling, and I'm still trying to work out where to go. I think this challenge trips up a lot of people because it feels like a sudden spike in complexity. But I don't know if that's true, or just a perceived thing due to user authentication being new at this point. We will see. This may be slow going but I don't want to stop outright.

### Day 54: May 16 2018

**Today's Progress:** Added tooltips and styling to the map. Calling this one done, too.

**Thoughts:** That's the data visualisation challenges all wrapped up. It feels like they went a bit too fast. I want to work more with D3 because I feel like I only touched upon the basics of what it can do. But I also don't want to stall on the rest of the backend challenges that are still waiting for me. I'll have to keep balancing things.

Still. Wow. Another certification down!

**Link to work:** [Global meteorite landings](https://codepen.io/jsanderson/full/xjaxPj/)

### Day 53: May 15 2018

**Today's Progress:** Tried starting fresh with the mapping challenge, finally got it to work after studying some examples, and also managed to get some basic pan/zoom behaviour. Now I can get started with the meteorite data.

Imported the data and managed to get it to show, which was a lot quicker and easier than can be said for the base map. But the points need some functionality, right now they're a load of black blobs that nobody wants to look at. I looked up how to render them as circles instead and apply the co-ordinates properly, and set up a scale for meteorite mass, though that was tricky to get right due to the wide range. Finally managed to get something working and looking reasonable. Next up will be getting some tooltips so I have more than just a load of circles.

**Thoughts:** Finally, some progress with this thing. I'm still not satisfied with how much I understand what's going on; I may try some more maps after this one.

**Link to work:** [Global meteorite landings](https://codepen.io/jsanderson/full/xjaxPj/)

### Day 52: May 14 2018

**Today's Progress:** Working some more on the mapping challenge. Not going well, the geoJSON does load but something is wrong when I try to draw paths and I still haven't worked out what. Kept trying several geoJSOn sources and not having any luck.

**Thoughts:** Aaaaaaaargh.

### Day 51: May 11 2018

**Today's Progress:** Did some more work with force directed graphs using some data from work. No links because it's work info, but found it quite helpful to try another graph and see how much I'd learnt; many things were much clearer the second time around, including how forceLink works.

Next up is the mapping challenge so I'm reading some more about how to do that. Reading through [this](https://maptimeboston.github.io/d3-maptime/#/62) and trying to follow through with some geoJSON data generated [here](https://geojson-maps.ash.ms/). Not worring about the meteorite data right now, I'm focusing on getting the basic map to work.

**Thoughts:** I liked doing some non-FCC work with D3, it was good for getting a handle on what I'm doing.

The mapping challenge is very exciting! I'm looking at some [interesting things](https://www.jasondavies.com/maps/transition/) and getting really excited. I love maps. The actual how to is a bit opaque here but that should improve with time.

### Day 50: May 10 2018

**Today's Progress:** Trying to get the flags to display. This was hard, I didn't realise at first that images couldn't be added to the svg, and once I added them as divs instead, they kept refusing to move. Spent too long on the JS, turned out I needed to work with the CSS positioning. Once that was fixed and they had proper margins and absolute positioning instead, the graph looked fine.

Added in some styling, this was fairly quick as there wasn't much to sort out.

**Thoughts:** Frustrating, I nearly wanted to start over a few times. Need to remember that the issue may not always be where I think it should be. But I'm happy this is sorted now.

**Link to work:** [Force directed graph](https://codepen.io/jsanderson/pen/RyjVWr)

### Day 49: May 08 2018

**Today's Progress:** Doing some [reading](http://www.puzzlr.org/basics-of-d3-force-directed-graphs/) about force directed graphs in D3 and trying to apply it to what I have so far. Managed to fix an issue with lines not displaying, now I have another problem with the nodes all going off the edge of the graph. I can drag them back but it's not useful or how it needs to be. Managed to figure out how to set maximum link distance and add in some bounding behaviour so nothing floats off.

Next up is working out what to do with the flags. So far everything's been on the svg, this time it seems things need to be different.

**Thoughts:** There's a long way to go but things are feeling a bit clearer now.

**Link to work:** [Force directed graph](https://codepen.io/jsanderson/pen/RyjVWr)

### Day 48: May 07 2018

**Today's Progress:** Started on the force directed graph. This is something very new to me, everything else was a concept I'd already encountered and had little difficulty applying to the projects, but this time I'm more lost. I've been going through the example linked yesterday and looking up the documentation for anything I'm unfamiliar with. Doing that I've managed to get a very rudimentary graph going, but there is still a lot to do.

**Thoughts:** This has gone from everything being in hand to an overwhelming new world. But it's kind of exciting too.

**Link to work:** [Force directed graph](https://codepen.io/jsanderson/pen/RyjVWr)

### Day 48: May 06 2018

**Today's Progress:** Added styling to the heatmap, calling this one done.

I was happy enough with d3tip's speed and positioning that I went back and edited my two previous challenges to use it as well. Normally I wouldn't worry about going back unless there was a serious bug, but I liked it enough it was worth the time.

Next up is the force directed graph. [This](https://bl.ocks.org/mbostock/4062045) looks like a good starting point for reference.

**Thoughts:** Feeling very satisfied overall.

**Link to work:** [Heatmap](https://codepen.io/jsanderson/pen/ELWzKW)

### Day 47: May 05 2018

**Today's Progress:** Fixed an issue with colours not showing correctly in Firefox. Set up the key and tweaked it to look better, added some explanatory text from the FCC original. Everything looks nice, the page just needs some styling.

**Thoughts:** I know this entry looks short, but that's only because it's close to midnight and I used up my brainpower on positioning that key!

**Link to work:** [Heatmap](https://codepen.io/jsanderson/pen/ELWzKW)

### Day 46: May 04 2018

**Today's Progress:** The tooltips were being too laggy, so I decided to try out d3.tip, which I had tried before but ended up not using because I couldn't find an up to date version I could use on Codepen. That was fine before but this time around I needed some speed so I kept looking until I found a version that would work. Set up the tooltips to use it and eveything is going great.

Next set up the colour scales using scaleQuantile and the map now has the correct colour values.  The key still needs working on, that will come next.

**Thoughts:** The colour scale was surprisingly easy, and worked first time... for once. This one feels like another project with the meat of things done. Very satisfying.

**Link to work:** [Heatmap](https://codepen.io/jsanderson/pen/ELWzKW)

### Day 45: May 03 2018

**Today's Progress:** Added boxes to the heatmap, and some test tooltips to check the data is transferring properly. Looking good so far. Next step will be to set up a colour scale and apply it to the boxes, right now they are just one colour. I may also see about setting up tooltips differently this time. They are laggy and seem to vanish before I've moused out of the box.

**Thoughts:** So far everything feels good apart from the tooltips. I guess the basic method I was using the last two times is too slow for a larger dataset?

**Link to work:** [Heatmap](https://codepen.io/jsanderson/pen/ELWzKW)

### Day 45: April 30 2018

**Today's Progress:** Putting together the axes for the heatmap. The year is working ok, but having trouble making the months show up as months. Reading [this](https://stackoverflow.com/questions/20803833/line-chart-d3-js-x-axis-months) to see if I can work out what to do. Using a band scale so far and it seems to work, will see if it still does when I add the data in...

**Thoughts:** Setting up a basic graph feels kind of routine now, though the axis formatting issues are still full of things I don't know.

**Link to work:** [Heatmap](https://codepen.io/jsanderson/pen/ELWzKW)

### Day 44: April 30 2018

**Today's Progress:** Added tooltips to the scatterplot, using the same method as the bar chart. After that added in some styling. Going to call this one done!

**Thoughts:** Everything's pretty much easy going for this one now. Still not happy with the forEach workaround on the labels but still unable to work out what's going on. Annoying.

I'm keeping the styling on these minimal; I don't want to detract from the main point of interest which should obviously be the chart itself.

Taking a look at the next challenge (heatmap visualisation) and I guess this is going to mean learning how to implement a colour scale. (Also I think the chart is eaier to read when tilted? I find the year/month data seems to make more sense that way. Maybe I will build it as such. [This](http://bl.ocks.org/tjdecke/5558084) also looks worth studying.)

**Link to work:** [Scatterplot](https://codepen.io/jsanderson/full/qYdxJx/)

### Day 43: April 27 2018

**Today's Progress:** Continued work on the scatterplot. First I added in the circles with a small amount of styling to indicate whether the rider had any doping allegations, as with the example chart. Next up was the name labels. This caused some problems as only approximately the last half of the dataset would display. I kept trying to work out the problem but no matter what I changed it didn't make any difference, could not seem to find any other examples of the problem, and there were no error messages displaying. Eventually tried using a forEach function on the dataset and rendering the name labels in there. This did work, but I kept the original enter() function commented out in case I can find out what's wrong.

Once that was done made some tweaks to the chart formatting, seperating out width and height as well as adding different padding variables for each side. Next time I will try to remember to do that earlier. Then added in some axis labels for the x and y axes.

**Thoughts:** Happy with the way the chart is looking and how flexible the scales are, but not pleased about having to use a workaround to get the name labels to show. It works, but it bugs me I'm not doing it the correct way.

**Link to work:** [Scatterplot](https://codepen.io/jsanderson/full/qYdxJx/)

### Day 42: April 24 2018

**Today's Progress:** Started work on the scatterplot graph, which is the next challenge. This time I decided to set up the axes first. I found that setting them up after I made the main body of the chart meant I had to rewrite a lot of things to take into account the padding I would need, so I decided to get the axes up first so I could see how much of the main chart would be dedicated to the data.

**Thoughts:** This already feels smoother than last time. I really think I've got a handle on what I'm doing now.

**Link to work:** [Scatterplot](https://codepen.io/jsanderson/full/qYdxJx/)

### Day 41: April 20 2018

**Today's Progress:** Working on the graphs and fixed the scales by creating two arrays out of the initial nested array, one for each axis. I now have a good enough looking graph, now it needs the bar hover effect specified in the project. Will need to look up how to do that. [This seems like what I'm going for.](http://bl.ocks.org/Caged/6476579)

Ended up going with [this method](http://bl.ocks.org/d3noob/a22c42db65eb00d4e369) as I don't need anything excessively complicated and I may as well learn how to do it with a basic div. Got some nice basic tooltips in there, now the chart is looking good and readable.

Added in some basic styling, and used the chance to try out the new native CSS variables as this project didn't require a preprocessor. I'm going to call this one done.

**Thoughts:** Much better than yesterday, and I have some idea of what I'm doing when I work with a scale now. Also happy to work with some CSS variables. I had been meaning to for a while but the last few projects all specified the usage of SCSS. I miss the nesting but native variables are always good to have.

**Link to work:** [Bar Chart](https://codepen.io/jsanderson/pen/VXQqEm)

### Day 40: April 19 2018

**Today's Progress:** Working on the D3 graphs. I can import the data required and get a basic bar chart going without any problems, but I'm still having trouble with the scales.

**Thoughts:** This is frustrating - I feel like there is a lot I don't properly understand about how scales work, and it's leading me to stumble in the dark. I know this feeling passes when I get a better handle on things, it's the early days like this that are annoying.

### Day 39: April 06 2018

**Today's Progress:** Finished the pixel art so went back to styling the dungeon crawler game, and got something good looking. I think I'm going to call this one done. There's plenty could still be done with this project, but it's time to call it finished and move on properly to the D3 projects.

**Thoughts:** So glad that this one is done - I've never had a project take so much time and energy as this. I do enjoy making things look nice once the functionality is done, even if it feels more trivial. Amongst other things I'm a sculptor, and both a strong framework and good looks are important to a sculpture; this is no different.

**Link to work:** [Roguelike](https://codepen.io/jsanderson/pen/YeyZxx)

### Day 38: March 29 2018

**Today's Progress:** Picking up some more D3 while I continue with pixel art for the roguelike. Worked on axes and now I think I have enough to create a basic chart. Put something together using the first FCC challenge's data (which meant learning to fetch JSON in D3 rather than using hardcoded sets). It looks ok but I need to get better at using scales.

**Thoughts:** Trying to assess if I feel confident enough to start the first FCC D3 challenge now or later... jumping in feels daunting but I figure making something is the best way to learn.

### Day 37: March 28 2018

**Today's Progress:** Coding for the roguelike has been put aside whilst I work on the pixel graphics. Once that's done I can get the stylesheet for the page looking good to match.

In the meantime I am continuing work on D3, picking up some more charting details and learning about scales.

**Thoughts:** D3 is very exciting, glad to be picking up something new. I'm already confident about the first FCC challenge as it's a simple enough bar chart, hopefully I should have enough to do that and keep me coding while I poke at the pixel art. I also think this may be something I can utilise in my day job as I already do a decent amount of data visualisation. Things are looking good!

### Day 36: March 23 2018

**Today's Progress:** Slept on the flickering problem and came back to it. I moved the image loader function into the main app's componentDidMount function and saved the images in the app state when they were all loaded in. These then get passed to the screen component as props and the board is rendered as usual. This seems to have solved the flickering problem and it does seem to be a lot more efficient as the page is not constantly having to fetch the images with each update.

With all that solved I think the only things left to worry about so far are the graphics but I will keep an eye on things if any bugs develop. It'd be nice to also allow the user to move using the arrow keys instead of just the on screen buttons.

While working on some pixel art and testing how it looks, I did find one potential bug - the player seems able to move out of the bounds of the dungeon. I think this is happening at the very edge points - perhaps the collison detection is not accounting for that. Added coordinate logging to the movement function to test it out. Oddly enough I found at one point the randomly placed weapon even spawned out of bounds. I think I can now see what happened - if a room dig is cut off because it reaches the edge, it still registers those array slots as "true" even if it shouldn't be possible to go there. That's a bad bug and one I'm surprised I didn't pick up on earlier. To fix this I added a couple of loops after the main dungeon layout had been generated to ensure all edge tiles are also wall tiles, and ensuring items etc cannot spawn on edge tiles. This seems to stop the "invisible rooms" but I will keep an eye on the issue.

**Thoughts:** I think this is the longest project I've worked on. Thinking for a future project I might rewrite it outside of Codepen, tidy up the code and have some proper modules in there instead of one big blob.

**Link to work:** [Roguelike WIP](https://codepen.io/jsanderson/pen/YeyZxx)

### Day 35: March 22 2018

**Today's Progress:** Did some tweaks to the dungeon tiles. They look a bit nicer but I'm still focused on the image problems. I've tried using the function linked earlier to only draw the screen when all the images are loaded in, which solved the issue with images not loading at all, but added a notable and very uncomfortable flicker sometimes when moving. My guess is the problem is to do with the images all loading each time the screen is drawn, leading to small lags which cause flickering. Not very efficient either. Currently trying to work out how to get around that, put up a help thread on freeCodeCamp.

There is also a possible bug I need to chase down with the player being unable to move in Firefox. I will have to chase this when I have access to a computer running it; right now I am only working on Chrome.

For now I managed to fix the bug where the board does not generate at all. Seems to be a type error where the stairs randomly generate on an edge tile. As the stair generator checks for free space all around, it throws an error when there is nothing at all to one side. Fixed it so that the stairs should always generate at least one tile in from the edge by starting at array position 1 rather than 0.

Not much else to do until I get the flickering sorted so I've started reading up on D3 using [this tutorial set](http://alignedleft.com/tutorials/d3/) in preperation for the next set of challenges.

Later on: managed to get to a system with Firefox and fixed the inability to move bug. One of those stupid errors where you used the wrong variable name again...

**Thoughts:** I really hope I don't need to rewrite anything big! I was so happy I had things working...

But I am happy to be working on D3. I think it's been way too long since I tried something new. I think I was stagnating a bit, picking up a new thing helps the brain go.

### Day 34: March 16 2018

**Today's Progress:** Moving on to layout and appearance. First off fixed the layout so that the screen is in between the status and the controls, and ensuring the status messages default to scrolling to the bottom whenever updated. I like the look of it, it seems vaguely reminiscent of a handheld console now.

I then created some basic pixel graphics and worked on the board rendering so that they display rather than some coloured squares as before. I had always wanted to use pixel art, the squares were just a placeholder. At the moment the graphics are very basic. I'm mostly concerned about whether they display, not what they look like. So far there are wall and floor tiles, the player, stairs, health potions, and an image for each monster and weapon type (I wanted those to be distinct because they are supposed to be different objects/creatures). They work ok, but sometimes don't load. My guess is that the canvas is trying to render them before they have properly loaded, leading to blanks. I'll try testing out loading them in before rendering the canvas to see what that does. ([Possible useful reading](https://www.html5canvastutorials.com/tutorials/html5-canvas-image-loader/)) There are also a few lingering type errors in the dungeon generator code that still need looking at...

**Thoughts:** There are two things here that I'm not happy with. First is that the layout is not responsive, indeed it uses fixed dimensions. I had the same issue with the Game of Life, because they both involve canvas grids. Not sure if there's a way around it, perhaps that is something to explore in a smaller project? Second, I admit I did copy paste the code to get the status div to scroll to the bottom, and I still don't fully understand it. Not great practice there, need to do some more reading on what refs actually do. But aside from those things I'm feeling quite happy.

**Link to work:** [Roguelike WIP](https://codepen.io/jsanderson/pen/YeyZxx)

### Day 33: March 15 2018

**Today's Progress:** Whilst trying to get the monsters to display, I ran into another problem, being that the player cannot move too close to the top or edge of the board, including tiles they should be able to access. This might be the source of all the movement issues I've been having and it seems to tie in to the way the board rendering is set up.

So I need to fix that. Disabled rendering anything except the board and the player, temp altered the player's stats so they can one shot any monsters (important when you're testing and they're currently invisible). It's something to do with the rendering code setting a start value to render from based on where on the board the player is. I found some code that would set it to zero if it was anything less, but of course that means it can't render top/left positions now. No wonder the player doesn't seem to move and all sorts of odd things happen. Removed that code and added a check in the board rendering that the calculated start position for each cell needs to be greater than 0.

This works to some extend - movement is no longer impeded in top/left positions - but cells on the other side of the screen stop rendering, I think because the check stops the whole row or column from rendering rather than just the ones that aren't there to render anyway. Tried moving some of the checks to the outer loop but it didn't make a difference. Going to have to dig deeper.

A little more checking the loops and it seems to be because the loop ends too soon once the starting position goes below zero. Fixed that so it will not end until the board size is reached. Now I seem to have free motion of the board. Time to put everything back on it. Adding the weapon and the stairs was easy enough. Now I'm back to fixing the monsters. I had some trouble so I tested by rendering just the first monster on the list. Once that was working I set a loop to render all the monsters. I then managed to do the same for the heals.

Now everything seems to work ok, the game is playable again, but I hit another snag - on hitting either of the replay options (continue after a win or death) the board does not render. I can't see why this should happen as nothing changed in the board setup code, just the rendering, but something is off. Checking error messages and it seems like nothing (or at least not the board) is getting passed to the screen component. However, moving just once causes the board to poperly generate with a new game which then seems to work ok. This probably has something to do with the reset function (triggered by restarting a game) sets everything back to default, including making the board into a blank array - but why then does this not happen in the old version without the zoomed in screen? Not sure, but removing the board reset seems to help. Going to have to keep an eye on this one.

But if that's all the issues I'm having, it seems that the rest of the work should be cosmetic.

**Thoughts:** I hope all those words above make sense...

Everything else aside, I'm happy that one of the biggest challenges so far has been (apparently) sorted. I feel like another milestone is down.

**Link to work:** [Roguelike WIP](https://codepen.io/jsanderson/pen/YeyZxx)

### Day 32: March 07 2018

**Today's Progress:** Managed to work out how to get the weapon to display in the right place. The character is also able to move into it and pick it up. Did the same to add in the stairs as they are placed in the same way as the weapon (a single item that is in a fixed spot) and they also work. Mostly...

Still running into issues with the player character not always rendering, or showing up in the wrong spot. I have yet to work out the problem, but I have noticed that when it happens, the weapon and stairs also vanish (but may still be interacted with). So I can tell that something is breaking that has a knock on effect with everything that should be rendered afterwards.

This showed that the rendering seems to stop somewhere in the board rendering section, and thus it never moves on to rendering anything but the board layout.

Further testing and it seems that the error occurs when the player moves into certain spots, but I have yet to work out what it is about them that causes it. Error handling in the rendering doesn't seem to be bringing anything to light. But it's another thing to think of. Going to try logging the player's position on the board with each step and seeing if a pattern shows.

There appears to be a cutoff when the playerPos.colPos variable (meaning in this situation what column the player is in) goes any higher than 22 - that's just under half the board size of 45. So something is happening to stop rendering when the player's position is on the right hand size of the board. If the player is on a column position of 22, the board starts drawing from column 13 in the board array, and ends at column 33. This seems to go ok.

And I think I have it - it's the error handing statement causing a return and stopping the render at that point, and errors are common due to the numbers involved outstepping the bounds of the board array. Instead of relying on error handling to solve the problem, I should have written the board rendering in such a way that I didn't need to - throwing in a try/catch statement was just lazy coding. Time to fix that. Set up a proper check when deciding whether to render a tile, and that problem has gone away.

There is still the issue of the player not always being able to move correctly across the board - moving on to wall tiles, being unable to move in free ones, as if the board is different to what we see. I will need to work out what's going on - perhaps it IS rendering the wrong board because something isn't updating?

**Thoughts:** It's a nothing works day. It's okay. We'll make it. I love a good puzzle.

### Day 32: March 06 2018

**Today's Progress:** Attempting to add things to the dungeon layout starting with the player character. Managed to get the player to display but on some occasions it does not show in the correct place, unsure why. Moving on for now to unstick things, I need to add more items. This is harder because the player is always at the centre of the screen, but the other items (stairs, heals, monsters, weapons) are in specific locations.

**Thoughts:** This part is a challenge and it sometimes feels tempting to not do the zoomed in thing... but I feel like that would be giving up. Don't want to go there.

### Day 31: March 02 2018

**Today's Progress:** Added death and victory popup boxes to the game and set the controls so that the player can no longer move and thus continue playing when either state has been reached.

I wanted to complete both these messages with a "Play again?" button so the player can restart without having to reload the page. The problem I'm now having is getting the state to update again to reset it back to its defaults, then calling the board setup function. As it stands the state is not properly updated, so the game thinks you are moving on to the next floor. Did some looking around and found that you can pass callbacks to setState, which solved everything immediately. Once that was resolved I added the same functionality to the win message.

The next step is to rework the canvas rendering function so that we can only see a small part of the dungeon at any one time. Did a rough mockup that just shows the dungeon layout, it is mostly working ok but falls apart when I try to add the player character and move them about. I think this will need some extra thought. Probably time to break out the graph paper.

**Thoughts:** I love it when what looks like a big problem has an easy solution.

Funny moment: setting the boss stats low for testing the win message, leading to a situatuion where you can slap a dragon to death in one hit.

I'm a bit intimidated by fixing the canvas as it will involve reworking a lot of code, but I'll be okay. It's not beyond me to figure it out.

**Link to work:** [Roguelike WIP](https://codepen.io/jsanderson/pen/YeyZxx)

### Day 30: February 23 2018

**Today's Progress:** Started out on the cleanup by making a "do you want to go down the stairs?" component that renders when the player bumps into a stair tile, rather than an alert box as was previously used. The box has basic styling like everything else right now, but should look nice with some proper styling later.

Next, to add some death and victory boxes that render in much the same way.

**Thoughts:** I ended up going back to my recipe box project to remember how to do components that only render at certain times. That was kind of embarassing but I think asking "how did I do this again?" is more common than people want to accept. Past you is a different person. Anyway, they were nice and easy to set up once I had it figured out. I expected an awkward logic snarl when replacing the alert, but it was all very smooth.

One thing that is annoying is the length of the code for this project, which is my longest so far. If I were not using Codepen, I would have split this thing up into modules ages ago.

**Link to work:** [Roguelike WIP](https://codepen.io/jsanderson/pen/YeyZxx)

### Day 29: February 14 2018

**Today's Progress:** Some small tweaks to monster stats and the game feels playable but reasonably challenging. Fixed the log so that it now displays as a list rather than an unbroken stream of text, and whilst it still needs some fixes it is a lot more readable.

For the last gameplay critical element I added in a boss monster that spawns on the final floor. It has unique messages and displays a "you won!" message when deleted, although there still needs to be a proper win screen. I'll handle that when working on the death screens as they will have similar "play again?" functionality.

The game is now reasonably complete but still very bare bones and nowhere near done. Things to work on next:

* a pop-up component for going down stairs rather than the basic alert I'm using right now.
* death and win screens that properly disable play and offer a new game. Theoretically it should still be possible to continue playing after death since all that happens is the screen no longer renders, and winning does nothing but add a "You won!" message to the log. Boring!
* the board should only render part of the dungeon, centred on the player, rather than all of it as it does now.

**Thoughts:** Very glad that I have basic gameplay sorted, although the list of things to do now is a little intimidating - there's a lot of new things to write. But not so intimidating that I can't do it. I think I have a handle on this now.

**Link to work:** [Roguelike WIP](https://codepen.io/jsanderson/pen/YeyZxx)

### Day 28: February 12 2018

**Today's Progress:** Adding more to the gameplay from the list I made last time. Each floor now spawns a weapon which can be picked up and adds to the player's strength. Also each floor will now spawn a progressively stronger monster than the last one to make it more of a challenge. Most have placeholder names and stats but that can get fixed later. There's also a nice amount of silliness, especially on the last floor...

Weapon spawning/pickup is easy enough, the same choosing a free square to place it and the same collision detection that tells the game if the player has hit a monster or the stairs. I will still need to tweak placements though so that things don't spawn on top of other things.

All that's left to spawn now is healing items. This should be the same as the monster placement loop - get square, check it's free, place item. Added that in, the code is just repurposed monster placement.

The last gameplay vital things to add are levels/EXP and death. Added a basic level system that lets you gain EXP based on the monster's attack stat (this is probably going to be temporary, I'll figure something else out later - if nothing else maybe the EXP should be slightly random). The player stats now contain a toNextLevel figure that decrements with EXP gained and allows levelling up if it passes 0. The status panel also shows how much more EXP the player needs to gain to level up.

Finally, we need a death function so that the player can't continue with negative HP. For now I set the screen component to only display the board if the player has more than 0HP. In the future I would like to update this to show a death screen and give the option to continue but for now this will do.

There is one more gameplay aspect left: the boss monster in the final dungeon - but I want to ensure the game is balanced enough to get you there with enough of a challenge to make it fun. A quick playtest and I think I need to better scale the heals to the dungeon floor. They become too useless later on. But it does so far seem to be reasonably well balanced.

**Thoughts:** Forget the bats. The rabbits are worse.

Starting to think the code is getting overly complex again. Trying not to worry about it, getting it to work is most important right now but I think there are some areas that could do to be more concise.

**Link to work:** [Roguelike WIP](https://codepen.io/jsanderson/pen/YeyZxx)

### Day 27: February 09 2018

**Today's Progress:** More monster placement. Monsters now display on the board and will only spawn in free spaces (though I have yet to tweak the stair/player placement so they do not spawn on top of a monster - put in a note to myself to add that later). Each monster is an object inside an array which so far contains the row and column position of the monster, the type (an index number that corresponds to the monster type array constant, which holds the name and stats for that monster species) and whether or not the board canvas renders it (this is true to begin with and will be set to false when defeated so it can no longer be seen or interacted with).

Now we need to be able to fight them! Wrote collision detection into the movement function so that it triggers a fightMonster function when bumping into an undefeated monster. This displays a message that you have been attacked, switches the monster's display property to false (meaning defeated) and updates the board. We can now walk around one shotting bats. But where's the fun in that? We need to actually fight. I set up a combat structure where the player does damage within a random range and can hit the monster, taking away HP and eventually defeating it. Next added in functionality for the monster to do the same to the player and possibly reduce their HP to 0, therefore killing them.

Next up:

* have some actual consequences for dying rather than a "You died!" message - right now you can keep going with negative HP. Wipe the whole board and make the player start over. Probably do this in a seperate death function.
* let the player gain EXP for defeating the monster and level up, giving HP and attack increases.
* scatter health items around the dungeon so we can heal.
* drop a weapon somewhere in the dungeon that we can pick up and get an attack bonus from.
* fix the play log so that there are actual line breaks in there.

**Thoughts:** I think I made the bats too hardcore.

**Link to work:** [Roguelike WIP](https://codepen.io/jsanderson/pen/YeyZxx)

### Day 26: February 08 2018

**Today's Progress:** Very quick check in today to set up some monster functionality. Generating the board now generates an array of monsters, though at the moment there are no stats associated with them or consideration for placement. The goal right now is to have them just show on the board, then I can find tune that and add combat functionality.

**Thoughts:** Not much done but a quick check in is always good to keep motivation up.

**Link to work:** [Roguelike WIP](https://codepen.io/jsanderson/pen/YeyZxx)

### Day 26: February 06 2018

**Today's Progress** Now that I have some basic functionality - dungeon generation, stairs, and movement - the game needs some action. First of all I created a playerStats object in the state to hold things such as the player's current HP, level, weapon, etc. This should be visible to the player so I set up a Status component above the board to display these things. So far it just shows the floor and current HP - weapons etc haven't been implemented yet.

The example project from FCC has the final boss on the fifth floor. I think I will do the same, so that the game has a defined endpoint. Set up a conditional so that the stairs will only place if the floor number is less than five. Also made sure that the dungeon generator is keeping proper track of what floor we're on - this way it can generate stronger and more challenging monsters the further down we go.

Now for some actual monsters. Set up an array constant to hold some weapon stats and another one to hold monster stats. (Feeling a little silly, because games are more fun with a little silliness, I named the starting weapon and monster the "Pointed Stick" and the "Ubiquitous Bat" respectively. Perhaps a later weapon will be a sharp slice of mango.) Set the game to display the palyer's HP and weapon.

I'd also like a scrolling status log that displays messages, like welcoming the player to the game, describing fights blow by blow, etc (what's the point of giving the monsters funny names if you can't see them?). Created a statusLog in the app state, which starts out with an empty array. Different events will push strings to this array which will then be displayed in the scrolling log. So far I have added a welcome message and another for going down the stairs. As I add more events such as fighting and picking up items, I will add more messages. (Also need to fix the rendering so that it displays line breaks but that can wait...)

Now I realise I need to think a bit about the maths beyond the player/monster stats and how to implement them. Typical RPG stuff: you have a level, EXP, HP, attack values, and trade blows with monsters who also have HP and attack - but I haven't yet thought about what values to plug in, what level curve to implement, all that stuff. I think it's time to step back from the code and get that all worked out before progressing any further.

**Thoughts:** I'm feeling quite positive about this project. It seems as though most of the big problems are behind me. Of course that could all change fast, but right now it's good. Mixed feelings about not doing this every day, but as everyone seems to want something at work (lots of mapping and visual diagram work) this is a good balance.

One thing is for certain: this challenge is loads of fun!

**Link to work:** [Roguelike WIP](https://codepen.io/jsanderson/pen/YeyZxx)

### Day 25: February 02 2018

**Today's Progress** It's been a while but I have been working on the roguelike React game. I now have the board set up to generate some nice looking random dungeons, and to place some stairs and a player character, which can be moved about with some basic controls, but I am getting various errors where the board does not load for whatever reason. I have decided to strip back the code and tackle things more slowly. Right now I am working on a very stripped back version of the game code. "Gameplay" is moving through a single room to the stairs, going down them (just using an alert box confirmation for now, I will replace it with something fancier later) and entering a newly generated room with new stairs. This lets me test the basics (moving around, generating new levels, placing the character and the stairs) without getting bogged down. I've also taken the chance to rewrite how the character/stairs are represented in the state - objects containing row/column figures corresponding to location, rather than being hardcoded into the board array like they were before, which was unsatisfactory). There's also a level counter variable that goes up by one with each new board, which should come in handy when the game needs to know when to bring out the final boss fight.

So far I've found that there were a lot of errors with the board trying to place rooms etc out of bounds, which was causing it to not render. This now seems to be fixed, it's a simple off by one error. Chrome console is your friend.

Next issue: whilst the stairs and room generate in new random positions with each level, the player character stays in the same place and often ends up inside a wall tile. Thankfully I haven't added in collision detection with walls in the movement function so you can still move around (I guess you're a ghost right now) and get to the stairs, but I need to fix that. My guess is that the player co-ordinates are not updating to the main app state properly.

Upon testing it does seem that the state is not updating with the player co-ordinates. The strange thing is that the other things that get passed to the state (the board layout, stair location, and level counter) pass on normally. I can't figure out why this should happen.

Finally figured it out - the problem was that the character movement function also sets the state at the end, including, if the character walked into stairs, after the board was done setting up. So it would update the character position state after setting up the board, then go back to the movement function and update the state again to the position the character was at. Fixed it by setting it so that the state update in the movement function only triggers if the character did not walk into the stairs.

Following that put collision detection back in, so that the player character can no longer walk through walls. Now to re-implement the dungeon generator so the levels are more interesting than a single room.

Set up the generator so that it "digs" passages and rooms in random directions. Really liking the resultsbut there is an issue - loads of type errors when the  generator digs out of bounds - i.e. outside the array. I think I will need to read up some more on catching errors.

Turned out to be as easy as wrapping the passage/room digging code in a try statement and catching the error with a console message. Playing about with different values for the room size/number constants now to see what gets the best looking results. I now have a very basic game - move around, find the stairs, go to another level with another random dungeon. Not pretty or fun, but it's a start. Next up, populate the dungeon with some stuff!

**Thoughts:** I'm going back to this challenge but for now it will not be everyday, just two or three days a week. I think that's a good balance to keep me going and leave me time for the day job too. So if the dates seem wrong, don't worry, I'm just pacing myself - I find I get a lot done on the days I do work on this project so it evens itself out.

And as always, problems aren't the framework being weird, it's you making a silly mistake.

### Day 24: October 26/10/17

Putting this challenge on hold for a while.

### Day 23: October 25/10/17

**Today's Progress:** Looking for some resources for random dungeon generation. [This](http://bigbadwofl.me/random-dungeon-generator/) may help, also [this](http://www.roguebasin.com/index.php?title=Dungeon-Building_Algorithm). Tried doing some basic setup, so far I can generate an initial chamber but I'm still unsure which one to go for...

**Thoughts:** I keep on feeling really intimidated. Is too much going on at once? It's okay. I have this. It's okay.

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
