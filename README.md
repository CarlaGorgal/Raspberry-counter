from gpiozero import LED

from gpiozero import Button

from time import sleep

 

A = LED(14) # 1 0 1 0 1 0 1 0 1 0

B = LED(15) # 0 1 1 0 0 1 1 0 0 0

C = LED(17) # 0 0 0 1 1 1 1 0 0 0

D = LED(18) # 0 0 0 0 0 0 0 1 1 0

button = Button(2)

press = 0

while press <= 10:

    if press == 10: press = 0

    if press == 0 : 

        A.off()

        B.off()

        C.off()

        D.off()

    elif press == 1 :

        A.on()

        B.off()

        C.off()

        D.off()

    elif press == 2 :

        A.off()

        B.on()

        C.off()

        D.off()

    elif press == 3 :

        A.on()

        B.on()

        C.off()

        D.off()

    elif press == 4 :

        A.off()

        B.off()

        C.on()

        D.off()

    elif press == 5 :  

        A.on()

        B.off()

        C.on()

        D.off()

    elif press == 6 :

        A.off()

        B.on()

        C.on()

        D.off()

    elif press == 7 :

        A.on()

        B.on()

        C.on()

        D.off()

    elif press == 8 :

        A.off()

        B.off()

        C.off()

        D.on()

    else: A.on()

        B.off()

        C.off()

        D.on()    

    button.wait_for_press()

    press = press + 1

