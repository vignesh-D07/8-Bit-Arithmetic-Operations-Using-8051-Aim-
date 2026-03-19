# 8-Bit-Arithmetic-Operations-Using-8051

## Aim:
To perform 8-bit arithmetic operations such as addition, subtraction, multiplication, and division using the 8051 microcontroller.

## Apparatus Required:

•	Laptop with Keil uVision software

## Algorithm:

## For Addition:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Add the contents of registers A and B.
4.	Store the result in memory location 40H.
5.	Store the carry (if any) in 41H.

## Program:
```
  MOV A,30H;
  ADD A,31H;
  MOV 40H,A;
  JNC NEXT ;
  MOV 41H,#01H;
  SJMP END_PROGRAM;
  NEXT:MOV 41H,#00H;
  END_PROGRAM:NOP;
  END
```

## Output:
<img width="1032" height="634" alt="image" src="https://github.com/user-attachments/assets/a41cbab2-03c0-4467-9a7a-819c8fc87066" />
<img width="1034" height="302" alt="image" src="https://github.com/user-attachments/assets/95503b92-190a-49d5-a85c-9a20e6467cad" />
<img width="291" height="717" alt="image" src="https://github.com/user-attachments/assets/8f300a77-6dc6-4826-aeda-33e9830b4fd7" />

   
## For Subtraction:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Subtract B from A.
4.	Store the result in memory location 40H.

## Program:
```
  ORG 0000H
  MOV A,30H
  SUBB A,31H
  MOV 40H,A
  JNC NEXT 
  MOV 41H,#01H;
  SJMP END_PROGRAM;
  NEXT:MOV 41H,#00H;
  END_PROGRAM:NOP;
  END
```


## Output:
<img width="1036" height="642" alt="image" src="https://github.com/user-attachments/assets/c7727bde-43b7-4248-9a4c-6f41f3fa575e" />
<img width="1031" height="307" alt="image" src="https://github.com/user-attachments/assets/c6614fa2-5e41-4001-b084-852427af0601" />
<img width="301" height="556" alt="image" src="https://github.com/user-attachments/assets/f6a456b7-5b20-4c42-acfd-5ca5c61601d8" />



## For Multiplication:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Multiply A and B.
4.	Store the lower byte of the result in memory location 40H.
5.	Store the higher byte of the result in memory location 41H.

## Program:
```
  ORG 0000H
  MOV A,30H
  MOV B,31H
  MUL AB
  MOV 40H,A
  MOV 41H,B
  END
```

## Output:
<img width="1034" height="642" alt="image" src="https://github.com/user-attachments/assets/f2c1ffc0-b33f-4f3c-aa36-ba56f5481ffb" />
<img width="1032" height="305" alt="image" src="https://github.com/user-attachments/assets/0389d016-3d19-494e-9fa9-929d22e58217" />
<img width="300" height="552" alt="image" src="https://github.com/user-attachments/assets/4fbb705f-0aea-4f05-a67c-306e60a6df77" />


## For Division:
1.	Load the dividend from memory location 30H into register A.
2.	Load the divisor from memory location 31H into register B.
3.	Divide A by B.
4.	Store the quotient in memory location 40H.
5.	Store the remainder in memory location 41H.


## Program:
```
  ORG 0000H
  MOV A, 30H
  MOV B, 31H
  DIV AB
  MOV 40H, A
  MOV 41H, B
  END
```

## Output:
<img width="1033" height="643" alt="image" src="https://github.com/user-attachments/assets/c5dd3776-243b-4864-bdaf-3703a0326e14" />
<img width="1035" height="307" alt="image" src="https://github.com/user-attachments/assets/4aab9893-cb07-4366-9ff7-887b1b959d4f" />
<img width="297" height="587" alt="image" src="https://github.com/user-attachments/assets/4d512347-213b-4b31-b07a-63ddc77a7667" />



## Result:
The 8-bit arithmetic operations using the 8051 microcontroller have been successfully executed and verified using Keil software.

