JDBC stands for Java Database Connectivity. JDBC is a Java API to connect and execute the query with the database. It is a part of JavaSE (Java Standard Edition). JDBC API uses JDBC drivers to connect with the database. There are four types of JDBC drivers:
   JDBC-ODBC Bridge Driver,
   Native Driver,
   Network Protocol Driver, and
   Thin Driver

Why Should We Use JDBC

Before JDBC, ODBC API was the database API to connect and execute the query with the database. But, ODBC API uses ODBC driver which is written in C language (i.e. platform dependent and unsecured). That is why Java has defined its own API (JDBC API) that uses JDBC drivers (written in Java language).
We can use JDBC API to handle database using Java program and can perform the following activities:
    Connect to the database
    Execute queries and update statements to the database
    Retrieve the result received from the database.

		try {
	         // Load the MySQL JDBC driver
	         Class.forName("com.mysql.jdbc.Driver");

	         // Connect to the database
	         String url = "jdbc:mysql://localhost:3306/new_schema";
	         String user = "user";
	         String password = "user";
	         Connection con = DriverManager.getConnection(url, user, password);

	         // Create a statement
	         Statement stmt = con.createStatement();

	         // Execute a query to retrieve the data from the table
	         ResultSet rs = stmt.executeQuery("SELECT * FROM courses");

	         //Adding the Records of the table to the Array List
	         while (rs.next()) {
	        	    String name = rs.getString("Name");
	        	    String info = rs.getString("Info");

	        	    Course course = new Course(name, info);
	        	    courses.add(course);
	        	   
	        	}
	         
	         for(Course s : courses) {
	        	 model.addElement(s.getName());
	         }
	         
	         // Close the connection and release resources
	         rs.close();
	         stmt.close();
	         con.close();
	      } catch (Exception e) {
	         System.out.println(e);
	      }
