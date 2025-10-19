
*Recall:
- A challenge of using symmetric encryption is sharing the key


**Key-Exchange**
---------------------------
**Scenario**: 
- Alice and Bob want to talk securely through a symmetric cryptography only for the key exchange
- Alice and Bob generate secrets independently (A, B) as well has some public material (C)
**Assume:**
- Whenever secrets are combined, they cannot separate
- The order in which they are combined doesn't matter
**Now:**
- Alice and Bob combine their secrets with the common material (AC and BC)
- They exchange and combine the received part with their secret to create **2 identical keys** (**ABC**)

![[Pasted image 20250701204204.png]]
