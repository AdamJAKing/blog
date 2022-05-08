---
title: "How I Built This Site"
categories:
  - Blog
  - Tutorial
tags:
  - Github
  - Jekyll
  - Website
  - Hosting
  - DNS
---

In this post we will take a deep dive into the tools, resources and steps that allowed 
me to get this site online in only a couple of hours. Though this guide is somewhat long I have tried to condense
it down as much as possible so that you can get a site online quickly. 

### Who Is This Guide Suitable For?

This guide is suitable for people with basic git and programming knowledge 
and who want to get a site online quickly without reinventing the wheel.

### Cost

Everything in this guide is free except for the custom domain name setup, which is an optional step.

## Resources

Below I have listed each resource and what you need it for. Don't worry about rushing off 
and setting up each one of these now, we will do this at each step

* [Github Pages](https://pages.github.com){:target="_blank"} - For hosting. You **will** need a Github account for this
* [Jekyll](https://jekyllrb.com){:target="_blank"} - Static site generator
* [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes){:target="_blank"} - A popular Jekyll theme. We will be setting this up as Github Repository via the [Minimal Mistakes Remote Theme Starter](https://github.com/mmistakes/mm-github-pages-starter/generate)
* A Domain name (Optional) - You can use whatever provider you want for this

It's important at this point to mention that Github Pages supports 3 different types of sites. These are organisation,
user and project. For our setup we will be using the project type. For more information on the different types you
can read [this](https://docs.github.com/en/enterprise-cloud@latest/pages/getting-started-with-github-pages/about-github-pages#types-of-github-pages-sites){:target="_blank"} section on the Github 

# Lets begin!

I'm running WSL2 with Ubuntu but whatever OS you have should work perfectly fine. The steps below will be 
based on Linux, so you will need to make sure to follow your specific OS setup guide at each step (if appropriate).

## Jekyll

The first thing we are going to need is to download Jekyll. Jekyll is a static site generator
that is built on Ruby. It's fairly minimal and has great support for Github Pages. 
There is a great [installation](https://jekyllrb.com/docs/installation/){:target="_blank"} page on the website, and it should only take
you a few minutes. Once completed you should be able to run the below command

`bundle exec jekyll --version`

If this command outputs the version information then you're ready for the next step!

## Minimal Mistakes

You must be logged into Github before going to the Minimal Mistakes Remote Theme Starter link below. If you aren't
logged in then you will be redirected to the Github page instead
{: .notice--warning}

There are multiple ways to build a Jekyll site but for this guide we will be using the 
[Minimal Mistakes Remote Theme Starter](https://github.com/mmistakes/mm-github-pages-starter/generate){:target="_blank"}. This method is
a really great way of getting up and running quickly with a Jekyll site as it will create a new repository on your
Github account with all the necessary files. 

Once you open the link you just follow the below

* Set a repository name, you can call this whatever you like.
* Set the repository visibility settings. I personally use public because I don't mind the website source code being open to the public.
* You can ignore all the other settings such as the description and including all branches.

Github Pages websites are accessible from the web by default. You should not store sensitive information
in your source code, and you should consult the official documentation if you're concerned about keeping your
information secure
{: .notice--danger}

Now generate the repository by clicking on `create repository from template`. This will take a few seconds but once
it is completed you will have a brand-new repository in your account that looks like the below

![repository.png](/assets/images/how-I-built-this-site/repository.png)

Once you have the repository created on Github, create a new branch from master called `gh-pages`. 
It is common on Github Pages repositories to have a `gh-pages` branch and to tell Github to deploy from 
here. There are other publishing methods available, but we won't be those discussing here. For more
information you can check out this page from the official [documentation](https://docs.github.com/en/enterprise-cloud@latest/pages/getting-started-with-github-pages/about-github-pages#publishing-sources-for-github-pages-sites){:target="_blank"}

## Github Pages

Now we are going to configure the repository to deploy to Github Pages. 

* Navigate to the repository settings via the ⚙ icon 
* Open the `Pages` section under the `Code and Automation` section
* From the `Source` section select the `gh-pages` branch and make sure that `/ root` is selected
* Now save. You should now be able to access your site at the following URL `<github_account_name>.github.io`

![repository-settings.png](/assets/images/how-I-built-this-site/repository-settings.png)

At this point if you don't want a custom domain then you are done! Now all that is left to do is to clone the 
repository onto your machine, read the Jekyll and Minimal Mistakes documentation and start customising
your site! 

Any changes you make on the `gh-pages` branch will automatically be deployed by Github once pushed. Bear in mind that
the changes can take a couple of minutes to appear.

## Custom Domain

If you're not satisfied with the free Github.io domain that comes with the site then this section is for you.

This section is going to be very brief because domain registration and DNS setup is a whole other topic. I am going to 
assume that you know how to register a domain and how to access the DNS settings.

Once you have your domain name you can do the following

* Open the DNS settings for your domain
* Create 4 A name records that point your domain towards the below IP addresses
    ```
    185.199.108.153
    185.199.109.153
    185.199.110.153
    185.199.111.153
    ```
* Create a CNAME record that points a `www` subdomain toward the `<github_account_name>.github.io` URL that was 
  generated earlier. It's important to not point this directly towards your custom domain!
* If your DNS settings contain a wildcard subdomain then you should remove this **urgently**. A wildcard subdomain
  will allow anyone to host a Github Pages site against your domain. This is an issue with Github Pages and not
  from this guide

That is it for the DNS settings. Now it's time to tell Github to use the custom domain

* Open the Github repository settings like we did in the [Github Pages](#github-pages) section
* In the `Custom Domain` section enter your domain without the www. subdomain and save
* Click on 'Enforce HTTPS'

These steps should create a new file called CNAME that contains your domain name on the `gh-pages` branch. Once 
the DNS updates you should now be able to access your custom domain and see your site.

That is all, you now have a fully working site with a custom domain name! For more information on custom domain
setup you can read the official Github Pages [documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/about-custom-domains-and-github-pages)

## Closing Thoughts

I hope this post has been insightful, it really is remarkable how quick it is to set up a basic website with the
right tools. Moving forward I'm hoping to play around with the CSS and layout. I might even try some other themes

If this post has been of interest you then be sure to follow me on [Twitter](https://twitter.com/KingSoftwareDev)
so that you can get alerted when future posts are released.