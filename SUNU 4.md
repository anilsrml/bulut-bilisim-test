# **Bulut Destekleyici** **Teknolojiler**


## **Bulut Destekleyici Teknolojiler**

###### **1. Ağlar ve İnternet Mimarisi** **2. Bulut Veri Merkezi Teknolojisi** 3. Modern Sanallaştırma 4. Çoklu Kiracılık Teknolojisi 5. Hizmet Teknolojisi ve Hizmet API’leri 6. Vaka Analizi Örneği


## **1. AĞLAR VE İNTERNET MİMARİSİ**


- **Tüm bulutlar bir ağa bağlı olmalıdır.**

- Bulut tüketicileri, çoğu bulut internete bağlı olmasına
rağmen, yalnızca **LAN** 'lardaki **özel** **ve** **adanmış** **ağ**
**bağlantılarını** **kullanarak** **buluta** **erişme** **seçeneğine**
**sahiptir.**

- Bu nedenle bulut platformlarının potansiyeli **genellikle**
**internet bağlantısı ve hizmet kalitesindeki** gelişmelerle
**paralel olarak artar.**


- İSS'ler tarafından kurulan ve
dağıtılan internetin en büyük
omurga ağları, **dünyanın** **çok**
**uluslu** **ağlarını** **birbirine**
**bağlayan** **çekirdek**
**yönlendiriciler** tarafından
**stratejik** **olarak** **birbirine**
**bağlanır.**

- Bu nedenle bulut
platformlarının potansiyeli
**genellikle** **internet** **bağlantısı**
**ve** **hizmet** **kalitesindeki**
gelişmelerle **paralel** **olarak**
**artar.**


###### **İnternet Servis Sağlayıcıları (İSS'ler)**


- **İnternetin** **topolojisi,** **çekirdek**
**protokolleri** **aracılığıyla** birbirine yüksek
oranda bağlı olan İSS'lerin **dinamik** ve
**karmaşık** bir toplamı haline geldi.

- İnternet ve İSS ağlarının iletişim
bağlantıları ve yönlendiricileri, **sayısız**
**trafik** **üretim** **yoluna** **dağıtılmış** BT
kaynaklarıdır.

- **İnternet** **ağı** **mimarisini** **oluşturmak** için
kullanılan **iki** **temel** **bileşen**, **bağlantısız**
**paket** **anahtarlama** (datagram ağları) ve
**yönlendirici tabanlı** bağlantıdır.



**Şekil:** İnternetin ağ yapısının bir
soyutlaması


###### **Bağlantısız Paket Anahtarlama (Datagram Ağları)** • Veri akışları, sınırlı boyutlardaki paketlere bölünerek ağ anahtarları (switch) ve yönlendiriciler (router) aracılığıyla işlenir, kuyruklanır ve bir ara düğümden (node) diğerine **iletilir.** • Her paket, İnternet Protokolü (IP) veya Medya Erişim Kontrolü (MAC) adresi gibi gerekli konum **bilgilerini taşır ve bu bilgiler sayesinde kaynak,** **ara ve hedef düğümlerde işlenerek yönlendirilir.**


###### **Yönlendirici Tabanlı Bağlantılılık (Router-Based Bağlantı)**

- **Yönlendirici,** paketleri ilettiği birden
**fazla ağa bağlı bir cihazdır.**

- Ardışık paketler aynı veri akışının bir
parçası olsa bile, yönlendiriciler her
paketi ayrı ayrı işler ve iletirken, kaynak
ve hedef düğümler arasındaki iletişim
yolunda bir **sonraki düğümü bulan ağ**
**topolojisi bilgilerini korur.**

- **Yönlendiriciler,** **ağ trafiğini yönetir** ve
**hem paket kaynağına** hem de **paket**
**hedefine özel oldukları** için **paket**
**teslimi için en verimli atlamayı ölçer.**


**İnternet Referans Modeli ve Protokol Yığınına Genel Bakış (TCP/IP**
**Modeli)**


###### **Fiziksel Ağ**

IP paketleri, Ethernet, ATM ağı ve 3G mobil HSDPA gibi bitişik
düğümleri bağlayan fiziksel ağlar üzerinden iletilir.
**Fiziksel ağlar iki temel bileşenden oluşur:**

