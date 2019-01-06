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