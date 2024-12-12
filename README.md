Huddlecam movement through python with variable speeds, used for ui intergration for klipper.


Install pyserial with this command, you need it
"pip install pyserial" or "python3 install pyseiral" if locally manged env please add the flag listed at the bottom of the error message 
should be something like  "python3 install --bypassmanagenvblahblahblah pyserial"

if you are in fact using this for klipper and your linux freaks out either its not connecting to the camera or it kicks your printer off klipper
you may have to remove brltty with the command "sudo apt-get remove brltty" are restart your machine.

You must install gcode shell commands in klipper, personally I am running klipper of of linux for user interface. Personally to install this I need to use kiluah,
the installer for klipper on linux(mint). To do this you need to cd into the dir on the command line open up the kiluah folder and run the command "kiauh.sh" run the experimental
mode or whatever gets you to the community plugins and then install gcode shell commands.

Documentation for the camera can be found here https://huddlecamhd.com/wp-content/uploads/2021/01/HuddlecamHD-VISCA-Command.pdf, this absoutely sucks or I just suck at coding,
one or the other, I had chat gpt try to figure it out and it couldnt. The way I got most of the commands besides the stop commands were by using a serial port monitor found here 
https://www.aggsoft.com/serial-port-monitor.htm using it in spy mode, selecting the port booting up the control software(AFTER opening the serial port monitor.) found here
 https://huddlecamhd.com/camera-control-app/ clearing the text, preforming a single action, selecting the code, right click, copy hex only, and then ask chat gpt that 
 "I am using a serial port monitor to send visca commands over usb to a camera, the hex is as follows __Hex here__ I need the Visca command from this._"
 it will give you the visca command :), you can whatever the command is to the code, I don't want to add more as I dont need anymore functionality.

After that add the g code macros and CHANGE THE PATH to the python file in gcode shell commands.

Put the g code macros into the printer config file and then add the gcode shell command(two seperate commands). They can also be found in the code. Please enjoy this
and make it better if you want.
