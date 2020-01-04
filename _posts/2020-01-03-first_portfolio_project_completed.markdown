---
layout: post
title:      "First Portfolio Project Completed!"
date:       2020-01-03 22:52:00 -0500
permalink:  first_portfolio_project_completed
---


Hi again everyone! As some of you already know, I enrolled in the Flatiron School Online Software Engineering Program (Self Paced) back in October. These past couple weeks I have been working on my first Portfolio Project!

For this project, I was required to develop a command line interface application from scratch. After completing all the previous lab work, I felt mostly confident in my knowledge of object oriented programming but I also knew the project
would be very challenging. 

First, I needed to find a website to scrape. 

Second, I needed to have a plan before writing the code.  What classes would I need? What would the architecture of the application look like?  How would I like the application to interact with the user?

And finally, write and test the code.

I thought a lot of topics/subjects that interest me (finance, sports, cars, etc.). I finally came across a hockey equipment website, www,.icewarehouse.com. The layout of website caught my eye because I noticed it showed clearance and top seller items separately.

When I saw this, I started to brainstorm how to apply what I learned in my previous Ruby readings/labs with the hockey equipment website. My goal would be to create an application to help a user find hockey equipment deals by classification (top seller and clearance) and also some extra selection criteria such as top seller and clearance items less than $75.

I knew then my application architecture would include a Clearance class and TopSeller class which would both inherit from a HockeyEquipmentDeal class.

In order to build objects of the class type above, I would have to scrape the website for the required information so I needed to create a Scraper class. The scraper class  would consist of two class methods,  scrape_top_seller and scrape_clearance.

After building and testing the above in repl.it, I created a repository skeleton for my project. I used the Flatiron School walk through video to guide me through the initial steps before I started adding files for the above.

Then I stopped. I should have planned earlier but I was so focused on finding a website to scrape that I overlooked the second part. How would my application interact with user? I knew I wanted to present a menu to user but didn't give too much thought about the details.

Due to my poor planning, I basically wrote all the user interaction in the application's executable file. And it took me much longer than expected as I was finding bugs in my code as I went. After debugging, I was left with an application that worked but was a big mess to read. My functions were way too long, function names were misleading, and the list goes on and on. 

Additionally, the architecture of the program didn't feel right to me. At this point I knew, I needed to make a Menu class which would hopefully shrink my executable file. I also transported code my from my application's executable to the CommandLineInterface class. 

Here I stopped once more. I felt confident in the current architecture of my application but the code inside my application's files needed to be cleaned. I picked up a book, *Clean Code* by Robert C. Martin. Here, I was able to get some ideas on the flaws currently present in my code.

With this book's lessons in mind, I reduced the size of my functions in the CommandLineInterface class, reduced the number of arguments passed in the methods, and made function/variable names more descriptive.

The result was more readable code but my command_line_interface file was way too long (200+ lines). 

Here was one of my biggest challenges. I was staring at code that worked and readable but even I got overwhelmed when looking at how long the file was. How was I going to refactor this to be even more efficient?

It took me some time, but I learned something by this point. Before make any changes, I grabbed a notebook and drew my application's class architecture. And I counted close to 20 methods in my CommandLineInterface class.

I scribbled some potential method destinations to each class. Took a step back. Said "no". Did some more scribbling. Still didn't like what I saw on my notepad. Took a break and then it hit me. I had some "get" methods that really belonged as class methods in my TopSeller and Clearance Class. There were 4 of these. By adding one argument, I could reduce it to one additional method for each class. That's 4 methods no longer in my CommandLineInterface class. There were for 4 more "run_menu" methods that I could reduce down to 2 with addition of one argument. And there were 4 "display" methods that I could reduce down to 2 with addition of one argument. In total, I was able to remove 8 methods from the CommandLineInterface class.

The result was still working, readable code which was relatively DRY and condensed file length sizes.

Lastly, I did some file renaming and moving  to hopefully make the files content more straightforward without having to open the files.

This was an enjoyable, rewarding project. Although daunting at first, I loved having to brainstorm an idea and then making it happen with the skills I previously learned in the curriculum. I gained confidence not only writing code but also in using developer workflows such as Github. Looking forward to what's ahead! 

[https://github.com/carrollm2/hockey_equipment_deals](http://)
