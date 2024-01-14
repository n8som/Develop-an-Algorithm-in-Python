# Develop-an-Algorithm-in-Python

<h2>Introduction</h2>

An algorithm is a set of steps that can be used to solve a problem. Security analysts develop algorithms to provide the solutions that they need for their work. For example, an analyst may work with users who bring them devices. The analyst may need an algorithm that first checks if a user is approved to access the system and then checks if the device that they have brought is the one assigned to them.

In this lab, I'll develop an algorithm in Python that automates this process.

<h2>Scenario</h2>

In this lab, I'm working as a security analyst and I'm responsible for developing an algorithm that connects users to their assigned devices. I'll write code that indicates if a user is approved on the system and has brought their assigned device to the security team.

<h2>Task 1</h2>

I'll work with a list of approved usernames along with a list of the approved devices assigned to these users. The elements of the two lists are synchronized. In other words, the user at index 0 in approved_users uses the device at index 0 in approved_devices. Later, this will allow me to verify if the username and device ID entered by a user corresponds to each other.

First, to explore how indices in lists work, run the following code cell as is and observe the output. Then, replace each 0 with another index and run the cell to observe what happens.

![image](https://github.com/n8som/Develop-an-Algorithm-in-Python/assets/110139109/3de4713a-aee0-4456-8447-52739da2f565)

![image](https://github.com/n8som/Develop-an-Algorithm-in-Python/assets/110139109/0418fc28-4b2a-4e0a-bbe7-c0a7eb8d1e31)

When approved_users[0] is displayed, the output is the first approved username from approved_users. When approved_devices[0] is displayed, the output is the first device ID from approved_devices. When you replace each 0 with another index, the output is the element at that index in approved_users, followed by the element at that index in approved_devices. For example, if you replace each 0 with 3, the output is the element at index 3 in approved_users, followed by the element at index 3 in approved_devices.

<h2>Task 2</h2>

A new employee is joining the organization, and they need to be provided with a username and device ID. In the following code cell, I am given a username and device ID of this new user, stored in the variables new_user and new_device, respectively. Use the .append() method to add these variables to the approved_users and approved_devices respectively. Afterward, display the approved_users and approved_devices variables to confirm the added information.

![image](https://github.com/n8som/Develop-an-Algorithm-in-Python/assets/110139109/ceeab19a-6f19-4d94-b3de-a8dfa795fe94)

After the new approved user is added, their username is at the end of the approved_users and their device ID is at the end of the approved_devices.

<h2>Task 3</h2>

An employee has left the team and should no longer have access to the system. In the following code cell, I am given the username and device ID of the user to be removed, stored in the variables removed_user and removed_device respectively. Use the .remove() method to remove each of these elements from the corresponding list. Afterward, display both the approved_users and the approved_devices variables to view the removed users. Run the code and observe the results.

![image](https://github.com/n8som/Develop-an-Algorithm-in-Python/assets/110139109/4386a9df-10c4-4c2c-8cde-da2667cae9db)

After the user who left the team is removed, their username is no longer part of the approved_users and their device ID is no longer part of the approved_devices.

<h2>Task 4</h2>

As part of verifying a user's identity in the system, I'll need to check if the user is one of the approved users. Write a conditional statement that verifies if a given username is an element of the list of approved usernames. If it is, display "The user ______ is approved to access the system.". Otherwise, display "The user ______ is not approved to access the system.". 

![image](https://github.com/n8som/Develop-an-Algorithm-in-Python/assets/110139109/b2e06172-73be-44cc-a47e-b54f8239a41e)

<h2>Task 5</h2>

The next part of the algorithm uses the .index() method to find the index of username in the approved_users and store that index in a variable named ind.

When used on a list, the .index() method will return the position of the given value in the list.

Add a statement to display ind in the following code cell to explore the value it contains.

![image](https://github.com/n8som/Develop-an-Algorithm-in-Python/assets/110139109/239eef71-10a0-4743-a3b7-57df5cc3f7c6)

When username is "sgilmore", the output is 2, which indicates that the index value of "sgilmore" is 2 in the approved_users. In other words, "sgilmore" is the third element in the approved_users. Remember, indexing in Python starts at 0.

<h2>Task 6</h2>

This task will allow me to build my understanding of list operations for the algorithm that I'll eventually build. It will demonstrate how I can find an index in one list and then use this index to display connected information in another list. First, use the .index() method again to find the index of username in the approved_users and store that in a variable named ind. Then, connect ind to the approved_devices and display the device ID located at the index ind. Afterward, run the cell to observe the result.

![image](https://github.com/n8som/Develop-an-Algorithm-in-Python/assets/110139109/27eb47ea-21f8-42e0-b7af-5d18bdafd89f)

When username is "sgilmore", the output is 4n482ts, which is the device ID that corresponds to "sgilmore". The third approved username in the approved_users is "sgilmore", and similarly the third device ID in the approved_devices is "4n482ts".

<h2>Task 7</h2>

My next step in creating the algorithm is to determine if a username and device ID correspond. To do this, write a conditional that checks if the username is an element of the approved_devices and if the device_id stored at the same index as username matches the device_id entered. I'll use the logical operator and to connect the two conditions. When both conditions evaluate to True, display a message that the username is approved and another message that the user has their assigned device. 

![image](https://github.com/n8som/Develop-an-Algorithm-in-Python/assets/110139109/911811f8-da0f-4a6f-a57d-a537cf336d48)

When username is "sgilmore" and device_id is "4n482ts", the output consists of The username sgilmore is approved to access the system. on the first line and 4n482ts is the assigned device for sgilmore on the second line.

<h2>Task 8</h2>

It would also be helpful for users to receive messages when their username is not approved or their device ID is incorrect.
Add to the code by writing an elif statement. This elif statement should run when the username is part of the approved_users but the device_id doesn't match the corresponding device ID in the approved_devices. The statement should also display two messages conveying that information.

(After I run the code once with a device_id of "4n482ts", I might want to explore what happens if I assign a different value to device_id.)

![image](https://github.com/n8som/Develop-an-Algorithm-in-Python/assets/110139109/b155fe17-8157-4398-b503-d2721ce2fca8)

When username is "sgilmore" and device_id is "4n482ts", the output consists of The user sgilmore is approved to access the system. on the first line and 4n482ts is the assigned device for sgilmore on the second line.

![image](https://github.com/n8som/Develop-an-Algorithm-in-Python/assets/110139109/405508c0-2d69-4bdc-93da-c7721d494344)

If username was in the approved_devices list but device_id didn't correspond with username, the output would be a message that the user is approved to access the system but the device ID is not assigned to them.

<h2>Task 9</h2>

In this task, I'll complete my algorithm by developing a function that uses some of the code I've written in earlier tasks. This will automate the login process.

There are multiple ways to use conditionals to automate the login process. In the following code, a nested conditional is used to achieve the goals of the algorithm. There is a conditional statement inside of another conditional statement. The outer conditional handles the case when the username is approved and the case when username is not approved. The inner conditional, which is placed inside the first if statement, handles the case when the username is approved and the device_id is correct, as well as the case when the username is approved and the device_id is incorrect.

To complete this task, I must define a function named login that takes in two parameters, username and device_id. Afterward, call the function and pass in different username and device ID combinations to experiment and observe the function's behavior.

![image](https://github.com/n8som/Develop-an-Algorithm-in-Python/assets/110139109/c3d04331-317c-4bd8-87da-a0881612d3f6)

<h2>Conclusion</h2>

What are the key takeaways from this lab?

- Indexing a list is similar to indexing a string. Index values start at 0.
- The ```.append()``` method helps me add new elements to the end of lists.
- The ```.remove()``` method helps me remove elements from lists.
- The ```.index()``` method can be used on different types of sequences. They can be used not only with strings but also with lists.
  - With a list, the ```.index()``` method allows me to identify the position where a specified element is located in that list.
- If two lists contain information that corresponds to each other in a specific order, I can use indices to pair elements from the lists together.
- Functions can be used to develop algorithms. When defining a function, I must specify the parameters it takes in and the actions it should execute.

