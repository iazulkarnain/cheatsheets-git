# cheatsheets-git
Detailed cheatsheets with instructions: [detailed-cheatsheets.md](detailed-cheatsheets.md)

## Git Installation on Ubuntu 20.04
```shell
sudo apt update
sudo apt install git
```

## Setting git configs on your PC
```shell
git config --global user.name "<YOUR_USERNAME>"
git config --global user.email "<YOUR_EMAIL>"
```

## Connecting your PC to Github Account
Ref: https://docs.github.com/en/authentication/connecting-to-github-with-ssh/checking-for-existing-ssh-keys
```shell
cd $HOME

ls -al ~/.ssh

ssh-keygen -t ed25519 -C "ihsan.a.zulkarnain@gmail.com"
# Prompt: Enter file in which to save the key (...): [Enter]
# Prompt: Enter passphrase (empty for no passphrase): <YOUR_PASSWORD>[Enter]
# <YOUR_PASSWORD will be asked whenever you interact with the remote github repos

ssh-add ~/.ssh/id_ed25519

cat ~/.ssh/id_ed25519.pub
# Copy the printed strings

# At Github page
# > Click your account icon > Settings > Access: SSH and GPG Keys
# > Click "New SSH Key"
# Paste the key
# > Click "Add SSH Key"
```

## Test connecting to one of your existing remote repositories.
```shell
git remote add origin git@github.com:<YOUR_USERNAME>/<YOUR_REPO_NAME>.git
git clone git@github.com:<YOUR_USERNAME>/<YOUR_REPO_NAME>.git
```

## Creating a new repository and add new/updated files from local to remote
```shell
cd <WORKING_DIR>
git init
echo "MIT License" > LICENSE
echo "# Readme" > README.md
git add ./*
git commit -m "Initial commit"
git remote add origin git@github.com:<YOUR_USERNAME>/<YOUR_REPO_NAME>.git
git push -u origin main
```

## Checking available branches in a local repo
```shell
cd <WORKING_DIR>
git branch
# * main
```

## Checking available branches in a remote repo
```shell
git remote
# origin
git remote --get-url origin
# https://github.com/<YOUR_USERNAME>/<YOUR_REPO_NAME>.git
```
