#GitHub Branching and Merging#
Git and GitHub are wonderful tools that allow us to keep well-documented versions of our project files, even allowing us to revert back to earlier versions of a file if needed. However, **branching** allows Git and GitHub users the ability to easily keep a "master" version of our Git repository while experementation and drafting can occur on a "working copy" or "testing copy" of your repository known as a **branch**.


##Local Branching##
As mentioned above, _*branching*_ is when you use Git to make an exact copy of your repository with a different name, or a "branch". Your original Github repository, the one you created or downloaded from GitHub, will always have the name "master". On the the command-line type:

```git branch``` 

This will show you the current branch you are on. If you have never actually created a new branch you should see this:

![Branching example 1](images_branching/git_branch.png)


The asterix next to the word "master" tells us that you are currently working on the master branch. There are no other branches associated with this repository, so every time you commit a change to a file or set of files you are doing so on the master branch.

Let's create a new branch that we can use to experement on without potentially wrecking all of the hard work already done to the master branch.  Creating a new branch is very easy. On the command line, simply type the following:

```git branch testing_branch```

Press ```Enter```.  Now when you type in ```git branch```, you will see that you have two branches of your repository, the "master" branch and the "testing" branch:


![Branching example 2](images_branching/git_branch2.png)

Now, instead of making all of your commits directly to your master branch, you can use "testing_branch" (or whatever you call your newly-created branch) to make initial changes, experiment, or to focus on one aspect of your Git project.

But right now the asterix is showing that you are on the master branch.  To switch to your newly-created branch, type the following:

```git checkout testing_branch```

Press ```Enter```. Now you will see the that you have switched to your new branch:

![Branching example 3](images_branching/git_branch3.png)

And when you type ```git branch``` again, you will see the list of all your branches with the asterix next to the one you most recently switched to:

![Branching example 4](images_branching/git_branch4.png)

When you need to, you switch back to the master branch by typing:

```git checkout master```

Will give you this output:

![Branching example 5](images_branching/git_branch5.png)

Using ```git checkout "name_of_branch"``` (without the quotation marks!) will let you switch between branches whenever you have the need.

##Naming Your Branches ##
Remember that you can name your branches anything you want to, but make sure that if you give it a name with more than one word in it that you _**do not**_ put spaces between words!  It will make your life a lot easier if you place underscores between words or _**camel-case**_ your branch names (ie. "testing_branch" or "testingBranch").  

Once you are satisfied with the results on your testing branch, you can _**merge**_ changes into the master branch.  

##Merging Branches##
Any branch may be merged with another branch. But most of the time, especially early in your Git and GitHubbing career, you will want to merge your working or test branches into the master branch. I will focus on merging testing branches into the master, but what you learn here will allow you to merge *any* branch with any other branch.

##Remote Branching##
//In Development