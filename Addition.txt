include irvine32.inc
.data
	msg1 byte "Enter your first NO:",0
	msg2 byte "Enter your Second NO:",0
	msg3 byte "Answer =",0
.code
main proc 
	
	mov edx ,offset msg1
	call writestring
	call readint
	mov ebx,eax

	mov edx ,offset msg2
	call writestring
	call readint

	add eax,ebx

	mov edx ,offset msg3
	call writestring
	call writeint
	call crlf

exit
main endp
end main