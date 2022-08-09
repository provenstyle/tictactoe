# Tic Tac Toe with git

## Challenge #1 - Play against a single opponent

    #both players clone the repository
    git clone ssh://git@bitbucket.pearson.com/~vdudlmi/tictactoe.git 
    or
    git clone https://bitbucket.pearson.com/scm/~vdudlmi/tictactoe.git

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
    #Open the _gameTemplate.txt file
    #Make your first move by entering an X in one of the squares
    #Check in your move and push to the server
    git status
    git diff
    git add .
    git commit -m "Player1's first move"
    git push

    #Player 2
    #pull commits from the server
    git pull

    #Open the _gameTemplate.txt file
    #Make your first move by entering an O in one of the squares
    git status
    git diff
    git add .
    git commit -m "Player1's first move"
    git push

    #Each Player continue's this process until the game is over
    #pull commits from the server
    git pull

    #Open the _gameTemplate.txt file
    #Make your next move by entering an X or O in one of the squares
    git status
    git diff
    git add .
    git commit -m "Player1's first move"
    git push

    #Each player delete your local branch 
    git checkout main
    git branch -D game1

    #Player 1 delete your branch from the server
    git push origin : game1

*** Challenge Complete ***

## Challenge #2 - a simple tournament

    #A judge will create a tournament branch from the main branch and push it to the server
    git checkout -b tournament1
    git push --set-upstream origin tournament1
    
    #each pair will play best 2 out of 3 games of tic tac toe as in Challenge #1 with the following modifications

    1. Create a seperate branch for each game.
      git checkout -b michaelCraigGame1
    2. Copy _gameTemplate.txt for each game and name it <player1><player2>game<gameid>.txt
      git add .
      git commit -m "starting new game"
      git push --set-upstream origin michaelCraigGame1
    3. Play your game as in Challenge #1
    4. Fill out who won the game
    5. Pull request your completed game into the tournament1 branch before starting the next game
      

## Challenge #3 - moderate your own tournament










