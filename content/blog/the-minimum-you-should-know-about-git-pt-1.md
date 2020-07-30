---
author: Gabriel Bussolo
date: "2018-11-21"
title: The minimum you should know about git (pt. 1)
tags: 
    - git
    - beginner
---
Hey guys. 

So, for my first post, I want to talk with you about git control version. I know many people don't know what is git, The most people and friends are from college, I hope that help you to understand what is "git" and its purpose. 

Git, it's a distributed version control system. That's okay, but what this means, right? This means what git take care of the state of your files. It tracks any change in your crawled archive.

(I will consider you have the git installed in your pc. If you don't have please follow <a href="https://git-scm.com/downloads" markdown="1" target="_blank">this steps</a>)

So let's see how it works in practice.

Let's say you have a *hello_git.txt*:
![terminal](../../post-images/the-minimum-you-should-know-about-git-pt-1/cool-file.png)

And, of course, you want to track it. What you should do is open your terminal and navigate until the folder of your archive and type ```git init .``` like this:
![terminal](../../post-images/the-minimum-you-should-know-about-git-pt-1/git-init.png) 

With this we start a repository in this folder, It means that **git** is looking at our folder now, but it not tracking our files yet. If we type ```git status```  we have something interesting. 
Look:
![terminal](../../post-images/the-minimum-you-should-know-about-git-pt-1/git-status.png)

The git warning us, "hey man I not tracking your file changes" so we can ask to git take care our file typing ```git add hello_git.txt```. Now if we run ```git status``` again we will see this:
![terminal](../../post-images/the-minimum-you-should-know-about-git-pt-1/git-add.png)

If we want git to take care of everything in our folder, we could have type  ```git add .``` (witch the dot).

So now git is watching our file, we can register this moment with a commit typing ```git commit -m 'my first commit'```, this command register the state of our file with a message. Now our ```git status``` was changed and we can see our commit registered typing ```git log```.
![terminal](../../post-images/the-minimum-you-should-know-about-git-pt-1/git-commit.png)
Congrats for your first commit \o/.

Okay, but what this means? This means we have a register in the time of our file. If we change our file and type ```git status``` we will see this.
![terminal](../../post-images/the-minimum-you-should-know-about-git-pt-1/git-status-2.png)

Are you see? It says *"hey man your file was changed would you want to track this alteration for a new commit?"*. Cool, we will accept the suggestion and will add the file, after that, do a new commit.
![terminal](../../post-images/the-minimum-you-should-know-about-git-pt-1/git-commit-2.png)

type ```git log``` and see.
![terminal](../../post-images/the-minimum-you-should-know-about-git-pt-1/git-log-2.png)

cool guys, we have now two commits, but... What is the purpose of this?
Let's say you want to know what the differences between your two commits (so many lines, you don't remember haha). With that registers in the time in form of commits we can compare versions of out file in the time with ```git diff``` command for example, for this we need the unique code of two commits (we get this with ```git log```):
![terminal](../../post-images/the-minimum-you-should-know-about-git-pt-1/git-diff.png)

So now, git tell us *"hey bro the difference between this two commit is this two lines"*. Imagine this function in a big change in a real project. Let's say we did shit in our last alteration, we did a commit and the things don't work more. What do we do? We cry? maybe... haha
Don't worry, if we do a shit but we know the last commit work, we can do a git ```reset --hard```, look that:
![terminal](../../post-images/the-minimum-you-should-know-about-git-pt-1/git-reset.png)

See the git log we have one commit from the beginning and the command cat shows what have in our file. Our first version with just "Hello Git!".

So, guys, I hope this helps you to understand the extremely basic of git. This is the part one I will write a part two, with git branch and merge. If you have some question, please leave a comment, I will be happy to ask questions.

ps: This is the first time I write an article in English, I sure I've killed the grammar. If you want to help me correcting something you can fork <a href="https://github.com/gabrielbussolo/gabrielbussolo-blog/blob/master/content/blog/the-minimum-you-should-know-about-git-pt-1.md" markdown="1" target="_blank">this article</a> on my GitHub and correct or just leave a comment for help me. 

Thanks a lot, see you in part 2!