Conference application for the Udacity building scalable apps course.

Uses app engine to run a conference application for users to browse
and register for conferences. 

API endpoints added to add Sessions and offer query functions. 


-------------------------------------------------------------------

List Of Files

Be sure that you have saved in your directory the following files:

static/	
templates/	
README.txt	
app.yaml	
conference.py	
cron.yaml	
index.yaml	
main.py	
models.py	
settings.py
utils.py	

-------------------------------------------------------------------

Instructions For Usage:

The code has been deployed to App Engine and you can see it in
action at:

studied-market-105601.appspot.com

You can also create your own googe project with a new app id to then
place in the app.yaml file. Then you can deploy to App Engine for
testing and using the site.


-------------------------------------------------------------------

As part of the assignment I created extra queries, particularly
to get non-workshop sessions after 7pm. This was a little tricky
for two reaons. For one, the datetime objects of NDB do not 
behave like the datetime objects in python, so there's some
adjustments that have to be made there. Second, we cannot directly
group inequalities into one query for Google's datastore. This is
a limitation that comes with the faster queries. To get around
this limitation the queries are run separately and then the code
iterates through each to identify overlaps to then save to the
list of sessions to return.

-------------------------------------------------------------------

Some of the code from this course was based on lessons taught in
the Udacity Full Stack Foundations course and the Authentication
and Authorization course. The code was modified to meet the 
requirements set by the Udacity project 4 rubric.



