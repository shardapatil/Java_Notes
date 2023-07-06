                                                        JavaServer Pages   
JavaServer Pages (JSP) is a technology for developing Webpages that supports dynamic content.

This helps developers insert java code in HTML pages by making use of special JSP tags, most of which start with <% and end with %>.

A JavaServer Pages component is a type of Java servlet that is designed to fulfill the role of a user interface for a Java web application.

Web developers write JSPs as text files that combine HTML or XHTML code, XML elements, and embedded JSP actions and commands.

Using JSP, you can collect input from users through Webpage forms, present records from a database or another source, and create Webpages dynamically.

JSP tags can be used for a variety of purposes, such as retrieving information from a database or registering user preferences, accessing JavaBeans components, passing control between pages, and sharing information between requests, pages etc.

                                                          MVC in JSP
MVC stands for Model View and Controller. It is a design pattern that separates the business logic, presentation logic and data.

Controller acts as an interface between View and Model. Controller intercepts all the incoming requests.

Model represents the state of the application i.e. data. It can also have business logic.

View represents the presentaion i.e. UI(User Interface).

Advantage of MVC (Model 2) Architecture

Navigation Control is centralized

Easy to maintain the large application

![image](https://github.com/shardapatil/Sharda/assets/53011896/1db994f6-b75e-47b7-9858-d65adb3cfcb1)


                                                      MVC Design Pattern
The Model View Controller (MVC) design pattern specifies that an application consist of a data model, presentation information, and control information. The pattern requires that each of these be separated into different objects. MVC is more of an architectural pattern, but not for complete application. MVC mostly relates to the UI / interaction layer of an application. You’re still going to need business logic layer, maybe some service layer and data access layer.

UML Diagram MVC Design Pattern

![image](https://github.com/shardapatil/Sharda/assets/53011896/7bf8cb78-40e0-4085-8a2d-2be65995062a)

                                                    Design components

The Model contains only the pure application data, it contains no logic describing how to present the data to a user. (Its just a data that is shipped across the application like for example from back-end server view and from front-end view to the database. In java programming, Model can be represented by the use of POJO (Plain-old-java-object) which is a simple java class.

The View presents the model’s data to the user. The view knows how to access the model’s data, but it does not know what this data means or what the user can do to manipulate it. View just represent, displays the application’s data on screen. View page are generally in the format of .html or .jsp in java programming (which is flexible).

The Controller exists between the view and the model. It is where the actual business logic is written. It listens to events triggered by the view (or another external source) and executes the appropriate reaction to these events. In most cases, the reaction is to call a method on the model. Since the view and the model are connected through a notification mechanism, the result of this action is then automatically reflected in the view.


                                                    The Lifecycle of a JSP Page

The JSP pages follow these phases:

Translation of JSP Page

Compilation of JSP Page

Classloading (the classloader loads class file)

Instantiation (Object of the Generated Servlet is created).

Initialization ( the container invokes jspInit() method).

Request processing ( the container invokes _jspService() method).

Destroy ( the container invokes jspDestroy() method).

![image](https://github.com/shardapatil/Sharda/assets/53011896/3f638bae-79c4-4624-8a0f-87e9cca10c30)

JSP page is translated into Servlet by the help of JSP translator. The JSP translator is a part of the web server which is responsible for translating the JSP page into Servlet. 

After that, Servlet page is compiled by the compiler and gets converted into the class file. 

Moreover, all the processes that happen in Servlet are performed on JSP later like initialization, committing response to the browser and destroy.
