---
title: "Using Azure Functions To Redirect URLs"
layout: post
date: 2021-05-06 08:00
image: /assets/images/markdown.jpg
headerImage: false
tag:
- azure
category: blog
author: brandonbabcock
description: Using Azure Functions to redirect URLs
---
## Table Of Contents
- [Backgrond](#background)
- [Implementation](#implementation)
- [Results](#results)

---

## Background

<span class="background">Recently I was tasked with finding a cloud native solution that would allow incoming URL requests to be redirected to another URL destination. The cloud native solution had to be cost effective, require minimal configuration, and handle hundreds of request per day.</span>

Enter **Azure Functions**.

Azure Functions are defined by Microsoft as the following:

*"Azure Functions is a cloud service available on-demand that provides all the continually-updated infrastructure and resources needed to run your applications. You focus on the pieces of code that matter most to you, and Functions handles the rest"*

Simply put, Azure Functions allow us to write code without worrying about the underlying hardware on which the code runs on. However, we wont be writing any code, so dont worry! This will be a simple click setup configuration!

---

## Implementation

<span class="implementation">To begin, deploy an Function App from the Azure portal using .Net core.</span>

![AzureFunction01](../assets/images/az_function_redirect01.jpg)

Make sure to set the pricing tier to *Consumption*.

![AzureFunction02](../assets/images/az_function_redirect02.jpg)

Once deployed, navigate to the Function App and select the *Proxies* blade.

![AzureFunction03](../assets/images/az_function_redirect03.jpg)

Create a new proxy configuration with the following settings (make sure to update your backend url):

![AzureFunction04](../assets/images/az_function_redirect04.jpg)

Hit **Save**, and take note of the generated URL. You can use this URL to test the redirection of your backend url.

![AzureFunction05](../assets/images/az_function_redirect05.jpg)

Testing with URL producings the expected results.

![AzureFunction05](../assets/images/az_function_redirect07.jpg)

Function App Proxy URL is Redirected to:

![AzureFunction05](../assets/images/az_function_redirect08.jpg)

Now we must updated our DNS provider with a CNAME recording pointing to the Function App Proxy URL.

![AzureFunction05](../assets/images/az_function_redirect06.jpg)

---
## Results

<span class="results"></span>