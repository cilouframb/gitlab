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