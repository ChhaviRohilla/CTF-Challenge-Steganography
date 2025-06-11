## Process of Making - Steganography 
### Description: 
Steganography is the art of concealing information within another file or object. In this challenge, the flag is hidden across two separate images. Your mission is to uncover the concealed data, piece it together, and reveal the full flag. <br>

Do you have the skills to uncover what's hidden in plain sight? Combine your tools and techniques to solve this puzzle! <br>
Process of making: <br> 

<strong> IMAGE_1:</strong> exiftool + steghide <br>

 ![image](https://github.com/user-attachments/assets/e0eee0f0-fac7-48ed-b9c4-5dc7d3af8e39)

  
We are going to password protect the flag.txt within an image and hide the encrypted key in metadata. <br>
Choose the key: “101hacking” encrypted to Base64 “MTAxaGFja2luZw==”  <br> 

   ![image](https://github.com/user-attachments/assets/387c8e3b-cb01-4d8e-87ab-b5ab5c4a6d18)

Removed extra data: exiftool -all= IMG_CRAC.JPG <br>
Hide the key in meta data: exiftool -Comment="MTAxaGFja2luZw==" IMG_CRAC.JPG <br>

   ![image](https://github.com/user-attachments/assets/5d359d6e-b269-496d-ae4f-0ff8288a981a)

Password protect the flag.txt using steghide  <br>

  ![image](https://github.com/user-attachments/assets/3253d89f-a8de-4e5d-ad6b-3ec631aba0a4)

Reversing the process user will get the part of flag <br>
 
 
 
 
<strong>IMAGE_2:</strong> 7-Zip <br>

  ![image](https://github.com/user-attachments/assets/48b3ffc4-9ed4-40a4-b94d-af3b5be385cb)

We will be hiding the flag.txt zip within an image using 7zip  <br>
Removed extra data: exiftool -all= IMG2.JPG <br>
Add a hint in metadata: exiftool -Comment=" NOT_THAT_DIRECT_try_some_other_ways_too” IMG2.JPG <br>
  ![image](https://github.com/user-attachments/assets/d4a221a9-a50b-40d8-aab6-f8f7886ad834)

Using command we hide flag.txt within image : copy /b IMG2.JPG + flag.zip IMG2.JPG <br>
  ![image](https://github.com/user-attachments/assets/c6b064cc-432c-478d-9324-9ed5b1d316e4)

When user add these flags to get the right flag. <br>
