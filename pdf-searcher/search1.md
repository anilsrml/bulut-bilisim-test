# SINAV NOTLARI — Bulut Destekleyici Teknolojiler (SUNU 4 & 5)

---

## 1. AĞLAR VE İNTERNET MİMARİSİ

- Tüm bulutlar bir ağa bağlı olmak zorundadır.
- Bulut tüketicileri yalnızca **LAN'lardaki özel ve adanmış ağ bağlantılarını** kullanarak buluta erişebilir.
- Bulut platformlarının potansiyeli, **internet bağlantısı ve hizmet kalitesindeki** gelişmelerle paralel artar.
- İSS'lerin kurduğu omurga ağları, **çekirdek yönlendiriciler** aracılığıyla birbirine bağlanır.

### İnternet Servis Sağlayıcıları (İSS)

- İnternetin topolojisi İSS'lerin **dinamik ve karmaşık** bir toplamıdır.
- İnternet ağı mimarisinin **iki temel bileşeni**:
  1. **Bağlantısız Paket Anahtarlama (Datagram Ağları)**
  2. **Yönlendirici Tabanlı Bağlantılılık**

### Bağlantısız Paket Anahtarlama

- Veri akışları sınırlı boyutlardaki **paketlere bölünür**.
- Her paket, **IP veya MAC adresi** gibi konum bilgilerini taşır.
- Paketler switch ve router'lar aracılığıyla **bir düğümden diğerine iletilir**.

### Yönlendirici Tabanlı Bağlantılılık

- Yönlendirici: birden fazla ağa bağlı, paketleri ileten cihaz.
- Her paketi **ayrı ayrı** işler; kaynak-hedef arasındaki **ağ topolojisi bilgilerini korur**.
- Paket teslimi için **en verimli atlamayı** ölçer.

---

## TCP/IP MODELİ (Internet Referans Modeli)


| Katman                       | Açıklama                                             |
| ------------------------------ | -------------------------------------------------------- |
| **Fiziksel Katman**          | Bit düzeyinde iletim (kablolu/kablosuz)               |
| **Veri Bağlantı Katmanı** | Komşu düğümler arası veri transferi kontrolü     |
| **İnternet Katmanı**       | IP adresleri eklenir → Datagram (veri bloğu) oluşur |
| **Taşıma Katmanı**        | TCP ve UDP → Uçtan uca iletişim                     |
| **Uygulama Katmanı**        | HTTP, SMTP, BitTorrent, SIP vb.                        |

- **TCP** = güvenilir, bağlantı yönelimli
- **UDP** = hızlı, bağlantısız
- HTTP (web), SMTP (e-posta), BitTorrent (P2P), SIP (VoIP)

---

## Teknik Değerlendirmeler

### Bant Genişliği ve Gecikme (Latency)

- **Gecikme** = bir paketin bir düğümden diğerine gitmesi için geçen süre.
- **"En iyi çaba" QoS** → paketler ilk gelen/ilk hizmet esasıyla iletilir.
- **Bant genişliği**: büyük veri aktarımı gereken uygulamalar için kritik.
- **Gecikme**: hızlı yanıt süresi gerektiren uygulamalar için kritik.
- İnternet gecikmesi **trafik koşullarına bağlı** → tahmin edilemez.

### Kablosuz ve Hücresel Bağlantı

- Mobil istemcilere yönelik bulut çözümleri **kablosuz/hücresel bağlantı** üzerinden erişilebilir olmalıdır.

---

## 2. BULUT VERİ MERKEZİ TEKNOLOJİSİ

- BT kaynaklarını **yakın mesafede gruplamak** → güç paylaşımı, yüksek verimlilik, daha iyi erişilebilirlik.
- Modern veri merkezleri: sunucular, veritabanları, ağ/telekomünikasyon cihazları ve yazılım sistemlerini barındırır.

### Veri Merkezi Temel Özellikleri


