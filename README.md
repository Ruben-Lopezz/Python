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
</pre></pre>
 
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

Day of Code 26 

<pre><code>import pandas

data = pandas.read_csv("nato_phonetic_alphabet.csv")

phonetic_dict = {
    row.letter: row.code
    for (index, row) in data.iterrows()
}

word = input("Enter a word: ").upper()

try:
    output_list = [
        phonetic_dict[letter]
        for letter in word
    ]
except KeyError:
    print("Sorry, only letters in the alphabet please.")
else:
    print(output_list)</pre></code>

Day of Code 27

<pre><code>from tkinter import *

# Window setup
window = Tk()
window.title("Miles to Km Converter")
window.minsize(width=300, height=150)
window.config(padx=20, pady=20)

# Convert miles to kilometers
def calculate():
    miles = float(miles_input.get())
    km = miles * 1.60934
    result_label.config(text=f"{km:.2f}")

# Input field
miles_input = Entry(width=10)
miles_input.grid(column=1, row=0)

# Labels
miles_label = Label(text="Miles")
miles_label.grid(column=2, row=0)

equal_label = Label(text="is equal to")
equal_label.grid(column=0, row=1)

result_label = Label(text="0")
result_label.grid(column=1, row=1)

km_label = Label(text="Km")
km_label.grid(column=2, row=1)

# Calculate button
calculate_button = Button(
    text="Calculate",
    command=calculate
)
calculate_button.grid(column=1, row=2)

window.mainloop()</code></pre>

Day of Code 28

<pre><code>import tkinter as tk

# ---------------------------- CONSTANTS ------------------------------- #
PINK = "#e2979c"
RED = "#e7305b"
GREEN = "#9bdeac"
YELLOW = "#f7f5dd"
FONT_NAME = "Courier"
WORK_MIN = 25
SHORT_BREAK_MIN = 5
LONG_BREAK_MIN = 20
reps = 0
timer = None

# ---------------------------- TIMER RESET ------------------------------- #
def reset_timer():
    global reps, timer

    if timer is not None:
        window.after_cancel(timer)
        timer = None

    reps = 0
    canvas.itemconfig(timer_text, text="00:00")
    title_label.config(text="Timer", fg=GREEN)
    check_marks.config(text="")

# ---------------------------- TIMER MECHANISM ------------------------------- #
def start_timer():
    global reps

    reps += 1

    work_seconds = WORK_MIN * 60
    short_break_seconds = SHORT_BREAK_MIN * 60
    long_break_seconds = LONG_BREAK_MIN * 60

    if reps % 8 == 0:
        count_down(long_break_seconds)
        title_label.config(text="Break", fg=RED)
    elif reps % 2 == 0:
        count_down(short_break_seconds)
        title_label.config(text="Break", fg=PINK)
    else:
        count_down(work_seconds)
        title_label.config(text="Work", fg=GREEN)

# ---------------------------- COUNTDOWN MECHANISM ------------------------------- #
def count_down(count):
    global timer

    minutes = count // 60
    seconds = count % 60

    canvas.itemconfig(
        timer_text,
        text=f"{minutes:02d}:{seconds:02d}"
    )

    if count > 0:
        timer = window.after(
            1000,
            count_down,
            count - 1
        )
    else:
        start_timer_button.config(state="normal")

        if reps % 2 == 1:
            check_marks.config(
                text=check_marks.cget("text") + "✓"
            )

        start_timer()


# ---------------------------- UI SETUP ------------------------------- #
window = tk.Tk()
window.title("Pomodoro")
window.config(padx=100, pady=50, bg=YELLOW)

title_label = tk.Label(
    text="Timer",
    fg=GREEN,
    bg=YELLOW,
    font=(FONT_NAME, 50)
)
title_label.grid(column=1, row=0)

canvas = tk.Canvas(
    width=200,
    height=224,
    bg=YELLOW,
    highlightthickness=0
)

# Simple timer illustration
canvas.create_oval(
    25, 25, 175, 175,
    fill=GREEN,
    outline=GREEN
)

timer_text = canvas.create_text(
    100, 100,
    text="00:00",
    fill="white",
    font=(FONT_NAME, 30, "bold")
)

canvas.grid(column=1, row=1)

start_timer_button = tk.Button(
    text="Start",
    command=lambda: [
        start_timer_button.config(state="disabled"),
        start_timer()
    ]
)
start_timer_button.grid(column=0, row=2)

reset_button = tk.Button(
    text="Reset",
    command=reset_timer
)
reset_button.grid(column=2, row=2)

check_marks = tk.Label(
    fg=GREEN,
    bg=YELLOW,
    font=(FONT_NAME, 16)
)
check_marks.grid(column=1, row=3)

window.mainloop()</code></pre>

Day 29 of Code

<pre><code>from tkinter import *
from tkinter import messagebox
from random import choice, randint, shuffle
import string

# ---------------------------- PASSWORD GENERATOR ------------------------------- #

def generate_password():
    letters = string.ascii_letters
    numbers = string.digits
    symbols = "!#$%&()*+"

    password_list = (
        [choice(letters) for _ in range(randint(8, 10))]
        + [choice(numbers) for _ in range(randint(2, 4))]
        + [choice(symbols) for _ in range(randint(2, 4))]
    )

    shuffle(password_list)
    password = "".join(password_list)

    password_entry.delete(0, END)
    password_entry.insert(0, password)

    # Copy generated password to clipboard
    window.clipboard_clear()
    window.clipboard_append(password)


# ---------------------------- SAVE PASSWORD ------------------------------- #

def save_password():
    website = website_entry.get().strip()
    email = email_entry.get().strip()
    password = password_entry.get().strip()

    if not website or not email or not password:
        messagebox.showwarning(
            title="Missing information",
            message="Please don't leave any fields empty!"
        )
        return

    is_ok = messagebox.askyesno(
        title="Confirm",
        message=f"Website: {website}\n"
                f"Email: {email}\n"
                f"Password: {password}\n\n"
                f"Is this information correct?"
    )

    if is_ok:
        try:
            with open("data.txt", "a", encoding="utf-8") as file:
                file.write(
                    f"{website} | {email} | {password}\n"
                )
        except OSError:
            messagebox.showerror(
                title="Error",
                message="Could not save the information."
            )
            return

        website_entry.delete(0, END)
        password_entry.delete(0, END)
        website_entry.focus()

        messagebox.showinfo(
            title="Success",
            message="Your information has been saved!"
        )


