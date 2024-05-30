# Building-with-Amazon-DocumentDB-Databases

## AWS services used In this lab
1. Amazon API Gateway
2. AWS Lambda
3. AWS Secrets Manager

## Step by step Instructions

1. On the AWS Console, I first started by navigating to EC2

<img width="726" alt="Step 1" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/a6b29240-dece-450c-9b4d-453a28701180">

2. I then selected Instances on the left hand side and under the instances section, I selected CommandHost followed by connect (Step not shown)

<img width="726" alt="Step 2" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/0c3ce542-d948-4292-8708-53e3cc104d6b">


3.  Select Session Manager followed by connect

<img width="726" alt="Step 3" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/5763baf9-2d98-4cbd-a9db-b339f580eeb4">


4. In the terminal, I ran the first command: cd ~ ,  Nothing should appear which I then entered the following command pictured below:

<img width="726" alt="Step 4" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/c77acfe6-b0bc-4df0-b5ac-8f6a99c7124e">


5. I followed up with another command to help run the docdbpush.py Python script:

<img width="726" alt="Step 5" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/33d43a06-2211-40d0-8b3a-a43b1f8fd2e3">

6. Once that was completed, I needed to connect to the Amazon DocumentDB database in which I did by using the following command:

<img width="726" alt="Step 6" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/9545d46a-2d01-4382-8e67-76c89cfa3ab5">


7. I needed to view the existing databases, I did so by running the command below:

<img width="726" alt="Step 7" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/4428bd78-3e25-4d14-8ea1-dcc1e899d71d">

8. I now needed to instruct the system to use the cast database and show a list of the existing collections running the new command:

<img width="726" alt="Step 8" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/7824629c-7f60-4776-a226-ace7d62e2a60">

9. I ran the following command to view the first document in the 1990 cast collection:

<img width="726" alt="Step 9" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/a873f95e-68b0-4430-831b-d90016a4ca9d">



10. I ran the following command to count the number of documents in the 1990 cast collection that went by the name Sylvester Stallone:

<img width="726" alt="Step 10" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/a3dedb3c-c2d6-4a63-9ea9-76cc44ef3397">


11. In the lab, I was challenged to write a query which counted the number of movies that actor Matt Damon was in between 1990 and 2005 in which I did by writing the following command:

<img width="726" alt="Step 11" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/4295fc09-e0b5-48c9-9810-d28e8b18d801">

12. Once I completed the above task, I existed the database connection and returned to the CommandHost terminal by using the command "exit."

13. I went back to the AWS Console, typed and chose the Lambda service and I chose the function named DocumentDBLambdaExample


<img width="726" alt="Step 12" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/5c4238a1-b59d-476f-9b60-dc8c67a70d14">

15. I chose the function named DocumentDBLambdaExample, scrolled down to the code source and reviewed the code.

16. I went back into the AWS console, searched and chose API Gateway. I then selected the link named DocDBAPIGW

<img width="726" alt="Step 13" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/8809ac5e-356d-4936-b6ce-8ec8fff0c3e7">


18. In the methods section, I chose the POST method type

<img width="726" alt="Step 14" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/f8edf6a9-2be9-42ff-8686-361ed5bf9ea7">

19. Select the test tab

<img width="726" alt="Step 15" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/fb040b3f-bcfc-4c9a-9c34-f81af925cc43">

20. I entered the following JSON payload in the request body (Shown below) followed by test:

<img width="726" alt="Step 16" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/6d214d2d-749e-4eaa-afc4-fcbdf308069c">


21. Once the test is complete, I had the following results shown below:       

    <img width="726" alt="Step 17" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/81193a72-82ba-47ee-9a9c-44d0bd902a96">

22. I went back to the AWS Console and searched and chose Amazon DocumentDB


23. I selected clusters on the left hand side, chose the name of the cluster on the list and selected the configuration tab and copied the cluster identifier which I put in a text editor for a later step.

<img width="726" alt="Step 23" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/1c614bbb-f829-4f85-8acb-8fa2ad566371">


24. I went back to the AWS Console and chose the Amazon DocumentDB service

<img width="726" alt="Step 18" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/77e557c5-203a-4b59-a052-6b8f74ee95ec">


25. I chose clusters on the left hand side and checked the status of the "mydocdb" cluster to ensure it's status was available

<img width="726" alt="Step 19" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/2826c3c0-e4f2-40f0-91e8-dd531f7ff710">

26. I chose the name of the cluster, went to the configuration tab

<img width="726" alt="Step 20" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/921d452d-6ede-4b63-90bc-94d158f5cc6d">

27. I copied the cluster identifier into a text editor in which I will use for a later step

<img width="726" alt="Step 21" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/14b04ec0-28d0-4f4e-84f8-a5bd68473855">

28. I then chose the monitoring tab and scrolled down to the CloudWatch section to review.


<img width="726" alt="Step 22" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/4e2f736f-071d-4623-9661-631b386565c1">

27. I went back to the browser tab of the CommandHost terminal and entered the following command:

<img width="726" alt="Step 24" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/58d6a963-bfcb-47b0-8fe6-81945abb7eba">

28. I then entered the following command into the terminal:   
  
<img width="726" alt="Step 25" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/b72c2a9c-3784-4e02-8821-574e59749faa">

29. To finish the lab, I had to create a manual cluster snapshot so I went back into the AWS Console and went into the Amazon DocumentDB service and selected clusters on the left

<img width="726" alt="Step 26" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/ca504bb8-7214-4598-a617-ac3c3cffa639">

30. I selected the mydocdb cluster, selected the drop down arrow under actions, and selected take snapsnot

<img width="726" alt="Step 27" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/e754770a-876b-4f83-bac7-0c408c6def7a">

31. I gave the snapshot identifier a name of castbackup followed by create at the bottom of the page.


32. Once your snapshot has been created, wait for the status to change to available.


<img width="726" alt="Step 29" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/f8ae967b-82d8-4e7f-9e40-44b61fdb6f7f">


33. To connect to the database mongo shell, I ran the following command:

    <img width="726" alt="Step 30" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/f0d1cd17-b0fe-4091-88cc-348a490db7d7">


33. To create a new collection named test, I ran the following command:




34. I had to query the test collection by running the following command:

<img width="726" alt="Step 32" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/f78c8eda-857b-4a2f-8a64-fc49380d6156">

35. To ensure the failover was working properly, I headed back to the AWS Console, into Amazon DocumentDB service, selected clusters on the left hand side, chose the "primary instance" and selected delete.

<img width="726" alt="Step 33" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/883d0b94-74ba-4553-bf1d-c9c23ad8778d">

36. The system asked to type delete me to confirm I was deleting the instance


<img width="726" alt="Step 34" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/f75f3f6f-9d98-4109-8d0c-b62f652ff836">


37. To confirm it is working, your Instance B will now become the Primary Instance as shown below:

<img width="726" alt="Step 35" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/3d4e1f17-2cbf-4e4e-9394-dc3aa56ec149">

38. To verify the failover operation, I used a mongo shell to add a new document in the test collection. It should allow me to add a new document even though the primary Instance has been deleted because the DocumentDB service should automatically promote the replica Instance and update all the connection information. I used the following command to verify:

<img width="726" alt="Step 36" src="https://github.com/Xalmonte/Building-with-Amazon-DocumentDB-Databases/assets/169603464/5199e82d-07e5-4a4a-8e6e-25939e413543">


This now concludes the lab!
