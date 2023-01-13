The first step you need to take is reseting your password for your CSE15L account by going this [link](https://sdacs.ucsd.edu/~icc/index.php)

after you reset the password you'll be shown a seemingly random arrangment of letters "cs15lwi23xxx" with the last three letters being different for every student. 
note down the last three letters.

next, download [git](https://gitforwindows.org/)

then, open up visual studio code and press the down arrow icon on the right side of the terminal. you'll find git bash, press on that.

in the terminal, enter "ssh cs15lwi23xxx@ieng6.ucsd.edu" and replace the three x's with the three letters you noted down.

![image](https://user-images.githubusercontent.com/89693979/212206158-a1295a50-f878-401d-9e4c-6fa4f38b9bd5.png)


then it'll ask you if you want to connect, type yes.

next, type in the password that you chose in the first step.

Congratulations! you're connected to the remote server.

try out some of these commands:

cd ~
cd
ls -lat
ls -a
cp /home/linux/ieng6/cs15lwi23/public/hello.txt ~/
cat /home/linux/ieng6/cs15lwi23/public/hello.txt

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
