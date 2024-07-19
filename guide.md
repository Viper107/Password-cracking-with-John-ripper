# John the Ripper Cracking Guide

## Overview

This guide provides step-by-step instructions for using John the Ripper to crack a password-protected `test.zip` file included in this repository. 

## Prerequisites

- **John the Ripper:** Make sure John the Ripper is installed on your system. Follow the installation instructions for your operating system from the [John the Ripper website](https://www.openwall.com/john/).

- **Zip2John Utility:** This is a utility included with John the Ripper for extracting hashes from ZIP files.

## Steps

### 1. Clone the Repository

First, clone this repository to your local machine:

git clone https://github.com/Viper107/Password-cracking-with-John-ripper.git
cd your-repository

### 2. Extract Hash from test.zip
Use the zip2john utility to extract the hash from the test.zip file. Run the following command:

zip2john test.zip > hashed.txt

This command creates a file named test_hash.txt containing the hash of the password.

### 3. Run John the Ripper
Start John the Ripper to crack the hash. Use the following command:

john hashed.txt

John the Ripper will begin the cracking process using its default wordlist and rules.

### 4. Use the password hash to crack the password using John the Ripper command:

john --format=zip hashed.txt

### 5. Congratulation you have cracked the password !

