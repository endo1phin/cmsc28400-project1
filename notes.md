# CMSC 28400 Project 1 Notes

## Basic Categorization
(Use shell command `head -c 100 ctxts/*` to print the first 100 bytes of each file)

- Pure letters: 01 03 04 06 10 12 13 14
  - Space/punctuation likely kept: 01 04 14
  - Space/punctuation likely changed: 03 06 10 12 13
- Pure numbers: 02 05 08 11 17 18 19 20
- Hybrid letters/numbers: 07 09 15 16

### Observations

Ciphertexts in the pure letters category has several common characteristics:
- The letters are all lowercase, meaning the mapping likely contains only lowercase letter to lowercase letter (from 0x61 (97 in decimal) to 0x7A (122 in decimal) in utf-8 encoding)

### Pure Letters

#### 01

#### 06
Several repetitive short phrases suggests that this may be either shift or substitution. 



## Initial Analysis - Tools

### Shift Cipher
To identify shift cipher, we simply use exhaustive key search: print out all possible shifts and find the most sensible result. 

### Substitution Cipher

To identify a potential substitution cipher, we can match the frequency of letters in cipher text to the frequency of letters in normal texts. We start from the most frequent letter and then work towards lower frequencies.

### Vigenere Cipher
To break the vigenere cipher:
1. Guess l base on distance between repeating patterns in ctxt
2. Shift ctxt by n amount, the shift with most matching patterns is the guess for l
3. Given key length l, divide cipher text into buckets
4. For each bucket, use the shift cipher attack


## Initial Analysis - Results

## Decryption Notes

### 01
Encryption method: shift, pure lower case letter, amount=12
Message: 
```
hey alex, you've got to stop reusing that one time pad. the students are onto us. let's switch to a stronger cipher. david
```

### 02



### 03
### 04
### 05