# ---------------------------- UI SETUP ------------------------------- #

window = Tk()
window.title("Password Manager")
window.config(padx=50, pady=50)

# Canvas / Logo
canvas = Canvas(width=200, height=200, highlightthickness=0)
canvas.grid(column=1, row=0)

# Simple lock illustration
canvas.create_oval(
    65, 25, 135, 95,
    outline="#333333",
    width=5
)
canvas.create_rectangle(
    50, 70, 150, 150,
    fill="#e7b34b",
    outline="#333333",
    width=3
)
canvas.create_oval(
    92, 92, 108, 108,
    fill="#333333"
)
canvas.create_rectangle(
    97, 103, 103, 123,
    fill="#333333",
    outline="#333333"
)

# Website
website_label = Label(text="Website:")
website_label.grid(column=0, row=1, sticky="w")

website_entry = Entry(width=35)
website_entry.grid(column=1, row=1, columnspan=2, sticky="w")
website_entry.focus()

# Email / Username
email_label = Label(text="Email/Username:")
email_label.grid(column=0, row=2, sticky="w")

email_entry = Entry(width=35)
email_entry.grid(column=1, row=2, columnspan=2, sticky="w")
email_entry.insert(0, "example@email.com")

# Password
password_label = Label(text="Password:")
password_label.grid(column=0, row=3, sticky="w")

password_entry = Entry(width=21)
password_entry.grid(column=1, row=3, sticky="w")

# Generate password button
generate_button = Button(
    text="Generate Password",
    command=generate_password
)
generate_button.grid(column=2, row=3, sticky="w")

# Add password button
add_button = Button(
    text="Add",
    width=30,
    command=save_password
)
add_button.grid(column=1, row=4, columnspan=2, sticky="w")

window.mainloop()</code></pre>

Day 30 of Code

<pre><code>from tkinter import *
from tkinter import messagebox
from random import choice, randint, shuffle
import string
import json

# ---------------------------- PASSWORD GENERATOR ------------------------------- #

def generate_password():
    letters = string.ascii_letters
    numbers = string.digits
    symbols = "!#$%&()*+"

    password_list = (
        [choice(letters) for _ in range(randint(8, 10))]
        + [choice(numbers) for _ in range(randint(2, 4))]
        + [choice(symbols) for _ in range(randint(2, 4))]
    )

    shuffle(password_list)
    password = "".join(password_list)

    password_entry.delete(0, END)
    password_entry.insert(0, password)

    window.clipboard_clear()
    window.clipboard_append(password)


# ---------------------------- SAVE PASSWORD ------------------------------- #

def save_password():
    website = website_entry.get().strip()
    email = email_entry.get().strip()
    password = password_entry.get().strip()

    if not website or not email or not password:
        messagebox.showwarning(
            title="Missing information",
            message="Please fill in all fields."
        )
        return

    new_data = {
        website: {
            "email": email,
            "password": password
        }
    }

    try:
        with open("data.json", "r", encoding="utf-8") as file:
            data = json.load(file)

    except FileNotFoundError:
        data = {}

    except json.JSONDecodeError:
        messagebox.showerror(
            title="Error",
            message="The data file is invalid. "
                    "Please check data.json before saving."
        )
        return

    # Update existing data or add a new website
    data.update(new_data)

    try:
        with open("data.json", "w", encoding="utf-8") as file:
            json.dump(data, file, indent=4)

    except OSError:
        messagebox.showerror(
            title="Error",
            message="Could not save your data."
        )
        return

    website_entry.delete(0, END)
    password_entry.delete(0, END)

    messagebox.showinfo(
        title="Success",
        message=f"Details saved for {website}."
    )


# ---------------------------- FIND PASSWORD ------------------------------- #

def find_password():
    website = website_entry.get().strip()

    if not website:
        messagebox.showwarning(
            title="Missing website",
            message="Please enter a website to search for."
        )
        return

    try:
        with open("data.json", "r", encoding="utf-8") as file:
            data = json.load(file)

    except FileNotFoundError:
        messagebox.showerror(
            title="No data",
            message="No saved passwords file was found."
        )
        return

    except json.JSONDecodeError:
        messagebox.showerror(
            title="Error",
            message="The data file contains invalid JSON."
        )
        return

    if website in data:
        details = data[website]

        messagebox.showinfo(
            title=website,
            message=(
                f"Email: {details['email']}\n"
                f"Password: {details['password']}"
            )
        )
    else:
        messagebox.showinfo(
            title="Not found",
            message=f"No details for {website} were found."
        )


# ---------------------------- UI SETUP ------------------------------- #

window = Tk()
window.title("Password Manager")
window.config(padx=40, pady=40)

# Logo
canvas = Canvas(width=180, height=180, highlightthickness=0)
canvas.grid(column=1, row=0)

canvas.create_oval(
    55, 20, 125, 90,
    outline="#333333",
    width=5
)
canvas.create_rectangle(
    40, 65, 140, 145,
    fill="#e7b34b",
    outline="#333333",
    width=3
)
canvas.create_oval(82, 88, 98, 104, fill="#333333")
canvas.create_rectangle(
    88, 101, 92, 122,
    fill="#333333"
)

# Website
Label(text="Website:").grid(
    column=0, row=1, sticky="w"
)

website_entry = Entry(width=22)
website_entry.grid(
    column=1, row=1, sticky="w"
)
website_entry.focus()

search_button = Button(
    text="Search",
    width=12,
    command=find_password
)
search_button.grid(column=2, row=1, sticky="w")

# Email
Label(text="Email/Username:").grid(
    column=0, row=2, sticky="w"
)

email_entry = Entry(width=38)
email_entry.grid(
    column=1, row=2, columnspan=2, sticky="w"
)
email_entry.insert(0, "example@email.com")

# Password
Label(text="Password:").grid(
    column=0, row=3, sticky="w"
)

password_entry = Entry(width=22)
password_entry.grid(
    column=1, row=3, sticky="w"
)

generate_button = Button(
    text="Generate Password",
    command=generate_password
)
generate_button.grid(
    column=2, row=3, sticky="w"
)

