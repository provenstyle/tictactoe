# Tic Tac Toe with git

## Git commands overview

    # clone a repository

    #
    git checkout -b myGame

    git push origin myGame

    git pull

    git pull --rebase

    git add .

    git add game1.txt

    git commit -m "x in the upper lefthand corner"

    git diff

    git push

## Challenge #1 - Play against a single opponent

    #both players clone the repository
    git clone git@github.com:provenstyle/tictactoe.git

    #change directories to the root of the repository
    cd tictactoe

    #Player 1 create a branch for your game
    git checkout -b game1

    #push your branch to the server
    git push --set-upstream origin game1

    #Player 2 checkout the branch for the game
    git fetch --all
    git checkout game1

    #Player 1
    #Open the game.txt file
    #Make your first move by entering a X in one of the squares
    #Check in your move and push to the server
    git status
    git diff
    git add .
    git commit -m "Player1's first move"
    git push

    #Player 2
    #pull commits from the server
    git pull

    #Open the game.txt file
    #Make your first move by entering an O in one of the squares
    git status
    git diff
    git add .
    git commit -m "Player1's first move"
    git push

    #Each Player continue this process untill the game is over
    #pull commits from the server
    git pull

    #Open the game.txt file
    #Make your next move by entering an X or O in one of the squares
    git status
    git diff
    git add .
    git commit -m "Player1's first move"
    git push