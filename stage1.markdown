---
layout: basic
---
[Back to Index](index.markdown)
<h2 id="challenge-001">Challenge 1 (From Tutorial Episode 2)</h2>

**Challenge:** As a coding challenge, I want you to write a piece of ASM code that increases the variable myMagic by 3 every time it’s run, but if the number goes higher than the number 25 (#$19) it sets the myMagic value to 25.

Hint: For this challenge you’ll need to use the JMP (Jump) command to skip to the end of the script! The syntax is very similar to a branch. We’ll cover it next tutorial.  
Syntax: `JMP [label]`  
Label is the label you wish to jump to. This is an unconditional jump. When it is encountered in the code the program will jump to the destination label.

Click **Assemble** then **Run** to assemble and run your result, then keep clicking **Run** until you confirm this challenge is complete!

Commands used in this challenge:  
`LDA`, `STA`, `ADC`, `CLC`, `CMP`, `BCS`, `JMP`

{% include start.html %}
define myMagic $0100
start:
;; Put your code here.
;; Replace these comments with the solution to the challenge!
;; This template sets up the myMagic variable for you.
;; In easy6502 check the "Monitor" checkbox, type in "100" in the "Start: $" text box and the
;;                                                       number 1 in the "Length:$" text box.
;; Write your code, click "Assemble" and then start clicking "Run". The first set of digits
;; in that box under the "Monitor" should show "0100: 03", and that number should climb by
;; 3 each time you click the Run button until the goal is met.
;; Good Luck!
end: ;You'll need to JMP here in the challenge. :)
BRK
JMP start
;End
{% include end.html %}