- **Veri Bağlantı Katmanı (Data Link Layer):** Komşu düğümler
arasındaki **veri transferini kontrol eder.**

- **Fiziksel Katman (Physical Layer):** Verileri kablolu veya
kablosuz ortamlar üzerinden **bit düzeyinde iletir.**


###### **İnternet Katmanı**

❖ Bu katmanda **hedef** veya **kaynak IP adresleri** veriye

eklenerek verinin hangi bilgisayara gönderileceği belirlenir
ve gönderilen paket Veri Bloğu (Datagram) halini alır.


###### **Taşıma Katmanı (Transport Layer Protocol)**

❖ **İletim Kontrol Protokolü (TCP)** ve **Kullanıcı Datagram**

**Protokolü (UDP)** gibi taşıma katmanı protokolleri, **IP’yi**
**kullanarak** **uçtan uca standart iletişim desteği sağlar.**
❖ **Bu** **protokoller**, internet üzerinde veri paketlerinin
yönlendirilmesini ve aktarılmasını kolaylaştırır.


**Uygulama Katmanı Protokolü (Application Layer Protocol)**


❖ **HTTP** (web), **SMTP** (e-posta), **BitTorrent** (P2P) ve **SIP** (IP telefon) gibi

protokoller, **taşıma katmanı protokollerini kullanarak** internet
üzerinden **belirli veri aktarım yöntemlerini standart hale getirir.**
❖ Diğer birçok protokol, uygulamaya özgü gereksinimleri karşılamak

için **TCP/IP veya UDP'yi** temel veri aktarım yöntemi olarak kullanır.
❖ Bu protokoller **hem internet hem de yerel ağlarda** (LAN) **veri**

**iletimi** için yaygın olarak kullanılmaktadır.


##### **Teknik ve İşletme Açısından Değerlendirmeler**

❖ **Bağlantı Sorunları (Connectivity Issues)**
Geleneksel şirket içi (on-premises) dağıtım modellerinde, **kurumsal**
**uygulamalar ve çeşitli BT çözümleri** genellikle kuruluşun kendi veri
merkezinde bulunan **merkezi sunucular** ve **depolama cihazları**
üzerinde barındırılır.


###### **Ağ Bant Genişliği ve Gecikme Sorunları (Network** **Bandwidth and Latency Issues)**


- **Ağları** **İSS** 'lere bağlayan **veri bağlantısının** **bant genişliğinden**
**etkilenmenin** yanı sıra, **uçtan uca bant genişliği aracı düğümleri**
bağlayan paylaşılan **veri bağlantılarının iletim kapasitesi**
tarafından belirlenir.

- **Zaman gecikmesi** olarak da adlandırılan **gecikme**, bir paketin bir
**veri düğümünden diğerine gitmesinin aldığı süredir.**

- **Ağlar,** paylaşılan düğümlerdeki **trafik koşullarına bağlıdır** ve bu
da **internet gecikmesini oldukça değişken** ve **genellikle tahmin**
**edilemez hale getirir.**


**Ağ Bant Genişliği ve Gecikme Sorunları (Network Bandwidth**
**and Latency Issues)**


- "En iyi çaba" **hizmet kalitesine (QoS)** sahip **paket ağları**,
genellikle **paketleri ilk gelen/ilk hizmet** esasına göre iletir.

- **BT çözümlerinin,** **bulut bağlantısının doğasında bulunan** **ağ**
**bant genişliği** ve **gecikmeden etkilenen iş gereksinimlerine**
göre değerlendirilmesi gerekir.

- **Bant genişliği**, **buluta ve buluttan önemli miktarda** **veri**
**aktarılması** gereken uygulamalar için **kritik öneme sahipken**
**gecikme**, **hızlı yanıt süreleri** gibi **bir iş gereksinimi** olan
uygulamalar için **kritik öneme sahiptir.**


###### **Kablosuz ve Hücresel (Wireless and Cellular)**


- Herhangi bir cihazdan, özellikle **mobil istemcilere** ve
**tüketicilere** yönelik olanlardan, **her yerden erişilebilir**
**olması** gereken **bulut tabanlı çözümlere,** **kablosuz** ve
**hücresel iletişim bağlantıları** aracılığıyla **erişilebilir**
**olması gerekir.**


#### **2. BULUT VERİ MERKEZİ TEKNOLOJİSİ** **(CLOUD DATA CENTER TECHNOLOGY)**


