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
git branch new_branch
git checkout new_branch
git branch
git show-branch --all
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

Git tags
```shell
git tag -a nombre-del-tag id-del-commit   // Create a new tag && assing it to commit
git tag -d nombre-del-tag                 // Delete tag in local repository
git tag o git show-refs --tags            // List all tags in local repository
git push origin --tags                    // Publish tag in remote repository
git tag -d nombre-del-tag                 // Delete tag in local repository
git push origin :refs/tags/nombre-del-tag // Delete tag in remote repository
```


Git clone
```
git clone repository_url
```

Git rebase: Reorganizing history
```
git rebase master
```

Git stash
```
git stash                    // Store temporal changes
git stash list               // List temporal changes
git stash pop                // Reestablish temporal store changes
git stash branch branch_name // Create new branch based on stash changes
git stash drop               // Delete stash changes
```

Git clean
```
git clean --dry-run
git clean -f
```

Git cherry-pick
```
git cherry-pick commitId
```

Git restart commit
```
git commit --amend
```


Git reset
```
git reset --soft HEAD_Hash
git reset --hard HEAD_Hash
```

Git reflog
```
git reflog
```


Search files
```
git grep -c "<p>"
git log --all --grep="Palabra"
```

More commands
```
git shortlog -sn --all --no-merges
git config --global alias.stats "shortlog -sn --all --no-merges"
git blame file.txt
git help blame
git blame css/styles.css -L35,53
git branch -r
git branch -a
```