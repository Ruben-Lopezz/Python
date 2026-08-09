Python
 
Este es mi recorrido diario y mi progreso aprendiendo Python.
 
Day 1 of Code
 
<pre><code>
print("Welcome to the Band Name Generator.")
city = input("Which city did you grow up in?\n")
pet = input("What is the name of a pet?\n")
print("Your band name could be " + city + " " + pet)
</code></pre>
 
Day 2 of Code
 
<pre><code>
print("Welcome to the tip calculator!")
bill = float(input("What was the total bill? $"))
tip = int(input("What percentage tip would you like to give? 10, 12, or 15? "))
people = int(input("How many people to split the bill? "))
 
tip_as_percent = tip / 100
total_tip_amount = bill * tip_as_percent
total_bill = bill + total_tip_amount
bill_per_person = total_bill / people
final_amount = round(bill_per_person, 2)
 
print(f"Each person should pay: ${final_amount}")
</code></pre>
 
Day 3 of Code
 
<pre><code>
print(r'''
*******************************************************************************
|                                                                              |
|________________.=""_;=.______________|_____________________|_______        |
|             ,-"_,="" `"=.|                                                  |
|___________________|__"=._o`"-._ `"=.______________|___________________     |
|        `"=._o`"=._ _`"=._                                                   |
|_____________________:=._o "=._."_.-="'"=.__________________|_______        |
|   __.--" , ; `"=._o." ,-"""-._ ".                                           |
|___________________|._" ,. .` ` `` , `"-._"-._ ". '__|___________________   |
|o`"=._` , "` `; .". , "-._"-._; ;                                            |
|___________| ;`-.o`"=._; ." ` '`."\ ` . "-._ /_______________|_______        |
|o ; `"-.o`"=._`` '` " ,__.--o;                                               |
|___________________|_| ; (#) `-.o `"=.`_.--"_o.-; ;___|___________________  |
*******************************************************************************
''')
 
print("Welcome to Treasure Island.")
print("Your mission is to find the treasure.")
 
choice1 = input('You\'re at a crossroad, where do you want to go? '
                 'Type "left" or "right".\n').lower()
 
if choice1 == "left":
    choice2 = input('You\'ve come to a lake. '
                     'There is an island in the middle of the lake. '
                     'Type "wait" to wait for a boat. '
                     'Type "swim" to swim across.\n').lower()
    if choice2 == "wait":
        choice3 = input("You arrive at the island unharmed. "
                         "There is house with 3 doors. One red, "
                         "one yellow and one blue. "
                         "Which colour do you choose?\n").lower()
        if choice3 == "red":
            print("It's a room full of fire. Game Over")
        elif choice3 == "yellow":
            print("You found the treasure. You Win!")
        elif choice3 == "blue":
            print("You enter a room of beasts. Game Over.")
        else:
            print("You chose a door that doesn't exist. Game Over.")
    else:
        print("You got attacked by an angry trout. Game Over.")
else:
    print("You fell in to a hole. Game Over.")
</code></pre>
 
Day 4 of Code
 
<pre><code>
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
 
if user_choice &gt;= 0 and user_choice &lt;= 2:
    print(game_images[user_choice])
 
computer_choice = random.randint(0, 2)
print("Computer chose:")
print(game_images[computer_choice])
 
if user_choice &gt;= 3 or user_choice &lt; 0:
    print("You typed an invalid number. You lose!")
elif user_choice == 0 and computer_choice == 2:
    print("You win!")
elif computer_choice == 0 and user_choice == 2:
    print("You lose!")
elif computer_choice &gt; user_choice:
    print("You lose!")
elif user_choice &gt; computer_choice:
    print("You win!")
elif computer_choice == user_choice:
    print("It's a draw!")
</code></pre>
 
Day 5 of Code
 
<pre><code>
import random
 
letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm',
           'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z',
           'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M',
           'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
numbers = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
symbols = ['!', '#', '$', '%', '&amp;', '(', ')', '*', '+']
 
print("Welcome to the PyPassword Generator!")
nr_letters = int(input("How many letters would you like in your password?\n"))
nr_symbols = int(input("How many symbols would you like?\n"))
nr_numbers = int(input("How many numbers would you like?\n"))
 
