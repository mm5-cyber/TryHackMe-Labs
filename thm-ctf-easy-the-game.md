
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

I downloaded the files by clicking on the blue "Download Task Files" button within the room's objective secting.

<img width="1170" height="357" alt="image" src="https://github.com/user-attachments/assets/b7d3d5ff-c8f3-47b7-a6df-4428e81f2cbe" /> 

<sub>THM "The Game" room objective section, featuring the download button (THM, n.d.)</sub> 

This was pretty simple, after downloading and unzipping the file, there was a "Tetrix.exe" application file. 

<b>Step 2: Using the command to find the flag </b> 

I was shown the Linux's string command in the walkthrough. This is what will be used to find the flag.  

According to the manual page for the command, which I viewed on die.net, The Linux "strings" command-line utility tool finds and prints text characters that you can read inside non-text files, like programs or data files (die.net, n.d.). This is exactly what is needed in the lab, as the task is to find a flag buried within its code. 

The command I used to find the flag was "strings Tetrix.exe | grep "THM"". I typed the command, than highlighted the executable, and used the | grep "THM" to filter the output and display only the lines containing the keyword "THM". This keyword is common in nearly all the THM flags, I've come across while learning on this site. 


<img width="625" height="124" alt="image" src="https://github.com/user-attachments/assets/d4964434-ac31-4a61-ad9c-8b554e7c55e9" /> 

<sub>Finding the flag using the command within my Linux terminal.</sub>

The CTF is now completed. 

## Conclusion 

This introductory CTF gave me practical exposure to basic analysis techniques and showed how simple tools like the Linux strings command can reveal hidden data inside executable files. Although I relied on a walkthrough, it helped me understand the correct methodology and gave me a clearer foundation for approaching future challenges with more confidence.

## Sources 

Anonymous World, 2025, The Game Walkthrough | TryHackme | 5 Minute Hacks, Youtube website, viewed 27th July 2026, Accessed: <https://www.youtube.com/watch?v=HRAFg2ga0FM>

Die.net, n.d., strings(1) - Linux man page, die.net website, viewed 29th July 2026, Accessed: <https://linux.die.net/man/1/strings>

THM, n.d., The Game, THM website, viewed, 27th July 2026, Accessed:<https://tryhackme.com/room/hfb1thegame> 


