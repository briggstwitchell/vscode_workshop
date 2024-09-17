---
title: What is Git?
layout: default
parent: Introduction
nav_order: 3
---

# What even is Git?
---

![git logo](../images/intro/git-icon.png)
{: .text-center}

Git is a __version control system__. It's a program that keeps track of a project and any changes that happen within that project's directories. 

Git was created by Linus Torvalds, the guy who wrote the Linux kernel. Linus made Git to help him develop software. He calls it "the dumb version control system".

---
# What does Git do?

---
### The Tale of Hansel and Git-el
<br>
!["hansel and gretel"](../resized/breadcrumbs.jpg)
{: .text-center}

Git keeps a record of all the files in your software project. 

Every time you decide to save the state of your project, Git takes a __snapshot__ of the way every file in the project looks at that moment.

You can think of each of these __snapshots__ as a __bread crumb__ you left on the trail of your software project. 

Git keeps track of all of your __bread crumbs__. This history of your project stays intact for the duration of your project, so you can go back to any prior state whenever you want.

Your bread crumb trail can have multiple branches, so that you can try out different ways to build your software without losing progress.

When used with a hosting service like GitHub, Git can help you collaborate with other software developers without getting in each others way.