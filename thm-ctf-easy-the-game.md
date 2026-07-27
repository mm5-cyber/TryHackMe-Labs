
# THM CTF Challenge: The Game 

Tools used: 

- Kali OS (Linux) 
- Linux "Strings" Command-line Utility tool

Difficulty: Easy 


## Objective 

The objective of this room is to uncover secrets (the flag) within the popular video game Tetris. The goal of this room is to uncover the encrypted data buried in the code. 

To reveal the flag I did rely on quick walkthrough as I did not much of an idea on how to complete this CTF as it's my first. Walkthrough's are important for learning how to do capture the flags because they teach the proper methodology. I followed the video by Anonymous World on this specific room (Anonymous World, 2025). 



## Steps 

<b> Step 1: Download and Unzip the provided task files. </b> 

I downloaded the files by clicking on the blue "Donwload Task Files" button within the room's objective secting.

<img width="1170" height="357" alt="image" src="https://github.com/user-attachments/assets/b7d3d5ff-c8f3-47b7-a6df-4428e81f2cbe" /> 

<sub>THM "The Game" room objective section, featuring the download button (THM, n.d.)</sub> 

This was pretty simple, after downloading and unzipping the file, there was a "Tetrix.exe" application file. 

<b>Step 2: Using the command to find the flag </b> 

The command used was "strings Tetrix.exe | grep "THM"" 

<img width="625" height="124" alt="image" src="https://github.com/user-attachments/assets/d4964434-ac31-4a61-ad9c-8b554e7c55e9" /> 

<sub></sub>


## Sources 

THM, n.d., The Game, THM website, viewed, 27th July 2026, Accessed:<https://tryhackme.com/room/hfb1thegame> 

Anonymous World, 2025, The Game Walkthrough | TryHackme | 5 Minute Hacks, Youtube website, viewed 27th July 2026, Accessed: <https://www.youtube.com/watch?v=HRAFg2ga0FM>
