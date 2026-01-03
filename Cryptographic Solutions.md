## Introduction
- **Encryption**
    
    - Process of converting ordinary information into an unintelligible form
        
- **Types of Data**
    
    - **Data at Rest**
        
        - Inactive data that is being archived
            
    - **Data in Transit**
        
        - Data that moves across the network
            
        - Resides inside RAM or moves to and from the processor
            
    - **Data in Use**
        
        - Data undergoing a current constant state of change
            
- **Cipher**
    
    - An algorithm that performs encryption or decryption
        
- **Encryption Strength**
    
    - Depends on the key and not the algorithm
        
- **Key**
    
    - Essential piece of information that determines the output of a cipher
        
    - Longer the key, the better the security

--- 

## Symmetric vs Asymmetric 

### Basic Introduction 

#### Classification based on key and algorithm type

- Symmetric Algorithm (Private Key) - 
  - Encryption Algorithm in which both the sender and the receiver must know the same shared secret using a privately held key
  
  - The main challenge is that as p2p connections increase, the number of keys increases, and we encounter a distribution problem, which leads to a lack of confidentiality when multiple people know that shared secret

- Asymmetric Algorithm(Public and Private Key) - 
  - An Encryption algorithm where different keys are used to encrypt and decrypt the data 
    
  - One key is for encryption and the other is for decryption

- Hybrid Implementation -
  - Utilizes asymmetric encryption to securely transfer a private key that can then be used with symmetric encryption

#### Classification based on the mathematical algorithm

- Stream Cipher -
  - Utilizes a keystream generator to encrypt data bit using a encrypt data bit by bit using a mathematical XOR function to create the ciphertext
- Block Cipher - 
  - Breaks the input into fixed-length blocks of data and performs the encryption on each block

## Symmetric Algorithms 

- What is it?
  - Method of encryption where the same key is used for both encryption and decryption of data

- Data Encryption Standard (DES) 
  - Encryption algorithm which break the input into 64-bit blocks and uses transportation and substitution to create ciphertext using an effective key strength of only 56-bits
    
- Triple DES (3DES)
  - Encryption algorithm which uses three separate symmetric keys to encrypt , decrypt, then encrypt the plaintext into ciphertext in order to increase the strength of DES

- International Data Encryption Algorithm (IDEA)
  - Symmetric block cipher, which uses 64-bit blocks to encrypt plaintext to ciphertext

- Advanced Encryption Standard (AES)
  - Symmetric block cipher that uses 128-bit, 192-bit or 256-bit blocks and a matching encryption key size to encrypt plaintext into ciphertext

- Blowfish
  - Symmetric block cipher that uses 64-bit blocks and a variable length encryption key to encrypt plaintext into ciphertext

- Twofish 
  - Provides the ability to use 128-bit blocks in its encryption algorithm and uses 128-bit , 192-bit or 256-bit encryption keys

- RC Cipher Suite 
  - Created by Ron Rivest , a cryptographer who’s created six algorithms under the name RC which stands for Rivest Cipher

- Rivest Cipher (RC4)
  - Symmetric stream cipher using a variable key size from 40-bits to 2048-bits that is used in SSL(Secure Socket Layer) and WEP(Wired Equipment Privacy)

- Rivest Cipher (RC5)
  - Symmetric block cipher that uses key sizes up to 2048-bits

- Rivest Cipher (RC6)
  - Symmetric block cipher that was introduced as a replacement for DES but AES was chosen instead


## Asymmetric Algorithms

- What is it?
  - Does not require a shared secret key, often referred to as public key cryptography since their key is considered to be freely and openly public 
  - Public Key cryptography provides us with confidentiality , integrity , authentication and non-repudiation
  - Confidentiality - Encrypt with public key and decrypt with private
  - Non-repudiation - Encrypt with private key and decrypt with public

- Digital Signature 
  - A hash digest of a message encrypted with the sender’s private key to let the recipient know the document was created and sent by the person claiming to have sent it

- Diffie-Hellman (DH)
  - Used to conduct key exchanges and secure key distribution over an unsecure network, susceptible to on-path or man-in-the-middle attacks 

- RSA
  - Asymmetric algorithm that relies on the mathematical difficulty of factoring large prime numbers
  - 1024 bits and 4096 bits based key-size

