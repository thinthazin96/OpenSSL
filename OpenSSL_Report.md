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
  
  <p>b. Compare the results for symmetric encryption (e.g., AES-CBC) and RSA signature.</p>
  <p> This shows the speed of AES 256 bits in CBC mode. As we know, AES is a symmetric block cipher which is faster and RSA is an asymmetric cryptosystem. That’s why RSA is a bit slower than AES.
  </p>
 
## 3. Using OpenSSL from commandline interface<a name="cmd"></a>
 
## 4. Exchange of encrypted data <a name="exchanged"></a>
  
