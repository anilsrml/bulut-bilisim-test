# **BULUT GÜVENLİĞİ VE SİBER** **GÜVENLİĞİ GİRİŞ**


#### **1. TEMEL GÜVENLİK TERMİNOLOJİSİ**

❖ **Bilgi güvenliği**, bilgisayar sistemlerinin ve verilerin

bütünlüğünü ve bunlara erişimi korumak için
birlikte **çalışan** **karmaşık** **bir** **teknikler**,
**teknolojiler**, **düzenlemeler** ve **davranışlar**
**bütünüdür.**


#### **Gizlilik (Confidentiality)**

❖ **Gizlilik**, bir **bilginin** **yalnızca** **yetkili** **tarafların** **erişimine** **açık**

**olması** durumunu ifade eder.


- **Bulut ortamlarında gizlilik**, **esas olarak taşınan** (iletim halindeki)
ve **depolanan verilere** erişimin **sınırlandırılmasıyla ilgilidir.**


##### **Bütünlük (Integrity)**

❖ **Bütünlük**, **bir** **bilginin** **yetkisiz** **bir** **tarafça** **değiştirilmemiş** **olması**
**durumunu ifade eder.**
❖ **Bütünlük** **kavramı**, verilerin bulut hizmetleri ve bulut tabanlı BT kaynakları

tarafından **nasıl** **depolandığı**, **işlendiği** ve **erişildiği** süreçlerini de
kapsayacak şekilde genişletilebilir.


❖ **Bulut** **tüketicisi** tarafından **bulut** **hizmetine** **gönderilen** **mesaj**,
**değiştirilmemişse bütünlüğe sahip kabul edilir.**


#### **Erişilebilirlik (Availability)**

❖ **Erişilebilirlik**, bir sistemin **belirli bir zaman dilimi**

**boyunca** **ulaşılabilir** ve **kullanılabilir** olma **durumunu**
**ifade eder.**
❖ Tipik bulut ortamlarında, **bulut** **hizmetlerinin**
**erişilebilirliği**, genellikle **bulut hizmet sağlayıcısı** ile
**bulut taşıyıcısı** arasında **paylaşılan bir sorumluluktur.**


**Örneğin destekleyici siber güvenlik teknolojileri**, **şifreleme yoluyla gizlilik**, çalışma
zamanı taraması yoluyla **bütünlük ve paylaşılan** bulut tabanlı veri tabanının **sürekli**


#### **Doğruluk / Gerçeklik (Authenticity)**



❖ **Doğruluk**, bir **bilginin** veya **işlemin** **yetkili bir kaynak**



**tarafından** sağlandığını gösterir.
❖ **Bu kavram**, aynı zamanda **inkâr edilemezlik (non-**



**repudiation)** ilkesini de kapsar.
❖ **İnkâr edilemez etkileşimlerde** yapılan **kimlik doğrulama**,

bu işlemlerin yalnızca **yetkili** **bir** **kaynakla**
**ilişkilendirilebildiğini ispatlar.**

- Örneğin, **bir kullanıcı inkâr edilemez nitelikteki bir dosyayı**
**teslim aldıktan sonra** **bu dosyaya eriştiğinde**, bu erişimin
**kaydedilmesi gerekir;** aksi takdirde **erişim mümkün**
**olmayabilir.**


##### **Güvenlik Kontrolleri (Security Controls)**

❖ **Güvenlik kontrolleri,** **güvenlik tehditlerini önlemek** veya

bu tehditlere **yanıt vermek**, ayrıca **riskleri azaltmak** ya da
**ortadan kaldırmak amacıyla** **kullanılan önlemlerdir.**
❖ **Bu tür karşı önlemlerin** **nasıl kullanılacağına ilişkin**

**ayrıntılar** genellikle **bir** **güvenlik politikası** **içerisinde**
**belirtilir** .
❖ **Güvenlik politikası;** hassas ve kritik _BT kaynaklarının_

_azami düzeyde korunması_ amacıyla, **bir sistemin, hizmetin**
**veya güvenlik planının** **nasıl uygulanacağını belirten**
**kural** ve **uygulamalar** bütününü içerir.


### **Örnek Önlemler**

##### ❖ IAM (Identity and Access Management) → Erişim yönetimi ❖ MFA (Multi-Factor Authentication) → Çok faktörlü doğrulama ❖ Firewall → Ağ trafiği kontrolü ❖ Encryption (Şifreleme) → Veri koruma ❖ SIEM (Security Information and Event Management) → Olay izleme ve analiz


#### **Güvenlik Mekanizmaları (Security Mechanisms)**

❖ **Güvenlik mekanizmaları;** BT **kaynaklarını**, **bilgileri**

ve **hizmetleri** **koruyan savunma altyapısının** birer
bileşeni olan yapılardır.

 - **Örnekler:**
