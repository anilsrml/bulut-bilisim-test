# **BULUT DESTEKLEYİCİ** **TEKNOLOJİLER (2)**


#### **Bulut Destekleyici Teknolojiler**

**3. Modern Sanallaştırma**
**4. Çoklu Kiracılık Teknolojisi**
**5. Hizmet Teknolojisi ve Hizmet API’leri**
**6. Vaka Analizi Örneği**


## **3. MODERN SANALLAŞTIRMA**


##### **3.1. DONANIM BAĞIMSIZLIĞI**

❖ **Bir** **işletim** **sisteminin** **yapılandırmasının** **ve** **uygulama**
yazılımının **benzersiz** **bir** **BT** **donanım** **platformuna** yüklenmesi,
birçok yazılım donanım **bağımlılığına neden olur.**
❖ **Sanallaştırma**, **benzersiz** **BT** **donanımını** **öykünülmüş** ve
**standartlaştırılmış** yazılım tabanlı kopyalara çeviren bir
**dönüştürme işlemidir.**


##### **3.1. DONANIM BAĞIMSIZLIĞI**



❖ **Donanım** **bağımsızlığı** **sayesinde,** **sanal** **sunucular** **kolayca**

**başka** **bir** **sanallaştırma** ana bilgisayarına taşınabilir ve birden
çok donanım-yazılım **uyumsuzluğu** **sorunlarını** otomatik olarak
çözer.
❖ Sonuç olarak **,** **sanal** **BT** **kaynaklarını** **klonlamak** ve **manipüle**

**etmek**, **fiziksel donanımı kopyalamaktan** çok daha kolaydır.


##### **1.2. SUNUCU KONSİDALASYONU**

❖ **Sanallaştırma** yazılımı tarafından **sağlanan** **koordinasyon**

**işlevi**, birden **çok sanal sunucunun aynı sanallaştırma ana**
**bilgisayarında aynı anda oluşturulmasına olanak tanır.**
❖ **Sanallaştırma** **teknolojisi**, **farklı** **sanal** **sunucuların** **tek** **bir**

**fiziksel sunucuyu paylaşmasını sağlar.**
❖ **Bu işleme sunucu konsolidasyonu** **denir.**


##### **1.2. SUNUCU KONSİDALASYONU**

❖ **Genellikle**

  - **donanım kullanımını,**

  - **yük dengelemesini**

  - **mevcut BT kaynaklarının**
**optimizasyonunu artırmak** için kullanılır.


###### **1.3. KAYNAK ÇOĞALTMA (RESOURCE**


###### **REPLICATION)**

❖ **Sanal** **sunucular,** **sabit** **disk** **içeriğinin** **ikili** **dosya**

**kopyalarını** **içeren** **sanal** **disk** **görüntüleri** olarak
**oluşturulur.**
❖ Bu **sanal** **disk** görüntülerine **ana** **bilgisayarın**



**işletim** **sistemi** **tarafından** **erişilebilir**, yani
**kopyalama**, **taşıma** ve **yapıştırma** gibi basit dosya
işlemleri **sanal** **sunucuyu** **çoğaltmak**, **taşımak** ve
**yedeklemek** için kullanılabilir.


###### **1.4. İŞLETIM SİSTEMİ TABANLI SANALLAŞTIRMA**

❖ **Sanallaştırma** **yazılımının** ana
bilgisayar işletim sistemi olarak
adlandırılan **önceden** **var** **olan** **bir**
**işletim sistemine** yüklenmesidir.
❖ İşletim sistemi tabanlı sanallaştırmanın

**farklı** **mantıksal** **katmanları** ; bu
katmanda,

**-VM** **ilk** **önce** **tam** **ana** **işletim**
**sistemine kurulur**

**-** **Daha** **sonra** **sanal** **makineler**
**oluşturmak için kullanılır.**


###### **1.4. İŞLETIM SİSTEMİ TABANLI SANALLAŞTIRMA**

hipervizördür.


**paylaştıran bir yazılımdır.**

- **VirtualBox**, **VMware Workstation** gibi
yazılımların iç yapısında:

   - **Hipervizör (asıl işi yapan motor)**

   - **GUI (görsel arayüz)**

   - **VM ayar ekranları**

   - **Ağ/Disk/USB bağlama özellikleri**
bunların hepsi birlikte **“Virtual Machine**
**Management”** olarak sunmaktadır.


###### **1.4. İŞLETIM SİSTEMİ TABANLI SANALLAŞTIRMA**

