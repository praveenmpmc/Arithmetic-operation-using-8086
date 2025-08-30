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
|         1200 : 12	           1204 : 24
          1201 : 34	           1205 : 68
          1202 : 12	           1206 : 00
          1203 : 34	           1207 : C4                              

#### Manual Calculations
![WhatsApp Image 2025-08-30 at 16 01 39_1204e8e9](https://github.com/user-attachments/assets/6533b6ee-96df-4ac3-b9f2-fe588cbab920)

(Add your calculation here)

---


# OUTPUT IMAGE FROM MASM SOFTWARE
<img width="630" height="428" alt="Screenshot 2025-08-30 161216" src="https://github.com/user-attachments/assets/df223988-eb66-4bbf-ad09-b19757176c46" />




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



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|          1200 : 12	              1204 : 00
           1201 : 34               1205 : 00
           1202 : 12	              1206 : 00
           1203 : 34	              1207 : C4              

#### Manual Calculations
![WhatsApp Image 2025-08-30 at 16 01 58_085a71bb](https://github.com/user-attachments/assets/22a5ddb9-4167-41d5-9fb9-597151b64746)

(Add your calculation here)

---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="637" height="423" alt="Screenshot 2025-08-30 193837" src="https://github.com/user-attachments/assets/4471d60f-c4f5-4503-8926-8545130016e3" />


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
|          1200 : 12	            1204 : 44
           1201 : 34	            1205 : 51
           1202 : 12	            1206 : 97
           1203 : 34	            1207 : 0A                                

#### Manual Calculations
![WhatsApp Image 2025-08-30 at 16 05 59_a0527a2f](https://github.com/user-attachments/assets/362f5f41-b41c-4c57-8018-af25bda35c75)


(Add your calculation here)

---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="639" height="424" alt="Screenshot 2025-08-30 194958" src="https://github.com/user-attachments/assets/d91f5485-6fce-4dcf-868d-3edb0555442a" />


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
|           1200 : 12	          1204 : 01
            1201 : 34	          1205 : 00
            1202 : 12	          1206 : 00
            1203 : 34	          1207 : 00         

#### Manual Calculations
![WhatsApp Image 2025-08-30 at 16 06 26_a71c1268](https://github.com/user-attachments/assets/afc2e9bf-5b1b-4fd8-b6c0-d834da86e0bc)


(Add your calculation here)

---
## OUTPUT FROM MASM SOFTWARE



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