❖ Hashing
❖ Dijital İmzalar
❖ Virtual Private Network (VPN)
❖ Multi-Factor Authentication (MFA) Sistem
❖ …..


❖ **Güvenlik politikası,** bir dizi **güvenlik kuralı**



ve **düzenlemesini belirler.**
❖ **Çoğu zaman**, **güvenlik politikaları bu kural**

ve **düzenlemelerin nasıl uygulanacağını** ve
**denetleneceğini** de ayrıntılı **olarak**
**tanımlar.**
❖ Örneğin, **güvenlik kontrollerinin** ve



**mekanizmalarının** **nerede**
**konumlandırılacağı** ve **nasıl kullanılacağı**,
**güvenlik politikaları** tarafından
**belirlenebilir.**


#### **2. TEMEL TEHDİT TERİMLERİ**

❖ **Risk**
**Risk**, belirli bir eylem sonucunda ortaya çıkabilecek **istenmeyen ve**

**beklenmedik kayıpların olasılığıdır** .
Siber güvenlik bağlamında risk;

  - **Dış tehditler,**

  - **İçsel zafiyetler,**

  - **Tehditlere karşı verilen yanıtlar,**


Ayrıca **insan hatası**, **teknolojik arızalar** ve **siber güvenlik**
**ortamının genel kalitesiyle** ilgili durumları kapsayabilir.


❖ **Zafiyet (Vulnerability)**

- Siber güvenlik bağlamında **zafiyet**, bir BT ortamında ya da buna
bağlı politika veya süreçlerde bulunan bir **kusur**, **açıklık** ya da
**zayıflıktır** .


Bu durum, bir organizasyonu **başarılı olabilecek güvenlik**
**ihlallerine karşı savunmasız** bırakabilir.


- Zafiyetler **fiziksel** ya da **dijital** olabilir.

- **Saldırganlar** bu **zafiyetlerden** **faydalanmaya** **çalışırken**,
**kuruluşlar** ise bu **zafiyetleri ortadan kaldırmak** ya da **etkilerini**
**azaltmak** için **çaba gösterir.**


❖ **Sömürme (Exploit)**
**Sömürme**, bir **saldırganın** **mevcut bir zafiyetten**
faydalanarak onu **kendi** **çıkarına** **kullanması**
**durumudur.**


❖ **Sıfır Gün Zafiyeti (Zero-Day Vulnerability)**
Sıfır gün zafiyeti, **bir kuruluşun** ya **henüz farkında olmadığı** ya
da **farkında olsa** bile **henüz bir yamayla (güncellemeyle)**


❖ **Güvenlik İhlali (Security Breach)**
Güvenlik ihlali, **bilgiye veya sistemlere yetkisiz**
**erişimle** **sonuçlanabilecek** herhangi bir **olayı ifade**
**eder.**
Genellikle, bir **saldırganın güvenlik mekanizmalarını**
**ve** **kontrollerini** **aşmayı** **başarması** durumunda
meydana gelir.


❖ **Veri İhlali (Data Breach)**
Veri ihlali, **bir tür güvenlik ihlalidir** ve bu durumda bir
saldırgan, **gizli bilgileri ele geçirmeyi** başarır.

- **Yanlış yapılandırılmış bir bulut veri tabanından** müşteri
bilgilerinin **yetkisiz kişiler tarafından ele geçirilmesi** **veri**
**ihlaline örnektir.**


Örneğin bulutta veri ihlalinin önlenmesi için **CIEM (Cloud**
**Infrastructure** **Entitlement** **Management)**
gibi teknolojiler yer almaktadır.
Bulutta **kim hangi kaynağa**
**hangi yetkiyle erişiyor** onu **yönetir** ve **denetler** .


##### ❖ Veri Sızıntısı (Data Leak)

- Veri sızıntısı, **herhangi** **bir** **saldırı**
**gerçekleşmeden**, hassas bilgilerin **yetkisiz**


## Örnek Olay


❖ **Veri sızıntısını önlemek** için **DLP (Data Loss**

**Prevention)** sistemleri kullanılır.
Örneğin

- Google Cloud DLP

- AWS Macie
Bunlardan birkaçıdır.
Örneğin Amazon Macie, makine öğrenimi kullanarak
geniş ölçekte hassas verileri (kişisel veriler, deneysel
sonuçlar vs.) otomatik olarak keşfeder, sınıflandırır ve
korur.


❖ **Tehdit (veya Siber Tehdit)**
Tehdit ya da siber tehdit, bir **kuruluşa yönelik bilinen** ve **potansiyel**
bir saldırı olup, **tehlike ve risk oluşturur.**
**Belirli bir kuruluşa yönelik tehditlerin tamamına** **tehdit ortamı**
(threat landscape) ya da siber tehdit ortamı denir.


