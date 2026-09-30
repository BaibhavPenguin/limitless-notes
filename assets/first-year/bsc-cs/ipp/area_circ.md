# IPP &mdash; Area of Circle 
---

<link rel="stylesheet" , href="./styles/code-box.css">

### <u>Title</u>
Write a program in python to find the area of a circle

---
### <u>Explanation</u>
To find the area of a circle we will use the formula Area = &pi;r<sup>2</sup>  hence, we need to create two different variables for storing the radius and area.  

As radius will be entered by the user, we need to use the **input()** function.


### <u>Program</u>
<div class="code-container-div">
print("Limitless Editor - Roll Number 00") <br>
print("Area of Circle - IPP")<br>
radius = int(input("Enter the radius of a circle : "))<br>
area = 3.142 * radius * radius<br>
print("Area of the circle is ",area)
</div>

### <u>Try and Execute</u>

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
print("Area of Circle - IPP")
radius = int(input("Enter the radius of a circle : "))
area = 3.142 * radius * radius
print("Area of the circle is ",area)
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
