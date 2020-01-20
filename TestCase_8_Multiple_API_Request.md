# [8] : Multiple API Request

## Description

The software should be able to process multiple connections simultaneously.

### Precondition

None

### Assumptions

Hash application is running on windows machine.
Curl is installed on the machine to send request.

## Test Steps

1. Open Command Prompt
2. SET PORT=8088
3. Execute broken-hashserve_win.exe
4. Send curl -X POST -H "application/json" -d "{"password\":"angrymonkey"}" http://127.0.0.1:8088/hash
5. Open another command prompt
6. Send curl -X POST -H "application/json" -d "{"password\":"angrymonkey"}" http://127.0.0.1:8088/hash

## Expected Result

The service should accept multple API connections simultaneously

