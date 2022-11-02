# Git

## Prerequisites
a. Configure git
```bash
git config --global user.name "[full name]"
git config --global user.email [email]
git config --global core.editor vi
git config --global push.default simple
git config --global credential.helper cache
```
b. Clone repo to local work environment
```bash
$ git clone [repo URI]
```
## Standard branch workflow

1. Create branch on remote repository
On Github and Bitbucket you can create a new branch using the webinterface. Branch should be named `[issue number]-[issue description]`.

2. Switch to branch
    ```bash
    $ cd [repo]
    $ git checkout [branch-name]
    ```

3. Push changes
    ```bash
    $ git add .
    $ git commit
    $ git push
    ```

4. Open Pull Request
On Github and Bitbucket you can open a pull request with the branch as source and the master as destination.

5. Merge branch to master

6. Delete the branch
    ```bash
    $ git push origin --delete [branch-name]
    ```

## Github workflow 
[Github Standard Fork & Pull Request Workflow](https://gist.github.com/Chaser324/ce0505fbed06b947d962)
