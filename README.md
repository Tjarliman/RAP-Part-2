# RAP-Part-2
Restful ABAP Programming - Part 2

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
  - You can copy and paste the code in the file ZTJ_I__FIDOC_U_bdef.txt into your new artifact
  - Dont forget to change the entity name to follow your entity name space, ZTJ_xxx into Znn_xxx, nn is your unique ID.
  - Once completed, save it, but dont activate it yet, since we need to create the corresponding ABAP class object. 
  - Actually for this time, we can just activate it, it is OK even though the class object still not yet created.

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
  - Once completed, you should be able to see this screen below, where you can copy and paste the code in ZTJ_BP_FIDOC_U.txt file into this screen. (make sure you are in the Local Type "TAB")
  - ![image](https://user-images.githubusercontent.com/39553318/190972145-b74ff3f7-b464-4453-95f8-aed47efc3927.png)
  - ![image](https://user-images.githubusercontent.com/39553318/190973007-b86875c6-9efe-494a-8319-5b48b6885fbe.png)

#Step 2.2 BDEF Class for Detail Part
  - Do the same thing for the corresponding item class.
  - You can copy the codes from ZTJ_BP_FIDOCI_U.txt for this Detail Part class. (remember to make sure that you are in the Local Type "TAB")
  - ![image](https://user-images.githubusercontent.com/39553318/190973031-ab280991-8695-4846-979c-6a1fcf5c1706.png)

 