**Örnek:** Aşağıdan yukarıya doğru bakarsak:
**1.Hardware** **(virtualization** **hos** t)
Fiziksel bilgisayarın kendisi (örneğin senin laptopun)
**2.Operating System (host OS)**
Bu bilgisayarda hali hazırda kurulu olan işletim sistemi
(örneğin Windows 10)
**3. Virtual Machine Management**
**VirtualBox**, **VMware** **Workstation** gibi sanallaştırma
yazılımı (yani hypervisor burada bir uygulama gibi
çalışıyor)
**4. VM (guest OS + uygulama yazılımı)**
Her biri ayrı ayrı işletim sistemi gibi çalışan sanal
makineler (örneğin içinde Ubuntu, Debian, Fedora vs.
kurulu)


###### **1.4. İŞLETIM SISTEMI TABANLI SANALLAŞTIRMA**

❖ Ana bilgisayar işletim sistemi, **kendi içinde eksiksiz**

**bir işletim sistemi olduğundan**, yönetim araçları olarak
kullanılabilen **birçok işletim sistemi tabanlı hizmet**,
**fiziksel** ana bilgisayarı yönetmek için kullanılabilir.
**Bu tür hizmetlere örnek olarak şunlar verilebilir:**
**1.** **Yedekleme ve Kurtarma**
**2.** **Dizin Servislerine Entegrasyon**
**3.** **Güvenlik Yönetimi**


**1.4. İŞLETIM SISTEMI TABANLI SANALLAŞTIRMA**


4. **Ana bilgisayar işletim sistemi CPU**, **bellek** ve **diğer**
**donanım BT kaynaklarını** tüketir.
5. **Konuk işletim sistemlerinden gelen donanımla** ilgili


**1.5. DONANIM TABANLI SANALLAŞTIRMA**

❖ Sanallaştırma yazılımının **doğrudan**

**fiziksel ana bilgisayar donanımına**
**yüklenmesini** temsil eder.
❖ **Başka bir ana işletim sistemine** ihtiyaç

duymayan, donanım tabanlı
sanallaştırmanın **farklı** **mantıksal**
**katmanlarıdır.**
❖ **Sanallaştırma yazılımı,** genellikle bu tür

işlemler için bir hipervizör olarak
**adlandırılır.**


- **Bir hipervizör,** ihmal edilebilir miktarda depolama alanı
gerektiren basit bir kullanıcı arayüzüne sahiptir.

- Bir **sanallaştırma yönetimi katmanı oluşturmak** için
**donanım yönetimi işlevlerini** **işleyen** ince bir **yazılım**
**katmanı olarak bulunur.**

- **Örnek**


**Type 1 Hypervisor (Bare-metal)**



❖ Doğrudan donanımın üzerine kurulur.
❖ Hiçbir ana işletim sistemi (Windows,



Linux vs.) yoktur.
❖ Sadece sanal makineleri çalıştırmak



için vardır.
**Örnekler** :

- VMware ESXi

- Microsoft Hyper-V (Sunucu sürümü)

- Xen

- KVM


aygıt sürücüleri ve destek yazılımıyla doğrudan **iletişim kuracak**
**şekilde tasarlanmıştır.**

- **Sanallaştırma katmanı,** doğrudan ana bilgisayar donanımıyla
**iletişim kurmak üzere tasarlanmıştır** ; bu, ilişkili tüm aygıt
sürücülerinin ve destek yazılımlarının **hipervizörle uyumlu olması**
gerektiği anlamına gelir.


###### **1.6. KONTEYNERLER VE UYGULAMA TABANLI** **SANALLAŞTIRMA**



❖ **Uygulama sanallaştırma**, işletim sistemine bağımlı olmadan



**uygulama oluşturma** ve **kullanma yöntemidir** .
❖ **Konteynerler**, **uygulama sanallaştırma yaklaşımına** uygun



olarak çalışır.
❖ **Her biri bağımsız** ve **kendi içinde çalışan uygulama** ya da



**hizmetleri barındırır.**
❖ **Bu yapı sayesinde** **yazılımlar**, **farklı sistemlerde sorunsuz**



**şekilde çalışabilir.**
❖ **Konteynerler** ; **taşınabilir**, **uyumlu** ve kolay yönetilebilir bir



**dağıtım ortamı sunar.**
❖ Bu sayede **hem geliştirme** hem de **dağıtım süreçleri** daha



**esnek ve verimli hale gelir.**


❖ Bir konteynerde **çalışan sanallaştırılmış bir uygulama**, altta

**yatan donanım veya işletim sistemi mimarilerinden**
**bağımsız** olarak, **ilgili konteynerleştirme motorunun** _kurulu_
olduğu **her yere dağıtılabilir.**


**KONTEYNERLER TEKNOLOJİSİ** **DONANIM TABANLI SANALLAŞTIRMA**


❖ **Docker, konteyner teknolojisinin temel aracıdır.** **2013 yılında Docker, Inc.**

