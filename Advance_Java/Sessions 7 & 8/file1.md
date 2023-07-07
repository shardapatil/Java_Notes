Q1. What is JDBC?

JDBC stands for Java Database Connectivity, which is a standard Java API for database-independent connectivity between the Java programming language,
and a wide range of databases.

The JDBC library includes APIs for each of the tasks mentioned below that are commonly associated with database usage. 

 Making a connection to a database.  Creating SQL or MySQL statements. 

 Executing SQL or MySQL queries in the database. 

 Viewing & Modifying the resulting records.

Fundamentally, JDBC is a specification that provides a complete set of interfaces that allows for portable access to an underlying database. 
Java can be used to write different types of executables, such as:

 Java Applications

 Java Applets

 Java Servlets

 Java ServerPages (JSPs)

 Enterprise JavaBeans (EJBs).

All of these different executables are able to use a JDBC driver to access a database, and take advantage of the stored data.

                                                          Architecture of JDBC
                                                          
 The JDBC API supports both two-tier and three-tier processing models for database access but in general, JDBC Architecture consists of two layers:                               
1) Application: It is the Java servlet or an applet that communicates with the data source.
                 This provides the application-to-JDBC Manager connection.

3) The JDBC API: It allows the Java programs to perform the execution of the SQL statements and then get the results.
                 This supports the JDBC Manager-to-Driver Connection.

The JDBC API uses a driver manager and database-specific drivers to provide transparent connectivity to heterogeneous databases.

The JDBC driver manager ensures that the correct driver is used to access each data source. The driver manager is capable of supporting multiple concurrent 
drivers connected to multiple heterogeneous databases.

Following is the architectural diagram, which shows the location of the driver manager with respect to the JDBC drivers and the Java application:

![image](https://github.com/shardapatil/Sharda/assets/53011896/c44fa78e-b862-4c63-870b-4f395bca305f)

                                                      Common JDBC Components
                                                      
The JDBC API provides the following interfaces and classes:

 DriverManager: This class manages a list of database drivers. Matches connection requests from the java application with the proper database 
                  driver using communication subprotocol. The first driver that recognizes a certain subprotocol under JDBC will be used to establish a database                       Connection.
                  
 Driver: This interface handles the communications with the database server. You will interact directly with Driver objects very rarely. Instead, 
            you use DriverManager objects, which manages objects of this type. It also abstracts the details associated with working with Driver objects. 
            
 Connection: This interface with all methods for contacting a database. 
              The connection object represents communication context, i.e., all communication with database is through connection object only.
              
 Statement: You use objects created from this interface to submit the SQL 
            statements to the database. Some derived interfaces accept parameters in addition to executing stored procedures.
            
 ResultSet: These objects hold data retrieved from a database after you execute an SQL query using Statement objects. It acts as an iterator to 
              allow you to move through its data.
              
 SQLException: This class handles any errors that occur in a database application

                                                              JDBC Drivers

JDBC driver implementations vary because of the wide variety of operating systems and hardware platforms in which Java operates. Sun has divided the implementation types into four categories, Types 1, 2, 3, and 4, which is explained below:

Type 1: JDBC-ODBC Bridge Driver

  In a Type 1 driver, a JDBC bridge is used to access ODBC drivers installed on each client machine. Using ODBC, requires configuring on your system a Data 
  Source Name (DSN) that represents the target database. When Java first came out, this was a useful driver because most databases only 
  supported ODBC access but now this type of driver is recommended only for experimental use or when no other alternative is available.

Type 2: JDBC-Native API

In a Type 2 driver, JDBC API calls are converted into native C/C++ API calls,which are unique to the database. These drivers are typically provided by the 
database vendors and used in the same manner as the JDBC-ODBC Bridge. The vendor-specific driver must be installed on each client machine.
If we change the Database, we have to change the native API, as it is specific to a database and they are mostly obsolete now, but you may realize some speed 
increase with a Type 2 driver, because it eliminates ODBC's overhead.

Type 3: JDBC-Net Pure Java

  In a Type 3 driver, a three-tier approach is used to access databases. The JDBC clients use standard network sockets to communicate with a middleware application   server. The socket information is then translated by the middleware application server into the call format required by the DBMS, and forwarded to the database     server.
  This kind of driver is extremely flexible, since it requires no code installed on the client and a single driver can actually provide access to multiple       
  databases.

Type 4: 100% Pure Java

  In a Type 4 driver, a pure Java-based driver communicates directly with thevendor's database through socket connection. This is the highest performance 
  driver available for the database and is usually provided by the vendor itself.
  This kind of driver is extremely flexible, you don't need to install special software on the client or server. Further, these drivers can be downloaded   
  dynamically.
