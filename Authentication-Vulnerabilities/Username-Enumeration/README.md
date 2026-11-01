# Username Enumeration via Different Responses

## Objective
Identify valid usernames by analysing differences in login responses.

**Platform:** PortSwigger Web Security Academy  

## Methodology
- Intercepted the login request using Burp Suite.
- Used Burp Intruder to test a list of candidate usernames.
- Compared response messages and lengths to identify a valid username.
- Tested password candidates against the identified account.

## Result
Successfully identified a valid username and gained access to the account in the lab environment.

## Key Concepts
- Username enumeration
- HTTP response analysis
- Password guessing
- Authentication weaknesses
