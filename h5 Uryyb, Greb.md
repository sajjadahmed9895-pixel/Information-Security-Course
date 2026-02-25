# Schneier (2015) Applied Cryptography

The basic concepts of cryptography by explaining how secure communication works between two parties. The main idea is that a sender wants to send information securely to a receiver so that unauthorized people cannot read or understand the message. Cryptography is the tools and methods that protect this communication. So the main goal of cryptography is to ensure that even if someone intercepts the message, they cannot understand it without proper authorization.

## Encryption and Decryption terms

+ Plaintext: The original readable message before any protection is applied.
+ Encryption: The process of converting plaintext into a secret form to hide its meaning.
+ Ciphertext: The encrypted message that appears unreadable to anyone without the correct key.
+ Decryption: The process of converting ciphertext back into readable plaintext.

So encryption protects the message during transmission, while decryption allows the receiver to recover the original content.

# Karvinen (2023): PGP

This article explains how to use PGP encryption with the GNU Privacy Guard (gpg) tool to send secure messages over an untrusted network such as the Internet.

+ First, I generated a PGP keypair using gpg --gen-key. The keypair consists of a public key and a private key. The public key can be shared with others, while the private key must remain secret. I verified the key creation using gpg --fingerprint.
<img width="829" height="550" alt="1" src="https://github.com/user-attachments/assets/4ead5ce4-48c8-48cc-8c21-4ff4bf21c453" />

+ Then I exported my public key using ASCII armor format so it can be easily shared through email or text.
<img width="737" height="507" alt="2" src="https://github.com/user-attachments/assets/d90fb8cf-934c-4ea7-b7d1-63189aab6e93" />

+ To simulate communication between two users, I created a separate directory representing another user (Alice). Using "gpg --homedir . --gen-key" stored keys separately.
<img width="813" height="540" alt="3" src="https://github.com/user-attachments/assets/f3324fcc-0025-482e-934b-242368a63785" />

+ Then imported my public key into alive to allow encryption toward me.
<img width="813" height="540" alt="4" src="https://github.com/user-attachments/assets/4f260978-cce7-416f-bd72-774f2a61d845" />

+ I wrote a message and encrypted using the recipient’s public key and signed using Alice’s private key.
<img width="816" height="548" alt="5" src="https://github.com/user-attachments/assets/158768e8-288e-45f4-a9c2-c697aab318b9" />

+ Here I decrypted the message using my private key. "gpg --decrypt encrypted.pgp" also verified Alice’s signature using her public key that confirming the message had not been modified.
<img width="825" height="550" alt="6" src="https://github.com/user-attachments/assets/09b0885a-0ee3-48b4-a291-5d1c21153556" />

# Install OpenSSH server and connect using ssh client

+ I installed the OpenSSH server using (sudo apt install openssh-server) apt package manager. SSH allows secure remote access to a system using encrypted communication.
+ Then I started the SSH service using "sudo systemctl start ssh". Afterwards i checked whether the server was running or not using "sudo systemctl status ssh" command.
<img width="825" height="550" alt="ssh running" src="https://github.com/user-attachments/assets/f962836b-9665-43c4-805a-b36b5c23c3d1" />

+ I connected to localhost using the ssh client, which simulates connecting to a remote machine securely.
<img width="818" height="550" alt="ssh client" src="https://github.com/user-attachments/assets/0d6f1a95-f49a-4b29-9456-5c2f1af66bc5" />

# Automate SSH connection using public keys

+ I generated an SSH keypair using ssh-keygen.
<img width="829" height="510" alt="saved" src="https://github.com/user-attachments/assets/e671b286-497a-428d-bebe-65148606acd1" />

+ Then I copied the public key to the server using ssh-copy-id sajjada@localhost. After this, I could connect using SSH without entering a password.
<img width="824" height="548" alt="automate" src="https://github.com/user-attachments/assets/b803f608-3551-4fc1-a6d8-c497064e10fc" />

# Password Manager open and cloudless

+ I installed KeePassXC, free, open-source, that works completely offline without cloud storage. The application stores passwords locally in an encrypted database file protected by a master password.
+ I created a new master password and saved the encrypted database file "Passwords.kdbx". This master password is required to unlock all stored credentials.
<img width="814" height="800" alt="open" src="https://github.com/user-attachments/assets/56a94e4d-a62f-48af-baa6-de8a4052cfff" />

+ Then I added a sample account entry with a generated strong password to demonstrate usage. So basically, KeePassXC allows a secure storage, password generation, and controlled copying of credentials.
<img width="817" height="800" alt="new pass" src="https://github.com/user-attachments/assets/eb91411a-9545-4717-a1a4-b8928eeeca10" />

+ If I right-click on the entry and then copy password, it copies to clipboard so it auto clears after few seconds.
<img width="822" height="635" alt="Problem" src="https://github.com/user-attachments/assets/492995ee-e937-40ed-bb7d-5008d8e2c6a4" />

This shows how password manager safely stores and retrieves passwords.

## Password managers are important because they:

+ Generate strong random passwords.
+ Protect against any kind of attacks.
+ Reduce risk of phishing.
+ Prevent password reuse across other services.
+ Eliminate need to remember multiple weak passwords.

# Presentation material

I have already submitted presentation materials

# References

+ https://oit.utk.edu/security/learning-library/article-archive/password-managers/#:~:text=A%20password%20manager%20ensures%20each,Strong%20passwords%20protect%20your%20identity.


