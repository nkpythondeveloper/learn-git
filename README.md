# GIT Tutorial

## 1. SETUP

- Download and install git, from [official git website](https://git-scm.com/downloads)

- Post installation, if you are going to setup Github account, create one.

- Now lets setup the **global configs**

    . To see/list global configs
    ```cmd
    git config --global --list
    ```
    . To setup global config
    ```cmd
    git config --global user.name 'your username'
    git config --global user.email your_github_email
    git config --global user.password your_github_password
    ```

## 2. USAGE

### GIT BASICS

- Create a Git Repo Locally
```cmd
    mkdir first_repo
    cd first_repo
    git init
```

- Add and Commit Changes
```cmd
    echo '# First Repo' > README.md
    git status
    git add README.md
    git commit -m 'Initial Commit'
```

- Check History
```cmd
    git log
```

### REMOTES

- Connect to Github
    
- Create a repo on Github (e.g., first-repo)

- In your local repo
```cmd
    git remote add origin https://github.com/your_user_name/first-repo.git
    git branch -M main
    git push -u origin main            
```

- To Clone existing repo from Github to local
```cmd
    git clone https://github.com/your_user_name/git-example.git
```

- Pull/Fetch Latest
```cmd
    git pull original main
    git fetch origin
```

### BRANCHING & MERGING

- Create & Switch Branch
```cmd
    git branch feature1
    git checkout feature1    
```
There is another direct way of doing this
```cmd
    git checkout -b feature1
```

- Merge Branch
```cmd
    git checkout main
    git merge feature1
```
After this we can delete the local feature branch
```cmd
    git branch -d feature1
```