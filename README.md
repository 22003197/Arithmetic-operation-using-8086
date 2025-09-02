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
|     1200 : 12           |      1204 : 24           |
1201 : 34  |  1205 : 68
1202 : 12   | 1206 : 00
1203 : 34    |1207 : C4

#### Manual Calculations

![ADD MC](![WhatsApp Image 2025-09-02 at 23 58 34](https://github.com/user-attachments/assets/0c902a43-1e7a-42e5-9f14-f962af4f9871))



---

## OUTPUT IMAGE FROM MASM SOFTWARE

![add code](https://github.com/user-attachments/assets/8b1009d6-bcd6-4345-870b-a5285555975f)
!![add code output](https://github.com/user-attachments/assets/c7b2332d-06e7-456d-bbf6-672204bd78f1)


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
|               1200 : 12          |      1204 : 00                    |
1201 : 34 | 1205 : 00
1202 : 12 | 1206 : 00
1203 : 34 | 1207 : C4

#### Manual Calculations

![SB MC](![WhatsApp Image 2025-09-02 at 23 58 35](https://github.com/user-attachments/assets/05286ae6-9be7-48eb-9e0c-ea636d8414bb))

---


## OUTPUT SCREEN FROM MASM SOFTWARE

![sub code](https://github.com/user-attachments/assets/46edd6c0-350a-4394-9289-079e25f97dcc)

![sub op](https://github.com/user-attachments/assets/7d1ae894-7e0d-4549-a587-3863ad3d24bc)



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
|         1200 : 12                |       1204 : 44                   |
1201 : 34 | 1205 : 51
1202 : 12 | 1206 : 97
1203 : 34 | 1207 : 0A

#### Manual Calculations

![MUL MC](![WhatsApp Image 2025-09-02 at 23 58 35 (1)](https://github.com/user-attachments/assets/b5c13b45-d0e7-4225-8e23-09584aff4b4a))



---

## OUTPUT SCREEN FROM MASM SOFTWARE

![mul code](https://github.com/user-attachments/assets/243184fd-6749-4a3e-ad0b-8f111b769c52)

![mul op](https://github.com/user-attachments/assets/fe7171cf-f669-42b3-a05d-456d2db488af)



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
|       1200 : 12                  |              1204 : 01            |
1201 : 34 | 1205 : 00
1202 : 12 | 1206 : 00
1203 : 34 | 1207 : 00

#### Manual Calculations

![DIV MC](![WhatsApp Image 2025-09-02 at 23 58 35 (2)](https://github.com/user-attachments/assets/b89b11d2-dc59-4505-bcd5-b99763439fd2))



---
## OUTPUT FROM MASM SOFTWARE

![div code](https://github.com/user-attachments/assets/c81c3497-1677-4133-9830-7559712a0230)

![div op](https://github.com/user-attachments/assets/2d53a9e4-fb5e-4585-8307-7d86a5c95154)



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
