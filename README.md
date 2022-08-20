@echo off
cls
:menu
cls

date /t
  
## Opçoes  
echo            MENU TAREFAS
echo  +++++++++++++++++++++++++++++++++++
echo * 1. Esvaziar a Lixeira            * 
echo * 2. Fazer Backup                  *
echo * 3. Escanear Disco Local          *
echo * 4. Painel de Controle            *
echo * 5. Sair                          * 
echo * 6. Versao do Sistema             * 
echo * 7. Help                          * 
echo  +++++++++++++++++++++++++++++++++++


set /p opcao= Escolha uma opcao: 
echo ------------------------------
if %opcao% equ 1 goto opcao1
if %opcao% equ 2 goto opcao2
if %opcao% equ 3 goto opcao3
if %opcao% equ 4 goto opcao4
if %opcao% equ 5 goto opcao5
if %opcao% equ 6 goto opcao6
if %opcao% equ 7 goto opcao7

## Opçoes
:opcao1
cls
rd /S /Q c:\$Recycle.bin
echo +++++++++++++++++++++++++++++++++++
echo *      Lixeira Esvaziada          *
echo +++++++++++++++++++++++++++++++++++
pause
goto menu

## Opçoes
:opcao2
cls
xcopy "C:\origem" "D:\destino" /e/h/s/y/d
echo +++++++++++++++++++++++++++++++++++
echo *      Backup concluido           *
echo +++++++++++++++++++++++++++++++++++
pause
goto menu

## Opçoes
:opcao3
cls
echo +++++++++++++++++++++++++++++++++++
echo *     Escaneamento de disco       *
echo +++++++++++++++++++++++++++++++++++
chkdsk c:
pause
goto menu

## Opçoes
:opcao4
cls
control.exe
pause
goto menu

## Opçoes
:opcao5
cls
exit

## Opçoes
:opcao6
echo +++++++++++++++++++++++++++++++++++++++++++++++
echo * V.0.0.1 *
echo +++++++++++++++++++++++++++++++++++++++++++++++
pause
goto menu

## Opçoes
:opcao7
echo +++++++++++++++++++++++++++++++++++++++++++++++
echo * Opção 1 - Essa opcao ira realizar a limpeza da sua lixeira                  *
echo * Opção 2 - Essa opcao ira realizar um backup na pasta deseja                 *
echo * Opção 3 - Essa opcao ira realizar um scaneamento no seu disco rigido        *
echo * Opção 4 - Essa opcao ira abrir o seu painel de controle do computador       *
echo * Opção 5 - Essa opcao ira fechar o sistema                                   *
echo * Opção 6 - Essa opcao ira mostrar a versão do sistema caso deseja saber      *
echo * Opção 7 - Essa opcao ira abrir a lista de comandos que serão possivel fazer *
echo +++++++++++++++++++++++++++++++++++++++++++++++
pause
goto menu