tarafından **piyasaya sürülmüştür** ve bu tarihten itibaren **yazılım geliştirme**
**ve dağıtım süreçlerinde devrim yaratmıştır.**
❖ **Uygulama** **ve** **onun** **bağımlılıklarını** **kapsayıcılar** içinde **paketleyerek**
**taşınabilirlik sağlar** . Bu, **her ortamda aynı şekilde çalışmasını garantiler.**


❖ Docker konteynerlerini birden fazla sunucuda yönetmek için

alternatif birçok seçenek vardır.

- Google Kubernetes Engine (GKE)

- Microsoft Azure Kubernetes Service (AKS)

- Amazon ECS (Elastic Container Service)

- RedHat OpenShift

- …


##### ÖRNEK

Bir e-ticaret uygulaması geliştiriyorsanız, aşağıdaki bağımlılıklar ve

ortam ihtiyaçları olabilir:

- **Programlama dili** : Python, Node.js, Ruby, vb.

- **Veritabanı** : PostgreSQL, MySQL, MongoDB, vb.

- **Önbellekleme sistemi** : Redis veya Memcached.

- **Diğer kütüphaneler** : Uygulama için gerekli olan yazılım
kütüphaneleri, örneğin Flask, Express, Django, vb.


##### ÖRNEK (DEVAM)

Normalde, bir uygulama farklı **sunucularda çalıştırılacaksa**, her sunucuda
yukarıdaki bağımlılıkların **teker teker yüklenmesi ve doğru versiyonların**
kurulması gerekir.
Bu da aşağıdaki sorunlara yol açar:

- **Bağımlılık uyumsuzlukları** :
Farklı ortamlar (geliştirme, test, prodüksiyon) arasında **versiyon farkları**
olabilir.
Örneğin, bir sunucuda kullanılan **Python 3.7** ve diğerinde **Python 3.8** olması
**uygulamanın tutarsız çalışmasına neden olabilir.**

- **Kurulum ve yapılandırma hataları** :
**Sunucularda gerekli yazılımlar ve bağımlılıklar hatalı yüklenebilir**, bu da
**uygulamanın çalışmamasına veya hatalı çalışmasına** neden olabilir.


##### ÖRNEK (DEVAM)

Konteyner teknolojisi, bu sorunları çözmek için **çalışma ortamını ve**

**bağımlılıkları tek bir paket içinde** toplar. Bu **paket**, **"kapsayıcı"**
**(container)** olarak adlandırılır.
Bir konteyner şu unsurları içerir:

- **Uygulama kodu** (Python veya Node.js kodu),

- **Gerekli bağımlılıklar** (kütüphaneler, yazılımlar, araçlar),

- **Konfigürasyon dosyaları** ve **ortam değişkenleri** .

- Konteyneri oluşturduğunuzda, **bütün bu bileşenler** kapsayıcı içinde
bir araya gelir ve **taşınabilir hale gelir** .

- Yani, konteyneri bir sunucudan diğerine taşıyabilirsiniz ve her
ortamda **aynı şekilde çalışır** .


###### **Konteynerin Avantajları**

**1.Taşınabilirlik** :

**Docker konteynerleri**, bir sunucudan diğerine kolayca
taşınabilir.
**Bu, uygulamanın ve bağımlılıklarının aynı şekilde**
**çalışmasını sağlar**, çünkü tüm bağımlılıklar konteyner
içinde barındırılmaktadır.
**Örnek:** **E-ticaret** **uygulamanızı** **geliştirdiğiniz**
**bilgisayarınızda** **çalışan** **bir** **konteyneri**, test
sunucusuna veya prodüksiyon ortamına taşıdığınızda
**aynı şekilde çalışır.**
Çünkü **tüm bağımlılıklar konteynerde yer alır**, bu
**yüzden sistemdeki diğer yazılım versiyonları** bu
durumu etkilemez.


**2. Hızlı Dağıtım** :

Konteynerler, **çok hızlı bir şekilde başlatılabilir** ve
çalıştırılabilir.
Çünkü konteyner, **işletim sistemi sanallaştırmasından**
**farklı olarak** yalnızca **uygulama ve bağımlılıkları**
**çalıştırır,** bu da daha hızlı başlatılmasına olanak tanır.
**Örnek:**
E-ticaret uygulamanızın **yeni bir sürümünü test**
**ortamında** **hızlıca çalıştırmak için** **sadece yeni bir**
**konteyneri başlatmak yeterlidir.**


**3. İzolasyon** :
**Konteynerler,** **uygulamanın bağımlılıkları ve ortamı** ile
**diğer uygulamalardan tamamen izole** edilmesini sağlar.
Bu, bir konteynerin diğerini **etkilemeden** çalışmasını
garanti eder.
**Örnek** :
E-ticaret uygulamanızın **test ortamı** ve **prodüksiyon**
**ortamı** **farklı konteynerlerde çalışır** .
Bu da, **test** **sunucusunda** yapılan değişikliklerin
**prodüksiyon ortamına** zarar vermemesini sağlar.


