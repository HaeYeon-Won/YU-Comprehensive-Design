#!/usr/bin/env/python

from time import sleep, time, localtime #import
import math
import pigpio
import rospy
from std_msgs.msg import *

def main():
    print("ready to Servo")
    sub = rospy.Subscriber("ServoAngle", Float64MultiArray, control_servo)
    rospy.spin()

def control_servo(angle):
    global pin
    print("angle = ", angle)
    y_angle = angle.data[1]
    pi.set_servo_pulsewidth(pin, y_angle)
    sleep(0.001)

pin = 27
pi=pigpio.pi()
print("change_servo angle 0 0")
pi.set_servo_pulsewidth(pin, 1500)

if __name__ == "__main__":
    try:
        rospy.init_node("servo_y", anonymous = True)
        main()
        sleep(0.01)
    except KeyboardInterrupt:
        flag=-1
        break
