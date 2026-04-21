## **İÇİNDEKİLER**

**1. Kapsayıcı (Container) Orkestrasyonu**
**2. Kapsayıcı Ağları**
**3. Zengin (Rich) Kapsayıcılar**
**4. Diğer Yaygın Kapsayıcı Özellikleri**
**5. Kapsayıcı İmajlarını Anlamak**
**6. Çoklu Kapsayıcı Türleri**


#### **1. KAPSAYICI (KONTEYNER) ORKESTRASYONU**


 - **Dağıtık** **bir** **bilgi** **işlem** **ortamında**
kapsayıcılaştırılmış uygulamaların **dağıtımını**,
**ölçeklendirilmesini** ve **yönetimini**
**otomatikleştirme** sürecine **kapsayıcı**
**orkestrasyonu** denir.

 - Bu süreçte, **kapsayıcı** **orkestratörü** olarak da
adlandırılan bir **kapsayıcı** **orkestrasyon** **aracı**
veya **kapsayıcı** **orkestrasyon** **platformu**
kullanılır.


#### **1.1. Kapsayıcı Orkestratörünün Görevleri**

Bir kapsayıcı orkestratörü, **dağıtık bir bilgi işlem ortamında** birçok
**işlemi yerine getirir. Bunlardan bazıları şunlardır:**
❖ **Kapsayıcı Dağıtımı:**
Kapsayıcı orkestratörü, **kapsayıcıları** **bir** **küme** **(cluster)** içindeki
**birden** **fazla** **düğüme** **dağıtarak**, bu kapsayıcıların **doğru** **şekilde**
**yapılandırılmasını** ve ağ **bağlantılarının kurulmasını sağlar** .
❖ **Yük Dengeleme:**
Orkestratör, aynı **uygulamayı** **çalıştıran** **birden** **fazla** **kapsayıcıya**
**gelen** **trafiği** **dengeler.** Bu sayede **yüksek** **erişilebilirlik** ve
**ölçeklenebilirli** k sağlanır.


❖ **Ölçeklendirme:**

Orkestratör, **talebe** **göre** **çalışan** **kapsayıcıların**
**sayısını** **otomatik** **olarak** **artırır** veya **azaltır** (yukarıaşağı, içe-dışa ölçeklendirme).
Bu, kaynakların verimli kullanılması ve maliyet
etkinliği sağlar.
❖ **Sağlık İzleme:**

Orkestratör, **kapsayıcıların** **sağlık** **durumunu** **izler** ve
**başarısız olan kapsayıcıları otomatik olarak yeniden**
**başlatır** veya **sağlıklı kapsayıcılarla değiştirir** .


❖ **Hizmet Keşfi (Service Discovery):**

Orkestratör, uygulamaların **ağ** **üzerinden** **birbirini**
**bulmasını** ve **iletişim** **kurmasını** **sağlayan** **bir** **hizmet**
**kaydı (registry) tutar** .
❖ **Depolama Orkestrasyonu:**

**Orkestratör**, **kapsayıcıların** **kalıcı** **veri** **depolama**
ihtiyaçlarını **yönetir** ve verilerin **doğru** **şekilde** **saklanıp**
**alınmasını** sağlar.


❖ **Ağ Orkestrasyonu:**
Orkestratör, kapsayıcıların **ağ** **ihtiyaçlarını** **yönetir**, her
**kapsayıcıya benzersiz bir IP adresi sağlar** ve **kapsayıcılar arası**
**ağ trafiğini yönlendirir.**
❖ **Yapılandırma Yönetimi:**
Orkestratör, **kapsayıcıların** **yapılandırmalarını** **yönetir**
ve çalışan kapsayıcılara **yapılandırma** **değişikliklerini**
**otomatik olarak uygular.**


#### **ÖRNEK SENARYO**

❖Bir e-ticaret uygulaması geliştirilmek istensin. Bu

uygulama dört ayrı modülden oluşsun. Her bir modül
için konteyner imajları oluşturulsun.


•Tek bir sanal
sunucu üzerinde
her bir bileşen
sorunsuz bir şekilde
çalışsın.


❖ **Problem (Trafik Artışı)**

- Kullanıcı sayısı hızla artıyor .

