# Git stuff
Intro to git
    
    There are four phases in git: working Directory, Staging Area, Local Repositroy, Remote Repository.

Some useful command
    
    git status: checking working Directory, Staging Area
    
    git log: checking commit history

    git fetch:command that tells your local git to retrieve the latest meta-data info from the original

    

Git problem

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

    Probably someone has pushed to the main already, and your commit is behind. So every time making sure that your working directory is up to date

solution: 

    we have to fetch, merge the changeset, and then you'll be able to push again.

    1) git fetch origin mian

    2) git merge origin main  quick Note you probably have git merge conflict so go inside that file and fix it

    3) Now you can do git add --all which add all your files to staging area, git commit -m"message" and git push

2)

Problem:

what happens:

solution:


    
