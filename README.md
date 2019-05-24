Git Course
---

Basic commands:

```shell
git init                  // Initialize repository
git show                  // Show current state
git add file.txt          // Add specific file to staging
git add .                 // Add all files in my current directory to staging
git commit -am "Message"  // Commit changes with current changes in staging adding a message
```

Initial configuration before push changes:
```shell
git config --global user.email "you@email.com"  // Base user email config 
git config --global user.name "Your name"       // Base user name config 
git config -l                                   // List git user config
```

Git changes between commits
```shell
git reset commitId --hard  // Back to previous commit ignoring all current changes
git reset commitId --soft // Back to previous commit keeping the current changes
```

Git logging
```shell
git log                                     // Show git history changes
git log --stat                              // Show git history changes with more stats and information
git log --all --graph                       // Show git history showing all branches graph
git log --all --graph --decorate --oneline  // Show git history showing all branches graph with pretty decoration
```

Git branching
```shell
git branch new_branch     //
git checkout new_branch   //
git branch                //
```

Git merge
```shell
git merge branch_name
```

Working with remote repositories
```shell
git pull origin branch_name
git pull origin branch_name --allow-unrelated-histories
git push origin branch_name
git remote -v
git remote set-url origin git_repository_url
```

Create rsa key
```shell
ssh-keygen -t rsa -b 4096 -C "youremail@example.com"  // Generate new rsa public && private key
eval $(ssh-agent -s)                                  // Verify if ssh server is running
```

Ssh config
```shell
Host *
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile ~/.ssh/id_rsa
```

Adding new ssh key
```shell
ssh-add -K ~/.ssh/id_rsa
```

Git aliases
```
alias arbolito="git log --all --graph --decorate --oneline" 
```