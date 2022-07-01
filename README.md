# find-the-volume-MIPS
Example to find the  volume by MIPS 

.data

aside: .word 73

bside: .word 14

cside: .word 16

volume: .word 0



.text



lw $t0,aside

lw $t1,bside

lw $t2,cside



mul $t3,$t0,$t1

mul $t4,$t3,$t2

sw $t4,volume



li $v0,1

lw $a0,volume

syscall



li $v0,10

syscall
