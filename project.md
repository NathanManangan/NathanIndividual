{% include navigation.html %}

# Data Structure
## <a href="https://github.com/ProRichyMan/NathanIndividual"> Github Link</a>
## <a href="https://replit.com/@ProRichyman"> Replit Link</a>

# Code
## TT0
### [MENU](https://replit.com/@ProRichyMan/menu?v=1)
<iframe frameborder="0" width="100%" height="800px" src="https://replit.com/@ProRichyMan/menu#main.py?embed=true"> </iframe>

### [TREE](https://replit.com/@ProRichyMan/treepyramid?v=1)
````
print("Christmas Tree")
#tree
tree = [("        ","*"," "),
        ("       ","* *"," "),
        ("      ","* * *"," "),
        ("     ","* * * *"," "),
        ("    ","* * * * *"," "),
        ("   ","* * * * * *"," "),
        ("  ","* * * * * * *"," "),
        (" ","* * * * * * * *"," "),
        ("","* * * * * * * * *"," "),
        ("       ","***"," "),
        ("       ","***"," "),
        ("       ","***"," "),
  ]
for x in tree:
    for y in x:
        print(y, end = " ")
    print()
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
