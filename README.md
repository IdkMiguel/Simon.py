# Simon.py
import random
import time
import board
from digitalio import DigitalInOut, Direction

bl = DigitalInOut(board.D7)
bl.direction = Direction.OUTPUT
re = DigitalInOut(board.D10)
re.direction = Direction.OUTPUT

ye = DigitalInOut(board.D8)
ye.direction = Direction.OUTPUT

gr = DigitalInOut(board.D9)
gr.direction = Direction.OUTPUT
# pin configuration / setup



w = DigitalInOut(board.D1)
w.direction = Direction.INPUT
b = DigitalInOut(board.D2)
b.direction = Direction.INPUT
g = DigitalInOut(board.D4)
g.direction = Direction.INPUT
y = DigitalInOut(board.D3)
y.direction = Direction.INPUT
r = DigitalInOut(board.D5)
r.direction = Direction.INPUT
bl = DigitalInOut(board.D6)
bl.direction = Direction.INPUT


# main / infinite loop

my_list = []
game = []


def add_to_sequence(my_trip):
    lsit.append(random.randint(0 , 3))

def display_sequence(my_trip):
    p = " "
    for x in my_trip:
        if x == 0:
            p = "red"
            re.value = not re.value
            time.sleep(.3)
            re.value = not re.value
        elif x == 1:
            p = "green"
            gr.value = not gr.value
            time.sleep(.3)
            gr.value = not gr.value
            time.sleep(.3)
        elif x == 2:
            p = "Yellow"
            ye.value = not ye.value
            time.sleep(.3)
            ye.value = not ye.value
            time.sleep(.3)
        else:
            p = "Blue"
            bl.value = not bl.value
            time.sleep(.3)
            bl.value = not bl.value
            time.sleep(.3)
           
def try_sequence(inputlist):
    user = " "
    for x in my_list:
        if x == 0:
            p = "red"
            re.value = not re.value
            time.sleep(.3)
            re.value = not re.value
        elif x == 1:
            p = "green"
            gr.value = not gr.value
            time.sleep(.3)
            gr.value = not gr.value
            time.sleep(.3)
        elif x == 2:
            p = "Yellow"
            ye.value = not ye.value
            time.sleep(.3)
            ye.value = not ye.value
            time.sleep(.3)
        else:
            p = "Blue"
            bl.value = not be.value
            time.sleep(.3)
            bl.value = not be.value
            time.sleep(.3)
while True:
    if w.value:
        display_sequence(my_list)
        time.sleep(.3)      
    if b.value:
        time.sleep(.3)
        add_to_sequence(my_list)
    if g.value:
        time.sleep(.3)
        add_to_sequence(my_list)        
    if y.value:
        time.sleep(.3)
        add_to_sequence(my_list)        
    if r.value:
        time.sleep(.3)
        add_to_sequence(my_list)        
    if bl.value:
         time.sleep(.3)
         add_to_sequence(my_list)        

