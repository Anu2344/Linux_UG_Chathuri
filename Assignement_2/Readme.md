**Script to List Level 2 Directory Contents in Linux**

*Question* </br>
</br>
<ins> 
Select five level 2 directories and save their contents in one file, "listing.md". Here "level 2" directory is for example /home/mylogin/, but not /tmp/ (level 1) or /usr/local/bin/ (level 3). Contents = listing of filenames.
</ins>


*Objective* </br>
The goal of this task was to:</br>
</br>1. Identify five Level 2 directories (subdirectories of subdirectories) with content.</br>
2. Save the contents of these directories to a .md file.</br>
3. Overcome challenges, such as permission issues, encountered during the process.

**Process and Commands** </br>
Navigating the Directory Structure

>Started at the root folder using the *cd* command.
Used the *ls* command to view all directories and files in the root folder. </br></br>
Selected directories from the list and navigated inside using:


*cd <directory_name>*
</br>

>Repeated the *ls* command inside each directory to view its contents and determine if it had files or subdirectories.</br>

>Saving Directory Contents to a File
Initially, attempted to save the output to *listing.md*:

*ls -p /sys/kernel | grep -v / >> listing.md*

>However, this resulted in an access denied error due to insufficient permissions.

**Resolving Permission Issues**

>Verified write permissions in the current directory using:

*ls -ld* </br>

>Since the directory lacked write permissions, redirected the output to a writable directory *(~/notedir)*: </br>

Created the directory:

*mkdir ~/notedir*
</br>
>Saved the output to the .md file:

*ls -p /sys/kernel | grep -v / >> ~/notedir/listing.md*

![](Assignment_2/Image_2/image_1.png)

![](/Image_2/image_2.png)

![](/Image_2/image_3.png)

![](/Image_2/image_4.png)

![](/Image_2/image_5.png)

![](/Image_2/image_6.png)

![](/Image_2/image_7.png)

![](/Image_2/listing.md.png)

**Challenges and Resolutions**
</br>
1. Access Denied While Creating .md File

Issue: Attempting to create listing.md in a directory without write permissions.</br>
*Solution: Redirected output to a writable directory (~/notedir).*</br>

2. Misuse of mkdir Command

Issue: Attempted to create a directory with a .md extension (~notedir.md), which caused confusion.</br>
*Solution: Used mkdir ~/notedir to create a valid directory and saved the .md file inside it.*

