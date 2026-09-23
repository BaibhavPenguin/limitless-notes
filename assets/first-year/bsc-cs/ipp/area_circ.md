# IPP &mdash; Area of Circle 
---
## <u>TITLE</u>
Write a program in python to find the area of a circle**  
---
### <u>EXPLANATION</u>
To find the area of a circle we will use the formula Area = &pi;r<sup>2</sup>  hence, we need to create two different variables for storing the radius and area.  

A Variable is a value either numeric or non numeric (encoded in ascii or utf-8) stored in Memory.  

To get user input we use the built in **input()** function of python, in simpler words, we are giving a command to the python interpreter to wait for the user and give them a chance to enter an input value. The input() function takes a prompt argument, the prompt is the message shown to the user while getting the input.

Python assumes that all user inputs are Strings by default so we must convert the string to an integer type before processing it.


<link rel="stylesheet" href="./styles/python.css">
<div class="code-sandbox-wrapper">
  <div class="py-status-badge">
    <span class="py-status-dot"></span>
    <span class="py-status-text">Waiting</span>
  </div>

  <div class="code-island">
    <div class="code-island-header">
      <div class="code-header-left">
        <span class="code-island-title">Python Sandbox</span>
      </div>
      <button class="code-run-btn" onclick="runPythonCode(this)">▶ Run</button>
    </div>
    <div class="code-island-body">
      <div class="code-source">
        <div class="code-gutter">1</div>
        <textarea readonly
          spellcheck="false" 
          placeholder="Write Python code here..." 
          oninput="updateCodeGutter(this)" 
          onscroll="syncCodeGutterScroll(this)"
        >print("Name & Roll No of Student")
         print("Area of Circle - IPP)
         radius = int(input("Enter the radius of a circle : ))
         area = 3.142 * radius * radius
         print("Radius of the circle is ",radius)
        </textarea>
      </div>
      <div class="code-term">
        <pre class="py-output"></pre>
      </div>
    </div>
  </div>
</div>

