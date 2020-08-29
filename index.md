# GETTING STARTED WITH GUESSING GAME
## This is your guide to the game!
        
This Guess is purely written in bash and from scratch and utilize function, a loop and conditional statement
Here is souce code of the bash script which power this game
        
       
```
#!/usr/bin/env bash
#File: guessinggame.sh


echo "''''Guessing Game''''"
echo " Guess the number of directory in this $(pwd) directory "
read guess

function get_n {
        local number=$(ls -d */ | wc -l)
        echo $number
}

tdir=$(get_n)


while [[ $guess -ne $tdir ]]
    do

        if [[ $guess -gt $tdir ]]
            then 
                echo " Your guess is too High "
        else 
                echo " Your guess is too low "
    fi    
    
    echo
    echo "Try again"
    read guess
done

echo "Congratulation! You guessed the right number"
```
