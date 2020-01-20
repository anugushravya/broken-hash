# [7] : Open the broken hashserve program

## Description

The broken hashserve program should listen for Http connections when opened through the command prompt. 

### Precondition

None

### Assumptions

Hash application is running on a windows machine.
Curl is installed on the machine to send the request.

## Test Steps

1. Open Command Prompt
2. SET PORT=8088
3. Execute broken-hashserve_win.exe
 
## Expected Result

On a successful start, the application should wait for Http connections 

![Post Hash](application-start.PNG)  

