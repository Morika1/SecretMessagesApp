# Secret Messages Application

![chat1](https://github.com/Morika1/SecretMessagesApp/assets/68543807/d1a0f160-484a-4d1f-920c-1ce844f84594)
![encode1](https://github.com/Morika1/SecretMessagesApp/assets/68543807/a387ea1e-ea67-480f-a4d8-9726f7c7f42e)
![permission](https://github.com/Morika1/SecretMessagesApp/assets/68543807/7876eb47-5fa1-424c-bc82-eec69fcdaa7a)  ![encode2](https://github.com/Morika1/SecretMessagesApp/assets/68543807/fb371484-fc41-46f2-ac1e-8a5d94570f1e)
![chat2](https://github.com/Morika1/SecretMessagesApp/assets/68543807/ce234131-8fac-48be-9216-3eaa5360923d)
![chat3](https://github.com/Morika1/SecretMessagesApp/assets/68543807/eb49f57b-bf13-4143-90a1-b1d2f7713a43)  ![dialogbox](https://github.com/Morika1/SecretMessagesApp/assets/68543807/db4571de-e8cc-4b01-98a2-f9a5c3bc0f86)

This application is intended to provide a secret messages chat service that allow users to encode their messages in an image. 
Each image can be decoded with its secret key.

** Note: This application can be extended to use real-time database and allow users to chat with each other. 

# Description

When the application is first openning, a chat screen appears. 
At top of the chat there is an 'Encode' button. 

Clicking the 'Encode' button will open an encoding screen that asks for an image to encode to, a message to encrypt and a secret key.
- Once the empty image in being clicked, the application requests permission to access gallery on device's storage.
- As soon as permission is granted, the gallery will open to allow image selection.
  
At the end of each encryption, the chat screen will appear with list of existing encrypted messages. 
Each image can be clicked in order to decode the secret message from the image:

At the bottom of chat screen there is a text field to enter the secret key of the selected image.
The 'Decode' button next to it will be enabled as soon as image will be selected from chat and a matching secret key will be entered.
- Wrong key: user will be notified key is wrong
- Correct key: the decrypted message will pop on the screen.
- Accepting the message will remove it from the chat. 

# Security

This application combines 2-level data encryption to ensure high security.
First the message is being encrypted using 'AES' encryption with password (secret key).
Next, the encrypted message is being encoded to the selected image using Steganographic (Hiding data in image pixels LSBs).

Finally, accepting the decrypted message will remove the image from the chat, so the data in the chat is not being stored. 
