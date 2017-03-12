# AdvertisingSystem
COMP4601 A3 - The main objective is to have the student analyze a body of documents and, given user access patterns, create a simple contextual advertising system.

## Creators
Elisa Kazan
Jack McCracken

## How to Test
1. Step 1
2. Step 2
3. etc

## Anlysis.pdf
The Analysis file can be found [here](https://docs.google.com/document/d/1qsCNq41wNMW4uConN1n6-jbX51ssa-AtyrIMome0KYA/edit?usp=sharing).

## To Do:
Web service name = COMP4601-RS
Root path = /rs
	
START URL (over 1000 web pages)
http://sikaman.dyndns.org:8888/courses/4601/assignments/training/pages/
	
Over 1000 users
Root directory for users: 
http://sikaman.dyndns.org:8888/courses/4601/assignments/training/users/
Here is the list of all the pages and the users that view the pages
	
Graph Directory
http://sikaman.dyndns.org:8888/courses/4601/assignments/training/graph/
	
Archives
http://sikaman.dyndns.org:8888/courses/4601/assignments/archive/
	
Given the user profiles, you are to create 3 or more categories of user. 
This is the value of m referenced in (9) and (12).
	
You are to design a contextual advertising system. 
When a user requests a page, the page will be retrieved and augmented with advertising. 
Review lecture 13 notes on Content Augmentation
	
1. Design a model for user preferences based upon the content of the web pages.
2. Determine communities for users.
3. Create advertising content that reflects the interests of the users in that community.
4. Design and implement a mechanism for associating appropriate advertising given a user and a page request.

/reset/{dir} using GET
This initializes the system, for testing only.

/context using GET
Analyzes the webpages and return profiles for users. HTML table with one row for the info of the user.

/community using GET
Runs after /context, returns the html representation of the communiies for the user
Returns a table where each row is a community name, followed by a cell containing a comma delimited list of user names
If this runs before context, must show an error

/fetch/{user}/{page} using GET
Retreives a page from context (he will give us a testing set after the deadline) and augments it with advertising. Must have 2 frames, , content and advertising.

Document the communities you have found in analuzing the test data in the web pages and users provided. Also document how we created the advertising content and the mechanism used to retrieve it using the /fetch/{user}/{page}

/advertising/{category} using GET
Returns the html representation of the advertising category (ex: C-X, X=1, ... m). There should be more than one advertisment for each community.

Design and document an algorithm called SUGGGEST (but do not implement it) that, for a given user, u, and a social graph G=<V,E>, where u is represented as a vertex along with the existing users, will suggest a set of pages that the new user might want to access. Also, indicate how the advertising system would work in this revised system. For your interest, a social graph that connects the users provided in the users directory may be found in the graph directory. This directory contains one web page per user. Each web page stores the links to other users representing a social relationship.



