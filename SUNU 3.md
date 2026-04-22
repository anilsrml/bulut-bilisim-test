 PDF To Markdown Converter
Debug View
Result View
# Temel Kavramlar ve

# Modeller


## KONU BAŞLIKLARI

### 1. Roller ve Sınırlar

### 2. Bulut Özellikleri

### 3. Bulut Hizmet Modelleri

### 4. Bulut Dağıtım Modelleri


## 1. Roller ve Sınırlar

##### Kuruluşlar ve insanlar, bir bulut ve barındırdığı BT

##### kaynaklarıyla nasıl ilişkilendiklerine ve/veya etkileşimde

##### bulunduklarına bağlı olarak farklı türde önceden

##### tanımlanmış rolleri üstlenebilirler.


#### Bulut Sağlayıcısı

- Bulut tabanlı BT **kaynaklarını sağlayan kuruluş** , bulut **sağlayıcısı**
    olarak **adlandırılır**.
- Bir kuruluş, bulut sağlayıcısı rolünü üstlendiğinde, bulut
    tüketicilerine hizmetleri sağlamakla ve bu hizmetlerin, üzerinde
    anlaşılan SLA (Hizmet Düzeyi Anlaşmaları) kapsamında belirtilen
    **taahhütleri karşılamasıyla** sorumludur.
- Bulut sağlayıcısı ayrıca, bulut **altyapısının sürekli** olarak
    **çalışmasını sağlamak** için gerekli **yönetim** ve idari **görevleri**
    yerine getirmekle yükümlüdür.


#### Bulut Tüketicisi

- Bulut **tüketicisi,** bir bulut sağlayıcısı ileBT kaynaklarını kullanmak
    üzere resmi bir sözleşme veya anlaşma yapmış olan bir **kuruluş**
    veya bireydir.


- Genellikle **“bulut** hizmeti **tüketicisi”** terimi, bir bulut hizmetinin
    teknik **sözleşmesi** veya **API’si** ile **programlı** olarak **etkileşime**
    giren **yazılım programlarını** veya **uygulamaları tanımlamak** için
    kullanılır.
- Buna karşılık “bulut **tüketicisi** ” terimi daha geniş bir kapsama
    sahiptir ve şu durumları ifade edebilir:
       - Bir kuruluş,
       - Bir kullanıcıarayüzü üzerinden erişim sağlayan birey,
       - Bir yazılımprogramı
- Bu **yazılım programı,** bir bulut, bulut tabanlı bir BT kaynağı veya
    bir bulut sağlayıcısı ile **etkileşime girdiğinde** bulut **tüketicisi**
    **rolünü** üstlenebilir.
- Ders **kapsamında** bulut **tüketicisi** terimi **kullanılacaktır**.


#### Bulut Aracısı (Cloud Broker)

- Bulut **aracısı** , _bir bulut tüketicisi adına bulut hizmetlerini_
    **_müzakere etme_** , **yönetme** ve **işletme sorumluluğunu** üstlenen
    **üçüncü** tarafbir **kuruluştur**.
- Bulut **aracısı** , bulut tüketicileri ile bulut sağlayıcıları arasında
    **aracı** hizmetleri sunabilir.

Buhizmetler **şunları içerebilir** :

- Aracılık (intermediation)
- Toplulaştırma(aggregation)
- Hakemlik(arbitrage)
- Diğeryönetim veentegrasyon işlemleri


**Şekil** : Bir bulut **aracısı** , üç
farklı bulut sağlayıcısına ait
bulut tabanlı hizmetleri ve BT
kaynaklarını kendi
müşterilerinesunar.

Bu müşteriler Bulut
TüketicileriA,BveC’dir.


#### Bulut Hizmeti Sahibi (Cloud Service Owner)

- Bir bulut hizmetinin yasal sahibi
    **olan kişi** veya **kuruluş** , "Bulut
    Hizmeti Sahibi" olarak
    adlandırılır.
- Bulut **tüketicisi** (Cloud
    Consumer), kendi bulut
    hizmetini (Cloud Service A) bir
    bulut **sağlayıcısına** ait olan
    bulut **ortamı** (Cloud X) **içinde**
    **dağıtmıştır**.
