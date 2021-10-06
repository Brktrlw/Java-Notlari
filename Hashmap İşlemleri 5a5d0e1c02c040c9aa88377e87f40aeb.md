# Hashmap İşlemleri

## Tanımlama İşlemi

```java
HashMap<String,String> sozluk=new HashMap<>();
```

## Eleman Ekleme

```java
sozluk.put("book","kitap");
```

## Elemana ulaşma

```java
sozluk.get("book"); // Key değerini veririz,value'sini alırız.
"********************************************************************"
sozluk.forEach((k, v) -> {
    System.out.println(k+" "+v);
});
```

## Eleman Silme

```java
sozluk.remove("book");  // keyi veririz tamamen siler
sozluk.clear();    // TÜm elemanları tamamen siler
```