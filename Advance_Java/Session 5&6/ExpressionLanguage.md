JSP Expression Language (EL) makes it possible to easily access application data stored in JavaBeans components. JSP EL allows you to create expressions both (a) arithmetic
and (b) logical. Within a JSP EL expression, you can use integers, floating point numbers, strings, the built-in constants true and false for boolean values, and null.

Simple Syntax: Typically, when you specify an attribute value in a JSP tag, you simply use a string. For example:

``` <jsp:setProperty name="box" property="perimeter" value="100"/> ```

JSP EL allows you to specify an expression for any of these attribute values. 
A simple syntax for JSP EL is as follows:  ``` ${expr} ```
