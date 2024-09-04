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

## Read the file contents
In order to read the file contents, I used the **.read()** method to convert it into the string.

![](/docs/py3.png)

When using an **.open()** function that includes the argument **"r"** for “read,” I can call the **.read()** function in the body of the **with** statement. The **.read()** method converts the file into a string and allows me to read it. I applied the **.read()** method to the **file** variable identified in the **with** statement. Then, I assigned the string output of this method to the variable **ip_addresses**.

In summary, this code reads the contents of the **"allow_list.txt"** file into a string format that allows me to later use the string to organize and extract data in my Python program.

## Convert the string into a list
To remove individual IP addresses from the allow list, I needed it to be in list format. Therefore, I used the **.split()** method to convert the **ip_addresses** string into a list:

![](/docs/py4.png)

The **.split()** function is used to convert a string into a list by splitting it at each whitespace by default. In this case, it splits the **ip_addresses** string into a list of individual IP addresses, making it easier to manage them. The resulting list is then reassigned back to the **ip_addresses** variable.

## Iterate through the remove list
A key part of my algorithm involves iterating through the IP addresses that are elements in the **remove_list**. To do this, I incorporated a **for** loop:

![](/docs/py5.png)

The **for** loop in Python repeats code for a specified sequence. The overall purpose of the **for** loop in a Python algorithm like this is to apply specific code statements to all elements in a sequence. The **for** keyword starts the **for** loop. It is followed by the loop variable **element** and the keyword **in**. The keyword **in** indicates to iterate through the sequence **ip_addresses** and assign each value to the loop variable **element**.