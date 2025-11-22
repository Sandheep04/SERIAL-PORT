
# Serial Transfer of Single Byte / Character using 8051 (Keil)

## AIM
To write and execute an Embedded C Program for Serial Transfer of Single Byte / Character using 8051 in Keil.

## APPARATUS REQUIRED
- Personal Computer  
- Keil µVision Software  

## PROGRAM

### (i) Serial Port Transfer a Single Character

```
ORG 00H
MOV TMOD, #20H
MOV TH1, #0FDH
MOV SCON, #40H
SETB TR1
MOV SBUF, #'B'
WAIT:JNB TI, WAIT
CLR TI
END

```
### (ii) Serial Port to Transfer a Message

```
ORG 00H 
MOV DPTR, #4500H
MOV TMOD, #20H 
MOV TH1, #0FDH 
MOV SCON, #40H 
SETB TR1 
AGAIN: MOVX A,@DPTR
MOV SBUF, A
 WAIT:JNB TI, WAIT
 CLR TI 
 INC DPTR
 SJMP AGAIN
 END


```

### OUTPUT:

<img width="1085" height="395" alt="image" src="https://github.com/user-attachments/assets/b32bcb9c-e9a4-41ef-97b9-98df6bda70ca" />




<img width="1920" height="343" alt="Screenshot 2025-10-27 105155" src="https://github.com/user-attachments/assets/44260dc9-a819-4f35-bf0e-ba8e2a2b7b10" />

### RESULT:
Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.
