Lab Report 2
=======
_Sravya Chittuluri_

**Part 1: StringServer**

Code for my StringServer.java file: 

<img width="893" alt="image" src="https://user-images.githubusercontent.com/75595601/215631966-9136499f-8ae6-4a5d-936b-9af3081da421.png">
* Here, I define the `handleRequest` method, which uses the `equals`, `getPath`, and the `split` methods. 
* The `handleRequest` method takes in a URI object (a url) and checks to see if it has "add-message" in the path using the equals method. If it does, then it checks if the query has a string to add to the message being displayed.

Output in the local host: 

<img width="499" alt="image" src="https://user-images.githubusercontent.com/75595601/215633689-9c38663e-ffd5-4b94-bec0-c4d2ba3ec721.png">
* Here, the `handleRequest` method is called and given the URL `http://localhost:4970/add-message?s=Hello%20World`. It first checks if the URL's path is only `\`, which it is not. It moves on to checking if the path is equal to `/add-message`, which it is. The part after the query is isolated and the message, "Hello World", is appended to `message`.

<img width="564" alt="image" src="https://user-images.githubusercontent.com/75595601/215633764-08237747-66ad-4f1d-9ec5-b1ff602e0b4b.png">
* Here, the `handleRequest` method is called and given the URL `http://localhost:4970/add-message?s=My%20name%20is%20Sravya`. It first checks if the URL's path is only `\`, which it is not. It moves on to checking if the path is equal to `/add-message`, which it is. The part after the query is isolated and the message, "My name is Sravya", is appended to `message`.

**Part 2: Bugs from Lab 3**

`reverseInPlace()` method:

<img width="737" alt="image" src="https://user-images.githubusercontent.com/75595601/215635326-e951a0f0-4ee4-42e2-bd6e-bcb676954775.png">
* This JUnit test was to see if the method correctly reversed the integers in an array. The test failed, so the method is buggy.

<img width="527" alt="image" src="https://user-images.githubusercontent.com/75595601/215636184-90596293-20e7-4e12-af7c-782fb1b186e7.png">
* This JUnit test was to see if the method would work for an array of one integer, and it worked.

The problem with the code is that it copies the values from the latter half of the array but then begins copying the same values onto the second half, making a palindrome. To fix this, I created a temp array to copy the data from the original array, and assigned the values in the temp array backwards into the original array.

Here is the fixed code: 

```
 static void reverseInPlace(int[] arr) {
   int[] temp = new int[arr.length];
   for (int i = 0; i < arr.length; i++) {
     temp[i] = arr[i];
   }
   for (int i = 0; i < arr.length; i++) {
     arr[i] = temp[temp.length - 1 - i];
   }
 }
```

Here are the JUnit tests that passed after the code was fixed:

<img width="527" alt="image" src="https://user-images.githubusercontent.com/75595601/215636845-fe1b50a9-5dbb-4bf5-b1da-0918475ed460.png">

<img width="581" alt="image" src="https://user-images.githubusercontent.com/75595601/215636902-1b95a65d-5652-4258-bdef-9365655b0e8c.png">


**Part 3: Reflection**

One thing I learned from week 2 was how to build and modify my own web server. While I've used web servers in the past, I've never attempted to edit their internal code to produce different results. I learned about how to process URLs using a URLHandler, and isolate their paths and queries. Then, in week 3, I built upon this knowledge by using what I've learned about JUnit tests in CSE 12 to write and debug  methods in web servers to produce different functionalities.


