# WebCrawlerAssignmet
---------------------


There are a lot of useful information on the Internet. How can we automatically get those information? - Yes, Web Crawler.

In this assignment, I have done how to make a prototype of Web crawler step by step by using Java. 
Things that are neccessary:-

Basic Java programming
A little bit about SQL and MySQL Database.

1. The goal


Given a organization root URL, e.g., "wiprodigital.com", return all pages that contains a string "All" from this organization

A typical crawler works in the following steps:

Parse the root web page ("wiprodigital.com"), and get all links from this page. To access each URL and parse HTML page, I will use JSoup which is a convenient and simple Java library.
Using the URLs that retrieved from step 1, and parse those URLs
When doing the above steps, we need to track which page has been processed before, so that each web page only get processed once. This is the reason why we need a database.
2. Set up MySQL database


I am using Windows, we can simply use WampServer. You can simple download it from wampserver.com and install it in a minute and good to go for next step.

I will use phpMyAdmin to manipulate MySQL database. It is simply a GUI interface for using MySQL. It is totally fine if we use any other tools or use no GUI tools.

3. Create a database and a table

Create a database named "Abhishek" and create a table called "Record" like the following:

CREATE TABLE IF NOT EXISTS `Record` (
  `RecordID` INT(11) NOT NULL AUTO_INCREMENT,
  `URL` text NOT NULL,
  PRIMARY KEY (`RecordID`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 AUTO_INCREMENT=1 ;

