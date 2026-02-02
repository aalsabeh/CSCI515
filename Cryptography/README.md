# Description of crack-aes-ebc blackbox code:
The python code crack-aes-ebc provides cryptography-related functionalities using AES-EBC encryption. Once you run the code, you can interact with it using the available endpoint requests:

- Encrypt endpoint (/encrypt)
    Purpose:  Encrypts a user-provided hexadecimal string using AES encryption.
    Important: If the string is "CSCI515_IS_COOL", the application will respond with "No cheating!".
    How to use: 
        - You want to encrypt the string "CSCI"
        - First, you get the hexadecimal value of that string '435343495f353135'
        - Then you submit the request: curl http://127.0.0.1:5000/encrypt?user='435343495f353135'

- Flag Retrieval Endpoint (/get_flag)
    Purpose: Allows you to retrieve the secret flag, but only if you can successfully decrypt a specific value.
    If the decrypted value matches "CSCI515_IS_COOL", the server will return the secret flag. Otherwise, it will respond with "Invalid user!"
    How to use:
        - You want to decrypt a value in hexadecimal: 

- Hex Conversion Endpoint (/get_hex)
    Purpose: Converts a user-provided string into its hexadecimal representation.
    How to use: Send any string through the user parameter.
    Example:
        curl http://127.0.0.1:5000/get_flag?user= 

- Download the python code crack-aes-ebc on a Linux machine.
- Allow execution through:
    chmod +x crack-aes-ebc

# Steps to Proceed with the Assignment:
- Watch the video Chapter2-2.mp4 on Blackboard under Week 3 starting minute 40. There are two capture the flag cryptography concepts in the video. The second one is similar to the assignment.
- Watch the video under the assignment to know how better understand the assignment.
- How to proceed?
- You will need to download the python code crack-aes-ebc on a Linux machine. If you have a local Linux machine, then that would be great. Otherwise, you will use the a Linux virtual machine on the cloud (using NetLab system).
- Steps to access the Linux virtual machine on NetLab are included in the Assignment on Blackboard.

 # What to submit?
 - A PDF report that documents with screenshots that:
 - Show that you downloaded the github repository locally (on a local VM or on NetLab)
 - Steps that you were following to get the block size of the encryption module
 - Steps that you were following to return the flag (input your were submitting to the blackbox code, returned value, explanation, etc.)
 - The final flag you got
 
# FAQs
- Q: I am getting "Something went wrong! when I use the encrypt function:
- A: Make sure you are providing the hexadecimal value of a string. Use the get_hex function prior. For instance: to encrypt CSCI515, get the hexadecimal value of it using
    - curl http://127.0.0.1:5000/get_hex?user='CSCI515'
    - Output is: 435343493531355f49535f434f4f4c
    - Then, use the encrypt function:
    - curl http://127.0.0.1:5000/encrypt?user="435343493531355f49535f434f4f4c"

- Q: I am getting "Something went wrong! when I use the get_flag function:
    - Make sure you are submitting a correct encrypted version of a text (e.g., must be a multiple of block size) 
