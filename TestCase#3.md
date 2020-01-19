# [2] : Get Hash Request

## Description

A GET to /hash should accept a job identifier.  It should return the base64 encoded password hash for the corresponding POST request.

### Precondition

1. The hash application should be listening at PORT 8088 and ready to accept curl request.
2. A POST has been submitted to the hash application, and it successfully returned a hash identifier. 

### Assumptions

Hash application is running on windows machine.
Curl is installed on the machine for sending request.

## Test Steps

1. Open Command Prompt
2. SET PORT=8088
3. Execute broken-hashserve_win.exe
4. Using curl application run the following command
curl -H "application/json" http://127.0.0.1:8088/hash/1


 

## Expected Result

The curl command should return the base64 encoded password has.  For example, Password text "angrybirds" will return

NN0PAKtieayiTY8/Qd53AeMzHkbvZDdwYYiDnwtDdv/FIWvcy1sKCb7qi7Nu8Q8Cd/MqjQeyCI0pWKDGp74A1g==


