# [1] : Shutdown Hash Application

## Description

The software should support a graceful shutdown request.  Meaning, it should allow any in-flight password hashing to complete, reject any new requests, respond with a 200, and shutdown.

### Precondition

The hash application should be listening at PORT 8088 and ready to accept curl requests.

### Assumptions

Testing is done on a windows machine.

## Test Steps

1. Open Command Prompt
2. SET PORT=8088
3. Execute broken-hashserve_win.exe 
4. curl -X POST -d "shutdown" http://127.0.0.1:8088/hash

## Expected Result

The hash application should complete any pending hash request before it is shutdown.