- Yeni sunucular ekleniyor.

- Container sayısı çoğalıyor.
❖ **Manuel yönetimde:**

- Hangi container nerede çalışıyor bilinmiyor.

- Çöken servisler yeniden başlatılamıyor.

- Yük dengesi yapılamıyor.

- Güncellemeler riskli hale geliyor.


### ❖ Çözüm: Kapsayıcı Orkestrasyonu
#### •Bir yönetim kolaylığı sunar. •Kapsayıcıları otomatik dağıtır. •Trafiğe göre ölçekleme yapar. •Çöken servisleri yeniden başlatır. •Yük dengeleme sağlar.


##### ❖Kubernetes açık kaynak bir platformdur. Kendi sunucularına kurulabilir. ❖Büyük bulut sağlayıcılardan hizmet alınabilir. • AWS → Elastic Kubernetes Service (EKS) • Microsoft Azure → Azure Kubernetes Service (AKS) • Google → Google Kubernetes Engine (GKE)


##### **1.2. Bir Kapsayıcı Orkestratörünün Bileşenleri**

### orkestratörü, **bileşenden oluşur.**


##### **1.2. Bir Kapsayıcı Orkestratörünün Bileşenleri**

Bir kapsayıcı orkestratörünün temel bileşenlerinden
bazıları şunlardır:
❖ **Kapsayıcı Çalıştırma Ortamı (Container Runtime):**

Küme (cluster) içindeki **her düğümde kapsayıcıları**
**çalıştırmaktan** ve **yönetmekten sorumludur.**


❖ **API Sunucusu (API Server):**
Orkestratörle etkileşim kurmak için merkezi bir arayüz
sağlar.
**İstemcilerden gelen API isteklerini kabul eder** ve
**istenilen işlemleri gerçekleştirmek** için **orkestratörün**
**diğer bileşenleriyle iletişim kurar.**
❖ **Zamanlayıcı (Scheduler):**

**Yeni bir kapsayıcının** **kümedeki hangi düğüme**
**yerleştirileceğine** **karar verir.**
Bu kararı verirken **kaynak kullanılabilirliği** ve **iş yükü**
**dengesi** gibi **faktörleri dikkate alır.**


❖ **Denetleyici Yöneticisi (Controller Manager):**

**Ölçeklendirme**, **çoğaltma** ve **sağlık** **izlemesi** gibi
kapsayıcılaştırılmış **uygulama yaşam döngüsünün farklı**
**yönlerini** **otomatikleştiren** **çeşitli** **denetleyicileri**
**yönetmekten sorumludur.**


Orkestratör tarafından **yapılandırma verilerini**, **hizmet keşfi**
**bilgilerini** ve **diğer meta verileri saklamak için kullanılır.**


❖ **Ağ Yönetimi (Networking):**

Kapsayıcıların küme genelinde **birbirleriyle** **iletişim**
**kurabilmesini** sağlayan **gerekli ağ altyapısını sağlar.**
Bu, **yönlendirme (routing)** ve **yük dengeleme işlemlerini** de
kapsar.
❖ **Depolama Yönetimi (Storage):**

Kapsayıcıların **kalıcı depolama ihtiyaçlarını yönetir.**
**Ortak** **depolama** **kaynaklarına** **erişim** **sağlar** ve **veri**
**bütünlüğünü garanti eder.**


##### **1.3. Kapsayıcı Orkestrasyonunda Yer Alan Temel** **Adımlar**

❖ **Kapsayıcı İmajının Oluşturulması:**

Geliştiriciler, **uygulama** **kodlarını** ve **tüm**
**bağımlılıklarını içeren** bir kapsayıcı imajı oluşturur.


❖ **İmajın Kapsayıcı Kayıt Deposuna Gönderilmesi:**

Oluşturulan **kapsayıcı imajı**, **kapsayıcı imajlarının**
**merkezi** ve **uzaktaki bir deposu** olan kapsayıcı **kayıt**
**deposuna yüklenir.**