# First attempt: build the password directly from random characters
password = ""
for char in range(0, nr_letters):
    password += random.choice(letters)
for char in range(0, nr_symbols):
    password += random.choice(symbols)
for char in range(0, nr_numbers):
    password += random.choice(numbers)
print(password)
 
# Improved version: shuffle the characters for extra randomness
password_list = []
for char in range(0, nr_letters):
    password_list.append(random.choice(letters))
for char in range(0, nr_symbols):
    password_list.append(random.choice(symbols))
for char in range(0, nr_numbers):
    password_list.append(random.choice(numbers))
 
print(password_list)
random.shuffle(password_list)
print(password_list)
 
password = ""
for char in password_list:
    password += char
 
print(f"Your password is: {password}")
</code></pre>
 
Day 6 of Code
 
<pre><code>
def my_function():
    print("Hello")
    print("Bye")
 
 
my_function()
</code></pre>
 
Day 7 of Code
 
<pre><code>
import random
 
word_list = ["aardvark", "baboon", "camel"]
chosen_word = random.choice(word_list)
print(chosen_word)
 
guess = input("Guess a letter: ").lower()
 
for letter in chosen_word:
    if letter == guess:
        print("Right")
    else:
        print("Wrong")
</code></pre>
 
Day 8 of Code
 
<pre><code>
import art
 
print(art.logo)
 
alphabet = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm',
            'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z']
 
 
def caesar(original_text, shift_amount, encode_or_decode):
    output_text = ""
    if encode_or_decode == "decode":
        shift_amount *= -1
 
    for letter in original_text:
        if letter not in alphabet:
            output_text += letter
        else:
            shifted_position = alphabet.index(letter) + shift_amount
            shifted_position %= len(alphabet)
            output_text += alphabet[shifted_position]
    print(f"Here is the {encode_or_decode}d result: {output_text}")
 
 
should_continue = True
 
while should_continue:
    direction = input("Type 'encode' to encrypt, type 'decode' to decrypt:\n").lower()
    text = input("Type your message:\n").lower()
    shift = int(input("Type the shift number:\n"))
 
    caesar(original_text=text, shift_amount=shift, encode_or_decode=direction)
 
    restart = input("Type 'yes' if you want to go again. Otherwise, type 'no'.\n").lower()
    if restart == "no":
        should_continue = False
        print("Goodbye")
</code></pre>
 
Day 9 of Code
 
<pre><code>
from art import logo
print(logo)
 
 
def find_highest_bidder(bidding_record):
    highest_bid = 0
    winner = ""
    for bidder in bidding_record:
        bid_amount = bidding_record[bidder]
        if bid_amount &gt; highest_bid:
            highest_bid = bid_amount
            winner = bidder
    print(f"The winner is {winner} with a bid of ${highest_bid}")
 
 
bids = {}
continue_bidding = True
while continue_bidding:
    name = input("What is your name?: ")
    price = int(input("What is your bid?: $"))
    bids[name] = price
    should_continue = input("Are there any other bidders? Type 'yes or 'no'.\n")
    if should_continue == "no":
        continue_bidding = False
        find_highest_bidder(bids)
    elif should_continue == "yes":
        print("\n" * 20)
</code></pre>
 
Day 10 of Code
 
<pre><code>
import art
 
 
def add(n1, n2):
    return n1 + n2
 
 
def subtract(n1, n2):
    return n1 - n2
 
 
def multiply(n1, n2):
    return n1 * n2
 
 
def divide(n1, n2):
    return n1 / n2
 
 
operations = {
    "+": add,
    "-": subtract,
    "*": multiply,
    "/": divide,
}
 
 
def calculator():
    print(art.logo)
    should_accumulate = True
    num1 = float(input("What is the first number?: "))
 
    while should_accumulate:
        for symbol in operations:
            print(symbol)
        operation_symbol = input("Pick an operation: ")
        num2 = float(input("What is the next number?: "))
        answer = operations[operation_symbol](num1, num2)
        print(f"{num1} {operation_symbol} {num2} = {answer}")
 
        choice = input(f"Type 'y' to continue calculating with {answer}, or type 'n' to start a new calculation: ")
 
        if choice == "y":
            num1 = answer
        else:
            should_accumulate = False
            print("\n" * 20)
            calculator()
 
 
