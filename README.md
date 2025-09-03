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
![WhatsApp Image 2025-09-03 at 21 16 41_3074ea0e](https://github.com/user-attachments/assets/d22d39e3-2e1e-4f44-aa3d-9805e31139e6)


(Add your calculation here)

---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="648" height="441" alt="Screenshot 2025-08-29 104445" src="https://github.com/user-attachments/assets/740e25ab-6274-486f-ac65-27a293026a7b" />
<img width="1112" height="653" alt="Screenshot 2025-08-09 154808" src="https://github.com/user-attachments/assets/5fb02433-8596-481a-9457-9f5fcd7e38f4" />


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



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|               1200 : 12          |      1204 : 00                    |
1201 : 34 | 1205 : 00
1202 : 12 | 1206 : 00
1203 : 34 | 1207 : C4


#### Manual Calculations
![Uploading WhatsApp Image 2025-09-03 at 21.16.59_43252165.jpg…]()


(Add your calculation here)

---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="657" height="441" alt="Screenshot 2025-08-30 141118" src="https://github.com/user-attachments/assets/a83553df-61a7-402d-88ef-43ca5ebf4086" />
<img width="674" height="490" alt="Screenshot 2025-08-09 160144" src="https://github.com/user-attachments/assets/8591be95-ce77-434f-b2ce-75dd52a9d1cf" />



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
| 1200:12                  |     1204:44
  1201:34                 |      1205:51
| 1202:12                |       1206:97
| 1203:34              |        1207:0A              |

#### Manual Calculations
![WhatsApp Image 2025-09-03 at 21 05 39_93fe64d8](https://github.com/user-attachments/assets/9a2e5269-fec9-458a-854e-073c3bdf55a1)


---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="622" height="372" alt="Screenshot 2025-09-03 103637" src="https://github.com/user-attachments/assets/c5186e38-17d5-4eaf-a3f8-a8d34df17f2c" />
<img width="637" height="438" alt="Screenshot 2025-09-03 103521" src="https://github.com/user-attachments/assets/f36a89bc-cfda-43aa-88e2-84a2aea197af" />


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
| 1200:12                       
  1201:34                   |   1204:01
| 1202:12                  |    1205:00
| 1203:34                  |   1206:00                   |

#### Manual Calculations

![WhatsApp Image 2025-09-03 at 21 05 14_7a6067bf](https://github.com/user-attachments/assets/bf49e28f-55a6-451e-b614-ea17e385b516)



---
## OUTPUT FROM MASM SOFTWARE
<img width="642" height="400" alt="Screenshot 2025-09-03 205032" src="https://github.com/user-attachments/assets/95f927a9-b32a-4239-bebd-0e2048f17e6f" />
<img width="646" height="402" alt="Screenshot 2025-09-03 204252" src="https://github.com/user-attachments/assets/a2a73a3d-49fe-4223-b64f-02aba29ee38f" />





## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