❖ **Uygulama Dağıtımının Tanımlanması:**
Geliştiriciler, **kapsayıcı orkestratörü kullanarak** uygulamanın
nasıl **dağıtılacağını tanımlar.**
Bu tanım, **kaç adet kopya (replica) çalıştırılacağı**, **ağ**
**yapılandırması** ve **depolama gereksinimleri** gibi bilgileri içerir.
❖ **Uygulamanın Dağıtılması:**
Kapsayıcı orkestratörü, **uygulamayı** **küme içerisindeki** **birden**
**fazla düğüme dağıtır.**
**Belirtilen sayıda kopyanın çalıştığından** ve **uygulamanın**
**kullanıcılar** tarafından **erişilebilir olduğundan emin olur.**


❖ **Uygulamanın İzlenmesi ve Yönetilmesi:**
Kapsayıcı orkestratörü, **uygulamanın sağlık durumunu izler**,

**ve izleme (monitoring) özellikleri sunar.**
❖ **Birden Fazla Uygulamanın Yönetilmesi** :
Kapsayıcı orkestratörü, **aynı** **anda** **birden** **fazla**
**kapsayıcılaştırılmış** uygulamayı yönetebilir.
**Her bir uygulamanın** **kendi ihtiyaçlarına göre dağıtılmasını**,
**ölçeklendirilmesini** ve **yönetilmesini sağlar.**


**Kapsayıcı paket yöneticisi**, **kapsayıcı imajlarını** ve
**onların bağımlılıklarını yönetmekten sorumludur.**
**Kapsayıcı orkestratörü** ise, **dağıtık bir bilgi işlem**
**ortamında** **kapsayıcılaştırılmış** **uygulamaların**
**dağıtımını**, **ölçeklendirilmesini** ve **yönetimini**
**otomatikleştirir.**


##### ❖ Kapsam: Kapsayıcı paket yöneticileri, yalnızca kapsayıcı imajlarının ve bağımlılıklarının yönetimine odaklanır. Kapsayıcı orkestratörleri ise, dağıtımdan ölçeklendirmeye ve yönetimine kadar tüm **kapsayıcılaştırılmış uygulamayı yönetir.**


##### ❖ Soyutlama Seviyesi:

- **Kapsayıcı paket yöneticileri**, daha **düşük bir soyutlama**
**seviyesinde** çalışır. Bireysel kapsayıcı imajları ve bağımlılıklarıyla
ilgilenir.

Örneğin "İçine hangi **kütüphaneler** **(dependencies)**
**kurulmalı** ?", " **Dosya izinleri nasıl ayarlanmalı** ?" gibi tamamen

  - kapsayıcının mikro düzeydeki yapısıyla uğraşırsınız.

- **Kapsayıcı orkestratörleri** ise, tüm kapsayıcılaştırılmış uygulamayı
**yüksek seviyeden yönetir ve genel bir bakış sağlar.**

  - _Örneğin bu web uygulamasından her zaman_ _**5 kopya çalışsın**_ _"_,
_"Sunuculardan biri çökerse,_ _**oradaki kapsayıcıları anında**_
_**başka bir sunucuda yeniden başlat**_ _"_, _"Sistem trafiği artarsa_
_**kopya sayısını 10'a çıkar.**_


❖ **Araç Seti:**
**Kapsayıcı** **paket** **yöneticileri,** genellikle yalnızca
kapsayıcı imajlarını ve bağımlılıklarını yönetmeye odaklı
**sınırlı araçlar sunar.**
**Kapsayıcı orkestratörleri** ise, kapsayıcıların, ağların,
depolamanın ve diğer altyapı kaynaklarının yönetimi
için **geniş bir araç ve API seti sağlar.**


### **2. KAPSAYICI AĞLARI**

❖ **Kapsayıcılaştırma platformları**, birbirleriyle iletişim kurması gereken

**kapsayıcılar arasında bağlantı sağlamak** için genellikle **sanal**
**kapsayıcı ağları sunar.**
Bir kapsayıcı ağı, şu yetenekleri sağlamak için çeşitli kapsayıcılaştırma
platformu ve **sistem özelliklerinin çalışmasına olanak tanır:**

- **Kapsayıcı Erişilebilirliği** (Container Availability)
Kapsayıcıların sürekli erişilebilir olmasını sağlar.

