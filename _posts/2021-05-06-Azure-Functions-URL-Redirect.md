---
title: "Using Azure Funtions To Redirect URLs"
layout: post
date: 2021-05-06 08:00
image: /assets/images/markdown.jpg
headerImage: false
tag:
- azure
category: blog
author: brandonbabcock
description: Using Azure Funtions to redirect URLs
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

Simply put, Azure Functions allow us to write code without worrying about the underlying hardware on which the code runs on.

---

## Implementation

<span class="implementation">To begin, deploy an Function App from the Azure portal using .Net core.</span>

![AzureFunction01](/assets/blogimages/azure_function_url_redirect_01.jpg)

Make sure to set the pricing tier to *Consumption*.

![AzureFunction02](/assets/blogimages/azure_function_url_redirect_02.jpg)

Once deploy, navigate to the Function App and select the *Proxies* blade.

---
## Results

<span class="results"></span>