❖ **Saldırı (veya Siber Saldırı)**
Bir tehdit, **bir saldırgan tarafından gerçekleştirildiğinde**, artık saldırı
ya da **siber saldırı adını alır.**


❖ **Saldırgan ve İzinsiz Giriş Yapan Kişi (Intruder)**
**Bulut güvenliği** ve **siber güvenlik bağlamında**, **saldırgan**, **siber**
**saldırıları** gerçekleştiren **kişi ya da kuruluştur.**


##### **Farklı türde saldırganlar vardır:**

###### • Siber Suçlular (Cyber Criminals): Kâr elde etmek ya da yasa dışı faaliyetlerde bulunmak amacıyla gizli bilgileri çalmaya çalışan saldırganlardır. • Kötü Niyetli Kullanıcılar (Malicious Users): Güvenilir ayrıcalıklara sahip olan ancak bu ayrıcalıkları kötüye kullanan yetkili kişilerdir (örneğin, kurum içindeki art niyetli çalışanlar). Bu kişiler, sisteme zarar vermek veya yetkisiz işlemler gerçekleştirmek amacıyla erişim sağlarlar.


**Farklı türde saldırganlar vardır:**


- **Siber Aktivistler (Cyber Activists):**
Politik bir gündem, dini inanç veya sosyal bir ideolojiyi desteklemek
için kötü **amaçlı faaliyetlerde** bulunan **saldırganlardır.**


- **Devlet Destekli Saldırganlar (State-Sponsored Attackers):**


Bir **devlet kurumu tarafından görevlendirilmiş** veya finanse
edilmiş saldırganlardır.

- Herhangi bir saldırgan, bir kuruluşun sınırları içinde **yetkisiz**
**erişim sağlamayı başardığında**, artık bu kişi veya oluşum **“izinsiz**
**giriş yapan kişi” (intruder)** olarak **adlandırılır.**


#### **Saldırı Vektörü ve Saldırı Yüzeyi (Attack Vector** **and Surface)**

❖ **Saldırı** **vektörü**, **bir** **saldırganın** **zafiyetleri**
**sömürmek** için **izlediği yolu ifade eder.**

- **E-posta ekleri, açılır pencereler**, **sohbet odaları** ve
**anlık mesajlar** gibi **unsurlar saldırı vektörlerine**
**örnektir.**


❖ **Saldırı** **yüzeyi,** bir
_**saldırganın bir sisteme**_
_**erişmek**_ veya
sistemden _**bilgi çalmak**_
için **kullanabileceği**
**saldırı** **vektörlerinin**
**tümünü** **kapsayan**
**alandır.**


#### **Saldırı Yüzeyi ve saldırı vektörü arasındaki** **farklar**

- **Saldırı vektörleri, genel saldırı yüzeyinin** bir **parçasıdır** .

- Siber saldırganların sistemlere ve verilere **yasa dışı erişim**
**sağlamak** için kullandığı **yöntemlerdir** .

- Birçok saldırı vektörü, saldırı yüzeyinin birden fazla bölümüne
karşı kullanılabilir. Örneğin:


##### **3. TEHDİT AKTÖRLERİ (THREAT AGENTS)**

**Tehdit aktörü**, bir saldırıyı gerçekleştirme kapasitesine sahip

olduğu için **tehdit oluşturan varlıktır.**
Bulut güvenliğine yönelik tehditler;

 - **İç kaynaklı** veya **dış kaynaklı**,

 - **İnsan** ya da **yazılım programları** tarafından kaynaklanabilir.


- **Tehdit aktörlerinin**
neden olduğu
**tehditler**,
**zafiyetler** ve
**risklerle** mücadele
etmek için,
**güvenlik**
**politikaları** ve
**güvenlik**
**mekanizmaları**
kullanılır.


❖ **Anonim Saldırgan (Anonymous Attacker)**
Anonim saldırgan, bulut ortamında **yetkisi olmayan**,



**güvenilmeyen** bir **bulut hizmeti kullanıcısıdır.**
Genellikle, **ağ düzeyinde saldırılar gerçekleştiren**



**harici bir yazılım programı** olarak **varlık gösterir**
ve bu **saldırıları** **genel ağlar üzerinden başlatır.**
Anonim saldırganlar sıklıkla;

- **kullanıcı hesaplarını atlamak**,

- **kullanıcı kimlik bilgilerini çalmak** gibi eylemlere
yönelirler
ve genellikle **anonimliklerini koruyan** ya da **cezai**
**takibi zorlaştıran** yöntemler kullanırlar.



Anonim saldırgan
için kullanılan
gösterim
(notasyon)


