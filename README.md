# Kodun Açıklaması:
Verilen kod önce rastgele bir dizi oluşturur, sonra bu oluşturulan diziyi sıralar ve matrisleri yazdırarak işlemler yapar. 
generate fonksiyonu, (A_SIZE) boyutundaki bir diziyi -MAX_W ile MAX_W arasındaki sayılarla rastgele random olarak oluşturur. 
function1 fonksiyonu, verilen diziyi BubbleSort algoritması ile sıralar.
function2 fonksiyonu, verilen dizideki pozitif ardışık toplamların ortalamasını hesaplar. İlk adımda, bir geçici değişken olan t ve ardışık toplamları takip eden bir geçici değişken olan current_sum tanımlanır. Ardından, dizinin her elemanı üzerinde dolaşılır. Eğer current_sum ve elemanın toplamı 0'dan büyükse, current_sum güncellenir. Aksi takdirde, current_sum sıfırlanır. Her güncelleme sırasında, t değeri en büyük ardışık toplama karşılık gelir. Son olarak, ardışık toplamların sayısı count ile takip edilir ve t değeri count ile bölünerek ortalaması hesaplanır.
function3 fonksiyonu, verilen ağırlık matrisi (g) üzerinde Floyd-Warshall algoritmasını kullanarak iki düğüm arasındaki en kısa yol uzunluklarını hesaplar. İlk adımda, g matrisi d matrisine kopyalanır. Ardından, her iki düğüm arasındaki ağırlık matrisi kontrol edilir. Eğer iki düğüm arasında doğrudan bir bağlantı varsa, ilgili değer kopyalanır. Aksi takdirde, sonsuz (INF) olarak işaretlenir. Ardından, Floyd-Warshall algoritması kullanılarak tüm düğümler arasındaki en kısa yol uzunlukları hesaplanır.
print fonksiyonları elde edilen sonuçları ekrana yazdırmak için kullanılır.

# Verilen Kodun Zaman Karmaşıklığı Hesabı:

Size değerini ‘n’ olarak alırsak eğer;
generate fonksiyonu: Bu fonksiyon, bir diziyi rastgele sayılarla dolduruyor. Her elemanı doldurmak için bir döngü kullanıldığından zaman karmaşıklığı O(n) olacaktır.
function1 fonksiyonu: Bu fonksiyon, BubbleSort Algoritması ile bir diziyi sıralıyor. İki iç içe for döngüsü kullanıldığı için, dizinin boyutu olan size kadar tekrarlanacak ve bu nedenle zaman karmaşıklığı O(n^2) olacaktır.
function2 fonksiyonu: Bu fonksiyon, bir dizideki ardışık en büyük toplamı buluyor. Tek bir for döngüsü kullanıldığı için, dizi boyutuna bağlı olarak doğrusal bir zaman karmaşıklığına sahiptir. Bu nedenle zaman karmaşıklığı O(n) olacaktır.
function3 fonksiyonu: Bu fonksiyon, Floyd-Warshall algoritmasını kullanarak bir graf matrisinin tüm en kısa yol değerlerini hesaplıyor. İki iç içe for döngüsü ve bir while döngüsü kullanıldığından, graf matrisinin boyutuna bağlı olarak zaman karmaşıklığı O(n^3) olacaktır.
print1 fonksiyonu: Bu fonksiyon, bir diziyi ekrana yazdırıyor. Tek bir for döngüsü kullanıldığı için zaman karmaşıklığı O(n) olacaktır.
print2 fonksiyonu: Bu fonksiyon, iki boyutlu bir matrisi ekrana yazdırıyor. İki iç içe for döngüsü kullanıldığı için, matrisin boyutu olan size kadar tekrarlandığı için zaman karmaşıklığı O(n^2) olacaktır.
print3 fonksiyonu: Bu fonksiyon, iki boyutlu bir matris üzerinde işlem yaparak belirli bir değerden küçük olan değerleri ekrana yazdırıyor. İki iç içe for döngüsü kullanıldığı için, matrisin boyutu olan size kadar tekrarlandığı için zaman karmaşıklığı O(n^2) olacaktır.
Toplam zaman karmaşıklığını hesaplamak için her fonksiyonun karmaşıklığını toplamamız gerekiyor:
O(n) + O(n^2) + O(n) + O(n^3) + O(n) + O(n^2) + O(n^2) = O(n^3)
Sonuç olarak, bu kodun zaman karmaşıklığı O(n^3) şeklindedir.

