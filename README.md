# Update a file through a Python algorithm

## Project description
At my organization, access to restricted content is managed through an IP-based allow list, defined in the **"allow_list.txt"** file. To ensure security and proper access control, we maintain a separate remove list containing IP addresses that should be revoked from the allow list. I developed an algorithm that automates the process of updating the **"allow_list.txt"** file by efficiently removing IP addresses that are listed in the remove list, ensuring that unauthorized addresses no longer have access to the restricted content.

## Open the file that contains the allow list
For the first part of the algorithm, I opened the **"allow_list.txt"** file. First, I assigned this file name as a string to the **import_file** variable:

![](/docs/py1.png)

Then, I used a **with** statement to open the file:

![](/docs/py2.png)

In my algorithm, the **with** statement is used with the **.open()** function in read mode to open the allow list file for the purpose of reading it. The purpose of opening the file is to allow me to access the IP addresses stored in the allow list file. 

The **with** keyword will help manage the resources by closing the file after exiting the **with** statement. In the code **with open(import_file, "r") as file:**, the **open()** function has two parameters. The first identifies the file to import, and then the second indicates what I want to do with the file. In this case, **"r"** indicates that I want to read it. 

The code also uses the **as** keyword to assign a variable named **file**; **file** stores the output of the **.open()** function while I work within the **with** statement.