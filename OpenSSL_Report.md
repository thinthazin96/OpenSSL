<h1 align=center> OpenSSL Report <h1>
  
# Table of contents
  
1. [OpenSSL installation](#installation)
2. [Performance of OpenSSL](#performance)
3. [Using OpenSSL from commandline interface](#cmd)
4. [Exchange of encrypted data](#exchanged)

## 1. OpenSSL installation <a name="installation"></a>
  ![Task 1](Task1-a,b.jpg)
  
  <p> In this project, I used Linux system Ubuntu flavor to test encryption and decryption.</p>

   <p>a. Start the OpenSSL command line
      <ul>
         <li><i>openssl version</i> = to check whether the openssl is installed on my system or not.</li>
      </ul>
   </p>

   <p>b. List commands by type 
      <ul>
        <li><i>openssl list -command</i> = shows the list of commands</li>
        <li><i>openssl list -cipher-commands</i> = to see the list of built-in cipher algorithm commands with different modes and bits to encrypt and decrypt data.</li>
        <li><i>openssl list -digest -commands</i> = shows a list of available digest algorithms to process the message.</li>
      </ul>
    </p>
    
  ![Task 1](Task1-c.jpg)

   <p> c. Use the help to find out more about OpenSSL
      <ul>
        <li><i>openssl help</i> = command shows the help menus.</li>
      </ul>
   </p>
   
## 2. Performance of OpenSSL <a name="performance"></a>
  ![Task 2](Task2.jpg)
  
  ![Task 2-a](Task2-a.jpg)
  
  <p>a. Make a speed test on your PC-platform with the speed command. </p>
  <p>The output of the speed command line means run the md4 hash routine in a loop for 3 seconds with a 16-byte input. After 3 seconds, observe that we ran just a bit over 17 million iterations. That's about 51 million bytes processed. This shows the speed of RSA 2048bits encryption per second and decryption per second on my PC.</p>
  
  ![Task 2-b](Task2-b.jpg)
  
  <p>b. Compare the results for symmetric encryption, AES-CBC, and RSA signature.</p>
  <p> This shows the speed of AES 256 bits in CBC mode. As we know, AES is a symmetric block cipher which is faster and RSA is an asymmetric cryptosystem. That’s why RSA is a bit slower than AES.
  </p>
 
## 3. Using OpenSSL from commandline interface<a name="cmd"></a>
![Task 3](Task3.jpg)

 <p>a. Create a text file with some input and encrypt it using. </p>
 <p> I. AES-128 CBC
  <p>First I created a message in nano pad to encrypt and decrypt.</p>
    <ul>
      <li>nano msg = to open the nano pad to write message</li>
      <li>cat msg = display the content of msg file</li>
    </ul>
      
Then set the password for AES encryption and the same password will be used for decryption.
    <ul>
      <li>openssl enc -aes-128-cbc -in msg = encrypt the message using 256 bit AES encryption and CBC mode and define the input file which is msg</li>
      <li>openssl enc -aes-128-cbc -in msg -out enc = The ciphertext was generated and store the output file called enc</li>
    </ul>
 </p>
 
 <p> II. AES-256 CTR </p>
 
 ![Task 3](Task3-ii.jpg)
 
 <p> III. DES </p>
 
 ![Task 3](Task3-iii.jpg)
 
AES and DES is a symmetric block cipher which means it uses the same key to encrypt and decrypt data as we did above. In the next task, we are going to use the RSA algorithm to do encryption and decryption.

B. creating a 2048 bit RSA public and private key

![Task 3](Task-3b.jpg)

<ul>
  <li>Openssl genrsa -out keypair.pem 2048 = generate private and public key which is 2048 bit long by using RSA and store the keys in keypair.pem</li>
</ul>

![Task 3](Task-3b1.jpg)

Then, we separate the public key from the keypair.pem and store it in publickey.pem.This public key has to be sent to the other user to encrypt the message.

## 4. Exchange of encrypted data <a name="exchanged"></a>
  
