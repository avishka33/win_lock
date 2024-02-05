# Win_lock
# How to Lock a Folder Using a Batch File
# Created By Avishka Shavinda

</p>
<p align="center">
<img src="https://raw.githubusercontent.com/avishka33/PRINCE-AVI-MD/main/Menu2.jpg" width="300" height="300"/>
</p>

Do you have items you want to keep hidden on your computer? Creating a locked folder using a batch script is a fun and easy way to hide files in low-stakes situations that don't require files to be encrypted. This Avi win_lok teaches you how to create a locker folder using a batch file.


ඔබට ඔබේ පරිගණකයේ සඟවා තබා ගැනීමට අවශ්‍ය අයිතම තිබේද? කණ්ඩායම් ස්ක්‍රිප්ට් එකක් භාවිතයෙන් අගුලු දැමූ ෆෝල්ඩරයක් නිර්මාණය කිරීම, ගොනු සංකේතනය කිරීමට අවශ්‍ය නොවන අඩු අවදානම් අවස්ථාවන්හිදී ගොනු සැඟවීමට විනෝදජනක සහ පහසු ක්‍රමයකි. මෙම Avi win-lock ඔබට කණ්ඩායම් ගොනුවක් භාවිතයෙන් ලොකර් ෆෝල්ඩරයක් සාදා ගන්නේ කෙසේදැයි කියා දෙයි.

# 1 step

Open Notepad. Notepad has an icon that resembles a blue notebook folder. Use the following steps to open Notepad:
Click the Windows Start Menu.
Type "Notepad."
Click Notepad.

Notepad විවෘත කරන්න. Notepad හි නිල් සටහන් පොත් ෆෝල්ඩරයකට සමාන අයිකනයක් ඇත. Notepad විවෘත කිරීමට පහත පියවර භාවිතා කරන්න:
වින්ඩෝස් ආරම්භක මෙනුව ක්ලික් කරන්න.
"නෝට්පෑඩ්" ටයිප් කරන්න.
Notepad ක්ලික් කරන්න.
# 2 step

Copy the following batch script. The batch script is in the box below. Highlight the entire script. Right-click it and click Copy, or press "Ctrl + C."
පහත බැච් ස්ක්‍රිප්ට් එක කොපි කරන්න. batch script එක පහත කොටුවේ ඇත. සම්පූර්ණ පිටපත ඉස්මතු කරන්න. එය දකුණු-ක්ලික් කර පිටපත් කරන්න ක්ලික් කරන්න, නැතහොත් "Ctrl + C" ඔබන්න.

# script

  cls

@ECHO OFF

title Folder Locker

if EXIST "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}" goto UNLOCK

if NOT EXIST Locker goto MDLOCKER

:CONFIRM

echo Are you sure you want to Lock the folder (Y/N)

set/p "cho=>"

if %cho%==Y goto LOCK

if %cho%==y goto LOCK

if %cho%==n goto END

if %cho%==N goto END

echo Invalid choice.

timeout 1

goto CONFIRM

:LOCK

ren Locker "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}"

attrib +h +s "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}"

echo Folder locked

timeout 3

goto End

:UNLOCK

@echo off
set "psCommand=powershell -Command "$pword = read-host 'Enter Password to Unlock folder' -AsSecureString ; ^
    $BSTR=[System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($pword); ^
        [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)""
for /f "usebackq delims=" %%p in (`%psCommand%`) do set password=%%p

if NOT %password%== <මෙතනට පාස්වර්ඩ් එක ගහන්න/ enter password> goto FAIL

attrib -h -s "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}"

ren "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}" Locker

echo Folder Unlocked Successfully

timeout 1

goto End

:FAIL

echo Invalid Password

timeout 1

goto end

:MDLOCKER

md Locker

echo Locker created successfully

timeout 5

goto End

:End


# 3 step


Paste the code into Notepad. Go back to your blank Notepad document. Right-click at the top of the page and click Paste, or press "Ctrl + V" to paste the code into Notepad.
කේතය Notepad එකට අලවන්න. ඔබගේ හිස් Notepad ලේඛනය වෙත ආපසු යන්න. පිටුවේ ඉහළින් ඇති දකුණු-ක්ලික් කර පේස්ට් ක්ලික් කරන්න, නැතහොත් කේතය Notepad වෙත ඇලවීමට "Ctrl + V" ඔබන්න.

# 4 step 


Change the password. Locate where it says " <මෙතනට පාස්වර්ඩ් එක ගහන්න/ enter password>" in the script. It's about three-quarters of the way down. It's in the line that starts with "if NOT %password%==".

මුරපදය වෙනස් කරන්න. එය ස්ක්‍රිප්ට් එකේ " <මෙතනට පාස්වර්ඩ් එක ගහන්න/ enter password>" යැයි කියන ස්ථානය සොයා ගන්න. හතරෙන් තුනක් විතර පහලට. එය "%මුරපද නොවේ%==" ලෙසින් ආරම්භ වන පේළියේ ඇත.


# 5 step 

Save the document as a batch file. Use the following steps to save the Notepad document as a batch file:
Click File.
Click Save as.
Click the drop-down menu next to "Save as type."
Select All files (*.*).
Type a file name in the File Name field (i.e. LockedFolder).
Type ".bat" at the end of the file name (I.e. LockedFolder.bat).
Click Save.

ලේඛනය කණ්ඩායම් ගොනුවක් ලෙස සුරකින්න. Notepad ලේඛනය කණ්ඩායම් ගොනුවක් ලෙස සුරැකීමට පහත පියවර භාවිතා කරන්න:
ගොනුව ක්ලික් කරන්න.
ලෙස සුරකින්න ක්ලික් කරන්න.
"වර්ගය ලෙස සුරකින්න" අසල ඇති පතන මෙනුව ක්ලික් කරන්න.
සියලුම ගොනු තෝරන්න (*.*).
ගොනු නාමය ක්ෂේත්රයේ ගොනු නාමයක් ටයිප් කරන්න (එනම් LockedFolder).
ගොනු නාමයේ අවසානයේ ".bat" ටයිප් කරන්න (එනම් LockedFolder.bat).
සුරකින්න ක්ලික් කරන්න.
