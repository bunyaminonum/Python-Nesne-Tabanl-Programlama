# Python Nesne Tabanlı Programlama

### Nesne Tabanlı Programlama (OOP) Nedir?

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

## Tekrar Kullanılabilirlik (Reusability)
Tekrar kullanılabilirlik (Reusability),  adından da anlışalacağı üzere bir kez yazılmış kodlar gerektiğinde yeniden yazmadan tekrar tekrar kullanılabilir ve bunu OOP'nin bir yapısı olarak bir sınıf (class) içerisinde kullanıldığında diğer programcıların da kodumuzu kullanabilir hale getirebiliyoruz.  Örneğin bir araba üreticisini düşünün, bu araba üreticisi ürettiği ilk aracın özelliklerini yeniden keşfetmek yerine yeni model araçlara entegre edip bu araçlara ek özellik ekleyebilir.  Tekrar kullanılabilirlik (reusability) kavramını inheritance (kalıtım)  konusunu anlatırken daha iyi anlaycaksınız.

## Genişleyebilirlik (Extensibility)
Genişleyebilirlik (Extensibility),  adından da anlaşılacağı üzere kodlarımıza kolayca yeni kodlar ekleyip genişletmemize olanak tanır.  Tekrar bir araba üreticisini düşünelim, bu üreticinin A1 model bir araba ürettiğini düşünelim. Bu araç modelinde silecekler açık döngü kontrol sistemine sahip, yani sadece insan müdahelesiyle açılıp kapanıyor. Üretici bir zaman sonra A2 modelinde yeni bir araç üretiyor ve bu araçta sileceklerler bir sensör yoluyla yağmur yağdığında otomatik olarak çalışabilmesini sağlamak istiyor.  İşte tam burada OOP'nin genişleyebilirlik özelliği sayesinde sileceklere bu özellik kolayca eklenerek silecekler, isteğe bağlı olarak otomatik veya manuel olarak çalıştırılabilir. 

## Sürdürülebilirlik (Maintainability)
Sürdürülebilirlik (Maintainability), bir yazılımın kolayca değiştirilebilir, kullanıcı dostu ve hızlı olmasıyla ilgilenir. Tam olarak aynı işlevselliğe sahip iki farklı yazılım sistemi düşünün. Aynı girdi verildiğinde, her ikisi de tam olarak aynı çıktıyı hesaplar. Bu iki sistemden biri hızlı ve kullanıcı dostudur aynı zamanda kaynak kodunun değiştirilmesi kolaydır. Diğer sistem ise yavaş, kullanımı zor ve kaynak kodunun değiştirilmesini bırakın anlaşılması bile neredeyse imkansızdır. Her iki sistem de aynı işlevselliğe sahip olsa da, kaliteleri farklıdır.  Bir sistemin hızlı, kullanıcı dostu ve kaynak kodunun kolayca değiştirilmesi tam olarak nesne tabanlı programlamayı ifade etmektedir. On binlerce kodun aynı kod parçasının altında birleştiğini düşünün ve bir de bu kod parçalarının sınıflara parçalandığını, her bir sınıfın hangi görevi üstlendiğini bildiğinizi düşünün. Hangisini seçerdiniz? Tahmin edildiği gibi sınıflara ayrılan kod sistemini seçtiniz çünkü bu sınıflara erişmek ve değiştirmek istdiğinizde bunu kolayca yapabiliyorsunuz. İşte bu yapıya OOP'nin Sürdürülebilirliği dioruz.

# Python Class Yapısı