❖ **Kötü Niyetli Hizmet Aracısı (Malicious Service**

**Agent)**
Kötü niyetli bir **hizmet aracısı**, bulut ortamı içinde
akan **ağ trafiğini yakalayabilir** ve **yönlendirebilir.**
Genellikle, ya doğrudan bir **hizmet aracısı** olarak ya
da hizmet aracısı gibi davranan bir **program** olarak
var olur ve **zararlı veya ele geçirilmiş bir mantığa**
sahiptir.
Ayrıca, uzaktan ağ trafiğini **yakalayabilen** ve
**iletilerin içeriğini bozma** potansiyeline sahip **harici**
**bir program** olarak da bulunabilir.



Kötü niyetli
hizmet aracısı
için kullanılan
gösterim
(notasyon).


❖ **Güvenilir Saldırgan (Trusted Attacker): Kötü Niyetli Kiracılar**
Güvenilir saldırgan, **bulut hizmeti kullanıcısıyla** aynı bulut
ortamında BT **kaynaklarını paylaşan** ve bu ortamda, **meşru**
**kimlik bilgilerini kötüye kullanarak** **bulut sağlayıcılarını** ya da
birlikte **kaynak paylaştıkları** diğer **kiracıları** **hedef alan kişidir.**
**Güvenilmeyen** **anonim** **saldırganların** **aksine**, **güvenilir**
**saldırganlar** genellikle **saldırılarını bulutun** **güven sınırları**
**içerisinden gerçekleştirir.**


**Güvenilir saldırganlar** (diğer adıyla **kötü niyetli kiracılar** ),

bulut tabanlı **BT kaynaklarını çok çeşitli amaçlarla**
**sömürmek** için kullanabilirler.
Bunlar arasında şunlar yer alır:

- **Zayıf kimlik doğrulama süreçlerini hacklemek**,

- **Şifrelemeyi kırmak**,

- **E-posta hesaplarına spam göndermek**,

- ve **hizmet reddi saldırıları** gibi yaygın saldırıları
başlatmak.


❖ **Kötü Niyetli İç Tehdit Unsuru (Malicious Insider)**
**Kötü niyetli iç tehdit unsurları**, **bulut sağlayıcısı adına** ya da

**onunla ilişkili olarak hareket eden** **insan kaynaklı tehdit**
**aktörleridir** .


Genellikle, **mevcut veya eski çalışanlar** ya da **bulut**
**sağlayıcısının tesislerine erişimi olan üçüncü taraf**

**kaynaklarına** **erişim için yönetici ayrıcalıklarına** sahip
olabilir.


##### **4. YAYGIN TEHDİTLER (COMMON THREATS)**

❖ **Trafik Dinleme (Traffic Eavesdropping)**
Trafik dinleme, **buluta gönderilen** ya da **bulut içinde aktarılan**
**verilerin** (genellikle bulut hizmeti kullanıcısından bulut sağlayıcısına
doğru) **kötü niyetli bir hizmet aracısı** tarafından **pasif bir şekilde**
**yakalanması** durumudur.


❖ **Kötü Niyetli Aracı (Malicious Intermediary)**
Kötü niyetli aracı tehdidi, **iletilerin kötü niyetli bir hizmet aracısı**
tarafından **yakalanıp değiştirilmesi durumunda** ortaya çıkar.
Bu durum, **iletinin gizliliğini** ve/veya **bütünlüğünü tehlikeye**
atabilir.
Ayrıca bu **hizmet aracısı**, **iletinin hedefine yönlendirilmeden** önce


❖ **Hizmet Dışı Bırakma (Denial of Service – DoS)**
Hizmet Dışı Bırakma (DoS) saldırısının amacı, **BT kaynaklarını aşırı**

**yükleyerek düzgün çalışamaz hale getirmektir** .
Bu tür saldırılar genellikle aşağıdaki şekillerde gerçekleştirilir:

  - **Bulut hizmetlerinin iş yükü**, **sahte iletiler** veya **tekrarlanan**
**iletişim talepleri** ile yapay olarak artırılır.

  - **Ağa yoğun trafik gönderilerek**, **yanıt süresi düşürülür** ve
performansı **zayıflatılır.**

  - Her biri **aşırı bellek ve işlemci kaynağı tüketmek** üzere
tasarlanmış **birden fazla bulut hizmeti isteği** gönderilir.


**Bulut Hizmeti Kullanıcısı A**, **Sanal Sunucu A üzerinde barındırılan bir bulut hizmetine** (gösterilmemiştir) **birden**

Sonuç olarak, Bulut **Hizmeti Kullanıcısı B** gibi **meşru kullanıcılar**, Sanal Sunucu A ve B üzerinde barındırılan hiçbir
bulut **hizmetine erişemez hale gelir.**


❖ **Yetersiz Yetkilendirme (Insufficient Authorization)**

- Yetersiz yetkilendirme saldırısı, bir saldırgana **yanlışlıkla** ya da **aşırı geniş**
**yetkilerle** **erişim izni verilmesi durumunda** meydana gelir.

