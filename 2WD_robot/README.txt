# README - IR Remote Control Car

## Important Instructions for Remote Control Usage

Before using the remote control to operate the car, please follow these steps to ensure
 proper functionality:

1. Run the Receiver Module Code: Execute the `Receiver Module` code to capture the hexadecimal 
values transmitted by your specific remote control. This step is crucial as remote control codes 
can vary between different devices.

2. Update the IR_Remote_Control_Car Code: After obtaining the correct hexadecimal 
values from the `Receiver Module`, open the `IR_Remote_Control_Car` code. Locate 
and replace the predefined hexadecimal values in the following definitions with the values you captured:

   #define IR_Go      0x00ff629d  //here
   #define IR_Back    0x00ffa857  //and here 
   #define IR_Left    0x00ff22dd   //and here
   #define IR_Right   0x00ffc23d   //and here
   #define IR_Stop    0x00ff02fd    //and here
   #define IR_ESC     0x00ff52ad    //and here

   Replace each 0x00ffXXXX value with the corresponding hexadecimal code from your
 remote control for the respective actions (Go, Back, Left, Right, Stop, and ESC).

3. Test the Setup: After updating the code, upload it to your Arduino and test the
 car with the remote to confirm that the commands work as expected.

Failure to update these values with your remote's specific codes may result
 in the car not responding correctly to the remote control inputs.