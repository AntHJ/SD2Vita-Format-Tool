# SD2Vita Format Tool
I Know its not perfect, but its helpful

# Running the tool

*RIGHT CLICK* the SD2Vita Format Tool.bat file and select 'Run as administrator' - this is needed due to needing permissions to repartition and format the drive.. on some computers you may get a security warning, just click 'More info' then click 'Run anyway'

# Using the tool

Select the location of the SD card you wish to blank, I have made the script try to work out your SD card location but PLEASE make sure you select the correct drive that shows your SD.. After selecting a drive a box will then show with details about your card. again make sure that the information shown reprsents the card you wish to blank / format.

If your card flags as fake, beware if you decide to continue, this could just be a miss calculation but as a rule, a genuine SD card should be 93% of there printed size. so for example :

        128gb   shows as between 116gb -> 119gb
        256gb   shows as aroud 238gb
        400gb   shows as around 372gb
        515gb   shows as around 476gb

once confirmed, the automated process begins. it will temporarily format the SD as a standard card and change its label. next the zzBlank.img will be flashed to clear all previous partitions. then it will determin which file allocation size it needs and formats accordingly.

Once the card has been prepared you will be asked if you would like to Clone the current Vita setup, you could just select NO and the app will will close. You would now need to make a backup of UX0 onto the SD

        Your SD card will NEED a copy of the Vitas UX0 drive, otherwise it will not boot up correctly and you may get stuck
        in a boot loop. if this happens, hold the L bumper as the system starts to boot from the origional storage instead.

# Clone / Upgrade an existing setup
for example, you can use this tool to copy data from a smaller SD onto a larger SD (Upgrade)

If you select YES and decide to clone/upgrade your current system setup you will need to prepare the Vita itself for the transfer. Unless the SD card is accessible with a 2nd Card reader.
To use the Vita as a card reader, do the following..

- Launch the VitaShell app
- Press the Start button and make sure USB Mode is set to the main storage,
    - Memory Card if your using the Sony memory
    - sd2vita if you currently have an sd2vita already running (i.e. Upgrade),
    - psvsd if your using a USB device or psvsd adaptor
- Press Start again to confirm the settings
- Press Select to start the USB Link
- Press Yes/OK on the computer to start the transfer process

After the files have copied, launch Autoplugin2 and goto the Vita plugins section and the sd2vita settings page. you now need to change the drive allocations to
  - MCD = NONE,   INT = NONE,   GCD = UX0,   UMA = NONE
  - if your using a psvsd or usb device then swap GCD = NONE to none and UMA to UX0
  - if you want to use your Sony memory card as additional storage, set MCD = UMA0
  - select save the goto exit for it to reboot the vita

you can now check Settings - System Information and confirm the SD card size