# Add button
add_button = Button(
    text="Add",
    width=33,
    command=save_password
)
add_button.grid(
    column=1, row=4, columnspan=2, sticky="w"
)

window.mainloop()</code></pre>

Day 31 of Code

<pre><code>
import tkinter as tk
import pandas as pd
import random
from pathlib import Path

# ---------------------------- CONSTANTS ------------------------------- #

BACKGROUND_COLOR = "#B1DDC6"
CARD_COLOR = "#FFFFFF"
TITLE_COLOR = "#2C3E50"

DATA_FILE = Path("french_words.csv")
PROGRESS_FILE = Path("words_to_learn.csv")

# Sample vocabulary created automatically if no CSV exists
SAMPLE_WORDS = [
    {"French": "partie", "English": "part"},
    {"French": "histoire", "English": "history"},
    {"French": "chercher", "English": "to look for"},
    {"French": "seulement", "English": "only"},
    {"French": "vraiment", "English": "really"},
    {"French": "apprendre", "English": "to learn"},
    {"French": "comprendre", "English": "to understand"},
    {"French": "toujours", "English": "always"},
    {"French": "ensemble", "English": "together"},
    {"French": "réponse", "English": "answer"},
    {"French": "question", "English": "question"},
    {"French": "maison", "English": "house"},
    {"French": "livre", "English": "book"},
    {"French": "eau", "English": "water"},
    {"French": "bonjour", "English": "hello"},
]

# ---------------------------- LOAD DATA ------------------------------- #

if not DATA_FILE.exists():
    pd.DataFrame(SAMPLE_WORDS).to_csv(DATA_FILE, index=False)

if PROGRESS_FILE.exists():
    try:
        data = pd.read_csv(PROGRESS_FILE).dropna()
        if not {"French", "English"}.issubset(data.columns):
            raise ValueError("Invalid vocabulary file")
    except (pd.errors.EmptyDataError, ValueError):
        data = pd.read_csv(DATA_FILE).dropna()
else:
    data = pd.read_csv(DATA_FILE).dropna()

data = data.reset_index(drop=True)
current_card = {}
flip_timer = None

# ---------------------------- NEXT CARD ------------------------------- #

def next_card():
    global current_card, flip_timer

    if flip_timer is not None:
        window.after_cancel(flip_timer)
        flip_timer = None

    if data.empty:
        canvas.config(bg=CARD_COLOR)
        canvas.delete("all")
        canvas.create_text(
            300, 150,
            text="Congratulations!\nYou learned all the words!",
            font=("Arial", 24, "bold"),
            fill=TITLE_COLOR,
            justify="center"
        )
        return

    current_card = data.iloc[random.randrange(len(data))].to_dict()

    canvas.config(bg=CARD_COLOR)
    canvas.delete("all")

    canvas.create_text(
        300, 60,
        text="French",
        font=("Arial", 24, "italic"),
        fill=TITLE_COLOR
    )

    canvas.create_text(
        300, 150,
        text=current_card["French"],
        font=("Arial", 38, "bold"),
        fill=TITLE_COLOR,
        width=500
    )

    flip_timer = window.after(3000, flip_card)

# ---------------------------- FLIP CARD ------------------------------- #

def flip_card():
    global flip_timer
    flip_timer = None

    canvas.config(bg="#91C8F0")
    canvas.delete("all")

    canvas.create_text(
        300, 60,
        text="English",
        font=("Arial", 24, "italic"),
        fill="white"
    )

    canvas.create_text(
        300, 150,
        text=current_card["English"],
        font=("Arial", 34, "bold"),
        fill="white",
        width=500
    )

# ---------------------------- KNOWN WORD ------------------------------- #

def known_word():
    global data

    if not current_card or data.empty:
        return

    # Remove the learned word from the remaining vocabulary
    data = data[
        data["French"] != current_card["French"]
    ].reset_index(drop=True)

    # Save progress so learned words won't appear again
    data.to_csv(PROGRESS_FILE, index=False)

    next_card()

# ---------------------------- UI SETUP ------------------------------- #

window = tk.Tk()
window.title("French Flash Cards")
window.config(bg=BACKGROUND_COLOR, padx=40, pady=30)

title_label = tk.Label(
    window,
    text="French Flash Cards",
    font=("Arial", 28, "bold"),
    bg=BACKGROUND_COLOR,
    fg=TITLE_COLOR
)
title_label.pack(pady=(0, 20))

canvas = tk.Canvas(
    width=600,
    height=300,
    bg=CARD_COLOR,
    highlightthickness=0
)
canvas.pack(pady=10)

button_frame = tk.Frame(window, bg=BACKGROUND_COLOR)
button_frame.pack(pady=20)

unknown_button = tk.Button(
    button_frame,
    text="❌ Don't Know",
    font=("Arial", 14),
    command=next_card,
    padx=15,
    pady=10
)
unknown_button.grid(row=0, column=0, padx=15)

known_button = tk.Button(
    button_frame,
    text="✅ I Know This",
    font=("Arial", 14),
    command=known_word,
    padx=15,
    pady=10
)
known_button.grid(row=0, column=1, padx=15)

next_card()

window.mainloop()
</code></pre>

Day 32 of Code

<pre><code>
import os
import csv
import random
import smtplib
from datetime import datetime
from pathlib import Path
from email.message import EmailMessage

# ---------------------------- SETTINGS ------------------------------- #

DATA_FILE = Path("birthdays.csv")

# Set these as environment variables before running the program.
MY_EMAIL = os.getenv("MY_EMAIL")
MY_PASSWORD = os.getenv("MY_PASSWORD")

SMTP_SERVER = "smtp.gmail.com"
SMTP_PORT = 465

# ---------------------------- EMAIL TEMPLATES ------------------------------- #

LETTER_TEMPLATES = [
    """Subject: Happy Birthday!

Dear [NAME],

Happy Birthday! 🎉

I hope your special day is full of happiness, laughter,
and wonderful memories.

Wishing you an amazing year ahead!

Best wishes,
Your Birthday Bot
""",
    """Subject: Wishing You a Wonderful Birthday!

Dear [NAME],

Many happy returns of the day!

May your birthday bring you lots of joy and success.
Have a fantastic celebration!

Best,
Your Birthday Bot
""",
    """Subject: It's Your Special Day!

Dear [NAME],

Happy Birthday! 🎂

I hope this new year of your life brings you exciting
opportunities, good health, and plenty of reasons to smile.

Enjoy your special day!

Warm wishes,
Your Birthday Bot
"""
]