calculator()
</code></pre>
 
Day 11 of Code
 
<pre><code>
import random
from art import logo
 
 
def deal_card():
    """Returns a random card from the deck"""
    cards = [11, 2, 3, 4, 5, 6, 7, 8, 9, 10, 10, 10, 10]
    card = random.choice(cards)
    return card
 
 
def calculate_score(cards):
    """Take a list of cards and return the score calculated from the cards"""
    if sum(cards) == 21 and len(cards) == 2:
        return 0
 
    if 11 in cards and sum(cards) &gt; 21:
        cards.remove(11)
        cards.append(1)
 
    return sum(cards)
 
 
def compare(u_score, c_score):
    """Compares the user score u_score against the computer score c_score."""
    if u_score == c_score:
        return "Draw 🙃"
    elif c_score == 0:
        return "Lose, opponent has Blackjack 😱"
    elif u_score == 0:
        return "Win with a Blackjack 😎"
    elif u_score &gt; 21:
        return "You went over. You lose 😭"
    elif c_score &gt; 21:
        return "Opponent went over. You win 😁"
    elif u_score &gt; c_score:
        return "You win 😃"
    else:
        return "You lose 😤"
 
 
def play_game():
    print(logo)
    user_cards = []
    computer_cards = []
    computer_score = -1
    user_score = -1
    is_game_over = False
 
    for _ in range(2):
        user_cards.append(deal_card())
        computer_cards.append(deal_card())
 
    while not is_game_over:
        user_score = calculate_score(user_cards)
        computer_score = calculate_score(computer_cards)
        print(f"Your cards: {user_cards}, current score: {user_score}")
        print(f"Computer's first card: {computer_cards[0]}")
 
        if user_score == 0 or computer_score == 0 or user_score &gt; 21:
            is_game_over = True
        else:
            user_should_deal = input("Type 'y' to get another card, type 'n' to pass: ")
            if user_should_deal == "y":
                user_cards.append(deal_card())
            else:
                is_game_over = True
 
    while computer_score != 0 and computer_score &lt; 17:
        computer_cards.append(deal_card())
        computer_score = calculate_score(computer_cards)
 
    print(f"Your final hand: {user_cards}, final score: {user_score}")
    print(f"Computer's final hand: {computer_cards}, final score: {computer_score}")
    print(compare(user_score, computer_score))
 
 
while input("Do you want to play a game of Blackjack? Type 'y' or 'n': ") == "y":
    print("\n" * 20)
    play_game()
</code></pre>
 
Day 12 of Code
 
<pre><code>
from random import randint
from art import logo
 
EASY_LEVEL_TURNS = 10
HARD_LEVEL_TURNS = 5
 
 
def check_answer(user_guess, actual_answer, turns):
    if user_guess &gt; actual_answer:
        print("Too high.")
        return turns - 1
    elif user_guess &lt; actual_answer:
        print("Too low.")
        return turns - 1
    else:
        print(f"You got it! The answer was {actual_answer}")
 
 
def set_difficulty():
    level = input("Choose a difficulty. Type 'easy' or 'hard': ")
    if level == "easy":
        return EASY_LEVEL_TURNS
    else:
        return HARD_LEVEL_TURNS
 
 
def game():
    print(logo)
    print("Welcome to the Number Guessing Game!")
    print("I'm thinking of a number between 1 and 100.")
    answer = randint(1, 100)
    print(f"Pssst, the correct answer is {answer}")
 
    turns = set_difficulty()
 
    guess = 0
    while guess != answer:
        print(f"You have {turns} attempts remaining to guess the number.")
        guess = int(input("Make a guess: "))
        turns = check_answer(guess, answer, turns)
        if turns == 0:
            print("You've run out of guesses, you lose.")
            return
        elif guess != answer:
            print("Guess again.")
 
 
game()
</code></pre>
 
Day 13 of Code
 
