@echo off
REM
If EXIST c:\windows\ltsvc\ltsvc.exe GOTO EXIT
GOTO INSTALL

:INSTALL
copy \\domain-name.local\Netlogon\LabTechAgent.exe %windir%\temp
call %windir%\temp\LabTechAgent.exe /s
GOTO EXIT

:EXIT
Exit
