
# SORTING---8051

**AIM:**

To write and execute Assembly language Program for sorting of data using 8051 keil.

**APPARATUS REQUIRED: Personal computer with Keil software**

**(i) Descending order ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is low, then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**

```
ORG 0000H 
MOV R7,#4
LOOP1:MOV R0,#40H 
MOV R6,#04
LOOP: MOV A,@R0 
INC R0
MOV 50H,@R0 
CJNE A,50H,NEXT 
SJMP DOWN 
NEXT:JNC DOWN 
MOV @R0,A
DEC R0
MOV @R0,50H 
DOWN:DJNZ R6,LOOP 
DJNZ R7,LOOP1
END

```

**OUTPUT:**


**MEMORY WINDOW:**

Before execution: D:0x40H:
<img width="948" height="432" alt="image" src="https://github.com/user-attachments/assets/17ccfce4-3ff2-4653-94e0-43814cb476b6" />

<BR>
<BR>
<BR>
After execution: D:0x40H:
<img width="956" height="435" alt="image" src="https://github.com/user-attachments/assets/9411f314-8584-4364-b58f-4195f4083537" />
<BR>
<BR>
<BR>


**(ii)	Ascending order**
 
**ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is high then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**

```
ORG 0000H 
MOV R7,#4
LOOP1:MOV R0,#40H
MOV R6,#04
LOOP: MOV A,@R0
INC R0
MOV 50H,@R0 
CJNE A,50H,NEXT
SJMP DOWN 
NEXT:JC DOWN
MOV @R0,A
DEC R0
MOV @R0,50H 
DOWN:DJNZ R6,LOOP 
DJNZ R7,LOOP1
END

```
**OUTPUT:**

**MEMORY WINDOW:** 

**Before execution:**
D:0x40H:
<img width="1232" height="357" alt="image" src="https://github.com/user-attachments/assets/5fa40511-cd09-482e-bf14-f2c095ae665f" />

<BR>
<BR>
<BR>
<BR>
After execution:
D:0x40H:
<img width="1226" height="354" alt="image" src="https://github.com/user-attachments/assets/9d607523-1aa8-49bd-84a6-3b095140f23f" />

<BR>
<BR>
<BR>
**Result:**

Thus the sorting of given data was done using 8051 keil and shown the output.

