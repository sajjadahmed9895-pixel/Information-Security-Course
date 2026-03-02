# Schneier 2015 - One-Way Functions

Bruce Schneier explains that one-way functions are a fundamental concept in modern cryptography, especially in public-key systems.
+ A one-way function is easy to compute in one direction but very difficult to reverse. If we know x, it is easy to calculate f(x) but If we only know f(x), it is extremely hard to calculate x.
+ Schneier gives a simple real-world example: Breaking a plate is easy, but putting all the tiny pieces back together perfectly is extremely difficult.
+ There is no strict mathematical proof that true one-way functions exist.
+ One-way functions alone cannot be used directly for encryption (can't decrypt).
+ A trapdoor one-way function is a special type of one-way function. It is easy to compute forward but Hard to reverse.BUT if you have secret information (trapdoor), reversing becomes easy.

# Schneier 2015 - 2.4 One-Way Hash Functions

+ A one-way hash function produces a fixed-length output from a variable-length input.
+ Main purposeof it is to create a digital fingerprint of data.
+ Hash many names: message digest, fingerprint, checksum, MDC, MIC
+ How secure one-way hash functions:
  * Easy to compute hash from input.
  * Hard to reverse hash to original input.
  * Hard to find two different inputs with same hash
+ Hash functions are public and used for Password storage, File verification, Data integrity, Digital signatures.
+ Hashing allows verification without sharing the original file.
+ Message Authentication Code (MAC):
  * Hash function combined with a secret key.
  * Only someone with the key can verify it.
  * Provides both integrity and authentication.

 # Install Hashcat and Test with Sample Hash

 + I installed Hashcat on my server and then tested was it work or not.
<img width="814" height="550" alt="installed" src="https://github.com/user-attachments/assets/f19ff88c-9902-45d7-8efc-40d16d48c6da" />

+ Then I create a new directory and downloaded the RockYou password dictionary, which contains over 14 million passwords.
<img width="820" height="543" alt="Number of password" src="https://github.com/user-attachments/assets/821b3c61-13eb-44cb-8693-82012170784d" />

+ I ran the example-hashes and identified many mood.
+ I used Hashcat in MD5 mode (0) with the hashes.
+ Hashcat performed a dictionary attack by hashing each word and comparing it to the target hash.
+ The result was successfully solved, revealing the original password was summer.
<img width="822" height="545" alt="solved" src="https://github.com/user-attachments/assets/b4539af7-349b-43c1-8552-a8d3c0001591" />




