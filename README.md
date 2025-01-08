# Helpful-Commands
- ## If we need to ignore a file from git track without caching or without adding it to gitignore then command =>
  git update-index --assume-unchange filename
- ## If we need to delete some file from windows, like by some extension file type then run below command as windows.bat file =>
  ```bat
  @echo off
  setlocal enabledelayedexpansion
  set "directory=C:\Users\ankit\Documents\Dheme\Dheme\pic\test\pic-test"
  for %%F in ("%directory%\*") do (
    set "filename=%%~nxF"
    set "basename=%%~nF"
    set "extension=%%~xF"

    set "copyname=!basename: - Copy (3)=!"
    set "copyname=!copyname: - Copy (2)=!"
    set "copyname=!copyname: - Copy=!"
    set "copyname=!copyname: (3)=!"
    set "copyname=!copyname: (2)=!"

    if "!basename!" neq "!copyname!" (
        del "%directory%\!filename!"
        echo Deleted: "%directory%\!filename!"
    )
  )
  echo Done.
  pause 
  ```
