# Test Case Specification - PCTO Manager

**Team 3** - April 10, 2020

**Team Members:** Ambrosi Marco, Bonoldi Enrico, Lorenzoni Luca

**Revision History**

| **Version** | **Date** | **Name**      | **Description**  |
| ----------- | -------- | ------------- | ---------------- |
| 1           | 10/04/20 | Marco Ambrosi | Initial Document |


- [Test Case Specification - PCTO Manager](#test-case-specification---pcto-manager)
  - [Introduction](#introduction)
  - [Test Cases: PCTO Manager Application](#test-cases-pcto-manager-application)


## Introduction

This document provides the test cases to be carried out for the PCTO Manager Application. Each item to be tested is represented by an individual test case. Each case details the input and expected outputs.

## Test Cases: PCTO Manager Application

| Test ID          | 2.1                                                                                                              |
| ---------------- | ---------------------------------------------------------------------------------------------------------------- |
| Title            | Correct Login                                                                                                    |
| Feature          | Login to PCTO manager                                                                                            |
| Objective        | Show the right interface when the user is logged in.                                                             |
| Setup            | PCTO manager is hosted on a reachable machine.                                                                   |
| Test Data        | Login information<br>Username = admin<br>Password = prOvaAdmin18                                                 |
| Test Actions     | 1. Connect to the app via a web browser <br> 2. Enter login information                                          |
| Expected Results | System displays the right interface from where the user can interact with the system as an authenticated person. |

| Test ID          | 2.2                                                                   |
| ---------------- | --------------------------------------------------------------------- |
| Title            | Incorrect Password                                                    |
| Feature          | Login to PCTO manager                                                 |
| Objective        | The website must deny the access if the given password is invalid.    |
| Setup            | PCTO manager is hosted on a reachable machine.                        |
| Test Data        | Valid username, invalid password<br>Username = adminPassword = abc123 |
| Test Actions     | 1. Connect to the app via a web browser<br>2. Enter login information |
| Expected Results | System displays error message with option to retry.                   |


| Test ID          | 2.3                                                                         |
| ---------------- | --------------------------------------------------------------------------- |
| Title            | Incorrect Username                                                          |
| Feature          | Login to PCTO manager                                                       |
| Objective        | The website must deny the access if the given username is invalid.          |
| Setup            | PCTO manager is hosted on a reachable machine.                              |
| Test Data        | Invalid username, valid password<br>Username = marioPassword = prOvaAdmin18 |
| Test Actions     | 1. Connect to the app via a web browser<br>2. Enter login information       |
| Expected Results | System displays error message with option to retry.                         |

| Test ID          | 2.4                                                                                                       |
| ---------------- | --------------------------------------------------------------------------------------------------------- |
| Title            | Modify system settings                                                                                    |
| Feature          | Modify the app&#39;s system settings                                                                      |
| Objective        | Block the user if he&#39;s not authorized to access system settings.                                      |
| Setup            | PCTO manager is hosted on a reachable machine.                                                            |
| Test Data        | Valid username and password of a non-admin user<br>Username = luigi<br>Password = SuperPassword22         |
| Test Actions     | 1. Connect to the app via a web browser<br>2. Enter login information<br>3. Try to access system settings |
| Expected Results | System displays error message, saying the user is not authorized.                                         |

| Test ID          | 2.5                                                                                                 |
| ---------------- | --------------------------------------------------------------------------------------------------- |
| Title            | Invalid research                                                                                    |
| Feature          | Search for internships in the PCTO Manager                                                          |
| Objective        | Return a 404 error (not found) and not a 500 error (internal server error).                         |
| Setup            | PCTO manager is hosted on a reachable machine.                                                      |
| Test Data        | Search for: '6AI' class internships                                                                 |
| Test Actions     | 1. Connect to the app via a web browser<br>2. Enter login information3. Search for the invalid data |
| Expected Results | System displays error message with option to try again.                                             |
