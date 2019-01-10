# 100 Days Of Code - Log

### Day 0: January 1, 2019 

**Today's Progress**: Worked some puzzles in CodinGame. Finished the Descent Puzzle and started working in Cooders Strike Back

**Thoughts:** I think the concept of the site is fun, but I think the "code within a game" is a little awkward. Especially if you've worked with canvases at all. You don't interact with the canavs. You read input and write output, and the website interprets it through their game engine. I might pick it back up, but I think I'll be focusing on Vue and ASP.NET Core

**Link to work:** [CodeinGame Profile](https://www.codingame.com/profile/ca39e42ddf1ebb943c9a4199a73f3ef51269891)


### Day 1: January 2, 2019 

**Today's Progress**: Dove into Azure's AD B2C authentication system. Scaffolded a Vue app to be authenticated with it.

**Thoughts:** I've worked with auth0 as a Saas, but I'm interested in Azure's offering because I'm trying to learn how Azure does everything. I liked auth0's interface better, but I'm trying to give this method a chance. Azure just has so many different entities in general that it takes some time to understand what I'm doing. Not much code written though. Just a scaffolded app with the basic idea of being a logging app for parenting activities for newborns. (feeding, diaper changes, etc.)

**Link to work:** [Vue App initial repo](https://github.com/Basaingeal/parenting-app-client)

### Day 2: January 3, 2019 

**Today's Progress**: Spent time fiddling with sample projects provided by Azure B2C. Ended up switching to auth0, and adding some prereqs to the client

**Thoughts:** Again, not very much coding. At least not that's worth committing. Trying to integrate with Azure B2C has proven to be a nightmare. I'm going to switch to Auth0, because I've gotten it to work, and they serve my SPA + API needs well. I'll want to figure out how to use their library without using classes if I can help it. Would like to keep all the entities functional. I need to really try to do some actual committable code in the near future. I just feel like there's so much (non-code) set-up I want to do if I don't want to re-write everything. At least getting an authentication scheme and database set up.

**Link to work:** [Vue Parenting App](https://github.com/Basaingeal/parenting-app-client)

### Day 3: January 4, 2019 

**Today's Progress**: Added a service to handle callbacks from the auth0 service

**Thoughts:** I'm looking at the guide for setting up authentication using auth0 and vue. I have a lot of disagreements with the implementation. It ends up making sense, but it's having me pass around the auth service as a prop. It turns the auth service into a state holder with a way to check the auth status on reload. But I don't want to pass around a service as a prop. To me it makes more sense to store auth info in an actual state management system. I should probably stop following guides, learn the auth0-js library and start trying to implement it myself. I keep getting hung up on little issues too. Like whether to use classes, constructor function object, or factory sunctions. Going with a simple factory function now. Tomorrow is Saturday, which will be nice, because I think there 1 hour increments are tough to settle into for solid stretches of work. Should maybe taker a break form auth for a while and just start working on a component, but it's hard for me to do that before I know exactly how auth, data storage, and routing will work.

**Link to work:** [Vue Parenting App](https://github.com/Basaingeal/parenting-app-client)

### Day 4: January 5, 2019 

**Today's Progress**: Implemented authorization with auth0 through VueX

**Thoughts:** I'm really happy with this implementation. The important stuff if stored in local storage so it persists through page reloads. I want to seperate logout logic between the app just forgetting about you, and actively loging out from auth0. Will probably only do the full log out if they hit log out, and will just forget about them on timeout. Timeout might be a week or two though. It's not a banking app after all. Connecting the login to google was easy but parts of it were unintuitive. Google has a customizable consent screen per project, so I'd want to use a different client id for a different app on auth0, but the third party connections seem to be global instead of application scoped. Tomorrow I'll try to set up the API backend and get that authorized too.

**Link to work:** [Vue Parenting App](https://github.com/Basaingeal/parenting-app-client)

### Day 5: January 6, 2019 

**Today's Progress**: Grab user profile and store it. Also add API to the authentication audience.

**Thoughts:** At this point, I'm happy with adding and loging in users. At least the oauth process. I will probably be revamping log-in and welcome screens in the near future. Might do it over a CORS request instead of dirrecting them out of the app. The main thing I'm concerned about is how to represent the user in the database. I feel like I should store the user so that I can join tables to them, but that also might be unnecessary, and all I have to do is reference them by Id. I'll probably need some kind of user profile table at least, so maybe that will fulfil both needs.

**Links to work:** [Vue Parenting App](https://github.com/Basaingeal/parenting-app-client) / [Vue Parenting Backend](https://github.com/Basaingeal/parenting-app-api)

### Day 6: January 7, 2019 

**Today's Progress**: Set up CI/CD on Azure Devops for the client and the api

**Thoughts:** No coding, (I know, I flubbing it a bit, but I can only spend a few hours a day, and there's more to learn than just code.) but I hooked up my Github repos to a CI/CD pipeline on Azure Devops. The api goes to an Azure app service, and the client goes to a $web container in Azure storage. I feel like I really learned a lot about how pipelines work. So much that I feel like I could even set one up at work if I wanted to. The main things that I'm still a bit loose on are how pull-requests factor into thing, how to set up a build-success badge on the readme, when to CD after a CI and when not to, and also where all the variables fit in. Very happy with it though, and it's nice to just commit and access the live sites.

**Links to work:** [Vue Parenting App](https://github.com/Basaingeal/parenting-app-client) / [Vue Parenting Backend](https://github.com/Basaingeal/parenting-app-api)

### Day 7: January 8, 2019 

**Today's Progress**: Break for time with family.

**Thoughts:** Worked 2+ hours yesterday, and wanted to spend some time with the family.

**Links to work:** [Vue Parenting App](https://github.com/Basaingeal/parenting-app-client) / [Vue Parenting Backend](https://github.com/Basaingeal/parenting-app-api)