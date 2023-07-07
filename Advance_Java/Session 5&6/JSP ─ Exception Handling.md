                                                            JSP ─ Exception Handling

When you are writing a JSP code, you might make coding errors which can occur at any part of the code. There may occur the following type of errors in your JSP code:

1. Checked exceptions
    A checked exception is an exception that is typically a user error or a problem that cannot 
    be foreseen by the programmer. For example, if a file is to be opened, but the file cannot 
    be found, an exception occurs. These exceptions cannot simply be ignored at the time of compilation.
   
2. Runtime exceptions
    A runtime exception is an exception that probably could have been avoided by the 
    programmer. As opposed to the checked exceptions, runtime exceptions are ignored at the time of compliation.
   
3. Errors
    These are not exceptions at all, but problems that arise beyond the control of the user or 
    the programmer. Errors are typically ignored in your code because you can rarely do 
    anything about an error. For example, if a stack overflow occurs, an error will arise. They are also ignored at the time of compilation.

ways to handle run time exception/error occuring in your JSP code.

Using Exception Object

The exception object is an instance of a subclass of Throwable (e.g., java.lang. NullPointerException) and is only available in error pages.
Following table lists out the important methods available in the Throwable class.

![image](https://github.com/shardapatil/Sharda/assets/53011896/c34056eb-08aa-4def-a8ca-2ac0951543df)
![image](https://github.com/shardapatil/Sharda/assets/53011896/ebc9167b-4f4c-45d1-8923-c285f913483f)