# ---------------------------- CHECK BIRTHDAYS ------------------------------- #

def get_todays_birthdays():
    today = datetime.now()

    if not DATA_FILE.exists():
        print("Error: birthdays.csv was not found.")
        return []

    birthdays = []

    try:
        with DATA_FILE.open(
            "r", newline="", encoding="utf-8"
        ) as file:
            reader = csv.DictReader(file)

            required_columns = {"name", "email", "year", "month", "day"}

            if not required_columns.issubset(reader.fieldnames or []):
                print(
                    "Error: CSV needs these columns: "
                    "name, email, year, month, day"
                )
                return []

            for row in reader:
                try:
                    birthday_month = int(row["month"])
                    birthday_day = int(row["day"])

                    if (
                        birthday_month == today.month
                        and birthday_day == today.day
                    ):
                        birthdays.append(row)

                except (ValueError, TypeError):
                    print(f"Skipping invalid birthday entry: {row}")

    except OSError as error:
        print(f"Could not read birthday file: {error}")

    return birthdays

# ---------------------------- CREATE EMAIL ------------------------------- #

def create_birthday_email(name):
    template = random.choice(LETTER_TEMPLATES)

    subject, body = template.split("\n", 1)
    subject = subject.replace("Subject: ", "").strip()
    body = body.replace("[NAME]", name)

    message = EmailMessage()
    message["From"] = MY_EMAIL
    message["Subject"] = subject
    message.set_content(body)

    return message

# ---------------------------- SEND EMAIL ------------------------------- #

def send_birthday_email(person):
    if not MY_EMAIL or not MY_PASSWORD:
        print(
            "Email credentials are missing. "
            "Set MY_EMAIL and MY_PASSWORD first."
        )
        return False

    message = create_birthday_email(person["name"])
    message["To"] = person["email"]

    try:
        with smtplib.SMTP_SSL(
            SMTP_SERVER, SMTP_PORT, timeout=20
        ) as connection:
            connection.login(MY_EMAIL, MY_PASSWORD)
            connection.send_message(message)

        print(f"Birthday email sent to {person['name']}!")
        return True

    except (smtplib.SMTPException, OSError) as error:
        print(f"Could not email {person['name']}: {error}")
        return False

# ---------------------------- MAIN PROGRAM ------------------------------- #

def main():
    birthdays = get_todays_birthdays()

    if not birthdays:
        print("No birthdays found for today.")
        return

    for person in birthdays:
        send_birthday_email(person)

if __name__ == "__main__":
    main()
</code></pre>

Day of Code 33

<pre><code>
import os
import smtplib
import requests
from datetime import datetime
from email.message import EmailMessage
from time import sleep

# ---------------------------- YOUR LOCATION ---------------------------- #

MY_LAT = 28.1235       # Replace with your latitude
MY_LONG = -15.4363     # Replace with your longitude

# Email settings: configure these as environment variables
MY_EMAIL = os.getenv("MY_EMAIL")
MY_PASSWORD = os.getenv("MY_PASSWORD")

# ---------------------------- CHECK ISS POSITION ---------------------------- #

def iss_is_overhead():
    try:
        response = requests.get(
            "https://api.wheretheiss.at/v1/satellites/25544",
            timeout=10
        )
        response.raise_for_status()
        data = response.json()

        iss_latitude = float(data["latitude"])
        iss_longitude = float(data["longitude"])

        latitude_close = abs(iss_latitude - MY_LAT) <= 5
        longitude_close = abs(iss_longitude - MY_LONG) <= 5

        return latitude_close and longitude_close

    except (requests.RequestException, KeyError, ValueError) as error:
        print("Could not retrieve ISS position:", error)
        return False


# ---------------------------- CHECK NIGHTTIME ---------------------------- #

def is_night():
    parameters = {
        "lat": MY_LAT,
        "lng": MY_LONG,
        "formatted": 0
    }

    try:
        response = requests.get(
            "https://api.sunrise-sunset.org/json",
            params=parameters,
            timeout=10
        )
        response.raise_for_status()
        data = response.json()

        if data.get("status") != "OK":
            print("Sunrise-sunset API returned an error.")
            return False

        sunrise = datetime.fromisoformat(
            data["results"]["sunrise"].replace("Z", "+00:00")
        )
        sunset = datetime.fromisoformat(
            data["results"]["sunset"].replace("Z", "+00:00")
        )

        now = datetime.now(sunrise.tzinfo)

        return now >= sunset or now <= sunrise

    except (requests.RequestException, KeyError, ValueError) as error:
        print("Could not retrieve sunrise/sunset:", error)
        return False


# ---------------------------- SEND EMAIL ---------------------------- #

def send_email():
    if not MY_EMAIL or not MY_PASSWORD:
        print("Set MY_EMAIL and MY_PASSWORD before sending email.")
        return

    message = EmailMessage()
    message["Subject"] = "Look Up! The ISS may be overhead!"
    message["From"] = MY_EMAIL
    message["To"] = MY_EMAIL
    message.set_content(
        "The International Space Station may be near your location "
        "and it is nighttime. Look up at the sky!"
    )

    try:
        with smtplib.SMTP_SSL("smtp.gmail.com", 465, timeout=20) as connection:
            connection.login(MY_EMAIL, MY_PASSWORD)
            connection.send_message(message)

        print("Notification email sent!")

    except (smtplib.SMTPException, OSError) as error:
        print("Could not send email:", error)


# ---------------------------- MAIN LOOP ---------------------------- #

while True:
    if iss_is_overhead() and is_night():
        send_email()
        sleep(60 * 60)  # Wait an hour to avoid repeated notifications
    else:
        print("ISS is not overhead at night right now.")
        sleep(60)
</code></pre>

Day of 34 Code

<pre><code>
import tkinter as tk
import requests
import html

# ---------------------------- CONSTANTS ------------------------------- #

THEME_COLOR = "#375362"
BACKGROUND_COLOR = "#F4F1DE"
CORRECT_COLOR = "#4CAF50"
WRONG_COLOR = "#E76F51"

# ---------------------------- GET QUESTIONS ------------------------------- #

