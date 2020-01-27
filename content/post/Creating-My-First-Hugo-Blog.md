+++
title = "Setting Up My First Hugo Blog"
description = "Steps I took to create this Hugo blog"
date = 2020-01-27
author = "Jonathan Greene"

+++

## Introduction

Welcome my name is Jonathan Greene I am Full Stack Developer that focuses on building clean easily scalable code to get a better ROI on for my clients. In this first blog we are going to talk about what it takes to be able to setup your own Hugo blog and how I did mine. I will Link to the resources I used at the bottom as well and reference them throughout the article where needed.  Without further ado let us begin. 

```

```


## Step 1. Setting up Hugo Initially 

There is not much to be said here except I followed the instructions from Mike Dane located here.  https://www.youtube.com/watch?v=G7umPCU-8xc

My only recommendation is that you take it slowly and go step by step in the end you will be pretty happy with the results. 



### Step 2.  Creating your new site blog

Following this page https://flaviocopes.com/start-blog-with-hugo/ you would start by creating your new Hugo site remember to do this in your home directory to make it easier on yourself later. 

### Step 3. Adding in a theme for Hugo to use

I followed the above article and used the ghostwriter theme. Also took the blog writers recommendation and did not use the git clone workflow and instead downloaded and put it inside  themes/ghostwriter.

### Step 4. Site Configuration File 

Again Following the above article make sure to post in the config file onto the root of your website folder it should resemble this picture. 

![image-20200127113742704](C:\Users\JonathanSchool\AppData\Roaming\Typora\typora-user-images\image-20200127113742704.png)

### Step 5. Getting the website to load

If your like me you are going to get some errors following the instructions in the above referenced blog.  What I had to do was as follows

1. Ensure yarn is installed and verify this by using cmd or similar to type "yarn  -version"

2. Make sure to cd into the themes folder and into the actual theme you chose. then type yarn and wait for all files to load. 

3. Make sure to change the name in the config file to match that of the theme you chose for example my theme was ghostwriter-master so instead of the default ghostwriter I had to change it to be ghostwriter-master on line 3 of the image below .

   ![image-20200127114023510](C:\Users\JonathanSchool\AppData\Roaming\Typora\typora-user-images\image-20200127114023510.png)

4. Last run hugo serve inside your base directory.  View application on http://localhost:1313/

#### Step 6. Setting up your Github Repo

I went ahead and loaded up my github and on the left side there is a button that says Repositories New I clicked on that. Entered the name Description and Did not initialize the repo with a readme.  After that I used cmd or ect to go the base directory of my site and input the following commands

```
git init
git add .
git commit -m "Initialized my first Hugo Blog"
git remote add origin https://github.com/YourNameHere/YourRepoName.git
git push -u origin master
```

#### Deploying to Netlify

The reason I chose netlify is because it is great for static hosting and Hugo allows your blog to be a static site that you just modify and add blogs to via the file structure instead of a live Full Stack Application. That would include a database, front-end, and back-end. Following this article https://flaviocopes.com/start-blog-with-hugo/

go to the part that is labeled  **Deploy the Hugo site to Netlify**

### Finding a markdown Editor

Going through and trying to create and edit your first blog is going to drive you crazy without a markdown editor. To solve this problem I chose to use Typora due to its clean and easy to use interface as well as not actually having to write in markdown. I would recommend this because its free and is so easy to use and has all the features I would ever need. However if you find it lacking for your specific uses feel free to try another one and let me know about it by sending me a message at jonathan-greene.com

#### Thank you for reading my first blog post

I hope this blog helps you to setup your own blog and start sharing your ideas and opinions and growth with yourself and the world.  Have a great day!



https://www.youtube.com/watch?v=G7umPCU-8xc

https://flaviocopes.com/start-blog-with-hugo/