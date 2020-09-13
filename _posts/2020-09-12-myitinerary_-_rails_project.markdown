---
layout: post
title:      "MyItinerary - Rails Project"
date:       2020-09-12 17:41:10 -0400
permalink:  myitinerary_-_rails_project
---


Hey Everyone! I'm back again after finishing my THIRD portfolio project as part of the Flatiron's Online Software Engineering Program! And whoa, was it a challenge!

**Overview**

To get this project off the ground I had to first think of an idea. I really struggled with this and had a difficult time settling on one. About a week into the project process, I joined a Study Group hosted by Flatiron School. This was really therapeutic for me because I realized other students were also struggling just like me. Not only that, other students gave tips on how they arrived on their web app ideas. I will definitely refer back to this for my next portfolio project because I feel like I'm fresh out of new ideas!

**Decision and Purpose**

In the end, I decided to build an itinerary builder in Rails and called it MyItininerary. I think there are many websites covering upcoming events in America's bigger cities, but how about smaller cities/towns? I thought it could be a great idea to aggregate as many small town/city events in one web application. Hopefully this will reduce time spent visiting individual small town sites.

**Models and Associations**

My Itinerary has 4 models and the following associations:

* User -- Has many Itineraries, Has many Events through Itineraries, Has many Destinations through Itineraries

* Itinerary (Join Model) -- Belongs to User, Belongs to Destination, Belongs to Event

* Destination -- Has many Itineraries, Has many Users through Itineraries, Has many Events

* Event -- Has many Itineraries, Has many Users through Itineraries, Belongs to Destination

**User Security**

User model includes the  has_secure_password field so a user's password is encrypted upon joining and authenticated when logging in to MyItinerary.

**Validations**

The most important validations I added to the models in my opinion are the following:

* Unique email and username
* Password Confirmation matches Password upon User SignUp
* Users cannot create an identical Itinerary so all User's Itineraries are unique
* Users cannot create an Itinerary that considered a time conflict with another Itinerary for the user

**Scope Methods** 

In the Event model, I added the following scope methods to help improve MyItinerary's functionality:

Upcoming Scope Method -- This allows only upcoming itineraries with upcoming events and filters out past itineraries

Sorted by Event Date Scope Method -- In addition to showing only upcoming itineraries/events, the events are sorted in chronological order from most recent to latest

**Other Functionality**

Created a selected_city route which allows users to display only their upcoming itineraries by city selected in the index view

**Views**

* Users
* Itineraries
* Destinations
* Events
* Sessions

With 5 Views, refactored some repetitive code into partial views.

For example, my Itinerary controller's routes for show, index and selected city displayed instances of a user's itinerary details. I created an _itinerary.html.erb inside my itineraries views where the repetitive code is relocated and also a locals variable so the instance of itinerary variable in each view can be supported inside _itinerary.html.erb

**Controllers**

* Users
* Itineraries
* Destinations
* Events
* Sessions

I added before actions in application's controllers to help reduce repetitive code used in controller routes.

For example, before actions are applied in the application's Itineraries controller to determine if a user is logged in, if the user is an admin, and if the user authorized to view selected itinerary

MyItinerary also allows users to sign in or login in with Google. For this, I created a sessions controller which finds or creates a user when a user signs in with Google or finds an existing user if the user elects to log in through MyItinerary.

Once a user is signed in, the session hash is populated with the user's id, which allows the application to determine if a user has authorization to view and persist data to the database.

**Routes**

I decided to use nested routes for User and the Itineraries index route so a user can only see all of their own itineraries. 

I also decided to use nested routes for Destination and Events, so an admin can create, update, and delete events for a particular destination.

**Challenges**

I would have to say my biggest challenge for this project was actually developing an idea which satisfied the project's requirements. I used draw.io to help determine my application's models and associations but I spent a good week doing this before I found a setup that I was happy with.

Once I arrived at my idea, the next challenge was finding the time required to complete the project. I spent a lot of time researching and with more research comes more ideas. More ideas to include and more ideas to improve.

In the end, I learned a ton through researching different project requirements. 

**Resources Used**

* Jennifer Hansen's, Rails MyBlog Project Build (5 parts) -- Youtube 
* Google sign in -- https://medium.com/@amoschoo/google-oauth-for-ruby-on-rails-129ce7196f35
* https://guides.rubyonrails.org/


**Things I would do differently**

Definitely join more Flatiron Study Sessions even if you don't have a particular question. It's good to hear what others are experiencing and the questions they have. Often, you will struggle in the same areas and it's good to hear other student's ideas and challenges.
