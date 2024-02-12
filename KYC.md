# Develop KYC Module

## Assignment 

To build a service to which can verify the customer details with an external provider. 

## Description 
Assume we have a stock trading platform. To perform any trading operations, the user has to complete their verification process. 
    </br>
**Assume:** 
- Authentication is a micro-service and can ready APIs for all auth activities 
- There is an external (to the system you are designing), third-party REST API where identity information can be submitted and a response received communicating whether the user's identity could be verified. Its not an instantaneous process rather works on async. 
    </br>
**System requirements** 
- Client has an API to always check the status
- The verification request must be raised from the client directly to external service without maintaining any state at client level. 
- All the state management has to be retained at server level. 
- After 3 failed / incorrect attempts, the verification service should be blocked. 
- The external verification API processes the data asynchronously. A webhook to an endpoint supplied in the initial request. Callback will contain the result of the identity verification request which would be either success or failure. 
  

  ## Tasks: 
  - Design a sequence diagram & high-level architecture </br>
  **Or**
  - Design a statemachine & high-level architecture. 