- Bu nedenle bulut hizmeti sahibi
    (Cloud Service Owner) rolünü de
    olmuştur.


#### Bulut Hizmeti Sahibi (Cloud Service Owner)

- Bir bulut sağlayıcısı, genellikle
    **diğer** bulut **tüketicilerinin**
    **kullanması** için kendi bulut
    hizmetini **dağıtırsa** bulut
    hizmeti sahibi olur.


##### Bulut Kaynak Yöneticisi (Cloud Resource Administrator)

Bulut kaynak **yöneticisi şu** taraflardanbiri olabilir:

- Bulut **tüketicisi** veya bulut **sağlayıcısı bünyesinde çalışan** bir
    **yönetici,**


##### Bulut Kaynak Yöneticisi (Cloud Resource Administrator)

Bulut kaynak **yöneticisişu** taraflardanbiriolabilir:

- Bulut hizmetinin **bulunduğu** bulutunsahibi olanbulutsağlayıcısı,
- Bu yönetim görevini yerine getirmek için **sözleşme yapılmış üçüncü** taraf
    birkuruluş.


##### Ek Roller (Additional Roles)

- **Bulut Denetçisi (Cloud** Auditor)

Bulut ortamlarının **bağımsız değerlendirmelerini** yapan **üçüncü**
bir taraf (genellikleakredite) bulut denetçisi rolünü üstlenir.

Bu rolle ilişkili tipik sorumluluklar arasında **güvenlik**
kontrollerinin, gizlilik etkilerinin ve **performansın
değerlendirilmesi** yer alır.

Bulut denetçisi rolünün temel amacı, bulut **tüketicileri** ile bulut
**sağlayıcıları arasındaki güven ilişkisini güçlendirmeye** yardımcı
olmak için bir bulut ortamının **tarafsız** bir **değerlendirmesini** (ve
**olası onayını)sağlamaktır**.


##### Ek Roller (Additional Roles)

- **Bulut Taşıyıcısı (Cloud Carrier)**

Bulut **tüketicileri** ile bulut **sağlayıcıları arasındaki bağlantıyı
sağlayan tarafı** temsil eder.

Genellikle **ağ** ve **telekomünikasyon** sağlayıcılarıbu **rolüüstlenir**.

Bulut hizmetlerinin **erişilebilirliğini** ve **sürekliliğini sağlamak** için
gerekli **ağ altyapısını yönetir**.


##### Organizasyonel Sınır (Organizational Boundary)

- Organizasyonel **sınır,** bir **kuruluşun**
    sahip **olduğu** ve y **önettiği** bir dizi BT
    **kaynağını çevreleyen** fiziksel **sınırı**
    temsil eder.
- Ancak, bu sınır doğrudan bir kuruluşun
    fiziksel sınırlarını değil, yalnızca onun
    **kontrolündeki** BT **varlıklarını** ve
    **kaynaklarını** kapsar.

```
Şekil : Bulut tüketicisinin (sol) ve bulut
sağlayıcısının (sağ) organizasyonel sınırları,
kesik çizgi gösterimiyle gösterilmektedir.
```

##### Güven Sınırı (Trust Boundary)

- Bir kuruluş, bulut **tüketicisi rolünü**
    **üstlenerek** bulut **tabanlı** BT **kaynaklarına**
    **eriştiğinde** , **güvenini yalnızca** kendi fiziksel
    **sınırlarıyla sınırlı** tutamaz.
- Bunun yerine, bulut ortamının belirli
    **bölümlerini** de **güvenilir** kabul etmek
    **zorundadır**.
- **Güven sınırı,** fiziksel sınırların ötesine uzanan
    ve hangi BT **kaynaklarının güvenilir** kabul
    **edildiğini** belirten **mantıksal** bir **çerçevedir**.


## 2. Bulutun Özellikleri (Cloud Characteristics)

