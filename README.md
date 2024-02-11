There are 4 phases in git: working Directory, Staging Area, Local Repositroy, Remote Repository.
## Basic command line
    cd : change directory
    
    cd .. : change to previous directory

    echo "some message" >> <filename.txt>: create filename(.txt file) and wrtie some message to that file

    rm - fr <directory name> : remove directory

    mkdir <directory name> : create directory

    pwd : show path of working directory

    ls : list all the files in that working directory
## Useful command for git
    git status : checking working Directory, Staging Area
    
    git log : checking commit history

    git fetch : command that tells your local git to retrieve the latest meta-data info from the original

    git remote -v : check our remote repository

    git branch <namebranch> : create branch
    
    git branch -d <namebranch> : delete branch

    git branch -a : list all the branches and check the current branch

    git checkout <namebranch> : change to the branches you wanna work on
## Git problem
Problem:

    ! [rejected]        main -> main (fetch first)
   
    error: failed to push some refs to 'your own git https'
   
    hint: Updates were rejected because the remote contains work that you do not
   
    hint: have locally. This is usually caused by another repository pushing to
   
    hint: the same ref. If you want to integrate the remote changes, use
   
    hint: 'git pull' before pushing again.
    
    hint: See the 'Note about fast-forwards' in 'git push --help' for details.
what happens:

    - You haven't made any local commits on your main branch
    
    - But new commits were pushed to the remote main branch by someone else
    
    - So your local main branch is now behind the remote 
solution: 

    we have to fetch, merge the changeset, and then you'll be able to push again.

    1) git fetch origin main

    2) git merge origin main  ****quick Note you probably have git merge conflict  
        
        2.1) so go inside that file and delete

             <<<<<<< HEAD

             =======
             
             >>>>>>> origin

    3) Now you can do git add --all which add all your files to staging area, git commit -m"message" and git push
 

Problem:
    
    ! [rejected]        main -> main (non-fast-forward)
    
    error: failed to push some refs to 'https://research-git.uiowa.edu/npipatkittikul/learninggit.git'
    
    hint: Updates were rejected because the tip of your current branch is behind
    
    hint: its remote counterpart. If you want to integrate the remote changes,
    
    hint: use 'git pull' before pushing again.
    
    hint: See the 'Note about fast-forwards' in 'git push --help' for details.

what happens:

    - You made commits to your local main branch
    
    - In the meantime, new commits were pushed to the remote main branch by someone else
    
    - Your local main branch now has diverged from the remote main branch
    
solution:

    1) git fetch origin main

    2) git merge origin main

    3) git push


    
