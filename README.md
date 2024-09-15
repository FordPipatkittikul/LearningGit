# Git terminology
## Stages
    working Directory
    
    Staging Area
    
    Local Repositroy
    
    Remote Repository.

![gitindex](https://github.com/FordPipatkittikul/LearningGit/assets/121902625/7d148ce8-73b6-49d9-a543-466ff028ad52)
## Basic command line for windows only

    cd <directory> : Change directory
    
    cd ~ : go to root directory
    
    cd .. : Change to previous directory

    echo "some message" >> <file>: Append some message to the file 

    del - fr <directory> : Remove directory
    
    del <file> : Remove file name
    
    start <directory> : open sepcific directory
    
    start .	 : open directory we are currently in
    
    mkdir <directory name> : Create a new directory
    
    ni <filename> : Create a new file

    rename <orignal name><name want to change>
    
    pwd : Print the path of the current directory

    clear : Clear the terminal window

    code . : open directory we are in as editor code
    
## basic git
    git add --all
    git commit -m "for Title" -m "for Description"
    git push
    git pull
    git status : checking working Directory, Staging Area
    
    git log : checking commit history

    git fetch : command that tells your local git to retrieve the latest meta-data info from the original

    git remote -v : lists all configured remote repositories for your local Git project, along with their corresponding URLs and any configured push/pull URLs.

## branch
    orign main refer tor main branch on remote rpo
    git branch <namebranch> : create branch.
    git branch -d <namebranch> : delete branch.
    git branch -a : list all the branches and check the current branch.
    git checkout <namebranch> : change to the branches you wanna work on.
    git checkout -b <namebranch> : create new branch and go that branch.
    git pull origin <namebranch>
    git push origin <namebranch>



    git remote add upstream https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git : To add a new remote repository to your local Git project
    git remote remove upstream
    git remote remove origin
    git pull upstream main : To pull everything from upstream repository to your local Git project

    git log --merge : list all the commits casuing conflict
## quick note on vs code merge conflict

    Accept current Change : accept what you currently have on your current branch
    Accept Incoming Change : accept what incoming from remote repo
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

    


    
