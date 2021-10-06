# Static ve Inner Class

# Static

- Classlarda static method çağrılırsa constructor çalışmaz onun yerine static methodlar kullanılır ve birden fazla static method tanımlanabilir

```java
public class MysqlCustomerDal{
        static {
            System.out.println("Statik method çalıştı");
        }
    }
```

# Inner Class

- Ana sınıf static olamaz ancak ana sınıfın altındaki sınıf static bir sınıf olabilir.Örnek:

```java
public class MysqlCustomerDal{
        public static class Sinif{
            
        }
}
```