---
layout: post
title:      "JS/Rails Project"
date:       2020-12-20 15:12:18 -0500
permalink:  js_rails_project
---


Hi Everyone! I just completed my fourth portfolio project as part of the Flatiron Software Engineering Program.

For this project, I decided to build a financial analysis API. With this API, I would be able to compare different stocks
on one screen and their related financial ratios.

### Backend
In order to achieve this, I first generated the backend. I decided on two models, Stock and Ratio. Ratio belongs to a Stock and Stock has many ratios. 

After establishing the relationship above, I created the database tables with rake db:migrate. At this point, I needed to determine how to seed my database with Stock and Ratio data. 

#### yaml gem
I finally decided to create a separate data folder and yaml file. This allowed the seed file to load the data using the yaml gem. The yaml gem provides the ability to load the yaml file as a dictionary into my ruby and seed files.

### Backend Testing
Now that I established my API's backend, I needed to test the previous relationships I created earlier. Using rails console sandbox (on the command line, rails c -s). Inside the rails console sandbox, I determined I could create instances of Stock and Ratio as well as their appropriate relationships. Time to move on to the frontend!!!

### Frontend
Getting to this point, I knew I still had a big mountain to climb. Event Listening and fetching were two areas where my comfortability decreased. 

There was a lot of information to digest in the Rails/JS Module so I had to slow down at this point. I watched some additional Youtube videos on event listening and especially fetching. Then I started playing around with some basic event listening and fetch code in my backend.

[Fetching](https://www.youtube.com/results?search_query=fetch+javascript)

After a couple days, I started to slowly understand how my frontend and backend were communicating with each other.

As it starting coming together for me, I was able to create functionality allowing users to create, update, and remove data from the database and DOM. 

Similar to the past projects I completed, this project really required me to dig and keep asking myself questions on each line and that line's significance. 


### Getting closer...
With the completion of this project, it's time to start the final Modules of the Flatiron Software Engineering Program!

