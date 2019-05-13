<p align="center"><img src="https://cdn.weeblrpress.net/clearstatus/assets/images/clearstatus-200.svg" alt="ClearStatus Logo"></p>

<p align="center"><a title="ClearStatus intro video link" href="https://www.youtube.com/watch?v=wFF2OBPfalQ"><img src="https://img.youtube.com/vi/wFF2OBPfalQ/0.jpg" alt="ClearStatus status page intro video"></a></p>
<p align="center">Click image to view intro video</p>
<p align="center">We also have a <a href="https://www.youtube.com/watch?v=f6gM84hD9Ug" title="ClearStatus setup and usage video link">full setup and usage video here.</a></p>

# ClearStatus - Professional status page - 5 minutes - Free

You run a website or an app? Have one or more systems your customers/community depends on? if something goes wrong and your site is down, we think what matters most is that you are able to communicate clearly and easily with your users: be transparent about the problem, what you do to solve it and when you're or will be back online.

It's called a status page and should be working no matter what happens to your own site and app. And it should be simple. And preferably cheap or free.

<img align="right" src="https://cdn.weeblrpress.net/clearstatus/features/event-in-progress-with-twitter-feed-small.png" alt="Clearstatus at work">

We've created ClearStatus to do just that for our own operations at [WeeblrPress](https://www.weeblrpress.com) and [Weeblr](https://weeblr.com) and it is now open-source and available for all.

## Key features

- Easy and reliable communication with your users
- One click implementation
- 100% independent from your own infrastructure
- Custom domain with HTTPS (Netlify)
- Worldwide CDN delivery (Netlify)
- High-availability (Netlify)
- Twitter integration
- Disqus commenting on each issue
- Pinned issue for security alerts
- Secure: static content is hard to hack
- All content under your control
- Multiple users, issues and status pages
- Mobile/tablets/desktop
- Highly customizable and expandable

And 100% free setup and operation with all the above included

<p>&nbsp;</p>

## How it works

<p align="center">Can't wait? view our video on settin up and using ClearStatus. Just click the image below</p>
<p align="center"><a title="ClearStatus setup and usage video link" href="https://www.youtube.com/watch?v=f6gM84hD9Ug"><img src="https://img.youtube.com/vi/f6gM84hD9Ug/0.jpg" alt="ClearStatus status page setup and usage video"></a></p>


