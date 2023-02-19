Lesson 1: 

### How to Clone a Repository (Cloning a repository means when you copy a repository from Github.com to your local machine)

1. First Go to Github and select the Green <Code> tab
2. Under this tab there are three options for cloning HTTP, SSH and Github CLI; Copy the Http link as we will use it in an upcoming step.
Note: The following instructions are applicable when you choose HTTP option for cloning
3. Go to your terminal; I was using Gitbash so I went in Gitbash and for convenience first I made a new directory named Git.
4. mkdir git
5. cd git
6. git clone <paste the HTTP link that we copied earlier from Github.com) (it will be something like this https://github.com/nameofrepository.git)
7. ls (you can see that what is inside the repository for example lets say ls command shows you a directory named Linux and now you want to go inside Linux)
8. cd Linux
9. ls (To see what is all there inside Linux)

#### Note: To make your file inside this directory you can use anything touch, nano or vi command; I used vi
                    
10. vi filename (it will create a new file)
11. press i (to edit your file)
12. ls (to check the file you just created is in there)
13. git add . (To promote pending changes in the working directory)
14. git commit -m "Message" (to create a snapshot of the staged changes along a timeline of gitprojects history)
15. git push (To upload local repository content to a remote repository)
