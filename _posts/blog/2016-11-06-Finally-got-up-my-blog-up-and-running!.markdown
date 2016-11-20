---
layout: post
title:  "Finally got up my blog up and running!"
date:   2016-11-06 02:38:00
categories: blog
---
It feels great that I'm able to get my blog up and running, especially creating this first blog post! After researching for hours, I finally realized how simple it is to set up a blog.
It's very simple so if you want to set up a blog and make your first blog post, let me teach you! It will be very quick!

First, you need to find a free jekyll blog theme that you like and want to base your blog off of that. There are a lot of jekyll themes out there, Just google "free jekyll blog theme" 
and you'll find tons of links. To help you find a jekyll theme, I put a link <a href="http://jekyllthemes.org/"> right here </a> for you to click on so you don't have to search every
single link result you found on google.


Next you need to make a Cloud9 account and create a workspace for just your blog. Once you're done with that you, in your terminal you need to install jekyll like this
`gem install jekyll`


Then you should upload the theme zip file you have downloaded for your blog to your cloud9 workspace. Go to "File"-->"Upload Local Files.."-->"Select folder", and that's where you search 
where the downloaded them zip file is in your laptop/computer.

You can either unzip it before you upload or once it is in your cloud9 workspace, unzip the file by entering in your terminal "unzip (yourzipfilename)". After doing that, you need to 
change into your directory of the unzipped file you uploaded like this:
'cd (nameofyourblogunzipfilefolder)'

You should type in this command once you're in the directory of the unzipped file:
`jekyll build`

Have you heard of markdown files? Well it's pretty simple to explain because this will make your life a lot easier instead of coding it in html. You can just write down in plain text like 
in a text file but once you put the code above into the terminal, it'll convert all of your markdown files to HTML files. You just have to create a new file in cloud9 of where your posts
folder is located in your unzipped theme file and the file name should start with the date in this format: "2016-11-05-Name-Of-Blog-Post.markdown". Within the file, it should
start with a few lines of a header then after doing that, it's basically just markdown:

```
---
layout: post

title:  "Name of Blog Post"

date:   2016-11-06 02:38:00

categories: blog

---
```

Since you have this part set up, you now need to link your workspace to a Github repository. First you need to login to your Github account (if you don't have one, then you need to create one,
it's free and simple to make one), next you need create a repository: the name of your repository should be (yourGitHubusername).github.io. Just to show you for example, the link of my blog here
is "immy1996.github.io".

Now you have to go back to your cloud9 blog workspace and link your workspace to your Github blog repository you just created. To do that, in your terminal change into your unzip blog folder
and follow along these codes to do it:

`git init`

`git remote add (linkofyourrepository)`

`git add -f *`

`git commit -m "messageyouwanttoputinhere"`

`git push -u origin master`

<!--<img src="sleek_blog-master/assets/img/CreatingaNewBlogPost.jpg" alt="Making a new blog post 7">-->

So what  `git init` does is that it'll initialize an empty git repository in your folder and in this case, it'll be your unzip blog folder. What `git remote add (linkofyourrepository)` does is that 
it'll put the empty git repository recognized as the git repository of the one you're connecting from GitHub. You can check what files you have changed to remember in case you forgot as `git status`,
it'll give you a list of what files and where it's located to add files towards your respository. Then do `git commit -m "messageyouwanttoputinhere"`, which will commit the files and the message you 
put in `"messageyouwanttoputinhere"` will be displayed on the commit page of Github. Finally, `git push -u origin master` is to push the file(s) to your repository on GitHub. That's all you had to do
to set up a blog AND making your first blog post. 

To check if your blog site has been published, just go to your repository, then click "Settings", go to the "GitHub Pages" section and you'll should see your blog has been published.