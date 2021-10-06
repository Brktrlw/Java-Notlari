# ArrayList İşlemleri

# Liste oluşturma işlemleri

```java
ArrayList liste=new ArrayList();
// Her sınıfta eleman eklenebilir
ArrayList<String> liste=new ArrayList()<String>;
// Sadece string listesi oluşturur.Ekleme /silme benzeri işlemleri yapılabilir.
```

# Listeye veri ekleme

```java
liste.add("Elma");
//add ile listeye veri ekleriz
```

# Listeden silme İşlemleri

```java
list.remove(0); 
//indexe göre silme işlemi yapar
list.remove("Berkay")
// Listeden "Berkay" elamanını siler
list.clear();
// Tüm elemanları siler
```

# Listeden eleman getirme

```java
liste.get(1); // 1. indexteki elemanı getirir. Pythondaki liste[1] gibi
```

# Listedeki elemanı değiştirme

```java
liste.set(0,"berkay"); // 0. indexteki elemanı "berkay" ile değiştirir
```

# Sıralama İşlemleri

```java
Collections.sort(liste); // Vermiş olduğumuz listeyi sıralar
```