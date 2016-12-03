---
layout: post
title:  "Google Cloud: Compute Engine"
date:   2016-12-2 8:38:00
categories: blog
---

I attended a Google Cloud Platform Workshop about a month ago. I learned so much about the Google Cloud Platform.
The speaker and host gave great lessons and labs for us to do. By practicing those labs, it helped me a lot to 
understand better more about the storage types and others. The topic that interested me the most was about the Compute Engine. 

From what I understood from the workshop Compute Engine is basically one of several Google Cloud Platform compute options for
running your applications. Google Compute Engine lets you create and run virtual machines on Google infrastructure. Compute 
Engine offers scale, performance, and value that allows you to easily launch large compute clusters on Google's infrastructure.

What an instance is that it is a virtual machine (VM) hosted on the Google's infrastructure. Simply, you can create an instance 
by using the Google Cloud Platform Console or the gcloud command-line tool. A Compute Engine instances can run Linux and Windows 
Server images provided by Google, or any customized versions of these images. 

You can also build and run images of other operating systems. You can choose the machine properties of your instances, such as the
number of virtual CPUs and the amount of memory, by using a set of predefined machine types or by creating your own custom machine types.
I'll show you an example of creating an instance by using the Google cloud Platform Console.

First go to <a href="console.cloud.google.com">console.cloud.google.com</a>. If you don't have an account, you can right now get a free
trial with a $300 free of credit for 30 days to use at this link: <a href="https://cloud.google.com/free-trial/">https://cloud.google.com/free-trial/
</a>. After getting your account set up and such, you should be able to see this screen when you go to your Google Cloud Platform Console:

<img src="/assets/img/GoogleCloudConsoleHomePage.jpg" alt="Google Cloud Console Home Page Example" height="500" weight="500">

Now click on the top left of your page and go to where it says "Compute Engine" and click on it like this:
<img src="/assets/img/GoogleCloudConsoleHomePageComputeEngine.jpg" alt="Google Cloud Console Home Page Compute Engine Example" height="500" weight="500">

After clicking that, you should come up at this page:
<img src="/assets/img/GoogleCloudConsoleComputeEnginePage.jpg" alt="Google Cloud Console Compute Engine Page Example" height="500" weight="500">

Now we want to create to an instance, so click on "Create Instance". You should be at this page as of now:
<img src="/assets/img/GoogleCloudConsoleComputeEnginePageCreatingInstance.jpg" alt="Google Cloud Console Compute Engine Page Creating Instance Example" height="500" weight="500">