- ECC
  - Heavily used in mobile devices and it’s based on the algebraic structure of elliptical curves over finite fields to define its keys , Very efficient and heavily used in small chips 
  - Elliptic Curve Diffie-Hellman (ECDH)
    - ECC version of the popular Diffie-Hellman key exchange protocol

  - Elliptic Curve Diffie-Hellman Ephemeral (ECDHE)
    - Uses a different key for each portion of the key establishment process inside the diffie-hellman key exchange
        
  - Elliptic Curve Digital Signature Algorithm(ECDSA)
    - Used as a public key encryption algorithm by the US government in their digital signatures

## Increasing Hash Security 

 - Hashing is a common method of storing passwords inside systems
 - Pass the hash attack 
   - Hacking technique that allows the attacker to authenticate to a remote server or service by using the underlying hash of a users password instead of requiring the associated plaintext password
   - Mimikatz is one such tool which provides the ability to automate the process of harvesting the hashes and conducting the attack

- Birthday Attack
   - Occurs when an attacker is able to send two different messages through a hash algorithm and it results in the same identical hash digest referred to as a collision 
   - Based on the birthday paradox

- Key Stretching 
   - Technique that is used to mitigate a weaker key by increasing the time needed to crack it

- Salting 
  - Adding random data into a one-way cryptographic hash to help protect against password cracking techniques
  - Dictionary Attack 
    - When an attacker tries every word from a predefined list 
  - Brute Force Attack
    - When an attacker tries every possible password combination
  - Rainbow Tables
    - Precomputed table for reversing cryptographic hash functions

- Nonce
  - Stands for “number used once” , is a unique , often random number that is added to password-based authentication process

## Public Key Infrastructure

- What is it
  - An entire system of hardware, software , policies , procedures and people that is based on asymmetric encryption

|**Feature**|**Public Key Cryptography (PKC)**|**Public Key Infrastructure (PKI)**|
|---|---|---|
|**Definition**|A method of encryption using two mathematically linked keys (Public & Private).|A comprehensive system to manage keys and digital certificates.|
|**Primary Goal**|Confidentiality (Encryption) & Authenticity (Digital Signatures).|Identity Verification & Trust Management.|
|**Components**|Algorithms (RSA, ECC), Key Pairs.|Certificate Authorities (CA), Registration Authorities, CRLs, Digital Certificates.|
|**Analogy**|The **lock and key mechanism** used to secure a safe.|The **passport office** that issues IDs so you know exactly _who_ owns the safe.|
|**Dependency**|Can exist without PKI (e.g., PGP), but is less scalable.|Relies entirely on PKC to function.|

- Certificate Authority 
  - Issues digital certificates and keeps the level of trust between all of the certificate authorities around the world

- Key Escrow 
  - Process where cryptographic keys are stored in a secure third-party location, which is effectively an “escrow”


## Digital Certificates

- What is it
  - Digitally signed electronic document that binds a public key with a user’s identity

- Wildcard certificate 
  - Allows all of the subdomains to use the same public key certificate and have it display as valid, if my main server gets affected and then my certificate gets revoked then then the the other subdomains certificates will get revoked 

- Subject Alternate Name
  - Certificate that specifies what additional domains and IP addresses are going to be supported
    
- Single-Sided Certificate 
  - Only requires the server to be validated , hence one one sided authentication between the user and the web server
    
- Dual-sided Certificate
  - Requires both the server and the user to be validated , certificate exchange between webserver and the user for verification but more processing 
    
- Self-Signed Certificate 
  - Digital Certificate that is signed by the same entity whose identity it certifies, less trust cuz no external verification , mainly for development

- Third-Party Certificate 
  - Digital certificate issued and signed by a trusted certificate authority (CA)

- Root of trust 
  - Each certificate is validates using the root of trust or the chain of trust , most of the time the root of trust is a third-party provider 
    

- Certificate Authority 
  - Trusted third party who is going to issue these digital certificates 

- Registration Authority 
  - Requests identifying information from the user and forwards that certificate request up to the certificate authority to create the digital certificate

- Certificate signing request 
  - A block of encoded text that contains information about the entity requesting the certificate , it may include a said set of details like Org name , Domain Name , locality and country
    
- Certificate Revocation List 
  - Serves as an online list of digital certificates that the certificate authority has already revoked

- Online certificate status protocol (OCSP)
  - Allows to determine the revocation status of any digital certificate using its serial number
    
- OCSP stapling 
  - Allows the certificate holder to get the OCSP record from the server at regular intervals
    
- Public Key Pinning 
  - Allows HTTPS website to resist impersonation attacks from users who are trying to present fraudulent certificates
    
- Key Escrow 
  - Occurs when a secure copy of a user’s private key is held

