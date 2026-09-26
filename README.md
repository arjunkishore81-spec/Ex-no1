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
MOV BX,1234H
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
|       1200🔢       01         12

|         1200                    |

#### Manual Calculations
<img width="1280" height="590" alt="image" src="https://github.com/user-attachments/assets/5b700722-1147-4a1e-b86e-72c9a04bddd4" />


---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="655" height="447" alt="image" src="https://github.com/user-attachments/assets/751e916d-3848-4696-811e-e66459ab8f66" />

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
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Output Table
<img width="637" height="200" alt="image" src="https://github.com/user-attachments/assets/c31eb819-d6ce-41d5-96f0-850497f9f3c7" />


#### Manual Calculations

<img width="1280" height="1251" alt="image" src="https://github.com/user-attachments/assets/2aee7c26-eef5-4eb7-8ca5-a0685a0e144f" />

---


## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="638" height="431" alt="image" src="https://github.com/user-attachments/assets/8b0d524b-6f71-41b3-b774-aaa30539bc34" />

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
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table
<img width="617" height="205" alt="image" src="https://github.com/user-attachments/assets/822b5659-f435-4f62-b0dd-1774ffd93dab" />

#### Manual Calculations

<img width="1599" height="606" alt="image" src="https://github.com/user-attachments/assets/367e7e2e-7d1b-466b-8396-e0f063027f37" />


---

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="642" height="424" alt="image" src="https://github.com/user-attachments/assets/fb0232b1-26c6-40ee-9d3f-3a83c61347a3" />

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
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

<img width="485" height="200" alt="image" src="https://github.com/user-attachments/assets/1cab2f07-abe1-43dc-8563-fd7665a0f24d" />

#### Manual Calculations

<img width="1047" height="769" alt="image" src="https://github.com/user-attachments/assets/a084c6f3-cbde-48dc-9846-d10ba132a90e" />


---
## OUTPUT FROM MASM SOFTWARE

<img width="638" height="431" alt="image" src="https://github.com/user-attachments/assets/a8ee5034-02dc-4301-bccb-343dd3519fe1" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

