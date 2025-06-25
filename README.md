# Microwave-Oven-using-PIC-Microcontroller-
Developed a Microwave oven system using a micro-controller to Manage timers for countdown,  pause/resume functionality and ensure a smooth transition between states.   • Technologies Used: Microcontroller PIC16F877A, LCD, I2C protocol, Timer0, MKP switches. 
# Microwave Oven Operations                            
• Designed and developed a Microwave oven system using PIC16F877A microcontroller. 
• Cooking Modes & Operations: Implement Micro (900W), Grill, and Convection (preheating up to 
180°C) with time setting, start, pause, stop, and resume functionalities.  
• Peripheral Control: Use CLCD for display, MKP switches for mode selection and input, a fan for 
cooking indication, and a buzzer for completion alerts.  
• Timer & Process Flow: Manage timers for countdown, pause/resume functionality, auto-increment 
by 30s during cooking, and ensure a smooth transition between states. 

# Requirement :
As soon as the hex file is loaded -> power on screen should display after few delay menu screen should display

menu screen :
1. Micro Mode :
-> MKP1 --> to select Micro mode --> display power = 900W for 1 sec
-> Set time min and sec --> press '*' to clear time [ or ] press '#' to set time
-> in order to set time press MPK switches from 0 to 9
-> once the time is set and entered --> time should decrement from the set time and fan should be on till time reaches 00:00
-> in this menu display operations as follows
-> start/resume :
-> start the timer if it is in pause mode --> MPK4 is used
-> increment the time by 30 sec if it is in run mode --> MPK4 is used
-> Pause : Pause the timer --> MKP5 is used
-> stop : stop the timer and return to main menu display --> MKP6 is used
-> after the time reaches 00:00 --> display " Times up Enjoy your meal " for 3 sec --> Buzzer should be on for 3 sec and fan OFF
-> returns to main menu screen

2. Grill Mode : [ Same as Micro mode ] --> MKP2 is used to enter into this mode

3. Convection Mode : MPK3 is used to enter into this mode
-> Set temperature from 0 to 180
-> press '*' to clear temp [ or ] press '#' to set temp
-> enter into pre heating mode and display time count of one min in this mode
-> goes to display set time [ same as micro mode from run operation till end]
-> if the temperature entered is more than 180
-> display Invalid temperature for 3 sec
-> return to set temp screen

4. start Mode :
-> MPK4 is used to get into this mode
-> After entering in to this mode Time decrements from 30 sec
-> same start, pause, stop is used
-> after 30 sec display message " Times up Enjoy your meal " for 3 sec --> Buzzer should be on for 3 sec and fan OFF
-> go back to main menu screen
