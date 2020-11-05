# Executor

Soru

![Soru](../../assets/web/0.png)

Çözüm

Soruda bizden filterleri atlatarak sistemde komut çalıştırmamızı istemekteydi. 

![Soru](../../assets/web/1.png)

Bir post isteğimiz vardı burp ile açıp repeteare atıyoruz "auth&commnad" şeklinde iki adet parametremiz vardı. Auth parametresi default false olarak geliyordu. O şekilde bir istek attığımızda "Not Authenticated" şeklinde response almaktayız.  

![Soru](../../assets/web/2.png)

Auth parametresini "true" olarak değiştiriyoruz. Ardından komut çalıştırabilir yetkide oluyorduk. 

![Soru](../../assets/web/3.png)

Bulunduğumuz dizinde flag.txt'yi görebilmekteyiz. Yapmamız gereken sadece cat flag.txt

![Soru](../../assets/web/4.png)

Ordasın ama ulaşamıyorum çok saçma!

Filterlerlanan karakterleri test etmek için denemeler yapmaya başladım. Dosya okumaya yarayan komutların birçoğu, space karakteri, "flag" gibi stringleri filterliyordu. 

![Soru](../../assets/web/5.png)

![Soru](../../assets/web/6.png)

Ozaman ihtiyacımız olanlar:
1- Dosyayı okuyabilecek bir komut
2- Boşluk karakteri
3- flag.txt'yi belirtecek bir alias yada tamamlayıcı

Sırasıyla kullandığım çözümler:
1- Base64
2- ${IFS}
3- fl*

![Soru](../../assets/web/7.png)




