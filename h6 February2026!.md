# Schneier 2015 - One-Way Functions

Bruce Schneier explains that one-way functions are a fundamental concept in modern cryptography, especially in public-key systems.
+ A one-way function is easy to compute in one direction but very difficult to reverse. If we know x, it is easy to calculate f(x) but If we only know f(x), it is extremely hard to calculate x.
+ Schneier gives a simple real-world example: Breaking a plate is easy, but putting all the tiny pieces back together perfectly is extremely difficult.
+ There is no strict mathematical proof that true one-way functions exist.
+ One-way functions alone cannot be used directly for encryption (can't decrypt).
+ A trapdoor one-way function is a special type of one-way function. It is easy to compute forward but Hard to reverse.BUT if you have secret information (trapdoor), reversing becomes easy.

# Schneier 2015 — 2.4 One-Way Hash Functions

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
