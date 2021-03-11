# 5 min python
# Description
> samples of code

# 11_beep.py
> add modules sys and os to your system
> use function system of the os module to say "Feed the Python"
> use sys.stdout to write a beep '\a' x 3 times.
> don't forget to flush after that

```python
#!/usr/bin/env python3
import sys
import os
os.system('say "feed the python"')
for x in range(3):
    sys.stdout.write('\a')
sys.stdout.flush()
```
# 12_board.py
> create an empty list called board
> prompt user to enter board size and store that value in var board_size
> create a loop with range from zero to board_size
> use append function of board to add a char times boad_size
> print each row in board, and make it pretty with .join(row)
```python
#!/usr/bin/env python3
board = []
board_size = int(input("enter board size:\n"))
for x in range(0, board_size):
    board.append(["X"] * board_size)
for z in board:
    print(" ".join(z))
```
# 13_pc_ship.py
> create an empty list called pc_board
> create variable called board_size and give it value of 10
> using function randint from random module generate pc_ship_row and pc_ship_col
> print out corrdinates of the PC's ship (make sure it's within range)
> place ship on the board and print out the board with the ship.
```python
#!/usr/bin/env python3
import random
pc_board=[]
board_size=10
for x in range(0, board_size):
    pc_board.append(["X"] * board_size)

pc_ship_row=random.randint(0, len(pc_board) - 1)
pc_ship_col=random.randint(0, len(pc_board[0]) - 1)
print("ship coordinates are ", pc_ship_row, pc_ship_col)
pc_board[pc_ship_row][pc_ship_col]="O"
for z in pc_board:
    print(" ".join(z))
```
# 14_ship.py
> crete an empty list called board
> create variable called board_size and give it value of 10
> prompt user to enter ship's row and column coordinates: ship_row and ship_col
> verify user's input and print out corrdinates of the ship
> define a funcion called print_board() to print your board and give it board as argument
> place ship on the board and print using function print_board().
```python
#!/usr/bin/env python3
import random
pc_board=[]
board_size=int(input("enter board size: ").strip())
for x in range(0, board_size):
    pc_board.append(["X" + str(x)] * board_size)

pc_ship_row=int(input("input row: ").strip()) - 1
pc_ship_col=int(input("input column: ").strip()) - 1
print("ship coordinates are ", pc_ship_row, pc_ship_col)
print(board_size)
if (pc_ship_row > board_size or pc_ship_col > board_size):
    print("dumbass")
else:
    print("ship coordinates are ", pc_ship_row, pc_ship_col)
    pc_board[pc_ship_row][pc_ship_col]="O"
    for z in pc_board:
        print(" ".join(z))
```
# 15_clear_screen.py
> import modules os and time
> in os use system('clear') to clear the screen
> prompt user to enter his name
> clear screen again
> from time use sleep and sleep for 2 sec
> print out hello and user's name, sleep for 2 sec and clear screen.
```python
#!/usr/bin/env python3
import os
import time
os.system('clear')
name=input("enter your name: ")
os.system('clear')
time.sleep(2)
print("hello " + name)
time.sleep(2)
os.system('clear')
```
# 40_if_statement.py
> For variable x, prompt to enter an integer
> * in case it's less then zero, print warning and change it to zero
> * in case it's a zero print word zero
> * and for everything other then above just print word more

```python
#!/usr/bin/env python3
print("enter an integer")
x=int(input())

if x < 0:
    print("warning")
    x=0
elif x == 0:
    print("zero")
else:
    print("word more")
```
```console
tim @ Vitaliys - Mini 5_min_python % . / 40_if_statement.py
enter an integer
0
zero
```
# 41_for_statement.py
> create a simple list called words with words cat, window and defenestrate
> inside the for loop print each word and provide count of letters in it

```python
words=["cat", "window", "defenstrate"]
print(len(words))
for w in words:
    print(w, len(w))
```

# 42_range_function.py
> create a for loop which would print 5 numbers starting with 0 using range function.
> also create a for loop to print numbers 0, 3, 6, 9 using range

