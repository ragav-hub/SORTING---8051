
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
<img width="1423" height="206" alt="image" src="https://github.com/user-attachments/assets/a76c3861-a124-4b20-9f38-e6a66ed7fd6f" />


<BR>
<BR>
<BR>
After execution: D:0x40H:
<img width="1428" height="210" alt="image" src="https://github.com/user-attachments/assets/a4bb8212-bd12-489e-b860-056b50d9ce77" />

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
<img width="949" height="432" alt="Screenshot 2025-11-11 195625" src="https://github.com/user-attachments/assets/0d308007-ffee-4887-a836-06a774f44b94" />
<BR>
<BR>
<BR>
<BR>
After execution:
D:0x40H:
<img width="956" height="435" alt="Screenshot 2025-11-11 195721" src="https://github.com/user-attachments/assets/481c9e2e-0fc2-4e56-83db-9c7aeb1c3a39" />
<BR>
<BR>
<BR>
**Result:**
Thus the sorting of given data was done using 8051 keil and shown the output.

