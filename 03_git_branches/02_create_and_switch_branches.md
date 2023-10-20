# Creating and Switching to Branches 🌳

In this section we step into the universe of branches where you create multiple paths for diverse tasks and jump between them seamlessly. We will visit the most fundamental commands, and unravel the methods to smoothly navigate through different branches of your project.

## A prelude: understanding the HEAD 🤯

In the realm of Git, the term HEAD holds significant weight. Let's demystify what HEAD is, understand its role, and learn how to use it efficiently.

### What is HEAD?

In Git, HEAD is a reference to the current snapshot in your working directory. It is used internally by Git to know which commit your working directory is currently on. It's like a bookmark, pointing to the branch and commit that you're currently working on. When you switch branches, the HEAD revision changes to the latest commit on the new branch.

HEAD assists you in navigating through the history of your project. When you make a new commit, HEAD is updated to that new commit.

### How to Use HEAD?

You often encounter HEAD when you want to move to previous commits without switching branches, but this subject is kind of hard to understand only by reading text, so here you have two videos for you to understand HEAD a bit better.

<img src="../images/dfvvQgOhFechd.jpg" alt="WindowsVenv" width="300" height="auto">

[Link to video](https://www.youtube.com/watch?v=dfvvQgOhFec)

<img src="../images/GN36mrrM12khd.jpg" alt="WindowsVenv" width="300" height="auto">

[Link to video](https://www.youtube.com/watch?v=GN36mrrM12k)




## `git branch` : laying down a new path 🛤️

The `git branch` command is your ticket to creating new branches where you can work on different tasks simultaneously without a hiccup. But it does even more, it is the basis for any operation that you want to perform, from checking information on the branches, to renaming, do deleting.

- `git branch` : it will list all of the branches in your repository.
- `git branch -r` : list all the remote branches.
- `git branch -a` : list both remote-tracking branches and local branches.
- `git branch <branch_name>` : create a new branch named `<branch_name>`.
- `git branch -d <branch_name>` : delete the specified local branch. Use `-D` to force delete unmerged branches.
- `git branch -m <old_name> <new_name>` : rename a branch from `<old_name>` to `<new_name>`.
- `git branch -u <upstream_branch>` : set an upstream branch for the current branch.
- `git branch --show-current` : show the name of the current branch.

## `git checkout` : hopping onto a new branch 🏃‍♂️

The `git checkout` command is your reference point to switching, but also creating, between branches.

- `git checkout <branch>` : switch to the specified branch and update the working directory.
- `git checkout -b <new_branch>` : create a new branch and switch to it.
- `git checkout -b <new_branch> <start_point>` : create a new branch, based on `<start_point>`, and switch to it.
- `git checkout -- <file>` : discard changes in your working directory to the specified `<file>`.
- `git checkout <commit>` : switch to a specific commit, detaching the HEAD.
- `git checkout -` : switch to the branch last checked out.
- `git checkout --orphan <new_branch>` : create a new branch, with no commit history, and switch to it.


## Visual Aid 🎥

To fully grasp these new concepts, check out this explanation of the git branch and git checkout commands. Notice the difference between a **local** branch and a **remote** one. 

<img src="../images/iO4QjPUkGJkhd.jpg" alt="WindowsVenv" width="300" height="auto">

[Link to video](https://www.youtube.com/watch?v=iO4QjPUkGJk)

## VSCode: Your Companion in Branch Management 🧭

As usual, we now introduce you into the nice world of VSCode, where this type of branch management becomes almost trivial. Here is an introduction to navigating branches using the VSCode interface.

<img src="../images/b9LTz6joMf8hd.jpg" alt="WindowsVenv" width="300" height="auto">

[Link to video](https://www.youtube.com/watch?v=b9LTz6joMf8)


Recall Git Graph? It makes a re-entry here! With Git Graph you can visualize your branches in a structured tree format, helping you to oversee and manage branches. This tool not only lets you visualize but also execute operations directly while overseeing the branch structure. now, you can revisit the part in which we navigate through commits and branches. 

<img src="../images/u9ZQpKGTog4hd.jpg" alt="WindowsVenv" width="300" height="auto">

[Link to video](https://www.youtube.com/watch?v=u9ZQpKGTog4)