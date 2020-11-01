# CounterStrike !Bomb has been oluşturulmuş planted flow'unda!





Çözüm
/assets/CounterStrike/
Dosya 32 bitlik upx ile sıkıştırılmış olarak gözükmektedir.   
![File](/assets/CounterStrike/1.png)

Önce upx ile dosyayı unpack ediyoruz.
![upx](/assets/CounterStrike/2.png)

Ardından dosyaları debuglamak için windows ortamina taşıyorum ve analiz başlasın.

Programı çalıştırdığımızda bize bombayı imha edebilmek için anahtar kelimeyi ve gizli numaralari bulmamızı ve aynı zamanda cryptexin şifresini çözmemizi söylüyor. 

![CS.exe](/assets/CounterStrike/3.png)

Programı r2 ile açip "sym._main" fonksiyonunu disassembly ettiğimizde jmp insructionu defauseTheBomb yada program sonuna gittiğini görüyoruz.
"cmp argv, 6" ile programın argüman sayisi 6'dan farklı olduğunda bomba çözme talimatlarının olduğu bölüme dallanip doğrudan kapanmaktadir.
![radare2](/assets/CounterStrike/5.png)


![CSParametre](/assets/CounterStrike/6.png)

Biz asıl görevimizi yapmak için defausetheBomb fonksiyonuna bakacağız. Aşağıda ida ile defauseTheBomb fonksiyonunun ölüm kalım haritasına bakalım.

![FuncGraph](/assets/CounterStrike/7.png)

Bizden "SafeVault" fonksiyonuna kadar ulaşmamız istenmektedir.

"SafeVault" fonksiyonuna doğru ilerlerken atoi fonksiyonlarına ve jmp instructionlarına dikkat etmemiz gerekecek. Birde dikkatimizi strcat fonksiyonuna "aI" ve "nn" stringlerinin parametre olarak gittiğini görüyoruz. Belki bu değerler bizim anahtarımız olacak diye umuyoruz.
 

