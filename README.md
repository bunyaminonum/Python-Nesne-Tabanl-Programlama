# Python Nesne Tabanlı Programlama

[Nesne Tabanlı Programlama (OOP) Nedir?](#nesne-tabanlı-programlama-oop-nedir)

[Nesne Tabanlı Programlamanın (OOP) Avantajları](#nesne-tabanlı-programlamanın-oop-avantajları)
* [Tekrar Kullanılabilirlik (Reusability)](#tekrar-kullanılabilirlik-reusability)
* [Genişleyebilirlik (Extensibility)](#genişleyebilirlik-extensibility)
* [Sürdürülebilirlik (Maintainability)](#sürdürülebilirlik-maintainability)

[Python Class Yapısı](#python-class-yapısı)
* [Pyhon Class (Sınıf) Tanımlama](#pyhon-class-sınıf-tanımlama)
* [Python Sınıf Öznitelikleri (Class Attributes)](#python-sınıf-öznitelikleri-class-attributes)
* [Sınıfların Örneklenmesi](#sınıfların-örneklenmesi)
* [Nesnelere Değer Atama](#nesnelere-değer-atama)
* [Örnek Öznitelikleri ve init Fonksiyonu](#örnek-öznitelikleri-ve-init-fonksiyonu)

[Sınıf Metotları](#sınıf-metotları)

[Statik Metotlar](#statik-metotlar)

[Kalıtım (Inheritance)](#kalıtım-inheritance)

[Python'da Override](#pythonda-override)

[Kapsülleme (Encapsulation)](#kapsülleme-encapsulation)

## Nesne Tabanlı Programlama (OOP) Nedir?
Nesne tabanlı programlama, ingilizce de OOP(Object Oriented Programming) olarak isimlendirilen, yazılım tasarımını işlevler ve mantıktan ziyade veriler veya nesneler etrafında organize eden bir programlama modelidir.

Nesne Tabanlı Programlama yaklaşımı; büyük, karmaşık ve aktif olarak güncellenen veya bakımı yapılan programlar için çok uygundur.  Buna imalat ve tasarım programlarını örnek olarak verebiliriz.  Nesneye yönelik programlama kavramını daha iyi anlamak adına şöyle bir örnek verebiliriz:  Bir arabayı  ve bu arabanın ne gibi özellikleri olduğunu düşün.  Bu arabanın rengi, modeli,  motor hacmi, hızı ve daha birçok özelliği bulunur. Bu arabanın bir de işlevleri vardır; hızlanmak, yavaşlamak, vites değiştirmek, direksiyonu döndürmek vb.  işlevleri sayabiliriz.  Bu özelliklerin ve işlevlerin bir araba "nesnesi" altında toplandığına dikkat edelim, zira nesne tabanlı programlama tam da buna benzer bir yapıdan oluşmaktadır.

Bu yazıda Python ile Nesne Tabanlı Programlama anlatılacak olup, konunun daha iyi anlaşılabilmesi adına aşağıda belirtilen Python konularını önceden bilmeniz beklenmektedir. Bu konular:

* Değişkenler ve Temel İşlemler
* Parametreler ve Argümanlar 
* Dosya Okuma ve Yazma
* Fonksiyonlar 
* if, elif, else karar yapıları
* Döngüler

Not:  Bu derste fonksiyonlar için bazen metot bazen de fonksiyon ismi kullanılmıştır. İkisi de aynı anlama gelmektedir.

## Nesne Tabanlı Programlamanın (OOP) Avantajları
İlk kez Nesne Tabanlı Programlama öğreniyorsanız doğal olarak aklınıza gelen ilk sorulardan biri "Nesne Tabanlı Programlama benim ne işime yarayacak?"  sorusu olabilir. Bu noktada eğer şimdiye kadar büyük ve karmaşık programlar yazmamışsanız OOP 'nin ne gibi avantajlar sağladığını anlama konusunda biraz zorluk çekebilirsiniz. Şimdi gelin OOP 'nin en önemli avantajlarına bir göz atalım.

### Tekrar Kullanılabilirlik (Reusability)
Tekrar kullanılabilirlik (Reusability),  adından da anlışalacağı üzere bir kez yazılmış kodlar gerektiğinde yeniden yazmadan tekrar tekrar kullanılabilir ve bunu OOP'nin bir yapısı olarak bir sınıf (class) içerisinde kullanıldığında diğer programcıların da kodumuzu kullanabilir hale getirebiliyoruz.  Örneğin bir araba üreticisini düşünün, bu araba üreticisi ürettiği ilk aracın özelliklerini yeniden keşfetmek yerine yeni model araçlara entegre edip bu araçlara ek özellik ekleyebilir.  Tekrar kullanılabilirlik (reusability) kavramını inheritance (kalıtım)  konusunu anlatırken daha iyi anlaycaksınız.

### Genişleyebilirlik (Extensibility)
Genişleyebilirlik (Extensibility),  adından da anlaşılacağı üzere kodlarımıza kolayca yeni kodlar ekleyip genişletmemize olanak tanır.  Tekrar bir araba üreticisini düşünelim, bu üreticinin A1 model bir araba ürettiğini düşünelim. Bu araç modelinde silecekler açık döngü kontrol sistemine sahip, yani sadece insan müdahelesiyle açılıp kapanıyor. Üretici bir zaman sonra A2 modelinde yeni bir araç üretiyor ve bu araçta sileceklerler bir sensör yoluyla yağmur yağdığında otomatik olarak çalışabilmesini sağlamak istiyor.  İşte tam burada OOP'nin genişleyebilirlik özelliği sayesinde sileceklere bu özellik kolayca eklenerek silecekler, isteğe bağlı olarak otomatik veya manuel olarak çalıştırılabilir. 

### Sürdürülebilirlik (Maintainability)
Sürdürülebilirlik (Maintainability), bir yazılımın kolayca değiştirilebilir, kullanıcı dostu ve hızlı olmasıyla ilgilenir. Tam olarak aynı işlevselliğe sahip iki farklı yazılım sistemi düşünün. Aynı girdi verildiğinde, her ikisi de tam olarak aynı çıktıyı hesaplar. Bu iki sistemden biri hızlı ve kullanıcı dostudur aynı zamanda kaynak kodunun değiştirilmesi kolaydır. Diğer sistem ise yavaş, kullanımı zor ve kaynak kodunun değiştirilmesini bırakın anlaşılması bile neredeyse imkansızdır. Her iki sistem de aynı işlevselliğe sahip olsa da, kaliteleri farklıdır.  Bir sistemin hızlı, kullanıcı dostu ve kaynak kodunun kolayca değiştirilmesi tam olarak nesne tabanlı programlamayı ifade etmektedir. On binlerce kodun aynı kod parçasının altında birleştiğini düşünün ve bir de bu kod parçalarının sınıflara parçalandığını, her bir sınıfın hangi görevi üstlendiğini bildiğinizi düşünün. Hangisini seçerdiniz? Tahmin edildiği gibi sınıflara ayrılan kod sistemini seçtiniz çünkü bu sınıflara erişmek ve değiştirmek istdiğinizde bunu kolayca yapabiliyorsunuz. İşte bu yapıya OOP'nin Sürdürülebilirliği dioruz.

# Python Class Yapısı
Python class yapısı, Python nesne tabanlı proramlamanın yapı taşlarından biridir. Bu yapıyı anlayabilmek için önce "class" kelimesinin anlamına ve bunun Türçe'deki karşılığına bakacağız. Class kelimesi İngilizce olup türkçe karşılığı "sınıf" olarak tanımlanır. Bu sınıflardan türettiğimiz bir de "nesneler(objects)" bulunur. Nesneleri ve özellikleri tanımlarken referans olarak aldığımız yapılar sınıflar(class) dır. Örneğin "Ahmet" adında bir kişi tanımlamak istiyoruz. Bu kişinin adı, soyadı, kimlik numarası vb özellikleri bulunur. Bir de bu kişinin; koşma, yürüme, nefes alma gibi işlevleri (fonksiyonları) bulunur.  Bu kişiyi oluşturmak için önce adı, soyadı, kimlik numarası gibi özellekleri ve koşma, yürüme, nefes alma gibi işlevleri(fonksiyonları) barındıran  "Ahmet" gibi farklı nesneleri de tanımlayabileceğimiz aynı zamanda ana referansımız olacak bir sınıf (class) oluşturmamız gerekecektir. Oluşturduğumuz sınıflar sayesinde, nesneye atamak istediğimiz öznitellikeri her nesne için ayrı ayrı tanımlamak durumunda kalmıyoruz. Bu kadar teorikten sonra Python (sınıf) class tanımlamaya geçebiliriz.

## Pyhon Class (Sınıf) Tanımlama
#### Aşağıdaki kodları inceleyiniz.
![Python_class_tanimlama](https://user-images.githubusercontent.com/59376910/153707361-83d01730-e64f-4940-a3e0-80dd5be1dc65.png)

Bildiğiniz üzere Python'da fonksiyon tanımlamak için "def" anahtar kelimesini kullanıyorduk. Python sınıf (class) yapısı tanımlamak için de "class" anahtar kelimesi kullanılır. Yukarıdaki resimde "class" anahtar kelimesinden sonra gelen "Personel" kelimesi ise tanımladığımız sınıfın ismidir.  Buraya siz herhangi bir isim verebilirsiniz, ama Python nesne tabanlı programlamada sınıf (class) isminin ilk harfi  büyük  olur. Bu yazım şekli zorunluluk olmasa da programcılıkta bu bir âdet haline gelmiştir. Python'da bildiğiniz üzere curly bracket (süslü parantez) kullanılmıyor, sadece girintilerden faydalınılıyor. Resimde de gözüktüğü üzere class tanımladıktan sonra tıpkı fonksiyonlarda yaptığımız gibi burada da özelliklerimizi ve fonksiyonlarımızı bir tab boşluk bırakarak yazıyoruz. 
Yukarıda tanımlanan class yapısını aşağıda gösterildiği şekilde yani parantezli olarak da tanımlayabiliriz. Parantezli ve parantezsiz arasındaki farklı Inheritence (kalıtım) konusunu işlerken anlayacaksınız.

![Python_class_tanimlama2](https://user-images.githubusercontent.com/59376910/153707431-6192b535-8947-46e2-8d94-d000000211a8.png)

## Python Sınıf Öznitelikleri (Class Attributes) 
Aşağıdaki kodların açıklamasını okumadan önce kendiniz yazmaya ve anlamaya çalışın.

#### sınıf özniteliği (class attribute) tanımlama ve ekrana yazdırma 
![Python_class_oznitelik_tanimlama](https://user-images.githubusercontent.com/59376910/153707551-1d2cd703-c37d-4544-ad33-75712c61ce63.png)

#### Öznitelik değer ataması
![oznitelik_atama](https://user-images.githubusercontent.com/59376910/153707586-5551b5cd-efc9-41de-9ac4-72568b1bd4ab.png)

Burada Personel sınıfının özniteliklerini (attributes) tanımlamış olduk.  Buradaki öznitelikere sınıf öznitelikleri (class attributes) adı verilir. Bu özniteliklere erişirken birçok programlama dilinde olduğu gibi nokta (.) erişim belirtecini kullanıdık. Burada ekrana yazdırdığımız zam oranı, atadığımız isim ve soyisim örnek özniteliklerdir. İsterseniz diğerlerini de ekrana bastırabilir, değer atayabilir veya ek öznitelik ekleyebilirsiniz. Dikkat ettiyseniz  özniteliklere erişirken (Personel.zam_orani)  sınıf ismini yazarken parantez kullanmadık. Parantez kullandığımızda farklı bir şey tanımlamış oluyoruz.  Bundan biraz sonra bahsedilecek.

Yukarıdaki kod örneklerinden de anlaşılacağı gibi, biz istediğimiz zaman istediğimiz özniteliğe erişebilir,değer atayabilir veya ek öznitelik ekleyebiliriz. Fakat bir sorunumuz var; biz bir Personel() nesnesi tanımlarken bu şekilde sadece bir nesne tanımlayabilyoruz. Bizim istediğimiz şey ise, Aynı Personel() sınıfından "Ahmet", "Mehmet", "Veli" gibi farklı "nesneler (objects)" tanımlamaktır. Bir sonraki başlıkta bu konuyu inceliyor olacağız.

## Sınıfların Örneklenmesi
Sınıflar belli birtakım özelliklere sahip grupları tanımlamak için harika yapılardır. Fakat önceki yazıda da bahsettiğimiz gibi, bu sınıfların işe yaraması için bir sınıftan birden çok nesne (object) yaratmamız gerekiyor. Aşağıdaki kodları dikkatlice inceleyin.

![instance_Python](https://user-images.githubusercontent.com/59376910/153708058-c17bffc2-b0e4-4396-96f0-b506f67e05a2.png)

Burada Personel() sınıfını Ahmet adında bir değişkene atadık. Teknik dilde bu işleme örnekleme (instantiation) adı verilir. 

Burada Ahmet artık Personel() sınıfının bir nesnesi (object) haline geldi. Örnekleme sayesinde tek sınıftan teorik olarak aynı özniteliklere fakat farklı özelliklere sahip sınırsız sayıda nesneler (object) oluşturabiliriz. Şimdi gelin bu nesnelere değer atamanın nasıl yapıldığını ve aynı değerlere sahip iki nesnenin eşit olup olmadığına bakalım.

## Nesnelere Değer Atama
Bir nesneye nasıl değer atanır görelim:

![nesneye_deger_atama](https://user-images.githubusercontent.com/59376910/153708306-758c1076-4a94-4756-a3c1-4895125185ec.png)

Python'da nesneye değer atama işlemi; "nesne_ismi.öznitelik_ismi = değer " şeklinde tanımlanır. Nesneye erişimek istediğimizde ise; "nesne_ismi.öznitelik_ismi" kalıbını kullanabiliriz. Bu örnekte Ahmet nesnesine isim ve yaş tanımladık. Önceki konularda da belirtildiği gibi, dilerseniz bu özniteliklere yenilerini ekleyebilir ve farklı değerler atayabilirsiniz. Şimdi de aynı sınıftan farklı bir nesne oluşturup, isim ve yaş ataması yapalım:

![nesne_tanimlama_2](https://user-images.githubusercontent.com/59376910/153708327-2be28a0f-2284-41f5-bb9a-58c0fd89783e.png)

Şimdi de "Ahmet" ve "Mehmet" nesnelerine atadığımız özellikleri ekrana bastıralım:

![nesne_ozelliklerine_erisim](https://user-images.githubusercontent.com/59376910/153708336-8492a19b-369c-44cb-b949-a30261b9bcc9.png)

Şimdi de Personel() sınıfına "kabiliyet" özniteliğini bir liste olarak tanımlayalım. Personel sınıfına tanımladığımız tüm öznitelikler aşağıdaki gibi oldu:

![personel_oznitelikler](https://user-images.githubusercontent.com/59376910/153708352-03b8cce0-491c-47c7-9b7f-41bdc35b1db5.png)

Şimdi de "Ahmet" nesnesine kabiliyet ekleyelim. "Mehmet" nesnesine bu öznitelik ile ilgili henüz herhangi bir değer atamış değiliz buna dikkat edelim.

![Ahmet_kabiliyet_ekleme](https://user-images.githubusercontent.com/59376910/153708362-7540c759-beee-47ce-a76b-d67ec0822767.png)

Şimdi de Ahmet ve Mehmet nesnelerinin kabiliyetlerini ekrana yazdıralım:

![kabiliyetler](https://user-images.githubusercontent.com/59376910/153708372-a556003f-cdb6-4c84-80aa-668f8bd46cca.png)

Görüldüğü üzere Ahmet'in kabiliyetleri tam olarak beklediğimiz gibi geldi, fakat Mehmet'e baktığımız zaman biz sadece Ahmet nesnesine kabiliyet eklemiştik ama Ahmet nesnesine eklediğimiz kabiliyet Mehmet nesnesine de eklenmiş. Peki neden?

Sınıf yapısının en özemli özelliklerinden biri,  özniteliklere atanan değerlerin ve yapılabiliyorsa bu değerler üzerinde sonradan yapılan değişikliklerin diğer tüm nesneler üzeride yapılmasını sağlamaktır. İlgili sınıf özniteliği; karakter, demet veya sayı gibi değiştirilemeyen (ummutable) veri tipi ise, bu sınıf özniteliği üzerinde zaten herhangi bir değişiklik yapamazsınız. Yapabileceğiniz tek şey, ilgili özniteliği yeniden tanımlamak olacaktır. Ancak eğer sınıf niteliği liste, sözlük ve küme gibi değiştirilebilir (mutable) veri tipi ise bu öznitelik üzerinde yapacağınız değişiklikler sınıfa ait tüm nesneleri etkileyecektir. Bu özellik bazı durumlarda istenebilir veya istenmeyebilir önemli olan yazılan program, class yapısı ile yazılıyorsa bu bilginin farkında olunarak yazılmalı. Mesela kabiliyet örneğinde bu özellik istenmeyen sonuçlara neden olabilir çünkü her personelin kendine ait kabiliyetleri bulunur dolayısı ile bir personele eklenen özellik diğer personele de eklenmemeli veya kontrollü eklenmeli. Eğer bu bir personel listesi olsaydı belki de istediğimiz şey tam da bu özellik olurdu. 

## Örnek Öznitelikleri ve __init__ Fonksiyonu
Bildiğimiz üzere hiçbir fonksiyon kullanmadan sınıf içerisinde oluşturduğumuz özniteliklere sınıf öznitelikleri (class attribute) adını veriyorduk. Sınıf özniteliklerine dışarıdan erişebilir ve değerlerini değiştirebiliyorduk. Ayrıca liste, sözlük ve küme gibi değiştirilebilir veri tipleri üzerinde yaptığımız değişiklikler yeni oluşturulan tüm nesneleri etkiliyordu. Peki biz bu özniteliklerin sınıf çağrıldığında erişim sağlamak istesek ve aynı zamanda bu özniteliklere istediğimiz şekilde erişim izni sağlamak istesek ne yapacağız? İşte tam burada __init__ fonksiyonu imdadımıza yetişiyor. Bu fonksiyona teknik dilde constructor (yapıcı metod) adı verilir. Bu metod içerisinde tanımlanan özniteliklere ise örnek öznitelikler (instance attributes) adı verilir.

 __init__ fonsksiyonda bulunan alt çizgiler onu özel bir fonksiyon yapmaktadır. Bu fonksiyonunun asıl görevi nesne (örn: Ahmet = Personel() ) ilk oluşturulduğu anda o fonksiyonda tanımlanan öznitelikleri ve gerçekleştirilecek işlemleri tanımlamaktır. Hatırlarsanız __init__ fonksiyonu tanımlamadan önce sınıf özniteliklerine erişmek için herhangi bir nesne tanımlamak gerekmiyordu. Fakat __init__ fonksiyonundaki özniteliklere erişmek için önce bir nesne tanımlamak durumundayız. Python'da yapıcı metod (__init__), şu şekilde tanımlanır:
 
 ![constructor](https://user-images.githubusercontent.com/59376910/153708402-aca67819-ea14-4142-a2c3-4ffc1906b16b.png)

__İnit__ fonksiyonunu tanımlarken  alt def anahtar kelimesini ayrı, içinde self bulunduran parantez yapısını birleşik yazmaya özen gösterelim.  Burada  self isminde bir parametreye ihtiyacımız var. Python nesne tabanlı programlamada belki de en çok kullanacağınız parametre self parametresi olacak. self parametresi, fonksiyonda parametreleri tanımlamak ve bu parametrelere erişmek için kullanılır. self yerine başka bir kelime de kullanabilirsiniz fakat kesinlikle önerilmez, çünkü Dünya'daki neredeyse tüm Python yazılımcıları self ismini kullanmaktadır. Kodunuz okunabilirliği açısından bu durum çok önemlidir. Şimdi instace attribute dediğimiz örnek özniteliklerimizi tanımlamaya başlayabiliriz:

![init_nitelik_tanimlama](https://user-images.githubusercontent.com/59376910/153708414-2f1b39de-f1c3-46b4-8e86-f6063b911d5c.png)

self parametresi kullanarak isim özniteliğimizi tanımladık şimdi bir Personel() nesnesi oluşturalım ve bu niteliğe erişmeye çalışalım:

![ekrana_yazma](https://user-images.githubusercontent.com/59376910/153708434-8901d3cc-921e-462c-877c-cb1de96ba0ef.png)

Yukarıdaki kodlarda per1 adında bir nesne oluşturduk ve bu nesneye önceden Personel sınıfımızdaki __init__ fonkisyonu içinde tanımladığımız isim özniteliğine erişmeye çalıştık. Gördüğünüz gibi kod başarılı bir şekilde çalıştı. Peki isim özniteliğimizi self parametresi olmadan aşağıdaki gibi tanımlasaydık isim özniteliğimize yine erilebilir miydik? Görelim:

![hata_self](https://user-images.githubusercontent.com/59376910/153708449-e619136c-2847-4276-9141-cf1efeee2868.png)

Görüldüğü üzere program, isim adında bir özelliğin olmadığını söyleyerek hata verdi. Bu hatanın nedeni tahmin ettiğiniz gibi isim özniteliğinin self parametresi almadığındandır, çünkü __init__ fonksiyonundaki özniteliklere erişmeyi sağlayan yapı self parametresidir. Sınıf içinde farklı fonksiyonlar tanımlarken de fonksiyon içinde bazen __init__ fonksiyonu içindeki özniteliklere erişmek gerekebilir. Burada da yine self parametresi sayesinde diğer fonksiyonlardan __init__ fonksiyonu içindeki özniteliklere erişim sağlayabiliyoruz.

Yukardıki örneklerde init fonksiyonunu sadece self parametresi ile kullanmıştık. Elbette nesne ilk oluşturulduğunda o nesneye atamak istediğimiz özellikler olabilir. İşte bu özellikleri __init__ fonksiyonuna parametre olarak yollayabiliriz. Bunun nasıl yapıldığını görelim:

![init_parametre_Atama](https://user-images.githubusercontent.com/59376910/153708584-7fc6a9d4-6896-459b-85ed-b48e1100cef4.png)

⚠ Burada isim, soyisim ve maas bilgilerini self parametresi kullanarak değişkenlere atadığımıza dikkat edelim. Şimdi de bu bilgilerin içinden isim ve soyismini listeleyen tam_ad fonksiyonunu tanımlayalım:

![tam_ad_fonks](https://user-images.githubusercontent.com/59376910/153708602-a3dff15e-4980-4d70-80d2-235381d67e1e.png)

Görüldüğü gibi tam_ad fonksiyonu tanımlarken fonksiyonel yapıda kullandığımız klasik metod tanımlamayı burada da kullanıyoruz.  Bu şekilde tanımladığımız fonksiyonlara örnek metodları (instance methods) adı verilir. Örnek metod tanımlarken __init__ fonsiyonunda olduğu gibi bu fonksiyona, oluşturduğumuz nesneden erişebilmemiz için self parametresi kullanıyoruz. Aynı şekilde tam ad örnek metodunda olduğu gibi örnek niteliklere veya fonkisiyona parametre atamışsak bu parametrelere nesneden erişebilmek için yine self öneki kullanmamız gerekecektir. Şimdi iki tane nesne oluşturalım ve oluşturduğumuz nesnelerden tam_ad örnek metodumuzu çağıralım:

![tam_ad_fonk_Call](https://user-images.githubusercontent.com/59376910/153708614-482d0da2-ce16-44b6-882a-b5122f263704.png)

Unutulmamalıdır ki örnek öznitelikler (instance attributes) nesneye özel özniteliklerdir, yani farklı nesneler için aynı metod kullanılabilir fakat o metod o an kullanıldığı nesneye aittir. Farklı nesneleri etkilemez. Örnek özniteliklerini sınıf öznitelikler ile arasındaki en önemli farklardan biri budur. Yukarıdaki örnekte de olduğu gibi atanan isim, soyisim ve maaş bilgileri nesneye özel olarak atanır. Dolayısı ile o nesnelerdeki özellikleri değiştirme, silme veya güncelleme işlemlerini yapmak sadece nesnenin özelliklerini ilgilendirir. Diğer nesnelerde herhangi bir değişiklik meydana gelmez. Bu arada yukarı per1 ve per2 nesnelerini oluştururken Personle sınıfına atadığımız argümanların nereden geldiği hakkında bir fikir karışıklığı olmuş olabilir. Bu argümanlar __init__ fonksiyonuna atadığımız parametrelerden geliyor, yani Python'da __init__ fonksiyonuna hangi parametreler atanmışsa nesne oluştururken o an kullanılan sınıfa bu parametrelere argüman olarak değer atanır. Dilerseniz argümanlarınızı parametre ismi olmadan direkt yazabilirsiniz.

# Sınıf Metotları
Sınıf metotları (class methods), sınıf özniteliklerine (class attribute) direkt sınıf adıyla erişmek ve sınıf özniteliklerini manipüle etmek içi kullanılır. Sınıf metotlarının kodlar yardımı ile daha kolay anlaşılabileceğine inanıyorum. Hatırlarsanız bir önceki derste şöyle bir kodumuz vardı:

![tam_ad_fonks (1)](https://user-images.githubusercontent.com/59376910/153711331-271c9943-bab9-44da-9a12-caafba73e577.png)

Personel sınıfımızda __init__ fonksiyonumuzun içinde tanımlanan yapılara örnek öznitelikleri (instance attribute) adı verildiğini biliyoruz.  Sınıf içinde yani init fonksiyonumuzun dışında tanımladığımız yapılara da sınıf öznitelikleri (class attribute) adını veriyorduk. Bu bilgiyi hatırlattıktan sonra  Personel sınıfımıza bir sınıf listesi değişkeni birkaç tane de fonksiyon ekleyelim:

![personel_genel_fonksiyonlar](https://user-images.githubusercontent.com/59376910/153711347-e2f118f9-0a33-47c4-bb99-783e8c0ec774.png)

Burada ek olarak Personel sınıfımıza personel_listesi adında bir liste değişkeni atadık. Bu liste değişkeninin sınıf özniteliği (class attribute) olduğunu hatırlayalım. Liste değişkenini atadıktan sonra personel_listesine_ekle edında bir sınıf metotu (instance method) tanımladık. Bu metot ile sınıf özniteliği olan personel_listesi değişkeninin append özelliğini kullanarak tam_ad fonksiyonunu parametre olarak atadık ve personel_listesine_ekle fonksiyonunu __init__ fonksiyonunda tanımladık. Bu şekilde biz nesne oluşturulduğu anda sınıfa verdiğimiz argümanlardan personel_listesi listesine tamd_ad fonksiyonunun döndürdüğü isim ve soyismi eklemiş oluyoruz. Bir de personel sayısını gösteren personel_sayisini_goruntule adında bir örnek metotu tanımladık. Bu fonksiyonuda len fonksiyonunu kullanarak personel listesindeki eleman sayısını ekrana yazdırmasını sağlıyoruz. Dikkat ettiyseniz personel_listesi  listesine sınıf adıyla erişim sağlanmış. Dilerseniz bu listeye self parametresi ile de erişim sağlayabilirsiniz. Şimdi hemen bir nesne oluşturalım ve neler olup bittiğine bir göz atalım:

![sinif_metotlari](https://user-images.githubusercontent.com/59376910/153711360-b7adf7ec-c859-43ce-a5f7-2ee12cfe8a3e.png)

Burada Ahmet adında bir nesne oluşturduk ve aynı nesne ile personel_sayisini_goruntule fonksiyonunu çağırdık. Bize Ahmet Öz adındaki kişinin personel listesine eklendiğini ve personel_listesi  listesindeki personel sayısını bildiriyor, yani bütün sınıfa hitap eden bir fonksiyonu bir nesne aracılığıyla çağırdık. Peki elimizde hiç eleman olmayan bir personel listesi olsa bu ve bu personel listesindeki eleman sayısını ekrana yazdırmak istesek bunu yapabilir miyiz? Tabi ki hayır, çünkü biz personel_sayisini_goruntule fonksiyonunu bir örnek metotu (instance method) olarak tanımladık, zira örnek öznitelikleri ve örnek metotları kullanabilmemiz için bir örnek yani bir nesne oluşturmamız gerekecektir. Burada bir diğer sorun da, bütün sınıfı ilgilendiren ve sınıf öznitelikleri üzerinde işlem yapan bir fonksiyon nesne adıyla değil sınıf adıyla çağrılması gerekir. Mantıklı olan da budur. İşte tam da burada bize sınıf metotları (class methods) yardım edecek. Sınıf metotları sayesinde, bir örnek(nesne) tanımlamadan ve direkt sınıf adını kullanarak o metoda erişebiliyoruz. Şimdi personel_sayisini_goruntule metodunu bir sınıf metodu (class method) olarak tanımlanmış halini Personel sınıfı üzerinde görelim:

![class_method](https://user-images.githubusercontent.com/59376910/153711368-20892c33-4050-4755-a544-468f06599ecd.png)

Burada önceden anlatılmayan iki terim var; @classmethod ve cls. @classmethod bezeyicisi altında tanımlanan fonksiyonlar birer sınıf metoduna dönüşür. cls öneki tıpkı self öneki gibidir. Python bu isimlerin ne olduğuyla ilgilenmez, ilk parametrenin ne olduğuyla ilgilenir, fakat biz bir sınıf metodu tanımlayacaksak bu metodun ilk parametresi, yani öneki cls adıyla tanımlarız. Eğer bir örnek metodu tanımlayacaksak bunun ilk parametresi self adıyla tanımlanır. Sınıf içinde fonksiyon tanımlarken fonksiyonundan önce bir bezeyici (decorator) yoksa python bunu örnek metodu olarak algılar, fakat her zaman her fonksiyonun örnek motodu olmasını istemeyiz, zira sınıf metotlarında görüdüğümüz üzere nesne oluşturmadan bir fonksiyonu çağırmak istediğimizde sınıf metotları biçilmiş kaftan olarak karşımıza çıkıyor. Dolayısıyla biz bir fonksiyonun önüne @classmethod bezeyicisini eklemişsek bu artık bir sınıf metodudur ve bu metoda nesne tanımlamadan sınıf ismiyle erişebilirsiniz anlamına gelir. Gelin personel_sayisini_goruntule metoduna sınıf adıyla erişmeye çalışalım:

![class_method_2](https://user-images.githubusercontent.com/59376910/153711377-bd000940-ee9e-4de2-b1d0-e59bf0614808.png)

Görüldüğü gibi personel_sayisini_goruntule metodunu nesne tanımlamadan sınıf adıyla tanımladık ve çıktı olarak ta 0 sonucunu aldık. Eğer biz bu fonksiyonu tanımlamadan önce @classmethod bezeyicisini kullanmasaydık bu fonksiyona sınıf adıyla erişmeye çalıştığımızda hata alacaktık, çünkü bir nesne tanımlamadan örnek metodları kullanamayız.

# Statik Metotlar
Python nesne tabanlı programlama içinde şimdiye kadar iki tane fonksiyon gördük; biri örnek metodu (instance method) diğeri de sınıf metodu (class method). Metod türünü belirtmesi adına Örnek metotları için self parametresini, sınıf metotları için ise cls parametresini kullanıyorduk. Örnek metodunu örnek öznitelikleri üzerinde işlemler yapmak için, sınıf metodunu da sınıf öznitelikleri üzerinde işlemler yapmak için kullanıyorduk. Eğer ikisini de kullanmaya ihtiyacımız yoksa bu fonksiyon statik metot (static method) olarak adlandırılır. Bilindiği gibi sınıf metodu tanımlarken @classmethod bezeyicisini kullanıyorduk. Static metot tanımlamak için de @staticmethod bezeyicisini (decorator) kullanacağız. Bu bezeyicileri kullanmamızın nedeni, sınıf içinde tanımlanan fonksiyonlar varsayılan olarak örnek metodu olarak tanımlanır, yani sınıfa atanacak ilk parametre örnek sınıfını temsil ediyor (self). Mesela bezeyici olmadan bir fonksiyon tanımlayıp ilk argümanını cls olarak tanımlarsanız bu, sınıf metodu değil, örnek metodu olarak tanımlanır. Bu yüzden fonksiyonlarda ilk parametrenin hangi metodu temsil edeceğini belirlemek için bezeyicileri kullanıyoruz. Şimdi bir örnek ile üç metodu da kullanalım:

![static_method](https://user-images.githubusercontent.com/59376910/153711592-0cfe2f9f-2449-4554-9a05-900c989711f7.png)

Görüldüğü üzere statik_metot fonksiyonunun içinde nesne özniteliklerini veya sınıf özniteliklerini kullanmamızı gerektirecek bir durum yok. Bundan dolayı @staticmethod bezeyicisini kullanarak fonksiyonu statik hale getirdik. Eğer hem sınıf hem de nesne özniteliklerine ihtiycaç duymayacağınız bir fonksiyon yaratacaksanız, fonksiyonunuzu statik metot olarak tanımlamanız mantıklı olacaktır. Şimdi bu metoda hem sınıftan hem de nesneden erişmeye çalışalım:

![access_static_methods](https://user-images.githubusercontent.com/59376910/153711639-78aeefbc-1cac-4d89-85ea-06c8ae3f0335.png)

Görüldüğü gibi static_metot fonksiyonununa sınıf metotları gibi hem nesneden hem de sınıf adıyla erişim sağlayabildik. Sınıf metotları ve statik metotlar birbirine çok benzer, sadece herhangi bir sınıf veya örnek özniteliği kullanılmadığı durumlarda cls parmetresi boşuna tanımlanmış olacaktır. Bu yüzden bu durumda statik metot kullanılır.

# Kalıtım (Inheritance) 
Kalıtım (inheritance), Python nesne tabanlı programlamanın en önemli konularından biridir. Kalıtımı bu kadar önemli kulan şey kod tekrarını engelemesidir. Kalıtıma aynı zamanda "miras alma" da denilebilir. Python'da miras alma yaparken iki terimden bahsedebiliriz bunlar; child class ve parent class sınıflarıdır. child class yani çocuk sınıfı ebeveny sınıftan miras alır. Bunları biraz sonra ayrıntılı olarak ele alacağız. Şimdi önce bir Personel isminde bir sınıf tanımlayalım:

Kalıtım (inheritance), Python nesne tabanlı programlamanın en önemli konularından biridir. Kalıtımı bu kadar önemli kulan şey kod tekrarını engelemesidir. Kalıtıma aynı zamanda "miras alma" da denilebilir. Python'da miras alma yaparken iki terimden bahsedebiliriz bunlar; child class ve parent class sınıflarıdır. child class yani çocuk sınıfı ebeveny sınıftan miras alır. Bunları biraz sonra ayrıntılı olarak ele alacağız. Şimdi önce bir Personel isminde bir sınıf tanımlayalım:

![personel](https://user-images.githubusercontent.com/59376910/153711685-38399504-308d-43c8-9d00-ce4f61b4e1a5.png)

Şimdi de Mudur isminde bir sınıf olusturalım:

![mudur_sinifi](https://user-images.githubusercontent.com/59376910/153711694-916c1f60-86a3-4733-bbd6-777300ac357b.png)

Mudur sınıfını tanımlarken şimdiye kadar görmediğiniz sınıf tanınlama şekli ile karşılaştınız. Burada amaçlanan şey, "Personel sınıfındaki tüm öznitelikleri ve metotların Mudur sınıfında da kullanılmasını sağla" yani Mudur sınıfı Personel sınıfını miras alıyor. Bu durumda Mudur sınıfı child class, Personel sınıfı ise parent class oluyor. Python da bir sınıfı miras almak istersek, oluşturduğumuz sınıfa bir parantez açarak parantez içine miras almak istediğimiz sınıfın ismini yazıyoruz. Bu basit yol ile miras aldığımız sınıfın tüm özelliklerimizi kendi sınıfımızda kullanabiliyoruz.  Şimdi Mudur isimli sınıfımızın neler yapabildiğine bir bakalım:

![Mudur_class](https://user-images.githubusercontent.com/59376910/153711711-3483f007-163b-49d7-a4d5-4cc6f04da463.png)

Görüldüğü gibi Mudur sınıfında herhangi bir öznitelik veya metot tanımlamadan miras aldığımız sınıfın özniteliklerini ve metotlarını kullanabiliyoruz.

Nesne tabanlı programlamanın en önemli konularından biri miras almadır. Kalıtım (miras alma) bizi kod tekrarından kurtarır ve kod okunabilirliğini iyileştirir. Peki miras aldığımız sınıfı değil de kendi sınıfımızın yapıcı fonksiyonunu tanımlayabilir miyiz? Evet tanımlayabiliriz. Paki nasıl? Hemen bir kod örneği ile açıklamaya çalışalım:

![MUDUR1](https://user-images.githubusercontent.com/59376910/153711731-783c8069-8848-4c40-bc44-47a862634621.png)

Yukardıki kodlarda olduğu gibi kendi yapıcı fonksiyonumuzu tanımladık ve ek __init__ fonksiyonumuza ek olarak personeller değişkenini parametre olarak atadık. Dikkat ettiyseni super adlı bir fonksiyon ile yapıcı fonksiyonumuz altında bir init fonksiyonu daha tanımladık. Bunu yapmamızın nedeni, kendi init fonksiyonumuzu tanımladığımızda derleyici artık içinde bulunduğumuz sınıfın (child class) __init__ fonksiyonunun içine bakacak. Yani biz ya burada kendi __init__ fonksiyonumuza atadığımız parametreleri yeniden miras aldığımız sınıftaki gibi tanımlayacağız ya da miras aldığımız sınıfta olan parametreleri hazır alıp, sadece ek olarak atadığımız parametreleri self parametresi ile tanımlarız. Biz burada mantıklı olan ikinci yöntemi kullandık. Yani burada aslında super() fonksiyonu miras aldığımız Personel sınıfını temsil ediyor. super() fonksiyonunun kullanımı da kodlarda gözüktüğü gibi super() deyip nokta erisim belirteci kullanarak miras aldığımız sınıfın __init__ fonksiyonunun aynısını buraya geçirmek olacaktır. super() fonksiyonunun miras aldığımız sınıfı temsil ettiğini unutmayalım. Dikkat ettiyseniz kendi sınıfımızda oluşturduğumuz __init__ fonksiyonu ile super() fonksiyonu ile çağırdığımız __init__ fonksiyonunun parametreleri aynı sırada yazılmış. Bu önemli bir ayrıntıdır. Nesne tabanlı programlamada bir sınıfı miras almışsak, nesne oluştururken miras almış olduğumuz sınıfı aynen tanımlayabilmemiz gerekir. Bu yüzden kendi __init__ fonksiyonlarınızı oluştururken miras aldığınız sınıftaki __init__fonksiyonunun yapısını bozmadan oluşturmanız gerekecektir. Yukarıdaki kodlarda personeller parametresine None değerini atamamızın temel nedir budur. Eğer None değerini atamasaydık bu sınıftan bir nesne oluşturduğumuzda miras aldığımız sınıftan nesne oluşturuyormuş gibi nesne oluşturamazdık. Burada super() fonksiyonu kullanırken self parametresini atamamıza gerek yok. Tabi alternatif olarak super() fonksiyonu yerine miras aldığınız sınıfın ismini kullanarak da __init__ fonksiyonunu çağırabilirsiniz. Eğer bu yolu seçerseniz bu sefer self parametresini kullanmanız gerekecektir. Sözün özü bir burada personel fonksiyonumuzun __init__ fonksiyonunu super() fonksiyonu sayesinde çağırdık ve kendi __init__ fonksiyonumuza atadığımız parametreleri arguman olarak da miras aldığımız sınıfın __init__ fonksiyonuna atadık. Bu şekilde isim soyisim ve maas bilgilerini yeniden tanımlamamıza gerek kalmadı, sadece ek olarak personeller değişkenini tanımlamamız gerekti. Şimdi Mudur sınıfımızından nesne oluşturalım:

![mudur_nesnesi](https://user-images.githubusercontent.com/59376910/153711749-f60f02a1-6ab8-43cf-ba36-21c0cf821be2.png)

Görüldüğü gibi Mudur sınıfını Personel sınıfı gibi kullanabiliyoruz. Şimdi de ek varsayılan değerini None olarak atadığımız personeller parametresine bir değer girelim ve bunu ekrana yazdıralım:

Yukarıdaki örnekte de görüldüğü üzere md1 nesnesine Personel sınıfından farklı olarak Mudur sınıfına bir personel listesi atadık. Buradaki kritik nokta, Mudur sınıfını tanımlarken önceki örnekte olduğu gibi aynı zamanda Personel sınıfını tanımladığımız gibi de tanımlamamız gerekecektir, yani bu örneğimiz bahsettiğimiz kurala uymaktadır. Bu yüzden bir sınıfı kalıtım yoluyla miras alırken miras alınan sınıfı aynen kullanabilmemiz gerektiğinin farkında olmak önemlidir.

# Python'da Override

![MUDUR1 (2)](https://user-images.githubusercontent.com/59376910/153711828-aa6273fd-2538-48f5-8670-b5ed74e17c7d.png)

Pyhton'da override işlemini anlamak için önce override kelimesinin anlamını bilmek konunun daha iyi anlaşılmasını sağlayacaktır. Override kelimesinin Türkçe karşılığı; geçersiz kılmak, üst üste binmek, ağır basmak, hükümsüz kılmak gibi anlamlara sahip. Nesne tabanlı programlama yaperken ve bir sınıfı kalıtım yoluyla miras alırken bazen miras aldığımız sınıf fonksiyonlarını veya özniteliklerini değiştirerek yeniden tanımlamamız gerekebilir. Biz bu işleme overriding adını veriyoruz. Python'da override etmek istediğimiz fonksiyonun ismini aynen yazarak tanımlamamız yeterli olacaktır. Fakat burada da önceden nesne tanımlarken bahsettiğimiz kurallar burada da ayen geçerli, yeniden tanımladığımız fonksiyon veya özellikler miras alınan sınıf gibi kullanılabilmesi gerekir. Aslında yukarıdaki Mudur sınıfına baktığnız zaman biz zam_orani değişkenini override etmişiz. Biz Mudur sınıfından bir nesne oluşturduğumuzda zam_orani değişkeninin değeri Personel sınıfındaki oran (1.05) değil 1.2 olarak güncellenecektir. Şimdi bir Personel ve bir Mudur nesnesi oluşturup bu nesnelere zam yapıp farkı görelim:

![override](https://user-images.githubusercontent.com/59376910/153711836-5f2c0551-5611-486a-9938-0cd62d8a912d.png)

Gördüğünüz üzere Mudur sınıfı ile oluşturduğumuz nesnenin zam oranı 1.2 olarak güncellenmiş. Bu nesneden zam_yap fonksiyonunu çağırdığımızda zam_yap fonksiyonu yeni zam oranı üzerinden zam uygulayacaktır, zira yukarıdaki örnekte de bunu görebiliyoruz. Her iki nesneye de 10000 birim maaş vermemize rağmen farklı oranlarda zam uygulanmış. Buna override denir.

# Kapsülleme (Encapsulation)
Kapsülleme, nesne tabanlı programlamada özniteliklere sınıf dışından kontrollü erişim sağlanmasını sağlar, yani getter ve setter fonksiyon mantığını kullanarak verilerimizi kontrol altına alıyoruz. Hatırlarsanız kalıtım konusunu anlatırken Personel adında bir sınıfımız vardı. O sınıfa geri dönelim ve kapsüllemeyi onun üzerinden anlatalım:

![personel (1)](https://user-images.githubusercontent.com/59376910/153712095-01c5f60c-cfb4-4157-9d00-40975e142bcc.png)

Dikkat ettiyseniz zam_orani değişkeni sınıf özniteliği olarak tanımlanmış. Bu özniteliğe sınıf dışından erişim sağlayabilir, manipüle edebiliriz. Şimdi biz sınıf dışından zam_orani özniteğini manipüle etmeye çalışalım:

![personel_sinifi_son](https://user-images.githubusercontent.com/59376910/153712104-095ddafe-3369-44e4-88c9-7597e3706c15.png)

Yukarıda tanımladığımız per1 nesnesine ait zam oranını değiştirerek zam yaptık, yani zam oranını manipüle ettik. Burada zam_orani özniteliğine negatif değer de verebilirdik. Bu durum bizim için bir sorun teşkil edecektir, çünkü zam oranı herkesin erişebileceği ve istediği gibi değerini değiştirebildiği bir öznitelik olmaması gerekiyor.  Erişilse bile kontrollü olarak getter ve setter fonksiyon mantığı ile dolaylı olarak erişilmesi gerekir. Bu durumda yapmamız gereken şey zam oranını kapsüllemek olacaktır. Python'da gizlemek (private) istediğimiz özniteliklerin önüne iki tane alt çizgi ekliyoruz. Bu şekilde özniteliklerimize dışarıdan erişilip müdahele dilmesini önlemiş oluyoruz. Hemen bir örnekle zam_orani özniteliğimize sınıf dışından erişilmesini engelleyelim:

![zam_orani_kapsulleme](https://user-images.githubusercontent.com/59376910/153712120-d342eeb7-cfe2-49c2-ad5b-baefc9866125.png)

Yukarıda da göründüğü gibi zam_orani özniteliğimizin önüne iki tane alt çizgi ekleyerek onu private hale getirdik. Şimdi bu özniteliğimize sınıf dışından erişmeye çalışalım:

![personel_zam_oranina_erisim](https://user-images.githubusercontent.com/59376910/153712136-7611e727-e9e5-4873-ae52-565e5e7a6d5a.png)

Görüldüğü üzere Personel sınıfımızdaki __zam_orani özniteliğine sınıf dışından erişmek istediğimizde bize hata veriyor. Bu özniteliğe kontrollü erişmek istersek getter setter fonksiyon mantığını burada kullanabiliriz. Şimdi özniteliğimize kontrollü erişebilmek ve değerini değiştirebilmek için iki tane fonksiyon tanımlayalım:

![getter_setter_fonksiyonlari](https://user-images.githubusercontent.com/59376910/153712146-d69ab9b0-7c8b-4dff-b9d0-d943cb2252bc.png)

Burada get_zam_orani fonksiyonu sayesinde __zam_orani özniteliğine sınıf dışından dolaylı olarak erişim sağlayabiliyoruz. set_zam_orani fonksiyonu sayesinde de __zam_orani özniteliğimizin değerini kontrollü olarak değiştirebiliyoruz.  Bu fonksiyona yeniOran parametresini float tipinde yollayarak değerin 0 dan büyük 2 den küçük olmasını zorunlu kıldık. Aynı zamanda try except yapısından yararlanarak veri sayı olarak atanması gereken argümanın farklı bir veri tipi gelmesi durumda kullanıcıya uyarıda bulunarak değer atama işleminin gerçekleşmesini engelliyoruz. Şimdi get_zam_orani fonksiyonunu kullanarak private durumundaki __zam_orani özniteliğimize erişmeye çalışalım:

![personel_private](https://user-images.githubusercontent.com/59376910/153712164-38237d75-0135-4733-b57a-b0955831f2ce.png)

Gördüğünüz gibi get_zam_orani fonksiyonu sayesinde private halindeki __zam_orani özniteliğimize dolaylı olarak (fonksiyon yardımıyla) erişebildik. Şimdi de set fonksiyonumuzu kullanarak __zam_orani özniteliğimize yeni değer atayalım:

![set_zam_orani](https://user-images.githubusercontent.com/59376910/153712172-255b9cee-5d6c-4a3b-aaa4-b3fcadaa2d4f.png)

Burada da set_zam_orani fonksiyonunu kullanarak kontrollü olarak değer atadık. Şimdi sayı yerine string değer atamayı deneyelim:

![set_zam_orani2](https://user-images.githubusercontent.com/59376910/153712181-4dda8440-cf4e-41f3-91e0-ca08625f217c.png)

Gördüğünüz set_zam_orani fonksiyonuna string değer atamak istediğimizde try catch yapısı devreye giriyor ve TypeError hatası fırlatıyor. Yeni değer oranına dikkat ederseni yeni zam oranının değişmediğini görürsünüz. Bu şekilde özniteliğimizi kontrol altına almış durumdayız gibi görünüyor. Peki değer sayı olup negatif olsa ne olur? Hemen görelim?

![set](https://user-images.githubusercontent.com/59376910/153712195-0e013782-9ffa-46aa-9805-17d25c0fb1e5.png)

Gördüğünüz gibi burada da oran değişmedi, çünkü set_zam_orani fonksiyonu içinde if else yapısı sayesinde yalnızca pozitif değer geldiğinde yeni değerin atanmasını sağlıyoruz. Eğer 2 den büyük değer verilirse de aynı şekilde değeri değiştirmeyecektir. Kapsülleme işlemini tıpkı özniteliklerde kullanıldığı gibi fonksiyonlarda da kullanılabilir.