**4. Mikro Servisler ve Ölçeklenebilirlik**
Mikro servisler, **büyük uygulamaların** küçük, bağımsız bileşenlere
ayrılmasını sağlar.
Docker, her mikro servisi **bağımsız bir konteynerde çalıştırmaya** olanak
tanır.
Docker ile, her bir konteyner bağımsız bir **bileşen** olarak çalışabilir ve
sadece gerektiğinde **yükseltilebilir veya ölçeklendirilebilir** . Bu sayede
daha esnek ve **ölçeklenebilir** uygulamalar geliştirilir.
**Örnek:**

- Bir e-ticaret uygulaması, **ödemeler**, **siparişler**, **ürün listeleri** gibi her
fonksiyonu **farklı konteynerlerde** çalıştırarak, her bir fonksiyonun
**bağımsız bir şekilde ölçeklenmesini sağlar** .

- Eğer ödeme sistemi yüksek trafik alıyorsa, sadece **o konteyner sayısını**
**arttırabilirsiniz ya da daha güçlü bir sunucuya konteynerı taşımak**
**gerekir.**


**5. Bulut ve Dağıtık Ortamlar için Uygunluk:**
Docker konteynerlerinin taşınabilirliği sayesinde, uygulamanız
herhangi bir bulut ortamında (AWS, Google Cloud, Azure) aynı
şekilde çalışabilir.

**Örnek:**
**Bir** **SaaS** **(Software** **as** **a** **Service)** **platformu**, **Docker**
**konteynerlerini** **kullanarak**, AWS veya Google Cloud'da
uygulamanın her bileşenini bağımsız bir şekilde çalıştırabilir ve yük
arttıkça **sadece ihtiyacı olan konteynerleri ölçeklendirebilir.**


###### **1.7. Sanallaştırma Yönetimi**

❖ Modern sanallaştırma yazılımı, **yönetim** **görevlerini**
**otomatikleştirebilen** ve **sanallaştırılmış BT kaynakları**


kaynaklarını toplu olarak yöneten ve **özel bir bilgisayarda**
**çalışan**, **denetleyici** olarak da bilinen merkezi bir **yönetim**
**modülüne dayanan sanallaştırma altyapı yönetimi (VIM)**
araçları tarafından desteklenir.


###### **1.8. DİĞER HUSUSLAR**

**1.** **Performans Yükü:** **Sanallaştırma**, **kaynak paylaşımı** ve

**çoğaltma** için çok az **kullanılan yüksek iş yüklerine** sahip
**karmaşık sistemler** için **ideal olmayabilir** .
Kötü formüle edilmiş bir sanallaştırma planı, aşırı performans
yüküne neden olabilir.
**2. Özel Donanım Uyumluluğu:** Özel donanım dağıtan birçok
donanım satıcısı, **sanallaştırma yazılımıyla uyumlu** **aygıt**
**sürücüsü sürümlerine sahip olmayabilir.**
Tersine, yazılımın kendisi yakın zamanda piyasaya sürülen
donanım sürümleriyle uyumsuz olabilir.
**Konteyner motorları bu düşünceden etkilenmezler.**


###### **1.8. DİĞER HUSUSLAR**

**3. Taşınabilirlilik:**
Bir sanallaştırma programının çeşitli sanallaştırma
çözümleriyle çalışması için yönetim ortamları oluşturan
programatik ve yönetim arayüzleri, uyumsuzluklar nedeniyle
**taşınabilirlik boşluklarına neden olabilir.**
**Sanal disk görüntü formatlarının standardizasyonu için** Açık
Sanallaştırma Formatı (OVF) **gibi girişimler** **bu endişeyi**
**hafifletmeye adanmıştır.**


### **4. ÇOK KİRACILI TEKNOLOJİ** **(MULTITENANT** **TECHNOLOGY)**


❖ **Çok kiracılı uygulama tasarımı**, birden çok kullanıcının

(kiracı) **aynı uygulama mantığına** **aynı anda erişmesini**
**sağlamak** için oluşturulmuştur.
❖ **Her kiracının**, **aynı uygulamayı kullanan diğer kiracılardan**

**habersiz kalırken**, yazılımının özel bir örneği olarak
**kullandığı**, **yönettiği** ve **özelleştirdiği** uygulamanın kendi
**görünümü** vardır.
❖ **Çok** **kiracılı** **uygulamalar,** **kiracıların** **kendilerine** **ait**
**olmayan** **verilere** ve **yapılandırma** **bilgilerine**
**erişememesini sağlar.**


❖ **Kiracılar**, uygulamanın aşağıdakiler gibi **özelliklerini tek**

