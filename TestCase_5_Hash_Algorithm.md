# [5] : Verify Password Hash Algorithm

## Description

A POST to /hash should accept a password and hash it using SH512 algorithm.

### Precondition

The hash application should be listening at PORT 8088 and ready to accept curl request

### Assumptions

Hash application is running on windows machine.
Curl is installed on the machine to send request.

## Test Steps

1. Open Command Prompt
2. SET PORT=8088
3. Execute broken-hashserve_win.exe
4. Using curl application run the following command

curl -X POST -H "application/json" -d "{\"password\\":\"angrymonkey\"}" http://127.0.0.1:8088/hash

5. Esnure that the quotes inside the json object needs to be escaped on windows machine.  
6. Using curl application run the following command

curl -H "application/json" http://127.0.0.1:8088/hash/1
 
![Post Hash](hash-post-request.PNG)  

## Expected Result

The API should the return base64 password, encoded using hash SHA512 algorithm.   The base64 password can be validating using any online SHA512 online generators.  
For example, https://hash.online-convert.com/sha512-generator

