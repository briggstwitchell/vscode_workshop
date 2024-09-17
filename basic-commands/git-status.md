---
title: git status
layout: default
parent: Basic Commands
nav_order: 2
---

# Git status
---

Anytime we want to see what's going on with git, we can run this command:

```bash
git status
```

![status empty](../images/status/stat-empty.png)
{: .terminal }

Git status is a very handy command. It tells us:
* where we are - right now, we're on the main branch
* what we've done - we haven't committed anything yet
* what we can do - we can add files to start tracking them

>Any time you're going to start issuing commands to Git, it's a good idea to run ```git status``` first. 
> 
> It's a passive command, it doesn't change anything about your directory or repository. Running git status never hurts!
{: .pro-tip}

***

When we ran Git init, Git started watching for files being created in that directory.

I'm going to create a README file for my website. 

README.md:
```
# Personal Website
```

Once I've created it, if I run ```git status```, I get the following output:

![status needs add](../images/status/stat-need-add.png)
{: .terminal }

---

Now git tells us we have an untracked file. 

What does this mean? 

Git only tracks files that we tell it to keep track of. We've started our project by adding the README file, but we haven't told Git to start watching it for changes yet. 

As far as git is concerned, this is still an empty directory. This is one quirk of git, it ignores anything in our folder that we don't specifically tell it about. Until we use our next commmand...

---
> ## Exercise
> - [ ] run ```git status``` in your project directory
> - [ ] create a README.md file in your project directory
> - [ ] run ```git status``` again and look at the output
{: .exercise}