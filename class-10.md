# Error Handling & Debugging

Lets make a quick how-to guide

Something to keep in mind while handling errors is the order of execution. Specifically how the code runs.

### JavaScript interpertes one line of code at at time!

By setting good rules within your statements the code will flow nicely based on the other functions triggering.

It's a good rule of thumb to practice
1. Prepare
  - Varibales, functions and arguments
2. Execute
  - assign values to varibales, reference functions and run that code, execute statements
  
### How to deal with Errors

First start with debugging the script by using the developer tools.

You can use try, catch, throw and finally statements within your script to handle bugs.

Use the console to see which error messages pop up.

Utilize the console.log method to test functions as well.

### Try Catch Finally

Try is used to specify the code you think might throw and exception. If the exception is thrown then it goes to catch.

Catch when the exception is thrown all the code within catch is now ran.

Finally code block will always run either way. Whether the try block succeeds or fails.

```
try {
  // code goes here
} catch (exception) {
  // if the exception is thrown run this code
} finally {
  // code here runs either way
}
```
