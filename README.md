# devsecops-learning-journal
Documenting my transition from Automation Testing to DevSecOps

Date: 25 April 2025
Status: Learning in public — Day 2

## Breach Analysis 001 — CircleCI 2023

As part of my study in to devsecops i have taken the CircleCI breach study case and listed out few points

1) Circle CI is a application where developer build the code , test it and run itl, where it needed contionus integration and long session tokens to test thier applications
2)one of the employee's machine got comprimised and using a malware INFOSTEALR he got access to all the secret keys(api,aws),sessiontokens,github tokens.
then he used the opportunity of the longlived session token to reuse them to login by bypassing the login credentials for almost a month, so the whole thing comprimised.
3)what could be done to avoid it is
  a)use shortlived session tokens adn forecd reauthentication overa certain time
  b)better sufficient EndPoint Detection And Response after malware installed on the employee device
  c)frequently rotating the secrets
  d)they should have better security regression testing having important cases such as
      1)testing with a newly generated session tokens os browser A and reproduce them in browser B 
      2)and also with different IP addresses
      3)checking the  expired tokens are still live 


