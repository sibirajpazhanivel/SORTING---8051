
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


**OUTPUT:**

**MEMORY WINDOW:**

Before execution: D:0x40H:
<img width="438" height="171" alt="image" src="https://github.com/user-attachments/assets/f48204f4-eb69-431f-b2d9-5c92dd05481e" />

After execution: D:0x40H:
<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/769a9746-a7bd-4581-94e7-fee89f165583" />



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

**OUTPUT:**

**MEMORY WINDOW:** 

**Before execution:**
D:0x40H:
<img width="931" height="285" alt="image" src="https://github.com/user-attachments/assets/b053cf74-f073-4947-89ea-8a21ffbebb78" />

After execution:
D:0x40H:
<img width="1600" height="1001" alt="image" src="https://github.com/user-attachments/assets/f7651e19-5bc4-4da3-909d-7882e729e94d" />

**Result:**

Thus the sorting of given data was done using 8051 keil and shown the output.

