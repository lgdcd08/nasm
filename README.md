# ESTUDO  DE COMANDOS NASM
<p align="center">
<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRnsTdtRQu9EAccLdvEURLvRmeNtwWTkObL5g&s" width=200 height=200>

<p>

# primeiros comandos

*Programa hello world

```Assembly
global _start
    section .text
    _star:
        mov rax,1   ; preparta o sistema para fazer a escrita de um texto
        mov rdi,1   ;preparar a saída do texto na tela
        mov rsi,mensagem ;imprimir a mensagem na tela
        mov rdx,13  ; quantidade de caracteres
        syscall     ;chama o sistema para preparar a saída
        mov rax, 60  ;chamada para saída do sistema
        xor rdi,rdi ;executar a saída do sistema
        syscall     ;invocar o sistema operacional prra fechar

        section .data
        mensagem:db 'Hello world'  ,10   ;o valor 10 representa a quebra de linhagi
```