**tek** özelleştirebilir:
**1.** **Kullanıcı Arayüzü** - Kiracılar, uygulama arayüzleri için
özel bir "görünüm " tanımlayabilir.
**2.** **İş Süreci** - Kiracılar, uygulamada uygulanan iş
süreçlerinin kurallarını, mantığını ve iş akışlarını
özelleştirebilir.
**3.** **Veri Modeli** - Kiracılar, uygulamanın veri şemasını,
uygulama veri yapılarındaki alanları dahil etmek, dışlamak
veya yeniden adlandırmak için genişletebilir.
**4.** **Erişim Denetimi** - Kiracılar, _kullanıcılar ve gruplar için_
**erişim** haklarını bağımsız olarak denetleyebilir.


❖ Çok kiracılı uygulama mimarisi genellikle **tek kiracılı**

**uygulamalardan önemli ölçüde daha karmaşıktır.**
❖ Çok kiracılı uygulamaların, **tek kiracı operasyonel**

**ortamlarını ayıran güvenlik düzeylerini korurken**,
**birden çok kullanıcı** (portallar, veri şemaları, ara
yazılımlar ve veri tabanları dahil) **tarafından çeşitli**
**yapıtların paylaşımını desteklemesi gerekir.**


##### **Çok Kiracılı Uygulamaların Ortak Özellikleri**

**Kullanım Yalıtımı** - Bir kiracının kullanım davranışı, diğer
kiracıların uygulama kullanılabilirliğini ve performansını
etkilemez.
**Veri Güvenliği** - Kiracılar, diğer kiracılara ait verilere
erişemez.
**Kurtarma –** _Yedekleme_ ve _geri yükleme_ yordamları her
kiracının verileri için ayrı ayrı yürütülür.
**Uygulama Yükseltmeleri** - Kiracılar, paylaşılan yazılım
yapıtlarının zaman uyumlu yükseltmesinden olumsuz
etkilenmez.


##### **Çok Kiracılı Uygulamaların Ortak Özellikleri**

**Ölçeklenebilirlik** - Uygulama, mevcut kiracılar tarafından
kullanımdaki artışlara ve/veya kiracı sayısındaki artışlara
uyum sağlayacak şekilde ölçeklendirilebilir.
**Tarifeli Kullanım** - Kiracılar yalnızca gerçekten tüketilen
uygulama işleme ve özellikler için ücretlendirilir.
**Veri Katmanı Yalıtımı** - Kiracılar, **diğer kiracılardan**
**yalıtılmış** **tek tek veritabanlarına**, tablolara ve/veya
şemalara **sahip olabilir.**


❖ **Aynı anda birden fazla**

**bulut hizmeti tüketicisine**
**hizmet veren çok kiracılı**
**bir uygulama.**


##### **ÇOK KİRALILIK VS. SANALLAŞTIRMA**

**1.** **Sanallaştırma ile:**
**Sunucu ortamının birden fazla sanal kopyası**, **tek bir fiziksel**
**sunucu tarafından barındırılabilir.**
**Her kopya farklı kullanıcılara sağlanabilir, bağımsız olarak**
**yapılandırılabilir** ve **kendi işletim sistemlerini ve uygulamalarını**
**içerebilir.**
**2.** **Çok kiracılı:**
Bir uygulamayı **barındıran fiziksel veya sanal bir sunucu**, **birden**
**çok farklı kullanıcı** tarafından kullanıma izin verecek şekilde
tasarlanmıştır. **Her kullanıcı, uygulamanın özel kullanımına**
**sahipmiş gibi hisseder.**


## **5. HİZMET TEKNOLOJİSİ VE** **HİZMET API'LERİ**


❖ **Hizmet teknolojisi alanı**, "hizmet olarak" bulut dağıtım

modellerinin temelini oluşturan **bulut bilişimin temel taşı**
**niteliğindedir.**
❖ **WEB TABANLI SERVİSLER**
Standartlaştırılmış protokollerin kullanımına bağlı olan **web tabanlı**
**hizmetler**, bir ağ üzerinden birlikte çalışabilir makineler arası
etkileşimi destekleyen **bağımsız mantık birimleridir.**
Bu hizmetler genellikle endüstri standartlarına ve sözleşmelerine
**uygun** **olarak** **tescilli** **olmayan** **teknolojiler** **aracılığıyla** **iletişim**
kurmak üzere tasarlanmıştır.
**Tek** **işlevleri** **bilgisayarlar** arasında **veri** **işlemek** **olduğundan**, bu
hizmetler **API'leri kullanıma sunar** ve **kullanıcı arayüzlerine sahip**
**değildir.**


**API (Application Programming Interface)**
❖ **API**, bir **yazılım uygulamasının** veya **servisinin** başka bir yazılım

