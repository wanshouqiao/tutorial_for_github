# tutorial_for_github
## procedures to push a local directory to online github
#### online
1. create a new repository in your github account
2. copy its ssh address which will be used for remote connect
#### local
1. use `git init` to make git manage your local directory
2. use `git add [file]` to add your file to temporary storage area
3. use `git commit -m [description]` to commit your changes
4. use `git branch -M main` to change the branch name to fit the github branch name to avoid merging
#### local to online
1. use `git config --global user.name "wanshouqiao"` to add your github account name to config file
2. use `git config --global user.email "x@x.com"` to add your github account email to config file
3. use `ssh-keygen -t rsa -C "x@x.com"` to create secret key, just return to finish the creation
4. add the id_rsa.pub to your github ssh and gpg keys
5. use `git remote add origin git@github.com:wanshouqiao/tutorial_for_github.git` to connect your local directory with your online repository
> use `git remote set-url origin another_repository` to change your repository
6. use `git push origin main` to push your directory to repository
> origin is bind to your ssh address
7. use `git clone "address"` to clone your online repository
## how to use .gitignore file
1. create .gitignore file in your git directory
2. add a file that has never been managed by git to .gitignore, such as ignore.txt
```.gitignore
ignore.txt
```
3. if a file has been managed, use `git rm --cached "filename"` to ignore it and add it to .gitignore
## erros
- ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'github.com:wanshouqiao/tutorial_for_github.git'
> use `git pull --rebase origin main` to specify the branch