| Özellik                          | Açıklama                                                      |
| ----------------------------------- | ----------------------------------------------------------------- |
| **Sanallaştırma**               | Hem fiziksel hem sanal BT kaynaklarından oluşur               |
| **Standardizasyon & Modülerlik** | Maliyetleri azaltır, ölçek ekonomisi sağlar                 |
| **Otonom Bilişim**               | İnsan müdahalesi olmadan kendi kendini yönetme               |
| **Uzaktan Yönetim**              | Uzak konsol ve yönetim sistemleriyle komuta edilir             |
| **Yüksek Kullanılabilirlik**    | Yedekli güç, kablolama, yük dengeleme, kümelenmiş donanım |
| **Güvenlik Odaklı Tasarım**    | Fiziksel + mantıksal erişim kontrolü, veri kurtarma          |
| **Tesisler**                      | Isıtma, havalandırma, iklimlendirme, yangın koruması        |
| **Bilgisayar Donanımı**         | Standartlaştırılmış ticari sunucular                       |

### Otonom Bilişim – 4 Öz-Yönetim Özelliği

1. **Kendi kendine yapılandırma (Self-Configuration):** Politikalara yanıt olarak otomatik yapılandırma.
2. **Kendi kendine optimizasyon:** Çalışma zamanında parametreleri değiştirerek performansı iyileştirme.
3. **Kendi kendini iyileştirme (Self-Healing):** Donanım/yazılım arızasından otomatik kurtarma.
4. **Kendi kendini koruma (Self-Protection):** Kötü niyetli saldırılara ve kademeli arızalara karşı savunma. *(Veri bilimi + yapay zeka ile güçlendirilir)*

### Sunucusuz Ortam (Serverless)

- Uygulamalar için çalışma zamanı kaynaklarını **otomatik sağlar**.
- Temel kaynakları kurmaya gerek kalmadan dağıtılabilir.

### NoSQL Kümeleme

- Dağıtık ortamlar için kullanılabilir.
- Çeşitli bulut tabanlı çözümler için dağıtım ortamı olarak görev yapar.

### Veri Merkezi Diğer Hususlar


| Sorun                          | Açıklama                                                                                                            |
| -------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| **Performans Yükü**          | Yüksek iş yüklü kompleks sistemlerde sanallaştırma ideal olmayabilir                                            |
| **Özel Donanım Uyumluluğu** | Bazı donanımlar sanallaştırma yazılımıyla uyumsuz olabilir; konteynerleştirme bunu çözer                    |
| **Taşınabilirlik**           | OVF (Açık Sanallaştırma Formatı) bu sorunu çözmeye adanmış; konteynerler çok yüksek taşınabilirlik sunar |

---

## 3. MODERN SANALLAŞTIRMA

### 3.1 Donanım Bağımsızlığı

- **Sanallaştırma**: benzersiz BT donanımını öykünülmüş ve standartlaştırılmış yazılım kopyalarına çeviren dönüştürme işlemi.
- Sanal sunucular farklı sanallaştırma ana bilgisayarlarına **kolayca taşınabilir**.
- Sanal BT kaynaklarını klonlamak/manipüle etmek, fiziksel donanımı kopyalamaktan **çok daha kolay**.

### 3.2 Sunucu Konsolidasyonu

- Birden çok sanal sunucu **aynı fiziksel sunucuyu paylaşabilir** → **Sunucu Konsolidasyonu**.
- Amaç: donanım kullanımını, yük dengelemesini ve BT kaynaklarının optimizasyonunu artırmak.

### 3.3 Kaynak Çoğaltma (Resource Replication)

- Sanal sunucular → **sanal disk görüntüleri** olarak oluşturulur (sabit diskin ikili kopyaları).
- Kopyalama, taşıma, yedekleme → basit **dosya işlemleriyle** yapılabilir.

### 3.4 İşletim Sistemi Tabanlı Sanallaştırma (Type 2 Hypervisor)

- Sanallaştırma yazılımı **mevcut bir işletim sistemine** (host OS) yüklenir.
- Örnekler: **VirtualBox, VMware Workstation**
- Katman sırası (aşağıdan yukarıya):
  1. Hardware (fiziksel bilgisayar)
  2. Operating System (host OS, örn. Windows 10)
  3. Virtual Machine Management (hypervisor uygulama olarak)
  4. VM (guest OS + uygulama — Ubuntu, Debian vb.)