<pre><code>
import random
import maths
 
 
def mutate(a_list):
    b_list = []
    new_item = 0
    for item in a_list:
        new_item = item * 2
        new_item += random.randint(1, 3)
        new_item = maths.add(new_item, item)
        b_list.append(new_item)
    print(b_list)
 
 
mutate([1, 2, 3, 5, 8, 13])
</code></pre>
 
Day 14 of Code
 
<pre><code>
from art import logo, vs
from game_data import data
import random
 
 
def format_data(account):
    account_name = account["name"]
    account_descr = account["description"]
    account_country = account["country"]
    return f"{account_name}, a {account_descr}, from {account_country}"
 
 
def check_answer(user_guess, a_followers, b_followers):
    if a_followers &gt; b_followers:
        return user_guess == "a"
    else:
        return user_guess == "b"
 
 
print(logo)
score = 0
game_should_continue = True
 
account_b = random.choice(data)
 
while game_should_continue:
    account_a = account_b
    account_b = random.choice(data)
 
    if account_a == account_b:
        account_b = random.choice(data)
 
    print(f"Compare A: {format_data(account_a)}.")
    print(vs)
    print(f"Against B: {format_data(account_b)}.")
 
    guess = input("Who has more followers? Type 'A' or 'B': ").lower()
 
    print("\n" * 20)
    print(logo)
 
    a_follower_count = account_a["follower_count"]
    b_follower_count = account_b["follower_count"]
 
    is_correct = check_answer(guess, a_follower_count, b_follower_count)
 
    if is_correct:
        score += 1
        print(f"You're right! Current score {score}")
    else:
        print(f"Sorry, that's wrong. Final score: {score}.")
        game_should_continue = False
</code></pre>
 
Day 15 of Code
 
<pre><code>
MENU = {
    "espresso": {
        "ingredients": {
            "water": 50,
            "coffee": 18,
        },
        "cost": 1.5,
    },
    "latte": {
        "ingredients": {
            "water": 200,
            "milk": 150,
            "coffee": 24,
        },
        "cost": 2.5,
    },
    "cappuccino": {
        "ingredients": {
            "water": 250,
            "milk": 100,
            "coffee": 24,
        },
        "cost": 3.0,
    }
}
 
profit = 0
resources = {
    "water": 300,
    "milk": 200,
    "coffee": 100,
}
 
 
def is_resource_sufficient(order_ingredients):
    for item in order_ingredients:
        if order_ingredients[item] &gt; resources[item]:
            print(f"Sorry there is not enough {item}.")
            return False
    return True
 
 
def process_coins():
    print("Please insert coins.")
    total = int(input("how many quarters?: ")) * 0.25
    total += int(input("how many dimes?: ")) * 0.1
    total += int(input("how many nickles?: ")) * 0.05
    total += int(input("how many pennies?: ")) * 0.01
    return total
 
 
def is_transaction_successful(money_received, drink_cost):
    if money_received &gt;= drink_cost:
        change = round(money_received - drink_cost, 2)
        print(f"Here is ${change} in change.")
        global profit
        profit += drink_cost
        return True
    else:
        print("Sorry that's not enough money. Money refunded.")
        return False
 
 
def make_coffee(drink_name, order_ingredients):
    for item in order_ingredients:
        resources[item] -= order_ingredients[item]
    print(f"Here is your {drink_name} ☕️. Enjoy!")
 
 
is_on = True
 
while is_on:
    choice = input("What would you like? (espresso/latte/cappuccino): ")
    if choice == "off":
        is_on = False
    elif choice == "report":
        print(f"Water: {resources['water']}ml")
        print(f"Milk: {resources['milk']}ml")
        print(f"Coffee: {resources['coffee']}g")
        print(f"Money: ${profit}")
    else:
        drink = MENU[choice]
        if is_resource_sufficient(drink["ingredients"]):
            payment = process_coins()
            if is_transaction_successful(payment, drink["cost"]):
                make_coffee(choice, drink["ingredients"])
</code></pre>
 
Day 16 of Code
 