# Verilen Kodu Geliştirmek İçin Ne Yapılabilir:
-function1 de BubbleSort yerine QuickSort algoritması kullandık.
-function2 de count değeri, pozitif olan elemanların sayısını takip ederek her pozitif indeksin üzerinde count değerini arttırır. Bu şekilde, count değişkenini ayrı bir döngü içinde hesaplamamız gerekmez. Ayrıca, t/count ifadesini döngü dışında hesaplar ve sonucu döneriz. Pozitif eleman yoksa, 0 değerini döneriz.

# Geliştirilmiş kodun Zaman Analizi:
size değerini n olarak alırsak eğer:
generate fonksiyonu: Bu fonksiyon, bir diziyi rastgele sayılarla dolduruyor. Boyutu size olan bir diziyi oluşturuyoruz ve her elemana bir rastgele sayı atıyoruz. Bu işlem, dizinin boyutu olan size kadar tekrarlandığı için zaman karmaşıklığı O(n)'tır.
quickSort fonksiyonu: Bu fonksiyon, hızlı sıralama algoritmasını kullanarak bir diziyi sıralıyor. Sıralama işlemi, dizinin boyutu olan size kadar tekrarlandığı için zaman karmaşıklığı O(n*log(n))'dir.
partition fonksiyonu: Bu fonksiyon, hızlı sıralama algoritmasında kullanılan bölütleme işlemini gerçekleştiriyor. Bu işlem, dizinin boyutu olan size kadar tekrarlandığı için zaman karmaşıklığı O(n)'tır.
function1 fonksiyonu: Bu fonksiyon, quickSort fonksiyonunu çağırarak bir diziyi sıralıyor. quickSort fonksiyonunun zaman karmaşıklığı O(nlog(n)) olduğundan, function1 fonksiyonunun zaman karmaşıklığı da O(nlog(n))'dir.
function2 fonksiyonu: Bu fonksiyon, bir dizideki sayıları işleyerek bir tamsayı değeri döndürüyor. Bu fonksiyonun zaman karmaşıklığı O(n)'dır çünkü for döngüsü, dizinin boyutu olan size kadar tekrarlanıyor.
function3 fonksiyonu: Bu fonksiyon, iki boyutlu bir matris üzerinde işlem yaparak matrisi güncelliyor. İlk iç içe for döngüsü, matrisin boyutu olan size kadar tekrarlandığı için O(n^2) zaman karmaşıklığına sahiptir. İkinci iç içe for döngüsü de matrisin boyutu olan size kadar tekrarlandığı için O(n^2) zaman karmaşıklığına sahiptir. Üçüncü iç içe for döngüsü de matrisin boyutu olan size kadar tekrarlandığı için O(n^2) zaman karmaşıklığına sahiptir. Bu nedenle, function3 fonksiyonunun toplam zaman karmaşıklığı O(n^3)'tür.
print1 fonksiyonu: Bu fonksiyon, bir diziyi ekrana yazdırıyor. for döngüsü, dizinin boyutu olan size kadar tekrarlandığı için zaman karmaşıklığı O(n)'tır.
print2 fonksiyonu: Bu fonksiyon, iki boyutlu özdeğişkeni ekrana yazdırıyor. İç içe iki for döngüsü, matrisin boyutu olan size kadar tekrarlandığı için zaman karmaşıklığı O(n^2)'dir.
print3 fonksiyonu: Bu fonksiyon, iki boyutlu bir matris üzerinde işlem yaparak belirli bir değerden küçük olan değerleri ekrana yazdırıyor. İki iç içe for döngüsü, matrisin boyutu olan size kadar tekrarlandığı için zaman karmaşıklığı O(n^2)'dir.
Toplam zaman karmaşıklığını hesaplamak için her işlevin karmaşıklığını toplamamız gerekiyor:
O(n) + O(n*log(n)) + O(n) + O(n^3) + O(n) + O(n^2) + O(n^2) = O(n^3)
Sonuç olarak, bu kodun zaman karmaşıklığı O(n^3) şeklindedir.
