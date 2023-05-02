Download Link: https://assignmentchef.com/product/solved-comp2100-exam
<br>
This question extends a red-black tree to a three-color tree data structure.There are the following properties for a three-color tree:

<ol>

 <li>Each node is either PINK, PURPLE or MAGENTA.</li>

 <li>Root and every leaf (NULL pointer) are PINK.</li>

 <li>Each path from Root-to-Leaf has the same number of PINK nodes.</li>

 <li>A MAGENTA node cannot have a MAGENTA child, and must at least has a PURPLE child.</li>

 <li>A PURPLE node must have only PINK children.</li>

</ol>

Please implement the checking functions testProp1, testProp2, testProp3, testProp4 to check if properties (1), (2), (3), (4) hold. Hint: testProp5() has been already implemented in the partial code. You are allowed to define additional methods in your implementation. But you cannot alter the signatures of the given methods and the package structures of the given classes. Please upload the ThreeColourTree.java file to wattle for marking.

<strong>Q2: </strong> You are given a java class called Something, which has a method called someMethod. Please implement a minimum number of test cases for testing someMethod that are <strong>branch complete </strong>within someMethod. Write your test case(s) in test() method in SomethingTest.java. You cannot alter the signatures of the given methods and the package structures of the given classes.

<strong><u>Please upload the </u></strong><strong><u>SomethingTest.java file to wattle for marking.</u></strong>

<strong>Q3</strong>. In this question, you will implement a simple database in XML supporting a simple SQL command INSERT.

The database is a Customer database. A table has multiple records, where a record represents a row in the table. The data in the same column of a table are associated with the same field name as the records. Each record has a unique numeric ID. The data can only include alphabet, numbers and spaces.

Here is an example of the database:

ID | Name        | Address   | City   | Postcode | Country

—————————————————————

1 | ‘J Doe’         |’1 Main St’|’Sydney’| ‘2000’ |’Australia’

Consider the following SQL command:

The SQL INSERT command aims to create a new record in a table and generate a new ID for the new record. It has the following format:

INSERT INTO <em>table_name </em>(<em>column1</em>, <em>column2</em>, <em>column3</em>, …) VALUES (<em>value1</em>, <em>value2</em>, <em>value3</em>, …);

Example:

INSERT INTO Customers (ID, Name, Address, City, Postcode,

Country)

VALUES (1, ‘J Doe’, ‘1 Main St’, ‘Sydney’, ‘2000’, ‘Australia’);

&lt;Command&gt; := INSERT INTO &lt;table_name&gt; (&lt;columns&gt;) VALUES &lt;values&gt;

&lt;table_name&gt; := &lt;str&gt;

&lt;columns&gt; := &lt;var&gt;, &lt;columns&gt; |  &lt;var&gt;

&lt;values&gt; := ‘&lt;str&gt;’, ‘&lt;num&gt;’, &lt;values&gt; |  ‘&lt;str&gt;’, ‘&lt;num&gt;’

where &lt;num&gt; is an integer literal,&lt;var&gt; and &lt;table_name&gt; are string literals with only alphabet, &lt;str&gt; is a string literal with only alphabet, numbers and spaces.

<strong>Tasks:</strong>

Implement the following tasks:

<ol>

 <li> Implement load() and insert() in XMLTable.java. save() is already given.</li>

</ol>

Each customer must have an ID value, but may not have all the following column values (e.g. Name, Address, City, Postcode, Country). Please see test cases in XMLTableTest.java.

<ol start="2">

 <li> Implement next() method in Tokeniser.java to extract the SQL commands as Tokens as follows

  <ol>

   <li>Token 1:</li>

  </ol></li>

</ol>

originalTokenStr: INSERT INTO table_name (column1, column2, column3, …) type: INSERT_INTO value: table_name (column1, column2, column3, …) b.   Token 2:

originalTokenStr: VALUES (value1, value2, value3, …) type: VALUES

value: (value1, value2, value3, …)

Note that some brackets in the SQL commands may be missing. Please return null if some brackets are missing. Please see the test cases in TokeniserTest.java

<ol start="3">

 <li> Implement parseExp() in Parser.java to extract the columns and values from tokens and execute the SQL command to insert new customers. Do not insert customers if the following errors are found:

  <ol>

   <li>some brackets are missing</li>

   <li>some column names are wrong</li>

  </ol></li>

</ol>

Please see the column names in Customer.java file and test cases in ParserTest.java

For each task, we provided you with some JUnit tests, whose file name ends with “[…]Test.java”. Please note that when marking, we might use different test cases.

<strong><u>Please upload the following files to Wattle for marking: </u></strong><strong><u>XMLTable.java, Tokeniser.java and </u></strong><strong><u>Parser.java.</u></strong>