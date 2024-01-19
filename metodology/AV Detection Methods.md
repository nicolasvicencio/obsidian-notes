
Av software will typically utilize signature, heuristic and behavior based detection 

- Signature based detection - An AV signature is a unique sequence of bytes that uniquely identifies malware, As as result , yo will have to ensure that your obfuscated exploit or payload doesn't match any known signature in the AV database.
We can bypass signature-based detection by modifying the malware's byte sequence therefore changing the signature.

- Heuristic-based detection = Relies on rules or decisions to determine whether a binary is malicious, It also looks for specific patterns within the code or program calls.
- Behavior based detection - Relies on identifying malware by monitoring it's behavior. (Used for newer strains of malware)
- On-disk Evasion Techniques
    - Obfuscation - Obfuscation refers to the process of concealing something important valuable or critical. Obfuscation reorganizes code in order to make it harder to analyze or RE.
    - Encoding = Encoding data is a process involving changing data into a new format using a scheme. Encoding is a reversible process data can be encoded to a new format and decoded to its original format
    - Packing - Generate executable with new binary structure with a smaller size and therefore provides the payload with a new signature.
    - Crypters - Encrypts code or payloads and decrypts the encrypted code-in memory. the decryption key/function is usually store in a stub