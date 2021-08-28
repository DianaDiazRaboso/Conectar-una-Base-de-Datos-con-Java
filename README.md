# Conectar-una-Base-de-Datos-con-Java

Código Java para acceder a una base de datos. Y así poder hacer una consulta en lenguaje SQL.

En primer lugar, importamos la librería java.sql para usar la base de datos desde Eclipse:

------
import pymysql
------

Es necesario asegurarnos de que el driver JDBC esté debidamente conectado. 
Una vez hecho, establecemos la conexión con la base de datos por medio de estas instrucciones:


-------

try {
	Connection miConexion =DriverManager.getConnection("rute", "user", "password", "bd" );
Statement miStatement =miConexion.createStatement();
			
			ResultSet miResultset =miStatement.executeQuery("SELECT  * FROM TTable");
			
			while(miResultset.next()) {
				
				System.out.println(miResultset.getString("n") + " " + miResultset.getString("n1"));
			}
			
		}catch (Exception e) {	
			System.out.println("error");
			
			e.printStackTrace();
      
--------
