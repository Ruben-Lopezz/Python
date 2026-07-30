Python

Este es mi recorrido diario y mi progreso aprendiendo Python.

Day 1 of Code

<pre><code>print("Welcome to the Band Name Generator.") city = input("Which city did you grow up in?\n") pet = input("What is the name of a pet?\n") print("Your band name could be " + city + " " + pet)</code></pre>

Day 2 of Code

<pre><code>print("Welcome to the tip calculator!") bill = float(input("What was the total bill? $")) tip = int(input("What percentage tip would you like to give? 10 12 15 ")) people = int(input("How many people to split the bill? ")) tip_as_percent = tip / 100 total_tip_amount = bill * tip_as_percent total_bill = bill + total_tip_amount bill_per_person = total_bill / people final_amount = round(bill_per_person, 2) print(f"Each person should pay: ${final_amount}")</code></pre>

Day 3 of Code

<pre><code>print(r''' ******************************************************************************* | | | | _________|________________.=""_;=.______________|_____________________|_______ | | ,-"_,="" `"=.| | |___________________|__"=._o`"-._ `"=.______________|___________________ | `"=._o`"=._ _`"=._ | _________|_____________________:=._o "=._."_.-="'"=.__________________|_______ | | __.--" , ; `"=._o." ,-"""-._ ". | |___________________|_._" ,. .` ` `` , `"-._"-._ ". '__|___________________ | |o`"=._` , "` `; .". , "-._"-._; ; | _________|___________| ;`-.o`"=._; ." ` '`."\ ` . "-._ /_______________|_______ | | |o ; `"-.o`"=._`` '` " ,__.--o; | |___________________|_| ; (#) `-.o `"=.`_.--"_o.-; ;___|___________________ ____/______/______/___|o;._ " `".o|o_.--" ;o;____/______/______/____ /______/______/______/_"=._o--._ ; | ; ; ;/______/______/______/_ ____/______/______/______/__"=._o--._ ;o|o; _._;o;____/______/______/____ /______/______/______/______/____"=._o._; | ;_.--"o.--"_/______/______/______/_ ____/______/______/______/______/_____"=.o|o_.--""___/______/______/______/____ /______/______/______/______/______/______/______/______/______/______/_____ / ******************************************************************************* ''') print("Welcome to Treasure Island.") print("Your mission is to find the treasure.") choice1 = input('You\'re at a crossroad, where do you want to go? ' 'Type "left" or "right".\n').lower() if choice1 == "left": choice2 = input('You\'ve come to a lake. ' 'There is an island in the middle of the lake. ' 'Type "wait" to wait for a boat. ' 'Type "swim" to swim across.\n').lower() if choice2 == "wait": choice3 = input("You arrive at the island unharmed. " "There is house with 3 doors. One red, " "one yellow and one blue. " "Which colour do you choose?\n").lower() if choice3 == "red": print("It's a room full of fire. Game Over") elif choice3 == "yellow": print("You found the treasure. You Win!") elif choice3 == "blue": print("You enter a room of beasts. Game Over.") else: print("You chose a door that doesn't exist. Game Over.") else: print("You got attacked by an angry trout. Game Over.") else: print("You fell in to a hole. Game Over.")</code></pre>

Day 4 of Code

<pre><code>import random rock = ''' _______ ---' ____) (_____) (_____) (____) ---.__(___) ''' paper = ''' _______ ---' ____)____ ______) _______) _______) ---.__________) ''' scissors = ''' _______ ---' ____)____ ______) __________) (____) ---.__(___) ''' game_images = [rock, paper, scissors] user_choice = int(input("What do you choose? Type 0 for Rock, 1 for Paper or 2 for Scissors.\n")) if user_choice &gt;= 0 and user_choice &lt;= 2: print(game_images[user_choice]) computer_choice = random.randint(0, 2) print("Computer chose:") print(game_images[computer_choice]) if user_choice &gt;= 3 or user_choice &lt; 0: print("You typed an invalid number. You lose!") elif user_choice == 0 and computer_choice == 2: print("You win!") elif computer_choice == 0 and user_choice == 2: print("You lose!") elif computer_choice &gt; user_choice: print("You lose!") elif user_choice &gt; computer_choice: print("You win!") elif computer_choice == user_choice: print("It's a draw!")</code></pre>

Day 5 of Code 

<pre><code>import random
letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
numbers = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
symbols = ['!', '#', '$', '%', '&', '(', ')', '*', '+']

print("Welcome to the PyPassword Generator!")
nr_letters = int(input("How many letters would you like in your password?\n"))
nr_symbols = int(input(f"How many symbols would you like?\n"))
nr_numbers = int(input(f"How many numbers would you like?\n"))


 password = ""
 for char in range(0, nr_letters):
     password += random.choice(letters)

 for char in range(0, nr_symbols):
     password += random.choice(symbols)

 for char in range(0, nr_numbers):
     password += random.choice(numbers)

 print(password)


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
  
print(f"Your password is: {password}")</code></pre>

Day 6 of Code 

<pre><code>def my_function():
    print("Hello")
    print("Bye")


my_function()</code></pre>

Day 7 of Code

<pre><code>import random
word_list = ["aardvark", "baboon", "camel"]

chosen_word = random.choice(word_list)
print(chosen_word)

guess = input("Guess a letter: ").lower()

for letter in chosen_word:
    if letter == guess:
        print("Right")
    else:
        print("Wrong")</code></pre>

Day 8 of Code

<pre><code>import art

print(art.logo)

alphabet = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u',
            'v', 'w', 'x', 'y', 'z']


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
        print("Goodbye")</code></pre>

Day 9 of Code

<pre><code>from art import logo
print(logo)


def find_highest_bidder(bidding_record):
    highest_bid = 0
    winner = ""
    for bidder in bidding_record:
        bid_amount = bidding_record[bidder]
        if bid_amount > highest_bid:
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
        print("\n" * 20)</code></pre>

Day 10 of Code

<pre><code>import art


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

 print(operations["*"](4, 8))


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


calculator()</code></pre>

Day 11 of Code 

