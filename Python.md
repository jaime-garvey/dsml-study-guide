# Python

# Table of Contents
* [Standard Input & Output](Standard Input & Output)
* [Complexity](complexity)

## Standard Input & Output
<details><summary>Summary</summary>
<p>

### Summary (Standard Input & Output)
* the _builtin function input` reads input from the _standard input stream (`sys.stdin`)<br/>
* the _builtin function`print` prints output to the _standard output stream_ (`sys.stdout`)<br/>
* the _standard error stream_ (`sys.stderr`), to which unhandled exceptions get printed<br/>

**Note:** a **stream** is a sequence of data elements made available over time  
</p>
</details>
  
## Complexity

<details><summary>Asymptopic Notation or Analysis</summary>
<p>

### Asymptopic Notation or Analysis
* Allows us to explain how an algorithm behaves as the input grows larger <br/>
* Two Parameters: <br/>
	* Time Complexity - How long an algorithm takes to run depending on it's input size (CPU or computing power)<br/>  
	* Space Complexity - how much memory is required depending on the input size (RAM) <br/>
* 3 Forms: Big-O, Big-Θ , Big Ω <br/>

</p>
</details>

<details><summary>Notation</summary>
<p>
#### Notation

| Big Ω (Big-Omega) | Big-Θ (Big-Theta) | Big-O  |
|-------------------|----------------|-----------------------|
|lower bound (or best case senario)  |average case scenario |Upper bound (or worst case senario)  |
|![Big Omega](https://photos.app.goo.gl/vGpbwZHxWkUbbYydA)	|![Big Theta](https://photos.app.goo.gl/p6ZwQAKqDHGL99hN6)	|![Big-O](https://photos.app.goo.gl/6SU2ERVj1x9eAxNo8)	|

</p>
</details>

<details><summary>Calculating Complexity</summary>
<p>
#### Calculating Complexity  
(how long algorithm takes in terms of the size of it's input (time))  
1. Different steps get added - Running time is the sumation of all fragments  
2. Drop constants   
3.  Different inputs => diffferent variables   
![Example of Naming Variables for Big O](https://photos.google.com/album/AF1QipPfjm3PHBCiN_eT1T8CAOtzKh6txR99WmTXPr93/photo/AF1QipO6ti8ZlIrT-mqBlEtWesSHBGwYwH0puYWkqJxw)
4. Drop non-dominate terms   
Example: O(n<sup>2</sup>) > O(n)  

Note: the specifics (processor, memory, 32/64 bit) of the machine are not considered  

#### Order of Complexity
![Complexity Graph](dsml-study-guide/images/Complexity%20Graph.png)

</p>
</details>

<details><summary>Resources</summary>
<p> 
**Resources**
 [Big O Explained](https://www.youtube.com/watch?v=v4cd1O4zkGw)
 [Khans Academy](https://www.khanacademy.org/computing/computer-science/algorithms/asymptotic-notation/a/asymptotic-notation)

</p>
</details>


> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbNjQ1OTM2MTc0LDY0NTkzNjE3NCwxMTQzMj
MxMzI3LDEwODUxNzMxMjIsLTEyNzA5NTM0NDQsLTIwMDUzODM3
MDksMTU0MDAwMDY4NSwxMzkyMzQwOTk1LDIxMjA2MzUzNjYsLT
E1MTM4NDUyMDIsMTgwNDU0NDI3N119
-->