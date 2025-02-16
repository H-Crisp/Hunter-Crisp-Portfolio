

# Hunter Crisp Programming Portfolio

| **Theme**                       | **Course**                                                  |
|--------------------------------:|:------------------------------------------------------------|
| Software Engineering and Design | CS-330: Computational Graphics and Visualization            |
| Algorithms and Data Structures  | CS-300: Analysis and Design                                 |
| Databases                       | CS-320: Software Testing, Automation, and Quality Assurance |

## Code Enhancements

<details>
<summary> 
#####Software Engineering and Design
</summary>

This artifact comes from CS330: Computational Graphics and Visualization. It is a program using OpenGL coded in C++ that generates a 3D scene entirely out of code. It was created in June 2024. For my project I created a basic desk setup with a screen, Xbox, notepad and pen.

I wanted to include this code in my ePortfolio because it is one of my cleanest and more complex pieces that I could show off. It also fits with the category of engineering and design quite well, showing that I can code in an organized manner that is readable and easy to understand. I improved the artifact by fixing a bug that prevented shaders from rendering in addition to adding user-friendliness by explaining controls and modifying the camera to be more intuitive, allowing full 360 degree rotation instead of slight panning.

I met all the course outcomes I planned to reach for this artifact, making all the enhancements plus a little extra.

The challenges I faced were having to remember how OpenGL works and looking for what is causing issues without any highlighted errors.



Changes and enhancements:

Added explanation of controls in MainCode.cpp
![image](https://github.com/user-attachments/assets/ece2aabc-4580-431f-983a-47272e3bf9dc)

Made a change in ViewManager.cpp so that cursor is locked while the program is running so the user has complete camera freedom:
![image](https://github.com/user-attachments/assets/214e1335-1677-4655-92a1-2607d38f868c)

Fixed an issue where rendered objects were all under one method which is bad practice.
Before: all objects in SceneManager.cpp were in method “RenderScene()”

![image](https://github.com/user-attachments/assets/6acc1328-4b89-4f1f-8e74-45c501a86d40)

After: Each object is nested in its own method
SceneManager.cpp:
![image](https://github.com/user-attachments/assets/7274c3c3-89fb-44f3-910d-2423d8909058)

The trade off here is that each method had to have the transformation variables defined every time.

A new function was added: SetupSceneLights()
This in combination with functions not nested correctly were the reasons for shaders not rendering.

![image](https://github.com/user-attachments/assets/719c0df6-a577-4734-a12d-5beb3c678856)

Methods for each object also must be in SceneManager.h
![image](https://github.com/user-attachments/assets/47a2c9b0-0219-492d-b479-d9fc998526b1)


Scene before shaders:
![image](https://github.com/user-attachments/assets/41c2c701-eb93-4f8c-8154-1fbaaaeec1c8)


Scene after shaders:
![image](https://github.com/user-attachments/assets/e536bb07-a613-4266-ae47-b90e27549596)

As we can see there is a yellow tint to simulate house lighting in addition to shadows.

</details>

<details>
<summary> 
#####Algorithms and Data Structures
</summary>
  
My 2nd code of choice comes from CS300, Analysis and Design. The course went over various vector sorting methods with this particular code using a binary search tree. The idea is to have a text file of data with various courses and having the sorting method read and interpret the course requirements and display them to the user. The code is able to read from multiple text files as well. This code was created in December 2023.

I chose this code because it fits the criteria of algorithms and data structures, using a vector sorting algorithm. It is also easy to understand from an outside perspective. A lot of time was spent optimizing the user experience, creating a sleeker and clean look in the console window with newly added instructions. In addition to this, more comments have been added within the code to better explain how it works. Also, a bug was fixed that caused a file to not be read properly.

The new interface looks as follows:
![image](https://github.com/user-attachments/assets/e616f4f1-9653-40fd-9755-0cc7326c03fa)

The previous design was clunky and difficult to read.

I met all planned course outcomes for this enhancement and even adjusted more than initially planned. When modifying the artifact I learned that multiple files can be loaded at the same time, meaning the program is not limited to just one file. The big challenge I faced was figuring out why the text file would not load and this was due primarily to a naming error causing issues.

</details>

<details>
<summary> 
#####Databases
</summary>

The third program enhancement comes from CS320: Software testing, automation, and quality assurance. This program demonstrates the database portion of the capstone by utilizing JUnit testing for three different class types in a database. JUnit testing runs multiple tests simultaneously through separate classes to add, update, or delete items. Initially the program only featured contacts and contact service and their corresponding testing classes, but the enhancement adds task and appointment classes. The code was also enhanced with comments that demonstrate the flow of the program better.
	
The code can be broken down in three sectors:

The contact and contact service classes take an ID, first and last name, and a phone number of no more than 10 characters, and an address of no more than 30 characters, and the JUnit test classes for both ensure the uniqueness of the ID’s and make sure the character criteria is fulfilled before creating a new contact.

For the additional task, task service, and their two testing classes, task IDs and contact IDs are created again this time with no more than 20 characters and a description of 30 or less characters. A fail test was implemented to make sure each criteria is filled with a corresponding error message for each type of error, including null inputs.

For the added appointment classes, the ID and descriptions follow the same rules as task and task service, with the difference of dates not allowed to be scheduled in the past.

With all these changes I met the planned enhancements accordingly, adding new classes and comments in code. During the process I had to re-learn the usages of JUnit testing which was neat.
</details>