```
Bir BT ortamının , uzaktan ölçeklenebilir ve ölçülebilir BT
kaynaklarının etkin bir şekilde sağlanmasını mümkün kılmak için
belirli özelliklere sahip olması gerekir.
Çoğu bulut ortamında ortak olan temel özellikler şunlardır:
```
- Talebe **bağlı kullanım** (On-demand usage)
- Her yerden **erişim** (Ubiquitous access)
- **Çoklu kiracılık** ve kaynak havuzu (Multitenancy & Resource
    Pooling)
- Esneklik (Elasticity)
- **Ölçülebilir** kullanım (Measured usage)
- **Dayanıklılık** (Resiliency)


**Şekil** : Tek **kiracı ortamında** , her
bulut tüketicisinin **ayrı** bir BT
kaynak **örneği vardır**.

```
Şekil : Çoklu kiracı ortamında, bulut
depolama aygıtı gibi bir BT kaynağının
tek bir örneği , birden fazla tüketiciye
hizmet eder.
```
##### Örnek: Çoklu kiracılık ve kaynak havuzu


```
Şekil : Cloud B, Cloud A'daki Cloud
Service A'nın devre dışı kalması
durumunda hizmetin kesintisiz
devam etmesini sağlamak amacıyla ,
Cloud Service A'nın yedek bir
uygulamasını barındıran dayanıklı bir
sistem sunar.
```
##### Örnek: Dayanıklılık

##### (Resiliency)


## 3. Bulut Hizmet Modelleri (Cloud Delivery

## Models)

```
Bulut bilişim, farklı hizmet modelleri aracılığıyla BT kaynaklarının
sağlanmasını ve yönetilmesini mümkün kılar.
En yaygın üç bulut hizmet modeli şunlardır :
Çoğu bulut ortamında ortak olan temel özellikler şunlardır :
```
- Hizmet Olarak **Yazılım** (SaaS - Software as a Service)
- Hizmet Olarak Platform (PaaS - Platform as a Service)
- Hizmet Olarak **Altyapı** (IaaS - Infrastructure as a Service)


#### Hizmet Olarak Yazılım (SaaS - Software as a Service)

- Paylaşımlı bir bulut hizmeti olarak konumlandırılan ve bir "ürün"
    veya genel bir yardımcı program olarak kullanıma sunulan bir
    yazılım programıdır.
- Bulut hizmeti **tüketicisine** **_bulut hizmeti sözleşmesine erişim_**
    **_hakkı verilir,_** ancak herhangi bir temel BT **kaynağına** veya
    uygulama **ayrıntısına erişim hakkı** verilmez.
- **Örnekler** :

Google Docs,

Microsoft 365 ,

Dropbox


### Hizmet Olarak Platform (PaaS - Platform as a Service)

- Genellikle **önceden dağıtılmış** ve **yapılandırılmış** BT **kaynaklarından**
    oluşan önceden tanımlanmış **"kullanıma hazır"** bir ortamı temsil eder.
Bir bulut **tüketicisinin** PaaS **ortamını kullanmasının** ve **yatırım
yapmasının yaygın** nedenleri şunlardır:
- Bulut **tüketicisi, ölçeklenebilirlik** ve ekonomik **amaçlar** için **şirket içi**
    **ortamları** buluta **genişletmek** ister.
- Bulut tüketicisi, **hazır ortamı şirket içi** bir **ortamın** tamamen yerini
    almak için kullanır.
- Bulut **tüketicisi** , bir bulut **sağlayıcısı** olmak ister ve diğer harici bulut
    tüketicilerine sunulmak üzere kendi bulut hizmetlerini **dağıtır**.


### Hizmet Olarak Platform (PaaS - Platform as a Service)

- **Hazır** bir platformda
    **çalışarak** , bulut **tüketicisi**
    IaaS modeli **aracılığıyla**
    **sağlanan yalın altyapı** BT
    **kaynaklarını** kurma ve
    **sürdürme** idari **yükünden**
    kurtulur.
- **Örneğin** Google App Engine
    Java ve Python **tabanlı**
    ortamlar sunar.
-


#### Hizmet Olarak Altyapı (IaaS - Infrastructure as a Service)

