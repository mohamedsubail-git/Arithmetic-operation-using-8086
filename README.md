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
<img width="601" height="375" alt="Screenshot 2025-09-03 222203" src="https://github.com/user-attachments/assets/2c2c23af-7b0b-42e9-a3ff-db48c565dc7b" />
<img width="630" height="397" alt="Screenshot 2025-09-03 221939" src="https://github.com/user-attachments/assets/065eb414-9c7c-419b-9287-83cbe0ca0e82" />



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
![WhatsApp Image 2025-09-03 at 21 16 59_a5f7fb1f](https://github.com/user-attachments/assets/276e2e1c-cd7d-460c-b8c8-743046a63a7a)



(Add your calculation here)

---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="490" height="312" alt="Screenshot 2025-09-03 222409" src="https://github.com/user-attachments/assets/ee76a69e-e32a-4696-a201-8b12a4e2a7b4" />

<img width="625" height="432" alt="Screenshot 2025-09-03 230846" src="https://github.com/user-attachments/assets/b292ee0d-c535-4d55-8ffe-abc5e3545597" />




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
<img width="622" height="372" alt="Screenshot 2025-09-03 103637" src="https://github.com/user-attachments/assets/4c322816-bcb0-479c-96a1-90bceaa18fb8" />
<img width="637" height="438" alt="Screenshot 2025-09-03 103521" src="https://github.com/user-attachments/assets/0a9a126e-77cf-472b-8d3f-fb76cf0c1c59" />



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

![WhatsApp Image 2025-09-03 at 21 05 14_0c9b2140](https://github.com/user-attachments/assets/d8c21a01-c6dd-49d3-81d5-5f89b96b32ad)





---
## OUTPUT FROM MASM SOFTWARE
<img width="642" height="400" alt="Screenshot 2025-09-03 205032" src="https://github.com/user-attachments/assets/95f927a9-b32a-4239-bebd-0e2048f17e6f" />
<img width="646" height="402" alt="Screenshot 2025-09-03 204252" src="https://github.com/user-attachments/assets/a2a73a3d-49fe-4223-b64f-02aba29ee38f" />





## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