def get_questions():
    parameters = {
        "amount": 10,
        "type": "boolean"
    }

    try:
        response = requests.get(
            "https://opentdb.com/api.php",
            params=parameters,
            timeout=10
        )
        response.raise_for_status()

        data = response.json()

        if data["response_code"] != 0:
            raise ValueError("Could not retrieve quiz questions.")

        questions = data["results"]

        for question in questions:
            question["question"] = html.unescape(
                question["question"]
            )
            question["correct_answer"] = html.unescape(
                question["correct_answer"]
            )

        return questions

    except (requests.RequestException, ValueError, KeyError) as error:
        print("Error loading questions:", error)
        return []


# ---------------------------- QUIZ INTERFACE ------------------------------- #

class QuizApp:

    def __init__(self, questions):
        self.window = tk.Tk()
        self.window.title("Trivia Quiz")
        self.window.config(
            bg=BACKGROUND_COLOR,
            padx=25,
            pady=25
        )
        self.window.minsize(width=450, height=400)

        self.questions = questions
        self.question_number = 0
        self.score = 0
        self.answered = False

        self.score_label = tk.Label(
            text="Score: 0",
            font=("Arial", 16, "bold"),
            bg=BACKGROUND_COLOR,
            fg=THEME_COLOR
        )
        self.score_label.pack(pady=10)

        self.canvas = tk.Canvas(
            width=400,
            height=220,
            bg="white",
            highlightthickness=0
        )
        self.canvas.pack(pady=15)

        self.question_text = self.canvas.create_text(
            200,
            110,
            text="",
            width=350,
            font=("Arial", 17, "bold"),
            fill=THEME_COLOR
        )

        self.feedback_label = tk.Label(
            text="",
            font=("Arial", 14),
            bg=BACKGROUND_COLOR
        )
        self.feedback_label.pack(pady=5)

        button_frame = tk.Frame(
            self.window,
            bg=BACKGROUND_COLOR
        )
        button_frame.pack(pady=10)

        self.true_button = tk.Button(
            button_frame,
            text="True",
            font=("Arial", 14),
            width=12,
            command=lambda: self.check_answer("True")
        )
        self.true_button.grid(row=0, column=0, padx=10)

        self.false_button = tk.Button(
            button_frame,
            text="False",
            font=("Arial", 14),
            width=12,
            command=lambda: self.check_answer("False")
        )
        self.false_button.grid(row=0, column=1, padx=10)

        self.next_button = tk.Button(
            self.window,
            text="Next Question",
            font=("Arial", 12),
            command=self.next_question,
            state="disabled"
        )
        self.next_button.pack(pady=10)

        if self.questions:
            self.show_question()
        else:
            self.end_quiz("No questions could be loaded.")

        self.window.mainloop()

    # ---------------------------- SHOW QUESTION ------------------------------- #

    def show_question(self):
        self.answered = False

        question = self.questions[self.question_number]

        self.canvas.itemconfig(
            self.question_text,
            text=question["question"]
        )

        self.canvas.config(bg="white")
        self.feedback_label.config(text="")

        self.true_button.config(state="normal")
        self.false_button.config(state="normal")
        self.next_button.config(state="disabled")

    # ---------------------------- CHECK ANSWER ------------------------------- #

    def check_answer(self, answer):
        if self.answered:
            return

        self.answered = True

        correct_answer = self.questions[
            self.question_number
        ]["correct_answer"]

        self.true_button.config(state="disabled")
        self.false_button.config(state="disabled")

        if answer == correct_answer:
            self.score += 1
            self.canvas.config(bg=CORRECT_COLOR)
            self.feedback_label.config(
                text="Correct!",
                fg=CORRECT_COLOR
            )
        else:
            self.canvas.config(bg=WRONG_COLOR)
            self.feedback_label.config(
                text=f"Wrong! The answer was {correct_answer}.",
                fg=WRONG_COLOR
            )

        self.score_label.config(
            text=f"Score: {self.score}/{self.question_number + 1}"
        )

        self.next_button.config(state="normal")

        if self.question_number == len(self.questions) - 1:
            self.next_button.config(text="See Results")

    # ---------------------------- NEXT QUESTION ------------------------------- #

    def next_question(self):
        if not self.answered:
            return

        self.question_number += 1

        if self.question_number < len(self.questions):
            self.show_question()
        else:
            self.end_quiz(
                f"Quiz complete!\nYour score: "
                f"{self.score}/{len(self.questions)}"
            )

    # ---------------------------- END QUIZ ------------------------------- #

    def end_quiz(self, message):
        self.canvas.itemconfig(
            self.question_text,
            text=message
        )

        self.canvas.config(bg=BACKGROUND_COLOR)

        self.true_button.config(state="disabled")
        self.false_button.config(state="disabled")
        self.next_button.config(
            text="Finish",
            state="disabled"
        )

        self.feedback_label.config(
            text="Thanks for playing!",
            fg=THEME_COLOR
        )


# ---------------------------- RUN APP ------------------------------- #

questions = get_questions()

QuizApp(questions)
</code></pre>

Day of Code 34

<pre><code>
import tkinter as tk
import requests
import html

# ---------------------------- CONSTANTS ------------------------------- #

THEME_COLOR = "#375362"
BACKGROUND_COLOR = "#F4F1DE"
CORRECT_COLOR = "#4CAF50"
WRONG_COLOR = "#E76F51"

# ---------------------------- GET QUESTIONS ------------------------------- #

def get_questions():
    parameters = {
        "amount": 10,
        "type": "boolean"
    }

    try:
        response = requests.get(
            "https://opentdb.com/api.php",
            params=parameters,
            timeout=10
        )
        response.raise_for_status()

        data = response.json()

        if data["response_code"] != 0:
            raise ValueError("Could not retrieve quiz questions.")

        questions = data["results"]

        for question in questions:
            question["question"] = html.unescape(
                question["question"]
            )
            question["correct_answer"] = html.unescape(
                question["correct_answer"]
            )

        return questions

    except (requests.RequestException, ValueError, KeyError) as error:
        print("Error loading questions:", error)
        return []


# ---------------------------- QUIZ INTERFACE ------------------------------- #

