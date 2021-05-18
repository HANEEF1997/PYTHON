# Random Moudule


```python
import random
```


```python
x = random.randint(1,5)
print(x)
```

    3
    


```python
y = random.random() # the range is between 0 -1
print(y*10) # if we multiply with any number we get from that range 
```

    8.279823646779725
    


```python
# example calculating your love score 

love_score = random.randint(1,100)
print(f'your love score is {love_score}')
```

    your love score is 12
    

###  write a program to flip a coin to toss


```python
coin = random.randint(0,1)
if coin == 0:
    print("Heads")
else:
    print("Tails")
```

    Tails
    


```python
## LIST
```


```python
country_names = ['India','USA','America','Pakistan']
```


```python
print(country_names[0])
print(country_names[-1])
```

    India
    Pakistan
    


```python
print(country_names[0:2])
```

    ['India', 'USA']
    


```python
country_names[1] = 'United State America'
```


```python
country_names
```




    ['India', 'United State America', 'America', 'Pakistan']



### example
#### Who's Paying
Instructions
You are going to write a program which will select a random name from a list of names. The person selected will have to pay for everybody's food bill.

Example Input

```
Angela, Ben, Jenny, Michael, Chloe
```
Note: notice that there is a space between the comma and the next name.  

Example Output

```
Michael is going to buy the meal today!


```python
# Split string method
names_string = input("Give me everybody's names, separated by a comma. ")
names = names_string.split(", ")
# 🚨 Don't change the code above 👆

import random 

random_choice = random.randint(0,len(names)-1)
random_names = names[random_choice]
print(f"{random_names} is going to buy the meal today!")
```

    Give me everybody's names, separated by a comma. Angela, Ben, Jenny, Michael, Chloe
    Ben is going to buy the meal today!
    

#### Nested List


```python
fruits = ['banana','apple','mango','grapes']
vegetables = ['Tomatoes','Potatoes','Pears']
```


```python
nested_list = [fruits,vegetables]
```


```python
print(nested_list)
```

    [['banana', 'apple', 'mango', 'grapes'], ['Tomatoes', 'Potatoes', 'Pears']]
    


```python
nested_list[1][1]
```




    'Potatoes'




```python
nested_list[0][1]
```




    'apple'



### Treasure Map

You are going to write a program which will mark a spot with an X.

In the starting code, you will find a variable called map.

This map contains a nested list. When map is printed this is what the nested list looks like:

['⬜️', '⬜️', '⬜️'],['⬜️', '⬜️', '⬜️'],['⬜️', '⬜️', '⬜️']
['⬜️', '⬜️', '⬜️'],['⬜️', '⬜️', '⬜️'],['⬜️', '⬜️', '⬜️']
In the starting code, we have used new lines (\n) to format the three rows into a square, like this:

['⬜️', '⬜️', '⬜️']

['⬜️', '⬜️', '⬜️']

['⬜️', '⬜️', '⬜️']

This is to try and simulate the coordinates on a real map.



Your job is to write a program that allows you to mark a square on the map using a two-digit system. The first digit is the vertical column number and the second digit is the horizontal row number. e.g.:


```python
# 🚨 Don't change the code below 👇
row1 = ["⬜️","⬜️","⬜️"]
row2 = ["⬜️","⬜️","⬜️"]
row3 = ["⬜️","⬜️","⬜️"]
map = [row1, row2, row3]
print(f"{row1}\n{row2}\n{row3}")
position = input("Where do you want to put the treasure? ")
# 🚨 Don't change the code above 👆

#Write your code below this row 👇

horizontal = int(position[0])
vertical = int(position[1])

map[vertical - 1][horizontal - 1] = 'SH'
#Write your code above this row 👆

# 🚨 Don't change the code below 👇
print(f"{row1}\n{row2}\n{row3}")
```

    ['⬜️', '⬜️', '⬜️']
    ['⬜️', '⬜️', '⬜️']
    ['⬜️', '⬜️', '⬜️']
    Where do you want to put the treasure? 12
    ['⬜️', '⬜️', '⬜️']
    ['SH', '⬜️', '⬜️']
    ['⬜️', '⬜️', '⬜️']
    

# Rock Paper Scissors
Rock Paper Scissors is a zero sum game that is usually played by two people using their hands and no tools. The idea is to make shapes with an outstretched hand where each shape will have a certain degree of power and will lead to an outcome.

now more https://www.wrpsa.com/the-official-rules-of-rock-paper-scissors/

### What are the rules of RPS?
Although the game has a lot of complexity to it, the rules to play it are pretty simple.
The game is played where players deliver hand signals that will represent the elements of the game; rock, paper and scissors. The outcome of the game is determined by 3 simple rules:

* Rock wins against scissors.
* Scissors win against paper.
* Paper wins against rock.


```python
import random

rock = '''
    _______
---'   ____)
      (_____)
      (_____)
      (____)
---.__(___)
'''

paper = '''
    _______
---'   ____)____
          ______)
          _______)
         _______)
---.__________)
'''

scissors = '''
    _______
---'   ____)____
          ______)
       __________)
      (____)
---.__(___)
'''
game_images = [rock, paper, scissors]

user_choice = int(input("What do you choose? Type 0 for Rock, 1 for Paper or 2 for Scissors.\n"))
if user_choice >= 3 or user_choice < 0: 
    print("You typed an invalid number, you lose!") 
else:
    computer_choice = random.randint(0, 2)
    print("Computer chose:")
    print(game_images[computer_choice])


    if user_choice == 0 and computer_choice == 2:
        print("You win!")
    elif computer_choice == 0 and user_choice == 2:
        print("You lose")
    elif computer_choice > user_choice:
        print("You lose")
    elif user_choice > computer_choice:
        print("You win!")
    elif computer_choice == user_choice:
        print("It's a draw")
```

    What do you choose? Type 0 for Rock, 1 for Paper or 2 for Scissors.
    2
    Computer chose:
    
        _______
    ---'   ____)____
              ______)
              _______)
             _______)
    ---.__________)
    
    You win!
    