- **Kapsayıcı Ölçeklenebilirliği** (Container Scalability)
Kapsayıcıların ihtiyaçlara göre kolayca ölçeklendirilebilmesini sağlar.

- **Kapsayıcı Dayanıklılığı** (Container Resiliency)
Kapsayıcıların hata ve kesintilere karşı dayanıklı olmasını sağlar.


- **Kapsayıcı** **ağı**, genellikle **bağımsız** **olarak** **yönetilebilen**,
**yapılandırılabilen** ve **şifrelenebilen** **sanal bir ağ** olarak bulunur.


İki temel kapsayıcı ağı türü vardır: **Ana (Host) Ağı ve Kaplama (Overlay) Ağı**
❖ **Ana ağı**, **aynı fiziksel sunucu (host)** üzerindeki **kapsayıcılar arasında iletişim**



**sağlamak** için **tek bir kapsayıcı motoru** tarafından yönetilir.
❖ **Kaplama ağı**, **farklı sunucularda çalışan** **kapsayıcı motorlarının**, farklı



sunuculardaki kapsayıcılar arasında **iletişim kurmasını sağlar.**


❖ **Bazı çözümler**, **yeniden kullanılabilir yardımcı hizmetler** veya **paylaşılan**

**bir veri tabanı** gibi **yazılım programlarını paylaşır.**


❑ **Kapsayıcı A** ve **Kapsayıcı B**, **aynı sunucuda bulunur**

ve **Ana (Host) Ağ A** üzerinden **iletişim kurabilir** .
❑ **Kapsayıcı B**, ayrıca **Kaplama (Overlay) Ağ B** 'nin de **bir**

**parçasıdır** ve **bu ağ üzerinden diğer kapsayıcılarla da**
**iletişim kurabilir.**


 - **Kapsayıcı ağının**, **çözümün kapsayıcı ağı sınırlarının** **dışındaki**
**sistemlerle** **iletişim kurmasına** izin verecek **şekilde yapılandırılması**
**gerekir.**


**iletişimi mümkün kılar.**


**tanımlanır.**


#### **3. ZENGİN (RICH) KAPSAYICILAR**

- **Farklı kapsayıcılaştırma platformları**, **bir kapsayıcının**
**desteklediği özellik yelpazesi açısından** **farklılık**
**gösterebilir.**

- **Daha fazla özelliğe sahip** **kapsayıcılara** **zengin**
**kapsayıcılar** denir.


Bu özellikler arasında, **hizmetin sürekli**
**durumunu** ve **sağlık** **bilgilerini**
sağlayabilen **izleme** **yetenekleri** de
bulunmaktadır.


###### **Gelişmiş kapsayıcı motorları tarafından sağlanan** **özelliklere örnekler şunlardır:** ❖ Kapsayıcı Kaynaklarının Sınırlandırılması: Kapsayıcının kullanabileceği maksimum kaynak miktarını kontrol etmek ve yönetmek mümkündür . ❖ Kullanım Kayıtlarının Toplanması: Denetim (audit) ve mevzuat uyumluluğu amaçlarıyla kullanım günlükleri (logları) toplanabilir.


Örneğin, **belirli bir olay** veya **hata gerçekleştiğinde**
kapsayıcının **otomatik olarak yeniden başlatılması**,
ancak **diğer olay veya hatalarda başlatılmaması** gibi
**kurallar tanımlanabilir** .
##### ❖ Kapsayıcı Depolamasının Yönetimi:

Birden fazla kapsayıcılaştırılmış hizmetin
paylaşabileceği, **izole bir dosya sistemi** gibi **özellikler**
**sunulabilir.**


##### Bu, denetim ve mevzuat gereksinimleri ya da kapsayıcı kapansa bile verilere erişimin devam etmesini sağlamak için gerekli olabilir.


**Aynı** **sunucuda** **barındırılan** **kapsayıcılar** içinde
dağıtılmış **hizmetlerin** **birbirleriyle** **etkileşimini**
**yönetmek için kullanılabilir.**


❖ **Vekil Sunucu (Proxy) Özellikleri Sağlanması:**


**Bazı kapsayıcı motorları**, **barındırdığı hizmetlere gelen**
**istekler** için **vekil (proxy)** görevi üstlenebilir.


