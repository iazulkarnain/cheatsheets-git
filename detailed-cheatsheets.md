# Detailed Cheatsheets

## Git Installation on Ubuntu 20.04
1. Open a terminal window by pressing Ctrl+Alt+T on your keyboard.
2. Update the package list on your computer by running the following command:
```shell
sudo apt update
```
3. Install Git on your computer by running the following command:
```shell
sudo apt install git
```

## Connecting your PC to your Github account
1. Once Git is installed, you will need to configure it with your GitHub account. To do this, run the following commands, replacing YOUR_USERNAME and YOUR_EMAIL with your GitHub username and email address:
```shell
git config --global user.name "YOUR_USERNAME"
git config --global user.email "YOUR_EMAIL"
```
## Test connecting to one of your existing private remote repositories.
1. You can now connect to your GitHub account by running the following command, replacing YOUR_USERNAME with your GitHub username:
```shell
git remote add origin https://github.com/<YOUR_USERNAME>/<YOUR_REPO_NAME>.git
```
2. To test that your connection to GitHub is working, you can try to clone one of your private remote repositories by running the following command, replacing YOUR_REPO_NAME with the name of your repository:
```shell
git clone https://github.com/<YOUR_USERNAME>/<YOUR_REPO_NAME>.git
```

