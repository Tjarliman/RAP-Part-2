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