#### **4. DİĞER YAYGIN KAPSAYICI ÖZELLİKLERİ**

Her kapsayıcıda ana programla birlikte, **veri**
**tabanları, yardımcı programlar** veya **izleyiciler**
(monitoring araçları) gibi **birçok** **destekleyici**
**program da dağıtılabilir.**
❖ **Kaynak Kullanımının Sınırlandırılması:**

Kapsayıcılar, **tüketecekleri altyapı kaynaklarının**
**miktarı sınırlanacak** şekilde **yapılandırılabilir.**


❖ **Dış Program ve Kaynaklara Erişimin Kısıtlanabilmesi:**
Bir kapsayıcıya ve onun içinde **çalışan programlara**
**erişebilecekleri** **dış programlar** ve **BT kaynakları**
**sınırlandırılabilir.**


Bir kapsayıcının içinde **çalışan programlar** genellikle
**kapsayıcıyla** **aynı yaşam döngüsünü paylaşır.**
Bu da, **programın** **başlatılması**, **durdurulması**,
**duraklatılması** ve **devam ettirilmesinin** **kapsayıcıyla**
**senkronize olduğu anlamına gelir.**


#### **5. KAPSAYICI İMAJLARINI ANLAMAK**

##### • Kapsayıcı imajları, kapsayıcılaştırma platformlarının merkezi bir parçasıdır . • Sürekli yeni kapsayıcıların oluşturulması bu imajlara dayanır . • Kapsayıcı imajlarının işlenmesi, kapsayıcı **motorunun temel sorumluluklarından biridir.**


#### **5.1. Kapsayıcı İmajı Türleri ve Rolleri**

**İki temel kapsayıcı imajı türü vardır:**

- **Temel (Base) Kapsayıcı İmajları:**
Bu kapsayıcı imajları, **özelleştirilmiş kapsayıcı imajları için**
**şablon** görevi görür.
Temel kapsayıcı imajları, **kısmi kapsayıcı imajları** olarak da
bilinir.

- **Özelleştirilmiş (Customized) Kapsayıcı İmajları:**
Bu kapsayıcı imajları, **kapsayıcı motoru tarafından**
**oluşturulur** ve **gerçek kapsayıcıları dağıtmak** için kullanılır.


- **Temel kapsayıcı imajı** olarak sınıflandırılan bir **kapsayıcı imajı**, **imaj kayıt**
**deposuna (image registry) yayımlanır.**

- Buradan da **kapsayıcı motoru tarafından** **erişilerek**, **özelleştirilmiş**
**kapsayıcı imajlarının temeli olarak kullanılabilir.**


**Kapsayıcı motoru**, kapsayıcılar içinde
dağıtılabilen **dört** **farklı** **çalışma**
**zamanını** (runtime) destekler.
**-Uygulama A**, Çalışma Zamanı A'nın
özelliklerine ihtiyaç duyar.
**-Temel Kapsayıcı İmajı A**, Kapsayıcı
Motoru tarafından özelleştirilmiş
**Kapsayıcı İmajı A** 'yı oluşturmak için
kullanılır.
-Bu imaj daha sonra **Uygulama A** için
gerçek **Kapsayıcı A'nın** oluşturulup
dağıtılmasında kullanılır.


#### **5.2. Kapsayıcı İmajlarının Değiştirilemezliği** **(Immutability)**
##### • Kapsayıcı imajlarının önemli bir özelliği, bir kez **oluşturulduktan sonra değiştirilemez** **olmalarıdır.** • Bu, yama yapılamayacağı, güncelleme uygulanamayacağı veya başka herhangi bir değişiklik yapılamayacağı anlamına gelir.


#### **5.2. Kapsayıcı İmajlarının Değiştirilemezliği** **(Immutability)**

##### • Bir kapsayıcı imajında değişiklik yapılması gerekiyorsa, yeni veya revize edilmiş bir yapı (build) dosyası oluşturulmalı ve yeni bir **kapsayıcı imajı üretilmelidir.** • Bu durum, dağıtılan kapsayıcının da yeni bir **sürümünün oluşturulması gerektiği anlamına** **gelir.**


#### **5.3. Kapsayıcı İmajı Soyutlaması**

