# [5] : Verify Password Hash Algorithm

## Description

A POST to /hash should accept a password and hash it using the SHA512 algorithm.

### Precondition

The hash application should be listening at PORT 8088 and ready to accept curl requests.

### Assumptions

Hash application is running on a windows machine.
Curl installed on the machine to send the request.

## Test Steps

1. Open Command Prompt
2. SET PORT=8088
3. Execute broken-hashserve_win.exe
4. Using curl application run the following command

curl -X POST -H "application/json" -d "{\"password\\":\"angrymonkey\"}" http://127.0.0.1:8088/hash

5. Make sure to add escape character to the quotes inside  JSON object for request on a windows machine. 
6. Using curl application run the following command

curl -H "application/json" http://127.0.0.1:8088/hash/1
 
![Post Hash](hash-post-request.PNG)  

## Expected Result

The API should return the base64 password encoded using the hash SHA512 algorithm.   The base64 password can be validated using any online SHA512 online generators.  
For example, https://hash.online-convert.com/sha512-generator