- Bu durum, saldırganın **normalde korunması gereken** **BT kaynaklarına**
**erişim sağlamasıyla** sonuçlanır.


**Bulut Hizmeti Tüketicisi A**,
( **Bulut Hizmeti Tüketicisi B'ye**
**göre** ) yalnızca yayınlanmış **bir**
**hizmet sözleşmesine sahip**
**bir web hizmeti aracılığıyla**
**erişilebileceği** **varsayımıyla**
**uygulanan** **bir veri tabanına**
**erişim elde eder.**


- **Zayıf** **kimlik** **doğrulama** **(weak** **authentication)**, **zayıf**
**parolalar** veya **paylaşılan** **kullanıcı** **hesapları** ile **BT**
**kaynaklarının korunmaya çalışılması** durumunda **ortaya**
**çıkabilir.**
Bulut ortamlarında, bu tür saldırılar;

- **Ele geçirilen BT kaynaklarının kapsamına** bu **kaynaklara**
**sağlanan** **erişim** **düzeyine**
bağlı olarak **ciddi etkilere yol açabilir.**


- Bir saldırgan, **Bulut** **Hizmeti**
**Kullanıcısı A** tarafından kullanılan
**zayıf bir parolayı kırmıştır** .


Bunun sonucunda, saldırgana ait
**kötü** **niyetli** **bir** **bulut** **hizmeti**

Bu sayede **bulut tabanlı sanal**
**sunucuya** **erişim** **sağlamayı**
**hedefler** .


❖ **Sanallaştırma Saldırısı (Virtualization Attack)**

- Sanallaştırma, **birden fazla bulut hizmeti kullanıcısına**, **aynı**
**fiziksel donanımı paylaşan**, ancak mantıksal olarak **birbirinden**
**izole edilmiş** BT kaynaklarına **erişim imkânı sağlar.**

- **Bulut sağlayıcıları,** **bulut kullanıcılarına** **sanal BT kaynakları**
(örneğin sanal sunucular) üzerinde **yönetici düzeyinde erişim**
**sağladıkları için**, bu **erişimin kötüye kullanılarak alttaki fiziksel**
**BT** kaynaklarına saldırı **yapılması riski doğar.**


Sanallaştırma saldırısı, **sanallaştırma platformundaki**
**zafiyetleri sömürerek**, **platformun gizliliğini**, **bütünlüğünü**
ve/veya **erişilebilirliğini tehlikeye** atmayı amaçlar.


##### **Çakışan Güven Sınırları (Overlapping Trust** **Boundaries)**

- Eğer bir **bulut ortamındaki fiziksel BT kaynakları**, **farklı bulut**
**hizmeti kullanıcıları** tarafından **paylaşılıyorsa**, bu kullanıcılar
**çakışan güven sınırlarına** sahip olur.


##### **Konteyner Tabanlı Saldırı (Containerization** **Attack)**

❖ Konteyner tabanlı yapıların kullanımı, **ana işletim sistemi**

**düzeyinde yalıtım eksikliğini** beraberinde getirir.
❖ **Aynı makinede konuşlandırılan konteynerler** **aynı ana işletim**

**sistemini** **paylaştıkları** için, **bu durum güvenlik tehditlerini**
**artırabilir** ; çünkü **tüm sisteme erişim sağlanması mümkün hale**
gelebilir.
❖ Eğer **alttaki ana sistem ele geçirilirse**, **o sistemde çalışan tüm**

**konteynerler etkilenebilir.**


##### **Konteyner Tabanlı Saldırı (Containerization** **Attack)**

❖ **Konteynerler**, bir **sanal sunucu üzerinde çalışan** işletim sistemi

içinde oluşturulabilir.
❖ Bu yöntem sayesinde, **bir güvenlik ihlali gerçekleştiğinde**

yalnızca **o işletim sistemi** ya da **o sanal sunucuda** çalışan
konteynerler etkilenir.
❖ Böylece saldırgan yalnızca **tek bir sanal sunucuya ait işletim**

**sistemine** ve o sunucuda **çalışan konteynerlere erişim**
**sağlayabilirken**, **diğer sanal sunucular** (veya fiziksel sunucular)
**etkilenmeden kalır** .


#### **5. KÖTÜ AMAÇLI YAZILIM (MALWARE)**



❖ **Bir bilgisayar sistemine** veya **ağa** **zarar vermek amacıyla**



tasarlanmış bir **yazılım türüdür.**
**Kötü amaçlı yazılımlar**, çeşitli zararlı faaliyetleri gerçekleştirmek



için kullanılabilir. Bunlar arasında şunlar yer alır:




- **Korunan verileri çalmak**,

- **Gizli belgeleri silmek**,

