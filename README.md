import random

print('Winning rules of the game ROCK PAPER SCISSORS are:\n'
    + 'Rock vs Paper -> Paper wins\n'
    + 'Rock vs Scissors -> Rock wins\n'
    + 'Paper vs Scissors -> Scissor wins\n'
    + 'Paper vs Rock -> Paper wins\n')

while True:
    print('Enter your choice:\n'
        + '1 - Rock\n'
        + '2 - Paper\n'
        + '3 - Scissors\n')
    choice = int(input('Enter your choice: '))
    
    while choice > 3 or choice < 1:
        choice = int(input('Enter a valid choice: '))
        
    choices = ['Rock', 'Paper', 'Scissors']
    choice_name = choices[choice - 1]
    
    print('User choice is:', choice_name)
    print('Now it\'s my Turn...')
    
    my_choice = random.choice(choices)
    print('here\'s my choice:', my_choice)
    print(choice_name, 'vs', my_choice)
    
    if choice_name == my_choice:
        print('It\'s a Draw!')
    elif (choice_name == 'Rock' and my_choice == 'Scissors') \
        or (choice_name == 'Paper' and my_choice == 'Rock') \
        or (choice_name == 'Scissors' and my_choice == 'Paper'):
        print('Congratulations! You Win!')
    else:
        print('Sorry! Computer Wins!')
        
    print('Do you want to play again? (Y/N)')
    ans = input().lower()
    if ans != 'y':
        break

print('Thanks for playing!')
