---
layout: post
title:      "Hashes - Organize Your Life and Your Code"
date:       2019-11-08 22:38:44 -0500
permalink:  hashes_-_organize_your_life_and_your_code
---


I would love to say I'm very well organized, but I know I'm not. For example, I spend way too much time every morning searching for clothes to  wear each day. I'm always guessing where I can find the exact shirt I'm looking for. Is it in the closet on a hanger, is it in the dresser and which drawer of the dresser? Or is in the laundry already?

If I simply took the time and categorized my clothes by maybe type and style (short sleeve vs long sleeve, shirt or pants, etc), I wouldn't waste nearly as much time every morning. I would simply know what location to start the search and the find that item in the location I'm looking. 

A lot of times in our code, we can find ourselves with working with a lot of variables. If we took the time to take a step back we would we realize a lot of the variables and values have a relationship with each other. By categorizing/grouping our variables with relationships, our code could easily look up the variable value we are looking for.

Hashes are key to an organized life and to organized code!

```
def organize_clothes(item_to_search_for)

  dresser = {"dresser_first_drawer" => ["green_short_sleeve_shirt", "red_short_sleeve_shirt", "striped_short_sleeve_shirt"], "dresser_second_drawer" => ["blue_long_sleeve_shirt", "black_long_sleeve_shirt", "plaid_long_sleeve_shirt"]}

  closet = {"closet_hangers" => ["tan khakis"], "closet_drawer" => []}

  clothing = { "tshirt" => "dresser_first_drawer", "pants" => "closet_hangers", "polo_shirt" => "closet_drawer"}

  clothing.each do |clothing_type, location|
    if clothing_type == item_to_search_for[0]
      if location.include?("dresser")
        if dresser[location].include?(item_to_search_for[1])
          puts "Found my #{item_to_search_for[1].gsub("_"," ")} in the #{location.gsub("_"," ")}."
        else
          puts "My #{item_to_search_for[1]} must be in the laundry."
        end
      end

      if location.include?("closet")
        if closet[location].include?(item_to_search_for[1])
          puts "Found my #{item_to_search_for[1].gsub("_"," ")} on the #{location.gsub("_"," ")}."
        else
          puts "My #{item_to_search_for[1].gsub("_"," ")} must be in the laundry."
        end      
      end      
    end
  end
end

first_item_to_search_for = ["tshirt", "red_short_sleeve_shirt"]
second_item_to_seach_for = ["pants", "tan khakis"]
third_item_to_seach_for = ["polo_shirt", "navy_blue_polo_shirt"]

organize_clothes(first_item_to_search_for)
organize_clothes(second_item_to_seach_for)
organize_clothes(third_item_to_seach_for)
```
