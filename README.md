# Git stuff
Intro to git
    
    There are four phases in git: working Directory, Staging Area, Local Repositroy, Remote Repository.

Some useful command
    
    git status: checking working Directory, Staging Area
    
    git log: checking commit history

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

2)

Problem:

what happens:

solution:


    
