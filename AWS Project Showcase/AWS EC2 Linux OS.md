### AWS EC2 Linux OS
 
#### Create EC2 Instance using Linux OS <br>
Step 1: Click “EC2” or “EC2 Dashboard”. <br>
 ![image](https://github.com/user-attachments/assets/735d905e-c250-43c5-8d86-d9ca14c463ce)



Step 2: Click “Launch instance”. <br>
 ![image](https://github.com/user-attachments/assets/d268600c-976d-4fb5-a417-b4d13575f145)

Step 3: Choose the Linux Amazon Machine Image (AMI).  <br>
![image](https://github.com/user-attachments/assets/9e5806c1-74b3-43fc-876d-b0e799d9a8c6)

 
Step 4: Generate a new key pair (Optionally give it a custom name).  <br>
![image](https://github.com/user-attachments/assets/5c68be4b-1b0b-4ce8-a5c9-06ef8f36d1f3)

 
Step 5: Network settings: Change allow SSH Traffic from “Anywhere” to “My IP”: <br>
![image](https://github.com/user-attachments/assets/75b0aaaf-6dfb-43f1-8c1c-4c22447adde3)

 
Step 6:  Select Launch Instance: <br>
![image](https://github.com/user-attachments/assets/b81de8d8-ec86-4b31-b28c-e5db9550667d)

 
Step 7: Select Instances: <br>
![image](https://github.com/user-attachments/assets/1a1c4e23-0cf4-4558-a21e-90855720964a)

 
Step 8:  Wait until the check status says “2/2 check passed” (A page reload may be required if the checks are stuck at initializing): <br>
![image](https://github.com/user-attachments/assets/2c287aa5-b7b3-4b21-a48f-1ac735ba157e)

 

Step 9: Right click your instance wait for the drop down menu to appear the click connect: <br>
![image](https://github.com/user-attachments/assets/f64d35cc-3318-406a-9f0b-dde58f647ba9)

 

Step 9 (Optional): If using a touch pad your instance then select “connect” located on the upper right:   <br>
![image](https://github.com/user-attachments/assets/fee3c42d-64ed-4576-bb4f-e15f2e7a3625)


#### Functionality Verification <br>
Step 1: Select SSH client then click on the boxes on the left under the example to copy it: <br>
![image](https://github.com/user-attachments/assets/569db7bf-6d8b-45c0-8e69-292ead6f36e8)

 
Step 2: Open power shell on your computer by typing into the search box: <br>
![image](https://github.com/user-attachments/assets/3207b029-234d-48a1-8cc9-da436ad0b316)

 
Step 2: Type the following command :cd downloads <br>
![image](https://github.com/user-attachments/assets/304a3eb1-2286-4fb6-b970-2c0bcac5a26c)

 
Step 3: Now paste the copied “example” from the AWS console into PowerShell (if it does not paste copy it again then paste in PowerShell): <br>
![image](https://github.com/user-attachments/assets/a678d526-06dd-4e73-9729-5bdb4237fe26)

 
Step 4: Type yes on the following screen: <br>
![image](https://github.com/user-attachments/assets/d28ddfa2-8252-4dd3-bd2a-ab9ec5ed9b84)

 
When successfully the following text will display <br>
![image](https://github.com/user-attachments/assets/c64e9912-bcf0-4f8a-be5e-d5c50b9ca93b)

 
Step 4 (Optionally): Create a simple text file to verify OS functionality: <br>
![image](https://github.com/user-attachments/assets/ea7c32ad-1281-483a-859c-fdc1c8e38d31)

 

