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