###### • Bir temel kapsayıcı imajı, genellikle barındırıldığı **sunucu işletim sisteminin sunduğu işlevlerin** yalnızca bir alt kümesini sağlar. Bu duruma işletim sistemi soyutlaması (operating system abstraction) ya da kısaca soyutlama denir. • Ancak, kapsayıcı imajı, işletim sisteminin tüm bileşenlerini soyutlamaz .


##### ❖ İşletim Sistemi Çekirdeği Soyutlaması


- **Her işletim sistemi**, en temel işletim sistemi işlevlerinden
oluşan **bir çekirdeğe (kernel) sahiptir.**

- Farklı işletim sistemlerindeki **çekirdekler**, birbirine oldukça
benzer **işlevlerden oluşur.**

- Örneğin, **Windows işletim sisteminin çekirdeği**, **Linux**
**işletim sisteminin çekirdeğiyle** **benzer işlevlere** sahiptir.


#### ❖ İşletim Sistemi Çekirdeği Soyutlaması

**Bir çekirdek (kernel) tarafından sağlanan yaygın işlevler şunları**
**içerebilir:**

  - CPU kaynaklarına erişim

  - İşlem gücüne erişim

  - Sunucu belleğine erişim

  - Sunucudaki giriş/çıkış (I/O) cihazlarına erişim

  - Donanım depolama birimlerine erişim

  - Aygıt sürücülerine erişim

  - Sunucu dosya sistemlerine erişim

  - Güç yönetimine erişim

- **Çekirdek, kapsayıcı imajı tarafından soyutlanmaz.**

- **Bunun yerine, kapsayıcı motoru tarafından kapsanır (yönetilir).**


#### ❖ Çekirdek Dışındaki İşletim Sistemi **Soyutlaması**

❖ **İşletim sisteminin çekirdek dışındaki bölümleri**, **soyutlanarak**

**kapsayıcı imajına dahil edilebilir** .
❖ **Çekirdek dışında yer alan** ve **kapsayıcı imajına dahil edilebilecek**

yaygın **işletim sistemi işlevleri ve kaynakları şunlardır** :

  - Programlama dili kütüphaneleri ve derleyiciler

  - Çeşitli sistem kütüphaneleri

  - Şifreleme platformları

  - Sistem izleyiciler ve izleme işlevleri

  - Yapılandırma dosyaları ve düzenleyiciler

  - Yönetim işlevleri ve platformları

  - Yönetici araçları (insan yöneticiler tarafından kullanılmak üzere)

  - Yerelleştirme (dil, bölge uyumu) programları


##### ❖ Kapsayıcı Yapı Dosyaları (Container Build Files)


- **Kapsayıcı yapı dosyası** (veya sadece yapı
dosyası), **insan tarafından düzenlenebilir**,
**makine tarafından işlenebilir** bir **yapılandırma**
**dosyasıdır.**

- Bu dosya, **özelleştirilmiş bir kapsayıcı imajında**
nelerin **yer** **alacağını** (veya nelerin
soyutlanacağını) **tanımlar** .


**Yapı dosyasında şunlar belirtilir:**

- **Özelleştirilmiş kapsayıcı imajına eklenecek** (veya
soyutlanacak) **ek işletim sistemi kaynakları**

- Dağıtılacak özelleştirilmiş kapsayıcının **katılacağı**
**kapsayıcı ağı** veya **ağları**

- **Yapı dosyasının söz dizimi** ve **biçimi**,
**kullanılan kapsayıcı motorunun** türüne göre **değişiklik**
**gösterebilir.**


#### ❑ Kapsayıcı İmajı Katmanları


- Bir **kapsayıcı imajı**, içeriğini **katmanlar halinde organize eder** .
**Her katman**, **kapsayıcı yapı dosyasındaki bir ifade veya**
**talimata karşılık gelir** .
**Kapsayıcı imajı katmanlarında yer alabilecek içerik örnekleri**
**şunlardır:**

- Veri dosyaları ve klasörler

- Yapılandırma dosyaları

- Veri tabanları ve depolar (repository)

- Çalıştırılabilir dosyalar (executable files)

- İşletim sistemi program dosyaları ve çalışma zamanları
(runtimes)


