# Password Hash API Testing

The password hash is a Windows API that allows user to hash their password.  The application uses the SHA512 algorithm to hash the password. The project is used to track the testing status of the application before application deployment to production. 

## Getting Started

Download the broken-hashware.exe application and save it to c:\

### Prerequisites

The application requires curl or equivalent tool to send API requests. 

### Installing

1. SET PORT=8080
2. SET an environment variable for PORT with a value of 8080. Without the environment variable, the application will crash. 

## Running the tests

The API supports three endpoints. 

1. A ​POST​ to ​/hash​ should accept a password.  It should return a job identifier immediately.  It should then wait 5 seconds and compute the password hash. The hashing algorithm should be SHA512.
2. A ​GET​ to ​/hash​ should accept a job identifier.  It should return the base64 encoded password hash for the corresponding POST request.
3. A ​GET​ to ​/stats​ should accept no data.  It should return a JSON data structure for the total hash requests since the server started and the average time of a hash request in milliseconds

A total of 8 test cases are written to validate the API endpoints.  The test cases cover multiple operations, and in some cases, it is a combination of any of the three endpoints.   

     - TestCase_1_POST_Shutdown.md 
    - TestCase_2_POST_Hash.md     
    - TestCase_3_Get_Hash.md     
    - TestCase_4_GET_Stats.md 
    - TestCase_5_Hash_Algorithm.md     
    - TestCase_6_Shutdown_New_RQST.md     
    - TestCase_7_Open_API.md
  - TestCase_8_Multiple_API_Request.md

## Versioning

0c3d817


## Authors

JumpCloud

## License

This project is licensed under the MIT License