<pre><code>
class MoneyMachine:
 
    CURRENCY = "$"
 
    COIN_VALUES = {
        "quarters": 0.25,
        "dimes": 0.10,
        "nickles": 0.05,
        "pennies": 0.01,
    }
 
    def __init__(self):
        self.profit = 0
        self.money_received = 0
 
    def report(self):
        """Prints the current profit"""
        print(f"Money: {self.CURRENCY}{self.profit}")
 
    def process_coins(self):
        """Returns the total calculated from coins inserted."""
        print("Please insert coins.")
        for coin in self.COIN_VALUES:
            self.money_received += int(input(f"How many {coin}?: ")) * self.COIN_VALUES[coin]
        return self.money_received
 
    def make_payment(self, cost):
        """Returns True when payment is accepted, or False if insufficient."""
        self.process_coins()
        if self.money_received &gt;= cost:
            change = round(self.money_received - cost, 2)
            print(f"Here is {self.CURRENCY}{change} in change.")
            self.profit += cost
            self.money_received = 0
            return True
        else:
            print("Sorry that's not enough money. Money refunded.")
            self.money_received = 0
            return False
</code></pre>
 
Day 17 of Code
 
<pre><code>
class QuizBrain:
    """Models the logic engine that runs the quiz."""
 
    def __init__(self, q_list):
        self.question_number = 0
        self.score = 0
        self.question_list = q_list
        self.current_question = None
 
    def still_has_questions(self):
        """Returns True if there are still questions left in the question list."""
        return self.question_number &lt; len(self.question_list)
 
    def next_question(self):
        """Displays the next question and gets the user's answer."""
        self.current_question = self.question_list[self.question_number]
        self.question_number += 1
        user_answer = input(f"Q.{self.question_number}: {self.current_question.text} (True/False)?: ")
        self.check_answer(user_answer)
 
    def check_answer(self, user_answer):
        """Checks the user's answer against the correct answer and updates the score."""
        correct_answer = self.current_question.answer
        if user_answer.lower() == correct_answer.lower():
            self.score += 1
            print("You got it right!")
        else:
            print("That's wrong.")
        print(f"The correct answer was: {correct_answer}.")
        print(f"Your current score is: {self.score}/{self.question_number}")
        print("\n")
</code></pre>
 
Day 18 of Code
 
<pre><code>
import turtle as turtle_module
import random
 
turtle_module.colormode(255)
 
 
def random_color():
    r = random.randint(0, 255)
    g = random.randint(0, 255)
    b = random.randint(0, 255)
    return (r, g, b)
 
 
color_list = [
    (237, 28, 36), (255, 127, 39), (255, 242, 0), (34, 177, 76),
    (0, 162, 232), (63, 72, 204), (163, 73, 164), (255, 174, 201),
    (181, 230, 29), (0, 0, 0), (255, 255, 255), (185, 122, 87),
]
 
timmy = turtle_module.Turtle()
timmy.speed("fastest")
timmy.penup()
timmy.hideturtle()
 
screen = turtle_module.Screen()
screen.colormode(255)
 
number_of_dots = 100
starting_x = -225
starting_y = -225
 
timmy.setpos(starting_x, starting_y)
 
for dot_count in range(1, number_of_dots + 1):
    timmy.dot(20, random.choice(color_list))
    timmy.forward(50)
 
    if dot_count % 10 == 0:
        timmy.sety(timmy.ycor() + 50)
        timmy.setx(starting_x)
 
screen.exitonclick()
</code></pre>
 
Day 19 of Code
 
<pre><code>
import turtle as turtle_module
import random
 
screen = turtle_module.Screen()
screen.setup(width=500, height=400)
user_bet = screen.textinput(title="Make your bet", prompt="Which turtle will win the race? Enter a color: ")
 
colors = ["red", "orange", "yellow", "green", "blue", "purple"]
y_positions = [-70, -40, -10, 20, 50, 80]
all_turtles = []
 
for turtle_index in range(0, 6):
    new_turtle = turtle_module.Turtle(shape="turtle")
    new_turtle.color(colors[turtle_index])
    new_turtle.penup()
    new_turtle.goto(x=-230, y=y_positions[turtle_index])
    all_turtles.append(new_turtle)
 
is_race_on = False
if user_bet:
    is_race_on = True
 
