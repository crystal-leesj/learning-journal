## Version Control

> Version Control is a system that allows you to revisit various versions of a file or set of files by recording changes. Through version control, one can revert a file or project to a previous version, track modifications and modifying individuals, and compare changes. By utilizing a Version Control System (VCS), mistakes with files can easily be rectified.

- Local Version Control
  - 
 
 
## Workflow

### Local Repository Structure
The local Git repository has three components:

1. Working Directory: The actual files reside here.
1. Index: The area used for staging
1. Head: Points to the most recent commit

![Local Repository Structure](https://blog.udemy.com/wp-content/uploads/2015/08/image036.png)

### The Life Cycle of File Status
1. After you edit a file, Git flags it as modified because of changes made after the previous commit.
1. You stage the modified file.
1. Then, you commit staged changes.

![The Life Cycle of File Status](https://blog.udemy.com/wp-content/uploads/2015/08/image006.png)


#### Check File Status
To determine the state of files, utilize the `git status` command:
```
$ git status
```


#### Tracking and Staging a New File
*Single File*
Track one file only by using the following format:
```
git add filename
```
*All Files*
Track all files in a repository by using the following command:
```
$ git add *
```

#### Committing a File
After staging one or multiple files, you should commit the changes and record what you did within the commit message:
```
$ git commit -m “made change x,y,z”
```

#### Committing All Changes
```
$ git commit -a
```

#### Pushing Changes
Next, you would push changes to a remote repository. We will discuss remote repositories in more depth in the next section. For now, we will look at a general overview of pushing changes to remotes.
```
$ git push origin master
```

#### Stashing Changes
When you are not ready to commit changes but do not want to lose them either, `git stash` is a great option. This command temporarily removes changes and hides them, giving you a clean working directory. When you are ready to continue working on the changes, simply use the `git stash apply` command to retrieve the hidden changes.

#### Cloned Repositories
As mentioned earlier, for cloned repositories, Git will automatically give the name “origin” to the server from which you cloned and the name “master” to your local branch.

#### Seeing Your Remotes
By running the `git remote` command, you can view the short names, such as “origin,” of all specified remote handles.

By using `git remote -v`, you can view all the remote URLs next to their corresponding short names.
```
$ cd example
$ git remote -v
remote1 https://github.com/remote1/example (fetch)
remote1 https://github.com/remote1/example (push)
remote2 https://github.com/remote2/example (fetch)
remote2 https://github.com/remote2/example (push)
remote3 https://github.com/remote3/example (fetch)
remote3 https://github.com/remote3/example (push)
```

#### Adding Remotes
To create a new remote Git repository with a short name, use the following format:
```
git remote add shortname url
```
Example:
```
$ git remote
origin
$ git remote add js https://github.com/janesmith/project1
$ git remote -v
origin https://github.com/johndoe/project1 (fetch)
origin https://github.com/johndoe/project1 (push)
js     https://github.com/janesmith/project1 (fetch)
js     https://github.com/janesmith/project1 (push)
```
This addition of these remote and short names allows you to use shortnames for Git collaboration.

#### Fetching
Fetching entails pulling data that you don’t have from a remote project.
```
git fetch [remote-name]
```

#### Pushing
To push your changes “upstream” for sharing, you would use the following `git push` command format:
```
git push [remote-name][branch-name]
```
Example:
```
$ git push origin master
```
#### Renaming/Removing Remotes
*Rename*
To rename a remote’s short name, use the `git remote rename` command.
```
$ git remote rename js jane
$ git remote
origin
jane
```
*Remove*
To remove a remote for whatever reason (e.g., a contributor has left the team, the server has moved), simply use the git remote rm command:
```
$ git remote rm jane
$ git remote
origin
```

### Branching
> Almost every type of Version Control System incorporates branching. By creating branches of a central repository, collaborators are able to work on a project simultaneously via multiple branches, without affecting this main repository.
![Branching](https://blog.udemy.com/wp-content/uploads/2015/08/image016.png)

#### Creating a New Branch
```
$ git branch test
```
![Creating a New Branch](https://blog.udemy.com/wp-content/uploads/2015/08/image027.png)

#### Switching Branches
To switch to another branch, use the `git checkout` command.
```
$ git checkout test
```
![Switching Branches](https://blog.udemy.com/wp-content/uploads/2015/08/image086.png)
If you make a commit while on the test branch, only this branch will point to the most recent commit. The master branch will still point at the commit it was pointing to when you checked out to the test branch. So, if you switch back to the master branch, none of your recent changes made on the test branch will exist on the master branch.

#### Create a Branch and Checkout
To simultaneously create a new branch and switch to it, use the -b switch with the `git checkout` command:
```
$ git checkout -b test2
```

#### List Branches
You can list available branches by using the `git branch` command.
```
$ git branch
*master
```
Above, we see that we have one local branch, named “master”.
