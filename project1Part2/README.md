# Human-Centered Input Recognition Algorithms - Online/Live Recognition - Project 1 Part 2

## Goals:
- The goals of part 2 of project 1 are as following:
  - store the points generated by the mouse or touch events on your canvas
  - store a default set of templates to compare new candidate (input) gestures to
  - implement the $1 recognition algorithm and call it when a gesture is drawn
  - output the result of the recognition call to the GUI onscreen

## Steps to run the project:
* Compile the project1Part2.java file\
```javac project1Part2.java```
* Run the project1Part2.java class file\
  ```java project1Part2```
* Click on clear button on canvas to clear the canvas
* Draw any gesture and click on output to recognize the gesture
* Click on close button of the canvas window to close the application
  
  
## Goals explained in detail:
### store the points generated by the mouse or touch events on your canvas
   * As the user makes gestures on the canvas, the points are captured and stored in an internal data structure in the mouse / touch event listeners.

### store a default set of templates to compare new candidate (input) gestures to
   * Used the stored gesture templates from the demo on the $1 recognizer homepage (http://depts.washington.edu/acelab/proj/dollar/index.html), located in dollar.js starting on Line 127.

### implement the $1 recognition algorithm and call it when a gesture is drawn
  * Using the pseudocode and reference implementation on the $1 recognizer homepage, I implemented the four steps of the recognition algorithm: (1) resampling, (2) rotation, (3) scaling + translation, and (4) matching process.
  * Each of these steps require multiple methods. 
  * I preprocessed templates at instantiation, and candidates (input) at input time.
  * I called the recognizer when a gesture is made on the canvas by clicking the ouput button.
   

### output the result of the recognition call to the GUI onscreen
   * After the recognition has returned a result, I displayed the result to the GUI.
   * The label of the template that had the best match to the input is displayed, along with the score through a display pop-up.
   
## Demo
![project 1 part 2 demo](https://github.com/sheelaippili/CIS6930-Human-centered-Input-Recognition-Algorithms/blob/main/project1Part2/project1Part2GIF.gif)