- Key recovering agent 
  - Specialized type of software that allows the restoration of a lost or corrupted key to be performed
    
## Blockchain

- What is it
  - A shared immutable ledger for recording transactions ,tracking assets and building trust
  - A blockchain is a really long series of information with each block containing information
  - ![[Pasted image 20251225234820.png]]

- Public-Ledger
  - A record-keeping system that maintains participants’ identities in a secure and anonymous format 

- Smart Contracts 
  - Self executing contracts where the terms of agreements or conditions are written directly into line of code
  - The decentralized and transparent nature of the blockchain ensures that once a smart contract is deployed, it cannot be altered , making the agreement tamper-proof and trustworthy
    
- Permissioned Blockchain
  - Used for business transactions and it promotes new levels of trust and transparency using this immutable public ledgers
  - Since its located inside a immutable public ledger , nobody can modify it and we all know exactly where everything has been located and what has been done to it
    
## Encryption Tools

- Trusted Platform Module (TPM)
  - Dedicated microcontroller designed to secure hardware through integrated cryptographic keys, A common example is the bitlocker encryption feature in the windowsOS

- Hardware Security Module (HSM)
  - A physical device that safeguards and manages digital keys, primarily used for mission-critical situations like financial transactions
  - Not only does an HSM securely generate cryptographic keys, but it also provides accelerated cryptographic operations
    
- Key Management System (KMS)
  - Integrated approach for generating, distributing and managing cryptographic keys for devices and applications
    
- Secure Enclave 
  - Co-processor integrated into the main processor of some devices , designed with the sole purpose of ensuring data protection
  - By keeping this data separate from the main processor, even if a device gets compromised withing the Secure Enclave remains untouched
    
## Obfuscation

- Steganography
  - Derived from the Greek words meaning “covered writing”, and it is all about concealing a message within another so that the very existence of the message in hidden
  - The primary goal here isn’t just to prevent unauthorized access to the data, but to prevent the suspicion that there’s any hidden data at all 
  - Steganography is frequently used alongside encryption for an extra layer of security

- Tokenization 
  - Transformative technique in data protection that involves substituting sensitive data elements with non-sensitive equivalents, called tokens, which have no meaningful value

- Data Masking 
  - Used to protect data by ensuring that it remains recognizable but does not actually include sensitive information
  - Data masking is also really prevalent in industries that handle vast amounts of personal data
    
## Cryptographic Attacks

- What is it
  - Techniques and strategies that adversaries employ to exploit vulnerabilities in cryptographic systems with the intent to compromise the confidentiality, integrity or authenticity of data

- Downgrade Attack
  - Aims to force a system into using a weaker or older cryptographic standard or protocol then what its currently utilizing 
  - Real example demonstrating this kind of attack was the POODLE attack , also known as a the Padding Oracle On Downgraded Legacy Encryption attack which targeted SSL version 3.0
  - These downgrade attacks are dangerous because they turn the very nature of evolving security, such as the development of stronger, more robust cryptographic protocols, against itself
  - Many systems have phased out support for legacy protocols that are known to be insecure, even if it means sacrificing backward compatibility

- Collision Attacks
  - Aims to find two different inputs that produce the same hash output
  - MD5 or Message direct Algorithm 5 was a popular hashing function
  - These collisions undermine the trust and reliability placed on the cryptographic tools, and they can potentially allow malicious actors to impersonate trusted entities, forge digital signatures, or distribute tampered data while appearing genuine
  - This works on the birthday paradox
    
- Quantum Computing 
  - A computer that uses quantum mechanics to generate and manipulate quantum bits (qubits) in order to access enormous processing powers
  - With quantum computing , instead of using ones and zeros, it uses quantum bits or qubits

- Quantum Communication 
  - A communications network that relies on qubits made of photons (light) to send multiple combinations of ones and zeros simultaneously which results in tamper resistant and extremely fast communication
    
- Qubit 
  - A quantum bit composed of electrons or photons that can represent numerous combinations of ones and zeros at the same time through superposition
    
- Post Quantum Cryptography 
  - A new kind of cryptographic algorithm that can be implemented using today’s classical computers but is also impervious to attacks from the future quantum computers
  - Two Primary methods are used-
    - Increasing the key size to increase the number of permutations that are needed to be brute-forced
    - Researchers are working on a wide range of approaches, including lattice-based cryptography and super singular isogeny key exchange
  
  - For general encryption needs, NIST has selected the CRYSTALS-KYBER algorithm
  - For digital Signatures CRYSTALS-Dilithium , FALCOM , SPHNICS+