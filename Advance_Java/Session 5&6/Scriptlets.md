                                                        JSP Scriptlet tag (Scripting elements)

In JSP, java code can be written inside the jsp page using the scriptlet tag. Let's see what are the scripting elements first.

JSP Scripting elements
The scripting elements provides the ability to insert java code inside the jsp. There are three types of scripting elements:

scriptlet tag
expression tag
declaration tag

                                                        JSP scriptlet tag
                                                        
A scriptlet tag is used to execute java source code in JSP. 

Syntax is as follows: ``` <%  java source code %>  ```

                                                            JSP expression tag

The code placed within JSP expression tag is written to the output stream of the response. So you need not write out.print() to write data. It is mainly used to print the values of variable or method.

Syntax of JSP expression tag: ``` <%=  statement %>  ```

                                                            JSP Declaration Tag
The JSP declaration tag is used to declare fields and methods.

The code written inside the jsp declaration tag is placed outside the service() method of auto generated servlet.

So it doesn't get memory at each request.

Syntax of JSP declaration tag: ``` <%!  field or method declaration %>  ```

![image](https://github.com/shardapatil/Sharda/assets/53011896/4b125c97-8821-456d-a08e-4746e22df1fa)

                                                                JSP Expression
                                                                
A JSP expression element contains a scripting language expression that is evaluated, converted to a String, and inserted where the expression appears in the JSP file.Because the value of an expression is converted to a String, you can use an expression within a line of text, whether or not it is tagged with HTML, in a JSP file.

The expression element can contain any expression that is valid according to the Java Language Specification but you cannot use a semicolon to end an expression.
Following is the syntax of JSP Expression:  ``` <%= expression %> ```

You can write the XML equivalent of the above syntax as follows:

```
<jsp:expression>

 expression
 
</jsp:expression>
```
                                                                JSP Comments
                                                                
JSP comment marks the text or the statements that the JSP container should ignore. 

A JSP comment is useful when you want to hide or "comment out", a part of your JSP page.

Following is the syntax of the JSP comments:   ``` <%-- This is JSP comment --%> ```

![image](https://github.com/shardapatil/Sharda/assets/53011896/2b006cc7-6490-46c5-9783-5aa9797b8d93)


