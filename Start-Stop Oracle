@echo off
color 0a
title Star/Stop Oracle
set est=0

:menu1
cls
echo.
echo                ##################################################
echo                #                                                #
echo                 #   0000 0000   00  0000 0    0000             #
echo               = #   0  0 0  0  0  0 0    0    0                # =
echo             === #   0  0 0000  0  0 0    0    000 =Start/Stop= # ===
echo               = #   0  0 0  0  0000 0    0    0                # =
echo                 #   0000 0   0 0  0 0000 0000 0000             #
echo                #                                                #
echo                ##################################################
echo                                                     *By:Tedezed
echo                  ----------------------------------------------
echo.
echo                **************************************************
echo                 *                                              *
echo                 *       1.Iniciar Oracle                       *
echo                 *       2.Parar Oracle                         *
echo                 *       3.SQL PLUS                             *
echo                 *       4.Salir                                *
echo                 *                                              *
echo                **************************************************
echo.

if %est%==0 goto est0
if %est%==1 goto est1
if %est%==2 goto est2

:est0
echo                       (Introduce el numero de la opcion)
echo.
goto menu2 

:est1
echo                **************************************************
echo                 * Comandos START ejecutados ** Oracle Iniciado *
echo                **************************************************
echo.
goto menu2

:est2
echo                **************************************************
echo                 * Comandos STOP ejecutados **** Oracle Cerrado *
echo                **************************************************
echo.
goto menu2

:menu2
SET /P ver= Que desea hacer?:
if %ver%==1 goto ini
if %ver%==2 goto stp
if %ver%==3 goto sql
if %ver%==4 goto sal

:ini
cls
echo.
echo                **************************************************
echo                *                                                *
echo                *              Iniciando Oracle                  *
echo                *                                                *
echo                **************************************************
echo.
echo Iniciando OracleServiceORCL:
net start OracleServiceORCL
echo Iniciando OracleOraDb11g_home1TNSListener:
net start OracleOraDb11g_home1TNSListener
echo Iniciando OracleOraDb11g_home1ClrAgent:
net start OracleOraDb11g_home1ClrAgent
echo Iniciando OracleMTSRecoveryService:
net start OracleMTSRecoveryService
echo Iniciando OracleDBConsoleorcl:
net start OracleDBConsoleorcl
echo Iniciando Oracle VSS Writer Service:
net start "Oracle VSS Writer Service"
set est=1
echo.
echo =!=Inicio de Oracle terminado=!=
echo.
pause
goto menu1

 
:stp
cls
echo.
echo                **************************************************
echo                *                                                *
echo                *                 Stop Oracle                    *
echo                *                                                *
echo                **************************************************
echo.
echo Stop OracleServiceORCL:
net stop OracleServiceORCL
echo Stop OracleOraDb11g_home1TNSListener:
net stop OracleOraDb11g_home1TNSListener
echo Stop OracleOraDb11g_home1ClrAgent:
net stop OracleOraDb11g_home1ClrAgent
echo Stop OracleMTSRecoveryService:
net stop OracleMTSRecoveryService
echo Stop OracleDBConsoleorcl:
net stop OracleDBConsoleorcl
echo Stop Oracle VSS Writer Service:
net stop "Oracle VSS Writer Service"
set est=2
echo.
echo =!=Stop Oracle terminado=!=
echo.
pause
goto menu1

:sql
start C:\app\%USERNAME%\product\11.2.0\dbhome_1\BIN\sqlplus.exe

:sal
exit 
