---
layout: page
title: Lab 1 - GitHub Pages and Markdown
---
This is a footnotes test.[^1]
This is another footnotes test.[^note]

[^1]: This is note 1.
[^note]: This is "note" note.

## Acknowledgments
Much of this lab is borrowed from [Lab 1](https://f20idh.ryancordell.org/2020/09/10/Github/){:target="_blank"} and [Lab 2](https://f20idh.ryancordell.org/2020/09/16/Jekyll-and-GithubPages/){:target="_blank"} of Ryan Cordell's Intro to DH course (F20).

## Resources for Building Your Site in addition to This Page
Since our first two labs will be held remotely via Zoom, I will turn recording on when we move to the lab portion of our class meetings. After class, I will make the recordings of these lab sessions available via our class Google drive folder so that you can refer to them outside of class.

Additionally, Ryan Cordell created a screencast of the process of building a website using GitHub Pages for an undergrad course he taught a few years ago. You can find that video [here](https://www.youtube.com/watch?v=qiJETQz7Phs){:target="_blank"}. You may find this video useful if you work on building your site outside of class. You may also find portions of this [2014 tutorial by Barry Clark](https://www.smashingmagazine.com/2014/08/build-blog-jekyll-github-pages/){:target="_blank"} useful, though some things have changed in the intervening years.

## Why We Are Doing This
I am asking you to create and publish your own website using GitHub Pages and Markdown (and Jekyll, but Jekyll will remain under the hood for our purposes) for several reasons:

- It's free to host your website using GitHub Pages.
- Publishing a website this way provides a gentle introduction to GitHub, which many digital humanists use to store and share their work. In GitHub, you can store and share writing, code, and data all in one place. [GitHub also provides version control](https://ourcodingclub.github.io/tutorials/git/){:target="_blank"}: it saves each instance of your work so you can return to previous versions easily, it helps you to collaborate asynchronously with other people, and it allows you to fork various branches of the same repository so that you can explore new drafts or versions of code while keeping other versions stable. We won't be working with most of the version control features of GitHub in this course, but these features are the main reasons GitHub has become a popular platform for storing and sharing code and data.
- It also provides a gentle introduction to writing in Markdown, which is a lightweight standard for writing in plain text while encoding the structure of your document for later representation in a format like Word, PDF, or HTML. We'll talk more about writing in Markdown in class.
- Building a website using a static website generator like [Jekyll](https://jekyllrb.com/){:target="_blank"}, which is the generator you will use to transform your Markdown files into a website hosted on GitHub pages (this transformation will happen, for us, entirely on GitHub's end and so will remain invisible), conforms to principles outlined by the [DH minimal computing community](https://go-dh.github.io/mincomp/about/){:target="_blank"}. Websites built using static generators load more quickly and require less overhead than websites built using platforms like Wordpress. They are also more future-proof than websites built using platforms like Wordpress: because your website content will be stored mainly as plain text, you will be able to locally save and store, and, if needed, migrate this content more easily.

## What If I Already Have a Personal Website?
If you already have a GitHub pages personal website that you build using Markdown and Jekyll, you can use this site for this class if you would like. Just make sure your site's theme allows for blogging (if it doesn't, but if you'd like to stick with your current website/theme anyway, you can talk to me about how to post your work for this class to your site in ways that make sense for your theme). But even if you already have a GitHub pages site, you may wish to create a separate repository/website for your work in this class.

If you already have a personal website built using another platform or service (like Wordpress, for example), you will need to create a GitHub pages site for your work for this class.

## A Brief Discussion of Website Architecture
In class, I'll talk briefly about what it means to "host" a website, what it means to "generate" a website, and what website "content" is; how the websites we will be building in class are different from websites built using other popular free platforms, like Wordpress; and what [Jekyll](https://jekyllrb.com/){:target="_blank"} is.

## One: Tour of our course site repository
We will discuss our [course site GitHub repository](https://github.com/lcthomas/eng612s22/tree/gh-pages){:target="_blank"}. We'll talk about how I created this repository, its different branches, how the site content is organized, some GitHub vocabulary (such as "commit," "push," and "master"), and where Jekyll "is"/how Jekyll is working under the hood to generate the site.

## Two: Introduction to Markdown
Cordell's [Lab 1 -- Github and Markdown](https://f20idh.ryancordell.org/2020/09/10/Github/){:target="_blank"} includes a great description of Markdown and its affordances and limitations (see the "Composing in Markdown" section). If you're new to Markdown, I recommend you read that post before continuing on.

Markdown files are plain-text files that are *marked up* with simple textual encoding. You can then render these plain-text files in various formats for publishing, including Word, PDF, and, in our case, HTML. For example, check out the "raw" view for our course site [home page](https://raw.githubusercontent.com/lcthomas/eng612s22/gh-pages/index.md). See how, after the header (the part within three horizontal lines), the first line reads "\# Topics in DH: Humanities Data"? That hashtag is an example of Markdown; it's telling the website to render that line as a header (heading 1, to be precise). If you go look at the rendered version of [our course site home page](https://lindsaythomas.net/eng612s22/){:target="_blank"} (i.e., how it appears online), you will see that that line is formatted as a heading.

In class, we will use <https://stackedit.io> to experiment with some formatting in Markdown. We will cover how to format headers, how to make text bold and italic, how to create links, and how to make ordered and unordered lists. There is more you can do in Markdown; for additional reference you can consult:

- The [Markdown Wikipedia page](https://en.wikipedia.org/wiki/Markdown){:target="_blank"}, which includes a very handy chart of the syntax.
- [John Gruber’s introduction to Markdown](https://daringfireball.net/projects/markdown/syntax){:target="_blank"}. Gruber developed the Markdown standard.
- [This interactive Markdown tutorial](https://www.markdowntutorial.com/){:target="_blank"}, which will teach you the syntax in a few minutes.
- You can also view (and download, if you wish) the [Markdown versions of our class website pages](https://github.com/lcthomas/eng612s22/tree/gh-pages){:target="_blank"} or the [Markdown for this very lab](https://github.com/lcthomas/eng612s22/blob/gh-pages/labs/lab-1.md){:target="_blank"} if you’d like to compare what you see in your browser with the marked-up text that created it (click the `Raw` button to see the Markdown without GitHub’s styling).
- This is getting into the weeds a bit and we won't be focusing on this in this class, but just so you know for future reference: You can use Markdown for more than writing content for your website. For example, I use Markdown for most of my writing. I write pieces in my Markdown editor (I use Atom, see step nine for others), and I store references using [Zotero](https://www.zotero.org/){:target="_blank"}. Then, when I am ready to submit something, I use [pandoc](https://pandoc.org/){:target="_blank"}, which is a command-line utility for converting documents between various formats, to convert my Markdown file into a Word document or PDF (with citations and references formatted *automatically* as whatever style I need) for submission. Scott Selisker has written a detailed and useful [post](http://u.arizona.edu/~selisker/post/workflow/){:target="_blank"} about his plain-text academic writing workflow; I recommend starting there if you're interested (there is a somewhat significant learning curve, especially if you're not already familiar with Zotero, the command line, and a programming editor like Atom).

## Three: Sign up for a GitHub account
You may sign up for a [free Github account](https://github.com/signup){:target="-blank"} or, if you would like the option to create private repositories, apply for a free Pro account under [Github Education](https://education.github.com/){:target="_blank"} (select "Student Developer Pack").

## Four: Find a theme you like and fork it
All Jekyll themes should work with GitHub Pages, though some take more tweaking than others. Check out [this list of Jekyll themes on Github](https://github.com/topics/jekyll-theme?o=desc&s=stars){:target="_blank"}, sorted by how many people like them. Find one you like, but **make sure it’s a theme that supports blogging**. The easiest way to know is to see if there’s a folder titled `_posts` in the theme's repository. We can work during the semester to customize these themes, so it doesn’t need to be perfect: just good enough. When you click on a theme name in this list you’ll see its repository on GitHub. Most of these pages will include a link to a sample site, which will give you a sense of what your site would look like.

If you're new to this or just want to get this part over quickly, I recommend using [Beautiful Jekyll](https://github.com/daattali/beautiful-jekyll/tree/master){:target="_blank"} or [Jekyll TeXt Theme](https://github.com/kitian616/jekyll-TeXt-theme){:target="_blank"}. Our course site is built using [Poole](https://github.com/poole/poole){:target="_blank"} (if using Poole, you should fork the `gh-pages` branch).

Once you’ve found a theme you like, we will fork the repository. Don’t worry if that phrase sounds like nonsense: we’ll do it together and I’ll explain what it means. Note: Some themes (such as Poole) may include instructions to fork specific branches; otherwise, fork the "master" branch. If you are using Beautiful Jekyll or TeXt Theme, you can follow along with these instructions:
- Beautiful Jekyll: [Follow the steps under "The easy way (recommended)" on the repo's README.md file.](https://github.com/daattali/beautiful-jekyll/tree/master){:target="_blank"}
- TeXt Theme: Do **just** step 3 under "Common Method" on the [Quick Start page](https://tianqi.name/jekyll-TeXt-theme/docs/en/quick-start).

After forking, click on the "Settings" tab. **If you DO NOT already have a personal GitHub Pages website**, under "Repository name," change the name of your repository to `your-github-username.github.io` (for example, my GitHub account name is `lcthomas` so mine would be `lcthomas.github.io`). This tells GitHub to map this repo to this address (the standard GitHub pages address for every account). **If you DO already have a personal GitHub pages website**, this won't work; you should give this repository the name you want and map it as a subdomain to your existing personal site (if this doesn't make sense to you let me know).

In the future, if you would like to purchase a custom domain (such as mine: <https://lindsaythomas.net>), you can also map that domain to your GitHub pages site. See [this page for more information on mapping a custom domain to your GitHub pages site](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site){:target="_blank"}.

## Five: Review your site's structure
Once everyone has their own GitHub Pages repository, we will spend some time studying the structure of a Jekyll website together. I will show you where to find the files for static pages, blog posts, and basic configuration files.

## Six: Edit the _config.yml file
The `_config.yml` file includes all the basic configurations for a Jekyll website. We need to customize these for each of your individual sites. We will work through this together as well.

## Seven: Use the GitHub interface to edit and create a post
There are different ways to edit the files for your GitHub Pages website (and to create new ones). We're going to focus first on editing and creating these files from within the GitHub interface. I'll walk you through how to do this, and we will discuss post naming conventions, YAML headers, and where your site's blog posts are displayed.

Note: Your theme likely comes with at least one sample post. After we edit it and create a new post, you can delete the sample post(s) that came with your theme so that they don't display on your website.

## Eight: Use GitHub interface to edit/create a page
We will also talk about how to edit and/or create standalone pages for your website. This process is very similar to creating or editing posts, but the YAML header is slightly different and the pages appear on your website in a different way. We will also talk briefly about your site's navigation structure.

Note: If your theme comes with any sample pages, you can delete them after we edit and create our own page.

## Nine: Download GitHub Desktop and a Markdown application
So far, everything we've done to change your website, we've done *remotely*. This is because all of your website's files live on GitHub's servers right now; there is nothing stored locally on your own computer. The GitHub interface is functional, but I find it much easier to compose and edit files locally, on my own computer, and then push these files to my GitHub website repo. This also ensures that you have a local copy of everything on your website in case of some disaster.

To work with your website files locally, you're going to need to download 2 programs: [GitHub Desktop](https://desktop.github.com/){:target="_blank"}, and a Markdown app. GitHub Desktop provides an interface for commiting and pushing your local files to GitHub's servers, so that they show up on your website (you can also do this using the command line, but using GitHub Desktop is easier if you don't have any command line experience). The Markdown app you choose will be a program designed for editing and creating Markdown files that can understand Markdown syntax.

First, download and install [GitHub Desktop](https://desktop.github.com/){:target="_blank"}, but don't configure anything yet.

Second, select a free Markdown application to use to edit and create Markdown files locally and download and install it. Technically, you can use any plain-text editor to edit and create Markdown files (for instance, Windows machines ship with Notepad and Macs with TextEdit; I use [BBEdit](https://www.barebones.com/products/bbedit/){:target="_blank"} as my plain-text editor of choice). However, you can also download a Markdown-specific app for more flexibility and customization, such as the following:

- [Macdown](https://macdown.uranusjr.com/){:target="_blank"} (Mac)
- [Mou](http://25.io/mou/){:target="_blank"} (Mac)
- [Markdownpad](http://markdownpad.com/){:target="_blank"} (Windows XP-8)
- [Ghostwriter](https://wereturtle.github.io/ghostwriter/) (Windows 10 & Linux)
- [Remarkable](https://remarkableapp.github.io/){:target="_blank"} (Linux)
- a bit more complicated to get started with, but [Atom](https://atom.io/){:target="_blank"} is more full-featured than some of those above (I use Atom) (Mac, Windows, Linux)

## Ten: Clone your website repository to your local machine using GitHub Desktop
Now you are going to copy the files in your website repository to your own computer. [This page by GitHub](https://docs.github.com/en/desktop/contributing-and-collaborating-using-github-desktop/adding-and-cloning-repositories/cloning-a-repository-from-github-to-github-desktop){:target="_blank"} takes you through how to do it, and I will also walk through it in class.

## Eleven: Edit a page on your machine, commit, and push to GitHub using GitHub Desktop
Now your website files exist on your computer as well as on GitHub's servers. This means you can edit and create files locally and push them to GitHub. Open up the sample page we created earlier on your computer, using the Markdown application you downloaded and installed. Make a small but noticeable change. Then, open up GitHub Desktop and confirm that it lists the name of your website repository under "Current Repository" in the top left and the correct branch under "Current Branch" (for most of you, this will likely be the "master" branch).

The name of the file you edited should show up under "Changes," and the changes should display in the right panel. Make sure that file is selected. On the bottom left, where it says "Summary," you can write a brief commit message, then press "Commit to \[name of branch here\]". Finally, up toward the top of GitHub Desktop, you will see a tab that is now named "Push origin." Click that tab to push your changes to GitHub's servers. Within a few minutes, your changes should display on your website.

## Lab Notebook Entry and Statement of Goals
Due:
- By class on Wed, Feb 2

After completing the above steps, you are ready to start publishing posts to your website. First, make sure to email me your website address as well as the link to its attendant repository on GitHub. If you are using a GitHub Pro account and have made your repository private, please make sure you have shared it with me (I am [lcthomas](https://github.com/lcthomas){:target="_blank"} on GitHub). If your repository is public, please let me know if you give me permission to post your website address in a document in our class Google drive folder so that other members of the class may read your posts, as well (note: because this document will only be available via our shared Google drive folder, people outside of this class will not have access to this list). My hope is that sharing your posts with your colleagues will foster community, not competition, and that it will help to build a sense that the writing you do in this class can find an audience beyond me.

Next, you will create your first lab notebook entry. Make sure to format the filename as I describe at the bottom of the [lab notebook assignment page](https://lindsaythomas.net/eng612s22/lab-notebook/){:target="_blank"}. In this lab notebook entry, you should include the following 2 things:

1. A description of any points in the above process that were confusing, difficult, frustrating, etc and/or any parts you weren't able to complete, as well as a description of how you overcame or worked around these challenges.
2. A statement and brief description of your goals for this class for the semester. These goals can range from the technical to the conceptual/intellectual, and they can concern readings, in-class discussion, assignments, and/or your general growth as a scholar and a teacher. What do you want to learn, do, discover, feel, know, etc by the end of this course? There is no specific number of goals you should have, but they should be thoughtful, specific, and accomplishable.

Unlike your other lab notebook entries, you do not need to cite any readings from class in this notebook entry. There is no specific length requirement, but your entry should be full and thoughtful.
