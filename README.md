import random
import time
import board
from digitalio import DigitalInOut, Direction

be = DigitalInOut(board.D12)
be.direction = Direction.OUTPUT
re = DigitalInOut(board.D9)
re.direction = Direction.OUTPUT

ye = DigitalInOut(board.D10)
ye.direction = Direction.OUTPUT

gr = DigitalInOut(board.D11)
gr.direction = Direction.OUTPUT
# pin configuration / setup



w = DigitalInOut(board.D2)
w.direction = Direction.INPUT
b = DigitalInOut(board.D3)
b.direction = Direction.INPUT
g = DigitalInOut(board.D5)
g.direction = Direction.INPUT
y = DigitalInOut(board.D6)
y.direction = Direction.INPUT
r = DigitalInOut(board.D4)
r.direction = Direction.INPUT
bl = DigitalInOut(board.D7)
bl.direction = Direction.INPUT


# main / infinite loop

my_list = []
game = []


def add_to_sequence(my_trip):
    my_trip.append(random.randint(0 , 3))

def display_sequence(my_trip):
    p = " "
    #code to make led blink on
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
            be.value = not be.value
            time.sleep(.3)
            be.value = not be.value
            time.sleep(.3)
           
def try_sequence(inputlist):
    user = " "
    #code to make led blink off
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
            be.value = not be.value
            time.sleep(.3)
            be.value = not be.value
            time.sleep(.3)
while True:
    #activates buttons but doesn't work
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

