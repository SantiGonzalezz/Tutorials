# Git

This is a tutorial of the use of Git in Windows, specially in Git Bash and GitHub.

It is based on the videos and webpage of Jon Mircha.

- [Git Video](https://www.youtube.com/watch?v=suzMNqDQiyU&t=423s)
- [Git Webpage](https://jonmircha.com/git)

---

## Index

- [Version](#version)
- [Update](#update)
- [Config](#config)
- [Help](#help)
- [Initialize a Git Repo Locally](#initialize-a-git-repo-locally)
- [Git Flow](#git-flow)
  - [Stage](#stage)
  - [Commit](#commit)
  - [Connection with GitHub](#connect-with-github)
  - [Push](#push)
- [Git Ignore](#git-ignore)
- [Clone](#clone)
- [Branches Management](#branches-management)
- [Merging Branches](#merging-branches)
- [Changes in **Last Commit**](#changes-in-last-commit)
- [Historial](#historial)

---

## Version

[Index](#index)

Get the version of the git package downloaded in your computer.

```git
git --version
```

---

## Update

[Index](#index)

Update your version of Git to the last published.

```git
git update-git-for-windows
```

---

## Config

[Index](#index)

Configure Git with your account.

- The name to be displayed

  ```git
  git config --global user.name "Your Name"
  ```

- The email to attach

  ```git
  git config --global user.email youremail@xmail.com
  ```

- Enable the UI of the Git Bash to be with colors

  ```git
  git config --global user.ui true
  ```

- See your current configuration

  ```git
  git config --list
  ```

- Standarize the New Lines for all OS in Windows

  ```git
  git config --global core.autocrlf true
  ```

  <br>
  <br>

Configure or change Git in Visual Studio Code

- Set VS Code to be your editor

  ```git
  git config --global core.editor "code --wait"
  ```

- Edit your Git settings in VS Code

  ```git
  git config --global -e
  ```

---

## Help

[Index](#index)

To get help on the Git commands

- On the Git Bash terminal

  ```git
  git _command_ -h
  ```

  - Help on the config command

    ```git
    git config -h
    ```

- On the Browser

  ```git
  git help _command_
  ```

  - Help on the config command

    ```git
    git help config
    ```

---

## Initialize a Git Repo Locally

[Index](#index)

- Go to the direction of your project. You can copy it from the File Explorer on Windows, however, be sure to replace the `\` with `/`.

  ```git
  cd /c/Users/_User_/_Folder_
  ```

- Know if it worked listing the contents of the folder selected

  ```git
  ls
  ```

- Create a Folder for your repository

  ```git
  mkdir _FolderName_
  ```

  - Create a folder with name `GitPractice`

    ```git
    mkdir GitPractice
    ```

- Go inside the folder

  ```git
  cd _FolderName_/
  ```

  - Go to the folder with name `GitPractice`

    ```git
    cd GitPractice/
    ```

- Create Files in your repository

  ```git
  touch README.md
  touch .gitignore
  ```

- Initialize the Folder as a Git Repo

  ```git
  git init
  ```

- See the content of your repo

  - Public files/folders

    ```git
    ls
    ```

  - Public and Private files/folders

    ```git
    ls -a
    ```

- Open your Git Repo in VS Code

  ```git
  code .
  ```

- You can see the Git Bash Terminal inside VS Code with the ShortCut

  ```java
  Ctrl + ñ
  ```

---

## Git Flow

[Index](#index)

<img 
src="https://i.ibb.co/ZLF57pn/image.png"
width="700"
height="300">

### Stage

- Add individual modfied files to _Staged_

  ```git
  git add _File/Folder_
  ```

- Add all the modified files to _Staged_

  ```git
  git add .
  ```

### Commit

- Commit the changes in terminal

  ```git
  git commit -m "_Message of the commit_"
  ```

- Commit the changes with VS Code. It will open a new tab in the editor where you add the message

  ```git
  git commit
  ```

### Connect with GitHub

- Create the _main_ branch

  ```git
  git branch -M main
  ```

- Create a new repository on Github.

  ```git
  git remote add origin https://github.com/_username_/_repositoryName_.git
  ```

- Create and Push the _main_ branch

  ```git
  git push -u origin main
  ```

### Push

```git
git push
```

### Pull

```git
git pull
```

---

## Git Ignore

To ignore some files to upload into the repository we use `.gitignore` file.

- Ignore particular **files** or **folder**

  ```gitignore
  _filename_
  _foldername_
  ```

- Ignore a file in a specific folder

  ```gitignore
  _foldername_/_filename_
  ```

- Ignore all files that contains something

  ```gitignore
  *_something_
  ```

  - Ignore all `.exe` files

    ```gitignore
    *.exe
    ```

  - Ignore all ending `b.md` files

    ```gitignore
    *b.md
    ```

- Ignore all files that contains something except one

  ```gitignore
  *_something_
  !_something_
  ```

  - Ignore all ending `.md` files except `important.md`

    ```gitignore
    *.md
    !important.md
    ```

- Ignore files that containg something inside a folder but no in its subfolders.

  ```gitignore
  _foldername_/*_something_
  ```

  - Ignore all ending `.md` files in `doc` folder

    ```gitignore
    doc/*.md
    ```

- Ignore files that containg something inside a folder and its subfolders.

  ```gitignore
  _foldername_/**/*_something_
  ```

  - Ignore all ending `.md` files in `doc` folder and its subfolders

    ```gitignore
    doc/**/*.md
    ```

---

## Clone

[Index](#index)

Go to the folder where you want to clone the repository using `cd` in the terminal.

```git
git clone https://github.com/_username_/_repositoryName_.git
```

---

## Branches Management

[Index](#index)

- **List** all the branches in the repo

  ```git
  git branch
  ```

  - List _non merged_ branches with the current branch

    ```git
    git branch --no-merged
    ```

  - List _merged_ branches with the current branch

    ```git
    git branch --merged
    ```

- **Create** a new branch

  ```git
  git branch _branchName_
  ```

- **Change** to other branch

  ```git
  git checkout _branchName_
  ```

- **Create** a branch and **Change** to that branch

  ```git
  git checkout -b _branchName_
  ```

- **Delete** a branch

  - _Locally_

    ```git
    git branch -d _branchName_
    ```

  - _Remotely_

    - ```git
      git push origin --delete _branchName_
      ```
    - ```git
      git push origin :_branchName_
      ```

  - **Force Delete** a branch

    ```git
    git branch -D _branchName_
    ```

- **Publish** a branch to the repository

  ```git
  git push -u origin _branchName_
  ```

---

## Merging Branches

[Index](#index)

Two types:

- Fast-Forward
- Manual Merge

<br>

- Locate on the _main_ branch or the one that will contain the merged content

```git
git checkout _principalBranchName_
```

- Merge

```git
git merge _secondaryBranchName_
```

---

## Changes in Last Commit

[Index](#index)

Add changes to the last commit, only if it has **not been pushed**.

- Commit without changing the message of the commit been modified.

  ```git
  git commit --amend --no-edit
  ```

- Commit changing the message of the one being modified.

  ```git
  git commit --amend -m "_message_"
  ```

- Delete the last commit

  ```git
  git reset --hard HEAD~1
  ```

- Change to an specific past commit,

  ```git
  git checkout _commitId_
  ```

---

## Historial

[Index](#index)

- Show all the **historial** of commits with all the information

  ```git
  git log
  ```

  ```git
  q
  ```

- Show all the historial of commits in **one line**

  ```git
  git log --oneline
  ```

- Show **_n_ last** commits

  ```git
  git log -_n_
  ```

- **Filter** commits by date

  - After

    ```git
    git log --after="2019-12-24 00:00:00"
    ```

  - Berfore

    ```git
    git log --before="2019-12-24 00:00:00"
    ```

  - Between

    ```git
    git log --after="2019-12-24 00:00:00" --before="2019-12-24 00:00:00"
    ```

- Register of all actions of the log.

  ```git
  git reflog
  ```

- Show the commits in a specific **format**

  ```git
  git log --pretty=format:"_format_"
  ```

  - `%h` - Short id
  - `%H` - Long id
  - `%s` - Message
  - `%d` - Reference to branch name
  - `%an` - Author name
  - `%ad` - Authored Date

    - Add

      ```git
      --date=short
      ```

      - Example

        ```git
        git log --pretty=format:"%ad %an %d %s %h" --date=short
        ```

- Show a **graph** of all **branches** and **commits**

  ```git
  git log --oneline --graph --all
  ```

- Get **difference** between **Working Directory** and **Staging**

  ```git
  git diff
  ```
