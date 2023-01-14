# Introduction to Git course

<details><summary><h2>Pre-requisites for the course</h2></summary>

 - sign up for a [github.com account](https://github.com/) and make sure you remember the password to sign in
 - make sure that git is installed on your machine.  You can check this by typing: 

```
git -- version
```
</details>

<details><summary><h2>
What is Git?</h2></summary>

Git is a version control system that allows you to track and save changes to your projects, files, code etc by taking annotated, reversible snapshots of your repositories. 
</details>


<details><summary><h2>
Git on your computer?</h2></summary>

1. Navigate to the directory where you want to create your Git repository. For example, if you want to create a repository for a new project called "myproject", you would navigate to the directory where you want to store your project and run the following command:

```
$ git init myproject
```
2. This will create a new directory called "myproject" that is now a Git repository. You can navigate into the directory and start adding files to it.
3. After adding some files, you can check the status of your repository using the command:

```
$ git status
```
This will show you which files have been modified or added since the last commit.

4. To add these changes to your repository, you need to first stage them. You can do this by running the command:

```
$ git add .
```

This will add all the changes you've made to the "staging area".

5. Once the changes are staged, you can commit them to your repository by running the command:

```
$ git commit -m "Initial commit"
```

This will save the changes to the repository and add a message describing the commit.

6. After commit, you can push the code to your remote repository (Github, Bitbucket, Gitlab etc.)

```
$ git push origin <branch-name>
```

</details>


<details><summary><h2>
Git on Github.com
</h2></summary>
### Organisation of Github
Git is organized in repositories. You can create, commit into and anoate into repositories right on github.
</details>

<details><summary><h2>
Git concepts </h2></summary>

### .gitignore
The .gitignore file includes all files that are not being tracked. 

### readme.md
###  contributing.md

</details>

<details><summary><h2>
Creating ssh keys </h2></summary>

Type the following in your terminal to create a new ssh key pair
![](img/Picture1.png)

add the key pair to your .ssh file:
![](img/Picture2.png)

copy the public(!) part of the pair
![](img/Picture3.png)

Add public(!) key to git hub:

<!--- 
![](img/Picture4.png)
![](img/Picture5.png)
--->

</details>

<details><summary><h2>Git at the command line</h2></summary>

## Commands

### show the status of the working tree
```
git status
```
### show local changes
``` 
git diff
```
Go back from `git  diff` by trying `q`
### staging
```
git add file
```
### committing
```
git commit -m "my commit"
```
### staging  and committing
```
git commit -a -m "Intro to git"
```
### push to remote (publish)
```
git push
```
</details>

<details><summary><h2>Branches </h2></summary>

#### new branch and publish it to remote
```
git checkout -b dev
git push -u origin dev
```
</details>


<details><summary><h2>Git via GUIs</h2></summary>

### VScode

### Github Desktob
</details>

<details><summary><h2>Best practices</h2></summary>

1. You should have at least two branches: *main* and *dev*. 
</details>

<details><summary><h2>Merge conflicts</h2></summary>
</details>
