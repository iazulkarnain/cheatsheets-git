# cheatsheets-git
Detailed cheatsheets with instructions: [detailed-cheatsheets.md](detailed-cheatsheets.md)

## Git Installation on Ubuntu 20.04
```shell
sudo apt update
sudo apt install git
```

## Connecting your PC to your Github account
```shell
git config --global user.name "<YOUR_USERNAME>"
git config --global user.email "<YOUR_EMAIL>"
```

## Test connecting to one of your existing remote repositories.
```shell
git remote add origin https://github.com/<YOUR_USERNAME>/<YOUR_REPO_NAME>.git
git clone https://github.com/<YOUR_USERNAME>/<YOUR_REPO_NAME>.git
```

## Creating new repositories and add files from local to remote
```shell
cd <WORKING_DIR>
git init
echo "MIT License" > LICENSE
echo "# Readme" > README.md
git add ./*
git commit -m "Initial commit"
git remote add origin https://github.com/<YOUR_USERNAME>/<YOUR_REPO_NAME>.git
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
