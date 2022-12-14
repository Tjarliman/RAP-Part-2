# Restful ABAP Programming Model - PART2

Let's continue our learning into this Part 2 of the RAP Concept.
In this lesson, we will create a transactional application using RAP Concept.
Also, we are going to re-use our artifacts which we have created in Part 1.

#Step 1 - Create Behaviour Definition.

Into the same project as we created in Part 1, let's add another object into it which is the Behaviour Definition.
For each of the artifacts we have created in Part 1, remember we have "_I_" (Interface artifact), and also "_C_" (Consumption artifact).
Behaviour defintion must be created againts those artifacts, and we need to create it as one-on-one base with the root entity which is the Header entity.
Meaning, one root entity, one behaviour definition. 

Here we will start to create our code using ABAP language.

#Step 1.1 Create Behaviour Definition (BDEF) -  for Interface artifact.
  - Right click on the Interface artifact of the root entity (Header entity), then click New Behaviour Definition
  - ![image](https://user-images.githubusercontent.com/39553318/190392747-919fb6ed-4963-434b-a461-fdc7d95c23c1.png)
  - Once clicked, the next screen will appear
  - ![image](https://user-images.githubusercontent.com/39553318/190392966-f18c9cfe-d395-4c4c-becd-aeb48c4918eb.png)
  - This time, we chose Unmanaged as Implementation Type.
  - Once completed you should be able to see something like below
  ![image](https://user-images.githubusercontent.com/39553318/191250955-66e9f53f-0745-4d4a-b7b1-c975f23936e7.png)

  - Then edit it, so it will be like below
  
  ![image](https://user-images.githubusercontent.com/39553318/191250683-2f112eec-05da-4b4a-8549-1f9a9e040a96.png)
  
  - Pls. notice that the command "implementation in class" was moved, and now we have 2 of them.
  - Now activate it

#Step 1.2 Create Behaviour Definition (BDEF) -  for Consumption artifact.

  - Right click on the consumption artifact of the root entity, then click New Behaviour Definition
  
  ![image](https://user-images.githubusercontent.com/39553318/190974326-41656dd3-d11d-4764-a888-383972dbe840.png)
  - Follow the wizard, and once completed you should be able to see something like below.
  ![image](https://user-images.githubusercontent.com/39553318/191252010-19903bc3-cc39-46de-b1e3-e4ce973d9a95.png)


#Step 2 - Create Corresponding Class

To create the corresponding class for our BDEF, we can create the class using SE24, or we can also do as below mentioned

#Step 2.1 - BDEF Class for Header Part
  - Notice that in our BDEF there is a yellow icon like below

![image](https://user-images.githubusercontent.com/39553318/190970734-0b9a1801-0418-40b2-8732-f1dac3ff594f.png)
  - Click on it, then a pop up will appear

![image](https://user-images.githubusercontent.com/39553318/190971309-c420217d-6a3d-4585-a3b8-512fdb24479f.png)
  - Then double click on it, another wizard to create a class should be appearing.
  ![image](https://user-images.githubusercontent.com/39553318/190971511-07a6e68c-1838-43b8-bd4e-bd0be4ca0be7.png)
  - then follow the instruction on the wizard
  - Once completed, you should be able to see this screen below, (make sure you are in the Local Type "TAB")
  - ![image](https://user-images.githubusercontent.com/39553318/191252924-1b37aaab-a163-4e01-aa4a-54af1248b7e3.png)

#Step 2.2 BDEF Class for Detail Part
  - Do the same thing to create the corresponding item class.
  - Follow the wizard, once completed you should be able to see something like below
  - ![image](https://user-images.githubusercontent.com/39553318/191253476-1dfcb4fb-7128-43bb-955f-1c33264199b0.png)

Dont forget to activate all the artifacts you have been created. Once completed your class objects can be shown in this folder
![image](https://user-images.githubusercontent.com/39553318/191138431-6bc19c6e-162c-4e55-897d-7bd2a8fe3c57.png)

#Step 2.3 Preview the OData Service
  - If everything are OK, you can open your previous OData Service in the Service Binding folder
  - ![image](https://user-images.githubusercontent.com/39553318/191143066-be86247d-07c1-45f9-bb75-8005a475626b.png)
  - ![image](https://user-images.githubusercontent.com/39553318/191143131-6a16bc13-1b88-4969-bd24-35397d8a90c5.png)
  - Click the Preview button, then your service will be displayed in a web browser. If requested, you need to Enter your user id and pwd to access the backend server
  - ![image](https://user-images.githubusercontent.com/39553318/191253928-f6d9e51e-a7df-45e9-971d-a03731633c56.png)
  - Notice that the Create and Delete button are there
  - When you click one of the item, you will be navigated to this screen below, and notice that you have Edit and Delete button
  - ![image](https://user-images.githubusercontent.com/39553318/191254241-ca3f4c59-f65c-4401-80c0-6b2e6e2b20d0.png)
  - when you click one of the item, you will also nagivated to another screen where Edit and Delete are now appearing
  - ![image](https://user-images.githubusercontent.com/39553318/191254461-bd6be9a1-5b1a-4c1c-aa8d-3bde17a4b68a.png)

 Notice that, those button are not really yet functioning properly, due to, in an "unmanaged" implementation type, all the CRUD logic must be typed/build from the scratch. THis is not the case when we use the "managed" implementation type. But that's for you to go deeper into this and more to see what I mean.

#Step 3 Change standard's code.

Now let's change those generated codes in each of the artifacts with our custom code by doing copy and paste.

#Step 3.1 Update the "I" Behaviour Definition
- Open the Znn_I_FIDOC_U BDEF, then copy and paste the code from ZTJ_I_FIDOC_U_bdef.txt
- Remember to change the entity names, to your entities name. See below in yellow
- ![image](https://user-images.githubusercontent.com/39553318/191257546-4d9b335c-068c-406a-9245-6d03c6df8653.png)

- ![image](https://user-images.githubusercontent.com/39553318/191258311-86454e65-e10d-49f8-9eb1-c068c16924f9.png)

- once completed you should be able to something like below, with your own entity name on it
- ![image](https://user-images.githubusercontent.com/39553318/191258008-080f68ba-6a4b-4969-b57a-aa099857ce76.png)

#Step 3.2 Update the "C" Behaviour Definition
- Open the Znn_C_FIDOC_U BDEF, then copy and paste the code from ZTJ_C_FIDOC_U_bdef.txt
- Remember to change the entity names, to your entities name. See below in yellow, those are the new entity name
- ![image](https://user-images.githubusercontent.com/39553318/191259509-9a18e4c4-a16f-45f2-b55b-6057b556e82e.png)
- Activate both BDEFs.

#Step 3.3 Update the Header BDEF class, Zbp_nnn_I_FIDOC_U.
- Open the class, and copy and paste the code in ZBP_TJ_I_FIDOC_U.txt into it.
- Dont forget to check if there are any lines with error, try to solve that error, if required change the entity name to your own name.
- also to change the entity name in these parts into your own object' name.
![image](https://user-images.githubusercontent.com/39553318/191634182-08b7fd58-9849-4db9-a6b8-0c9026abbb6e.png)

- Active it

#Step 3.4 Update the Item BDEF Class, Zbp_nnn_I_FIDOCI_U
- Open the class, and copy and paste the code in ZBP_TJ_I_FIDOCI_U.txt into it.
- Dont forget to check if there are any lines with error, try to solve that error, if required change the entity name to your own name.
- Active it

If everything OK, we can try to Preview our OData service, and you will notice some differences with previous one. Can you spot the differences?

1. Delete Button for header part was removed
2. For those documents which having "Posted" as their status, we cannot add anymore items into it.
3. ...etc

#Step 3.5 Adding annotation to show the Post and Simulate button.

Since we have implemented our custom code in our BDEF class. All we have to do is to add annotation into our "C" metadata extension.

- Open the MDE of Znn_C_FIDOC_U
- Find this part of code
- ![image](https://user-images.githubusercontent.com/39553318/191264234-8802c37c-fd5c-4a4a-9545-28113124eae5.png)

- add this lines of codes
{ type: #FOR_ACTION, dataAction:'simulate', label: 'Simulate' },
{ type: #FOR_ACTION, dataAction:'post', label: 'Post' },
{ type: #FOR_ACTION, dataAction:'update', label: 'Edit' }

- Pls. be notice the comma signs, they should be in the correct position.
- Thens you should be able to see something like below
- ![image](https://user-images.githubusercontent.com/39553318/191264610-5b1ff441-2e04-460e-90a1-bd7b0ae76bb6.png)
 
- Once completed, pls. activate it.

Now you should be able to preview you service again, and see the new look / differences.
![image](https://user-images.githubusercontent.com/39553318/191265340-a3f59b0b-1430-4422-a309-3f5619cac490.png)

GOOD LUCK !!!
