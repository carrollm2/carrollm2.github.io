---
layout: post
title:      "Rails/React Project"
date:       2021-03-16 21:59:12 -0400
permalink:  rails_react_project
---


Hi Everyone! I'm back with my final project!

### Purpose of Application

I currently work in Structured Finance. Unlike a lot subjects and topics, not a lot of great content exists to help aspiring professionals in this particular industry.

With that in mind, I decided to build an application which will provide users a location where they can go to learn more.

### Long-Term Goals

My long term goal is to provide an application which will have the following:

* User sign-up 
* Deals/Rating Reports
* Recommended Books
* Recent News and Articles
* Job Posts
* Message Board
* Events

### Backend

For now, I started building my application with 2 Rails models:
* Deal
* Report

Association: Deal has may Reports and Report belongs to Deal

The reason for this is because reading recent Rating Reports is one of the best ways to get insight into the industry.
These reports are great summaries of important components pertaining to specific Deals such as Mortgage Characteristics, Risk Factors, and Strengths of Deal Structure. They also provide a glance at the larger picture outside the specific Deal and into the Mortgage Industry itself.

Along with the models above, I created controllers for each with controller actions for getting, creating, and deleting deals and reports. 

### Frontend

When the user opens the application, they will be presented with a Navigation Bar along with the Hero section and  a Footer. From here the user can learn more about the application and select different links. 

If the user selects the Deals Reports link on the Navigation Bar, they will redirected to the Deals page. Here my application is making a fetch GET request to my application's backend and rendering the data from the Deal controller index action. The result gives users a card item rendered on the page for each deal which is a link to the spefic deal itself. Also on this page, users will be allowed to add/create a new deal by selecting a link.  

If the user elects to select a Deal card item, they will  be redirected to a page which show all the Reports available for the deal. And the user can select the Report link to open for reading in a separate tab.

If the user elects to select the Add a New Deal link, they will be redirected to a form. Once the form is populated correctly, the application will make a fetch POST request to the backend which will call the Deal controller create action.

With the Deal/Report functionality now working, I will next build a page where all the Recommend Reading (Books) will be displayed. 

### Looking forward...

Building this application should really strengthen my skills as I continue add to the backend and provide a responsive frontend for all the user content I aim to provide.

Stayed tuned for any posts with updates and progress I make!




