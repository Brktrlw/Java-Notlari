# Interfaceler

- Interfacler referans tutucudur.
- Bir sınıf birden fazla interface'i implements edilebilir.
- Bir sınıf hem kalıtım hem implement edilebilir (örnek alt satırda)
    
    ```java
    public class MysqlCustomerDal extends BaseDatabaseManager implements ICustomerDal{
        @Override
        public void add() {
            System.out.println("Müşteri Eklendi MYSQL");
        }
    ```
    
- Abstract sınıflar gibi çalışır. Methodları yazmak zorundayız.

```java
public interface Irepository {
    public void add();               // İnterface'imiz
}
```

```java
public class MysqlCustomerDal implements ICustomerDal,Irepository{
    @Override
    public void add() {
        System.out.println("Müşteri Eklendi MYSQL"); 
    }
}
```