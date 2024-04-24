# Git Experiment

Repository for experimenting with [Git](https://git-scm.com/).

## First steps

Follow these steps to set up Git:

- Install Git with the package manager
- Configure user information for all local repositories:

    ```shell
    git config --global user.name "[name]"
    git config --global user.email "[email address]"
    ```

- Clone this repository to your machine:

    ```shell
    git clone git@github.com:lug-taunus/git-experiment.git
    ```

    This will clone the repository in the subdirectory `git-experiment`.

## Experimentation

### Basics

#### Add a file

Create a new file with your username (e.g. `philip.txt`) in the directory `users`:

```shell
echo "My own file" > "users/$USER.txt"
```

Review the status of the working tree:

```shell
git status
```

Stage the file in order to commit it:

```shell
git add "users/$USER.txt"
```

Review the status of the working tree:

```shell
git status
```

Commit the changes:

```shell
git commit -m "Add my own file"
```

#### Modify a file

Append the name of the file created in the section [Add a file](#add-a-file) to the `index` file in the directory `users`:

```shell
echo "$USER.txt" >> users/index
```

Review the status of the working tree:

```shell
git status
```

Stage the file in order to commit it:

```shell
git add users/index
```

Review the status of the working tree:

```shell
git status
```

Commit the changes:

```shell
git commit -m "Update index file"
```

#### Delete a file

Delete the file of the dummy user:

```shell
git rm users/dummy.txt
```

Remove the corresponding line from the index file:

```shell
sed -i '/dummy\.txt/d' users/index
```

Review the status of the working tree:

```shell
git status
```

Automatically stage the modified and deleted files and commit the changes:

```shell
git commit -am "Delete dummy user file"
```

## Resources

### Git

- [Pro Git Book](https://git-scm.com/book)
- [Git Cheat Sheet](https://training.github.com/downloads/github-git-cheat-sheet/)
- [Lerne Git Branching](https://learngitbranching.js.org/)

### GitHub

- [GitHub Training Kit](https://training.github.com/)
- [GitHub Basics](https://docs.github.com/en/get-started/start-your-journey)
- [GitHub Skills](https://skills.github.com/)