- **En son katman hariç**, kapsayıcı imajındaki
**tüm katmanlar salt okunur (read-only)**
durumdadır.

- Kapsayıcılaştırma platformu, **kapsayıcı imajı**
**katmanlarının** temelini oluşturmak için
**birlikte dosya sistemi (union file system)**
kullanır.

- **Bu** **birlikte dosya sistemi ve katmanlama**
**yöntemi**, **temel kapsayıcı imajlarının**
**yeniden kullanılabilirliğini** **mümkün kılar.**


- **Temel kapsayıcı imajından türetilen özelleştirilmiş**
**kapsayıcı imajı**, **temel imajda bulunan içeriklerin üzerine**
**yeni katmanlar ekler** .

- **Özelleştirilmiş kapsayıcı imajında**, **tüm temel kapsayıcı**
**imajı**, **en alt katman olarak** yer alır.


 - **Özelleştirilmiş kapsayıcı imajından** oluşturulup **dağıtılacak kapsayıcıda**
**barındırılacak** **bir yazılım programı**, **özelleştirilmiş kapsayıcı imajının bir**
**katmanında yer alabilir.**


Özelleştirilmiş kapsayıcı imajındaki **bir**
**katman**, dağıtılacak kapsayıcının
barındırmasından sorumlu **olacağı**
**yazılım programından oluşur.**


**imajı sürümü oluşturulmalıdır** .


#### Özelleştirilmiş Kapsayıcı İmajları Nasıl Oluşturulur?

- **Kapsayıcı motoru**, **yapı dosyasını** ve **temel kapsayıcı**
**imajını** birlikte kullanarak **özelleştirilmiş kapsayıcı**
**imajını oluşturur.**
**(1)** Yönetici, **Kapsayıcı A** için bir **yapı dosyası hazırlar**
**(2)** Yönetici bu yapı dosyasını **kapsayıcı motoruna**
**sağlar.**
**(3) Kapsayıcı motoru**, gerekli **temel kapsayıcı imajını**
imaj **kayıt deposundan alır.**
**(4) Ardından kapsayıcı motoru**, **temel kapsayıcı**
**imajını** ve **yapı dosyasındaki bilgileri** kullanarak **yeni**
**bir özelleştirilmiş** Kapsayıcı İmajı A oluşturur.
Bu imajdan **Kapsayıcı A** ’yı oluşturup dağıtır.


- **Özelleştirilmiş kapsayıcı imajından** **gerçek kapsayıcı**
**uygulaması oluşturulup dağıtıldıktan sonra,** **yapı**
**dosyasını saklamaya gerek kalmayabilir** .

- Çünkü kapsayıcı motoru, **gelecekte daha fazla kapsayıcı**
**örneği oluşturmak** için **özelleştirilmiş kapsayıcı** imajına
**zaten sahiptir** .

- Dikkat edilmesi gereken bir diğer nokta da,
**özelleştirilmiş kapsayıcı imajlarının genellikle imaj kayıt**
**deposunda** **değil**, **kapsayıcı** **motorunun** **dahili**
**depolamasında saklanmasıdır** .


##### • Kapsayıcı imajlarının kapsayıcı motorunun dahili depolamasında saklanmasıyla kapsayıcı motoru, **yeni kapsayıcı örneklerini hızlı ve verimli bir** şekilde oluşturabilmek için doğrudan erişim sağlayabilir. • Bununla birlikte, yönetici, bu özelleştirilmiş **kapsayıcı imajının yeni tür özelleştirilmiş imajlar** için temel olarak kullanılabileceğine karar verirse, bu imajı imaj kayıt deposuna da yayımlayabilir .


#### **6. ÇOKLU KAPSAYICI TÜRLERİ**

##### **Temel çoklu kapsayıcı türleri tanıtılmaktadır:** • Sidecar Kapsayıcı (Sidecar Container) • Adaptör Kapsayıcı (Adapter Container) • Elçi Kapsayıcı (Ambassador Container)


##### **6.1. Sidecar Kapsayıcı**

❖Bir uygulama, **hem birincil iş mantığını** **hem de genel**

**yardımcı** (utility) **işlemleri gerçekleştirecek** şekilde

**işlemesi risk altına girebilir.**


