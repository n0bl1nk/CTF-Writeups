# Luping

## Soru

![Soru](../../assets/Lupin/0.png)

## Çözüm

Rar dosyasını açtığımızda içerisinde 6 adet jpg çıkıyor. Bu resimlere bakınca insan kör oluyor. 

![Soru](../../assets/Lupin/Question/1.jpg)

![Soru](../../assets/Lupin/Question/2.jpg)

![Soru](../../assets/Lupin/Question/3.jpg)

![Soru](../../assets/Lupin/Question/4.jpg)

![Soru](../../assets/Lupin/Question/5.jpg)

![Soru](../../assets/Lupin/Question/scheme.jpg)

![Soru](../../assets/Lupin/Question/x5.jpg)

Resimlere exif ile baktığımızda ilginç birşey görmüyoruz.

"Binwalk *" ile tüm resimlere baktığımızda x5.jpg dosyasında bir jpeg daha gömülü olduğunu görüyoruz. 

![Binwalk](../../assets/Lupin/2.png)

İçerisindeki jpeg'i çıkartıyoruz.

![Binwalk](../../assets/Lupin/3.png)

![Flag](../../assets/Lupin/4.jpg)