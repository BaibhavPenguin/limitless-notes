# Half Subtractor & Full Subtractor

## <u> Definition of a Subtractor </u>
---
An Adder is a combinational digital circuit which performs arithmetic addition on binary bits and generates sum and carry as result.

## <u> Half Subtractor </u>
---
A Half Adder is a combinational digital logic circuit which performs arithmetic addition on two binary bits and generates Sum and Carry as results.  
It is constructed using an XOR and AND gate, the output at the XOR gate is the **Sum** while the output at the AND gate is the **Carry**.

<table>
  <thead>
    <tr>
      <th>A</th>
      <th>B</th>
      <th>Difference</th>
      <th>Borrow</th>
       <th>Minterms</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>A&#773;B&#773;</td>
    </tr>
    <tr>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>A&#773;B</td>
    </tr>
    <tr>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
       <td>AB&#773;</td>
    </tr>
    <tr>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>AB</td>
    </tr>
  </tbody>
  <caption><strong>Truth Table</strong></caption>
</table>
<figure>
    <figcaption><strong>Circuit Diagram</strong> </figcaption>   
    <img src="https://i.postimg.cc/T2r5JwKj/Half-Subtractor.png">  
</figure>

> **Boolean Expression**  
> **Sum :** A &oplus; B   
> **Carry :** A &middot; B

## <u> Full Subtractor </u>
---
A Full Adder is a combinational digital logic circuit which performs arithmetic addition on three binary bits and generates Sum and Carry as results.  
It is constructed using an XOR, AND and OR gates, the output at the XOR gate is the **Sum** while the output at the OR gate is the **Carry**.

<table>
  <thead>
    <tr>
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>Sum</th>
      <th>Carry</th>
      <th>Minterms</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>A&#773;B&#773;C&#773;</td>
    </tr>
    <tr>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>A&#773;B&#773;C</td>
    </tr>
    <tr>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>A&#773;BC&#773;</td>
    </tr>
    <tr>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>A&#773;BC</td>
    </tr>
    <tr>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>AB&#773;C&#773;</td>
    </tr>
    <tr>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>AB&#773;C</td>
    </tr>
    <tr>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>ABC&#773;</td>
    </tr>
    <tr>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>ABC</td>
    </tr>
  </tbody>
</table>
<figure>
    <figcaption><strong>Circuit Diagram</strong> </figcaption>   
    <img src="https://i.postimg.cc/66d4f38h/Full-Subtractor.png">  
</figure>

> **Deriving the boolean expression for Sum** :  
> Sum = A&#773;B&#773;C + A&#773;BC&#773; + AB&#773;C&#773; + ABC  
> &therefore;  A&#773;B&#773;C + ABC + A&#773;BC&#773; + AB&#773;C&#773;  
> &therefore;  C(A&#773;B&#773; + AB) +  C&#773;(A&#773;B + AB&#773;)  
> &therefore;  C(A &odot; B) +  C&#773;(A &oplus; B)  
> Hence,  
> **Sum = A &oplus; B &oplus; C**

> **Deriving the boolean expression for Carry** :  
> Carry = A&#773;BC + AB&#773;C + ABC&#773; + ABC  
> &therefore; C (A&#773;B + AB&#773; ) + AB (C + C&#773;)  
> &therefore; (A &oplus; B) &middot; C  + AB  
> Hence,  
> **Carry = (A &oplus; B) &middot; C  + AB**  

*&mdash; Edited by Baibhav Bhattacharya*