uygulamasıyla nasıl iletişim kurduğunu tanımlayan bir **arayüzdür** .
❖ **API** 'ler, bir sistemin **fonksiyonlarına** ve **verilerine** dışarıdan

**erişim sağlamak** için kullanılan bir **protokol** veya **aracıdır** .
❖ **API** 'ler, farklı yazılımlar arasında **bilgi paylaşımı ve etkileşimi**

sağlar.
❖ **API** 'ler, belirli bir sistemin **fonksiyonlarını** dışarıya **sunmak** için

kullanılır.
❖ Örneğin, **bir** **hava** **durumu** **verisi** **sağlayan** uygulama,
kullanıcıların **hava durumu verisine** erişebilmesi için bir **API**
sunar.

- **API** 'ler, genellikle **HTTP** protokolü ile çalışır, ancak diğer
protokoller de kullanılabilir (örneğin **WebSocket**, **SOAP**, **FTP** ).


##### **REST HİZMETLERİ**


- **REST (Representational State Transfer)**, **web servislerinin**
tasarımı için yaygın olarak kullanılan bir mimaridir.

- REST hizmetleri, **World Wide Web'in** özelliklerini taklit etmek için
hizmet mimarisini şekillendiren bir **dizi kısıtlamaya** göre
**tasarlanmıştır.**

- **B** u da temel web teknolojilerinin **kullanımına dayanan** **hizmet**
**uygulamalarıyla sonuçlanır.**


##### **REST HİZMETLERİ**

❖ **REST tasarım kısıtlaması şunlardır:**

**1.** **İstemci-Sunucu (Client-Server)**
**2.** **Durumsuzluk** **(Stateless:** **her** **istek** **bağımsız**
**şekilde işlenir)**
**3.** **Önbellekleme (Cache)**
**4.** **Arayüz/Standart** **Sözleşme** **(Interface/Uniform**
**Contract)**
**5.** **Katmanlı Sistem (Layered System)**
**6.** **İsteğe Bağlı Kod (Code-On-Demand)**


##### **WEB SERVİSLERİ**

Web Servisleri Genellikle "SOAP tabanlı" ifadesiyle anılan web
servisleri, **gelişmiş ve web tabanlı servis mantığı** için **yaygın**
**olarak kullanılan köklü bir ortamı temsil eder.**
**XML ile birlikte,** web servislerinin **temel teknolojileri** aşağıdaki
endüstri standartlarıyla belirlenir:
❑ **Web** **Servis** **Açıklama** **Dili** (WSDL Web Service Description

Language)
Bu işaretleme dili, **bir web servisinin uygulama programlama**
**arayüzünü** (API) **tanımlayan** bir **WSDL tanımı oluşturmak** için
kullanılır.
Bu tanım, **servisin bireysel işlemlerini** (fonksiyonlarını) ve her
**işlemin giriş ve çıkış mesajlarını** kapsar.


##### **WEB SERVİSLERİ**

Web servisleri tarafından **değiş tokuş edilen mesajlar** **XML**
**formatında ifade edilmelidir.**
XML şemaları, **web servisleri tarafından değiş tokuş edilen** XML
tabanlı **giriş ve çıkış** mesajlarının **veri yapısını tanımlamak** için
oluşturulur.
**XML şemaları,** doğrudan **WSDL tanımlarına bağlanabilir** veya bu
**tanımların içine gömülebilir.**


Web servisleri tarafından değiş tokuş edilen istek ve yanıt
mesajları için **ortak bir mesajlaşma formatı tanımlar.**
SOAP mesajları **gövde (body)** ve **başlık (header)** bölümlerinden



oluşur:

- **Gövde:** Ana mesaj içeriğini barındırır.

- **Başlık:** Çalışma zamanında işlenebilecek **meta verileri** içerir.



Bu standart, **hizmet kayıtlarını düzenler** ve WSDL tanımlarının **, keşif**
**amacıyla** bir **hizmet kataloğunun parçası** olarak **yayınlanmasına**
**olanak tanır.**


                          - **XML** **Schema,** **veri**
**yapılarının** **ve** **türlerinin**
**tanımlandığı yerdir.**

                          - **WSDL,** **web** **servislerinin**
**işlevselliklerini tanımlar** **ve**
**keşfedilmesini sağlar.**

                          - **SOAP, veri iletimini sağlayan**

**protokoldür** **ve** **WSDL**
**üzerinden yönlendirilir.**

                          - **UDDI,** **web** **servislerinin**
**keşfi** **için** **kullanılır.** **Bu,**
**sistemlerin birbirine nasıl**
**bağlanacağını gösteren bir**
**dizindir.**


**Birinci nesil web servis teknolojilerinin** birbirleriyle nasıl ilişkilendiğine dair genel bir bakış.


