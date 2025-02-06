The python code aes-cbc-crack provides cryptography-related functionalities using AES-EBC encryption. Once you run the code, you can interact with it using the available endpoint requests:

- Encrypt endpoint (/encrypt)
    Purpose:  Encrypts a user-provided hexadecimal string using AES encryption.
    Important: If the string is "CSCI_515", the application will respond with "No cheating!".
    How to use: 
        - You want to encrypt the string "CSCI"
        - First, you get the hexadecimal value of that string '435343495f353135'
        - Then you submit the request: curl http://127.0.0.1:5000/encrypt?user='435343495f353135'

- Flag Retrieval Endpoint (/get_flag)
    Purpose: Allows you to retrieve the secret flag, but only if you can successfully decrypt a specific value.
    If the decrypted value matches "CSCI_515", the server will return the secret flag. Otherwise, it will respond with "Invalid user!"
    How to use:
        - You want to decrypt a value in hexadecimal: 

- Hex Conversion Endpoint (/get_hex)
    Purpose: Converts a user-provided string into its hexadecimal representation.
    How to use: Send any string through the user parameter.
    Example:
        curl http://127.0.0.1:5000/get_flag?user= 

- Download the python code aes-ebc-crack on a Linux machine.
- Allow execution through:
    # chmod +x aes-ebc-crack

