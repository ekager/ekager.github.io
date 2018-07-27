---
layout: post
title:  "How to Make A Website And Blog in 20 Minutes"
date:   2018-07-26 18:59:05 -0700
categories: writing
---

Do you want a personal website?  :computer:

Want it to be a nice looking static site?  :sparkles:

Maybe with blog capabilities?  :pencil:

Need it to be free and easy?  :dollar:

You came to the right place!

## Let's get started!
### What you'll need!
* 20 Minutes
* A Mac
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
[Ruby](https://www.ruby-lang.org/en/downloads/) is a programming language we need. You probably already have this! Type into your command line `ruby -v` (and press Enter) to see which version of Ruby you have. Anything higher than 2.1 will work! If you need or want to update, it's easiest to do that through Homebrew.

#### Gem
Gem is Ruby's command line tool for package managing, which lets you easily install Ruby libraries and programs (referred to as Gems).

### Homebrew :beer:
[Homebrew](https://brew.sh/) is package management software that allows you to easily install software on Mac via the command line. Get it quickly and easily by typing:
 `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"` in your command line.

To update versions of all of your Homebrew installed packages, you just type `brew upgrade` and then `brew cleanup` to remove the older files.

### Jekyll
Good job installing everything so far!

Now we're going to get [Jekyll](https://jekyllrb.com/) and [Bundler](https://bundler.io/). Jekyll is the static site generator written in Ruby and Bundler manages Gems. Just type `gem install bundler jekyll` in your command line to get both.

Now we can actually create your website! In one command we create a basic empty site in the current directory with all the files you need. Are you ready?

`jekyll new your-awesome-site`

Just replace `your-awesome-site` with whatever you want the project folder to be named.

You now have a website! It may not seem like it, so let's prove it.

Use `cd your-awesome-site` to enter the project's folder (You'll see something like `(MacBook-Pro:your-awesome-site YourName$`), and then run `bundle exec jekyll serve` to run your site. It will output something like:
```
Server address: http://127.0.0.1:4000/
```
Copy that address or just go to http://localhost:4000/ to see your site running locally!

Now let's put it on the world wide web!

## Git
[Git](https://git-scm.com/) is version control software that helps you keep track of changes in a project. To get it, run `brew install git` in the command line.
Now to start using version control for your project, make sure you're in the `your-awesome-site` directory, and run `git init`.

Congrats you're now using version control!

## GitHub :octocat:
[GitHub](https://github.com/) is an online service for hosting code that uses version control. Conveniently, it also gives every member a free site, called [GitHub Pages](https://pages.github.com/).

If you don't have an account it's free to sign up and if you're a student make sure to sign up for a [Student account](https://education.github.com/pack) with lots of free goodies!

Following the pages tutorial, [create a repository](https://github.com/new) named username.github.io, where username is *your* username (or organization name) on GitHub. So my repository is named `ekager.github.io`. **Make sure it matches your username, or it won't work.**

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


** A note on git add: **

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

Go to the text editor, and open your project folder. You should see a file named `_config.yml`. Go through and change the info to be about you.

### Themes

There are tons of free Jekyll themes out there, some more complicated than others. For the simplest themes (like the [one I used for example](https://broccolini.net/swiss/about/)). You just have to add a line to your Gemfile like `gem "jekyll-swiss"` and then edit the `theme` in `config.yml`, in my case `theme: jekyll-swiss`. The theme I use also had a `theme_color` that I could edit, which I quickly did to `theme_color: blue`. Whenever you add a new gem, you'll have to run `bundle` in the command line to install the new gems before previewing it.

### Write a blog post
Since you did the Jekyll quick start, you should see a post already there that you can modify and copy to create new posts!

It is easy to use the Markdown language to format posts. According to Wikipedia:
~~~~
Markdown is a lightweight markup language with plain text formatting syntax. It is designed so that it can be converted to HTML and many other formats using a tool by the same name
~~~~

[Learn more about Markdown syntax!](https://guides.github.com/features/mastering-markdown/)

To make a new post from scratch, all you have to do is add a new file to the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext`, where ext is the extension of the file (like `.markdown`) and the date is not in the future or it won't work. The post file has to include the necessary "front matter" which is like a header for each file.

Example:
```
---
layout: post
title:  "How to Make A Website With Blog in 20 Minutes"
date:   2018-07-26 18:59:05 -0700
categories: writing
---
```

Fun fact: when writing in Markdown and using Atom, you can type `Ctrl+Shift+M` to preview your post formatted!

### Link Your Own Domain
Want to use your own domain? No problem! The exact instructions will depend on where you buy your domain name.

Generally, you'll have to buy a domain name and then hook up the domain name to point to your free Github address, and then tell you GitHub repo with a created CNAME file. A [great tutorial with photos is here](https://hackernoon.com/custom-domain-on-github-pages-tutorial-using-namecheap-7112bf2b8882).

## Finally
You created a great looking static website with blog capabilities, congratulations! :tada:

### Final Thoughts
You don't *have* to use the text editor at all to continue to write on your blog, you can use the Github UI to add or edit posts. If you use both, you'll need to remember to keep your GitHub repo in sync with your local files. Pull down changes from the GitHub repo by running `git pull origin master` before editing files locally so you don't lose changes, and remember to push any changes so you can see them with the 3 push steps we talked about above.

### Thanks
Thanks to my siblings for testing and editing this tutorial. Without them, this post would have way more exclamation points.