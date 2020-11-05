# Executor

## Soru

![Soru](../../assets/Executor/0.png)

## Çözüm

Soruda bizden filterleri atlatarak sistemde komut çalıştırmamızı istemekteydi. 

![1](../../assets/Executor/1.png)

Bir post isteğimiz vardı burp ile açıp repeteare atıyoruz "auth&commnad" şeklinde iki adet parametremiz vardı. Auth parametresi default false olarak geliyordu. O şekilde bir istek attığımızda "Not Authenticated" şeklinde response almaktayız.  

![2](../../assets/Executor/2.png)

Auth parametresini "true" olarak değiştiriyoruz. Ardından komut çalıştırabilir yetkide oluyorduk. 

![3](../../assets/Executor/3.png)

Bulunduğumuz dizinde flag.txt'yi görebilmekteyiz. Yapmamız gereken sadece cat flag.txt

![4](../../assets/Executor/4.png)

Ordasın ama ulaşamıyorum çok saçma!

Filterlerlanan karakterleri test etmek için denemeler yapmaya başladım. Dosya okumaya yarayan komutların birçoğu, space karakteri, "flag" gibi stringleri filterliyordu. 

![5](../../assets/Executor/5.png)

![6](../../assets/Executor/6.png)

**Ozaman ihtiyacımız olanlar:**
1- Dosyayı okuyabilecek bir komut
2- Boşluk karakteri
3- flag.txt'yi belirtecek bir alias yada tamamlayıcı

**Sırasıyla kullandığım çözümler:**
1- Base64
2- ${IFS}
3- fl*

![flagls](../../assets/Executor/7.png)




