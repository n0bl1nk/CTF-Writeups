# Find The Picture

Soru

![Soru](../../assets/findthepic/0.png)

Çözüm

Dosyayı indirip "7z" ile açmaya çalıştığımızda password istemektedir. Hashcat veya johntheRipper ile bruteforce yaptığımızda "RockYou" parolasi ile zipi açıyorum açıyoruuuum aaaaa

![hiyarReis](../../assets/findthepic/1.jpg)

Zamanını boşa harcama şeklinde bir resim çıkıyor. 

![DontWasteTime](../../assets/findthepic/2.jpg)

Binwalk ile baktığımızda PNG uzantılı bir dosya olduğunu görüyoruz.

![binwalk](../../assets/findthepic/3.png)

Dosyayı çıkartmak için binwalk veya dd komutunu kullanabiliriz. 

![BinwalkExtPng](../../assets/findthepic/4.png)

Çıkarttığımız resmi açtığımızda paintle çizilmiş flagi buluyoruz.

![flag](../../assets/findthepic/5.png)
