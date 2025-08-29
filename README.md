# Hello.asm
Impressão de mensagem na tela assembly
section .data
msg db 'Olá, Mundo!', 0

section .text
global _start

_start:
    ; Imprimir a mensagem
    mov eax, 4
    mov ebx, 1
    mov ecx, msg
    mov edx, 13
    int 0x80

    ; Sair do programa
    mov eax, 1
    xor ebx, ebx
    int 0x80
    