**Uygulama A**, hem **iş mantığını** hem
de **yardımcı işlemleri** (Örneğin Log
toplama ve aktarma, sıkıştırma vb.)
**yerine getirme yükünü**
**taşımaktadır.**


##### **6.1. Sidecar Kapsayıcı**

❖ **Bu** **durumu** **önlemek** **için**,
**yardımcı** **işlemleri** **soyutlamak**
üzere **ikincil** **bir**
**kapsayıcılaştırılmış** **bileşen**
(sidecar bileşeni) **eklenir** .

- **Sidecar** **bileşeni**, genellikle
uygulamayla **aynı pod içinde**, **ayrı**
**bir kapsayıcı** olarak dağıtılır.

- **Yardımcı işlemin niteliğine bağlı**
**olarak,** uygulamanın **sidecar**
**bileşeniyle** **iletişim** **kurması**
**gerekebilir veya gerekmez** .


#### **6.2. Adaptör Kapsayıcı (Adapter Container)**

- Bir uygulama, **birincil** **iş**
**mantığını yürütmenin** yanı sıra,
harici tüketici uygulamalara
uyum sağlamak için **veri**
**dönüştürme** **işlemleri** de
yapacak şekilde tasarlandığında,
iş mantığını güvenilir ve etkili bir
şekilde işleyebilme **yeteneği**
**zayıflayabilir.**


**B** tarafından gereken **özel dönüştürme** işlemlerini **gerçekleştirmekle**
**yüklenmiş durumdadır.**


#### **6.2. Adaptör Kapsayıcı (Adapter Container)**


- **Gerekli veri dönüştürme işlemlerini soyutlamak** amacıyla,
**ikincil bir kapsayıcılaştırılmış uygulama bileşeni** (adaptör bileşeni olarak
adlandırılır) **eklenir.**


Dönüştürme (conversion) mantığı, aynı pod içinde yer alan, ayrı bir Kapsayıcı B'de bulunan Adaptör Bileşeni A'ya
yerleştirilir.
Bu sayede Uygulama A,yalnızca kendi iş mantığını yürütmeye odaklanabilir.


#### **6.3. Elçi (Ambassador) Kapsayıcı**

  - **Birincil iş mantığını işleyen bir uygulama**, **harici tüketici**
**uygulamalarla bağlantı kurmak** için **dış iletişim işlemlerini**
**de yürütmek üzere tasarlandığında**, **iş mantığını güvenilir** ve
**etkili bir şekilde işleyebilme yeteneği tehlikeye girebilir.**


- **Uygulama A**, hem **kendi iş**
**mantığını yürütmekle**, hem de
**Uygulama** **B** ile **bağlantı**
**kurmak için gerekli** olan **özel**
**iletişim** **işlemlerini**
**gerçekleştirmekle** **yüklenmiş**
**durumdadır.**


- Gerekli iletişim işlemlerini soyutlamak amacıyla, **ikincil**
**bir kapsayıcılaştırılmış uygulama** bileşeni (elçi bileşeni
olarak adlandırılır) **eklenir.**

- İletişim mantığı, **aynı pod**
**içinde bulunan**, ayrı bir
**Kapsayıcı B** ’de yer alan
**Elçi** **Bileşeni** **A’ya**
yerleştirilir.

- Bu sayede **Uygulama A**,
**yalnızca** **kendi** **iş**
**mantığını** **yürütmeye**
odaklanabilir.


#### ❖ Çoklu Kapsayıcıların Birlikte Kullanılması


- **Bu** **üç** **çoklu** **kapsayıcı** **türü**,
gereksinimlere bağlı olarak **ayrı ayrı**
**veya birlikte kullanılabilir.**

- Örneğin, **iş mantığının doğasına**
**bağlı olarak**, **bir uygulamanın bazı**
veya **tüm yardımcı kapsayıcıların**
**birlikte** **dağıtılmasına** **ihtiyaç**
**duyması söz konusu olabilir.**


#### KAYNAKLAR


- Thomas Erl, Eric Monroy - Cloud Computing_ Concepts, Technology,
Security, and Architecture (The Pearson Digital Enterprise Series from
Thomas Erl)-Pearson (2023)


