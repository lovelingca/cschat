<!-- Readme-->
**Table of Contents**  

- [Cschat](#cschat)
    - [Cschat Goal](#cschat-goal)
    - [Description](#description)
  - [Install](#%E5%AE%89%E8%A3%85)
  - [start](#%E4%BD%BF%E7%94%A8)
  - [Main focus](#%E4%B8%BB%E8%A6%81%E5%8A%9F%E8%83%BD)
    - [Simple description how to prevent the 3 main threats](#%E7%AE%80%E5%8D%95%E6%8F%8F%E8%BF%B0%E6%80%8E%E4%B9%88%E9%A2%84%E9%98%B2%E4%B8%BB%E8%A6%81%E5%A8%81%E8%83%81)
        - [XSS attack](#xss%E6%94%BB%E5%87%BB)
        - [SQL injection](#sql-injection)
        - [MITM attack](#mitm%E6%94%BB%E5%87%BB)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# Cschat Goal
Develop a secure messaging platform with end-to-end encryption.
In this project, we will develop a messaging platform that allows users to securely exchange information with end-to-end encryption. we will need to ensure that wer platform is not vulnerable to buffer overflow attacks. A buffer overflow attack is when an attacker sends more data into a buffer than it can handle, causing the buffer to overflow and potentially execute malicious code. we also need to ensure that all information exchanged on wer platform is encrypted to prevent unauthorized access.

## Description
We are using PHP here, PHP itself is not susceptible to traditional buffer overflow attacks.

## install

Installation Steps

## start
Webpage: https://cschat.fun/

## Main focus
The 3 main threats we focused on in this project is XSS attack, SQL injection and MITM attack.

## Simple description how to prevent the 3 main threats
### XSS attack
Our project simply retrieves data from a database and outputs the results in JSON format. In this case, our code is not outputting data directly in an HTML page, so there is no direct risk of an XSS attack.
### SQL injection
Use the *mysqli_real_escape_string* function to escape input variables to ensure that special characters are handled correctly and to prevent SQL injection attacks. The escaped value is then safely inserted into the SQL query to prevent malicious injection.
### MITM attack
We encrypt the information, and the data is encrypted in transit so that only a legitimate recipient with the correct decryption key can decrypt and read the contents of the data. This means that even if an attacker is able to intercept the communication data, they will not be able to understand its contents because the data is encrypted before transmission. By encrypting communications, sensitive information such as chat logs are not exposed in plaintext during transmission. Attackers, even if they intercept the encrypted data, will not be able to access this sensitive information because they do not have the key needed to decrypt it.

## How to use