- **BT kaynaklarını coğrafi olarak dağıtılmış olmaktansa** birbirine **yakın**
**bir mesafede gruplamak**, **güç paylaşımına**, **paylaşılan BT kaynak**
**kullanımında** daha **yüksek verimliliğe** ve **BT personeli** için **daha iyi**
**erişilebilirliğe olanak tanır.**

- Bunlar, **veri merkezi konseptini doğal olarak** popülerleştiren
avantajlardır.

- **Modern** **veri** **merkezleri**, **sunucular**, **veritabanları**, **ağ** **ve**
**telekomünikasyon cihazları** ve **yazılım sistemleri** gibi merkezi BT
kaynaklarını barındırmak için kullanılan **özel BT altyapısı olarak**
**mevcuttur.**

- **Bulut sağlayıcıları** için **veri merkezleri genellikle ek teknolojiler**
**gerektirir.**


❖ **Sanallaştırma (Virtualization)**
**Veri merkezleri** **hem fiziksel** hem
de **sanallaştırılmış** **BT**
**kaynaklarından oluşur** .
**Fiziksel** **BT** **kaynak** **katmanı**,
**donanım** **sistemleri** ve **işletim**
**sistemleriyle** birlikte **bilgi işlem/ağ**
**sistemleri** ve **ekipmanlarını**
**barındıran tesis altyapısını** ifade
eder


❖ **Standardizasyon ve Modülerlik (Standardization and Modularity)**
Modülerlik ve standardizasyon

tedarik,
edinim,
dağıtım,
işletme
bakım
süreçleri için **ölçek ekonomileri sağladıkları** için **yatırım ve işletme**
**maliyetlerini azaltmak** için **temel gereksinimlerdir.**


❖ **Otonom Bilişim/Hesaplama**
Bir sistemin kendi kendini yönetme yeteneğidir.
Otonom bilgi işlem kullanılarak bulutlar, insan müdahalesi olmadan
belirli görevleri kendileri yönetecek şekilde donatılabilir.

**Öz yönetimin ortak özellikleri şunları içerebilir:**
**1.Kendi kendine yapılandırma (Self configuration):**
Yerleşik politikalara yanıt olarak kendilerini otomatik olarak
yapılandırabilir.
**2. Kendi kendine optimizasyon:**
Bulut kaynaklarının, ölçeği **dinamik** **olarak** **artırma** veya
**genişletme** gibi **çalışma** **zamanında** **yapılandırma**
**parametrelerini** **değiştirerek** **performans** **göstergelerini** sürekli
olarak **iyileştirmeye çalışır.**


❖ **Otonom Bilişim/Hesaplama**

**Öz yönetimin ortak özellikleri şunları içerebilir:**
**3. Kendi Kendini İyileştirme (Self-Healing):**
Bulut hizmetlerinin **donanım** **veya** **yazılım** **arızasından**
**kurtarabildiği**, **sorunları** önceden otomatik olarak algılamayı ve
tanılamayı sağlar.
**4. Kendi kendini koruma (Self-Protection):**
Bulut bilişim platformlarının _**kendilerini kötü niyetli saldırılara**_
veya _**kademeli arıza durumlarına**_ karşı **savunabilmesidir.**
Bu, **veri bilimi ve yapay zeka** teknolojileri ile otonom bilişim
güçlendirilmektedir.


❖ **Uzaktan Çalıştırma ve Yönetim**
Veri merkezlerindeki BT **kaynaklarının operasyonel** ve **idari**
**görevlerinin çoğu**, ağın **uzak konsolları ve yönetim sistemleri**
aracılığıyla **komuta edilir.**


❖ **Yüksek Kullanılabilirlik**

Veri merkezlerinde genellikle sistem arızası beklentisiyle  yedekli,
**kesintisiz güç kaynakları**, **kablolama** ve **çevresel kontrol** alt
sistemlerinin yanı sıra **yük dengeleme** için **iletişim bağlantıları**
ve **kümelenmiş donanım** bulunur.


###### ❖ Yüksek Erişilebilirlik (High Availability)

- Veri merkezlerinde genellikle **sistem** **arızası** **beklentisiyle** **yedekli**,
**kesintisiz** **güç** **kaynakları**, **kablolama** ve **çevresel** **kontrol** **alt**
**sistemlerinin** yanı sıra **yük** **dengeleme** için **iletişim bağlantıları** ve
**kümelenmiş donanım bulunur.**


