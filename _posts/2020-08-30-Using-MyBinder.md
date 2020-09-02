---
toc: true
layout: post
description: Using my binder.
categories: [markdown]
title: Using binder to deploy your code in Jupyter as an app
---
# Using mybinder.org

This will show you two ways to deploy your model as an app. This follows the FastAI lesson 2 example. I faced a few problems when deploying my notebook with iPywidgets into binder. This had less to do with iPywidgets and more with the set of accompanying files that you need to have in your repo.

## Assumption

1. You know how to create a git repo and use from the command line on your computer. [Here](https://product.hubspot.com/blog/git-and-github-tutorial-for-beginners) is a neat tutorial on how to get started.
2. I am using [Paperspace](https://console.paperspace.com/notebooks) for this example because it just works with FastAI lessons and notebooks.
3. You have created a separate notebook to test the image recognition code following the code provided here [Bear_voila](https://github.com/fastai/bear_voila).

## Basic setup

1. You should have created a notebook fashioned after the FastAI lesson [notebook](https://github.com/fastai/course-v4/blob/master/nbs/02_production.ipynb).
2. This particular line `learn.export()` in the notebook will export your model as a `.pkl` file. The name of the file is `export.pkl`. This will be in the same directory where you created the notebook. 

![]({{ site.baseurl }}/images/blog-images/export.png "export.pkl")

3. Download the export.pkl file into your newly created gihub repo.
4. Add another file called `requirements.txt` from [here](https://github.com/fastai/bear_voila) to your repo
5. In the end your repo should look like this

![]({{ site.baseurl }}/images/blog-images/export.png "export.pkl")

6. Commit and push your code.

### Setting up binder

1. Goto my [Binder](https://mybinder.org/)
2. Here is a screenshot of my Binder cofig.

![]({{ site.baseurl }}/images/blog-images/binder.png "Binder setup")