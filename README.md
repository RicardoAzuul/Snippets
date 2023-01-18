# Snippets
Collection of various code snippets that don't really warrant having their own repo

Batch code to get datetime in ISO format. `echo %date% `gets date based on locale and region settings, so is not system independent.
```
@echo off
for /f "tokens=2 delims==" %%G in ('wmic os get localdatetime /value') do set datetime=%%G

echo %datetime%

set year=%datetime:~0,4%
set month=%datetime:~4,2%
set day=%datetime:~6,2%
set hour=%datetime:~8,2%
set minute=%datetime:~10,2%

echo %year%-%month%-%day% %hour%:%minute%
```
