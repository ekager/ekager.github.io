---
layout: post
title:  "How to Make A Website With Blog in 20 Minutes"
date:   2018-07-26 18:59:05 -0700
categories: writing
---

Do you want a personal website?

Want it to be a nice looking static site?

Maybe with blog capabilities?

Need it to be free and easy?

You came to the right place!

## Let's get started!
### What you'll need!
* 20 Minutes
* A little familiarity with the command line would be helpful but not absolutely necessary!

### First we're going to need to download some things
* Text editor
* Homebrew
* Ruby
* Jekyll
* Git + GitHub

### Text Editor
Let's get you a text editor so that you can view, edit, and add files. I recommend [Atom](https://atom.io/). Download through the link there. Woohoo you already made it through Step 1!

### Command Line
If you know how to find your command line, then skip this step!
To find your command line on Mac, go to Spotlight search and open "Terminal".

[Here's](https://www.codecademy.com/learn/learn-the-command-line) a tutorial on the command line if you're interested in learning more, but I'll provide all the commands you need in this tutorial.

The main thing you need to know for this tutorial is when I say "type a command into the command line" you just need to copy and paste it and press enter for it to run.

The `cd` command is also known as chdir (change directory), is a command-line command used to change the current working directory. This just basically means you can enter and exit folders like in Finder just on the command line!

If you get lost in your directories, you can just run `cd` at any time to reset your command line adventures. You can also kill any process with `Ctrl + C`.

The `ls` command lists the files and folders in the current directory.

For example if my file system was like: `/Desktop/ImportantStuff/importantfile.txt` I could `cd Desktop` to get into my Desktop folder. `cd ImportantStuff` to get into the ImportantStuff folder and then `ls` to see the files in ImportantStuff.

### Ruby
[Ruby](https://www.ruby-lang.org/en/downloads/) is a programming language we need. You may already have this! Wouldn't that be easy! Type into your command line `ruby -v` (and press Enter) to see which version of Ruby you have. Anything higher than 2.1 should be fine. If you need or want to update, it's easiest to do that through Homebrew.

### Homebrew
[Homebrew](https://brew.sh/) is package management software that allows you to easily install software on Mac via the command line. Get it quickly and easily by typing `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"` in your command line.

Then, quickly install a new version of Ruby by typing `brew install ruby`.

In the future it is so easy to update, you just type `brew upgrade` and then `brew cleanup` to remove the older files.

### Jekyll
Good job installing everything so far! Now we're going to get [Jekyll](https://jekyllrb.com/), which drives the static site creation. Just type `gem install bundler jekyll` in your command line to get it!

Woohoo now we can actually create your website! In one command we create a basic empty site with all the files you need! Are you ready?

`jekyll new your-awesome-site`

And just replace `your-awesome-site` with whatever you want the project folder to be named!

Woohoo! You have a website! It may not seem like it yet, so let's prove it.

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

## GitHub
[GitHub](https://github.com/) is an online service for hosting code that uses version control. Conveniently, it also gives every member a free site, called [GitHub Pages](https://pages.github.com/).

If you don't have an account it's free to sign up and if you're a student make sure to sign up for a [Student account](https://education.github.com/pack) with lots of free goodies!

Following the pages tutorial, [create a repository](https://github.com/new) named username.github.io, where username is your username (or organization name) on GitHub. So my repository is `ekager.github.io`. Make sure it matches your username, or it won't work!

## Let's get your site up there
Good job setting up Git and GitHub!

In your directory, you're going to want to connect the site that's running locally to GitHub so it can host it for everyone else to see!
Make sure you're in your project directory, and then run `git remote add origin https://github.com/username/username.github.io`. This connects your created repository with your new project!

The repository is still looking pretty empty though, so let's send the new files to the repository.

Three steps!
1. `git add .` to add every file you just created to the commit.
2. Then run `git commit -m "Initial Commit"`. The `-m` is for message.
3. Lastly run `git push -u origin master` to get push your new website files to GitHub!

If you refresh your https://github.com/<username>.github.io you should see your new site, and going to <username>.github.io should now work!

Now when you edit files or add posts, you'll just have to run steps 1-3 again to update the GitHub repository!

Congrats you have a website!! Now let's make it yours!

## Make it Yours
Great job with all the set up! Let's explore how to make the site about you!
There's a ton to customize, but I'll go into a few ways to make it yours quickly!

### Customize

Go to the text editor, and open your project folder. You should see a file named `_config.yml`. Go through and change the info to be about you!

### Themes

There are tons of free Jekyll themes out there, some more complicated than others. For the simplest themes (like the [one I used for example](https://broccolini.net/swiss/about/)). You just have to add a line to your Gemfile like `gem "jekyll-swiss"` and then edit the `theme` in `config.yml`, in my case `theme: jekyll-swiss`. The theme I use also had a `theme_color` that I could edit, which I quickly did to `theme_color: magenta`. Whenever you add a new gem, you'll have to run `bundle` in the command line to install the new gems before previewing it.

### How to write a blog post
Since you did the Jekyll quick start, you should see a post already there that you can modify and copy to create new posts!

I (and many people) are using the Markdown language to format posts. According to Wikipedia:
~~~~
Markdown is a lightweight markup language with plain text formatting syntax. It is designed so that it can be converted to HTML and many other formats using a tool by the same name
~~~~

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
Don't want to have your site be .github.io? No problem, but it'll cost you. Not a lot though don't worry!

The exact instructions will depend on where you buy your domain name.

Generally, you'll have to buy a domain name and then hook up the domain name to point to your free Github address, and then tell you GitHub repo with a created CNAME file. A [great tutorial with photos is here](https://hackernoon.com/custom-domain-on-github-pages-tutorial-using-namecheap-7112bf2b8882).

## Finally
You created a great looking website with blog capabilities! Congratulations!

### Final Thoughts
You don't *have* to use the text editor at all to continue to write on your blog, you can use the Github UI to add or edit posts. If you use both, you'll need to remember to keep your GitHub repo in sync with your local files. Pull down changes from the GitHub repo by running `git pull origin master` before editing files locally so you don't lose changes, and remember to push any changes so you can see them with the 3 push steps we talked about above!
