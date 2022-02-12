# Python Nesne Tabanlı Programlama

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
