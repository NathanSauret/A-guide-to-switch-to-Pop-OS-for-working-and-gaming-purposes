# A-guide-to-swith-to-Pop-_OS-fro-working-and-gaming-purposes

</br>

## Gaming
### Get every games to works with Proton:  
Activate "Enable Steam Play for supported titles" in Compatibility settings  
  
Make apps background transparent: Activate "Blur my shell" in the Extension Manager (gnome extension), and then select the apps you want in the "Applications" panel of the Blur my shell settings  
Better system monitoring: install Resources  
Customize RGB: install OpenRGB  

## Solve techincal issues:  
### Have the audio share on Discord:  
This one is a bit tricky but you have to create a virtual microphone by tapping theses commands in the terminal:  
```
pactl load-module module-null-sink media.class=Audio/Sink sink_name=Virtual-Mic channel_map=front-left,front-right
pactl load-module module-null-sink media.class=Audio/Source/Virtual sink_name=Virtual-Mic channel_map=front-left,front-right
pw-link Virtual-Mic:monitor_FL Virtual-Mic:input_FL
pw-link Virtual-Mic:monitor_FR Virtual-Mic:input_FR)
```
Then set the monitoring device in OBS to the virtual microphone you've created in the Audio settings.  

![image](https://github.com/user-attachments/assets/cd5a08e7-ac94-41f2-9ccd-a4451892943e)

Now configure the audio channels in the Audio Mixer to monitor them (for exemple mic and desktop Audio).  
To do so, click on the gear on the right of one of your audio channel in the Audio Mixer, then on *Advanced Audio Proprieties*.  

![image](https://github.com/user-attachments/assets/b655717c-2b09-4834-8960-efca71dd8460)

Select the audio sources you want to add to the virtual microphone by setting them to *Monitor and Output*  

![image](https://github.com/user-attachments/assets/2e606b0c-695e-4703-a6f0-18a0c98edfb2)

Finally, change the microphone source in Discord to the virtual microphone and disable the Noise Suppression so you can hear all the audio and not just people speaking.  
You can also set the Input Sensitivity to the minimum to hear the whole audio without cut.  

## Upgrades
### - Better store:  
The Pop!_shop is great but it's sooo slow.  
Instead you can install the COSMIC App Store, it's the same thing but faster (coded in Rust), simpler to use and prettier.  
This store is also made by System76 but it's a beta version of what is going to come in Pop!_OS.

### - Better Steam rich presence on Discord:  
On Linux, Discord will normally display Steam games with weird names and without the game icon.  
To solve this problem you can install this program: https://github.com/JustTemmie/steam-presence  

BEFORE:  
![Screenshot from 2024-08-26 18-01-38](https://github.com/user-attachments/assets/6aa4b4e1-63c1-4730-8d0f-76d889205f90)  

AFTER:  
![Screenshot from 2024-08-26 18-01-02](https://github.com/user-attachments/assets/8d54e886-3238-4851-9950-43b0f4598100)  

### - Recording last 30s (or more):  
You can record the last 30s by using OBS with the Replay Buffer acivated.  
You can configure it in the Ouput settings, under Replay Buffer.  
To activate the Replay Buffer at the startup you can add ```obs --startreplaybuffer``` in the Startup Applications Preferences.  
If you did right an OBS icon with a red dot should appear on the top bar.  

![Screenshot from 2024-08-26 18-23-36](https://github.com/user-attachments/assets/c0493597-3bda-490c-93b0-4c829d40e947)

You can now configure a keybind to save the replay in the *Hotkeys* settings.  

### - Change the screen brightess:  
You can change the screen brightness by activate "Adjust Display Brightness" in the Extension Manager (gnome extension).  
Now you can click on the brightness icon on the top bar to ajust the brightness.  

![Screenshot from 2024-08-26 18-11-45](https://github.com/user-attachments/assets/fe5adb4d-690d-42f4-a204-cd6c7e69a8a5)

### - Add an Input/Output selector:
You can add an Input/Output selector by activate "Sound Input & Output Device Chooser" in the Extension Manager (gnome extension).  

![image](https://github.com/user-attachments/assets/006488ae-412c-4a42-acad-a04e63df6059)
