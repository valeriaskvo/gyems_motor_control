# Gyems motor control

In the file lies `motor_control.py` lies a set of basic functions of how to connect to the motor and set different current value on it. 

In the `RMD_L_Series_Servo_Actuator_User_Manual_Rev_1_01_Release_1.pdf` file, you can find the motor wiring pinout and basic information about the motor interface.

# How to fix problems with CANable

If you get error **OSError: [Errno 19] No such device**:

1. Go to **can-utils** folder and compile by the

``make``

``sudo make install``

2. Run following comand to setup the CANable:

``sudo slcand -o -c -s0 /dev/ttyACM0 can0``

``sudo ifconfig can0 up``

``sudo ifconfig can0 txqueuelen 1000``


References:
https://canable.io/getting-started.html