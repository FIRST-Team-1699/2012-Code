AUTO SCRIPT Notes
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
Robot Commands:
WAIT  [ Milliseconds]     	-1000 Milliseconds = 1 Second- Enter time you want wait or hold.
STOPALL			- Stops Drive motors (sets input to zero)
DRIVE_TIME [ Time] [Speed] 	- (time in Seconds) (speed +/- 1.0 - 1.0 = Full Scale)- Drive straight for a give time at a given rate.
DRIVE_STRAIGHT  [Distance] [Speed] - (distance in Inches) (speed +/- 1.0 - 1.0 = Full Scale)- Drive for a given distance based on Encoder output at a given rate.
											    - Note  : Encoder must be working to use. 
DRIVE_CAMMERA  [(Distance] [Speed] - (distance in Inches) (speed +/- 1.0 - 1.0 = Full Scale)- Drive for a given distance based on Cammera output for a given 											       rate.
DRIVE_SIDEWAYS  [Time) [Speed)    - [time in Seconds] [speed +/- 1.0 - 1.0 = Full Scale] - shaff Right or Left for a given time and rate.
ROTATION_TIME ( Time) [Speed)    - [time in Seconds] [speed +/- 1.0 - 1.0 = Full Scale] - Rotate for a given time (Seconds)
TURN_GYRO ( Angle) [Rate]    - [angle to turn too] [rate +/- 1.0 - 1.0 = Full Scale] -  Turn to a given angle based on GYRO out put.
ARM [Hold time after ARM is lowered down] [time in secounds to allow ARM to be lowered] -Arm moves at a set rate, enter time  in seconds from start of 												  movement to end of movement  , enter time to hold after lowered to 											  bring back-up to start location.
SHOOTER [Shooter power] [user input for shooter power[ - Shooter power enter - 1.Frount of the 3 point target   -  User Input -(rate +/- 1.0 - 1.0 = Full Scale) 
                         						       2. Frount of 2 point target
                         						       3. Key frount of 3 point target 
                         						       4. User Input	
Script files:
Each command must have it's own line. Comments start with #. Comments must have their own
line, they cannot be typed after commands. Only commands registered in CreateCommands can be
called, if a command does not exist it will be skipped. Blank lines will also be skipped.




++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++Example:


#Auto_Test1.rcat
#Move forward for three seconds and shoot two balls
#then move back to starting point
#wait 250ms alow Auto to start
WAIT 250
#First 
#Go forward for three seconds at 1/2 speed
DRIVE_TIME 3.0 .50

#wait 250ms
WAIT 250

#Shoot ball at 65% powwer
SHOOTER 4 .650

#wait a little bit
WAIT 250

#Shoot ball at 65% powwer
SHOOTER 4 .650

#wait a little bit
WAIT 250

#Go backward for three second
DRIVE_TIME 3.0 -.50

#Stop and wait for tele-op
STOP

#EOF
