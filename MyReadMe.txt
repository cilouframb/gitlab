Installer cmder

Dans settings, on peut changer le répertoire de startup :
Startup ->Tasks, choisir {cmd::Cmder} puis le boutin Startup dir
et ajouter le répertoire de travail GitRepo


Puis pour lier le Repo local à un repo distant :

C:\Users\framb\OneDrive\Documents\GitRepo
? git clone https://github.com/cilouframb/gitlab
Cloning into 'gitlab'...
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (4/4), done.

C:\Users\framb\OneDrive\Documents\GitRepo
? ls
gitlab/

C:\Users\framb\OneDrive\Documents\GitRepo
? cd gitlab

C:\Users\framb\OneDrive\Documents\GitRepo\gitlab (master -> origin)
? git branch
* master

C:\Users\framb\OneDrive\Documents\GitRepo\gitlab (master -> origin)
? git help


créer une branche 
C:\Users\framb\OneDrive\Documents\GitRepo\gitlab (master -> origin)
? git branch myFirstBranch

C:\Users\framb\OneDrive\Documents\GitRepo\gitlab (master -> origin)
? git branch -a
* master
  myFirstBranch

qu'y a t'il d'ajouté de modifié dans ma branche ?
C:\Users\framb\OneDrive\Documents\GitRepo\gitlab (myFirstBranch -> origin)
? git status
On branch myFirstBranch
Untracked files:
  (use "git add <file>..." to include in what will be committed)

        MyReadMe.txt

nothing added to commit but untracked files present (use "git add" to track)

C:\Users\framb\OneDrive\Documents\GitRepo\gitlab (myFirstBranch -> origin)
? git add MyReadMe.txt

C:\Users\framb\OneDrive\Documents\GitRepo\gitlab (myFirstBranch -> origin)
? git commit -m "MyFirstBranch contains MyReadMe.txt"

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got 'framb@LAPTOP-UJT959GP.(none)')

C:\Users\framb\OneDrive\Documents\GitRepo\gitlab (myFirstBranch -> origin)
? git config --global user.email framb1112@hotmail.fr

C:\Users\framb\OneDrive\Documents\GitRepo\gitlab (myFirstBranch -> origin)
? git config --global user.name framb1112

C:\Users\framb\OneDrive\Documents\GitRepo\gitlab (myFirstBranch -> origin)
? git commit -m "MyFirstBranch contains MyReadMe.txt"
[myFirstBranch 3ffeee2] MyFirstBranch contains MyReadMe.txt
 1 file changed, 31 insertions(+)
 create mode 100644 MyReadMe.txt

pousser ma branche en remote :
C:\Users\framb\OneDrive\Documents\GitRepo\gitlab (myFirstBranch -> origin)
? git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

C:\Users\framb\OneDrive\Documents\GitRepo\gitlab (master -> origin)
? git pull
Already up to date.

C:\Users\framb\OneDrive\Documents\GitRepo\gitlab (master -> origin)
? git checkout myFirstBranch
Switched to branch 'myFirstBranch'

C:\Users\framb\OneDrive\Documents\GitRepo\gitlab (myFirstBranch -> origin)
? git push origin myFirstBranch
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 711 bytes | 711.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
remote:
remote: Create a pull request for 'myFirstBranch' on GitHub by visiting:
remote:      https://github.com/cilouframb/gitlab/pull/new/myFirstBranch
remote:
To https://github.com/cilouframb/gitlab
 * [new branch]      myFirstBranch -> myFirstBranch


merger ma branche à la master :

C:\Users\framb\OneDrive\Documents\GitRepo\gitlab (myFirstBranch -> origin)          
? git checkout master                                                               
Switched to branch 'master'                                                         
Your branch is up to date with 'origin/master'.                                     
                                                                                    
C:\Users\framb\OneDrive\Documents\GitRepo\gitlab (master -> origin)                 
? git pull                                                                          
Already up to date.                                                                 
                                                                                    
C:\Users\framb\OneDrive\Documents\GitRepo\gitlab (master -> origin)                 
? git merge myFirstBranch                                                           
Updating 6f33ab8..3ffeee2                                                           
Fast-forward                                                                        
 MyReadMe.txt | 31 +++++++++++++++++++++++++++++++                                  
 1 file changed, 31 insertions(+)                                                   
 create mode 100644 MyReadMe.txt                                                    
                                                                                    
C:\Users\framb\OneDrive\Documents\GitRepo\gitlab (master -> origin)                 
? git branch                                                                        
* master                                                                            
  myFirstBranch                                                                     
                                                                                    
C:\Users\framb\OneDrive\Documents\GitRepo\gitlab (master -> origin)                 
? git push origin master                                                            
Total 0 (delta 0), reused 0 (delta 0)                                               
To https://github.com/cilouframb/gitlab                                             
   6f33ab8..3ffeee2  master -> master                                               
                                                                                    