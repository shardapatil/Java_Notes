JSP Expression Language (EL) makes it possible to easily access application data stored in JavaBeans components. JSP EL allows you to create expressions both (a) arithmetic
and (b) logical. Within a JSP EL expression, you can use integers, floating point numbers, strings, the built-in constants true and false for boolean values, and null.

Simple Syntax: Typically, when you specify an attribute value in a JSP tag, you simply use a string. For example:

``` <jsp:setProperty name="box" property="perimeter" value="100"/> ```

JSP EL allows you to specify an expression for any of these attribute values. 
A simple syntax for JSP EL is as follows:  ``` ${expr} ```

Here expr specifies the expression itself. The most common operators in JSP EL are . and []. These two operators allow you to access various attributes of Java Beans and built-in JSP objects.

For example, the above syntax <jsp:setProperty> tag can be written with an expression 
like:

``` <jsp:setProperty name="box" property="perimeter"  value="${2*box.width+2*box.height}"/> ```

When the JSP compiler sees the ${} form in an attribute, it generates code to evaluate the expression and substitues the value of expresson.

![image](https://github.com/shardapatil/Sharda/assets/53011896/b4914945-94b0-456c-b4ef-a1dc45cde5d3)

![image](https://github.com/shardapatil/Sharda/assets/53011896/a139d510-e46b-4278-a33e-26744d290825)
