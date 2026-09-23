# IPP &mdash; Simple Interest  
---
### <u>Title</u>  

Write a program in python to find Simple Interest
---

### <u>Explanation</u>
To find the simple interest we will use the formula **SI = principal amount x rate of interest x tenure** 

Here, we require four distinct variables to store principal amount, rate of interest, tenure and the simple interest. 

To get user input we use the built in **input()** function of python, in simpler words, we are giving a command to the python interpreter to wait for the user and give them a chance to enter an input value. The input() function takes a prompt argument, the prompt is the message shown to the user while getting the input.

Python assumes that all user inputs are Strings by default so we must convert the string to an float type before processing it.  
A floating point number is a number with a decimal place. We use floats when storing values like percentages, interest rates, temperature, etc.


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
        >print("Limitless Editor - Roll Number 00")
print("Simple Interest - IPP")
p = float(input("Enter the principal amount : "))
r = float(input("Enter the rate of interest : "))
t = int(input("Enter the tenure : "))
si = p * r * t
print("Simple Interest : " , si)
        </textarea>
      </div>
      <div class="code-term">
        <pre class="py-output"></pre>
      </div>
    </div>
  </div>
</div>


Replace the first print statement with your own name and roll number.  
*&mdash; Edited by Baibhav Bhattacharya*
