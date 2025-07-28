# Servo Torque

In this task we'll calculate the amount of torque required for each servo motor to pick up an object with 1kg of weight in the following picture:
<img width="480" height="436" alt="image" src="https://github.com/user-attachments/assets/2aff720d-61df-4965-b504-38c25e02bf18" />

First, we need to know the formula to calculate the torque of the servo motor:

The formula is: Torque = force x radius

When we calculate the torque of the base servo we need to combine the radius from the base to the end effector and also we need to multiply the mass of the object by the gravity to get the force.
  
1- Base Servo Required Torque: (0.15m+0.10m+0.04m) * (1kg * 9.8 m/s) = 2.84 N.m, we need to convert from N.m to kg.cm so we can compare it to the datasheet of the chosen servo motor, so we need to multiply it by 10.2 = 28.98 kg.cm

2- Second Servo Required Torque: (0.10m+0.04m) * (1kg * 9.8 m/s) = 1.37 N.m, converting to kg.cm = 13.99 kg.cm

3- Third Servo Required Torque: (0.04) * (1kg * 9.8 m/s) = 0.392 N.m, converting to kg.cm = 3.84 kg.cm

We'll use the following table to choose the ideal servo for each joint:
<img width="945" height="217" alt="image" src="https://github.com/user-attachments/assets/00febe20-9fc0-4daf-86b9-25350a4101b8" />

For the base servo motor we'll choose the DS3235 as it provides 33kg.cm torque at 5v.

For the second servo motor we'll choose the MG995 as it provides 15
