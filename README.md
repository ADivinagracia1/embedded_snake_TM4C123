# MSE450 Project: Embedded Snake Game 

Write an interactive program on the TM4C123 microcontroller utilizing timers, interrupts, peripherals, and an output screen. Apply a data structure in your application.

[![VirtualSnakeGame](https://markdown-videos-api.jorgenkh.no/url?url=https%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3DpFEp2IjxQ0Y%26ab_channel%3DAtodo)](https://www.youtube.com/watch?v=pFEp2IjxQ0Y&ab_channel=Atodo)

This is a project I am quite fond of. This is a very low level system and we developed a running application on a microcontroller. This is a legacy project, im quite fond of our little comments around the git files. Please excuse some of what's written here. This is more sentimental than technical, but I may build a physical version of it. 

-------

## Team:
- Andrei Divinagracia
- Zainab Vajahath
- Dexter Zamora

## Random Notes:
- When building files, always click "Rebuild" then start debug session (ctrl+F5)
- View simulator: Peripherals > TExaS Port F
- View UART msg: ON taskbar: Serial Windows > Uart #1

## Project/VirtualSnake notes:

### Pushing to git
When pushing updates to git, it is very imporant to close your uVision4 window before doing the git commands. This casues the files you pushed not being entirely saved to the github cloud. It is like trying to send a PDF to send someone a PDF file while having the PDF file open on your machine. Not closing your uVision4 project would result in merge conflicts like in Zainab's branch, and would cause the pushing + debugger conflict as seen below. 

### Pulling from git + debug error
There is a common issue when pulling a new file, where the debugger will have issues runing. A fix for that is when a new .c file is added, you must manually add that to the project. The steps below will show an example for Movement.c:
- RClick Source
- Click "Add existing to project group"
- Find the file that you want to add, in this case, Movement.c
- The header files do not need to be included, just the .c files
- Rebuild the project

- June 7th lecture explains how to make new uproj file

## Meeting Notes:

(June 22)
- use left and right buttons to control snake on TEXaS ADC
- Snake is always moving forward
- Implement snake speeding up in release 2
- focus on getting snake as a pixel and food as a pixel



(June 8)
- There's 3 sections we need to implement
	- Draw
	- Input 
	- Logic (game logic)

- We need to setup inputs and draw
	- We want to see the snake
	- We want to make it move
	
- Drawing the snake involves being able to see things on the LCD screen + communication protocol between Tiva and LCD screen

- Inputs to the screen == GPIO, interrupts, push buttons

- In 2 weeks we need draw and input finished
	- A dot we can control with up/down/left/right

- Logic and drawing are completely different from each other and will be implemented differently

