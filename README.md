# Helpful-Commands
- ## If we need to ignore a file from git track without caching or without adding it to gitignore then command =>
  ```git
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
- ## For pushing project to firebase for hosting purpose
  ```git bash
  npm install -g firebase-tools
  firebase login
  firebase init
  firebase deploy
  ```
- ## For iterating and changing file extension into different extension
  ```git bash
  for %f in (*.txt) do ren "%f" "%~nf.md"
  ```
- ## For testing different error codes, url below mention URL for testing
  - https://httpstat.us/500
  - https://httpstat.us/200 - Success
  - https://httpstat.us/404 - Not Found
  - https://httpstat.us/401 - Unauthorized
  - https://httpstat.us/403 - Forbidden
  - https://httpstat.us/503 - Service Unavailable
  - URL Pattern: https://httpstat.us/{status_code}
