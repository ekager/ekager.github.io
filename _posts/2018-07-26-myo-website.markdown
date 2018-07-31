---
layout: post
title:  "How to Make A Free Website And Blog in 20 Minutes Or Less"
date:   2018-07-26 18:59:05 -0700
categories: writing
---

#### Do you want a personal website?  :computer:

#### Want it to be a nice looking static site?  :sparkles:

#### Maybe with blog capabilities?  :pencil:

#### Need it to be free and easy?  :dollar:

#### You came to the right place!

### Disclaimer
I should clarify that there are actually quicker ways to make a blog with Jekyll, namely forking someone else's blog or template which there are [plenty of on GitHub](https://github.com/barryclark/jekyll-now). But if you're curious about the entire process from scratch, being able to preview locally, version control, and customizing, stay tuned!

## Let's get started!
### What you'll need!
* 20 Minutes
* A computer (My exact experiences were with macOS, but should work with slight modification for another OS)
* A little familiarity with the command line would be helpful but not absolutely necessary!

### First we're going to need to set up some things
* Text editor
* Homebrew
* Ruby + Gem
* Jekyll + Bundler
* Git + GitHub

### Text Editor
Let's get you a text editor so that you can view, edit, and add files. I recommend [Atom](https://atom.io/), and you can download it through that link.

### Command Line
If you know how to find your command line, then skip this step!
To find your command line on Mac, go to Spotlight search and open "Terminal".

