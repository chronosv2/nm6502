---
layout: basic
---
[Back to Index](index.markdown)
<h2 id="challenge-002">Challenge 2 (From Tutorial Episode 3)</h2>

**Challenge:** Write Assembly code that stores the numeric result of the following problems into memory:
The result of `#%10010011` **AND** `#%11100010` should be stored into `AndLoc`  
The result of `#%10100011` **ORA** `#%11100111` should be stored into `OrLoc`  
The result of `#%11110011` **EOR** `#%11111111` should be stored into `XorLoc`  
Lastly, there will be code in the template that will attempt to overwrite your results. I want you to `JMP` past it.

Commands used in this challenge:  
`LDA`, `STA`, `AND`, `ORA`, `EOR`, `JMP`

Check the "Monitor" checkbox. In the "Start $" textbox enter the number 0100, and in the "Length $" textbox enter the number 3.
Click **Assemble** then **Run** to get the answer 

{% include start.html %}
;Define Memory Locations for memory use
define AndLoc $0100
define OrLoc $0101
define XorLoc $0102

;Start
;Put your code here.

;Oh no! Some random code is overwriting the answers!
LDA #$FE	;Jump over it! :)
STA AndLoc
STA OrLoc
STA XorLoc
noOverwrite:
{% include end.html %}
