# JDBC-iNTERVIEW-PREPARATION-Question
Interview-asked question-JDBC
1. What is Jdbc?
JDBC stands for java database connectivity. It is a standard API provided by Oracle for java application to interact with different set of databases.
2. What is API?
API is predefine classes and interfaces in java 

3.Why we use JDBC?

we want to store users  data permanently thats why we are using JDBC by using java programs .

3.what is advantage of Jdbc?

It automatically creates the XML format of data from the database that you are storing.
It does not require the content to be converted.
It provides full support to query and stored procedure.
It provides support to both Synchronous and Asynchronous processing.

4.what is disadvantage of Jdbc?

It is very sensitive when it comes to the driver. Hence, it is very important to install correct drivers and to deploy them for each type of database in order to make use of it. This is a time taking task and challenging at times.
It does not allow a single sequence to update or insert multiple tables.

5.what is difference between File system and DBMS?

The file system(Management or arrangement of file) is basically a way of arranging the files in a storage medium like a hard disk. The file system organizes the files and helps in the retrieval of files when they are required. File systems consist of different files which are grouped into directories. The directories further contain other folders and files. The file system performs basic operations like management, file naming, giving access rules, etc. 
Database Management System(Data-Mangement-software) is basically software that manages the collection of related data. It is used for storing data and retrieving the data effectively when it is needed. It also provides proper security measures for protecting the data from unauthorized access.

6.List the Basic Step Which helps to perform CRUD-Operartion on JDBC?
#Step to connect with the database:
 1) Load the driver:
	Class.forName("com.mysql.jdbc.Driver")//we will write this code inside try catch block OR
	DriverManager.registerDriver(new com.mysql.jdbc.Driver());// you can follow anyone of them
 2) Create a Connection:
	Connection conn= DriverManager.getConnection("jdbc:mysql://localhost:3306/dbname","username","password");
 3) Create query:
•	Statement //simple query
•	PreparedStatement //parameterized query
•	CallableStatement //Stored procedure
Example: 
•	String s = "select * from students";
•	Statement stmt = conn.createStatement();
•	ResultSet set=stmt.excecuteQuery(q); //we can write update also
 4) Process the data/Execute the Query:
While(set.next())
{
int id = set.getInt("StudentID");//or we can pass number also 1 2 3 row wise
String name = set.getString("StudentName");
System.out.println(id);
System.out.println(name);
}
 5) Close the Connection
Conn.close();

7.What do you mean by CRUD OPERATION?
CRUD refers to the four basic operations a software application should be able to perform – Create, Read, Update, and Delete.
In such apps, users must be able to create data, have access to the data in the UI by reading the data, update or edit the data, and delete the data.
8. What is difference between DRIVER AND DRIVERMANGER?
JDBC DriverManager(Class) is a Class that manages a list of database drivers. It matches connection requests from the java application with the proper database driver using communication subprotocol. 
JDBC Driver(Interface) is an interface enabling a Java application to interact with a database.
9.What is a Connection ?
Connection is an Interface which provide session between between Java Application and database.It helps to establish a connection with Database.

10.What is Properties and Properties File?
Properties File is on which contain the Data in the form of (key,value) pair.Which includes different properties in form of key.

11.what is difference between Statement and Prepared Statement?

Statement and Prepared Statement is used for accessing your database.

Statement interface cannot accept parameters and useful when you are using static SQL statements at runtime. If you want to run SQL query only once then this interface is preferred over PreparedStatement.

Prepared Statement is used when you want to use SQL statements many times. The PreparedStatement interface accepts input parameters at runtime.

12.what is callable Statement?
CallableStatement interface is used to call the stored procedures and functions.

13.What is difference between execute,executeUpdate and executeQuery?

ExecuteQuery:
This method is use to execute the SQL statements which retrieve some data from database.

ExecuteUpdate:
This statement is used to execute SQL statements which update or modify database.

Execute:
This method can be use for any kind of SQL statements.

14.Why do we need to close the connection?

After finishing every task we have to close connection else it may lead to resourse leaks.










