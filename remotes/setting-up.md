---
title: setting up a remote
layout: default
parent: Remotes and Github
nav_order: 1
---

# Setting up our remote

---

In this section, we will be taking our web page and creating a remote tracking repository for it on GitHub.

Setting up remote tracking for your repository has many benefits:
* your work is backed up to the cloud
* you can maintain the repo from multiple machines
* other developers can look at your code
* you can grant permission for other developers to work on your code with you

Go to [GitHub](https://github.com/) and log in to your account.

Click on your profile icon in the upper right hand corner and choose the "Your repositories" option.

![step1](../images/remote/remote-s1.png)

In order to make this the landing page for your github account, you must name the repository "\<your username\>.github.io". 

If you'd rather not, just choose another name.

![step2](../images/remote/step-2.png)

All of the other defaults for the repo should be just fine. Scroll to the bottom of the page and click "Create Repository"

![step3](../images/remote/step-3.png)

Next, we need to choose an authentication method. For this demonstration, we will use HTTPS. On the page that pops up after creating the repo, choose HTTPS, and copy the link.

![step4](../images/remote/step-4.png)

Now go to your command line in your repository and type:

```bash
git remote add origin [URL]
```

Paste the link after the command. In the terminal, you will need to press Ctrl+Shift+V to paste.

---

Now we need to create an access token. Go to the dropdown menu in the upper right, and choose "Settings".

![step5](../images/remote/step-5.png)

At the very bottom of the left hand menu, choose "Developer settings":

![step6](../images/remote/step-6.png)

From the "Personal access tokens" dropdown choose "Tokens (classic)", and on the right hand "Generate new token (classic)"

![step7](../images/remote/step-7.png)

You must include a note. Choose an expiration date (I chose no expiration), and set the scope to repo.

![step8](../images/remote/step-8.png)

Now scroll to the bottom and click "Generate token":

![step9](../images/remote/step-9.png)

Finally! Copy your token to your clipboard. Make sure you do this. If you leave this page without copying the token you will have to start all over.

> If you are planning to push and pull from GitHub a lot, you should set up SSH access
> 
> SSH is beyond the scope of this workshop, but you can learn more [here](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)
{: .note}
---
A brief aside on `git remote add origin [URL]`:
* When we execute this, we're setting `origin` is the alias for the URL of the remote copy of our local repo
* This command modifies the config file in my .git hidden folder, specifying what `origin` is pointing to
* For the curious, execute `cat .git/config` and see for yourself
