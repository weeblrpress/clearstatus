<p align="center"><img src="https://cdn.weeblrpress.net/clearstatus/assets/images/clearstatus-150.svg" alt="ClearStatus Logo"></p>

You run a website or an app? Have one or more systems your customers/community depends on? if something goes wrong and your site is down, we think what matters most is that you are able to communicate clearly and easily with your users: be transparent about the problem, what you do to solve it and when you're or will be back online.

It's called a status page and should be working no matter what happens to your own site and app. And it should be simple. And preferably cheap or free.

We've created ClearStatus to do just that for our own operations at [WeeblrPress](https://www.weeblrpress.com) and [Weeblr](https://weeblr.com). It is open source, free for all.

## How it works

ClearStatus is mostly a theme for the [Hugo CMS](https://gohugo.io). Hugo is a very fast static site generator. It does the bulk of the work, transforming a text file you write to describe an issue into a fully working status page.

> When hosting your status pages at Netlify as suggested below, all the transformation process is automatic. You do not need to perform any additional setup or configuration and you'll never have to deal with Hugo yourself (not that Hugo is difficult, quite the opposite in fact!)

Now any web page must be hosted on a server to be available. We suggest and use ourselves [Netlify](https://netlify.com) to host ClearStatus pages because setting up the whole thing can pretty much be done with a couple of clicks (just see below). In addition, it will be free including an SSL certificate for your site.

The last part missing is a repository for your content, that is the issues description and updates. That content needs to be stored in a GIT repository. You can use your own git repositories if you are a developer but we suggest you sign up for free accounts at [GitLab.com](https://gitlab.com) or [GitHub.com](https://github.com). Those 2 will work perfectly with ClearStatus. 

By using ClearStatus, GitLab or GitHub and Netlify, you can create and customize your statuspage in no time. Adding issues and communicating with your audience about your bad times will be simple and done completely outside of your own server(s) - an absolute necessity for a status page: the most important time it should work is exactly when the rest of your servers are down!

> Did we mention ClearStatus is multilingal? if you so desire, your status page will have a language switcher and separate content per language. Messages for English, Spanish and French are built-in and you can easily add your own.

## Requirements

Either:

- a Gitlab.com or Github.com account
- a Netlify account for easy and automated setup and operation

or:

- your own git repository and any other hosting for static files (you take care of hosting the status page)
 
## Getting started (automatic setup)

The easiest way to enable your status page is to use the Deploy to Netlify buttons below. Depending on whether you have/prefer to host your git repository on GitHub or GitLab, select one of the buttons below.

> Note that you will need to have signed up for a Gitlab or Github account and a Netlify account prior to getting started.

When you click one of those buttons, you will be taken to the Netlify website and the following will happen:

- They'll ask you to connect your Gitlab or Github account
- They'll ask you for **a project name** (you can create as many status pages as you like by the way)
- They'll start building your status page for you, it should take roughly 10 or 15 seconds
- The status page will be available at a weird URL such as https://tender-goodall-bd0396.netlify.com/ (you'll find the exact link on the Netlify page)

Just click that link and view your status page: it has some sample issues. You can start customizing it now (see below)

> From this point all customization or content update will be done using your GitLab or GitHub account.

### Create a Clearstatus status page on Netlify using GITHUB

Deploy to Netlify with one click from GitHub: 

[![Deploy to Netlify from Github](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/weeblrpress/clearstatus)

### Create a Clearstatus status page on Netlify using GITLAB

Deploy to Netlify with one click from GitLab: 

[![Deploy to Netlify from Gitlab.com](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://gitlab.com/weeblrpress/clearstatus)

## Customization 

After initial setup, your ClearStatus status page has sample content and default settings, titles, etc You certainly want to change them which you will do by visiting either your Gitlab/Github account and selecting the **project name** you choose on Netlify.

## Configuration

Almost everything should be configured through the single `config.yml` file located at the root of your project root repository. You can edit that file directly from GitLab/GitHub and change it as you whish.

After configuring all settings and text to your liking, you should `Commit changes`. This will cause:

- your file to be updated on GitHub/Gitlab
- and it will also trigger a rebuild of the status page to take your changes into account at Netlify. 

Wait 10-15 seconds and reload the status page: it should have all your changes now.

> Most likely the most important setting is the component definition: for instance if you run a website and a helpdesk. They are independant and can go down or up independantly so they are listed separately. Use the `systems` option to set them up as needed.

## Logo change

Upload your logo to the `/static/images` folder using GitHub/Gitlab upload feature. Then make sure the corresponding logo name is correctly set in  `config.yml`

````
logo: "/images/our-logo.png"
````

> Note that the "logo" setting should not include the initial /static part.


## Using a custom domain

As seen before, this default setup will cause your status page to be available at a weird Netlify URL such as  https://tender-goodall-bd0396.netlify.com/

That's OK for testing but not best for real world operation so you probably want to setup a custom domain for your status page, such as `status.company.net`. This is a 2-steps process:

1. At your Netlify control panel, set up a **custom domain**. See doc [on this page](https://www.netlify.com/docs/custom-domains/).
2. At your DNS provider (the company where you registered your domain name most likely), you will need to tell them to point your chosen address (`status.company.net`) to Netlify servers. The process depends on your registrar but, please follow the Netlify documentation there as well.

> It is advised to use a separate domain entirely for your status page. If your site is at https://example.com then it's best to purchase as well, for instance,  example.net or examplestatus.net and use that for your status page. The reason is simply that your DNS may also breaks and maybe someday anything at example.com will not be accessible. That's when you want to have example.net for your status page.
 
## Entering and updating content

Whenever a problem occurs on one of your systems, you will create *an issue*. An issue is actually a single file that you create in the `/content/en/issues` folder which exists in your ClearStatus installation on Gitlab/GitHub. This is assuming your site language is **en** which you may have changed in the configuration file. Adjust instructions accordingly.

> On multilingual setups, you should create one file per language in  `/content/en/issues`, `/content/es/issues` at least if you need to report the issue to all your audiences.

## Issue file naming

The issue file should be created with the following convention:

````
2019-04-10-title-of-issue.md
````   

- should start with a date in the `YYYY-MM-DD` format
- then a title with no spaces
- with a `.md` extension

## Issue file content and template.

The issue file should use the MARKDOWN language, which is basically just text and images with little in terms of formatting and is what Hugo normally uses.

The first section of the file is however used to tell ClearStatus about the, well, status of the event happening and you should use it to convey your message to visitors.

Once you have written the current event description, use the `Commit changes` button in Github/GitLab to save the content. This will trigger an update of your status page after a few seconds.

When the issue status changes, for instance when it's resolved or some more information is available, come back to this page, modify the event file and use `Commit changes` again to update your status page.

Here is a sample issue file, you should use it as a template:


````

---
title: Connectivity issue

draft: false

# Full date: 2019-03-29 17:26:09
date: 2019-03-30 20:03:00

# Status: "resolved" | "in_progress" | "scheduled"
status: "resolved"

# Duration: Raw text, ie 5mn, 1h, 1 hour,..
duration:

# Max severity: will be displayed when issue is resolved, in the past events section
# Max_severity: ok | disrupted | down | monitoring | maintenance
max_severity: down

# Current severity: used for current issue display
# current_severity: ok | disrupted | down | monitoring | maintenance
current_severity: ok

# Full date: 2019-03-29 17:26:09
resolvedOn: 2019-03-30 20:45:19

# Affected components, must use exact names defined in site config
affected:
  - Site
  - Helpdesk

section: issue

# Short code available in content to display current date
# in a short format. For instance for issue updates.

# {{< track "2019-03-26 15:31:06" >}}
# {{< track "" >}}

## Enter below issue description and subsequent updates if any
---

Both our website and customer support area cannot be reached at the moment. We are investigating the matter.
\
**Issue identified:** Our hosting company has informed us of a failure in the datacenter network equipment. They are working on it and expect a quick resolution.  {{< track "2019-03-30 20:08:19" >}}
\
**Monitoring:** The equipment in question has been replaced and website and support site can be reached. We are monitoring the servers for the next few minutes to be sure all is OK. {{< track "2019-03-30 20:31:19" >}}
\
**Resolved:** Both servers are operating normally, issue is solved. Really sorry about the trouble!
\

````

Here is a breakdown of options available:

- `title`: a short and explicit title for the event happening such as "Helpdesk not available" or "Site under maintenance" 
- `date`: the date and time at which the event started - or will start in the case of scheduled events 
- `status`: 3 options: `resolved`, `in_progress` or `scheduled`. 

`in_progress` events are listed at the top of your status page, with a red header
`resolved` events are listed at the bottom of the page, with a neutral colored header
`scheduled` events are listed just below the list of components (systems) on your page with a lighlty colored header.

- `duration` is only used for **scheduled** event. Use that field to tell visitors how long that scheduled event is supposed to last. It's free text, can be "about 5 mn", "1 hour" or "1h"

- `max_severity` and `current_severity` are used to display an event importance and severity. Both can be: `ok`, `disrupted`, `down`, `monitoring` or `maintenance`

`current_severity` is used when an event is `in_progress`. `max_severity` will be used when the event is resolved to indicate what the worst state of operation was. Typically, while an event is in progress, you will first set `current_severity` to `down`. Then as you make progress towards resolution then maybe you can change the state to `disturbed` or `monitoring` after you think the problem is solved but you are monitoring to be sure it does not come back. 
Once the problem is fully solved, you can set its `status` option to `resolved`. That's when we'll use the `max_severity` as it is important to remember the system was down, even though the last severity level displayed may have been `disrupted` or `monitoring` only.



## Getting started (manual setup)

Assuming you are familiar with git and/or Hugo, you may prefer to setup ClearStatus using a local git repo and then possibly host your status page elsewhere than Netlify.

ClearStatus comes in 2 flavors or rather 2 git repositories:

- `clearstatustheme` is a **Hugo theme**. You can check it out and use it in any Hugo web site. It has an ExampleSite folders with a sample config.yml file you should use. 

- `clearstatus` is a **Hugo site**. It's basically an empty site with the `clearstatustheme` setup as a git submodule, a config.yml file and some sample content. This is what is deployed to Netlify when using the automated setup. It's the preferred method deployment.

A suggested use is to clone the `clearstatustheme` repository in your own repo and just configure it for your own hosting as needed.

You can update the ClearStatus theme, whenever we a new version is available, by running the following from the root of the main repository:

````  
git submodule foreach git pull origin master
````

Both original repositories are available at:

#### `clearstatustheme`

- [https://github.com/weeblrpress/clearstatustheme](https://github.com/weeblrpress/clearstatustheme)
- [https://gitlab.com/weeblrpress/clearstatustheme](https://gitlab.com/weeblrpress/clearstatustheme)

#### `clearstatus`

- [https://gitlab.com/weeblrpress/clearstatus](https://github.com/weeblrpress/clearstatus)
- [https://github.com/weeblrpress/clearstatus](https://gitlab.com/weeblrpress/clearstatus)

> Please us the [Github clearstatus repository](https://github.com/weeblrpress/clearstatustheme/issues) for any issue you may have, suggested changes or pull requests

## Credits

This project is inspired by [CState](https://github.com/cstate/cstate) and started out both out of slightly different requirements and the desire to work with Hugo, Netlify, Go templates and such.


