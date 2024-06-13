if you want to push your first project to github repo:

 - login your github account on your browser. Create new repository
***

 - Firstly you must go `root` directory of your project
 - you should create `.gitignore` file. inside the file you can write paths of files or folders that you don't want to upload to you github repo. For example: if your project written on `reactjs` then you don't need upload your `node_modules` folder to the github repo... Like this example you must know  what files or folders that  could get with installation or big memory files, folders...
 - Recommended create `README.MD` file and write inside file how to get and how to install and how to run your project....
 after these steps you can write code below:
```shell
git init
git branch -M main # set branch to `main`
git add .
git commit -m "first commit"
git remote add origin <your link> 
git push -u origin main
```