- **Avantaj:** Host OS'un yedekleme, dizin servisleri, güvenlik yönetimi gibi araçlarını kullanabilir.
- **Dezavantaj:** Host OS CPU, bellek ve diğer kaynakları tüketir.

### 3.5 Donanım Tabanlı Sanallaştırma (Type 1 Hypervisor / Bare-metal)

- Sanallaştırma yazılımı **doğrudan fiziksel donanıma** yüklenir.
- Başka bir host OS gerektirmez.
- **Hipervizör** = ince bir yazılım katmanı, donanım yönetimini üstlenir.
- Örnekler: **VMware ESXi, Microsoft Hyper-V (sunucu), Xen, KVM**
- Tüm aygıt sürücüleri hipervizörle **uyumlu olmak zorundadır**.

### 3.6 Konteynerler ve Uygulama Tabanlı Sanallaştırma

- **Uygulama sanallaştırma**: OS'a bağımlı olmadan uygulama oluşturma/kullanma.
- **Konteynerler**: bağımsız, kendi içinde çalışan uygulamaları barındırır.
- Konteynerleştirme motoru kurulu olan **her ortama dağıtılabilir**.
- **Docker** → 2013'te Docker Inc. tarafından piyasaya sürüldü; konteyner teknolojisinin temel aracı.

#### Konteynerin 5 Temel Avantajı


| # | Avantaj                                   | Açıklama                                                                |
| --- | ------------------------------------------- | --------------------------------------------------------------------------- |
| 1 | **Taşınabilirlik**                      | Tüm bağımlılıklar konteyner içinde → her ortamda aynı çalışır |
| 2 | **Hızlı Dağıtım**                    | Tam OS sanallaştırmasına gerek yok → daha hızlı başlatılır       |
| 3 | **İzolasyon**                            | Bir konteyner diğerini etkilemez                                         |
| 4 | **Mikro Servisler & Ölçeklenebilirlik** | Her servis bağımsız konteynerde; ihtiyaca göre ölçeklenir           |
| 5 | **Bulut Uyumluluğu**                     | AWS, Google Cloud, Azure'da aynı şekilde çalışır                    |

#### Konteyner Orkestrasyon Araçları

- Google Kubernetes Engine (GKE)
- Microsoft Azure Kubernetes Service (AKS)
- Amazon ECS (Elastic Container Service)
- RedHat OpenShift

### 3.7 Sanallaştırma Yönetimi

- **VIM (Virtualization Infrastructure Management)**: merkezi yönetim modülü (denetleyici/controller).
- Sanallaştırılmış BT kaynaklarını toplu olarak yönetir.

### 3.8 Sanallaştırmanın Olumsuz Hususları

1. **Performans Yükü**: Yoğun iş yüklerinde sanallaştırma ideal olmayabilir.
2. **Özel Donanım Uyumluluğu**: Sürücü uyumsuzlukları olabilir; konteynerler bu sorundan etkilenmez.
3. **Taşınabilirlik**: OVF standardı bu boşluğu kapatmaya çalışır.

---

## 4. ÇOK KİRACILI TEKNOLOJİ (MULTITENANT TECHNOLOGY)

- **Çok kiracılı uygulama**: birden fazla kullanıcı (kiracı) **aynı uygulama mantığına eş zamanlı erişir**.
- Her kiracı, yazılımın **kendine özel bir örneğini** kullanıyormuş gibi hisseder.
- Kiracılar birbirlerinin **verilerine ve yapılandırmalarına erişemez**.

### Kiracıların Özelleştirebileceği Alanlar

1. **Kullanıcı Arayüzü** – Özel görünüm/tema
2. **İş Süreci** – Kurallar, mantık ve iş akışları
3. **Veri Modeli** – Şema genişletme, alan ekleme/çıkarma/yeniden adlandırma
4. **Erişim Denetimi** – Kullanıcı ve grup erişim haklarını bağımsız yönetme

### Çok Kiracılı Uygulamaların Ortak Özellikleri