- **Özel iletişimleri dinlemek**,

- **Gizli faaliyetler hakkında bilgi toplamak** .


**Bir saldırgan**, örneğin bir web sitesi aracılığıyla, bir **sunucuyu kullanıcıya**
**erişilebilir** hale getirir ve **kullanıcı farkında olmadan** kötü amaçlı yazılımı **yerel iş**
**istasyonuna indirir.**


❖ **Kötü amaçlı yazılıma (malware) dayalı yaygın siber saldırı**

**türleri:**

- **Virüs:** Sisteme ve dosyalara bulaşarak yayılan ve bu sayede
kendini çoğaltabilen, ayrıca bulaştığı sistemde ek eylemler
gerçekleştirebilen kötü amaçlı yazılımdır.

- **Truva Atı (Trojan):** Meşru bir uygulama veya hizmet gibi
görünen kötü amaçlı yazılım parçasıdır. Genellikle arka
planda çalışarak, sistemde arka kapı kodu yükleme,
çalışmakta olan işlemlere kod enjekte etme gibi zararlı
faaliyetler gerçekleştirir. Truva atları, bir virüs içerebilir veya
içermeyebilir.

**yazılımdır.**


- **Reklam Yazılımı (Adware):** İstenmeyen reklamlar veya açılır
pencereler (pop-up) görüntülemek üzere tasarlanmış
yazılımdır. Adware, hassas bilgileri toplayabileceği, sistemleri
yavaşlatabileceği ve diğer kötü amaçlı yazılımlara karşı
savunmasız bırakabileceği için bir güvenlik tehdidi olarak
kabul edilir.

- **Fidye Yazılımı (Ransomware):** Verilerin kullanımını ya da
erişimini kısıtlayan veya engelleyen, karşılığında bir ücret
talep eden kötü amaçlı yazılımdır. Aktif bir fidye yazılımı
saldırısı, uzaktan kod yürütme (remote code execution)
yoluyla da gerçekleştirilebilir (bu konu ilerleyen bölümlerde
ele alınacaktır).


- **Sahte Antivirüs (Rogue Antivirus):** Kurbanları kandırmak için
antivirüs yazılımı gibi davranan kötü amaçlı uygulamadır.
**Kurulduktan sonra sahte güvenlik uyarıları vererek,**
**kullanıcıyı yazılımın "tam sürümünü" satın almaya**
yönlendirir.

- **Kripto** **Madenciliği** **Yazılımı** **(Crypto** **Jacking):** Web
içeriklerine gömülü script'leri çalıştırarak, kullanıcının bilgisi
ve rızası olmadan tarayıcı tabanlı **kripto para madenciliği**
**yapılmasıdır.**

- **Solucan (Worm):** Kendi kendini çoğaltan, yayılabilen ve
bağımsız çalışan bir **programdır** . Ağ üzerinden yayılmak için
ağ mekanizmalarını kullanır. Solucanlar genellikle hesaplama
kaynaklarını tüketmenin ötesinde **doğrudan zarar vermez ve**
**artık çok yaygın değildir.**


#### **İç Tehdit (Insider Threat)**

- İç tehdit, bir kuruluşun personeli veya kuruluşun tesislerine ya da
sistemlerine **erişimi olan diğer kişiler** tarafından **verilebilecek**
**potansiyel zararı** ifade eder.
**Yaygın iç tehdit türleri şunlardır:**

- **Kötü niyetli (Malicious):** Örneğin **memnuniyetsiz bir çalışan** gibi bir iç
unsurun, kuruluşa ait **verilere, sistemlere veya BT altyapısına**
**erişerek zarar verme girişimidir** .

- **Kazara (Accidental):** **Bilgisizlik ya da insan hatası** nedeniyle **içeriden**
**kaynaklanan kazara zarar** durumudur. Örneğin; _önemli bir dosyanın_
_yanlışlıkla silinmesi_ veya _gizli verilerin yetkisiz bir kişiyle farkında_
_olmadan paylaşılması_ gibi.

- **İhmalkâr (Negligent):** **Dikkatsizlik** ya da mevcut **siber güvenlik**
**standartları ve politikalarına uymama isteksizliği** sonucu içeriden
kaynaklanan zararlardır.


Kuruluşa tehdit oluşturan **kötü niyetli (solda)**, **ihmalkâr (ortada)** ve **kazara**
**(sağda)** iç tehdit unsurlarına ait örnekler.

_**İç tehditler,**_ _bir kuruluşun varlıklarını tehlikeye atabilir._
_Bu varlıklar arasında; fiziksel donanımlar, ürün stokları, kurumsal web_
_siteleri, sosyal medya iletişimleri ve bilgi varlıkları yer alır._


**Sosyal Mühendislik ve Oltalama (Phishing)**


