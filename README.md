# **Documentation Course Websites: A Jekyll theme (based on Millennial)** {#documentation-course-websites:-a-jekyll-theme-(based-on-millennial)}

[Documentation Course Websites: A Jekyll theme (based on Millennial)](<#documentation-course-websites:-a-jekyll-theme-(based-on-millennial)>)

## Table of Contents

[1\. Introduction](#1.-introduction)

[1.1 Publishing Scenarios](#1.1-publishing-scenarios)

[1.2 Remote Build Prerequisites](#1.2-remote-build-prerequisites)

[1.3 Local Build Prerequisites](#1.3-local-build-prerequisites)

[1.3.1 Jekyll](#1.3.1-jekyll)

[1.3.2 Visual Studio Code](#1.3.2-visual-studio-code)

[2\. Installation](#2.-installation)

[2.1 Local installation](#2.1-local-installation)

[2.2 Installation via Github and Github Desktop](#2.2-installation-via-github-and-github-desktop)

[2.3 GitLab](#2.3-gitlab)

[2.3.1 Advanced Github-GitLab Sync](#2.3.1-advanced-github-gitlab-sync)

[2.3.1.1 .git config](#2.3.1.1-.git-config)

[2.3.2 Enable pages and CI Pipelines](#2.3.2-enable-pages-and-ci-pipelines)

[2.4 Directory Structure](#2.4-directory-structure)

[3\. Configuration / Features](#3.-configuration-/-features)

[3.1 Posts](#3.1-posts)

[3.2 Slides / Reveal.JS](#3.2-slides-/-reveal.js)

[3.2.1 Sidebar-Menu](#3.2.1-sidebar-menu)

[3.3 Zotero / Bibliography integration](#3.3-zotero-/-bibliography-integration)

[3.4 Pages](#3.4-pages)

[3.4.1 Redirects](#3.4.1-redirects)

[3.5 HTML-Layouts](#3.5-html-layouts)

[3.6 Glossary](#3.6-glossary)

[3.7 Podcast](#3.7-podcast)

[3.7.1 Podcast-Page](#3.7.1-podcast-page)

[3.7.2 Podcast-Posts](#3.7.2-podcast-posts)

[3.7.3 Podcast.xml](#3.7.3-podcast.xml)

[4\. Further modifications](#4.-further-modifications)

[4.1 Ruby Gems](#4.1-ruby-gems)

[4.2 GitHub](#4.2-github)

# **1\. Introduction** {#1.-introduction}

Course Websites is a customized Jekyll theme inspired by the layout and structure of the [Millennial theme](https://github.com/LeNPaul/Millennial). Students can easily follow the structure of your course with pages for each class session, reading assignments from Zotero, slides using RevealJS, glossary pages, and podcasts. Creating content is primarily done with Markdown, but you can also use HTML where you need more advanced options. Detailed information about this theme is provided below in the README.

## **1.1 Publishing Scenarios** {#1.1-publishing-scenarios}

You will create and edit content for your course website on your own device in Markdown. To publish it to a website, you have the following options:

1. **Remote build:** Upload your files to GitHub Pages or GitLab Pages, where they are converted to an HTML website. _Optional_: If you want to test your website _before_ uploading, you should install Jekyll on your own computer (see Local build below).
2. **Local build:** Install Jekyll on your own computer and use it to create the HTML website, then upload these HTML pages to any server.

## **1.2 Remote Build Prerequisites** {#1.2-remote-build-prerequisites}

On GitHub Pages, you can create and serve your website with a free user account, but your website and its code will have to be public.

GitLab is not centralized, so you may be using an instance from your university. You will need an account with permissions to create “organizations” and “projects,” and your administrator must have GitLab Pipelines and Pages enabled. Using the process described here, your website created with GitLab will be public, but the code you use to create it doesn’t have to be.

## **1.3 Local Build Prerequisites** {#1.3-local-build-prerequisites}

To run and use Course Websites on your own computer, you need to install Ruby and [Jekyll](https://jekyllrb.com). Jekyll is a static site generator that transforms [Markdown](https://www.markdownguide.org/) content and [Liquid](https://jekyllrb.com/docs/liquid/) templates into a complete static website, blog, or documentation site. Ruby plays a critical role as the programming language that powers the tool. It is a dynamic, open-source programming language with a focus on simplicity and productivity. Additionally, using a source editor like Visual Studio Code is highly recommended, as it offers plugins that make working with your Jekyll page much easier.

### 1.3.1 Jekyll {#1.3.1-jekyll}

As Course Websites is a customized Jekyll theme, the first step is to install Jekyll and Ruby on your device. For detailed installation instructions, please visit [Jekyll's official installation guide](https://jekyllrb.com/docs/installation/). This step-by-step tutorial provides comprehensive instructions for different operating systems.

### 1.3.2 Visual Studio Code {#1.3.2-visual-studio-code}

Using a source editor like Visual Studio Code will significantly enhance your workflow when working with a Jekyll page. It offers several useful plugins that can greatly improve your efficiency. Notable plugins for improving your Jekyll workflow in Visual Studio Code include:

- **Jekyll Run**: This extension allows you to run your Jekyll site locally and open it in a browser easily.
- **GitHub Copilot**: An AI tool that can assist you in solving various problems.

To install Visual Studio Code on your device, please follow the instructions at [Visual Studio Code download page](https://code.visualstudio.com/download).

# **2\. Installation** {#2.-installation}

Once you have met the prerequisites, there are several ways to install Course Websites on your device. The following section outlines the different methods for a successful installation.

## **2.1 Local installation** {#2.1-local-installation}

The first method to install Course Websites is by downloading it from [this link](https://github.com/jirelations/Millennial/archive/refs/heads/gh-pages.zip) and adding it to your local files. Simply unzip the file and place it in its own directory. Once done, open the directory with your preferred source editor. First, run `bundle install`, then run `jekyll serve` in a new terminal. Your Jekyll page will now be running locally at [`http://localhost:4000/`](http://localhost:4000/).

## **2.2 Installation via Github and Github Desktop** {#2.2-installation-via-github-and-github-desktop}

Another method of installing Course Websites is through GitHub or GitHub Desktop. To use the GitHub web interface, navigate to [this repository](https://github.com/jirelations/Millennial) and fork it. You can then edit your version in a codespace or download it and use it with your preferred source editor. If you prefer GitHub Desktop, simply clone the repository using the same link and open it directly in a source editor to start working.

## **2.3 GitLab** {#2.3-gitlab}

First, navigate to **“Groups"** in the sidebar navigation and create a new group by clicking the **“create group”** button. The website can get its own subdomain only if it is a website for a group. Name the new group. The group name also will be part of the url for your course. Once everything is done, click on the blue **“create group”** at the bottom of the page and your group is created.

After creating a new group, the next step is to create a new project in GitLab. To create a new project, navigate to the group you just created and click on the **“Create new project”** prompt. Please note that the name you choose for the project needs to match the web address. This depends on the setup of your GitLab instance. For example, for the GitLab instance at gitlab.gwdg.de, websites are served under _yoursite_.pages.gwdg.de. In this example, the name of your project would be yoursite.pages.gwdg.de. Once you finish the setup, click on the blue **“Create project”** button.

![](assets\img\readme\2.3gitlab.png)

Now it's time to configure some settings. For this, navigate to your project settings, and then expand the section **“Visibility, project features, permissions”**. Then, under **“Pages”** select **“Everyone”**, as seen here:

Once you successfully set the correct settings, it is time to dive deeper into the configuration section of your project.

### 2.3.1 Advanced Github-GitLab Sync {#2.3.1-advanced-github-gitlab-sync}

In this project setup, we manage the repository by forking it from the original "Millennial" repository on GitHub. To maintain a synchronized backup, we utilize a "push-only" version of the repository on GitLab. This means the GitLab repository is never directly modified—changes are exclusively pushed from the GitHub version.

To establish and maintain advanced synchronization between GitHub and GitLab, the first step is to examine the `.git/config` file. Below is an image of the file that illustrates the configuration setup:

![](<assets/img/readme/2.3.1(1).png>)

![](<assets/img/readme/2.3.1(2).png>)

For a better understanding of the file, please find a detailed explanation here:

#### **2.3.1.1 .git config** {#2.3.1.1-.git-config}

First of all, there are some **core settings** (line 1-7) which are explained in the following part.

- **`repositoryformatversion = 0`**: Specifies the repository format version (typically 0 for standard Git repositories).
- **`filemode = true`**: Git checks for changes in file permissions.
- **`bare = false`**: Indicates that this is not a bare repository (it contains a working directory).
- **`logallrefupdates = true`**: Enables logging of all reference updates.
- **`ignorecase = true`**: Git ignores case sensitivity (useful for case-insensitive file systems).
- **`precomposeunicode = true`**: Ensures Unicode compatibility, especially on macOS.

Next up are the **submodule settings** (line 9, 17-20):

- **`active =`** Indicates that submodules are activated for the current repository.
- **`url`**: URLs of the submodules linked to this repository.
- Submodules allow embedding external repositories as part of the main project. For example, `course-website-tools` and `reveal.js` are added as submodules.

Furthermore, we have the **remote settings** (line 11-12,24-32):

- **`url`**: The URL of the primary remote repository (`origin`).
- **`fetch`**: Specifies which branches are fetched from the remote.
- **`remote = origin`**: The branch `gh-pages` is synchronized with the `origin` remote.
- **`merge = refs/heads/gh-pages`**: Local changes are merged with the `gh-pages` branch on the remote.
- **`upstream`**: Another remote repository, often used to sync with the original source repository (e.g., for a fork).
- **`gitlab`**: A remote repository hosted on GitLab.
- **`lfs`**: Configures Git Large File Storage (LFS) for managing large files (e.g., media assets)

Once you have successfully configured the settings as shown in the example, your repository will be ready to push changes to GitLab. To verify that everything is working correctly, open a new terminal and execute the following command: **git push all**  
This command ensures that your changes are pushed to all configured remotes, including GitHub and GitLab. If the setup is correct, the push should complete without errors, and your changes will be mirrored to the GitLab repository as intended.

### **2.3.2 Enable pages and CI Pipelines** {#2.3.2-enable-pages-and-ci-pipelines}

After successfully completing the previous steps, the next step is to enable Pages for your project. This involves configuring the CI/CD pipeline to ensure that the deployment process functions correctly. Here's how to proceed:

**Enable CI/CD in Project Settings**:

- Navigate to the **Settings** section of your GitLab project.
- Under the **CI/CD** tab, enable the necessary options to activate continuous integration and deployment for your project.

![](<assets\img\readme\2.3.2(1).png>)

**Configure the `.gitlab-ci.yml` File**:

- While starting the configuration of pages, make sure to check the box “The application files are in the “public” folder. GitLab Pages publishes files in the public folder only. If needed, change your jobs to send output to this folder.” and enter the following for the image: **ruby:3.3.1**
- Ensure that your repository includes a properly configured `.gitlab-ci.yml` file. This file defines the pipeline stages and jobs necessary to build and deploy your project.
- You can find the **`.gitlab-ci.yml`** file in the root of the project directory. Simply copy the contents and paste it in the needed section, which will look like this:

![](<assets\img\readme\2.3.2(2).png>)

After finishing the Pages setup, it is time to check if the Pipeline is running as intended:

![](<assets\img\readme\2.3.2(3).png>)

To verify that the pipeline is running correctly, click on **"Check the Pipeline Status"** in your GitLab project. If everything is configured properly and running as intended, the pipeline should display a status similar to this:

![](<assets\img\readme\2.3.2(4).png>)

However, if nothing appears to be running yet, you may need to click on **"Retry"** or **"Start over"** in the pipeline interface to reinitialize the process. This typically resets the pipeline and gives it another attempt to execute the defined steps.

If the issue persists, revisit the configuration:

1. Double-check the `.gitlab-ci.yml` file for any errors or missing configurations.
2. Ensure that all necessary project settings (like enabling Pages and CI/CD) are correctly applied.
3. Verify that the required files and dependencies (e.g., `ruby:3.3.1`) are properly included.

Once these steps are corrected and the pipeline is restarted, everything should run as intended, successfully setting up your GitLab Pages deployment.

## **2.4 Directory Structure** {#2.4-directory-structure}

In this section, you will explore the key components of the GH-Pages directory.

└── 📁_data // Relevant for editing session posts, glossary,nav bar **(3.1, 3.6, 3.4)**.  
└── 📁_includes // Relevant to store reusable HTML snippets or other content that can  
be included in multiple layouts or pages.  
└── 📁_layouts // Relevant for configuring the content of existing and new pages and posts **(3.4, 3.5, 3.1).**  
└── 📁_plugins // Relevant for Reveal.js, ensures that HTML gets properly formatted.  
└── 📁_podcasts // **(3.7)** Metadata files for podcast episodes  
└── 📁_posts // Relevant for posts and slides for each session **(3.1, 3.2).**  
└── 📁_sass // Relevant for customizing the look of the site if you’re familiar with CSS/SCSS**.**  
└── 📁_site // HTML pages automatically generated by Jekyll for your site.  
└── 📁assets // Relevant for user multimedia (images, PDFs, podcast audio), as well as for plugin files (sidebar menu and reveal.js) **(3.2.1 ,3.7)**.  
└── 📁pages // Relevant for course-wide pages (rather than individual session posts) **(3.4).**  
└── \_config.yml // Relevant for the main configuration of the site.

You will see some additional files, some of which are necessary for Course Websites to function. Don’t delete or change these manually unless you know what you’re doing\!

# **3\. Configuration / Features** {#3.-configuration-/-features}

GH-Pages provides a range of features designed for innovative teaching. The following section will highlight the most important features and explain how to use them.

## **3.1 Posts** {#3.1-posts}

One of the key features of Course Website is the Post structure, which enables you to organize your page according to your course sessions. In this setup, posts function as your course sessions. When users navigate to the page, they will see the sessions listed in chronological order (provided the dates are set correctly), as shown here:

![](<assets\img\readme\3.1(1).png>)

Each page shown in the previous image represents a single post, which serves as a course session. To help illustrate this, here’s an example of a session post:

![](<assets\img\readme\3.1(2).png>)

To add a new post, follow these steps:

1. Add your session details to the `sessions.csv` file within the existing data structure. Ensure that you include at least the date (in the format YYYY-MM-DD) and session number.
2. Create a new .md file in the `_posts` folder, naming it using the following format: `YYYY-MM-DD-SESSIONNUMBER`.
3. Once the file is created, include the following in the front matter:

```---
layout: post // the post.html layout …
session: 1 // number of your session.
tags: \[1\] // the session number serves as a tag.
level: overview //
\---
```

If you want to add additional instructions, like to-dos for your students, simply place them under a heading such as `## To-Do` after the front matter (i.e., after the \--- ).

## **3.2 Slides / Reveal.JS** {#3.2-slides-/-reveal.js}

As indicated in the previously mentioned directory structure, each session post can have an assigned slide presentation, which can be accessed on the specific post page, as shown in the earlier section. The slides are powered by [Reveal.js](https://revealjs.com/), which is already integrated into GH-Pages. To add a new presentation to your post, start by creating a new markdown file in the `_posts` folder using the `YYYY-MM-DD-SESSIONNUMBER-slides` format (`-slides` follow the session number).

Once you've created the markdown file for the slides, follow these steps:

1. **Create your Front Matter**: In this example, the Front Matter includes parameters such as layout, title, author, session, tags, image, and parallaxBackgroundImage. You can copy these from below and change them to your needs.
2. **Write your presentation content**: Ensure that all content is written in Markdown. Markdown is easily convertible to HTML using various tools and libraries, making it ideal for static site generators like Jekyll, which convert Markdown files into HTML pages. Here are a couple important points to keep in mind (for more possibilities, see the Reveal.js documentation):
   - All slide content is in a single document. Begin a new slide by using a heading of level 1 or 2 (\# or \#\# in markdown).
   - The code {: .fragment} can be used on a new line directly after text portions you want to appear in stages in your presentation. (For images, put it directly after the image code without a line break.)
3. **Key considerations for Front Matter**:
   - **Layout**: Set this to "reveal" since it specifies that the presentation is based on reveal.js.
   - **Session**: Indicate the session the presentation is assigned to.
   - **Tags**: Include the session tag (e.g., "2" for session 2\) and "slides".
   - **ParallaxBackgroundImage**: Specify the background image for your presentation, typically stored in assets/img.

Here’s an example of a slides markdown file code:

```---

layout: reveal // this uses the reveal.js layout which is needed for the slides.

title: "1. Vorstellungen" // enter the title of your presentation.

author: "Nathan Gibson" // enter the author of the presentation

session: 1 // enter the session number your presentation is connected to.

tags: \[1,slides\]

image: interreligious-conversation.png // add an image for the preview.

parallaxBackgroundImage: 'assets/img/interreligious-conversation.png' //add a background picture for the slides.

\---

**\# Interkulturelle Kommunikationswege**

**\#\#\# in sich wandelnden religiösen Umfeldern**

**\#\#\# 1\. Vorstellungen**

**\#\# This is the header of the next slide**

**This is the content of the next slide**
```

By following these steps, you can easily add a new presentation to your post

### 3.2.1 Sidebar-Menu {#3.2.1-sidebar-menu}

In the slides, you can utilize a built-in sidebar menu based on the GitHub repository denehyg/reveal.js-menu. The menu layout is included in the reveal.html file, located in the \_layouts folder, starting at line 42\. To access the menu within the slides, click on the button located at the bottom-left corner of the screen, as shown in the image below:

![](<assets\img\readme\3.2.1(1).png>)

To better understand how the sidebar menu works, please refer to the image below:

![](<assets\img\readme\3.2.1(2).png>)

![](<assets\img\readme\3.2.1(3).png>)

Here you can jump to a particular slide or go to external links relevant to the session. To modify the external links (“custom collections”) or add a new one, go to line 144 in the reveal.html file. If you want to add another custom collection, structure it as follows:

```
{
 title: "(title)", // add your preferred title.
 icon: '\<i class="fa fa-external-link"\>', // add a fa-icon.
 content: "(Content)”, // add your content for the collection.

   },
```

Please note that there are several settings you can adjust for the sidebar menu, including an option to automatically include slide navigation within the sidebar. You can find these settings in the `reveal.html` file located in the `_layouts` folder, along with detailed instructions for each additional setting and how to configure them. See the Reveal.js documentation for more details.

## **3.3 Zotero / Bibliography integration** {#3.3-zotero-/-bibliography-integration}

A particularly useful feature, especially in academic settings, is the ability to integrate your Zotero bibliography. This allows you to directly link specific readings to individual sessions within your Zotero library.

1. Log into your Zotero account and create a “group” that you will use for your course. The group settings must allow anyone to view the group library. Copy the URL of the Zotero group library (including the number followed by the name of the library but nothing after this, e.g., [https://www.zotero.org/groups/5490829/24inter](https://www.zotero.org/groups/5490829/24inter)) and enter this in the base-urls \> zotero: section of the \_data/settings.yml file.
2. Add items to this Zotero group library. Make sure the URL field of each item points to a URL where the reading can be accessed.
3. Tag the items according to the session they will be used in. You can generate a list of Zotero tags automatically using the file \_data/sessions.xlsx, which you can copy into Zotero. The tags you use for specific sessions in your Zotero library should match the ones in the zotero-tag column of \_data/sessions.csv or in the zotero-tag front matter of your session post. This will create a link to the relevant items in “Further reading” for each session of your course.
4. [Install the Better BibTex plugin](https://retorque.re/zotero-better-bibtex/installation/index.html) for Zotero.
5. In the Zotero desktop app, right-click on the group library you created \> Export library … \> Better CSL YAML with Keep updated and Background Export \> Save in your Course Websites folder under \_data/zotero.yaml. This will make the metadata of your Zotero library available to your Course Websites site.

For each session for which you want to assign a reading, add the “Citation key” for that item from your Zotero library to the zotero-readings column of the \_data/sessions.csv file or to a zotero-readings front matter item for that session’s post. (Currently, only one reading per session is supported in the CSV file, so if you want to add multiple readings, use comma-separated citation keys in the zotero-readings front matter of a post.).

## **3.4 Pages** {#3.4-pages}

In GH-Pages, you can create new pages and add them to the navigation bar, like the previously mentioned Glossary page.

![](assets\img\readme\3.4.png)

In the following section, you'll learn how to create a new page and add it to the navigation bar menu. To begin, navigate to the “pages” folder (refer to section 2.3 for detailed instructions on locating this folder). Next, create a Markdown file with your desired page name. In the Front Matter of this Markdown file, be sure to include at least the following information:

```
\---
layout: glossary // choose the layout from the \_layouts folder or create a new.
title: Glossar // pick a desired title for your new page.
permalink: /glossary // choose a valid permalink for the page.
\---
```

After creating the Markdown file and editing the Front Matter, go to the `settings.yml` file located in the `_data` folder. In line 11, you'll find a list of all the pages currently included in the menu overview. To add your new page, enter the following within the menu section of `settings.yml`:

```
\- { name: "Glossar", url: "glossary" } // add the name as well as the permalink you created in the Front Matter of your new Markdown file here to make your page appear in the navigation bar.
```

If you want to remove a bar from the menu, simply delete the corresponding line in the menu section of `settings.yml`.

### 3.4.1 Redirects {#3.4.1-redirects}

In the navigation bar, some pages, such as Zotero, act as redirects to external or new pages to efficiently handle and manage redirections. The layout used for these redirects is located in the `_layouts` folder and is named `redirect.html`.

For pages like Zotero that require a redirect, you can define the redirection directly in the front matter. Here’s an example of how the front matter would look:

```
\---
layout: redirect
title: Zotero
permalink: /zotero
redirect: https://zotero.org
\---
```

## **3.5 HTML-Layouts** {#3.5-html-layouts}

This section will cover the previously mentioned HTML-Layouts which are needed to create new pages as well as new sessions and more. You can find the HTML-Layouts within the \_layouts folder. As we previously mentioned, the HTML-Layouts are needed for the Front Matter when you create a new file. In case we want to create a new session post, we use the post.html layout. In most cases, you will use the existing layouts provided; however, for special scenarios, you can create a custom layout if needed. The following example of the glossary page shows how a custom layout is structured.

```
\---
layout: default
\---

\<div class\="post-content"\>
 \<h1 class\="page-title"\>{{ page.title }}\</h1\>

\<div class\="featured-image"\>
 \<figure\>
 \<img src\="assets\\img\\glossary-ms-designer.jpeg" /\>
 \<figcaption\>
 Image: Generated by Microsoft Designer from the prompt. "Classic picture of a glossary."
 {{ page.image\_attribution | markdownify }}
 \</figcaption\>

\<article class\="content-with-margin"\> {{ content }}\</article\>
\</div\>
```

## **3.6 Glossary** {#3.6-glossary}

The built-in glossary page allows you to add specific glossary terms to various sessions and display all terms on a dedicated glossary page. To add new glossary terms, first navigate to glossary.csv. Enter your data in the following format:

```
term,definition,session,sessionname
```

In the glossary.csv file, "term" refers to the glossary term, while "definition" provides the explanation of the term. The "session" tag allows you to associate the glossary term with one or more sessions if desired. The "sessionname" tag is used on the separate glossary page to indicate in which session the term appears, provided it has been assigned to a session.

As previously explained, the `session` and `sessionname` tags are used to assign specific glossary terms to sessions and display them on the dedicated glossary page. For a clearer understanding, a detailed example of how this works is provided below:

```
Term 1,Definition of Term 1,\[1\],Session 1
```

As noted, both the `session` and `sessionname` tags are set to 1\. Assigning the `session` tag a value of 1 links the glossary term to the first session, which will appear as follows:

![](<assets\img\readme\3.6(1).png>)

As we can see, the glossary term is correctly assigned to the first session when we visit the session page. However, we also mentioned the `sessionname` tag, which is also set to 1, indicating it is linked to the first session. Earlier, we discussed the dedicated glossary page that displays all possible glossary entries on a single page. Here's how it looks in our example:

![](<assets\img\readme\3.6(2).png>)

In this example, the glossary term appears only in Session 1, making it the only session listed for this term. If a term is relevant to multiple sessions, you can assign several sessions to the `sessionname` tag.

## **3.7 Podcast** {#3.7-podcast}

Since Jekyll supports RSS, you can use GH-Pages to create a podcast. The following section will guide you through on how to use the podcast function.

### 3.7.1 Podcast-Page {#3.7.1-podcast-page}

In the `pages` folder, you'll find the dedicated `podcast` page, which serves as the central hub for displaying all entries from the `_podcast` folder. This page dynamically lists and organizes your podcast episodes for easy browsing.

If you'd like to customize the appearance or layout of the podcast page, navigate to the `_layouts` folder and modify the `podcast.html` file. This file controls the structure and design of the podcast page. Remember to save your changes and rebuild the site to apply the updates.

### 3.7.2 Podcast-Posts {#3.7.2-podcast-posts}

The `_podcasts` folder is where new podcast entries are created and managed. To add a new podcast entry, follow these steps:

1. **Create a New File**: In the `_podcasts` folder, create a new file and name it using the following format: `YY-MM-DD-EPISODENUMBER.md`.
2. **Structure the Front Matter**: Add the required metadata in the front matter of the file with the following details:
   - **Layout**: Set the layout to `"podcast"`.
   - **Title**: Provide a title for the episode.
   - **Episode Number**: Specify the episode number.
   - **Category**: Assign the entry to the `"podcast"` category.
   - **Short Description**: Write a brief description of the episode.
   - **Full Description**: Include a more detailed description of the content.
   - **Author**: Indicate the author or host of the episode.
   - **MP3**: Provide the URL to the episode’s audio file (MP3 format).
   - **Image**: Include the URL or path to the image you want displayed for the episode.

Once you've completed these steps, your new podcast entry will be ready for inclusion in the podcast RSS feed and displayed on the podcast page.

```---
layout: podcast
title: "Episode 1: The Great Journey of Jekyll-Podcasts"
episode: 1
categories: podcast
short_description: "A brief overview of our first episode."
description: "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat."
author: "Max Mustermann"
mp3: "https://audio.podigee-cdn.net/1455775-m-7a846c71ddf192fb2352b949bd4f2dca.mp3"
image: wool.jpg
\---
This is a test podcast episode.
```

### 3.7.3 Podcast.xml {#3.7.3-podcast.xml}

The `podcast.xml` file serves as a customizable RSS feed template for hosting and distributing podcast episodes. Designed with Jekyll, it dynamically generates RSS feeds that are fully compatible with major podcast directories, including Apple Podcasts and Spotify. In this setup, its primary role is to process and display the podcast entries from the “\_podcast”-folder.

## **4\. Further modifications** {#4.-further-modifications}

As we already pointed out in the beginning, GH-Pages is based on Jekyll, which can be extended in its functionality by implementing the so-called “gems”. In Jekyll, "gems" are Ruby libraries, also known as RubyGems, that extend the functionality of your Jekyll site. They can provide a wide range of features, from adding support for different markup languages to integrating with third-party services.

## **4.1 Ruby Gems** {#4.1-ruby-gems}

As mentioned in the introduction to this section, Ruby Gems are essential for modifying this Jekyll-based page. You can explore a full list of available Ruby Gems at [https://rubygems.org/gems](https://rubygems.org/gems). It's important to note that some gems may not be compatible with the latest version of Ruby, as certain Ruby Gems have not been updated recently.

## **4.2 GitHub** {#4.2-github}

For features like the previously mentioned sidebar menu, GitHub can be a valuable resource for finding modifications to enhance your Jekyll page. However, similar to Ruby Gems, some modifications you find on GitHub may not be compatible with the latest version of Ruby.