- Bulut hizmeti tabanlı **arayüzler** ve araçlar aracılığıyla erişilebilen ve
    **yönetilebilen altyapı** merkezli BT **kaynaklarından** oluşan kendi
    kendine yeten bir BT **ortamını** temsil eder.
- Bu ortam donanım, **ağ, bağlantı, işletim** sistemleri ve **diğer** "ham"
    BT **kaynaklarını içerebilir**.
- Geleneksel **barındırma** veya **dış** kaynak **ortamlarının** aksine, IaaS
    ile BT **kaynakları** genellikle **sanallaştırılır** ve **altyapının önceden**
    **çalışma zamanı ölçeklenmesini** ve **özelleştirilmesini basitleştiren**
    paketler halinde paketlenir.


#### Hizmet Olarak Altyapı (IaaS - Infrastructure as a Service)

- Bir bulut **tüketicisi** , bir IaaS
    ortamında sanal bir sunucu
    kullanır.
- Bulut **tüketicilerine** , kapasite,
    performans ve **kullanılabilirlik**
    gibi özelliklerle ilgili olarak bulut
    **sağlayıcısı tarafından** bir dizi
    **sözleşmesel** garanti **sağlanır**.


#### Bulut Dağıtım Modellerini Karşılaştırma


##### Bulut Hizmet Modelleri: Tüketici ve Sağlayıcı Etkinlikleri


### Bulut Hizmet Modellerinin Birleştirilmesi

### (Combining Cloud Delivery Models)

- Bulut bilişimde, SaaS, PaaS ve IaaS hizmet modelleri genellikle
    birbirini tamamlayacak şekilde entegre edilir.
- Bu yaklaşım, organizasyonların esneklik **kazanmasını** ,
    maliyetleri optimize etmesini ve teknik **ihtiyaçlarına** uygun bir
    **yapı oluşturmasını sağlar**.


## IaaS + PaaS

- Bir PaaS ortamı, bir IaaS ortamında sağlanan fiziksel ve sanal
    sunuculara ve **diğer BT kaynaklarına** benzer bir **temel altyapı**
    **üzerine inşa edilecektir.**

**Şekil** : Altta yatan bir IaaS

**ortamının sağladığı** BT

kaynaklarına dayalı PaaS

**ortamı**


## IaaS + PaaS

- **Bazı** durumlarda, belirli bir
    bulut **tüketicisi** , verilerin
    fiziksel olarak belirli bir
    **bölgede saklanmasını** yasal
    olarak zorunlu **kılabilir**.
- Bulut **Sağlayıcı** X ve Bulut
    **Sağlayıcı** Y arasındaki bir
    **sözleşme kapsamında** , Cloud
    Provider X tarafından sunulan
    hizmetler, Cloud Provider Y'ye
    ait sanal sunucular **üzerinde**
    **barındırılmaktadır**.


## IaaS + PaaS + SaaS

- **Üç** bulut **dağıtım** modelinin
    hepsi, birbirinin **üzerine inşa**
    edilen BT **kaynaklarının**
    katmanlarını oluşturmak için
    **birleştirilebilir**.


#### Bulut Hizmet Alt Modelleri (Cloud Delivery Submodels)

- Bulut dağıtım modellerinin **birçok özel çeşidi vardır** ve her biri **farklı**
    BT **kaynakları** kombinasyonundan **oluşur**.
- Bu bulut dağıtım alt modelleri de genellikle "hizmet olarak" kuralı
    kullanılarak **adlandırılır** ve her biri **üç** temel bulut **dağıtım**
    modelinden birine **eşlenebilir**.

Örneğin, yandaki şekilde Hizmet
Olarak **Veritabanı** alt modeli
**verilmiştir**.
Bir **veritabanı** sistemi genellikle bir
PaaS platformunun parçası olan
**hazır ortamın** bir **bileşeni**
olduğundan PaaS modeline aittir.


#### Bulut Hizmet Alt Modelleri (Cloud Delivery Submodels)

