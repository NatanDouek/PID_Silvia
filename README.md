# PID_Silvia
Arduino PID control of brew temp on Rancilio Silvia

## But WHAT??
This is a ready to use arduino sketch based on the wonderful https://github.com/br3ttb/Arduino-PID-Library.git

## Check out Brett Beauregard's work! http://brettbeauregard.com/blog/

## HOW??
I used a MAX6675 module and a K type thermocouple with M3 thread. (Find on AliExpress).
* Add the MAX6675 Library to Arduino IDE
* Add PID by Brett Beauregard Library (It's in the library manager).

Tinker with Kp, Ki, Kd values untill you get a stable temp!

I added a serial output so you can read the temps and setpoints while tuning the system. Once you find the sweet spot you can comment out the serial output. It's not realy needed because there's more than enough memory on the Arduino. Also, there's no speed benefit becuse the polling rate of the MAX chip is 250ms. You'll notice the 250 delay after myPID.compute.