| Özellik                      | Açıklama                                                    |
| ------------------------------- | --------------------------------------------------------------- |
| **Kullanım Yalıtımı**     | Bir kiracının davranışı diğerlerini etkilemez           |
| **Veri Güvenliği**          | Kiracılar birbirlerinin verilerine erişemez                 |
| **Kurtarma**                  | Yedekleme/geri yükleme her kiracı için ayrı yapılır     |
| **Uygulama Yükseltmeleri**   | Paylaşılan yazılım güncellemelerinden olumsuz etkilenmez |
| **Ölçeklenebilirlik**       | Kullanım ve kiracı artışına uyum sağlar                 |
| **Tarifeli Kullanım**        | Yalnızca tüketilen kaynaklar için ücretlendirilir         |
| **Veri Katmanı Yalıtımı** | Ayrı veritabanları, tablolar veya şemalar                  |

### Çok Kiracılık vs. Sanallaştırma


|                | Sanallaştırma                            | Çok Kiracılık                                  |
| ---------------- | -------------------------------------------- | --------------------------------------------------- |
| **Yapı**      | Fiziksel sunucu → birden çok sanal kopya | Tek uygulama → birden çok kullanıcıya sunulur |
| **İzolasyon** | Her VM'in kendi OS ve uygulamaları var    | Her kiracı özel kullanım hisseder              |

---

## 5. HİZMET TEKNOLOJİSİ VE HİZMET API'LERİ

### Web Tabanlı Servisler

- Standartlaştırılmış protokollere dayalı, **birlikte çalışabilir makineler arası** etkileşimi destekleyen **bağımsız mantık birimleri**.
- **API'leri kullanıma sunar**, kullanıcı arayüzleri yoktur.
- Tescilli olmayan teknolojilerle iletişim kurar.

### API (Application Programming Interface)

- Bir yazılımın başka bir yazılımla nasıl iletişim kurduğunu tanımlayan **arayüz**.
- Sistemin fonksiyon ve verilerine **dışarıdan erişim sağlar**.
- Genellikle **HTTP** protokolüyle çalışır (ayrıca WebSocket, SOAP, FTP kullanılabilir).

### REST Hizmetleri

- **REST** = Representational State Transfer
- World Wide Web özelliklerini taklit eden mimari.
- **6 REST Tasarım Kısıtlaması:**
  1. İstemci-Sunucu (Client-Server)
  2. Durumsuzluk (Stateless) — her istek bağımsız
  3. Önbellekleme (Cache)
  4. Arayüz/Standart Sözleşme (Uniform Interface)
  5. Katmanlı Sistem (Layered System)
  6. İsteğe Bağlı Kod (Code-On-Demand)

### Web Servisleri (SOAP Tabanlı)

- Gelişmiş ve web tabanlı servis mantığı için köklü ortam.
- **Temel teknolojiler:**
  - **WSDL** (Web Service Description Language) – API'yi tanımlar, işlemlerin giriş/çıkış mesajlarını belirtir.
  - **XML Schema** – veri yapılarını ve türleri tanımlar.
  - **SOAP** – istek/yanıt mesajları için ortak mesajlaşma formatı. Gövde (body) + Başlık (header) içerir.
  - **UDDI** – web servislerinin keşfi için dizin (katalog).

> **Kısaca:** XML Schema → veri tanımı | WSDL → servis tanımı | SOAP → iletim | UDDI → keşif

### Servis Temsilcileri / Ajanları (Service Agent)