- Başka bir örnek ise, bulut **sağlayıcısının** bulut **tüketicilerine** bulut
    depolama ile ilgili hizmetler sunmak için kullanabileceği IaaS'nin
    Depolama Hizmeti alt modeli olarak aşağıdaki şekilde verilmiştir.

Bir Hizmet Olarak Depolama teklifi,
**yapılandırılmış** ve **yapılandırılmamış**
veri depolama, dosya depolama,
nesne depolama ve uzun vadeli **arşiv**
depolama gibi farklı depolama ile ilgili
hizmetler **sağlayabilir**.


#### Bulut Hizmet Alt Modelleri (Cloud Delivery Submodels)

- SaaS'ın bir alt modeli olarak da kabul
    edilen bulut yerel (native) **dağıtım**
    alt modeli, bulut yerel
    **uygulamalarının** hafif
    **kapsayıcılarda paketlenmiş** kendi
    kendine yeten hizmet
    **koleksiyonları** olarak
    **oluşturulmasına** ve **dağıtılmasına**
    olanak **tanır**.


#### Bulut Hizmet Alt Modelleri (Cloud Delivery Submodels)

**Yaygın** bulut **dağıtım** alt modellerinin diğer **örnekleri şunlardır** (ancak
bunlarla **sınırlı değildir)** :

- Hizmet Olarak İletişim (SaaS'ın bir alt modeli)
- Hizmet Olarak Entegrasyon (PaaS'ın bir alt modeli)
- Hizmet Olarak Test (SaaS'ın bir alt modeli)
- Hizmet Olarak Süreç (SaaS'ın bir alt modeli)
- Hizmet Olarak Masaüstü (IaaS'ın bir alt modeli)


## 4. Bulut Dağıtım Modelleri

❖Dört yaygın bulut dağıtım modeli vardır:

- Genel/Kamu (Public) Bulut
- Özel (Private) Bulut
- Çoklu Bulut (Multiclouds)
- Hibrit Bulut


### Genel/Kamu (Public) Bulut

- Genel bulutlardaki BT kaynakları
    genellikle daha **önce açıklanan**
    bulut **dağıtım** modelleri
    aracılığıyla sağlanır ve genellikle
    bulut **tüketicilerine** bir maliyetle
    sunulur veya diğer yollarla (reklam
    gibi) ticarileştirilir.
- Bulut sağlayıcısı, genel bulutun ve
    BT **kaynaklarının**
    **oluşturulmasından** ve **sürekli**
    **bakımından** sorumludur.


### Özel (Private) Bulut

- Özel bir bulut tek bir kuruluşa aittir.
- Özel bulutlar, bir **kuruluşun** bulut
    **bilişim** teknolojisini, **kuruluşun**
    **farklı bölümleri** , **konumları** veya
    **departmanları** tarafından BT
    **kaynaklarına erişimi**
    **merkezileştirmenin** bir yolu olarak
    kullanmasını **sağlar**.


### Çoklu Bulut (Multiclouds)

- Çoklu bulut dağıtım modeliyle, bir
    bulut tüketici kuruluşu, yandaki
    şekilde gösterildiği gibi, birden
    fazla bulut **sağlayıcısı** tarafından
    sağlanan **farklı** genel bulutlardaki
    bulut hizmetlerini ve BT
    **kaynaklarını** kullanabilir.


### Hibrit Bulut (Hybrid Clouds)

- Hibrit bulut, iki veya daha fazla
    **farklı** bulut dağıtım modelinden
    oluşan bir bulut ortamıdır.
- Örneğin, bir bulut **tüketicisi**
    hassas verileri işleyen bulut
    hizmetlerini **özel** bir buluta ve
    diğer, daha az hassas bulut
    hizmetlerini genel bir buluta
    **dağıtmayı** seçebilir.


## KAYNAKLAR

- Thomas Erl, Eric Monroy - Cloud Computing_ Concepts,
    Technology, Security, and Architecture (The Pearson Digital
    Enterprise Series fromThomas Erl)-Pearson ( 2023 )



This is a offline tool, your data stays locally and is not send to any server!
Feedback & Bug Reports