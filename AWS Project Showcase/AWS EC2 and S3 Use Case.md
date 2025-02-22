### AWS EC2 and S3 Use Case  <br>
#### Agenda:<br>
Use the AWS EC2 and S3 features to facilitate data migration in a production environment between the business, data engineer and data analyst.<br>

Assumptions:
1.	The Data Engineer will access the bucket using the Linux OS instance. <br>
2.	The Data Analyst will access the bucket using the Windows OS instance. <br>
3.	Direct bucket access will be used to facilitate the data that is already present on behalf of the business via “host computer”.<br>
4.	The host computer will also be used to verify functionality for the Data Analyst since both use the same operating system. <br>


 
Step 1: Ensure all instances are running<br>
 
![image](https://github.com/user-attachments/assets/25775be1-ccca-49aa-813c-00de63c6f570)

Step 2: Connect to Linux Instance: <br>
![image](https://github.com/user-attachments/assets/0f056484-c35c-4075-8d56-0b8b2972fa0c)

Step 3: Connect to your Windows Instance:<br>
![image](https://github.com/user-attachments/assets/7b5ee5d8-2edf-4f90-9922-681d91276b6a)


Step 4: Verify creation of S3 Bucket<br>
 ![image](https://github.com/user-attachments/assets/768ac8da-3b53-47bc-b3fe-a47648d7417b)


Step 5a: Verify data file on host computer:<br>
![image](https://github.com/user-attachments/assets/84f7dc07-dc76-43c6-ba28-a61573d24824)

Step 5b: Upload data file on S3 bucket from host computer:<br>
 ![image](https://github.com/user-attachments/assets/9a9f6416-efa2-4d7d-8a32-01a2ee8b1c13)

Step 5c: Successful upload to S3 bucket:<br>
 ![image](https://github.com/user-attachments/assets/5388e665-d32a-4c3e-909e-a08c3303b594)


Step 6: Successful download from S3 bucket to host computer:<br>
 ![image](https://github.com/user-attachments/assets/d249495b-75f2-416a-85ca-d83b5fee4af3)

Step 7: Successful data file upload to instance:<br>
 ![image](https://github.com/user-attachments/assets/bae5b3ba-aacf-4e86-b313-37304d85385c)


Step 8: Successful download from instance to S3 bucket (file renamed to shows data file difference):<br>
 
![image](https://github.com/user-attachments/assets/3b7c594f-631a-41c0-9bfc-b2981ed755b8)