[Here's a tutorial on the command line](https://www.codecademy.com/learn/learn-the-command-line) if you're interested in learning more, but I'll provide all the commands you need in this tutorial.

The main thing you need to know for this tutorial is when I say "type a command into the command line" you just need to copy and paste it and press enter for it to run.

The `cd` command, also known as chdir (change directory), is a command line command used to change the current working directory. This basically means you can enter folders like in Finder, just on the command line.

The `ls` command lists the files and folders in the current directory.

For example if my file system was like: `~/ImportantStuff/importantfile.txt`, I could `cd ImportantStuff` to get into the ImportantStuff folder and then run `ls` to see all the files in ImportantStuff.

If you get lost in your directories, you can just run `cd` at any time to go to your home directory. `~` represents your home directory. Your home directory is the directory that you're in after logging into the system. You're probably familiar with this as the place where your "Documents", "Downloads", and "Pictures" folders reside.

You can also kill a process currently running on the command line with `Ctrl + C`.

### Ruby :gem:
[Ruby](https://www.ruby-lang.org/en/downloads/) is a programming language we need. You probably already have this! Type into your command line `ruby -v` (and press Enter) to see which version of Ruby you have. Anything higher than 2.1 will work! If you don't have it, you can install it through their website. If you need or want to update, it's easiest to do that through Homebrew.

#### Gem
Gem is Ruby's command line tool for package managing, which lets you easily install Ruby libraries and programs (referred to as Gems).

### Homebrew :beer:
[Homebrew](https://brew.sh/) is package management software that allows you to easily install software on Mac via the command line. Get it quickly and easily by typing:
 `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"` in your command line.

To update versions of all of your Homebrew installed packages, you just type `brew upgrade` and then `brew cleanup` to remove the older files.

### Jekyll
Now we're going to get [Jekyll](https://jekyllrb.com/) and [Bundler](https://bundler.io/). Jekyll is the static site generator written in Ruby and Bundler manages Gems. Just type `gem install bundler jekyll` in your command line to get both.

Now we actually have everything we need to create your website! In one command we can create a basic site in the current directory with all the files you need. Are you ready?

`jekyll new your-awesome-site`

Just replace `your-awesome-site` with whatever you want the project folder to be named.

You now have a website! It may not seem like it, so let's prove it.

Use `cd your-awesome-site` to enter the project's folder (You'll see something like `(MacBook-Pro:your-awesome-site YourName$`), and then run `bundle exec jekyll serve` to run your site. It will output something like:
```
Server address: http://127.0.0.1:4000/
```
Copy that address or just go to [http://localhost:4000/](http://localhost:4000/) to see your site running locally!

Now let's put it on the world wide web!

## Git
[Git](https://git-scm.com/) is version control software that helps you keep track of changes in a project. If you have Homebrew, run `brew install git` in the command line to get it.
Now to start using version control for your project, make sure you're in the `your-awesome-site` directory, and run `git init`.

Congrats you're now using version control!

## GitHub :octocat:
[GitHub](https://github.com/) is an online service for hosting code that uses version control. Conveniently, it also gives every member a free site, called [GitHub Pages](https://pages.github.com/).

If you don't have an account it's free to sign up and if you're a student make sure to sign up for a [Student account](https://education.github.com/pack) with lots of free goodies!

Following the pages tutorial, [create a repository](https://github.com/new) named `username.github.io`, where username is *your* username (or organization name) on GitHub. So my repository is named `ekager.github.io`. **Make sure it matches your username, or it won't work.**

### Let's get your site up there
Good job setting up Git and GitHub!

In your directory, you're going to want to connect the site that's running locally to GitHub so it can host it for everyone else to see!
Make sure you're in your project directory, and then run `git remote add origin https://github.com/username/username.github.io`. This connects your created repository with your new project.

The repository is still looking pretty empty though, so let's send the new files to the repository.

#### Three steps to push your changes to your repository
Make sure you're in the project directory and then execute these three commands.
1. `git add .` to tell git what *added* files in the working directory you want to track changes of.
2. Then run `git commit -m "Initial Commit"`. A commit marks the tracked files as done being changed (for now). The `-m` is for adding your commit message.
3. Lastly run `git push -u origin master` to push your new website files from local to remote (GitHub).


**A note on git add:**

* `git add -A` - track All files
* `git add .` - track new and modified, without deleted
* `git add -u` - track modified and deleted, without new

To check which files you're about to commit, run `git status` before committing.

If you refresh your repository `https://github.com/<your-username>/<your-username>.github.io` you should see your new site, and loading `<username>.github.io` should show your site.

Now when you edit files or add posts, you'll just have to run steps 1-3 again to update the GitHub repository.

Congrats you have a website! Now let's make it yours.

## Make it Yours
There's a ton to customize, but I'll go into a few quick and easy ways.

### Customize

Go to the text editor, and open your project folder. You should see a file named `_config.yml`. Go through and change the info to be about your new site.

### Themes

First let's go to your Gemfile and remove `gem jekyll` and uncomment or add `gem "github-pages", group: :jekyll_plugins`. Run `bundle update github-pages` to update the new Gem. This will let us preview the themes locally!

To activate one of the [officially supported themes](https://pages.github.com/themes/), add `theme:` followed by the name of the theme in your `_config.yml` (as shown in the README in the theme's source repository).

To activate any other unofficial open source Jekyll theme hosted on GitHub, add `remote_theme: <theme-creators-github-username>/<theme-repo>` (as shown in the README or other documentation in the theme's source repository) to `_config.yml`.

There are [tons of free Jekyll themes out there](https://github.com/topics/jekyll-theme), some more complicated than others. For the simplest themes (like the [one I used for example](https://broccolini.net/swiss/about/)), you just have to edit the theme in `config.yml`. There may be more options to customize, so read the theme's documentation. For example, the theme I use also had a `theme_color` that I could edit, which I set to `theme_color: magenta` in `_config.yml`.

I recommend following the documentation of the theme you choose to use for the best instructions. [Read more about adding a theme.](https://help.github.com/articles/adding-a-jekyll-theme-to-your-github-pages-site/)

#### Overriding theme elements

Find a theme you like but want to override some elements? To override the default structure and style of the theme, create the concerned directory at the root of your site, copy the file you wish to customize to that directory, and then edit the file. For example, to override the `_includes/head.html` file to specify a custom style path, create an `_includes directory`, copy `_includes/head.html` from the theme's gem folder to `<yoursite>/_includes` and start editing that file. When building your site, the files that you have edited and included will override the original theme files. See [minima theme customization instructions](https://github.com/jekyll/minima#customization) for more information.


### Write a blog post
Since you did the Jekyll quick start, you should see a post already there that you can modify and copy to create new posts!

It is easy to use the Markdown language to format posts. According to Wikipedia:
~~~~
Markdown is a lightweight markup language with plain text formatting syntax. It is designed so that it can be converted to HTML and many other formats using a tool by the same name
~~~~

[Learn more about Markdown syntax!](https://guides.github.com/features/mastering-markdown/)

To make a new post from scratch, all you have to do is add a new file to the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext`, where ext is the extension of the file (like `.markdown`) and the date is not in the future. The post file also has to include the necessary "front matter" which is like a header for each file.

Example:
```
---
layout: post
title:  "How to Make A Website With Blog in 20 Minutes"
date:   2018-07-26 18:59:05 -0700
categories: writing
---
```

**Fun fact: when writing in Markdown and using Atom, you can type `Ctrl+Shift+M` to preview your post formatted!**

### Link Your Own Domain
Want to use your own domain? No problem! The exact instructions will depend on where you buy your domain name.

Generally, you'll have to buy a domain name and then hook up the domain name to point to your free Github address, and then tell your GitHub repo with a created CNAME file. A [great tutorial with photos is here](https://hackernoon.com/custom-domain-on-github-pages-tutorial-using-namecheap-7112bf2b8882).

### Get a Favicon
A favicon is the icon associated with your website in the URL bar or in a bookmarks list.
First you'll need the favicon. I used this [favicon generator](https://favicon.io/) to create mine with text but you can also use a logo image you already have! Once you have the `favicon.ico` file, add it to the root of your project (you can drag and drop in finder or your text editor). Then you'll need to add `<link rel="shortcut icon" type="image/x-icon" href="favicon.ico">` to the `head` of your `index.html` file. You may have to do an override to this file as mentioned above.

## Finally
You created a great looking static website with blog capabilities, congratulations! :tada:

### Final Thoughts
You don't *have* to use the text editor at all to continue to write on your blog, you can use the Github UI to add or edit posts. If you use both, or edit on multiple computers, you'll need to remember to keep your GitHub repo in sync with your local files. Pull down changes from the GitHub repo by running `git pull origin master` before editing files locally so you don't lose changes, and remember to push any changes so you can see them with the 3 push steps we talked about above.

### Thanks
Thanks to my siblings for testing and editing this tutorial. Without them, this post would have way more exclamation points.
