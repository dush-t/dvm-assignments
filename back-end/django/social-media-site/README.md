# Winter Assignment

### Aim
1. The Django polls app tutorial is only a way to get introduced to Django. It's not enough if you want to be able say that you actually "know" Django. So here, we are going to give you an opportunity to really learn Django and show us what you can do. This project will help/make you build proficiency in Django by having to create a full out project: a social media/blog kind of application.

2. Learn/use some new and important Python libraries and APIs.

3. Learn about what is involved in actually launching a live project. You'll have to host this project online (i.e. publically accessable from anywhere in the world... anywhere with an internet connection that is). You'll pick up some basic Linux server administration/management skills from this project.

### Task
There are several "phases" or "legs" of this project:

#### Phase 0: Apply for a GitHub Student Pack
GitHub currently offers this great plan for students where you'll be able to get a ton of premium stuff for free. We'll let you find out what that stuff is. Apply for this pack ASAP, since it will take a day or two for your application/request to be processed. It won't be needed untill phase 3 though.

#### Phase 1: The Basics
Create a mini social media website using Django and some of the frontend skills that you have picked up.   

Apart from the following essential features, we're giving you the freedom of creativity in deciding what else you want to include.

**Essential features** - these are some things that we expect to see implemented and certain aspects of Django and Python that we want to see being used.
1. Implement user authentication. Django has a built in auth system and we expect you to use it (it's part of Django's *"batteries included"* appeal). It's a really handy session based auth system.
2. Create a well defined database structure and then implement it in the models.
3. Associate users with a profile. Let users modify their profile data.
4. Allow users to make their own posts and also comment on others' posts (no need to implement commenting on comments).
5. Allow users to follow each other (hint: you'll need to use many-to-many fields). When you follow other users, make it so that the relavent posts can easily be accessed somewhere (sort of like a news feed).
6. Make it possible to edit and delete posts. But think about this issue: what if someone posts something offensive and then edits or deletes it.... how would you prevent cyber-crime and cyber-bullying caused by this? (this is an example of where your creativity as a developer will be needed)

Make sure that you have a decent frontend for this. No need to make it too good, but just presentable enough... don't waste too much time on the frontend until after phase 3.


#### Phase 2: Some Cool Features
Now you will extend the basic project you created by adding some cool features which will require "some" additional learning on your part. Patience is key here.
1. Up until now, you've only been using an Sqlite3 database. Time to upgrade. Change your database backend to MySQL (since it's part of the DVM's tech stack).
2. Add a profile pictures feature. For this you'll need to learn how to store and reference/retrieve files and images in Django. You'll also probably need to learn how to do some image formatting using Pillow.
3. **Without** using the student pack that you got, make a seperate account on SendGrid. Then using SendGrid's API, extend the "following other people" feature so that you can choose to recieve mail based notificiations whenever that person makes a new post (so now there are two ways to follow a person.)
4. Extend the login system. Make it so that a person can also log in with Google. Use Google's API to provide OAUTH 2.0 based log-in.
5. Create a feature where staff and site admins can generate a report containing all of the basic profile data of each person registered on the site. The profile should be in the form of an excel sheet and we suggest using Openpyxl to get this done in python.


#### Phase 3: Time To Go Live!
You'll learn about more than programming here. Now you'll be introduced to the concept of tech stacks, Linux server administration and a bunch of other cool stuff.
Finally, you'll be hosting your project on the internet.
1. Read up on web servers and what they are. Hint: Don't get confused between the hardware and software parts. The word "server" can refer to either one - there is the physical machine which you will be "renting" and then there is the server software that you'll be running which actually manages all of the requests e.g. Nginx or Apache.
2. Using the GitHub student pack, sign up on [Digital Ocean](https://m.do.co/c/9667283a00b2) to be able to get your own VPS (Virtual Private Server). Note the hyperlink I provided you with is my referal link.
3. Create an Ubuntu 16.04 or 18.04 server and then host your Django application. You'll find this [tutorial](http://michal.karzynski.pl/blog/2013/06/09/django-nginx-gunicorn-virtualenv-supervisor/) **extremely** useful, and of course, google stuff to atleast roughly figure out what you're doing at each step of the tutorial. It will probably take some time and experience before you know what you're *exactly* doing at each step.

#### Phase 4: Celebrate the completion of your project with a treat from your seniors back on campus :D

### Time Alloted
  - Phase 1: 7 Days
  - Phase 2: 4 Days
  - Phase 3: 3 Days

### Submission Rules
***Securely*** share the source code on GitHub under your own account.  

What Securely means:
  1. Don't share the Django secret key.
  2. Don't share any test databases.
  3. Don't share any database passwords/names or anything of the kind.
  4. Don't share any API keys.
  5. **Do** use common sense.

Basically, don't share any data that must be kept secret.  
**Hint**: Make a python file where you store all of these values as variables (sort of like C/C++ macros in a header file), then add this file to your gitignore. Generally, we prefer to call that file the keyconfig.

Assignment compiled by [hypro999](https://github.com/hypro999)
