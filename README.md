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
<img width="707" height="707" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


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

![add](https://github.com/user-attachments/assets/292a65b0-6ac0-4cab-9c91-cacb1893fbe3)



---

## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="644" height="430" alt="Screenshot 2025-09-03 113518" src="https://github.com/user-attachments/assets/09d540d8-123e-449e-aa2a-a6661e1396af" />

<img width="634" height="379" alt="Screenshot 2025-09-03 113342" src="https://github.com/user-attachments/assets/466cf339-83d9-412d-9b34-e99f4d4ba6b9" />




## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="578" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


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

![sub](https://github.com/user-attachments/assets/c53678f9-fdd0-4f2c-8bee-ee11ff73447d)


---


## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="634" height="429" alt="Screenshot 2025-09-03 113636" src="https://github.com/user-attachments/assets/24857e37-0dd8-4992-8908-56ef73745b8b" />

<img width="637" height="428" alt="Screenshot 2025-09-03 113800" src="https://github.com/user-attachments/assets/17fbe5ea-2bc9-44cc-90bb-9e8e7a1638f9" />



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

![mul](https://github.com/user-attachments/assets/7fd0dbd5-ab5c-447c-891f-bbf1cd50b461)



---

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="635" height="427" alt="Screenshot 2025-09-03 113924" src="https://github.com/user-attachments/assets/324b6d47-c70e-4196-99a4-863c6d3e5f22" />

<img width="635" height="427" alt="Screenshot 2025-09-03 114034" src="https://github.com/user-attachments/assets/05cc6092-7a87-4283-bfb8-d9b51995cb10" />



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

![div](https://github.com/user-attachments/assets/62f8edef-58e4-4b83-a154-445721c9881b)


---
## OUTPUT FROM MASM SOFTWARE

<img width="633" height="428" alt="Screenshot 2025-09-03 114651" src="https://github.com/user-attachments/assets/d8b7f2ce-6a3d-4e82-a025-9dd489b3ce8e" />

<img width="632" height="428" alt="Screenshot 2025-09-03 114551" src="https://github.com/user-attachments/assets/b1b159c4-3750-4ff7-8586-6db9f1a9f2eb" />



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
