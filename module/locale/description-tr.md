# Improved Siegeengines

**Sürüm**: 1.0.29

Değiştirilmemiş oyunda yapay zekânın kuşatma araçları kendini heba eder: mancınıklar uzaktan vurabilecekleri surun dibine kadar sürer, uzun oyunlarda kuşatma çadırları trebuşelerin yetişemeyeceği kadar uzaklaşır, kuşatma kuleleri uygun sur bekleyip boş durur ve taşınabilir kalkanlar geyiklerin peşinden gider. Bu modül bunların her birini düzeltir.

Aşağıdaki her özellik tek tek açılıp kapatılabilir. Kuşatma kulelerinin yanaşması ve yolcu taşıması ile yağ mühendisleri oyuncuya da yarar sağlarken diğer değişiklikler yapay zekâ kuşatma araçlarını kapsar.

## Neler yapar

**Mancınıklar ve trebuşeler kendi hedeflerini seçer.** Yapay zekâ mancınığı veya trebuşesi tam menzili içinde her yöne bakarak en yakın düşman surunu, kulesini veya kapı binasını durduğu yerden vurur. Sivil binalar yalnızca menzilde tahkimat kalmadığında hedef alınır; yalnızca menzilde hiçbir şey yoksa yaklaşır. (Oyunun kendi araması tek yöne bakıp hasarlı surları yok sayıyordu.)

**Yolda durup ateş ederler.** Oyun yalnızca araç dururken hedef aradığından hareket hâlindeki yapay zekâ mancınıkları menzilindeki hedeflerin yanından geçip gidiyordu. Artık yürüyen mancınık ve trebuşeler sık sık etrafına bakar ve menzile giren ilk düşman suru, kulesi, kapı binası veya binasında durup ateş eder.

**Sonraki rakibe geçer.** Bir mancınık veya trebuşe yalnızca ordusunun gönderildiği oyuncuya nişan alır. O oyuncu yenilince (lordu ölünce) boş durmak yerine menzildeki başka bir düşmana ateş eder.

**Menzildeki diğer düşmanlar.** Kuşatılan oyuncudan menzilde hedef yoksa mancınık veya trebuşe diğer düşmanların surlarına ve binalarına ateş eder. Kuşatılan oyuncunun hedefleri önceliklidir; yıkılmış binalar asla hedeflenmez.

**Artık harabelere ateş edilmez.** Bir binaya nişan alan araç (ateş balistası veya mancınık), bina yıkıldıktan sonra boş yere ateş etmeyi sürdürüyordu. Artık yıkılan hedef bırakılır ve yeni hedef seçilir; ateş balistaları da dâhildir.

**Daha iyi nişan.** Oyun yapay zekâ mancınık taşlarının 12 kare kısa ve 6 kare yana düşmesine izin verir. Sapma artık yarıya indirilir ve hedefe ortalanır (ayarlanabilir; %100 oyunun nişanını korur). Kendi araçların değişmez.

**Çadır noktaları yeniden kullanılır.** O noktada inşa eden birlik gittikten, yer boşaldıktan ve yakın tehdit kalmadıktan sonra yapay zekâ oraya yeniden çadır kurabilir. Oyunun orijinalinde nokta maç sonuna dek kilitli kalıyordu.

**Menzilli araç çadırları menzile göre konur.** Mancınık, trebuşe ve ateş balistası çadırları düşman sur, kule ve kapı binalarından menzilin 0–10 kare (ayarlanabilir) içine yerleştirilir; böylece kalenin içini de vurabilirler.

**Mühendisler çadırlarına hep ulaşır.** Kapalı çadır girişi boş kenara taşınır; vazgeçen veya takılan mühendisler yeniden gönderilir, yakındaki boş mühendisler destek olur. Tamamen çevrili çadır yol açılır açılmaz mühendislerini alır.

**Kuşatma kuleleri daha fazla sura yanaşır.** Oyun yer bulamazsa kule köşesiyle çapraz sura veya aynı surda üç kare öteye yanaşır.

**Yapay zekâ kuşatma kuleleri kendi surunu bulur.** Boştaki yapay zekâ kulesi 100 kare içindeki en yakın yanaşılabilir sura gider; bulamaz veya ilerleyemezse bir sur erişilebilir olana dek devriye, kuşatma koruması, ana ordu, rastgele menzilli birlik veya yedeklerle büyük bir kalkan gibi yürür.

**Piyadeler kuşatma kulelerine biner.** Piyadeleri seçip kulene tıkla: en fazla 9 asker tepeye çıkar, okçular giderken bile ateş eder ve yanaşmış kule koruması alır. Giderken seçilemezler; kuleyle ölür ya da yanaşınca üstünde kalırlar. Kuleye tıklayınca ilk tık yolcuları, ikinci tık mühendisleri indirir. Yapay zekâ kuleleri 3 kare içindeki kendi menzilli birliklerini alır.

**Kalkanlar kendi birlikleriyle yürür.** Yapay zekâ kalkanları hendek dolduranlara, saldırı ordusunun menzilli araçlarına (evdekilere değil) ve menzilli birliklerine eşit dağılır. Yedekler ancak bunlar kalmazsa alır; kimse yoksa kalkan bekler.

**Yağ mühendisleri yalnızca zemine döker.** Mühendisler — seninkiler de — yağı yalnızca yanabileceği açık zemine döker, asla sur, merdiven veya kuleye değil. Kendi başlarına yalnızca zemindeki düşmanlara dökerler; uygunsuz noktaya gönderilirlerse 45 derece içindeki en yakın zemine döker veya «olanaksız konum» diyerek yağını saklarlar.

**Yağ miktarına göre yayılır.** Bir kazanın yağı nişan noktasından başlayarak belirli sayıda kareye (varsayılan 41) yayılır. Açık zeminde oyunla aynıdır; dar geçitlerde ardışık kazanlar gibi uzar. Yanabilir binalar (kulübeden cephanelik, kilise ve katedrale) canlarının üçte birine kadar hasar alır; surlar, kuleler, kapı binaları ve iç kaleler zarar görmez.

## Bilmeniz gerekenler

* Çok oyunculuda herkesin bu modülü aynı ayarlarla kullanması gerekir.
* Kayıt dosyalarına hiçbir şey kaydedilmez.