class QuizApp:

    def __init__(self, questions):
        self.window = tk.Tk()
        self.window.title("Trivia Quiz")
        self.window.config(
            bg=BACKGROUND_COLOR,
            padx=25,
            pady=25
        )
        self.window.minsize(width=450, height=400)

        self.questions = questions
        self.question_number = 0
        self.score = 0
        self.answered = False

        self.score_label = tk.Label(
            text="Score: 0",
            font=("Arial", 16, "bold"),
            bg=BACKGROUND_COLOR,
            fg=THEME_COLOR
        )
        self.score_label.pack(pady=10)

        self.canvas = tk.Canvas(
            width=400,
            height=220,
            bg="white",
            highlightthickness=0
        )
        self.canvas.pack(pady=15)

        self.question_text = self.canvas.create_text(
            200,
            110,
            text="",
            width=350,
            font=("Arial", 17, "bold"),
            fill=THEME_COLOR
        )

        self.feedback_label = tk.Label(
            text="",
            font=("Arial", 14),
            bg=BACKGROUND_COLOR
        )
        self.feedback_label.pack(pady=5)

        button_frame = tk.Frame(
            self.window,
            bg=BACKGROUND_COLOR
        )
        button_frame.pack(pady=10)

        self.true_button = tk.Button(
            button_frame,
            text="True",
            font=("Arial", 14),
            width=12,
            command=lambda: self.check_answer("True")
        )
        self.true_button.grid(row=0, column=0, padx=10)

        self.false_button = tk.Button(
            button_frame,
            text="False",
            font=("Arial", 14),
            width=12,
            command=lambda: self.check_answer("False")
        )
        self.false_button.grid(row=0, column=1, padx=10)

        self.next_button = tk.Button(
            self.window,
            text="Next Question",
            font=("Arial", 12),
            command=self.next_question,
            state="disabled"
        )
        self.next_button.pack(pady=10)

        if self.questions:
            self.show_question()
        else:
            self.end_quiz("No questions could be loaded.")

        self.window.mainloop()

    # ---------------------------- SHOW QUESTION ------------------------------- #

    def show_question(self):
        self.answered = False

        question = self.questions[self.question_number]

        self.canvas.itemconfig(
            self.question_text,
            text=question["question"]
        )

        self.canvas.config(bg="white")
        self.feedback_label.config(text="")

        self.true_button.config(state="normal")
        self.false_button.config(state="normal")
        self.next_button.config(state="disabled")

    # ---------------------------- CHECK ANSWER ------------------------------- #

    def check_answer(self, answer):
        if self.answered:
            return

        self.answered = True

        correct_answer = self.questions[
            self.question_number
        ]["correct_answer"]

        self.true_button.config(state="disabled")
        self.false_button.config(state="disabled")

        if answer == correct_answer:
            self.score += 1
            self.canvas.config(bg=CORRECT_COLOR)
            self.feedback_label.config(
                text="Correct!",
                fg=CORRECT_COLOR
            )
        else:
            self.canvas.config(bg=WRONG_COLOR)
            self.feedback_label.config(
                text=f"Wrong! The answer was {correct_answer}.",
                fg=WRONG_COLOR
            )

        self.score_label.config(
            text=f"Score: {self.score}/{self.question_number + 1}"
        )

        self.next_button.config(state="normal")

        if self.question_number == len(self.questions) - 1:
            self.next_button.config(text="See Results")

    # ---------------------------- NEXT QUESTION ------------------------------- #

    def next_question(self):
        if not self.answered:
            return

        self.question_number += 1

        if self.question_number < len(self.questions):
            self.show_question()
        else:
            self.end_quiz(
                f"Quiz complete!\nYour score: "
                f"{self.score}/{len(self.questions)}"
            )

    # ---------------------------- END QUIZ ------------------------------- #

    def end_quiz(self, message):
        self.canvas.itemconfig(
            self.question_text,
            text=message
        )

        self.canvas.config(bg=BACKGROUND_COLOR)

        self.true_button.config(state="disabled")
        self.false_button.config(state="disabled")
        self.next_button.config(
            text="Finish",
            state="disabled"
        )

        self.feedback_label.config(
            text="Thanks for playing!",
            fg=THEME_COLOR
        )


# ---------------------------- RUN APP ------------------------------- #

questions = get_questions()

QuizApp(questions)
</code></pre>

Day 35 of Code

<pre><code>
import os
import requests
from twilio.rest import Client

# ---------------------------- CONFIGURATION ------------------------------- #

MY_LAT = 28.1235       # Replace with your latitude
MY_LONG = -15.4363     # Replace with your longitude

OWM_API_KEY = os.getenv("OWM_API_KEY")
TWILIO_ACCOUNT_SID = os.getenv("TWILIO_ACCOUNT_SID")
TWILIO_AUTH_TOKEN = os.getenv("TWILIO_AUTH_TOKEN")
TWILIO_FROM_NUMBER = os.getenv("TWILIO_FROM_NUMBER")
TWILIO_TO_NUMBER = os.getenv("TWILIO_TO_NUMBER")

OWM_ENDPOINT = "https://api.openweathermap.org/data/2.5/forecast"


# ---------------------------- GET WEATHER DATA ------------------------------- #

def will_rain():
    if not OWM_API_KEY:
        raise RuntimeError("Please set your OWM_API_KEY environment variable.")

    parameters = {
        "lat": MY_LAT,
        "lon": MY_LONG,
        "appid": OWM_API_KEY,
        "units": "metric",
    }

    response = requests.get(
        OWM_ENDPOINT,
        params=parameters,
        timeout=15
    )
    response.raise_for_status()

    weather_data = response.json()

    # Forecast entries are normally spaced three hours apart.
    next_12_hours = weather_data.get("list", [])[:4]

    if not next_12_hours:
        raise ValueError("The API returned no forecast data.")

    for forecast in next_12_hours:
        for condition in forecast.get("weather", []):
            weather_id = condition.get("id", 0)

            # OpenWeather condition codes below 700 include
            # thunderstorms, drizzle, rain, and snow.
            if weather_id < 700:
                return True

    return False


# ---------------------------- SEND SMS ------------------------------- #

