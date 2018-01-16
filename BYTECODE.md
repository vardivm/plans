# Vardi Bytecode
The instruction set of the Vardi virtual machine.
All bytecodes are encoded in a single octet (0-255).

# 
| HEX | DECIMAL | ENGLISH |
| :---: | :---: | ---: |
| 0x00 | 0 | NO OP |
| 0x01 | 1 | JMP ABSOLUTE |
| 0x11 | 17 | JUMP STACK ADDR |
| 0x03 | 3 | PEEK PRINT |
| 0x05 | 5 | POP |
| 0x07 | 7 | SHUFFLE |
| 0x0D | 13 | PUSH ABSOLUTE |
| 0x0F | 15 | EXIT PROGRAM |
| 0xFF | 255 | JMP TO RETURN ADDRESS |
| 0xCA | 202 | CALL SUBROUTINE ABSOLUTE |
| 0x1F | 31 | JUMP IF ZERO ABSOLUTE |
| 0xFE | 254 | PAUSE ABSOLUTE |
| 0xC5 | 197 | CALL SUBROUTINE STACK ADDR |
| 0xDD | 221 | DUPLICATE STACK |
| 0x02 | 2 | SWAP STACK |
| 0x22 | 34 | SWAP RETURN ON STACK |
| 0xE2 | 226 | SWAP NEXT INSTR ON STACK |
| 0x04 | 4 | TO BE DETERMINED |
| 0x06 | 6 | ADD |
| 0x08 | 8 | SUB |
| 0x0B | 11 | MUL |
| 0x0C | 12 | DIV |
| 0x0A | 10 | TEXT | 
| 0x0E | 14 | PRINT |
| 0x40 | 64 | MEMORY STORE |
| 0x3C | 60 | MEMORY FETCH |
| 0x4D | 77 | LOGICAL AND |
| 0x5D | 93 | LOGICAL NOT | 