while is_race_on:
    for racing_turtle in all_turtles:
        if racing_turtle.xcor() &gt; 230:
            is_race_on = False
            winning_color = racing_turtle.pencolor()
            if winning_color == user_bet:
                print(f"You've won! The {winning_color} turtle is the winner!")
            else:
                print(f"You've lost! The {winning_color} turtle is the winner!")
            break
 
        random_distance = random.randint(0, 10)
        racing_turtle.forward(random_distance)
 
screen.exitonclick()
</code></pre>

Day 20 of Code
 
<pre><code>
from turtle import Turtle
 
STARTING_POSITIONS = [(0, 0), (-20, 0), (-40, 0)]
MOVE_DISTANCE = 20
UP = 90
DOWN = 270
LEFT = 180
RIGHT = 0
 
 
class Snake:
 
    def __init__(self):
        self.segments = []
        self.create_snake()
        self.head = self.segments[0]
 
    def create_snake(self):
        for position in STARTING_POSITIONS:
            self.add_segment(position)
 
    def add_segment(self, position):
        new_segment = Turtle("square")
        new_segment.color("white")
        new_segment.penup()
        new_segment.goto(position)
        self.segments.append(new_segment)
 
    def move(self):
        for seg_num in range(len(self.segments) - 1, 0, -1):
            new_x = self.segments[seg_num - 1].xcor()
            new_y = self.segments[seg_num - 1].ycor()
            self.segments[seg_num].goto(new_x, new_y)
        self.head.forward(MOVE_DISTANCE)
 
    def up(self):
        if self.head.heading() != DOWN:
            self.head.setheading(UP)
 
    def down(self):
        if self.head.heading() != UP:
            self.head.setheading(DOWN)
 
    def left(self):
        if self.head.heading() != RIGHT:
            self.head.setheading(LEFT)
 
    def right(self):
        if self.head.heading() != LEFT:
            self.head.setheading(RIGHT)
</code></pre>
 
Project of learned things between the first 20 days
 
<pre><code>
MAX_BUDGET = 50.0
 
shopping_list = []
 
 
def add_product(name, price):
    shopping_list.append({"name": name, "price": price})
    print(f"'{name}' added for ${price}.")
 
 
def remove_product(name):
    for product in shopping_list:
        if product["name"].lower() == name.lower():
            shopping_list.remove(product)
            print(f"'{name}' removed.")
            return
    print(f"Could not find '{name}'.")
 
 
def calculate_total():
    total = 0
    for product in shopping_list:
        total += product["price"]
    return total
 
 
def show_list():
    if len(shopping_list) == 0:
        print("The shopping list is empty.")
        return
    print("\n--- Shopping List ---")
    for product in shopping_list:
        print(f"- {product['name']}: ${product['price']}")
 
 
print("Shopping List Manager")
print("Options: add / remove / view / exit")
 
program_active = True
 
while program_active:
    choice = input("\nWhat would you like to do?: ").lower()
 
    if choice == "add":
        name = input("Product name: ")
        price = float(input("Price: "))
        add_product(name, price)
 
    elif choice == "remove":
        name = input("Which product to remove?: ")
        remove_product(name)
 
    elif choice == "view":
        show_list()
        total = calculate_total()
        print(f"Total: ${round(total, 2)}")
        if total > MAX_BUDGET:
            print("⚠️ You've gone over budget.")
 
    elif choice == "exit":
        program_active = False
        print("Goodbye!")
 
    else:
        print("Invalid option.")
</code></pre>

Day 21 of Code
<code><pre>
from turtle import Turtle

STARTING_POSITIONS = [(0, 0), (-20, 0), (-40, 0)]
MOVE_DISTANCE = 20
UP = 90
DOWN = 270
LEFT = 180
RIGHT = 0


