{% include navigation.html %}

# Data Structure
## <a href="https://github.com/ProRichyMan/NathanIndividual"> Github Link</a>
## <a href="https://replit.com/@ProRichyman"> Replit Link</a>

# Code
## TT0
### [MENU](https://replit.com/@ProRichyMan/menu?v=1)
<iframe frameborder="0" width="100%" height="500px" src="https://replit.com/@ProRichyMan/menu?lite=true#menu.py"></iframe>
````
import math 

import animation

# Creates Title 
border = "=" * 40
banner = f"\n{border}\nWhat do you want to do with the list\n{border}"

def menu():
  print(banner)
  options = [
    ["swap", "swap.py"], 
    ["matrix", "matrix.py"], 
    ["tree", "tree.py"],
    ["animation", animation.ship],
    ["createtask", "createtask.py"]
  ]

  functions = {}
  functions[0] = ["Exit"] 
  for op in options:
    index = len(functions)
    functions[index] = op

  for key, value in functions.items():
    print(key, '->', value[0])

#  number = 1 
#  for thing in functions: 
#    print( str(number) + " " + str(thing)
#    number = int(number) + 1  

  choice = input("What function would you like: ")

  try: #try converting to integer
    #convert to number
    choice = int(choice)
    if choice == 0: #exit choice, stop loop
      exit() #return means leave function
    try:  #try to run as playground function
      action = functions.get(choice)[1]
      exec(open(action).read())
    except:
      try:  #try to run as function
        action()
      except:
        print(f"Bad action: {action}")
      #end function try
    #end playground try
  except ValueError: #not a number error
    print(f"Not a number: {choice}")
  except: #traps all other errors
    print(f"Invalid choice: {choice}")
while "choice" != 0:
    menu()
````

### [TREE](https://replit.com/@ProRichyMan/treepyramid?v=1)
````
import math

try:
  layers = int(input("How many layers of the pyramid (enter an integer): "))
except:
    print("That\'s not an integer! Please run again.")
    exit()
star = "* "
x = 1
spaceNum = layers

print("Here's your tree")

while x <= layers:
  print((spaceNum * " ") + star)
  star += "* "
  spaceNum -= 1
  x += 1

print(" " * math.floor(layers/1.11) + "***")
````
### [ANIMATION](https://replit.com/@ProRichyMan/animation?v=1)
````
import time

# terminal print commands
ANSI_CLEAR_SCREEN = u"\u001B[2J"
ANSI_HOME_CURSOR = u"\u001B[0;0H\u001B[2"
OCEAN_COLOR = u""
SHIP_COLOR = u"\u001B[32m\u001B[2D"
RESET_COLOR = u"\u001B[0m\u001B[2D"

def ocean_print():
    # print ocean
    print(ANSI_CLEAR_SCREEN, ANSI_HOME_CURSOR)
    print("\n\n\n\n")
    print(OCEAN_COLOR + "  " * 35)

# print ship with colors and leading spaces
def ship_print(position):
    print(ANSI_HOME_CURSOR)
    print(RESET_COLOR)
    sp = " " * position
    print(sp + " _____________   ")
    print(sp + " [][][][][] |_\_   ")
    print(sp + " |  City Bus |   )   ")
    print(sp + " =--OO-------OO--=    ")
    print(RESET_COLOR)

# ship function, iterface into this file
def ship():
  ocean_print()
  # loop control variables
  start = 0  # start at zero
  distance = 75  # how many times to repeat
  step = 2  # count by 2

  # loop purpose is to animate ship sailing
  for position in range(start, distance, step):
      ship_print(position)  # call to function with parameter
      time.sleep(.1)

ship()
````
