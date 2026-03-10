---
title: 'Devlog No.1: Creating a URL Shortener'
description: 'Planning out the project and creating diagrams'
pubDate: 'Mar 10 2026'
---
Whilst I was thinking of projects to do and found that yeah I can make a url shortener but not just any url shortener, one with the most weeb aesthetic ever as well a cool qr generator! Why? CUZ I CAN!

## Planning
I really don't know how shit like this works so i started with what even is a url shortener? Why do people even use those. I started with mostly just reading an article about it on [wikipedia](https://en.wikipedia.org/wiki/URL_shortening). The gist of it is, people used it mostly for a cost effective way of sending long url links on SMS as well as making links aesthetically pleasing. Although there are some drawbacks, first of all you're hiding the nature of the link, the obfuscated link made by the url shortener could be anything from ill phishing links to urls that would steal your data! So i kept that in mind that i would make my url shortener to have expiration.

## How Does It Shorten Urls?
Referencing wikipedia again, we basically assign the long ass url to a key and store it in the database. Said key would now be the params of the top level domain of our webapp. So sites with longs url's like www.foobar/this/is/so/long../etc would be www.myUrl/awJSkel, this raises the question on how we should encode the keys of our urls? For now a simple [base36](https://en.wikipedia.org/wiki/Senary#Base_36_as_senary_compression) would work fine since I don't think this site would pop off any time.

## Proceeding With The Diagrams
I wanted a way to visualize the "flow" of data and actions within the project so I proceeded with making a [Sequence Diagram](https://developer.ibm.com/articles/the-sequence-diagram/) and a [Activity Diagram](https://www.geeksforgeeks.org/system-design/unified-modeling-language-uml-activity-diagrams/). Though they were a basis on how I made my diagrams, i didn't really follow the OOP'ness of IBM's article. Nonetheless it really helped me visualize the plan I'm going for, shout out to [UMLet](https://www.umlet.com/) I used their tool to make these awesome diagrams.


![Awesome Sequence Diagram](../../assets/images/Sequence-Url-Shortener.png)

![Awesome Activity Diagram](../../assets/images/Activity-Url-Shortener.png)

## Closing Remarks
Yeah... up next I'm planning to design the UX/UI of this project and after that we'll talk about deploying this project and the database.