class Snake:

    def __init__(self):
        self.segments = []
        self.create_snake()
        self.head = self.segments[0]

    def create_snake(self):
        for position in STARTING_POSITIONS:
            self.add_segment(position)

    def add_segment(self, position):
        new_segment = Turtle("square")
        new_segment.color("white")
        new_segment.penup()
        new_segment.goto(position)
        self.segments.append(new_segment)

    def extend(self):
        self.add_segment(self.segments[-1].position())

    def move(self):
        for seg_num in range(len(self.segments) - 1, 0, -1):
            new_x = self.segments[seg_num - 1].xcor()
            new_y = self.segments[seg_num - 1].ycor()
            self.segments[seg_num].goto(new_x, new_y)
        self.head.forward(MOVE_DISTANCE)

    def up(self):
        if self.head.heading() != DOWN:
            self.head.setheading(UP)

    def down(self):
        if self.head.heading() != UP:
            self.head.setheading(DOWN)

    def left(self):
        if self.head.heading() != RIGHT:
            self.head.setheading(LEFT)

    def right(self):
        if self.head.heading() != LEFT:
            self.head.setheading(RIGHT)

from turtle import Turtle
import random


class Food(Turtle):

    def __init__(self):
        super().__init__()
        self.shape("circle")
        self.penup()
        self.shapesize(stretch_len=0.5, stretch_wid=0.5)
        self.color("blue")
        self.speed("fastest")
        self.refresh()

    def refresh(self):
        random_x = random.randint(-280, 280)
        random_y = random.randint(-280, 280)
        self.goto(random_x, random_y)

from turtle import Turtle

ALIGNMENT = "center"
FONT = ("Courier", 24, "normal")


class Scoreboard(Turtle):

    def __init__(self):
        super().__init__()
        self.score = 0
        with open("data.txt") as data:
            self.high_score = int(data.read())
        self.color("white")
        self.penup()
        self.goto(0, 270)
        self.hideturtle()
        self.update_scoreboard()

    def update_scoreboard(self):
        self.clear()
        self.write(f"Score: {self.score}  High Score: {self.high_score}",
                    align=ALIGNMENT, font=FONT)

    def reset(self):
        if self.score > self.high_score:
            self.high_score = self.score
            with open("data.txt", mode="w") as data:
                data.write(f"{self.high_score}")
        self.score = 0
        self.update_scoreboard()

    def increase_score(self):
        self.score += 1
        self.update_scoreboard()

    def game_over(self):
        self.goto(0, 0)
        self.write("GAME OVER", align=ALIGNMENT, font=FONT)

from turtle import Screen
from snake import Snake
from food import Food
from scoreboard import Scoreboard
import time

screen = Screen()
screen.setup(width=600, height=600)
screen.bgcolor("black")
screen.title("Snake Game")
screen.tracer(0)

snake = Snake()
food = Food()
scoreboard = Scoreboard()

screen.listen()
screen.onkey(snake.up, "Up")
screen.onkey(snake.down, "Down")
screen.onkey(snake.left, "Left")
screen.onkey(snake.right, "Right")

game_is_on = True
while game_is_on:
    screen.update()
    time.sleep(0.1)

    snake.move()

    if snake.head.distance(food) < 15:
        food.refresh()
        snake.extend()
        scoreboard.increase_score()

    if (snake.head.xcor() > 280 or snake.head.xcor() < -280
            or snake.head.ycor() > 280 or snake.head.ycor() < -280):
        game_is_on = False
        scoreboard.game_over()

    for segment in snake.segments[1:]:
        if snake.head.distance(segment) < 10:
            game_is_on = False
            scoreboard.game_over()

screen.exitonclick()
</code></pre>

Day 22 of Code

<pre><code>
from turtle import Turtle
 
FONT = ("Courier", 80, "normal")
 
 
class Scoreboard(Turtle):
 
    def __init__(self):
        super().__init__()
        self.l_score = 0
        self.r_score = 0
        self.color("white")
        self.penup()
        self.hideturtle()
        self.update_scoreboard()
 
    def update_scoreboard(self):
        self.clear()
        self.goto(-100, 200)
        self.write(self.l_score, align="center", font=FONT)
        self.goto(100, 200)
        self.write(self.r_score, align="center", font=FONT)
 
    def l_point(self):
        self.l_score += 1
        self.update_scoreboard()
 
    def r_point(self):
        self.r_score += 1
        self.update_scoreboard()
</pre></pre>code>
 
Day 23 of Code
<pre><code>
from turtle import Turtle
 