##### ÖRNEK

**Cevap** : Bu tür bir veri paylaşımı için en uygun yöntem **web servisi**

kullanmaktır. Çünkü **web servisleri**, farklı sistemlerin birbiriyle veri
alışverişi yapabilmesini sağlayan standart yöntemler sunar. Bir kişinin
öğrenci olup olmadığına dair veri **XML formatında** paylaşılabilir.

- **API**, genellikle **bir sistemin işlevlerini dış dünyaya sunmak** için
kullanılır ve daha geniş bir iletişim protokolü yelpazesi sunar.

- Ancak **web servisleri**, özellikle **SOAP veya REST** gibi protokollerle
**yapılandırılmış veri paylaşımı** için daha yaygın bir tercihtir.


##### ÖRNEK

**Cevap: API (Uygulama Programlama Arayüzü) sunmak**, bu
durumda **en uygun çözüm olacaktır** .
Çünkü API, dışarıdan gelen **sorgulamalara hızlı bir şekilde yanıt**
**verir** ve kaynak kodunuzu paylaşmadan, sadece işlevi dışarıya
sunmanıza olanak tanır.
**Web servisleri genellikle daha ağır ve yapılandırılmış veri**
**paylaşımı gerektirir**, bu da **esneklik ve hız açısından daha az**
**verimli olabilir.**


##### **Servis Temsilcileri/Ajanları (Servis Agent)**

- Servis Temsilcileri (Servis Agent), **genellikle** **yazılım**
**mimarilerinde** ve özellikle dağıtık sistemlerde önemli bir rol
oynayan aracılardır.

- Genellikle **, servislerin yönetimi** ve **izlenmesi** gibi işlemleri
yapmak için kullanılırlar.

- **Servis ajanları,** sunucular ve istemciler arasında **aracılık yapan**
**bileşenlerdir.**

- **Web servisleri** bağlamında servis ajanları görev yapmaktadır.


##### **Servis Temsilcileri/Ajanları (Servis Agent)**

- **Servis/Hizmet aracıları**, **iletileri çalışma zamanında kesmek**
için tasarlanmış **olay odaklı programlardır.**

- **Her ikisi de bulut ortamlarında** yaygın olan **aktif ve pasif hizmet**
aracıları vardır.

- **Etkin hizmet aracıları**, bir iletinin içeriğini yakaladıktan ve
okuduktan sonra bir eylem gerçekleştirir.

- **Aktif hizmet aracıları**, genellikle ileti içeriğinde (en yaygın olarak
ileti üstbilgisi verileri ve daha az sıklıkla gövde içeriği) veya ileti
yolunun kendisinde değişiklik yapılmasını gerektirir.


##### **Servis Temsilcileri/Ajanları (Servis Agent)**


- **Pasif hizmet temsilcileri** ise **mesaj içeriklerini değiştirmez** .
Bunun yerine, mesajı okurlar ve daha sonra genellikle izleme,
günlüğe kaydetme veya raporlama amacıyla içeriğinin belirli
**bölümlerini yakalayabilirler.**


##### **Servis Ara Katmanı (Service Middleware)**


- Bu platformlar, başta **entegrasyonu** **kolaylaştırmak** **için**
**kullanılırken**, zamanla karmaşık servis bileşimlerini
destekleyebilen **gelişmiş servis ara katmanı platformlarına**
**dönüşmüştür.**

- Servis bilişimi açısından en yaygın iki ara katman platformu
şunlardır:
**1.** **Kurumsal Servis Veri Yolu (ESB - Enterprise Service Bus):**
Servis aracılığı (brokerage), yönlendirme (routing) ve mesaj kuyruğa
alma (message queuing) gibi bir dizi ara işlem özelliğini kapsar.
**2. Orkestrasyon Platformu:** Servislerin çalışma zamanındaki
bileşimini yönlendiren **iş akışı mantığını** (workflow logic) barındıran
ve yürüten ortamdır.


##### **Web Tabanlı RPC (Web-Based RPC)**


- Bulut sağlayıcıları, sundukları **kaynaklara erişimi genellikle**
**RESTful servisler aracılığıyla sağlar.**

- **RESTful servisler** ile **hizmet tüketicileri arasındaki etkileşim**, ağ

**Call)** çerçeveleri, RESTful mimarilerde **karşılaşılan** **bazı**
**performans zorluklarını aşabilir.**

- Ancak, bu çerçeveler yalnızca **TCP/IP üzerinden iletişime**
bağımlıdır, bu **da web tabanlı uygulama gereksinimleriyle**
**uyumsuz** bir **kısıtlama oluşturur.**


##### **Web Tabanlı RPC (Web-Based RPC)**


