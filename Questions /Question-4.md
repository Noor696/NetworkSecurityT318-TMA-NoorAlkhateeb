## Question 4: 
--------------------

### Encryption using Openssl tool [20 Marks]


a.	**Task 1.** Create two plaintext files(2 Marks) 

   1. **name.txt**: a text file containing the first 8 characters of your name. The file should be exactly 8 Bytes in length. There must be no newline character.
   2. **repeated.txt**: a text file containing the first 8 characters of your name, repeated 10 times. The file should be exactly 80 Bytes in length. There must be no newline character.
   
Also choose a random key to be used for DES, and save the 16 digit hexadecimal value in a file key.txt. There are different ways to generate a random value, an easy way is to use openssl rand (try man rand for an explanation).



b.	**Task 2.** Encrypt the first plaintext file, name.txt using DES, your key and ECB mode of operation. The ciphertext should be in a file named name.enc. Look at the binary version of the file. Note that OpenSSL adds a 1 Byte integrity check to the end of the ciphertext. you can ignore these last 8 Bytes.SG 2012-12-07: To avoid the integrity check, which may cause confusion later, use the nopad option. Create a text file, discussion.txt, and include the exact command you used to encrypt the first plaintext file. (3 Marks)



c.	**Task 3.** Determine if the avalanche effect is present in the cipher when different key values are used. (Remember to ignore the last 8 Bytes of ciphertext - the integrity check - when comparing values). You should try at least 3 different keys. In the file discussion.txt, add an explanation of how you tested for the avalanche effect (including the keys you used), your results and conclusions. You don't have to study the avalanche effect with different plaintexts - only with different keys. (SG 2012-12-10: Be careful when changing the key: recall that DES takes a 64-bit key as input but only uses 56 of those bits in the encryption - 8 bits are used for parity check. So when changing the key, make sure you change one of the 56 bits. The 8th, 16th, 24th, ...64th bit of the input key are not used in encryption). (6 Marks)


d.	**Task 4.** Encrypt the second plaintext file, repeated.txt, using DES, the same key and with three different modes of operation: ECB, CBC and OFB. Save the ciphertext as repeated-ecb.enc, repeated-cbc.enc and repeated-ofb.enc. Look at the output binary values and in the file discussion.txt, comment on the different binary values (i.e. do you notice anything about them?). (3 Marks)

e.	**Task 5.** In each of the 3 ciphertext files from Task 4, modify 1 bit in the first byte, creating three new files: repeated-ecb-mod.enc, repeated-cbc mod.enc and repeated-ofb-mod.enc. (3 Marks)


f.	**Task 6.** Decrypt the 6 ciphertext files, saving the output of each as decrypt-ecb.txt, decrypt-cbc.txt, decrypt-ofb.txt, decrypt-ecb-mod.txt, decrypt-cbc-mod.txt and decrypt-ofb-mod.txt. please add your comments on the decrypted values. (3 Marks)



Explain your notes/comments from the different tasks. you may include copy-and-paste of output of your commands or print screen if it is useful in the explanation. Also must clarify in details your changes in each round when you solve task3.It is recommended to write down all the results of your steps in a table. also you have to submit one zip file after naming it Q4-[yourid]-[name] the zip file contains the following  files.
1.	name.txt
2.	repeated.txt
3.	key.txt
4.	name.enc
5.	repeated-ecb.enc
6.	repeated-cbc.enc
7.	repeated-ofb.enc
8.	repeated-ecb-mod.enc
9.	repeated-cbc-mod.enc
10.	repeated-ofb-mod.enc
11.	decrypt-ecb.txt
12.	decrypt-cbc.txt
13.	decrypt-ofb.txt
14.	decrypt-ecb-mod.txt
15.	decrypt-cbc-mod.txt
16.	decrypt-ofb-mod.txt



[Question 1 : network security tools](/Questions%20/Question-1.md)

[Question 2 : Classical Encryption Techniques Cryptoanalysis](/Questions%20/Question-2.md)

[Question 3 : Encryption using a block cipher ](/Questions%20/Question-3.md)