FONT = ("Courier", 24, "normal")
 
 
class Scoreboard(Turtle):
 
    def __init__(self):
        super().__init__()
        self.level = 1
        self.color("black")
        self.penup()
        self.hideturtle()
        self.goto(-280, 250)
        self.update_scoreboard()
 
    def update_scoreboard(self):
        self.clear()
        self.write(f"Level: {self.level}", align="left", font=FONT)
 
    def increase_level(self):
        self.level += 1
        self.update_scoreboard()
 
    def game_over(self):
        self.goto(0, 0)
        self.write("GAME OVER", align="center", font=FONT)
</pre></pre>code>
 
Day 24 of Code
<pre><code>
with open("./Input/Names/invited_names.txt") as names_file:
    names = names_file.readlines()
    names = [name.strip() for name in names]

with open("./Input/Letters/starting_letter.txt") as letter_file:
    letter_contents = letter_file.read()

    for name in names:
        new_letter = letter_contents.replace("[name]", name)

        with open(f"./Output/ReadyToSend/letter_for_{name}.txt", mode="w") as completed_letter:
            completed_letter.write(new_letter)

print(f"Mail merge complete. Generated {len(names)} letters in ./Output/ReadyToSend/")
</pre></pre>code>

Day 25 of Code
<pre><code>
import turtle
import pandas
 
FONT = ("Arial", 10, "normal")
 
STATE_DATA = [
    ("Alabama", 100, -71), ("Alaska", -320, -190), ("Arizona", -189, -47),
    ("Arkansas", 36, -36), ("California", -279, 3), ("Colorado", -115, 34),
    ("Connecticut", 263, 78), ("Delaware", 231, 34), ("Florida", 151, -142),
    ("Georgia", 139, -74), ("Hawaii", -230, -190), ("Idaho", -220, 125),
    ("Illinois", 73, 51), ("Indiana", 106, 49), ("Iowa", 23, 85),
    ("Kansas", -33, 25), ("Kentucky", 118, 8), ("Louisiana", 40, -102),
    ("Maine", 303, 142), ("Maryland", 217, 34), ("Massachusetts", 273, 90),
    ("Michigan", 116, 124), ("Minnesota", 14, 157), ("Mississippi", 67, -73),
    ("Missouri", 35, 25), ("Montana", -163, 169), ("Nebraska", -50, 76),
    ("Nevada", -243, 39), ("New Hampshire", 275, 113), ("New Jersey", 240, 52),
    ("New Mexico", -122, -44), ("New York", 231, 100), ("North Carolina", 186, -25),
    ("North Dakota", -55, 178), ("Ohio", 146, 58), ("Oklahoma", -23, -24),
    ("Oregon", -288, 118), ("Pennsylvania", 206, 66), ("Rhode Island", 277, 80),
    ("South Carolina", 168, -52), ("South Dakota", -54, 125), ("Tennessee", 106, -19),
    ("Texas", -44, -93), ("Utah", -186, 39), ("Vermont", 263, 118),
    ("Virginia", 192, 8), ("Washington", -288, 176), ("West Virginia", 172, 27),
    ("Wisconsin", 65, 129), ("Wyoming", -138, 102),
]
 
data = pandas.DataFrame(STATE_DATA, columns=["state", "x", "y"])
all_states = data.state.to_list()
 
screen = turtle.Screen()
screen.title("U.S. States Game")
screen.setup(width=725, height=491)
 
writer = turtle.Turtle()
writer.hideturtle()
writer.penup()
 
guessed_states = []
 
while len(guessed_states) < 50:
    answer_state = screen.textinput(
        title=f"{len(guessed_states)}/50 States Correct",
        prompt="What's another state's name?"
    )
 
    if answer_state is None:
        break
 
    answer_state = answer_state.title()
 
    if answer_state == "Exit":
        missing_states = [state for state in all_states if state not in guessed_states]
        new_data = pandas.DataFrame(missing_states, columns=["State"])
        new_data.to_csv("states_to_learn.csv")
        break
 
    if answer_state in all_states and answer_state not in guessed_states:
        guessed_states.append(answer_state)
        state_row = data[data.state == answer_state]
        writer.goto(int(state_row.x.iloc[0]), int(state_row.y.iloc[0]))
        writer.write(answer_state, align="center", font=FONT)
 
screen.exitonclick()
</pre></pre>code>