def send_sms():
    required_values = [
        TWILIO_ACCOUNT_SID,
        TWILIO_AUTH_TOKEN,
        TWILIO_FROM_NUMBER,
        TWILIO_TO_NUMBER,
    ]

    if not all(required_values):
        raise RuntimeError(
            "Please set all four Twilio environment variables."
        )

    client = Client(
        TWILIO_ACCOUNT_SID,
        TWILIO_AUTH_TOKEN
    )

    message = client.messages.create(
        body="☔ Rain or other precipitation is forecast. "
             "Remember to check the weather before heading out!",
        from_=TWILIO_FROM_NUMBER,
        to=TWILIO_TO_NUMBER,
    )

    print("SMS submitted to Twilio. Message SID:", message.sid)


# ---------------------------- MAIN PROGRAM ------------------------------- #

def main():
    try:
        if will_rain():
            print("Precipitation is forecast in the next 12 hours.")
            send_sms()
        else:
            print("No precipitation detected in the checked forecast.")

    except (requests.RequestException, ValueError, RuntimeError) as error:
        print("Weather alert error:", error)


if __name__ == "__main__":
    main()
</code></pre>

Day 36 of Code 

<pre><code>
import os
import requests

# ---------------------------- CONFIGURATION ------------------------------- #

STOCK = "TSLA"
COMPANY_NAME = "Tesla"

ALPHA_VANTAGE_API_KEY = os.getenv("ALPHA_VANTAGE_API_KEY")
NEWS_API_KEY = os.getenv("NEWS_API_KEY")

STOCK_ENDPOINT = "https://www.alphavantage.co/query"
NEWS_ENDPOINT = "https://newsapi.org/v2/everything"

PERCENT_THRESHOLD = 5


# ---------------------------- GET STOCK PRICES ------------------------------- #

def get_stock_prices():
    if not ALPHA_VANTAGE_API_KEY:
        raise RuntimeError(
            "Set the ALPHA_VANTAGE_API_KEY environment variable."
        )

    parameters = {
        "function": "TIME_SERIES_DAILY",
        "symbol": STOCK,
        "outputsize": "compact",
        "apikey": ALPHA_VANTAGE_API_KEY,
    }

    response = requests.get(
        STOCK_ENDPOINT,
        params=parameters,
        timeout=15
    )
    response.raise_for_status()

    data = response.json()

    if "Error Message" in data or "Note" in data:
        raise RuntimeError(
            f"Stock API response: {data.get('Error Message', data.get('Note'))}"
        )

    time_series = data.get("Time Series (Daily)")

    if not time_series:
        raise RuntimeError(
            f"No stock prices returned. API response: {data}"
        )

    # Dates are sorted newest first.
    sorted_dates = sorted(time_series.keys(), reverse=True)

    if len(sorted_dates) < 2:
        raise RuntimeError("Not enough stock-price history available.")

    latest_date = sorted_dates[0]
    previous_date = sorted_dates[1]

    latest_close = float(
        time_series[latest_date]["4. close"]
    )
    previous_close = float(
        time_series[previous_date]["4. close"]
    )

    return (
        latest_date,
        latest_close,
        previous_date,
        previous_close,
    )


# ---------------------------- CALCULATE CHANGE ------------------------------- #

def calculate_percentage_change(latest_close, previous_close):
    if previous_close == 0:
        raise ValueError("Previous closing price cannot be zero.")

    difference = latest_close - previous_close

    percentage_change = (
        abs(difference) / previous_close
    ) * 100

    if difference > 0:
        direction = "🔺"
    elif difference < 0:
        direction = "🔻"
    else:
        direction = "➡️"

    return percentage_change, direction


# ---------------------------- GET NEWS ------------------------------- #

def get_company_news():
    if not NEWS_API_KEY:
        raise RuntimeError(
            "Set the NEWS_API_KEY environment variable."
        )

    parameters = {
        "q": COMPANY_NAME,
        "language": "en",
        "sortBy": "publishedAt",
        "pageSize": 3,
        "apiKey": NEWS_API_KEY,
    }

    response = requests.get(
        NEWS_ENDPOINT,
        params=parameters,
        timeout=15
    )
    response.raise_for_status()

    data = response.json()

    if data.get("status") != "ok":
        raise RuntimeError(
            f"News API error: {data.get('message', 'Unknown error')}"
        )

    return data.get("articles", [])


# ---------------------------- DISPLAY ALERT ------------------------------- #

def display_news(percentage_change, direction, articles):
    print("\n" + "=" * 45)
    print(f"{COMPANY_NAME} ({STOCK}) STOCK NEWS ALERT")
    print("=" * 45)

    print(f"Stock movement: {direction} {percentage_change:.2f}%")
    print(
        "\nThis is an informational alert, "
        "not a recommendation to buy or sell."
    )

    if not articles:
        print("\nNo news articles were found.")
        return

    for index, article in enumerate(articles, start=1):
        print(f"\nArticle {index}")
        print(f"Headline: {article.get('title', 'No title')}")
        print(f"Source: {article.get('source', {}).get('name', 'Unknown')}")
        print(f"Summary: {article.get('description') or 'No summary available'}")
        print(f"Link: {article.get('url', '')}")


# ---------------------------- MAIN PROGRAM ------------------------------- #

def main():
    try:
        latest_date, latest_close, previous_date, previous_close = (
            get_stock_prices()
        )

        percentage_change, direction = calculate_percentage_change(
            latest_close,
            previous_close
        )

        print(f"Latest trading day: {latest_date}")
        print(f"Previous trading day: {previous_date}")
        print(f"Latest close: ${latest_close:.2f}")
        print(f"Previous close: ${previous_close:.2f}")

        if percentage_change >= PERCENT_THRESHOLD:
            print("\nSignificant price movement detected!")

            articles = get_company_news()

            display_news(
                percentage_change,
                direction,
                articles
            )
        else:
            print(
                f"\nPrice movement was below "
                f"{PERCENT_THRESHOLD}%. No news alert needed."
            )

    except (requests.RequestException, RuntimeError, ValueError) as error:
        print(f"\nError: {error}")


if __name__ == "__main__":
    main()
</code></pre>

Day 37 of Code

<pre><code>import random

# Welcome message
print("Welcome to the Number Guessing Game!")
print("I'm thinking of a number between 1 and 100.")

# Generate a random number
secret_number = random.randint(1, 100)

# Set the number of attempts
attempts = 0
max_attempts = 7

print(f"You have {max_attempts} attempts to guess the number.")

