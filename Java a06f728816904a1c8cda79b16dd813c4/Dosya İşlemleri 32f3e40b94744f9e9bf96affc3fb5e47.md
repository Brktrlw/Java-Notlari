# Dosya İşlemleri

## Dosya Metotları

```java
File file= new File("deneme.txt");
if(file.exists()){
    System.out.println("Böyle bir dosya var");
}
else {
    System.out.println("Böyle bir dosya yok");
}
```

```java
file.getName();          // Dosyanın ismini getirir
file.getAbsoluteFile();  // Dosyanın Yolunu getirir;
file.canRead();          // Dosya okunuyorsa true döndürür
file.canWrite();         // Dosya yazılabiliyorsa true döndürür
file.length();           // Dosyanın boyutunu getirir (byte)
```

## Dosyadan Okuma

```java
File file= new File("berkay2.txt");
Scanner scanner=new Scanner(file);
while (scanner.hasNextLine())
{
    String line =scanner.nextLine();    //Dosyadaki her satırı değişkene aktarır
}
scanner.close();
// try catch gerekebilir
```

## Dosyaya Yazma

```java
BufferedWriter writer=new BufferedWriter(new FileWriter("berkay2.txt"));
writer.write("Yazılacak Metin");   // Tüm verileri siler tekrardan yazar
writer.close(); 
// try catch gerekebilir
"*****************************************************************************"
BufferedWriter writer=new BufferedWriter(new FileWriter("berkay2.txt",true));
// İkinci parametre true girilirse appende modu ile açar ve metinler dosyaya eklenir.
```