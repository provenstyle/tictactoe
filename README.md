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

    1. Checkout the tournament1 branch
    2. Create a seperate branch for each game.
    3. Play your game on _gameTemplate.txt
    4. Add your results to the _tournamanetResults.txt file on the tournament1 branch and push your changes
        1. The winners adds their name to the winner list
        2. The loser adds their name to the loser list
        3. If the cat wins add your team name to the cat list
    5. Start your next game. 

## Challenge #4 - rebase tournament 

    This challenge is the same as Challenge #3 with a focus on rebasing
    
    During step 4 when you add your results to the _tournamanetResults.txt file on the tournament1 branch and push your changes:
        1. git fetch --all --prune
        2. git checkout tournament1
        3. git pull --rebase
        4. Fix and merge conflicts
        5. The winners adds their name to the winner list
        6. The loser adds their name to the loser list
        7. If the cat wins add your team name to the cat list
        8. Push your changes to the server
        9. If you get and merge conflicts go to step 3 and repeat

        Rebase commands you may need:
        git pull   --rebase
        git rebase --continue
        git rebase --abort

    There should be no merge commits.
    Another way to say this is each commit only has one parent.
    Another way to say this is when I look at git lg or gitk there should be no merge lines in the graph


## Challenge #5 - Push Champion  

    This is an individual challenge.

    #A referee will create a tournament branch from the main branch and push it to the server

    1. Checkout the tournament branch
    2. Open the _pushChampion.txt file
    3. Add your name to highest place not taken. Commit. Push.
    4. If you get a merge conflict on your line resolve it taking the next available place and push again.
    5. The first person to successfully push their name to the server at a place claims it and you must take the next available place when you resolve your conflict.