```python
for x in range(5):
    print(x)
for y in range(0, 10, 3):
    print(y)
```
# 44_for_loop_break.py
> create a variable called my_break equal 6
> create a for loop which would print 10 numbers starting with 0 using range function.
> inside the loop add if statement to check if we hit number 6 and get out of loop
```python
my_break=6
for x in range(10):
    print(x)
    if x == 6:
        break
print("out of loop")
```
# 50_lists.py
> create a simple list called fruits with words orange, apple, pear, banana, kivi, and apple
> * print count of apple in the fruits,
> * print index of banana, and print whatever is with index 5
> (time: 2 mins)

```python
fruits=["orange", "apple", "pear", "banana", "kivi", "apple"]
print(fruits.count("apple"))
print(fruits.index("banana"))
print(fruits[5])
```
# 51_lists_methods.py
> create a simple list called fruits with words orange, apple, pear, banana, kivi, and apple
> * add a grape to the list fruits
> * reverse the order of the list and print
> * sort given list and print
> * get rid of last element using pop and print the list
> Note: use Cmd + Shift + D and Ctrl + Win + down

```python
fruits=["orange", "apple", "pear", "banana", "kivi", "apple"]
fruits.append("grape")
print(fruits)
fruits.reverse()
print(fruits)
fruits.sort()
print(fruits)
fruits.pop()
print(fruits)
```
> TODO: very ugly, fix it

# 55_dictionary.py
> create a simple dictionary called phone with words jack: 5555 and bob: 6666
> * add another phone record for vit: 3456;
> * print all records
> * delete bob's phone
> * print just jack's record
> * print list of phone dictionary
```python
phone={"jack": 5555, "bob": 6666}
phone["vit"]=3456
print(phone)
del phone["bob"]
print(phone)
print(phone["jack"])
print(list(phone))
```
# 56_dict_loops.py
> import json
> create a simple dictionary called friends with elements
> "Tim": {"age": 14, "note": "Awesome kid"}
> "Dillan": {"age": 20 "note": "old fart"}
> create a loop with three variables and use friends.items()
> print each name of the friend and his note
> print using json.dumps with indent=3
```python
import json

friends={"Tim": {"age": 14, "note": "swag"}, "Dylan": {"age":
                                                         14, "note": "unswag"}}

for x, y in friends.items():
    print(x, "is ", y["note"])
print(json.dumps(friends, indent=1))
```
# 72_read_file.py and test.txt(with some text inside)
> create variable filename and give it file you want to read as a string
> use with open() as f to access file
> use variable read_data and assign it results of f.read()
> print out what you have in read_data
> to test how it breaks - change name of the file in filename varialbe.
> modify so you'd use try: and workout the exception in case no file found

```python
filename="test.txt"
try:
    with open(filename) as f:
        read_data=f.read()
    print(read_data)
except IOError:
    print("dumbass")
```
# 73_write_file.py
> create variable filename and give it file you want to write to as a string
> create var user_data and prompt user to enter his name
> use with open(filename, "w") as fo to access the file for writing
> use fo.write and give it filename to write to
> after a few tests replace "w" with "a", check output
> after that fix it to add new line for each name
```python
#!/usr/bin/env python3
filename="blah.txt"
user_data=input("enter your name: ")
with open(filename, "a") as fo:
    fo.write(user_data + "\n")
```
### 74_write_json.py
> use json module, create var filename with string value of friends_json.txt
> define function write_json_file with input parameter called data
> this function should open file for writing and save data using json.dumps
> copy friends dictionary, print it and save it using write_json_file

```python
import json
filename = "friends_json.txt"


def write_json_file(data):
    with open(filename, "w") as fo:
        fo.write(json.dumps(data, indent=1))


friends = {"Tim": {"age": 14, "note": "swag"}, "Dylan": {"age":
                                                         14, "note": "unswag"}}
print(json.dumps(friends, indent=1))
write_json_file(friends)
```