- Mesajları çalışma zamanında kesen **olay odaklı programlar**.
- **Aktif (Active) Ajanlar:** Mesajı okur ve **içeriği değiştirir** (genellikle header'da).
- **Pasif (Passive) Ajanlar:** Mesajı değiştirmez; **izleme, loglama, raporlama** amaçlı kullanılır.

### Servis Ara Katmanı (Service Middleware)

İki yaygın ara katman platformu:

1. **ESB (Enterprise Service Bus):** Servis aracılığı, yönlendirme, mesaj kuyruğa alma.
2. **Orkestrasyon Platformu:** İş akışı mantığını barındıran ve yürüten ortam.

### Web Tabanlı RPC

- Bulut sağlayıcıları kaynaklara erişimi genellikle **RESTful servisler** aracılığıyla sunar.
- RPC çerçeveleri bazı performans sorunlarını aşabilir ancak **yalnızca TCP/IP'ye bağımlıdır** → web uygulamalarıyla uyumsuz.
- Modern protokoller (hem REST hem RPC avantajları):
  - **gRPC** – Google tarafından
  - **GraphQL** – Facebook tarafından
  - **Falcor** – Netflix tarafından

---

## 6. VAKA ANALİZİ — DTGOV Bulut Uyumlu Altyapısı

### Altyapı Bileşenleri


| Bileşen                              | Açıklama                                                                   |
| --------------------------------------- | ------------------------------------------------------------------------------ |
| **Tier-3 Tesis Altyapısı**          | Tüm merkezi alt sistemler için yedekli konfigürasyonlar                   |
| **Yedekli Bağlantılar**             | Elektrik ve su temini için yerel kapasite; arızada otomatik devreye girer  |
| **Ağlar Arası Bağlantı**          | Üç veri merkezi arasında ultra yüksek bant genişlikli özel hatlar      |
| **Yedekli İnternet Bağlantıları** | Birden fazla ISP bağlantısı + .GOV ekstraneti                             |
| **Standartlaştırılmış Donanım** | Sanallaştırma platformuyla soyutlanan yüksek kapasiteli standart donanım |

### Fiziksel Sunucu Altyapısı

- Sunucular → **sunucu raflarında** (server racks) organize.
- Her rafa **iki yedekli üst raf yönlendirici anahtarı** (Layer 3 router switch) bağlı.
- Router switch'ler → **küme yapılandırmalı LAN çekirdek anahtarlarına** bağlanır.
- Çekirdek anahtarlar → **yönlendiricilere** ve **güvenlik duvarlarına** bağlanır.

### Depolama Ağı (Storage Network)

- Sunucular ile depolama sistemlerini bağlayan **ayrı bir ağ**.
- **SAN (Storage Area Network)** anahtarları kullanılır; yedekli bağlantılarla donatılmıştır.

### Veri Merkezleri Arası Ağ

- **AS (Autonomous System)** olarak tasarlanmıştır.
- Veri merkezleri → **LAN'larla intra-AS yönlendirme** alanı oluşturur.
- Dış ISP'lere bağlantılar → **inter-AS yönlendirme teknolojisiyle** kontrol edilir.
- **Yük dengeleme (load balancing)** ve **hata toleransı (failover)** için esnek yapılandırma.

---

## HIZLI ÖZET / AKILDA KALAN TANIMLAR


| Terim                       | Tanım                                                                   |
| ----------------------------- | -------------------------------------------------------------------------- |
| **Sanallaştırma**         | Fiziksel donanımı yazılım tabanlı kopyalara çeviren işlem         |
| **Hipervizör**             | Sanal makineleri yöneten yazılım katmanı                             |
| **Type 1 (Bare-metal)**     | Doğrudan donanımda çalışır (ESXi, Hyper-V, KVM)                    |
| **Type 2 (Hosted)**         | Host OS üzerinde çalışır (VirtualBox, VMware Workstation)           |
| **Konteyner**               | Uygulama + bağımlılıkları birlikte paketleyen izole ortam           |
| **Docker**                  | 2013'te çıkan en popüler konteyner platformu                          |
| **Kubernetes**              | Docker konteynerlerini birden çok sunucuda yönetir                     |
| **Çok Kiracılık**        | Birden fazla kullanıcının aynı uygulamayı özel gibi kullanması    |
| **REST**                    | Durumsuz, HTTP tabanlı servis mimarisi (6 kısıt)                      |
| **SOAP**                    | XML tabanlı, WSDL + UDDI ile birlikte kullanılan web servis protokolü |
| **Gecikme (Latency)**       | Paketin bir düğümden diğerine gitme süresi                          |
| **Otonom Bilişim**         | Kendi kendine yapılandırma, optimizasyon, iyileştirme ve koruma       |
| **OVF**                     | Açık Sanallaştırma Formatı – sanal disk imaj standartlaştırması |
| **VIM**                     | Sanallaştırma Altyapı Yönetimi merkezi yönetim modülü             |
| **SAN**                     | Storage Area Network – depolama ağı                                   |
| **ESB**                     | Enterprise Service Bus – servis ara katman platformu                    |
| **gRPC / GraphQL / Falcor** | Modern web tabanlı RPC protokolleri                                     |
