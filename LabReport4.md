1)  First of all, we need to login to ieng6.

Use the following command-line to login.




![image](https://user-images.githubusercontent.com/89693979/221756372-1b18ff4b-ed68-4164-ab1f-1731c5c5c9b7.png)



```
ssh cs15lwi23zz@ieng6.ucsd.edu
```



replace the zz between wi23 and the "@" with your three letter username which can be found [here](https://sdacs.ucsd.edu/~icc/index.php).

If its your first time logging in during your session, an authenticity warning will pop up. type "Yes"



![image](https://user-images.githubusercontent.com/89693979/221757252-191ffb66-bf7b-4bdd-be1f-d3757f4f380c.png)



You might be prompted to enter your password, it varies from account to account (if you type in your password, it will be invisible. Not a bug, a feature!)



![image](https://user-images.githubusercontent.com/89693979/221756908-42c23c5a-198b-46d2-aac2-ce30ffa880a6.png)



An indicator of a successful login is the display of a Last Login in time (which you might not have if this is your first time)

![image](https://user-images.githubusercontent.com/89693979/221757167-1692a7f9-4fc1-4967-95b8-388eb9a741ff.png)


2)

Next,

go to the [lab7 repo](https://github.com/ucsd-cse15l-w23/lab7) and fork it.

![image](https://user-images.githubusercontent.com/89693979/221758355-883c4e98-f4c4-49cc-88ef-94124f16ebf2.png)


This will take you to your fork of the repo. Copy the link shown below:

![image](https://user-images.githubusercontent.com/89693979/221758453-489dc145-d882-4f7f-8173-2bd5d689e783.png)



Clone the lab7 repository you forked by using:

```
git clone *repo link*
```

![image](https://user-images.githubusercontent.com/89693979/221758981-e4cc67af-99e2-419d-8c0f-08be47a70da6.png)


Before you move on to the next step, don't forget to ```cd``` into the lab7 directory.

Side note: you can check what directory you're in by looking to the left of the command-line number.


```
cd lab7
```



![image](https://user-images.githubusercontent.com/89693979/221759463-3f30595c-e3d1-479c-b22f-d7c92c9cfa79.png)


3)


Now that you've cloned the repo and ```cd```'d into it,



Compile and Run the tests on our file:


Compile:


```
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
```

![image](https://user-images.githubusercontent.com/89693979/221759880-3df65dab-f981-40b7-8c3d-65e75aee0f22.png)


A sign of success for compilation is nothing showing up and a new command-line being presented




Run:

```
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
```

![image](https://user-images.githubusercontent.com/89693979/221760110-b7460468-9258-468e-9905-aeca5c26b1d7.png)



There is a failure in the Test!


4)

To fix it, use the the ```nano``` command on the file with the error. In our case, that file is "ListExamples.java."


```
nano ListExamples.java
```

The file with the error should be displayed:

![image](https://user-images.githubusercontent.com/89693979/221767744-4f4aea9f-35b3-4ac1-9d2d-c3ba7010f19e.png)



The error with our file is a typo, index1 was written when it should have been index2.

![image](https://user-images.githubusercontent.com/89693979/221767824-a15205cb-8165-4d04-b370-c536666707d8.png)


To fix the error follow these key clicks:

```
<down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down>
<down><down><down><down><down><down><down><down><down><down><down<down><down><down><down><down>
<down><down><down><down><down><down><down><down><down><down>

<right><right><right><right><right><right><right><right><right><right><right><right>

<backspace>

<2>
```

If you following the key clicks above correctly, index1 should be corrected to index2.


Next, you need to exit and save the file.


To save the file: press ```ctrl + <O>```

you will be prompted with the following prompt to change the files name:


![image](https://user-images.githubusercontent.com/89693979/221763900-63de09ab-57be-49b1-a0ba-e6c7fdadb749.png)

For our case we don't change anything so just press ```<Enter>```.

Lastly, press ```ctrl + <X>``` to exit the file.


5)

Now, lets run the tests again to see if we've passed them. 

To skip the time waste of typing our the compile code line again, press ```<up><up><up>``` to find it. This is the history of your command-line.


![image](https://user-images.githubusercontent.com/89693979/221765196-c94b037e-c65f-4cc6-a6d1-0159afa52098.png)


Press  ```<up><up><up>``` on the new command-space to find the "run" command-line.


your tests should pass:

![image](https://user-images.githubusercontent.com/89693979/221769832-97b1a5a4-9dcf-43c7-8dbf-dd4078c2e6ad.png)


6)

Now, we need to push the fix to github.

we'll use the ```add```,```commit```, and ```push``` commands.

```
git add ListExamples.java
```

![image](https://user-images.githubusercontent.com/89693979/221799699-bf92131a-e557-433c-acd1-86e734c52a6f.png)





Then, 

```
git commmit - m "comitted"
```

![image](https://user-images.githubusercontent.com/89693979/221800101-b6ab6908-1159-4662-a376-e936fef17ce1.png)



Finally,


```
git push origin main
```

![image](https://user-images.githubusercontent.com/89693979/221800297-dde85756-9183-4b17-b940-4cceb7b8ab78.png)



