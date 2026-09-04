# Basic Logic Gates
---

## Definition of Logic Gates
*Logic Gates are the fundamental physical building blocks of digital logic.*
Logic Gates operate in Boolean Logic i.e. they take one or more digital inputs and produce
a single output corresponding to the underlying predefined logic rules.

## Types of Logic Gates
There are mainly two types of Logic Gates namely **Basic Logic Gates** and **Universal Logic Gates**, the basic logic gates perform a single logical function while universal gates can be used to create any logic gate.


> **Basic Gates :** AND , OR , NOT  
> **Universal Gates :** NAND , NOR  
> **Special Function Gate :** XOR , XNOR

## Theory, Truth Table, Circuit Symbol and Boolean Expression
---
### AND GATE
The AND is a digital logic gate which only outputs high (1) when all of the inputs are high (1)


<table align='center'>
<tr>
<th> A
<th> B
<th> Y
</tr>

<tr>
<td> 0
<td> 0
<td> 0
</tr>

<tr>
<td> 0
<td> 1
<td> 0
</tr>

<tr>
<td> 1
<td> 0
<td> 0
</tr>

<tr>
<td> 1
<td> 1
<td> 1
</tr>

<caption><strong>Truth Table</strong></caption>
</table>
<figure align='center'>
    <figcaption><strong>Circuit Symbol</strong> </figcaption>   
    <img src="https://i.postimg.cc/htW9dqzV/AND-GATE.png">
    
</figure>

> **Boolean Expression : A &middot; B**
---

### OR GATE
The OR GATE is a digital logic gate which outputs high (1) when any one or both inputs are high (1)

<div align='center'>
<table>
<tr>
<th> A
<th> B
<th> Y
</tr>

<tr>
<td> 0
<td> 0
<td> 0
</tr>

<tr>
<td> 0
<td> 1
<td> 1
</tr>

<tr>
<td> 1
<td> 0
<td> 1
</tr>

<tr>
<td> 1
<td> 1
<td> 1
</tr>

<caption><strong>Truth Table</strong></caption>
</table>
<figure align='center'>
    <figcaption><strong>Circuit Symbol</strong> </figcaption>   
    <img src="https://i.postimg.cc/kg3xbd6t/OR-GATE.png">
    
</figure>
</div>

> **Boolean Expression : A + B**
---


### NOT GATE
The NOT GATE is a digital logic gate which inverts the state of the input i.e. *If A = 0 then Y = 1 and If A = 1 then Y = 0 where A is the input and Y is the output*


<table align='center'>
<tr>
<th> A

<th> Y
</tr>

<tr>
<td> 0
<td> 1
</tr>

<tr>
<td> 1
<td> 0
</tr>


<caption><strong>Truth Table</strong></caption>
</table>
<figure align='center'>
    <figcaption><strong>Circuit Symbol</strong> </figcaption>   
    <img src="https://i.postimg.cc/VkQjCcrt/NOt-GATE.png">
    
</figure>

> **Boolean Expression : A&#773; = Y**
---

### NAND GATE
The NAND is a digital logic gate which outputs high (1) if any one of the inputs is low (0). It is an inversion of the AND Gate and can also be formed by attaching a NOT Gate to the output of an AND GATE.


<table align='center'>
<tr>
<th> A
<th> B
<th> Y
</tr>

<tr>
<td> 0
<td> 0
<td> 1
</tr>

<tr>
<td> 0
<td> 1
<td> 1
</tr>

<tr>
<td> 1
<td> 0
<td> 1
</tr>

<tr>
<td> 1
<td> 1
<td> 0
</tr>

<caption><strong>Truth Table</strong></caption>
</table>
<figure align='center'>
    <figcaption><strong>Circuit Symbol</strong> </figcaption>   
    <img src="https://i.postimg.cc/t4QhxHZW/NAND-GATE.png">
    
</figure>
<blockquote><strong>Boolean Expression : <span style="text-decoration:overline;">A &middot; B</span> = Y</strong></blockquote>

---

### NOR GATE
The NOR is a digital logic gate which only outputs high (1) if all the inputs are low (0). It is an inversion of the OR Gate and can also be formed by attaching a NOT Gate to the output of an OR GATE.


<table align='center'>
<tr>
<th> A
<th> B
<th> Y
</tr>

<tr>
<td> 0
<td> 0
<td> 1
</tr>

<tr>
<td> 0
<td> 1
<td> 0
</tr>

<tr>
<td> 1
<td> 0
<td> 0
</tr>

<tr>
<td> 1
<td> 1
<td> 0
</tr>

<caption><strong>Truth Table</strong></caption>
</table>
<figure align='center'>
    <figcaption><strong>Circuit Symbol</strong> </figcaption>   
    <img src="https://i.postimg.cc/jS0z7rwN/NOR-GATE.png">
    
</figure>
<blockquote><strong>Boolean Expression : <span style="text-decoration:overline;">A + B</span> = Y</strong></blockquote>

---


### XOR GATE
The XOR Gate is a digital logic gate which only outputs high (1) if the inputs are different I.e. when A &ne; B


<table align='center'>
<tr>
<th> A
<th> B
<th> Y
</tr>

<tr>
<td> 0
<td> 0
<td> 0
</tr>

<tr>
<td> 0
<td> 1
<td> 1
</tr>

<tr>
<td> 1
<td> 0
<td> 1
</tr>

<tr>
<td> 1
<td> 1
<td> 0
</tr>

<caption><strong>Truth Table</strong></caption>
</table>
<figure align='center'>
    <figcaption><strong>Circuit Symbol</strong> </figcaption>   
    <img src="https://i.postimg.cc/8zQh6VJF/XOR-GATE.png">
    
</figure>

<figure align='center'>
    <figcaption><strong>XOR Circuit Diagram</strong> </figcaption>   
    <img src="https://i.postimg.cc/CxBTff2H/XOR-CIRCUIT.png">
</figure>

> **Boolean Exppression : AB&#773; + A&#773;B**
> **Simplified Boolean Exppression : A &oplus; B**

---


### XNOR GATE
The XNOR Gate is a digital logic gate which only outputs high (1) if the inputs are same I.e. when A = B
It is the inversion of an XOR Gate. It is considered as a special function gate.

<table align='center'>
<tr>
<th> A
<th> B
<th> Y
</tr>

<tr>
<td> 0
<td> 0
<td> 1
</tr>

<tr>
<td> 0
<td> 1
<td> 1
</tr>

<tr>
<td> 1
<td> 0
<td> 1
</tr>

<tr>
<td> 1
<td> 1
<td> 0
</tr>

<caption><strong>Truth Table</strong></caption>
</table>
<figure align='center'>
    <figcaption><strong>Circuit Symbol</strong> </figcaption>   
    <img src="https://i.postimg.cc/mgfQHGz1/XNOR-GATE.png">
    
</figure>

<figure align='center'>
    <figcaption><strong>XOR Circuit Diagram</strong> </figcaption>   
    <img src="https://i.postimg.cc/8k7zbsxr/XNOR-CIRCUIT.png">
</figure>

> **Boolean Exppression : A &middot; B + A&#773; &middot; B&#773;**
> **Simplified Boolean Exppression : A &odot; B**

---

> **NOTE:** Special function gates are different from universal gates, we can use AND and OR GATES to construct an XOR GATE but we cannot use an XOR GATE to construct an AND or OR GATE hence, an XOR GATE is a Special Function Gate but is **NOT** an Universal Logic Gate.






