Hello, this is a tutorial regarding the installation of VScode and how to connect to a remote server.


1. reset your password for your CSE15L account by going to the following [link](https://sdacs.ucsd.edu/~icc/index.php)

![image](https://user-images.githubusercontent.com/89693979/215351866-8478461b-ed32-4e9b-a867-f8eefe086060.png)

Type in your username and your PID and you should be directed to the following page:

![image](https://user-images.githubusercontent.com/89693979/215351959-367fa31d-c601-4f94-b6d8-a30a6cd89671.png)

The three letters circled in red will be your username, they will be different for you, remember them for later. After noting down these three letters, click on the following button:

![image](https://user-images.githubusercontent.com/89693979/215352106-dec8bac5-e824-453b-ae2b-ca7171aa379c.png)

After clicking on it, you'll find a link to change your password (you may be asked to input your username and PID again):

![image](https://user-images.githubusercontent.com/89693979/215352074-432676e6-263f-4b34-b1db-7c2f05342553.png)

Once you get to the following page, enter your current password, and the new password twice. next to the green arrow, you'll see an option for yes and no. Press "yes" if you want to change your tritonlink password aswell. next to the red arrow, you should press "Yes" if you want to change the password for course specific accounts (Recommended). After inputting all the input, Do NOT press on check password. go the field next to the blue arrow then press enter.

![image](https://user-images.githubusercontent.com/89693979/215352908-d2274ae6-e92f-4066-a455-757d10e35b58.png)

After getting the following page, you should wait 15-60 mins for the new password to take effect:

![image](https://user-images.githubusercontent.com/89693979/215352435-9ac200b6-5694-4a92-a9e7-51f979be517b.png)

2. Use the following [link]( https://code.visualstudio.com/) to download VScode. (you can skip this step if you already have it downloaded.)

After you have it downloaded, a window similar to the following one should open (color and general layout shouldn't matter):

![image](https://user-images.githubusercontent.com/89693979/215352734-2479cc8a-f5d8-4bac-bf1c-2244358ef71e.png)



3. Download [git](https://gitforwindows.org/)

If you followed the steps correctly and are currently at the previously included image of VScode, you can open the terminal using either ctrl + shift + ` (top left button under esc if you're using qwerty layout) or using the terminal tab shown in the following image:

![image](https://user-images.githubusercontent.com/89693979/215353443-8e2a3a71-afff-41aa-b08d-53c79aa8c656.png)

A terminal should pop up at the bottom of the window.

After confirming that it has appeared, press ctrl+ shift + P. A search bar should appear. type "default profile" then click on it ( should be the online option if typed in correctly.)

![image](https://user-images.githubusercontent.com/89693979/215353566-d9f68132-fe6c-4730-8632-bcfbd5a0e233.png)

Then select Git Bash.

![image](https://user-images.githubusercontent.com/89693979/215353602-4b5852fd-cfb3-43fc-878e-dcc6d4d21786.png)




4. In the terminal, enter "ssh cs15lwi23xxx@ieng6.ucsd.edu" and replace the three x's with the three letters you noted down in step 1.

![image](https://user-images.githubusercontent.com/89693979/212206158-a1295a50-f878-401d-9e4c-6fa4f38b9bd5.png)

Next, type in the password that you chose in the first step(password shouldn't appear, dont worry, that's a feature not a bug.)

If the following text appears in the terminal, you're connected to the remote server (network delay issue doesn't have to be there for confirmation):

![image](https://user-images.githubusercontent.com/89693979/215353894-860b2dd9-afd4-463b-9e47-82211499f2c8.png)


5. Lets Experiment!

try out some of these commands:

1. cd ~
2. cd
3. ls -lat
4. ls -a
5. cp /home/linux/ieng6/cs15lwi23/public/hello.txt ~/
6. cat /home/linux/ieng6/cs15lwi23/public/hello.txt

![image](https://user-images.githubusercontent.com/89693979/212207499-6965f8f9-f31c-47f9-ba3c-a7dae4fc1d8d.png)


Next, we'll try creating a website where you can show your creations.

go to [github](www.github.com)

click on the + in the top right and create a new repository. name it cse15l-lab-reports.

then, under the set up in desktop button, you'll find a create new file button.

create a file called index.md and type anything in it.

next, go to the settings of the repository and click on the pages tab.

go the branch seciton and select main, then save.

wait 20 seconds before refreshing the page.

Congratulations, you now have a web page.

you can include links to other files in your repository in index.md to reference them.

now, make a tutorial on what you just learned for your underclassmen
