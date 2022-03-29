# Robot arm extension


## Project original planning

<img src="Capture.PNG">

<img src="Capturec.PNG">

<img src="Capturev.PNG">

<img src="Capturex.PNG">

## Update on Plan

1/25 We revised the plan and took out the anthropomorphic feature due to added difficulty. We decided toe build a phone holder in order to we able to help multi task. The new idea will give us an easy way to watch a show on your phone while also playing cards, playing catch, or working on your computer. 

## Milestone 1

1/31 As of right now, we have finished the arm attachment and the phone holder. Next we need to find a code, and wire up servos to make the phone rotate back and forth. We have achieved our first milestone because we built the 2 parts we said we would. These a pictures of our finished parts in cad. The first is the phone holder, the second is the axle that the servos will use to turn, the third is the arm attachment.

<img src="Capturea.PNG">

<img src="Captureb.PNG">

<img src="Captured.PNG">

## Finish assembly

2/7 Today I finished all of the parts and assembly. This picture shows a phone holder attached to an axel and 2 servos. The servos will rotate forward and backward to the person's liking. The objective of the project is to make a arm attachment that will hold a phone while giving you the freedom to move both hands. This project will allow you to eat, watch the news, and use the other hand for fidgiting, playing cards, or just resting.

<img src="Capturebc.PNG">

## Code

```
import time
import board
import pwmio
from adafruit_motor import servo

# create a PWMOut object on Pin A2.
pwm = pwmio.PWMOut(board.A2, duty_cycle=2 ** 15, frequency=50)

# Create a servo object, my_servo.
my_servo = servo.Servo(pwm)


while True:
    for angle in range(0, 180, 5):   # 0 - 180 degrees, 5 degrees at a time.
        my_servo.angle = angle
        time.sleep(0.05)
    for angle in range(180, 0, -5):  # 180 - 0 degrees, 5 degrees at a time.
        my_servo.angle = angle
        time.sleep(0.05)
```

The code still isn't fully working. It should be done soon but this is where we are at now.


