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
How to use Git it on your computer</h2></summary>

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
How to use git it on Github.com
</h2></summary>

### Organisation of Github
Git is organized in repositories. You can create, commit into and anoate into repositories right on github.

### How create a new repository on Github:
1. First, make sure you have a GitHub account and are logged in. You can sign up for an account at https://github.com/.

2. Next, navigate to the main page of GitHub and click the "New repository" button.

3. You will be prompted to enter a name for your repository and a brief description. You can also choose to make the repository public or private. Once you have filled in the information, click the "Create repository" button.

4. Now you will be taken to the main page of your new repository. On this page, you will see the repository's URL, which you will need in the next step.

5. Next, open a terminal window on your computer and navigate to the directory where you want to store a local copy of your repository.

To clone your newly created repository, you need to run the command:

```
$ git clone https://github.com/<username>/<reponame>.git
```

7. This command will create a new directory with the same name as your repository and download a copy of the repository to your computer. You can navigate into the directory and start adding files to it.
   
</details>

<details><summary><h2>
Git concepts </h2></summary>

### .gitignore
The .gitignore file includes all files that are not being tracked. 

### Readme.md

A README.md file is a text file that contains information about a project. It is typically located in the root directory of a repository and is used to provide documentation and instructions for users who want to understand or contribute to the project.

The README.md file typically contains the following information:

- Project name and description: A brief summary of what the project is and what it does.

- Installation instructions: Instructions on how to install and set up the project, including any dependencies that need to be installed.

- Usage instructions: Information on how to use the project, including any command-line arguments or configuration options.

- Contribution guidelines: Information on how to contribute to the project, including any coding standards or conventions that need to be followed (also sometimes in a seperate Contributing.md)

- License information: Information on the license under which the project is released, such as the MIT License or the GNU General Public License.
###  Contributing.md

A CONTRIBUTING.md file is a text file that contains information about how to contribute to a project. It is typically located in the root directory of a repository and is used to provide guidelines and instructions for users who want to contribute code, documentation, or other types of changes to the project.

A CONTRIBUTING.md file typically contains the following information:

- Code of Conduct: Information on the code of conduct that must be followed when contributing to the project. This can include guidelines for behavior, communication, and inclusivity.

- Reporting issues: Instructions on how to report issues or bugs, including any templates or guidelines that should be followed.

- Submitting changes: Information on how to submit changes to the project, including any coding standards or conventions that should be followed, and instructions on how to create a pull request.

- Testing: Information on how to test the code and any instructions on how to run the tests.

- Documentation: Information on how to contribute to the documentation, including any guidelines or conventions that should be followed.

- Styleguides: Information on any styleguides or linting rules that should be followed when contributing code.

</details>

<details><summary><h2>
Creating ssh keys </h2></summary>

Type the following in your terminal to create a new ssh key pair

```
$ ssh-keygen -t 4096 -C ">your_git_email<"
```

This will generate a private/public rsa key pair. Hit `enter` when promyted to giev a passphrase (no passphrase).
You should receive a prompt that your key pair has been generated and where it has been stored.


Now you need to add the key pair to your .ssh file. Type:

```
$ ssh-add ~/.ssh/id_rsa
```

copy the public(!) part of the pair
```
$ clip < ~/.ssh/id_rsa.pub
```
Add public(!) key to git hub.

<!--- 
![](img/Picture4.png)
![](img/Picture5.png)
--->

</details>


<details><summary><h2>Git via GUIs</h2></summary>

### VScode

### Github Desktob
</details>


<details><summary><h2>Important git commands</h2></summary>

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

<details><summary><h2>Merge conflicts</h2></summary>
</details>

Merge conflicts occur when there are changes in the same lines of code in different branches that Git is unable to automatically merge. When this happens, Git will mark the conflicting lines in the file, and you will need to resolve the conflict manually. Here is the general process for resolving merge conflicts:

1. Identify the conflict: Git will mark the conflicting lines in the file with special markers, such as <<<<<<< and >>>>>>>. The lines between these markers will show the conflicting changes.

2. Decide on the changes to keep: Look at the conflicting changes and decide which changes you want to keep and which changes you want to discard. You can use a text editor or a merge tool to make this process easier.

3. Remove the conflict markers: Once you have decided on the changes to keep, remove the conflict markers (<<<<<<<, =======, >>>>>>>) and any lines that you don't want to keep.

4. Add the resolved file: Once you have resolved the conflicts, you need to stage the resolved file

```
$ git add <file-name>
```

Commit the merge: After you have resolved the conflicts and added the file, you can commit the merge with a meaningful commit message.
```
$ git commit -m "resolved merge conflict"
```
Push the changes: Finally, push the changes to the remote repository.
```
$ git push
```
It is also possible to use a merge tool to resolve conflicts. A merge tool provides a graphical interface that allows you to view and compare the conflicting changes, and select which changes to keep. Some popular merge tools include `kdiff3`, `meld`, and `p4merge`.

It is important to keep in mind that merging conflicts can be a complex process and it's always better to communicate with the team members and coordinate with them before merging your changes.


<details><summary><h2>Branches </h2></summary>

To create a new branch in Git, you can use the command:

```
$ git branch <branch-name>
```
This will create a new branch with the name specified. For example,

```
$ git branch feature-x
```
Once the branch is created, you can switch to the new branch by using the command:

```
$ git checkout <branch-name>
```
For example,

```
$ git checkout feature-x
```
When you create a new branch, it is created based on the commit that you are currently on. You can make changes and commit them as usual once you are on the new branch.

It's also worth noting that you can also create a new branch and switch to it in one command:

```
$ git checkout -b <branch-name>
```
This will create a new branch with the name specified and switch to it.

It is good practice to use branches for different features, bug fixes and also for testing purpose. It helps to keep your code organized and maintain the quality of the code.

Once you made your changes, you can push the branch to remote repository.

```
$ git push origin <branch-name>
```
Then you can create a pull request on GitHub, it will notify the team members that you have made changes and ready to merge it with the main branch.
</details>

<details><summary><h2>Best practices</h2></summary>

1. **Commit often** : Committing your changes frequently allows you to track your progress and easily undo mistakes. It's also easier to review smaller, more focused commits than a large one.

2. ***Use meaningful commit messages**: Each commit message should briefly describe the changes made in the commit. This makes it easier for others to understand the purpose of the commit and to review the code.

3. **Keep commits small and focused**: A commit should include only related changes. Avoid including multiple unrelated changes in a single commit, as it makes it harder to understand and revert the changes.

4. **Use branches**: Create branches for different features or bug fixes, so that you can work on them independently without affecting the main branch. Use branches also for testing purpose. You should have at least two branches: *main* and *dev*. 

5. **Pull before pushing**: Before pushing your changes, make sure to pull the latest changes from the remote repository to avoid conflicts.

6. **Review code before pushing**: It is a good practice to review your code before pushing it to the remote repository. This can help to catch any errors or mistakes that might have been missed during development.

7. **Use a .gitignore file**: Use a .gitignore file to exclude files and directories that should not be tracked by Git. Common examples include build artifacts, dependencies, and sensitive files.

8.**Keep your repository clean**: Keep your repository clean by deleting branches that have been merged or are no longer needed.

9. **Use pull requests**: Use pull requests to review and merge code changes. This allows other team members to review the code and suggest changes before it is merged into the main branch.

10 **Use version tags**: Use version tags to mark specific commits as releases. This allows you to easily revert to a previous version if needed.
</details>
