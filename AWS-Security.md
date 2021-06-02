**Encryption**

    Encryption in flight (SSL)
        . Data is encrypted before sending and decrypted after receving
        . SSL certificate helps with Encryption (HTTPS)

    Server Side Encryption
        . Data is encrypted after being received by the server
        . Data is decrypted before being sent
        . Keys managed in AWS-KMS

    Client Side Encryption
        . Data is encrypted and decrypted in CLient Side
        . Server should not be able to decrypt the data

**KMS - Customer Master Key (CMK Types)**

    Symmetric (AES-256)
        . First offering of AWS, single encryption key is user for both encrypt a
          and decrypt data
        . Never get access to the key unencrypted

    Asymmetric (RSA & ECC Key pairs)
        . Public Encrypt key and Private Decrypt key

    * KMS can only encrypt data 4KB per call, use envelop encryption for data
      more than 4KB (GenerateDataKey API)
    * KMS keys are bounded to Region

**SSM Parameter**

    * Secure Storage for Config and Secrets
    * Types
        1) Standard
            . 10,000 Parametres
            . 4 KB
        2) Advanced
            . 100,000 Parameters
            . 8 KB
    * KMS encryption is optional

**Secrets Manager**

    * Newer Service to store secrets
    * Rotation Policy, Tightly integarted with RDS
    * KMS encryption is mandatory

**Cloud Watch Log Encryption**

    Associate or Create 