# Python

## Table of Contents
* [Complexity](complexity)


### Complexity

#### Asymptopic Notation or Analysis
* Allows us to explain how an algorithm behaves as the input grows larger
* Two Parameters:
	* Time Complexity - How long an algorithm takes to run depending on it's input size (CPU or computing power)
	* Space Complexity - how much memory is required depending on the input size (RAM)
* 3 Forms: Big-O, Big-Θ , Big Ω


##### Time Complexity

| Big Ω (Big-Omega) | Big-Θ (Big-Theta) | Big-O  |
|-------------------|----------------|-----------------------|
|lower bound (or best case senario)  |average case scenario |Upper bound (or worst case senario)  |
|![Big Omega](https://photos.app.goo.gl/vGpbwZHxWkUbbYydA)	|![Big Theta](https://photos.app.goo.gl/p6ZwQAKqDHGL99hN6)	|![Big-O](https://photos.app.goo.gl/6SU2ERVj1x9eAxNo8)	|


**R** 
(how long algorithm takes in terms of the size of it's input (time))
1. Different steps get added - Running time is the sumation of all fragments
2. Drop constants 
3.  Different inputs => diffferent variables 
![Example of Naming Variables for Big O](https://photos.google.com/album/AF1QipPfjm3PHBCiN_eT1T8CAOtzKh6txR99WmTXPr93/photo/AF1QipO6ti8ZlIrT-mqBlEtWesSHBGwYwH0puYWkqJxw)
4. Drop non-dominate terms 
Example: O(n<sup>2</sup>) > O(n)

Note: the specifics (processor, memory, 32/64 bit) of the machine are not considered

**Order of Complexity**
![Order of Complexity](https://photos.app.goo.gl/Cz5trQN5iHiCPpho7)

#### Space Complexity
* Measure of how efficient your code is in terms of memory used

**Resources**
 [Big O Explained](https://www.youtube.com/watch?v=v4cd1O4zkGw)
 [Khans Academy](https://www.khanacademy.org/computing/computer-science/algorithms/asymptotic-notation/a/asymptotic-notation)

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE0MjA2MTI1OTYsLTIwMDUzODM3MDksMT
U0MDAwMDY4NSwxMzkyMzQwOTk1LDIxMjA2MzUzNjYsLTE1MTM4
NDUyMDIsMTgwNDU0NDI3N119
-->