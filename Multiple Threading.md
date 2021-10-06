# Multiple Threading

# Thread Oluşturma

> `Bir sınıf üretip yapılacak işlemleri buraya yaz`
> 

```java
public class Kronometre implements Runnable{ // Runnable sınıfınsan imlepemnt edilmeli
    @Override
    public void run() {
        //Do something
    }
}
```

# Thread Başlatma

```java
Kronometre kronometre=new Kronometre();
Thread t1=new Thread(kronometre);

Kronometre kronometre1=new Kronometre();
Thread t2=new Thread(kronometre1);
//Sınıftan nesneler üret

t1.start();
t2.start();
//Thread'leri başlat
```