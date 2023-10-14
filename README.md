# Git stuff
Intro to git
    
    There are four phases in git: working Directory, Staging Area, Local Repositroy, Remote Repository.

Some useful command
    
    git status: checking working Directory, Staging Area
    
    git log: checking commit history

    git fetch:command that tells your local git to retrieve the latest meta-data info from the original

    

# Git problem

1) common one so far
   
Problem:

    ! [rejected]        main -> main (fetch first)
   
    error: failed to push some refs to 'your own git https'
   
    hint: Updates were rejected because the remote contains work that you do not
   
    hint: have locally. This is usually caused by another repository pushing to
   
    hint: the same ref. If you want to integrate the remote changes, use
   
    hint: 'git pull' before pushing again.
    
    hint: See the 'Note about fast-forwards' in 'git push --help' for details.

what happens:

    the remote main branch has progressed(ล่าช้า) since you last pulled from it, so Git won't allow you to push your changes and overwrite the remote history. 

solution: 

    we have to fetch, merge the changeset, and then you'll be able to push again.

    1) git fetch origin mian

    2) git merge origin main  quick Note you probably have git merge conflict  
        
        2.1) so go inside that file and delete

             <<<<<<< HEAD

             =======
             
             >>>>>>> origin

    3) Now you can do git add --all which add all your files to staging area, git commit -m"message" and git push

2) similar to first one

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


    
