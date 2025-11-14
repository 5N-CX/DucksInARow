# DucksInARow
Step-by-step Saintcon 2025 Presentation:
https://youtu.be/OfddHMtNwCE?si=MtG3GHDrH6x4NM-P

Get Your Rubber Duckies in a Row 
Presented by Madeline Kaye (5N-CX) 
 
Let’s use an ATTINY85 development board to make rubber duckies! We will program it through Arduino IDE. https://www.amazon.com/AiTrip-Digispark-Kickstarter-Attiny85-Development/dp/B0836WXQQR/ref=sr_1_2?crid=1NIANG8A31TVA&dib=eyJ2IjoiMSJ9.WMlZ_YfTi4TD17TYNrMUiWDfcOWXzDZuqR1NTeAg2Nk5Ai1Wtba7LmH8LZ_DgXp2tazVpNttP7uJb9HAt6NfiyasJc6UjyrBP4jZSpkX3O7hZPaOb-dVobyLWWHKOHaKqIKVo7_N2czQ4eDNW3yR-rs2l0Pnat4-uyfuqYQzLmflCZs1qCnkaZ6MzDTxYVOWdMBVVDMFKxskTnrPoR1_UWSEBkP4aOKR_jX5LomyN8w.RKUyVyVhQL3PldN3rpdyFIaYnGejV7VH1NVg71FXtGk&dib_tag=se&keywords=rubber%2Bducky%2Busb%2Battiny85&qid=1763144895&sprefix=rubber%2Bducky%2Busb%2Battiny8%2Caps%2C258&sr=8-2&th=1

*You are free to modify the code of your rubber ducky, as you wish, but these repositories are meant to include code that cannot be used in a malicious or illegal manner. These codes are only meant to be used for educational purposes for an individual looking to learn more about Arduino IDE, and how to use the runbox on their own offline, personal computer. I use a burner computer to download the libraries, board manager, zadig, and other unfamiliar code, and I recommend you do the same to be safe.*


First, download Arduino IDE from their website: www.arduino.cc/en/software 
*For this talk, we will be downloading ‘Windows Win 10 or newer (64-bit)’ 
*For additional installation options, click on ‘legacy IDE 1.8.19’ 

After Arduino finishes installing, let’s add a board manager now.  
Using the toolbar at the top, navigate to file > preferences 
On the preference pop-up, scroll down and add the following URL to where it says, “Additional Boards Manager URL” 
https://descartes.net/package_drazzy.com_index.json 

Now, using the left hand toolbar, click on the “boards manager” icon and search for “ATTinyCore by Spence Konde” and install this. 

Next, you will need to add a library.  
Towards the top of the screen, click on tools > manage libraries and search for ‘ATTinyCore by Spence Konde’ and click on ‘install’ 
If it gives you an error that it could not install this, try installing a previous version. On my own computer, I had to install the 1.3.3 version on various devices 

After the installation of the library, go to tools > board > and hover over it to select ‘ATTiny 45/85 (optiboot)’ 

**Now, the next tool we will use can change drivers, so if you do not use it properly, you can disable your mouse, keyboard, bluetooth, or other things on your laptop. Please follow the steps below carefully to ensure you don’t acidentally replace the drivers on the wrong component. **

Before we program the dev board, we need to change the driver of it by using ZADIG. http://zadig.akeo.ie/ 
The ATtiny85 does not have built-in hardware support for USB and relies on a software-based bootloader, which Windows does not automatically recognize, which is why we need to replace the driver before it can be recognized. 
Now let’s load up the payload! 

Navigate to my “DucksInARow” repository to pick which payload you’d like to download: github.com/5N-CX/DucksInARow 

Once you select the code, copy all lines, and paste to replace the text you see in Arduino IDE. 
Towards the top of the page, click on “verify” and look towards the bottom right hand side for the status message, letting you know when it is done verifying. In this process, Arduino checks for syntax errors and compiles it into a binary file without uploading it to the board. 

Make sure your ATTiny85 is no longer plugged in. Right next to the ‘verify’ button at the top, click on ‘upload’ and wait before you plug in your dev board. It will prompt you once it’s ready and it will give you 60 seconds to do so. Once it’s plugged in, give it about 10 seconds and if it says, “micronucleus done”, then your code is ready! 

The way we programmed this ATTINY 85 makes it so that it is recognized by the system as a USB for about 5 seconds, and then goes into auto-run mode, so as soon as the code is uploaded, it will immediately run on your computer. 

Your rubber ducky is now ready! Please find me on Discord or LinkedIn, if you'd like to share your feedback with me.
