# Linux-basic_FOE-SJP
try to be fammilier with linux operating system
Task Overview
Start the Oracle VM VirtualBox and install Linux in VirtualBox according to the given instructions.
Practice basic Linux commands.
Open a text editor and write a simple C program. Then compile and run it using the Terminal.
Installing Ubuntu in Oracle Virtual Box
First, download VirtualBox and Ubuntu (2.6 GB) following the links. Then, install VirtualBox in your computer and follow the instructions given below to install Ubuntu on it. If you have already installed Ubuntu on your computer, you can skip this section.

Initial VirtualBox Settings
First, Start Virtual Box on your desktop, and click on the New icon. Give the virtual OS a proper name such as Ubuntu2018. Select Linux as Type and Ubuntu (64-bit) as Version. Then click on the Next button.

Set the memory size by moving the slider. The recommended size of memory for the virtual machine is 2 GB (2048 MB) as the system has only 8 GB of RAM. Then click on the Next button.

Now, select an existing virtual hard disk file. Use the third option and select the already created Virtual Hard Disk (E:\Linux2018.vhd) by clicking the folder icon. This works like the hard disk of the virtual Linux system. This is where the virtual system will store its files. Then click the Create button.

You will get a screen like this.


Virtual OS Settings
Now you are going to set the settings of Ubuntu by just clicking the Settings icon.

Go to System -> Processor
Change as 2 processors

Go to System -> Motherboard
Enable I/O APIC

Go to System -> Acceleration
Enable VT-x/AMD-V

Go to Display -> Screen
Enable 3D Acceleration

Go to Storage -> Controller: IDE 
Change the optical drive to the Ubuntu ISO file. Click the CD drive icon and then select the Choose Virtual Optical Disk File… option. Then locate the Ubuntu-18.04-desktop-amd64.iso (downloaded Ubuntu ISO) file. 

Go to Audio -> Enable Audio Input

Go to User Interface -> Enable Show at Top of Screen and click Ok.

Installing Ubuntu
Once everything is in place, it is time to boot that ISO and install Ubuntu as a virtual operating system by clicking the Start button.

If Virtual Box doesn’t detect the Ubuntu ISO file, browse to its location by clicking the folder icon. Then click on the Start button.






Soon you’ll find yourself inside Linux. You should be presented with the option to install it by pressing the Install Ubuntu button.

Select the keyboard layout as English (US). Then, click on Continue.

Now select the Normal installation and Download updates while installing Ubuntu. Then click on Continue.

Select ’Erase disk and install Ubuntu’. Don’t worry. It won’t delete anything on the Windows operating system. You are using the virtual disk space of 10 GB that we selected in previous steps. It won’t impact the real operating system. Then select Install Now. Just click on Continue.

Now you must select the correct location (Colombo) from the given map. Then click on Continue.

Choose a username and password.

You are almost done. It should take 10-15 minutes to complete the installation.

Once the installation finishes, restart the system.

If it gets stuck on the screen, you may press the Enter, or you may close the VirtualBox and just click on the installed Linux virtual machine. You’ll be able to use it directly. 

Login by entering your login password. A KDE (Kool desktop environment) should spring up.

Practising Basic Linux Commands
Start a Terminal window by using the App Drawer (Or Press Ctrl+Alt+T). 

Use the following command to check your current location. What does it say?

$ pwd





If you are not in your home directory, change your current location to your home directory.

$ cd /home/student 
or 
$ cd ~

Use the following command to list all files in your current location. What are the files you have?

$ ls





If you don't already have one, create a directory called “Labs”, then go into that folder, and create a directory called “Lab1”.

$ mkdir Labs
$ cd Labs
$ mkdir Lab1

Change directory to Lab1. What is the command you must use?





Check the address of your current location and write it below.





Go back to Labs directory using the following command.
$ cd ..

Go back to the home directory. What is the command you must use?





Examine the differences between ls and ls –l. What does column 8 show?





Make subdirectory named as Lab2 inside the Labs directory while staying at the home directory. What is the command you have to use?





Run the following command. Explain what happens.

$ clear





Compile and Run a C Program
Open the terminal window and run the following commands to install the C compiler.
$ sudo apt install gcc
$ sudo apt install make

You may have to enter the password of the user account (Password is not visible when you type it).

Move to the Lab1 directory and create a new source file named as Hello.c using the following command. It will open the file in a text editor.
$ gedit Hello.c

Write a simple C program to print “Hello World..!!” to the terminal.

#include <stdio.h>
int main(){
printf(“Hello World..!!\n”);
return 0;
}
Save the changes and close the text editor.

Run the following command to compile the source code. It will create an executable file name as “Hello” in the same folder.
$ make Hello

Run the following command to execute the program
$ ./Hello

Edit your code, compile it, and run again to practice.

Examine and Manipulate Files
Go into the Lab1 directory and run the following command. What is the output?
$ more Hello.c





Copy your Hello.c file to Lab2 sub-directory. 
$ cp Hello.c  ../Lab2/ 

Move to Lab2 directory and run the following command. Then check what has happened using the ls command.
$ mv Hello.c  Hello2.c 





Move the Hello2.c file to Lab1 directory using the following command.
$ mv Hello2.c  ../Lab1/

Delete the Lab2 directory. First, you have to move out of the Lab2 directory.
$ cd ..
$ rmdir Lab2

Delete the Hello2.c file from Lab1 directory.
$ rm Lab1/Hello2.c

Go into the Lab1 directory and check the content of it. What are the commands you have to follow? 





Some Helpful Linux commands

man
Manual. Give this command along with the command you need more information on, and a series of the manual will appear that describes how to use the specified utility.
cd    
Change Directory. Use cd to move to different directories on the network.
cd ..  
Moves you up one directory in the tree.
cd ~
Moves you to your “home” directory.
pwd
Present Working Directory. Use pwd to see the name of the directory you are currently in.
ls  
Show list. Use ls to see the contents of your current directory.
ls –l
List (Long option). Use ls –l to see file properties.
ls –a 
Will list all files in the directory (including “hidden” files).
rm 	
Remove files.
mv  	
Moves a file from one directory to another or rename a file.
cp  
Copy. Copies a specified file or files from a specific location to another specific location (directory). Source and destination files, with paths, must be specified.
mkdir  
Make a directory.
rmdir  
Remove a directory.
more 
Will display an ASCII text file on the screen.

