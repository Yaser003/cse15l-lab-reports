PART 1:


Code for String Server:


```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;
public class StringHandler implements URLHandler {
    private ArrayList<String> messages = new ArrayList<String>();
    
    public String handleRequest(URI uri) {
        if (uri.getPath().contains("/add-message")) {
            System.out.println(uri.getPath());
            String[] message = uri.getQuery().split("=");
            messages.add(message[1]);
            StringBuilder result = new StringBuilder();
            for (String s : messages) {
                result.append("\n" +s);
            }
            return result.toString();
        }else{
            return "Invalid request";
        }
    }
}
class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new StringHandler());
    }
}
```


![SCREENSHOT](./screenshot1.png)




When the server is first started, the main method is called.

- When I add my name to the URI as show in the image above, the handleRequest method is called and it divides the url into two parts, a string before the equal sign and a string after the equal sign. with the string after the equal sign being the message to be added to the "messages" arrayList that will be returned at the end of the method.

- The values affected include the arrayList which has now been appended with my name (the message.)



![SCREENSHOT](./screenshot2.png)




-When I add all the strings to the query the handleRequest method seperates each of them after the "=" sign.

-The values affected include the arrayList which has now been appended with multiple strings including my last name, the class code, etc.





PART 2:


method bug chosen: 

```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
}
```



Failure-inducing input:


```
public void testReverseInPlace() {
    int[] input = {6,1,2 , 3};
    ArrayExamples.reverseInPlace(input);
    assertArrayEquals(new int[]{3,2,1,6}, input);
	}
```


Non-Failure-Inducing Input:


```
public void testReverseInPlace() {
    int[] input = {6};
    ArrayExamples.reverseInPlace(input);
    assertArrayEquals(new int[]{6}, input);
}
```


Symptoms:



Failure Inducing:






![SCREENSHOT](./screenshot3.png)






Non-Failure-Inducing:






![SCREENSHOT](./screenshot4.png)





The buggy code before the fix:



```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
}
```



Fixed:



```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length /2; i++) {
      int j = arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i - 1] = j;
    }
    
  }
```



The fix works because it prevents the earlier indexes from being overwritten by storing said indexes in the variable "j"  on each run of the loop and then storing them back into the end of the array for the first element (or their corresponding place.)



PART 3:



In the week 2 lab I learned to create local servers and how to edit their outputs based on the requests of the user. I learned several new server related terms such as "port", which is a number the server is assigned, and "localhost" which turns out to be the device running the local server. example: My laptop.



In the week 3 lab I learned an efficient way to debug using the JUNIT program. I learned how to use assertEquals and all its derivatives. I also learned a more efficient way to read symptoms of bugs to better take care of them.







