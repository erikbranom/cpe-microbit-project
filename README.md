# CPE micro:bit Term Project

Term project for students in the CPE 1040 course at MSUD, Fall 2018.

## Assignment

Design and implement some application of the [micro:bit](https://microbit.org/) educational computer. It can be a new design of your own or an already existing design from the Web.

### Language requirement

The implementation has to be in [MicroPython](https://microbit-micropython.readthedocs.io/en/latest/) (the version of Python that works on the micro:bit). 

**Note:** It is perfectly acceptable to take a project implemented in JavaScript/Blocks and rewrite it in MicroPython.

## Submission

### 1. Github

Fork and clone this directory and submit the URL of your fork (remote) on [Canvas](https://canvas.instructure.com/courses/1397722/assignments/10046266?module_item_id=20700270).

### 2. Individual

You can collaborate with one or two team mates on the design, implementation, and testing of the project, but you have to have *your own* separate Github repository and make an *individual* submission on Canvas.

### 3. Due date

**Sun, Dec 2, 2018, by 23:59**

**Note:** You can submit your URL at any time before the deadline on Canvas. Only your latest commit on Github earlier than the deadline will be evaluated.

### 4. Project report

Write the project report in your README using the template provided below. 

**Note:** Projects without reports will receive **0 points** for the whole project.

### 5. Project demo

The project has to be demonstrated by the team in the lab period on **Wed, Nov 28**. Presentation slides are *optional* but will be noted in the evaluation of your submission. If you can't make this date, you can demo at any *earlier* date, but no later dates.

**Note:** The demo is **not optional**. If a project is not demonstrated, the grade will be at the discretion of the instructor.

## Grading

The project is worth a total of 600 points. Breakdown:

| Criterion | Points |
| --- |:---:|
| Functionality of application | 300 |
| Good use of [micro:bit](https://microbit.org/) capabilities | 100 |
| Input and output | 50 |
| Complexity of the application | 50 |
| Quality of demo | 50 |
| Clarity of report | 50 |

# Project Report

Fill out this template in place in the README of your own fork of the assignment repository. Put any supporting materials (diagrams, schematics, pictures, presentation slides, etc) in the [assets](assets) folder. You can reference them from this report. For example, [todo file](assets/todo.md). Use this [Markdown cheat sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) to format the report.

**Acknowledgement:** Adopted from [Bob Yusko](mailto:ryusko1@msudenver.edu).

## 1. Project Title

Multiplayer Battleship

## 2. Team

I worked alone crerating this project.

## 3. Project Objective

Earlier in the semester I wrote a Javascript Battleship game for my computer science class. The program was a remake of the popular multiplayer game battleship. The game allowed you to choose the placement of your own ships and compete against a cpu which generated random ships. The cpu had different difficulty levels each with different algorithms that could accurately sink your ships. My goal for this project was to try and create a similar version of my game that allows you to play against another player instead of a cpu. 

## 4. Research

For the construction of this project I got help from Professor Ivo, Professor Rajan, and followed the tutorial from chapter 10 of the book Networking With The Micro:Bit. https://microbit.nominetresearch.uk/networking-book/networking_with_the_microbit.pdf 

## 5. Design

Given that the microbit only has a 5x5 matrix I had to make adjustments to my previous 10x10 game I created in javascript. The game starts off by using a while loop to randomly generate 5 ships in a 4x5 matrix. The microbit will output an LED signal to show the location of your ships. The function calls for all ships to be placed in the bottom four rows of the LED matrix allowing room in the top row to display whether the shot fired was a hit or miss. The microbits connect remotely since they both have the same radio group number. When firing a shot, the microbit takes input from the A button pressed, B button pressed, as well as the A+B button pressed. Pressing the A button on the microbit changes the fire_x or the colomn in which you wish to fire a shot. Each press moves the fire_x position to the right and when pressed on the last LED to the right will reset it on the left. Where as pressing the B button changes the fire_y or the row you wish to fire a shot. Pressing A+B at the same time fires your shot and sends a radio number to the enemy that will go though an if statement to determine if the shot hit or miss. If the shot landed, an LED will light up on the top left corner of the matrix and the LED of the sunken ship will unplot. 

## 6. Development

My original plan was to follow the blocks tutuorial and convert it to Micropython. Though after help and discussion from the professor, it was decided that blocks code would be sufficient since I worked alone on the project.

## 7. Testing

When testing the game, I had trouble getting the code to transfer to the microbit, and struggled to run the game on the microbit itself. I created the full game using micro blocks that ran seamlessly on the simulator but when I programmed the same code to the microbit I got a blank screen. After breaking down the code and downloading over 20 different hex files of the game, I found that the problem was occuring because I did not have the plot function for the ships included in the while loop. 

## 8. Demo

The in class demo perfectly summarized and demonstrated how the game works, the inputs, outputs, and storage used, but at the time I did not have the Battleship game fully functional on the microbit, only the simulator.

## 9. Summary

This project as a whole taught me alot about writing code to program other devices. MicroPython required much more knoledge than just the basics of programming. MicroPython was a new language that has its own functions to accomodate the microbits features. My final game is not what I wanted it to be. I plan to continue working on this game to make it what I originally envisioned and to make it easier to understand and play.
