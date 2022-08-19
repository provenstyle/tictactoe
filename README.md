# Tic Tac Toe with git

## Challenge #1 - Play against a single opponent

    #both players clone the repository
    git clone <repo uri>

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
    git push origin :game1

*** Challenge Complete ***

## Challenge #2 - a simple tournament

    #A referee will create a tournament branch from the main branch and push it to the server
    git checkout main
    git pull
    git checkout -b tournament1
    git push --set-upstream origin tournament1
    
    #each pair will play 2 games of tic tac toe as in Challenge #1 with the following modifications

    1. Checkout the tournament branch
    2. Create a seperate branch for each game.
    3. Copy _gameTemplate.txt for each game and name it <player1><player2>game<gameid>.txt
    4. Play your game as in Challenge #1
    5. Fill out who won the game
    6. Pull request your completed game into the tournament1 branch 
    7. The referee will review and approve your game
    8. Merge your game branch with the delete branch checkbox checked. 
    9. Start your next game. 
      

## Challenge #3 - moderate your own tournament

    #A referee will create a tournament branch from the main branch and push it to the server
    git checkout main
    git pull
    git checkout -b tournament1
    git push --set-upstream origin tournament1

    #each pair will play 2 games of tic tac toe as in Challenge #1 with the following modifications

    1. Checkout the tournament branch
    2. Create a seperate branch for each game.
    3. Play your game on _gameTemplate.txt
    4. Add your results to the _tournamanetResults.txt file on the tournament branch and push your changes
        1. The winners adds their name to the winner list
        2. The looser adds their name to the looser list
        3. If the cat wins add your team name to the cat list

        git checkout tournament1
        git add _tournamanetResults.txt
        git push

    5. Start your next game. 










