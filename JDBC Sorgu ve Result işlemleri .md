# Sorgu ve Result işlemleri

```java
Statement statement;      //Oluşturacağımız sql sorgusu nesnesi
ResultSet resultSet;      //Gelen değerleri tutan parça
```

```java
Connection connection = dBhelper.getConnector();
statement=connection.createStatement(); 
resultSet=statement.executeQuery("SELECT * FROM city");
while (resultSet.next()){
    System.out.println(resultSet.getString("Name"));  //Name sütununda işlem yapar
}
connection.close();
```

## Insert INTO işlemleri

```java
Connection connection=null;
DbHelper dbHelper=new DbHelper();
PreparedStatement statement=null;
ResultSet resultSet;
try
{
    connection=dbHelper.getConnection();
    statement=connection.prepareStatement("INSERT INTO araba (Name,Surname) VALUES (?,?)");
		statement.setString(1,"Berkay");
		statement.setString(2,"Şen");
    statement.executeUpdate();
}
catch (SQLException exception)
{
    System.out.println(exception.getMessage());
    System.out.println(exception.getErrorCode());
}
```