- Sosyal mühendislik, **bireylerin hassas bilgileri ifşa etmeye** veya
**zarar verici eylemler gerçekleştirmeye** (örneğin yetkisiz kişilere
erişim izni vermek gibi) **ikna edilerek kandırıldığı** **bir saldırı**
**türüdür.**


**Botnet**

- Botnet saldırısı, **farklı cihazlara yayılmış** **birden fazla botun**,
**eşgüdümlü bir ağ** (bot ağı – botnet) **aracılığıyla saldırı**
**gerçekleştirmesiyle ortaya çıkar.**


Bir saldırgan, **Kuruluş A** ’daki
**normal bir sunucuyu**, **zombi**
**sunucuya dönüştürmüştür** .
**Bu** **sunucu**, **saldırgan**
**tarafından** **Kuruluş B** ’deki bir
kullanıcının **bilgisayarına kötü**
**amaçlı yazılım göndermek** için
kontrol edilmektedir.


❖ Bot, **bir** **kez** **kurulduğunda**, **diğer**
**bulaşmış cihazlardaki botlarla** **bağlantı**
**kurmaya çalışır** ve **böylece saldırganın**
**kullanabileceği bir ağ oluşturur.**
**Bu ağ;**




  - **geniş çaplı DDoS saldırıları**,

  - **kripto para madenciliği (crypto**
**jacking)**,

  - **zararlı içerikli toplu e-postalar**
**gönderme**,

  - **veri hırsızlığı**,

  - hatta **yeni botlar devşirme** gibi
kötü amaçlı işlemler
için kullanılabilir.
❖ Botnet'ler, **dark web üzerinden satın**



**alınabilir** ve hatta **kısa süreliğine**
**kiralanabilir** .


**Yetki Yükseltme (Privilege Escalation)**


❖ Bir saldırganın, **sınırlı erişim yetkilerine sahip bir kullanıcı**

**hesabını ele geçirdikten sonra**, **yönetici (admin) yetkileri**
**kazanmaya çalıştığı** durumlarda meydana gelir.


**Kaba Kuvvet Saldırısı (Brute Force)**


 - Kaba kuvvet saldırısında, **bir saldırgan**, çok sayıda olası kullanıcı
adı ve parola kombinasyonunu dener.

 - Amaç, **doğru kombinasyonu bulmak** ve **böylece yetkisiz şekilde**
bir sisteme **erişim sağlamaktır.**


                                           - Kaba kuvvet saldırısının **en basit türü,**
saldırganın muhtemel parolalardan oluşan

saldırgan, **önceki veri ihlallerinden elde**
**edilen kullanıcı adı ve parolaları,** **başka**
**sistemlere sızmak** için **yeniden kullanır.**


##### **Uzaktan Kod Yürütme (Remote Code Execution)**


 - Uzaktan kod yürütme, **bir saldırganın başkasına ait bir bilgisayar**
**cihazında uzaktan komut çalıştırdığı** bir **siber saldırı türüdür.**
**Bu saldırının başarılı olabileceği bazı örnekler şunlardır:**

 - **Kötü amaçlı yazılımın (malware),** **hedef sistem tarafından**
**indirilmesi**,

 - **Tünelleme (tunneling)** yöntemi kullanılarak, **uzaktan erişim elde**
**edilmesi** ve bunun aracılığıyla **sunucu veya veri tabanı**
**komutlarının çalıştırılması,** ya da sistem ve işletim sistemi
hizmetlerinin kontrol altına alınması.

 - **Not:** _Tünelleme,_ _**ağ trafiğinin**_ _başka_ _**bir protokol veya bağlantı**_
_içinde_ _**gizlenerek taşınması**_ _yöntemidir._


Zaten kurulmuş bir kötü amaçlı yazılım programını kullanan bir saldırgan, bu
yazılıma kuruluşun sunucusunda zarar verici eylemleri gerçekleştirmesi için
**komutlar verebilir.**


- **Uzaktan kod yürütme saldırısı**, genellikle **bir bilgi toplama**
**süreciyle başlar.**

- Bu süreçte saldırgan, **otomatik tarama araçları kullanarak**
sistemdeki **zafiyetleri tespit etmeye çalışır.**

- Uzaktan kod yürütme tekniği, **botnet saldırıları**, **fidye yazılımı** ya
da **Truva atı kullanan kötü amaçlı yazılım saldırıları** gibi **diğer**
**siber saldırılar tarafından da kullanılabilir.**


##### SQL Enjeksiyonu (SQL Injection)


- SQL enjeksiyonu, **uygulamalara yönelik bir saldırı tekniğidir.**

- Bu teknikte, **kötü amaçlı SQL ifadelerinden oluşan kod**, bir web
uygulamasının **kullanıcı arayüzündeki giriş alanına yerleştirilir**
ve **bu sayede web uygulama sunucusunun** bu **zararlı kodu**
**çalıştırması sağlanır.**


