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
