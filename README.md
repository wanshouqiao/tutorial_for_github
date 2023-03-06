# tutorial_for_github
## procedures to push a lolocal directory to online github
#### online
1. create a new repository in your github account
2. copy its ssh address which will be used for remote connect
#### local
1. use `git init` to make git manage your local directory
2. use `git remote add origin git@github.com:wanshouqiao/tutorial_for_github.git` to connect your local directory with your online repository
3. use `git add [file]` to add your file to temporary storage area
4. use `git commit -m [description]` to commit your changes
5. use `git push origin master` to push your directory to repository
> origin is bind to your ssh address
7. use `git clone origin` to clone your online repository
