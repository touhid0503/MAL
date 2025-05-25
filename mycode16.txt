.model small
.stack 100h
.code

main proc
    mov ah, 1      
    int 21h       

    cmp al, 'A'
    jb exit       ; If AL < 'A', exit. JB = Jump if below 

    cmp al, 'Z'
    ja exit       ; If AL > 'Z', exit. JA = Jump if above 

    mov dl, al      
    mov ah, 2     
    int 21h

exit:
    mov ah, 4ch  
    int 21h
main endp
end main
