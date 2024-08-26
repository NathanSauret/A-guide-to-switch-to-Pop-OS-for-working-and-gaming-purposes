# A guide to switch to Pop!_OS for working and gaming purposes

</br>

I've used Pop!_OS for one month now and I had some minor problems.  
I found the solutions to my problems and I want to share them, it's a guide to help you to setup Pop!_OS for working and gaming purposes.  

</br>

## Gaming
### - Get every games to works with Proton in Steam:  
When you want to install a Windows game it don't let you install it? It's normal, you have to change a setting.  
To do so, activate *Enable Steam Play for supported titles* in the Compatibility settings.  

![image](https://github.com/user-attachments/assets/afe78bac-b5d8-4b85-b320-f85c9f4b087a)

### - Better Steam rich presence on Discord:  
On Linux, Discord will normally display Steam games with weird names and without the game icon.  
To solve this problem you can install this program: https://github.com/JustTemmie/steam-presence  

BEFORE:  
![Screenshot from 2024-08-26 18-01-38](https://github.com/user-attachments/assets/6aa4b4e1-63c1-4730-8d0f-76d889205f90)  

AFTER:  
![Screenshot from 2024-08-26 18-01-02](https://github.com/user-attachments/assets/8d54e886-3238-4851-9950-43b0f4598100)  

</br>

## Solve techincal issues:  
### - Have the audio share on Discord:  
In Discord you can share your screen but it will not share the audio.  

![image](https://github.com/user-attachments/assets/9c17e5e5-efdb-49df-99f4-ae0680b37a58)

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

Finally, change the microphone source in Discord to the virtual microphone and disable the Noise Suppression so your friends can hear all the audio and not just people speaking.  
You can also set the Input Sensitivity to the minimum to hear the whole audio without cuts.  

</br>

## Upgrades
### - Better store:  
The Pop!_shop is great but it's sooo slow.  
Instead you can install the COSMIC App Store, it's the same thing but faster (coded in Rust), simpler to use and prettier.  
This store is also made by System76 but it's a beta version of what is going to come in Pop!_OS.

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


### - Customize RGB:  
To customize your RGB devices you can install "OpenRGB".  
It's compatible with most products of popular brands like Corsair, Razer, NZXT or Logitech.  

![image](https://github.com/user-attachments/assets/62375ab1-5684-4885-9564-25ec0c81d0bc)

### - Better system monitoring:  
The basic system monitoring is not user friendly as the Windows one and don't display all the informations.  
A better system monitoring is "Resources", you can install it in the store.  

![image](https://github.com/user-attachments/assets/e7c2d7a5-b7e7-4a2d-872d-cf804b3f5fd7)

### - Make apps background transparent:  
This one is a bit gadget but it looks so cool.  
To make the backgrounds of your apps transparent, activate "Blur my shell" in the Extension Manager (gnome extension).  
Then select the apps you want in the Applications panel of the Blur my shell settings.  

![image](https://github.com/user-attachments/assets/3b10ac0d-f790-4558-b194-89f4c0a10991)  

Result:  
![image](https://github.com/user-attachments/assets/110bda4c-818d-4662-b8b3-86ed4421bd62)

</br>

I hope you found this guide helpful.  
If something don't works like espected, let me know.  
