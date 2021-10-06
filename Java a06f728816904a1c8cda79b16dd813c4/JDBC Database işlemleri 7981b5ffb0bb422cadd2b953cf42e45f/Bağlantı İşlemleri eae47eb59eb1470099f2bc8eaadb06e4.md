# Bağlantı İşlemleri

- İlk önce gerekli connectörü ekle.

### Bağlanma işlemleri

```java
static String userName="root";
static String password="12345";
static String dbUrl="jdbc:mysql://localhost:3306/databaseName";
```

```java
Connection connection=null; //baglantı nesnesi ürettik
try{
    connection= DriverManager.getConnection(dbUrl,userName,password);   //baglantı
}
 catch (SQLException throwables) {
     System.out.println("Hata oluştu "+throwables.getMessage()); //bağlantıda sorun olursa
}
finally {
    connection.close();   //her zaman calısan veritabanını kapatan blok
}
```

### Örnek Bağlantı 2 Sınıf İle

```java
import java.sql.Connection;         //Main Sınıfımız
import java.sql.SQLException;

public class Main {
    public static void main(String[] args) throws SQLException {
        Connection connection=null;
        DBhelper dBhelper=new DBhelper();
        try{
            connection= dBhelper.GetConnection();
            System.out.println("Bağlantı oluştu");
        }
        catch (SQLException throwables) {
            dBhelper.showErrorMessage(throwables);
        }
        finally {
            connection.close();
        }
    }
}
```

```java
import java.sql.Connection;         //DBHelper Sınıfımız
import java.sql.DriverManager; 
import java.sql.SQLException;

public class DBhelper {
    private String userName="root";
    private String password="12345";
    private String dbUrl="jdbc:mysql://localhost:3306/world";

    public Connection GetConnection() throws SQLException
    {
        return DriverManager.getConnection(dbUrl,userName,password);
    }
    public void showErrorMessage(SQLException exception)
    {
        System.out.println("Error: "+exception.getMessage());
        System.out.println("Error Code: "+exception.getErrorCode());
    }
}
```