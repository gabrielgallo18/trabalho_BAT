@echo off
cls
:menu
cls

date /t
  
## Menu 
```
echo            MENU TAREFAS
echo  +++++++++++++++++++++++++++++++++++
echo * 1. Fazer Backup                  *
echo * 2. Escanear Disco Local          *
echo * 3. Painel de Controle            *
echo * 4. Sair                          * 
echo * 5. Versao do Sistema             * 
echo * 6. Help                          * 
echo  +++++++++++++++++++++++++++++++++++
```

##opcao
```
set /p opcao= Escolha uma opcao: 
echo ------------------------------
if %opcao% equ 1 goto opcao1
if %opcao% equ 2 goto opcao2
if %opcao% equ 3 goto opcao3
if %opcao% equ 4 goto opcao4
if %opcao% equ 5 goto opcao5
if %opcao% equ 6 goto opcao6
```

## Relizar um Backup
```
:opcao1
cls
xcopy "C:\origem" "D:\destino" /e/h/s/y/d
echo +++++++++++++++++++++++++++++++++++
echo *      Backup concluido           *
echo +++++++++++++++++++++++++++++++++++
pause
goto menu
```

## Escanear o Disco
```
:opcao2
cls
echo +++++++++++++++++++++++++++++++++++
echo *     Escaneamento de disco       *
echo +++++++++++++++++++++++++++++++++++
chkdsk c:
pause
goto menu
```

## Abrir o painel de controle
```
:opcao3
cls
control.exe
pause
goto menu
```

## Sair do programa
```
:opcao4
cls
exit
```

## Versão do programa
```
:opcao5
echo +++++++++++++++++++++++++++++++++++++++++++++++
echo * V.0.0.1 *
echo +++++++++++++++++++++++++++++++++++++++++++++++
pause
goto menu
```

## Descrição (help)
```
:opcao6
echo +++++++++++++++++++++++++++++++++++++++++++++++
echo * Opcao 1 - Essa opcao ira realizar a limpeza da sua lixeira                  *
echo * Opcao 2 - Essa opcao ira realizar um backup na pasta deseja                 *
echo * Opcao 3 - Essa opcao ira realizar um scaneamento no seu disco rigido        *
echo * Opcao 4 - Essa opcao ira abrir o seu painel de controle do computador       *
echo * Opcao 5 - Essa opcao ira fechar o sistema                                   *
echo * Opcao 6 - Essa opcao ira mostrar a versão do sistema caso deseja saber      *
echo * Opcao 7 - Essa opcao ira abrir a lista de comandos que serão possivel fazer *
echo +++++++++++++++++++++++++++++++++++++++++++++++
pause
goto menu
```
