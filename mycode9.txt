.model small               
.stack 100h
.code 

main proc 
    mov al,5
    mov bl,2
    div bl ;al=al/bl
    
    mov cl,al
    mov ch,ah
    
    mov ah,2
    mov dl,cl
    add dl,48
    int 21h 
    
    mov ah,2
    mov dl,10
    int 21h
    mov dl,13
    int 21h
    
    mov ah,2
    mov dl,ch
    add dl,48
    int 21h
    
    exit:
    mov ah,4ch
    int 21h  
    main endp
end main
    
    