# Game loop
while attempts < max_attempts:

    guess = int(input("Make a guess: "))
    attempts += 1

    if guess < secret_number:
        print("Too low! Try again.")

    elif guess > secret_number:
        print("Too high! Try again.")

    else:
        print("Congratulations! You guessed the number!")
        print(f"The secret number was {secret_number}.")
        print(f"You guessed it in {attempts} attempts!")
        break

# Check if the player ran out of attempts
if attempts == max_attempts and guess != secret_number:
    print("Game over! You ran out of attempts.")
    print(f"The secret number was {secret_number}.")</code></pre>

Day 38 of Code

<pre><code># Day 38 - Quiz Game

print("Welcome to the Python Quiz Game!")
print("Answer the following questions.\n")

questions = [
    {
        "question": "What is the capital of France?",
        "options": ["A. London", "B. Paris", "C. Madrid"],
        "answer": "B"
    },
    {
        "question": "Which language are we learning?",
        "options": ["A. Java", "B. C++", "C. Python"],
        "answer": "C"
    },
    {
        "question": "What is the result of 5 + 3?",
        "options": ["A. 8", "B. 10", "C. 15"],
        "answer": "A"
    },
    {
        "question": "Which symbol is used for comments in Python?",
        "options": ["A. //", "B. #", "C. &"],
        "answer": "B"
    },
    {
        "question": "Which function displays text on the screen?",
        "options": ["A. input()", "B. print()", "C. int()"],
        "answer": "B"
    }
]

score = 0

for question in questions:
    print(question["question"])

    for option in question["options"]:
        print(option)

    user_answer = input("Your answer (A, B or C): ").upper()

    if user_answer == question["answer"]:
        print("Correct answer!\n")
        score += 1
    else:
        print("Incorrect answer!")
        print(f"The correct answer was {question['answer']}.\n")

print("Quiz finished!")
print(f"Your final score is: {score}/{len(questions)}")

if score == len(questions):
    print("Excellent! You got everything right!")
elif score >= 3:
    print("Good job! Keep practising!")
else:
    print("Keep learning Python. You can do it!")</code></pre>

Day 39 of Code

<pre><code># Day 39 - Quiz Game with Categories

print("Welcome to the Python Quiz Game!")
print("Choose a category:\n")

categories = {
    "python": [
        {
            "question": "Which function displays text?",
            "options": ["A. input()", "B. print()", "C. int()"],
            "answer": "B"
        },
        {
            "question": "Which symbol is used for comments?",
            "options": ["A. #", "B. //", "C. &"],
            "answer": "A"
        }
    ],

    "general": [
        {
            "question": "What is the capital of France?",
            "options": ["A. London", "B. Paris", "C. Rome"],
            "answer": "B"
        },
        {
            "question": "How many days are in a week?",
            "options": ["A. 5", "B. 6", "C. 7"],
            "answer": "C"
        }
    ],

    "science": [
        {
            "question": "Which planet is known as the Red Planet?",
            "options": ["A. Mars", "B. Venus", "C. Jupiter"],
            "answer": "A"
        },
        {
            "question": "What gas do plants absorb?",
            "options": ["A. Oxygen", "B. Carbon dioxide", "C. Hydrogen"],
            "answer": "B"
        }
    ]
}

print("Available categories:")
print("1. Python")
print("2. General Knowledge")
print("3. Science")

choice = input("\nChoose a category: ").lower()

if choice == "1":
    category = "python"
elif choice == "2":
    category = "general"
elif choice == "3":
    category = "science"
else:
    print("Invalid category!")
    category = None

score = 0

if category:
    questions = categories[category]

    print(f"\nYou selected {category.title()}!")
    print("Let's start!\n")

    for question in questions:
        print(question["question"])

        for option in question["options"]:
            print(option)

        answer = input("Your answer: ").upper()

        if answer == question["answer"]:
            print("Correct!\n")
            score += 1
        else:
            print("Incorrect!")
            print(f"Correct answer: {question['answer']}\n")

    print("Quiz finished!")
    print(f"Your score: {score}/{len(questions)}")

    percentage = (score / len(questions)) * 100

    print(f"Your percentage: {percentage:.0f}%")

    if percentage == 100:
        print("Perfect score! Excellent!")
    elif percentage >= 50:
        print("Good job! Keep practising!")
    else:
        print("Keep learning. You can improve!")</code></pre>

Day 40 of Code

<pre><code># Day 40 - Password Manager

import random
import string
import json
from pathlib import Path

DATA_FILE = Path("passwords.json")


def generate_password(length=12):
    characters = string.ascii_letters + string.digits + string.punctuation
    password = "".join(
        random.choice(characters) for _ in range(length)
    )
    return password


def load_passwords():
    if DATA_FILE.exists():
        try:
            return json.loads(DATA_FILE.read_text(encoding="utf-8"))
        except json.JSONDecodeError:
            print("The data file is invalid.")
    return {}


def save_passwords(passwords):
    DATA_FILE.write_text(
        json.dumps(passwords, indent=4),
        encoding="utf-8"
    )


def add_password(passwords):
    website = input("Website name: ").strip()
    username = input("Username or email: ").strip()

    if not website or not username:
        print("Website and username cannot be empty.")
        return

    length = int(input("Password length (minimum 12): "))

    if length < 12:
        print("Please choose at least 12 characters.")
        return

    password = generate_password(length)

    passwords[website] = {
        "username": username,
        "password": password
    }

    save_passwords(passwords)

    print("\nPassword generated and saved!")
    print(f"Website: {website}")
    print(f"Username: {username}")
    print(f"Password: {password}")


def view_passwords(passwords):
    if not passwords:
        print("No passwords saved yet.")
        return

    print("\nSaved accounts:")

    for website, details in passwords.items():
        print(f"\nWebsite: {website}")
        print(f"Username: {details['username']}")
        print("Password: [hidden]")


def main():
    passwords = load_passwords()

    while True:
        print("\n===== PASSWORD MANAGER =====")
        print("1. Generate and save a password")
        print("2. View saved accounts")
        print("3. Exit")

        choice = input("Choose an option: ")

        if choice == "1":
            add_password(passwords)

        elif choice == "2":
            view_passwords(passwords)

        elif choice == "3":
            print("Goodbye!")
            break

        else:
            print("Invalid option. Try again.")


main()</code></pre>
