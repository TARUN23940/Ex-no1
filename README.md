# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS:CODE, DS:CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,124H
ADD AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI],AX
MOV [SI+2],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200              |         58               |
|       1201              |         13               |

#### Manual Calculations

(Add your calculation here)

---

## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="649" height="429" alt="Screenshot 2026-02-02 105103" src="https://github.com/user-attachments/assets/e7382ee9-1645-44a4-a927-d7a95d468f19" />


## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,124H
SUB AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI], AX
MOV [SI+2], CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|          1200           |            10            |
|          1201           |            11            |
#### Manual Calculations

(Add your calculation here)

---


## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="636" height="423" alt="Screenshot 2026-02-02 110750" src="https://github.com/user-attachments/assets/05da9c74-e339-4bb2-b16f-4b3ccfed0ee9" />


## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS:CODE,DS:CODE
ORG 1000H
MOU DX,000OH
MOU AX, 1234H
MOU BX, 1234H
MUL BX
MOU SI, 1200H
MOV[SI],AX
MOU [SI+02H],DX
MOU AH, 4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|            1200           |            10              |
|             1201         |            11            |

#### Manual Calculations

(Add your calculation here)

---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="425" alt="image" src="https://github.com/user-attachments/assets/bb2b4a2c-bf20-43c6-a9b0-25f03f73c059" />

## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS:CODE,DS:CODE
ORG 1000H
MOU DX,000OH
MOU AX, 1234H
MOU BX, 1234H
DIV BX
MOU SI, 1200H
MOV[SI],AX
MOU [SI+02H],DX
MOU AH, 4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|              1200         |           10               |
|          1201            |              11            |
#### Manual Calculations

(Add your calculation here)

---
## OUTPUT FROM MASM SOFTWARE

<img width="635" height="428" alt="image" src="https://github.com/user-attachments/assets/c71f5358-84f8-4812-a331-899aab583a3e" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

