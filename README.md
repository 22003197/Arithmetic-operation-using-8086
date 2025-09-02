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
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
| 1200: 31                | 1204: 62                 |
| 1201: 12                | 1205: 24                 |
| 1202: 31                | 1206: 00                 |
| 1203: 12                | 1207: C4                 |
#### Manual Calculations
<img width="201" height="349" alt="image" src="https://github.com/user-attachments/assets/caa07a0b-02d3-4841-8363-81506e3b02ea" />



## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="628" height="390" alt="image" src="https://github.com/user-attachments/assets/3be45d1f-248e-40f8-8754-423e6a57347f" />


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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  1200: 31               |  1204:   00              |
|  1201: 12               |  1205:   00              |
|  1202: 31               |  1206:   00              |
|  1203: 12               |  1207:   C4              |
#### Manual Calculations
<img width="214" height="346" alt="image" src="https://github.com/user-attachments/assets/0bb96f56-eb1a-4c27-88e8-d2393bd1d440" />




## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="629" height="392" alt="image" src="https://github.com/user-attachments/assets/39e20cec-937c-42a7-abbf-7471aa31401f" />



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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  1200: 31               | 1204: 61                 |
|  1201: 12               | 1205: ED                 |
|  1202: 31               | 1206: 00                 |
|  1203: 12               | 1207: C4                 |
### Manual Calculations



## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="634" height="394" alt="image" src="https://github.com/user-attachments/assets/d0513b33-8a08-469f-95a4-a2ea38849ff1" />


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
| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  1200: 31               | 1204: 01                 |
|  1201: 12               | 1205: 00                 |
|  1202: 31               | 1206: 00                 |
|  1203: 12               | 1207: 00                 |

#### Manual Calculations
<img width="188" height="351" alt="image" src="https://github.com/user-attachments/assets/e281e3d7-865a-46bd-a50c-b80e9b8aafd2" />




## OUTPUT FROM MASM SOFTWARE
<img width="624" height="386" alt="image" src="https://github.com/user-attachments/assets/f776ddb7-ec7f-4a8b-b186-f081eb5e292f" />





## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