##### **Tünelleme (Tunneling)**


 - Tünelleme (Tunneling), **verilerin yetkili bir protokol paketine gömülerek**
**güvenlik duvarı kontrollerinin atlatılmasını sağlayan** bir tekniktir.

 - Bu yöntemle, **hassas veriler ağdan dışarı çıkabilir** ve **yetkisiz ya da zararlı**
**veriler ağa** girebilir. (Bu süreçte herhangi bir uyarı tetiklenmeden ya da kayıt
oluşturulmadan)


yer alır.


**Gelişmiş** **Kalıcı** **Tehdit**
**(Advanced** **Persistent** **Threat**

**– APT)**


**dilimine yayılmış**, **eşgüdümlü şekilde**
**gerçekleştirilir.**

- APT'lerin (Gelişmiş Kalıcı Tehditlerin) **temel**
**hedeflerinden biri**, bir **güvenlik ihlali**
**yoluyla** kuruluşun sistemine erişim
sağladıktan sonra, **kuruluşun ortamında**
**kalıcı olarak yerleşmek olabilir.**


##### **Ek Hususlar**

❖ **Hatalı Uygulamalar**
Bulut hizmetlerinin **yetersiz**
**tasarımı**, **uygulanması** veya
**yapılandırılması**, **yalnızca**
**çalışma** **zamanı** **hataları**
veya **sistem** **arızalarının**
**ötesinde**, **BT kaynaklarının**
**bütünlüğünü**, **gizliliğini**
ve/veya **kullanılabilirliğini**
**tehlikeye atabilir.**
Bulut Hizmeti Tüketicisi A'nın gönderdiği mesaj, Bulut
Hizmeti A'daki bir yapılandırma hatasını tetikler. Bu da, aynı
zamanda Bulut Hizmetleri B ve C'yi barındıran sanal
sunucunun çökmesine neden olur.


❖ **Güvenlik Politikası Uyumsuzluğu**


❖ **Sözleşmeler**
Sözleşmede, **bulut sağlayıcısının üstlendiği sorumluluk miktarını**
ve/veya **talep edebileceği tazminat seviyesini** açıkça belirten
ifadeler yer almalıdır. **Bulut sağlayıcısının üstlendiği sorumluluk**
**ne kadar fazlaysa**, **bulut hizmeti kullanıcısı** için **risk o kadar az**
**olur.**


- **Risk Yönetimi**
**Bulut hizmeti kullanıcılarının**
**bir risk yönetim stratejisinin**
parçası olarak **resmi bir risk**
**değerlendirmesi** **yapmaları**
**teşvik edilir.**



Sürekli olarak yürütülen risk yönetim süreci, **bu üç aşamadan**
**herhangi birinden başlatılabilir.**


**1- Risk Değerlendirmesi**
Bulut ortamı, **tehditlerin** **yararlanabileceği**
potansiyel zayıflıklar ve eksiklikler belirlemek
amacıyla analiz edilir.
Bulut sağlayıcıdan, bulut ortamında gerçekleşmiş
geçmiş saldırılar (hem başarılı hem de başarısız) ile
**ilgili istatistikler ve diğer bilgileri sunması**
**istenebilir.**


**2- Riskin Bertaraf Edilmesi (Risk Treatment)**
Risk değerlendirmesi sırasında **tespit edilen riskleri**
**etkili bir şekilde yönetmek amacıyla** azaltma
**politikaları ve planları** geliştirilir.
Bazı riskler **tamamen ortadan kaldırılabilir**, bazıları
**azaltılabilir**, bazıları ise **dış kaynak kullanımıyla**
**yönetilebilir** ya da **sigorta kapsamına** veya **işletme**
**kaybı bütçelerine** **dâhil edilebilir.**


**3- Riskin Kontrolü (Risk Control)**

**Risklerin izlenmesiyle ilgili bir süreçtir** ve **üç adımdan oluşur:**
**A. İlgili olayların gözlemlenmesi**,
**B. Bu olayların önceki risk değerlendirmeleri**
**C.** **Bertaraf** **yöntemlerinin** **etkinliğini** **belirlemek** **üzere**
**incelenmesi**, ve **gerekirse güvenlik politikalarında ayarlama**
yapılması.


**İzleme sürecinin doğasına bağlı olarak**, bu aşama **bulut**
**sağlayıcısı** tarafından **yürütülebilir** **ya** **da** **bulut** **hizmeti**
**kullanıcısıyla** birlikte **paylaşılabilir.**


#### **KAYNAKLAR**


- Thomas Erl, Eric Monroy - Cloud Computing_ Concepts,
Technology, Security, and Architecture (The Pearson
Digital Enterprise Series from Thomas Erl)-Pearson (2023)


