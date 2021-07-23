# Create a git repo

## Create A Repo From Scratch

Before you can make commits or do anything else with a git repository, the repository needs to actually exist. To create a new repository with Git, we'll use the git init command.

The init subcommand is short for "initialize", which is helpful because it's the command that will do all of the initial setup of a repository. We'll look at what it does in just a second.

Git Init
Fantastic work - we're all set up and ready to start using the git init command!

This is one of the easiest commands to run. All you have to do is run git init on the terminal. That's it! Go ahead, why not give it a try right now!

Git Init's Effect
Running the git init command sets up all of the necessary files and directories that Git will use to keep track of everything. All of these files are stored in a directory called .git (notice the . at the beginning - that means it'll be a hidden directory on Mac/Linux). This .git directory is the "repo"! This is where git records all of the commits and keeps track of everything!

Let's take a brief look at the contents of the .git directory.

## Clone a repository

The way that cloning relates to Git is that the command we'll be running on the terminal is git clone. You pass a path (usually a URL) of the Git repository you want to clone to the git clone command.

```$ git clone https://github.com/udacity/course-git-blog-project```

## Git Status

Working with Git on the command line can be a little bit challenging because it's a little bit like a black box. I mean, how do you know when you should or shouldn't run certain Git commands? Is Git ready for me to run a command yet? What if I run a command but I think it didn't work...how can I find that out? The answer to all of these questions is the git status command!

```$ git status```

The output tells us two things:

1 - On branch master – this tells us that Git is on the master branch. You've got a description of a branch on your terms sheet so this is the "master" branch (which is the default branch). We'll be looking more at branches in lesson 5

2 - Your branch is up-to-date with 'origin/master'. – Because git clone was used to copy this repository from another computer, this is telling us if our project is in sync with the one we copied from. We won't be dealing with the project on the other computer, so this line can be ignored.

3 - nothing to commit, working directory clean – this is saying that there are no pending changes.

# Review A Repo`s History

## Displaying A Repository's Commits

The Git Log Command

Finding the answers to these questions is exactly what git log can do for us! Instead of explaining everything that it can do for us, let's experience it! Go ahead and run the git log command in the terminal:

```git log```

Navigating The Log
If you're not used to a pager on the command line, navigating in Less can be a bit odd. Here are some helpful keys:

to scroll down, press
j or ↓ to move down one line at a time
d to move by half the page screen
f to move by a whole page screen
to scroll up, press
k or ↑ to move _up_ one line at a time
u to move by half the page screen
b to move by a whole page screen
press q to quit out of the log (returns to the regular command prompt)

## Changing How Git Log Displays Information

```git log --oneline```

The git log command has a flag that can be used to alter how it displays the repository's information. That flag is --oneline:

```$ git log --stat```

This command:

displays the file(s) that have been modified
displays the number of lines that have been added/removed
displays a summary line with the total number of modified files and lines that have been added/removed

```$ git log -p```

Viewing A Specific Commit

But did you know, you can supply the SHA of a commit as the final argument for all of these commands? For example:

```$ git log -p fdf5493```

or 

```$ git show fdf5493```