# [6] : New request after service is shutdown

## Description

No additional password requests should be allowed when the shutdown is pending.

### Precondition

1. The hash application should be listening at PORT 8088 and ready to accept curl requests.
2. A POST submitted to the hash application, and it successfully returned a hash identifier. 

### Assumptions

Hash application is running on a windows machine.
Curl installed on the machine for sending requests.

## Test Steps

1. Open Command Prompt
2. SET PORT=8088
3. Execute broken-hashserve_win.exe
4. Using curl application run the following command
curl -d "shutdown" http://127.0.0.1:8088/hash
5. Using curl application run the following command
curl http://127.0.0.1:8088/stats


## Expected Result

The curl command should return curl: (7) Failed to connect to 127.0.0.1 port 8088: Connection refused