❖ **Güvenlik Odaklı Tasarım, İşletim ve Yönetim (Security-**

**Aware Design, Operation, and Management)**

- Fiziksel ve mantıksal erişim kontrolleri ve veri kurtarma stratejileri

gibi **güvenlik gereksinimlerinin**, **iş verilerini depolayan** ve
**işleyen merkezi yapılar oldukları** için veri merkezleri için kapsamlı
olması gerekir


###### ❖ Tesisler (Facilities)

**Veri merkezi tesisleri**, **özel bilgi işlem**, **depolama ve ağ**
**ekipmanı** ile donatılmış, **özel** **olarak** **tasarlanmış**
**konumlardır** .
Bu tesisler, **ısıtma, havalandırma, iklimlendirme**,
**yangından korunma** ve diğer ilgili alt sistemleri düzenleyen
çeşitli güç kaynakları, kablolama ve çevre kontrol
istasyonlarının yanı sıra çeşitli işlevsel yerleşim alanlarına
sahiptir.
❖ **Bilgisayar Donanımı**
Veri merkezlerindeki ağır işlemlerin çoğu, genellikle önemli
bilgi işlem gücüne ve depolama kapasitesine sahip
**standartlaştırılmış ticari sunucular tarafından yürütülür.**


###### ❖ Sunucusuz Ortam

Sunucusuz bir ortam, **uygulamalar için çalışma zamanı**
**kaynaklarını otomatik** olarak sağlayan ve bunların çalışması
için **gereken temel kaynakları kurmaya gerek kalmadan**
dağıtılabilen teknolojilerden oluşur.


❖ **NoSQL Kümeleme (NoSQL**

**Clustering)**
Bir küme, **NoSQL veritabanları**
da dahil olmak **üzere çeşitli**
**bulut tabanlı çözümler** için bir
**dağıtım** **ortamı** **olarak**
**kullanılabilir.**


**Bulut Veri Merkezi Teknolojisi (Cloud Data Center Technology)**


❖ **Diğer Hususlar (Other Considerations)**

- **Performans Yükü:**
**Sanallaştırma**, **kaynak paylaşımı** ve **çoğaltma** için çok az
**kullanımla yüksek iş yüklerine sahip karmaşık sistemler** için
**ideal olmayabilir.**
**Kötü formüle edilmiş bir sanallaştırma planı**, **aşırı performans**
**yüküne neden olabilir.**


**Bulut Veri Merkezi Teknolojisi (Cloud Data Center Technology)**


❖ **Diğer Hususlar (Other Considerations)**

- **Özel Donanım Uyumluluğu:**
Özel donanım dağıtan birçok donanım satıcısının sanallaştırma yazılımıyla
uyumlu aygıt sürücüsü sürümleri **olmayabilir** .
Tersine, yazılımın kendisi **yakın zamanda piyasaya sürülen** donanım
sürümleriyle **uyumsuz olabilir.**
**Donanım uyumluluğunu soyutlayarak** **konteynerleştirmeyi** oldukça
taşınabilir **bir sanallaştırma teknolojisi haline getirir.**


**Bulut Veri Merkezi Teknolojisi (Cloud Data Center Technology)**


❖ **Diğer Hususlar (Other Considerations)**

- **Taşınabilirlik:**
Bir sanallaştırma programının **çeşitli sanallaştırma çözümleriyle**
**çalışması** için **yönetim ortamları oluşturan programatik** ve **yönetim**
**arayüzleri**, **uyumsuzluklar** nedeniyle **taşınabilirlik** **boşlukları**
**oluşturabilir.**
**Sanal disk görüntü formatlarının standartlaştırılması** için **Açık**
**Sanallaştırma Formatı (OVF)** gibi girişimler **bu endişeyi gidermeye**
**adanmıştır.**
Dahası **,** **konteynerleştirme çok yüksek taşınabilirlik seviyelerine**
sahip alternatif bir sanallaştırma teknolojisi türü sağlar.


### KAYNAKLAR


- Thomas Erl, Eric Monroy - Cloud Computing_ Concepts,
Technology, Security, and Architecture (The Pearson Digital
Enterprise Series from Thomas Erl)-Pearson (2023)


