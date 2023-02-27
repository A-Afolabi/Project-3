# General Assembly Project 3 - FaceCook

## Project Overview

Project 3 was my first full-stack application and the first project built as part of a team. The application created used the MERN stack and included RESTful API. The project had a 9-day duration before needing to be presented to both instructors and other students on the course. While on the software engineering immersive course at General Assembly, this third project was very taxing but also very beneficial and my favourite project. I learned a lot while doing this project, through some struggles, and from my other group members [Tony Haunschmidt](https://github.com/tonyhaunschmidt/) and [Ryan Arnold](https://github.com/RY44). 

As a group, we settled on an idea for our app very quickly. Our app was a social media food app where you could share, favourite and plan meals.


## Deployed Project

[FaceCook](https://facecook.herokuapp.com/) 


## Brief

* Build a Fullstack application by creating your own backend and frontend.
* Use an Express API to serve your data created with MongoDB Mongoose and Node.
* Consume your API with a separate frontend built with React.
* Be a complete product with multiple relationships and CRUD functionality for at least a couple of models.


## Concept

With my previous project still fresh in my mind, I felt the planning phase of this one was something our group would value most if done with a good amount of detail. This was echoed by my other group members and we took the planning stage as a very important and integral part of the project. While planning we were able to have a collective vision of what the final outcome would look like and easily separate the workload into different tasks we could do collectively and individually.

Once ideas were bounced off each other, we settled for the social media food app and then commenced wireframing. This concept came from one of our group members using a food delivery service and speaking about ways he thought it could be better. From there, I mentioned how I often use myFitnessPal to track what I am eating for calories, protein, carbs, etc. This brought about the idea of combining the two with additional features.

The planning process was fairly smooth throughout, with everyone in the team open to ideas and suggestions to ultimately help bring the best version of our vision to life. During the project, we met every day and worked throughout the entire day. There were a lot of late nights but on the weekend we had a more relaxed individual schedule to try and do what we could as a bonus. When working together we regularly utilised VS Code’s Live Share feature so we could minimise conflicts, but on the weekend we just communicated through Slack what we planned to do in our own time.

FaceCook is a social media application with the main purpose being the ability to share and see other recipes. Without the need to log in, users can search and browse through recipes. With an account and logged in, the additional features a user gets are the ability to create and edit a recipe, leave comments, like recipes and follow other faceCook users. In addition, the ability to customise their own profile page, create meal plans and even generate shopping lists.


## Technologies Used

#### Front-end:
* HTML
* CSS/SCSS
* JavaScript (ES6)
* React
* JSX
* Axios
* Google Font
#### Back-end:
* Node.js
* Express
* MongoDB
* Mongoose
* JsonWebToken
* Cloudinary
#### Development Tools:
* VS code
* Insomnia
* Git & GitHub
* Zoom
* Slack
* Trello
* Excalidraw
* Heroku


## Approach Taken

### Day 1-2
#### Planning
This was the first project I was doing where I would be collaborating with others, and as I already mentioned above, planning was an important part of it. During the first day we spent the majority of the time planning out how the app would work, the features we would implement, what was feasible and some stretch goals if time permitted us. Once we had a fair few concrete Ideas that would 100% be implemented, we began to wireframe.

The next day we further touched up on our wireframe, which was done using Excalidraw, by reviewing our ideas from the night before. Once we settled on these we moved on to the branding where we came up with FaceCook. This played off the social media site Facebook and having our meal attributes incorporated in the name. Doing the branding as part of our wireframe helped during the rest of the project, particularly when it came to the front-end. This also helped minimise changes during the process and limited any inconsistencies in our work.

![Screenshot 2023-02-27 at 23 11 39](https://user-images.githubusercontent.com/95321738/221710346-afb69caf-4292-411b-9c53-3c7b6005032f.png)

The wireframe in this much detail helped when it came to reviewing the structure of our project throughout the process of building it. This first became evident during the back-end data structure and then later on during the front-end for functionality and styling. As a group, we completed the back-end together first before moving on to the front-end. This ensured we did not run into any conflicts in our code or inadvertently deviate from the collective direction.

Working in a group of three presented the opportunity to break down the entire project we had agreed upon, into smaller tasks and stages with the use of Trello. We used different colours for our cards to identify what part of the project a task was on, and moved cards to different areas depending on the current status. We also assigned ourselves cards to avoid confusion and make it easy for everyone to keep track of who was doing what.

![Screenshot 2023-02-27 at 23 14 54](https://user-images.githubusercontent.com/95321738/221710771-a2ffe532-4dfd-424a-9670-f6a978a62237.png)

During the whole production process, we had daily stand-up meetings in the morning where we could discuss our progress and issues, aim for the day, and provide support to others. As a group we decided to work on zoom together, muted but able to ask for help quickly if we ran into problems or needed advice. I found this very beneficial throughout the project and I was able to learn a lot from my group members while working on the recipes page in particular. To allocate tasks, we would simply pick something from Trello we wanted or needed to be done first, due to other tickets potentially relying on a task being completed before it could be done. Before picking up a task we would notify each other to ensure we don’t run into any conflicts or issues with picking up a particular task at a certain point.


### Day 3-5 
#### Express
Having a well-planned data structure provided us with clarity when starting and is likely to be a key reason why collectively we managed to complete our back-end in 2 days. In these two days, we created our models for the recipe and user, controllers for the profile, recipes and auth, and config for the routes and secure routes. This allowed us more time when it came to the front-end, something that we felt would be necessary. Although we started a little bit of seeding the data while doing the back-end, once we were all on individual pages, we took some time out each day to do a bit more towards the end of the project.

In order for us to demonstrate all CRUD operations within our controllers, in the example below for our Recipe collection, all routes are secure ones with middleware called before the controller (apart from getOneRecipe controller). While this meant the users needed to be logged in to make these requests, for our delete and edit controllers we needed to ensure the correct owner of the recipe could do this. This is where we added an additional check to do so but also had admin control where faceCook admin users could also delete or edit.

![Screenshot 2023-02-27 at 23 18 11](https://user-images.githubusercontent.com/95321738/221711255-c9356f7c-67cd-41e1-8462-c532e5f10276.png)

With the use of JSON web tokens, we managed to add the secure route middleware to verify the token before using it. This would ensure the token matched the one for the correct user in our database, and if so then be passed by the controller.

![Screenshot 2023-02-27 at 23 20 00](https://user-images.githubusercontent.com/95321738/221711496-499facfa-a12a-4630-87ed-0b4fadd54a36.png)


### Day 6-9
#### React
After working together to complete all of the controllers and routes correctly in the previous two days, we moved on to the front-end where we first began working on the Home page together, before breaking off and working on individual pages.

This was helpful to me as it allowed me to learn from my other group members as well as offer some potential solutions to errors occurring. When I moved onto the recipe page I found that I was making some mistakes which I could correct by referring back to the home page we did together. I was also able to ask my colleagues for help due to being in a great team where I felt comfortable doing so. I found most of the errors I was having were syntax related. Once the functionality and the page were working as intended, I was able to follow the layout and styling from our wireframe to present a satisfying result.

Most of the content on the page was simple enough to pull off using `dot notation`, but getting the rating system to work and particularly setting up the CRUD functionality was pleasing to me.

![Screenshot 2023-02-27 at 23 23 04](https://user-images.githubusercontent.com/95321738/221711949-6928daae-e544-4a85-91c8-53a2fc8ee892.png)

The last full day was the 8th day when we were still finishing off some of the front-end, but we had scheduled to start styling on this day in our plan. We were able to split the style to the pages we worked on individually but at this point, I was able to help with some styling on some other pages, but mostly add more seeding that we were lacking. Fortunately, functionally our app was working as intended on the last day and we only had a little bit of styling to do. Although we never managed to complete all of our stretch goals within the timeframe of the project, we managed to incorporate all of our MVPs and some of these bonus stretch goals.


## Wins

* Although challenging to implement creating our own back-end through the MERN stack only taught the week before, working together helped elevate major issues
* Understanding and utilising documentation and its importance.
* The importance and thoroughness of our planning.
* Working with both Tony and Ryan was an invaluable experience and I learnt a lot from them. I appreciated their patience at times as well as being able to contribute significantly while learning from the two of them.


## Challenges

* I struggled to get to grips with some of the MERN stack initially but really enjoyed passing the early hurdles.
  * Understanding models, controllers, schema, etc. This took a bit of time to understand and fully grasp but it is something I am continually getting used to now.
* Incorporating everything within the timeframe.
  * This project really opened me up to how much detail can be done in the planning stage. Thanks to that, we managed to hit most of our intended MVPs but not all of our stretch goals. The extent and detail put into planning felt a bit excessive at first but it is something we greatly benefited from and I will continue to do in the future.


## Key Learnings

* During the 3 days of building our back-end, there were initial challenges of understanding some parts of the MERN stack that we overcame. 
* Having the chance to go over React from scratch again in the project benefited me, and I learnt a lot from doing so while in a group environment where my peers could offer support.
* How to work well in a team and generally feel comfortable throughout the projects no matter what issues occur.


## Future Features

* Incorporating a nutritional information breakdown, similar to MyFitnessPal
* Improving the functionality of the shopping list feature
* Resolving the following multiple users’ issue when trying to follow more than one user and all other users after the initial one show unfollow, despite not following them.