- Hem **RESTful** mimarilerin hem de geleneksel **RPC** çözümlerinin
sınırlamalarını gidermek amacıyla, **RPC'nin** **performans**
avantajlarını sunarken **web tabanlı iletişimi destekleyen** çağdaş
protokoller geliştirilmiştir.

- **Bunlar şunlardır:**

- gRPC (Google tarafından geliştirilmiştir)

- GraphQL (Facebook tarafından geliştirilmiştir)

- Falcor (Netflix tarafından geliştirilmiştir)
**Bu protokollerin her biri**, **mevcut protokollerde yaşanan**
**kısıtlamaları aşma ihtiyacına yanıt olarak geliştirilmiştir.**


## **6. VAKA ANALİZİ ÖRNEĞİ**


##### **DTGOV'un Bulut Uyumlu Altyapısı**

**DTGOV**, her veri merkezinde **bulut** **uyumlu** **altyapılar**
**oluşturmuştur.**
Bu altyapılar aşağıdaki bileşenlerden oluşmaktadır:
❖ **Tier-3 tesis altyapısı:**
Veri merkezi tesis katmanındaki **tüm merkezi alt sistemler** için
**yedekli konfigürasyonlar** sağlar.
❖ **Yedekli bağlantılar:**
_Elektrik üretimi_ ve _su temini_ için yerel kapasiteye sahip hizmet
sağlayıcılarla **bağlantılar kurulmuştur** . Genel bir arıza durumunda
bu sistemler otomatik olarak devreye girer.
❖ **Ağlar arası bağlantı (internetwork):**
**Üç veri merkezi** arasında ultra yüksek bant genişliğine sahip
bağlantıyı sağlayan özel hatlardan oluşur.


##### **DTGOV'un Bulut Uyumlu Altyapısı**

❖ **Yedekli internet bağlantıları:**
Her veri merkezinde **birden fazla internet servis sağlayıcısına**
(ISP) bağlı yedekli internet bağlantıları ve .GOV ekstraneti bulunur.
Bu ekstranet, DTGOV'u ana **devlet müşterileriyle bağlar.**
❖ **Standartlaştırılmış yüksek kapasiteli donanım:**
**Bulut uyumlu sanallaştırma platformu** tarafından **soyutlanan**,
**daha yüksek bütünleşik kapasiteye** sahip **standart donanımlar**
**kullanılır.**


**Fiziksel Sunucu Alt Yapısı**

- **Fiziksel sunucular**, **sunucu raflarında**
**(server racks)** organize edilmiştir.

- Her sunucu rafında, **her** **fiziksel**
**sunucuya bağlı** **iki yedekli üst raf**
**yönlendirici anahtarı** **(Layer 3 router**
**switch)** bulunmaktadır.

- **Bu yönlendirici anahtarlar**, **küme**
**(cluster) olarak yapılandırılmış LAN**
**çekirdek** **anahtarlarına** **(core-**
**switches)** bağlanır.

- **Çekirdek** **anahtarlar,** **ağlar** **arası**
**bağlantı sağlayan yönlendiricilere** ve
**ağ erişim kontrol yetenekleri sunan**
**güvenlik** **duvarlarına** **(firewalls)**
bağlanarak güvenli ve ölçeklenebilir bir
ağ altyapısı oluşturur.


❖ **Depolama Ağı (Storage Network)**
**Depolama sistemleri** ile sunucuları
bağlayan ayrı bir ağ kurulmuştur.
**Bu ağ, kümeleme** (clustered) **özellikli**
**depolama alan ağı** (SAN - Storage Area
Network) **anahtarları** **ve** **çeşitli**
**cihazlara** **yönelik** benzer **yedekli**
**bağlantılar ile donatılmıştır.**


❖ **Veri Merkezleri Arası Ağ Yapısı**

- DTGOV'un ağlar arası bağlantı yapısı
(internetwork), internette bağımsız
bir sistem (AS - Autonomous System)
olacak şekilde tasarlanmıştır.

- **Bu yapı,** veri merkezlerini **LAN'larla**
**birbirine** **bağlayan** bağlantıların,
**intra-AS yönlendirme alanını** (intraAS routing domain) oluşturmasını
sağlar.

- **Harici** **internet** **servis**
**sağlayıcılarına** (ISP) **yapılan**
**bağlantılar**, **inter-AS yönlendirme**
**teknolojisi** ile kontrol edilir.

- Bu teknoloji, **internet** **trafiğini**
**şekillendirerek** **yük** **dengeleme**
(load balancing) ve **hata toleransı**
(failover) için **esnek**
**konfigürasyonlar** yapılmasına
olanak tanır.


##### **KAYNAKLAR**


 - Thomas Erl, Eric Monroy - Cloud Computing_ Concepts,
Technology, Security, and Architecture (The Pearson Digital
Enterprise Series from Thomas Erl)-Pearson (2023)


