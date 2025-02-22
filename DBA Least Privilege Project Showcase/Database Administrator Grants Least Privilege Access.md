#### Agenda:
Several users in the database will be administered privileges to perform specific tasks. Users will be granted privileges based on roles and responsibilities. 
#### Assumptions:
1.	Users will be granted privileges following a least privilege schema. 
2.	The faculty members are the employees while the students are the customers.

####Privilege Schema:

|TABLE	|USER|	PRIVLEDGE|
| :---        |    :----:   |         :---: |
|STUDENT	|ABLE	|SELECT|
|STUDENT	|BAKER|	SELECT,UPDATE|
|STUDENT	|CHARLES|	SELECT, INSERT|
|STUDENT	|DRAKE	|SELECT, DELETE|
|STUDENT	|ELLIOT	| SELECT, UPDATE ON MAJOR ONLY|
|FACULTY	|MARTIN	| SELECT, UPDATE|
|ACULTY	|SEAVER	| SELECT, INSERT, DELETE|
|FACULTY	|LOONEY	| SELECT, UPDATE ON ADDRESS ONLY|
|FACULTY	|MILLS	| SELECT, UPDATE, INSERT|
STUDENT|	ABLE	|SELECT





#### User: Able
#### Proof of Granted Privileges:
SQL> select * from admin.student;<br>
![image](https://github.com/user-attachments/assets/cba95075-dbc7-4622-bdd2-02b99914a9c7)<br>
 
#### Proof of Denied Privileges:
SQL> select * from admin.faculty;<br>
![image](https://github.com/user-attachments/assets/ea6dd45d-b1ac-44a5-a051-1304385246f1)<br>

SQL> update admin.student set major='haha' where studentid=100;<br>
![image](https://github.com/user-attachments/assets/18ec1821-2f8d-4e8b-b5a9-215746fd82df)<br>

#### User: Baker
#### Proof of Granted Privileges:
SQL> select * from admin.student;<br>
![image](https://github.com/user-attachments/assets/e6a7712a-1ca3-4476-aff3-aef6c20a2ef9)<br>

SQL> update admin.student set major='haha' where studentid=100;<br>
![image](https://github.com/user-attachments/assets/48a0448b-95d9-48d1-81e6-5d486ffd4891)<br>

SELECT * FROM ADMIN.STUDENT;<br>
![image](https://github.com/user-attachments/assets/65af5887-e528-475c-8b03-65d288a288e5)<br>
 
#### Proof of Denied Privileges:
SQL> select * from admin.faculty;<br>
![image](https://github.com/user-attachments/assets/5e314b0c-fce5-4990-ad40-bc0a22bebbd3)<br>

SQL> update admin.faculty set name='haha' where facultyid=0980;<br>
![image](https://github.com/user-attachments/assets/26db72b2-454e-47ac-9cc3-6f79c0c3013c)<br>
 
SQL> DELETE FROM ADMIN.STUDENT WHERE NAME LIKE '%ABL_%';<br>
![image](https://github.com/user-attachments/assets/b1e337fb-9b87-4dde-b89b-f10ef0233935)<br>

#### User: Charles
#### Proof of Granted Privileges:
SQL> select * from admin.student;<br>
![image](https://github.com/user-attachments/assets/4646ea53-e83b-437e-897c-41daa965d19e)<br>

SQL> insert into admin.student (studentid,name,major,status,age,address,gpa) values (050, 'Kevin', 'Reading', 'TM', 45, '1 New York', 2.75);<br>
![image](https://github.com/user-attachments/assets/e59a9fef-3cb6-4f49-9a57-5274458dcafc)<br>

Select * from admin.student;<br>
![image](https://github.com/user-attachments/assets/21125f9c-1658-40b6-a00d-f8755b11f619)<br>

Denied privileges:
SQL> select * from admin.faculty;<br>
![image](https://github.com/user-attachments/assets/4ba39076-0ae3-4588-ab9c-c56c4d08c98e)<br>
![image](https://github.com/user-attachments/assets/a471074f-ae9f-468b-8d74-ffcc76bf7b71)<br>
 
SQL> insert into admin.faculty (facultyid, name, department, address, rank) values(970, 'Brain', 'hb', '45 new york', 'instructor');<br>
![image](https://github.com/user-attachments/assets/9efa92ac-9463-4fe8-9f86-07a4931298ba)<br>

#### User: Drake
#### Proof of Granted Privileges:
select * from admin.student;<br>
![image](https://github.com/user-attachments/assets/410c252d-a2b1-4d81-a273-9db091114661)<br>

SQL> delete from admin.student where age like '%1_%';<br>
![image](https://github.com/user-attachments/assets/621ca0c2-1a0e-40bc-acb1-cd95c0991ec3)<br>

SQL> select * from admin.student;<br>
![image](https://github.com/user-attachments/assets/56de525c-145d-4aa3-aeab-fae36e7f24a2)<br>

#### Proof of Denied Privileges:
SQL> update admin.student set name='ashley' where name ='able';<br>
![image](https://github.com/user-attachments/assets/4dd446f4-cf31-423c-b4a4-de8c495c7b95)<br>

#### User: Elliot
#### Proof of Granted Privileges:
select * from admin.student;<br>
![image](https://github.com/user-attachments/assets/6c2434b3-6ddc-4f54-bcfc-ab34358d2227)<br>

SQL> update admin.student set major = 'ENGLISH' where STUDENTID='200';<br>
 ![image](https://github.com/user-attachments/assets/739ce0f3-31b7-487b-8115-edcd6d3ebf5b)<br>

select * from admin.student;<br>
 ![image](https://github.com/user-attachments/assets/b715f564-23c4-4b0e-bc05-df7ac02a5006)<br>

#### Proof of Denied Privileges:
SQL> update admin.student set address = 'newyork' where address='utah';<br>
![image](https://github.com/user-attachments/assets/219d19a6-24f7-4bb4-accc-5cb23e1dff61)<br>

SQL> select * from admin.faculty;<br>
 ![image](https://github.com/user-attachments/assets/0e7579b4-7b3f-4a34-a4dc-2de79f1bbdfa)<br>

#### User: Martin
#### Proof of Granted Privileges:
select * from admin.faculty;<br>
![image](https://github.com/user-attachments/assets/9f89cc92-6adb-4e96-afd9-e97ced4d402b)<br>

SQL> update admin.faculty set address='44 manhattan' where facultyid='5430';<br>
![image](https://github.com/user-attachments/assets/5ee4652c-ca85-439e-b4d8-e51705b7bb7f)<br>

SQL> select * from admin.faculty;<br>
![image](https://github.com/user-attachments/assets/af1fd2bb-7317-4662-b9f1-f895d5ca8572)<br>
 
#### Proof of Denied Privileges:
SQL> select * from admin.student;<br>
![image](https://github.com/user-attachments/assets/ed9a7e2e-1f50-4b01-a03e-7db9235956e0)<br>

 
SQL> update admin.student set address='44 manhattan' where studentid='100';<br>
![image](https://github.com/user-attachments/assets/c99275ce-907b-43f2-8c11-82efe977023a)<br>

 
#### User: Seaver
#### Proof of Granted Privileges:
SQL> SELECT * FROM ADMIN.FACULTY;<br>
![image](https://github.com/user-attachments/assets/99c6b199-0592-42cc-9c09-e7de4b1b31e0)<br>

 
SQL> INSERT INTO ADMIN.FACULTY VALUES( '768', 'BILL','GH', '345 MD', 'DEAN');<br>
![image](https://github.com/user-attachments/assets/b228b358-e779-4b2f-af33-a6d571e38bc8)<br>
 
SQL> SELECT * FROM ADMIN.FACULTY;<br>
![image](https://github.com/user-attachments/assets/98ab1734-7071-4baa-aa16-6caf05cc1e5a)<br>

 
SQL> DELETE FROM ADMIN.FACULTY WHERE FACULTYID='768';<br>
![image](https://github.com/user-attachments/assets/e16806bc-4ba9-4f36-abde-71624e216f24)<br>

 
Select * from admin.faculty;<br>
![image](https://github.com/user-attachments/assets/4d26f1ca-3132-493b-bbf7-77bfc722be62)<br>

#### Proof of Denied privileges:
SQL> UPDATE ADMIN.FACULTY SET NAME ='STEVE' WHERE NAME = 'LOONEY'; <br>
![image](https://github.com/user-attachments/assets/d9f1ec38-629e-43f0-b008-66aa9780fc19)<br>

#### User: Looney
#### Proof of Granted Privileges:
SQL> SELECT * FROM ADMIN.FACULTY;<br>
![image](https://github.com/user-attachments/assets/29f67372-6ce9-454d-b7c7-dc6ebb56ac1e)<br>

 
UPDATE ADMIN.FACULTY SET ADDRESS= '1 NORTH' WHERE FACULTYID ='980';<br>
![image](https://github.com/user-attachments/assets/8b53c15b-50f3-45b9-b490-c25eb19ee8a4)<br>

 
SQL> SELECT * FROM ADMIN.FACULTY;<br>
![image](https://github.com/user-attachments/assets/985763bb-cff1-4abc-890a-31e829eddfa3)<br>
 
#### Proof of Denied Privileges:
SQL> UPDATE ADMIN.FACULTY SET NAME= 'KING' WHERE FACULTYID ='980';<br>
![image](https://github.com/user-attachments/assets/40bbb232-a5b6-4172-882a-360ccfc19314)<br>

SQL> DELETE FROM ADMIN.FACULTY WHERE FACULTYID='980';<br>
![image](https://github.com/user-attachments/assets/5d26d8db-5d06-49f4-98ea-13d35b5b4362)<br>

SQL> INSERT INTO ADMIN.FACULTY VALUES( '1', 'KING', 'GA', '17 WEST', 'DEAN');<br>
![image](https://github.com/user-attachments/assets/a1669598-cb4a-42be-a32e-cad6ec480e85)<br>

 
#### User: Mills
#### Proof of Granted Privileges:
UPDATE ADMIN.FACULTY SET NAME= 'JEAN' WHERE FACULTYID ='980';<br>
![image](https://github.com/user-attachments/assets/1c0c4d82-a3f6-48ba-bc60-697a93705cd9)<br>

 
SQL> SELECT * FROM ADMIN.FACULTY;<br>
![image](https://github.com/user-attachments/assets/8d99b3bc-e0da-467c-833d-5b8af2f0a891)<br>

 
SQL> INSERT INTO ADMIN.FACULTY VALUES ('678', 'TOM', 'GH', '1 FIRETOWN', 'INSTRUCTOR');<br>
![image](https://github.com/user-attachments/assets/0a4fbd0f-cb8a-4a8b-8d28-e28afa2d8d82)<br>
 
SQL> SELECT * FROM ADMIN.FACULTY;<br>
![image](https://github.com/user-attachments/assets/98f49b6e-bb70-4079-9bda-6619d935abdd)<br>

#### Proof of Denied Privileges:
SQL> DELETE FROM ADMIN.FACULTY WHERE NAME LIKE '%TO_%';<br>
![image](https://github.com/user-attachments/assets/c1603290-192e-4837-ad7c-eb6d37f3b4ce)<br>
 



