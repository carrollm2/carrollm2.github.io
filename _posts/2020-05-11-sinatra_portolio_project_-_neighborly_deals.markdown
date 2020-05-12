---
layout: post
title:      "Sinatra Portolio Project - Neighborly Deals"
date:       2020-05-12 02:57:10 +0000
permalink:  sinatra_portolio_project_-_neighborly_deals
---


**Overview**

Hi Everyone! I'm back to talk to you about my second portfolio project as part of Flatiron's Software Engineering Self Paced Online Program.

The first app I built was based on sports so I wanted to try and think of something a little different this time. And I started thinking about philanthropy and an app that can be useful during these hard times caused by the pandemic.

Even before the pandemic, my wife would usually go on a website where community citizens can post about items they are giving away. She loved the site but became frustrated when an item was taken but still posted as available.

I thought to myself that this could be a perfect situation to build a web app which uses a relational database so users can post items they are willing to give away and then also read other user posts,  update their own post and delete their post once they successfully found another user interested in the item.


**App Models and Relationships**

To successfully build this app so users can not only perform the basic CRUD functions but also be able to run customized queries in the future, I needed to establish class models with relationships to other class models.

The first models I built were the User and Post models.

The User could have many posts and each Post would belong to a User.

And each Post would have a category for the item posted (toy, fitness, music, etc) and also a Post Type (user request or user give away).

Therefore, I added models for Category and Post Type because Category can have many Posts as could Post Type. And each Post would belong to a Category and to a Post Type.

**Security

In order for a user to see the posts of others and to create a post themselves, they need to sign up for the app. Any account which has the same username or email account of another user will be returned to the sign up page. Once successfully signed up, their password is encrypted and stored in the database.

**App Controllers and Views**

For users to see their posts, the app has a PostController with 4 different views (index, new, show, and edit). After successfully signing-in, the user is presented with a table of the posts from other users outstanding and a Create Post link. After selecting the Create Post link, the user is then presented with a menu of options to describe their item.

After submitting their post, the post will be added to all the posts in the database. If the user elects to edit/update the post, they can do so but will not be able to edit or delete the posts of other users.

[Check it out!](https://github.com/carrollm2/neighborly-deals) And see all the great neighborly deals in your community.




