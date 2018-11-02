---
layout: basic
---
[Back to Index](index.markdown)
<h2 id="challenge-002">Challenge 3 (From Tutorial Episode 4)</h2>

**Challenge:** For this challenge, you will receive random numbers in the baseDamage variable and playerFlags variable. If the 3rd bit (########) in playerFlags is set, set damage to baseDamage divided by 2. If baseDamage is odd, add 1 to the result of the division to round the number up. If the 3rd bit in playerFlags is not set, simply store baseDamage in the damage variable.
This challenge will utilize information from all three ASM Basics tutorials: Branching, Conditions/Binary Operations and Simple Division.

Commands used in this challenge:  
`LDA`,`STA`,`AND`,`BNE`,`BEQ`,`JMP`,`CLC`,`ADC`,`LSR`

Check the "Monitor" checkbox. In the "Start $" textbox enter the number 0, and in the "Length $" textbox enter the number 3.
Click **Assemble** then **Run** multiple times to see if your code works. Use the Debugger on the right to step through and watch your code in action if you want to see it operating.

{% include start.html %}
define playerFlags $00
define baseDamage $01
define damage $02
define rnd $fe
start:
LDA rnd ;The PC should read $0600 here
STA playerFlags ;PC should read $0602
LDA rnd ;And so on.
STA baseDamage
LDA #$00
STA damage ;PC should be 060c here. Next step will be your code working.
;; -------User code begins here.-------

; Put your code here, in this blank space.

;; -------User code ends here.-------
end:
BRK
JMP start
{% include end.html %}