ClearStatus is mostly a theme for the [Hugo CMS](https://gohugo.io). Hugo is a very fast static site generator. It does the bulk of the work, transforming a text file you write to describe an issue into a fully working status page.

> When hosting your status pages at Netlify as suggested below, all the transformation process is automatic. You do not need to perform any additional setup or configuration and you'll never have to deal with Hugo yourself (not that Hugo is difficult, quite the opposite in fact!)

Now any web page must be hosted on a server. We suggest and use ourselves [Netlify](https://netlify.com) to host ClearStatus pages because setting up the whole thing can pretty much be done with a couple of clicks (just see below). In addition, it will be free including an SSL certificate for your site, served over a worldwide CDN and in a high-availability configuration.

The last part missing is a repository for your content, that is the issues description and updates. That content needs to be stored in a GIT repository. You can use your own git repositories if you are a developer but we suggest you sign up for free accounts at [GitLab.com](https://gitlab.com) or [GitHub.com](https://github.com). Those 2 will work perfectly with ClearStatus. 

By using ClearStatus, GitLab or GitHub and Netlify, you can create and customize your statuspage in no time. Adding issues and communicating with your audience about your bad times will be simple and done completely outside of your own server(s) - an absolute necessity for a status page: the most important time it should work is exactly when the rest of your servers are down!

You can and should use other media to communicate such as Twitter. But tweets come and go and quickly disappear in the Twitter feeds - when they are not simply hidden by Twitter algorithms. Your status page provides a fixed location where your users can go and be updated.
As a matter of fact, you can easily embed relevant tweets to a specific issue so you get best of both worlds as you can see in the screenshot above.

> Did we mention ClearStatus is multilingal? if you so desire, your status page will have a language switcher and separate content per language. Messages for English, Spanish and French are built-in and you can easily add your own.

## Requirements

Either:

- a Gitlab.com or Github.com account
- a Netlify account for easy and automated setup and operation

or:

- your own git repository and any other hosting for static files (you take care of hosting the status page)
 
## Getting started (automatic setup)

The easiest way to enable your status page is to use the **Deploy to Netlify** buttons below. Depending on whether you have/prefer to host your git repository on GitHub or GitLab, select one of the buttons below.

> Sign up for a Gitlab or Github account and a Netlify account prior to getting started.

When you click one of those buttons, you will be taken to the Netlify website and the following will happen:

- They'll ask you to connect your Gitlab or Github account
- They'll ask you for **a project name** (you can create as many status pages as you like by the way)
- They'll start building your status page for you, it should take roughly 10 or 15 seconds
- The status page will be available at a weird URL such as https://tender-goodall-bd0396.netlify.com/ (you'll find the exact link on the Netlify page)

Just click that link and view your status page: it has some sample issues. You can start customizing it now (see below)

> From this point all customization or content update can be done using your GitLab or GitHub account. You can also setup **Netlify CMS** to customize your status page with a simple online interface. Setting up Netlify CMS is simple and is described below.

### Create a Clearstatus status page on Netlify using GITHUB

Deploy to Netlify with one click from GitHub: 

[![Deploy to Netlify from Github](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/weeblrpress/clearstatus)

### Create a Clearstatus status page on Netlify using GITLAB

Deploy to Netlify with one click from GitLab: 

[![Deploy to Netlify from Gitlab.com](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://gitlab.com/weeblrpress/clearstatus)

## Netlify configuration

There are 2 additional steps you probably want to take when using Netlify:

### Using a custom domain

As seen before, this default setup will cause your status page to be available at a weird Netlify URL such as  https://tender-goodall-bd0396.netlify.com/

That's OK for testing but not best for real world operation so you probably want to setup a custom domain for your status page, such as `status.company.net`. This is a 2-steps process:

1. At your Netlify control panel, set up a **custom domain**. See doc [on this page](https://www.netlify.com/docs/custom-domains/).
2. At your DNS provider (the company where you registered your domain name most likely), you will need to tell them to point your chosen address (`status.company.net`) to Netlify servers. The process depends on your registrar but please follow the Netlify documentation there as well.

> It is advised to use a separate domain entirely for your status page. If your site is at https://example.com then it's best to purchase as well, for instance,  example.net or examplestatus.com and use that for your status page. The reason is simply that your DNS may also break and maybe someday anything at example.com will not be accessible. That's when you want to have example.net for your status page. Ideally, you would purchase that second domain name at a separate provider just in case it is your DNS provider which is down.

### Enable Netlify CMS

[NetlifyCMS](https://netlifycms.org) is a simple content management system that lets you update your ClearStatus configuration and content in a convenient interface, without having to deal with your git repository. This may be more convenient for users not familiar with git.

ClearStatus comes with support for NetlifyCMS. You need to enable user authentication **inside of your Netlify control panel**:

1. On your team page, select the ClearStatus website you just created
2. Select the `Settings` page and then `Identity` in the left side menu
3. Click on `Enable identity`
4. Scroll down to `Registration` and select `Invite only` so that only selected users can modify your page
5. Scroll down to `Services`, then `Git gateway` and click the `Enable git gateway` button 

The final step is to invite yourself so that you can modify the site:

1. On your team page, select the ClearStatus website you just created
2. Select the `Identity` tab
3. Click on the `Invite users` button
4. Enter your email address in the popup dialog, and possibly that of more users (they'll need to have a Netlify account for this to work)

Invited users receive an email invite with a confirmation link. Clicking the *Accept invite* link in that email will take them to your site with a login prompt.

Once a user has accepted the invite, they can always access the Netlify CMS interface to add or modify content using the address:

```
https://yourstatuspage.com/admin
```


## Customization 

After initial setup, your ClearStatus status page has sample content and default settings, titles, etc You certainly want to change them. There are 2 ways to do that:
 
- use your Gitlab/Github account and update files in the **project name** you choose on Netlify
- use the Netlify CMS support built-in ClearStatus which we suggested to enable earlier

> You can use both methods at the same time on the same status page. All data from Netlify CMS is written to your git repository so both will always be in sync. You can also use your preferred git workflow. In the end, the status page content is updated based on the git repository content in `master` branch.

## Configuration

Most options should be configured through the single `config.yml` file located at the root of your project root repository. You can edit that file directly from GitLab/GitHub and change it as you whish.

Most likely the most important setting is the component definition: for instance if you run a website and a helpdesk, they are independent and can go down or up independently so they are listed separately. Use the `systems` option to set them up as needed.

> You can change those options as well using the **Netlify CMS** interface under the `Settings` tab.

After configuring all settings and text to your liking, you should `Commit changes`. This will cause:

- your file to be updated on GitHub/Gitlab
- and it will also trigger a rebuild of the status page to take your changes into account at Netlify. 

Wait 10-15 seconds and reload the status page: it should have all your changes now.

> There are several additional options files located under the `/config/_default` folder: they contain other settings including language-related ones under `languages.yml` and color-related under `params.yml`


## Logo change

You can include your organization log in all pages header. Upload your logo to the `/static/images` folder using GitHub/Gitlab upload feature. Then make sure the corresponding logo name is correctly set in  `config.yml`. Leave that setting empty if you do not have any logo.

````
logo: "/images/our-logo.png"
````

> Note that the "logo" setting **should not include the initial /static** part.

## Entering and updating content

Whenever a problem occurs on one of your systems, you will create *an issue*. An issue is actually a single file that you create in the `/content/default/issues` folder which exists in your ClearStatus installation on Gitlab/GitHub. This is assuming you have enabled only one language which is the default configuration.

In the following steps, we assume you are using Gitlab/Github to directly create the issue file. You can of course create it anywhere using standard git procedure. The issue will be added to the site once you push it to the `master` branch of your Clearstatus repository.

> On multilingual setups, you should create one file per language in  `/content/default/issues`, `/content/es/issues`, `/content/fr/issues`  at least if you need to report the issue to all your audiences.

## Issue file naming

The issue file should be created with the following convention:

````
2019-04-10-title-of-issue.md
````   

- should start with a date in the `YYYY-MM-DD` format
- then a title with no spaces
- with a `.md` extension

> The start page of a ClearStatus status page displays all present and past events. However each event also has an individual URL that you can share. Click on an issue header to reach that page.

## Issue file content and template.

Issue files use the [markdown](https://daringfireball.net/projects/markdown/syntax) language, which is basically just text and images with little in terms of formatting and is what [Hugo](https://gohugo.io) normally uses.

The first section of the file is used however to tell ClearStatus about the, well, status of the event happening and you should use it to convey your message to visitors.

Once you have written the current event description, use the `Commit changes` button in Github/GitLab to save the content. This will trigger an update of your status page after a few seconds.

When the issue status changes, for instance when it's resolved or some more information is available, come back to this page, modify the event file and use `Commit changes` again to update your status page.

Here is a sample issue file, you can use it as a template:


````

---
title: Connectivity issue

draft: false

# Full date: 2019-03-29 17:26:09
date: 2019-03-30 20:03:00

# Status: "resolved" | "in_progress" | "scheduled"
status: "resolved"

# This message will be taken out of the flow of events
# and displayed at top of page or below the header
# as long as its status is marked as in_progress
# pinned: (empty) | top | belowheader
pinned: 

# Duration for "scheduled" issues: Raw text, ie 5mn, 1h, 1 hour,..
duration:

# Max severity: will be displayed when issue is resolved, in the past events section
# Max_severity: ok | disrupted | down | monitoring | maintenance
max_severity: down

# Current severity: used for current issue display
# current_severity: ok | disrupted | down | monitoring | maintenance
current_severity: ok

# Full date: 2019-03-29 17:26:09
resolved_on: 2019-03-30 20:45:19

# Affected components, must use exact names defined in site config
affected:
  - Site
  - Helpdesk

# If set and the status is in_progress, this feed will be embedded
# in the event display. Leave empty for no Twitter feed.
# Possible URL formats:
# See:  https://help.twitter.com/en/using-twitter/embed-twitter-feed
#
# - Profile: Display public Tweets from any user on Twitter:
#    https://twitter.com/weeblrpress
#  
# - Likes: Show all Tweets a specific user has marked as likes.
#    https://twitter.com/TwitterDev/likes
#
# - List: Show Tweets from public Lists that you own and/or subscribe to.
#    https://twitter.com/TwitterDev/lists/national-parks
# 
# - Collection: Show Tweets from a curated collection.
#    https://twitter.com/WeeblrPress/timelines/1118432874733219840
#
# - Moment: Show Tweets from a public moment.
#    https://twitter.com/i/moments/625792726546558977
#
twitterFeed:

# Enable Disqus commenting on this page. This will only works if 
# you added your Disqus identifier in the global config.yml file
# under the disqusShortname option.
# enabledDisqus: true | false
enableComments: true

# Do not change
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

- `pinned`: if you set this to `top` or `belowheader` and set its status to `in_progress`, the event will be taken out of the regular display and will show at the very top of each page or just below the header, respectively. This is meant to display an important message in a prominent manner to all visitors such as a security warning. Once the status is reset to anything else but `in_progress`, the event will not be displayed anywhere anymore.

Pinned items also have a simplified layout:

<p align="center"><img src="https://cdn.weeblrpress.net/clearstatus/features/pinned-item.png" alt="Pinned message example"></p>

- `duration` is only used for **scheduled** event. Use that field to tell visitors how long that scheduled event is supposed to last. It's free text, can be "about 5 mn", "1 hour" or "1h"

- `max_severity` and `current_severity` are used to display an event importance and severity. Both can be: `ok`, `disrupted`, `down`, `monitoring` or `maintenance`

`current_severity` is used when an event is `in_progress`. `max_severity` will be used when the event is resolved to indicate what the worst state of operation was.

Typically, while an event is in progress, you will first set `current_severity` to `down`. Then as you make progress towards resolution you can change the state to `disrupted` or `monitoring` after you think the problem is solved but you are monitoring to be sure it does not come back. 

Once the problem is fully solved, you can set its `status` option to `resolved`. That's when we'll use the `max_severity` as it is important to remember the system was down, even though the last severity level displayed may have been `disrupted` or `monitoring` only.

- `resolved_on`: an optional date and time. Required when an event has been marked as `resolved` in its `status` field.

- `affected`: a list of components that are affected by the event. Add one component per line and use exactly the same name you used on your configuration file.

- `twitterFeed`: an optional Twitter feed or collections. If provided, the feed will be embedded in the issue card as long as it is marked as `in_progress`. We specifically recommend creating a [Twitter collection](https://developer.twitter.com/en/docs/tweets/curate-a-collection/overview/overview.html) for this purpose. This way only tweets related to that specific issue will be displayed.

- `enableComments`: another excellent way to communicate directly with your users. Clearstatus can include commenting on each issue individual page. You can enable/disable commenting per issue. The only pre-requisite is to set your [Disqus shortname](https://disqus.com) under the `disqusShortname` option in the global configuration file. You will of course need to set up a Disqus account for your status page to make this work.

> We advise to use a dedicated shortname for your status page, separate from any other Disqus shortname you may be using on your other websites.

- `body`: the body is the free text area located after the `---` line (do not touch or remove this line by the way). It is just plain text you can write to describe it. You can add to, remove from or update that text to your liking using markdown for nicer formatting. 
 
## Getting started (manual setup)

Assuming you are familiar with git and/or Hugo, you may prefer to setup ClearStatus using a local git repo and then possibly host your status page elsewhere than Netlify.

ClearStatus comes in 2 flavors or rather 2 git repositories:

- `clearstatustheme` is a **Hugo theme**. You can check it out and use it in any Hugo web site. It has an ExampleSite folders with a sample config.yml file you should use. 

- `clearstatus` is a **Hugo site**. It's basically an empty site with the `clearstatustheme` setup as a git submodule, a config.yml file and some sample content. This is what is deployed to Netlify when using the automated setup. **It's the preferred method deployment**.

Alternatively, you can clone only the `clearstatustheme` repository in your own repo and just configure it for your own hosting as needed.

Make sure to clone the `clearstatustheme` with **submodules** or else you will only get the main site without the Clearstatus theme. For instance:

````
git clone --recurse-submodules https://github.com/weeblrpress/clearstatus.git mystatuspage
````

You can update the ClearStatus theme whenever a new version is available by running the following from the root of the main repository:

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

> Please us the [Github Clearstatus repository](https://github.com/weeblrpress/clearstatustheme/issues) for any issue you may have, suggested changes or pull requests

## Changing text - Translation

Longer descriptions in header and footers can be changed from the `config.yml` file in the root folder of your ClearStatus site. Other strings and messages are available for translation or just to better suit your liking or use case.

Those strings are stored in the `/themes/clearstatustheme/i18n` folder. There is one file per language called for instance `en.yml`, `fr.yml`,...

> You can select the site language in the `/config.yml` file under the `languageCode` key. It defaults to `en`.

Here is a sample content from the `en.yml` file:

````
# Summary status message
- id: scheduled
  translation: Scheduled

- id: isDown
  translation: Something's happening here...
- id: isDisrupted
  translation: Having a little bit of trouble...
- id: isMonitoring
  translation: Some systems being monitored...
- id: isMaintenance
  translation: Some systems under maintenance...
- id: isOk
  translation: All systems operational.
````

Should you want to add your own translation or just override one of those messages, you should not modify directly those files as this would make updating ClearStatus more dificult.

Instead, you can add an override in your site that will take over the original ClearStatus text. Proceed as follow to change text for the English language:

- Create a `i18n` folder at the root of your site
- Create a file called `en.yml` in that folder
- Insert the following in that file:

````
- id: isDown
  translation: Houston, we have a problem...
````
- Save the file and commit the changes.

Now the original _Something's happening here..._ will be replaced with _Houston, we have a problem..._ whenever one component in your systems is down.

Note that you do not have to copy across **all** text from the original file. Just copy and modify the content you need to modify.

Should you want to add translation for another language, copy the entire `en.yml` file to `xx.yml` where xx is the desired language code and start translating.

## Enabling multilingual support

ClearStatus can manage events in several languages so that you can communicate with your users in their language. Each language has **independent** content. Per language content is stored in per-language folders and if you do not provide a language-specific version of an event, it will not be displayed for that language.

> At this moment, multilingual support cannot be managed through the **Netlify CMS** interface. Use Gitlab/Github or your own git workflow to manage content.

### Enabling multilingual support.

Open the `/config/_default/languages.yml` file to enable and configure multilingual content. Here is the default language configuration: 

````
#
#en:
#  weight: 1
#  languageName: English
#fr:
#  title: Etat de nos systèmes
#  weight: 2
#  contentDir: content/fr
#  languageCode: fr
#  languageName: Français
#  params:
#    systems:
#      - name: Website
#        description: Le site web de notre société
#        link: https://www.example.fr/
#      - name: Support
#        description: Notre site de support
#        link: https://support.example.fr/
#
#es:
#  title: Nuestra página de estado
#  weight: 3
#  contentDir: content/es
#  languageCode: es
#  languageName: Español
````

As you can see, all lines in that file start with a `#`: they are commented out and have no effect. To add more languages to your site, you will need to remove the `#` symbol at the start of the desired lines and configure as needed. Here is an example for adding both Spanish and French to a site with English as the default language:

````
en:
  weight: 1
  languageName: English
fr:
  title: Etat de nos systèmes
  weight: 2
  contentDir: content/fr
  languageCode: fr
  languageName: Français
  params:
    systems:
      - name: Website
        description: Le site web de notre société
        link: https://www.example.fr/
      - name: Support
        description: Notre site de support
        link: https://support.example.fr/

es:
  title: Nuestra página de estado
  weight: 3
  contentDir: content/es
  languageCode: es
  languageName: Español
````

A few key points:

- each language is defined under its language code (use what you want there, it really is up to you)
- for each language, you can redefine configuration items already defined for the default language.
For instance, adding the `title: Etat de nos systèmes` line replaces the original `title` text for French. You can also redefine the name and list of components in your systems per language
- the `weight` parameter will determine the order of languages in the language switcher and default language.

> As with all `yml` files, **indentation matters**. Be sure to respect spaces at the start of lines or else your file will be invalid and the status page won't be built.

After saving and committing this configuration file, you will get the following:

<p align="center"><img src="https://cdn.weeblrpress.net/clearstatus/features/multilingual-default-language-small.png" alt="Sample Clearstatus multilingual status page"></p> 

There is a language switcher added at the top. Clicking on the `Français` link goes to the following page:

<p align="center"><img src="https://cdn.weeblrpress.net/clearstatus/features/multilingual-other-language-small.png" alt="Sample French Clearstatus multilingual status page"></p>

## In-depth customization

### Colors

ClearStatus output uses the [Tailwind CSS](https://tailwindcss.com) framework. Most of the colors used throughout the status page can be modified without having to deal with Tailwind though as they are stored in parameters in the `/config/_default/params.yml` file. Here is the relevant content of that file:

````
############################################################
## Status default config. Valid for ALL languages.
############################################################

## Source for CSS
enablePostCSSProcessing: false
fullCSSSourceFile: "css/src/styles.css"
fullCSSDistFile: "css/dist/styles.css"
postCSSConfigFolder: "themes/clearstatustheme"

# Colors
bodyBackground: "bg-grey-lighter"
bodyColor: "text-grey-dark"
visibleBordersColor: "border-grey-dark"
bordersColor: "border-transparent"
headerBackground: "bg-white"
headerColor: "text-grey-darkest"
footerBackground: "bg-white"
footerColor: "text-grey-darkest"
componentsBackground: "bg-white"
componentsColor: "text-black"
componentsBorders: "border-grey-lighter"
refreshColor: "text-grey-dark"
paginationLinksColor: "text-grey-darkest"
disabledPaginationLinksColor: "text-grey-dark"

# Severity
defaultSeverityBackground: "bg-grey-light"
defaultSeverityColor: "text-black"
downSeverityBackground: "bg-red-dark"
downSeverityColor: "text-white"
disruptedSeverityBackground: "bg-orange-dark"
disruptedSeverityColor: "text-white"
monitoringSeverityBackground: "bg-orange"
monitoringSeverityColor: "text-white"
maintenanceSeverityBackground: "bg-grey-light"
maintenanceSeverityColor: "text-black"
okSeverityBackground: "bg-green-dark"
okSeverityColor: "text-white"

# Incident types
scheduledHeaderBackground: "bg-blue-lighter"
scheduledHeaderColor: "text-grey-dark"
scheduledHeaderTitleColor: "text-black"
scheduledBodyBackground: "bg-white"
scheduledBodyColor: "text-grey-darkest"
scheduledBodyTitleColor: "text-black"

smallBodyBackground: "bg-white"
smallBodyColor: "text-grey-darkest"
smallBodyTitleColor: "text-black"

pastBodyBackground: "bg-white"
pastBodyColor: "text-grey-darkest"
pastBodyTitleColor: "text-black"

# Affected components
affectedBackground: "bg-grey-lighter"
affectedColor: "text-grey-darkest"

````

Various items each have a color assigned to them such as `bg-grey-lighter`  or `text-grey-dark`. Those are standard Tailwind CSS classes that each correspond to a color. Find the list of Tailwind built-in colors:
 
 - [for text](https://tailwindcss.com/docs/text-color)
 - [for backgrounds](https://tailwindcss.com/docs/background-color)
 - [for borders](https://tailwindcss.com/docs/border-color)

If you simply want to swap around colors from the existing list in `/config/_default/params.yml`, just do it, save and commit the file and your status page will be updated accordingly.

If you want to use a color that is not listed already in `/config/_default/params.yml`, you will need a bit more configuration described in the paragraph below, **Even more in-depth customization**.

### CSS customization / Head customization

To only add a few CSS classes or override existing ones, you can insert a `<style></style>` tag in your own copy of one specific layout file.

- copy `/themes/clearstatustheme/layouts/partials/custom/meta.html` to `/layouts/partials/custom/meta.html`

The content of this file will be automatically included just before the closing `</head>` tag. You can also use this method to add support for an Analytics provider or other script for instance.

> There are other files in that `/themes/clearstatustheme/layouts/partials/custom/` folder. Make your own copy under `/layouts` and use them to add HTML to various parts of your status page: above the header, above footer, below footer, etc

### Layouts

All output files are generated using **layouts** files located in the ClearStatus theme under the folder `/themes/clearstatustheme/layouts`.

You can safely and completely change any of those files by creating a `/layouts` folder at the root of your status page git repo and copy the files you want to change from the `/themes/clearstatustheme/layouts` folder.

Be sure to reproduce the original folders hierarchy though: `/themes/clearstatustheme/layouts/issues/single.html` should be copied to `/layouts/issues/single.html` or else ClearStatus won't pick it up.

> If you only use TailwindCSS CSS classes already present in the default version of ClearStatus, there is nothing more to do. If not, follow the steps in **Even more in-depth customization** below. 

### Even more in-depth customization

To include CSS classes from TailwindCSS that are not in the default ClearStatus version, do the following:

- copy the files `/themes/clearstatustheme/package.json` and `/themes/clearstatustheme/package-lock.json` to the root of your git repository
- run `npm install` in the root folder of your repositiry
- change `enablePostCSSProcessing` setting from `false` to `true` in `/config/_default/params.yml`

When `enablePostCSSProcessing` is set to `true`, ClearStatus will run a module called `PostCSS` to build the final CSS stylesheet starting with TailwindCSS framework. This allows including any class from TailwindCSS in an optimized manner, by including only those classes that are actually used.

You can go one step further and define your own colors inside of TailwindCSS:

- in `/config/_default/config.yml`, change `assetsDir: themes/clearstatustheme/assets` to `assetsDir: assets`
- copy the `/themes/clearstatustheme/assets` folder to the root of your repository, that is to `/assets`
- open the file `/assets/css/src/tailwind.js`
- customize it as described on [TailwindCSS documentation](https://tailwindcss.com/docs/colors)
- save and commit 

From now on, all colors added to the `/assets/css/src/tailwind.js` configuration file can be used through your status page custom layouts. Only CSS classes actually used will be included to generate the smallest possible file.

## Credits

This project is loosely inspired by [CState](https://github.com/cstate/cstate) and started out both out of different requirements and the desire to work with Hugo, Netlify, Go templates and such.


