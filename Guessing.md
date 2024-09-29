#Guessing Game

##generate random number between 1 and 10
SECRET_NUMBER$(( RANDOM % 10 + 1))

# prompt first guess
echo "Guess the secret number between 1 and 10:"
read USER_GUESS

# loop to prompt user to guess until correct
until [[ $USER_GUESS == $SECRET_NUMBER ]]
do

# check guess is valid/an integer
if [[ ! $USER_GUESS =~ ^[0-9]+$ ]]
then
# request valid guess
echo -e "\nThat is not an integer, guess again:"
read USER_GUESS

#if its a valid guess
esle
# check inequalities and give hint
if [[ $USER_GUESS < $SECRET_NUMBER ]]
then
echo "It's higher than that, guess again:"
read USER_GUESS
else
echo "It's lower thatn that, guess again:"
read USER_GUESS
fi
fi

# winning message
echo You guessed it. The secret number was $SECRET_NUMBER. Nice job\!

