## **Konu Başlıkları**

**1. Konteynerleştirmenin Kökeni ve Etkileri**
**2. Temel Sanallaştırma ve Konteynerleştirme**
**3. Konteynerleri Anlamak**
4. Konteyner İmajlarını Anlamak
5. Çoklu Konteyner Türleri
6. Örnek Vaka İncelemesi


## **Kökeni ve Etkileri**


- Konteyner kavramı, **1970’lerden** **bu** **yana** **varlığını**
sürdürmektedir.

- Bu kavram, ilk olarak **Unix** **sistemlerinde** **uygulama**
**kodlarını** **daha** **iyi** **şekilde** **birbirinden** **ayırmak**
amacıyla kullanılan **bir yetenek olarak ortaya çıkmıştır.**

- Erken dönem konteynerler, **hizmetlerin** ve
**uygulamaların** **birbirine** **müdahale** **etmeden**
çalışabildiği **izole bir ortam sunuyordu.**

- Bu da uygulamaların, **hizmetlerin** ve **diğer** **işlemlerin**
test edilmesi için bir tür **sandbox** ortamı sağlıyordu.

**Sandbox**, **genellikle test edilmemiş veya**

**güvenilmeyen program ya da kod çalıştırmak** için
oluşturulmuş **güvenlik mekanizmasıdır.**


- **Konteynerler,** yıllar sonra **birçok Linux dağıtımının yeni dağıtım** ve
**yönetim** **araçları** **yayınlamasıyla** birlikte _**yaygın**_ _**şekilde**_
_**kullanılmaya başlandı.**_

- Linux sistemlerinde çalışan **konteynerler**, aynı **Linux ana makinesi**
**üzerinde** **birden** **fazla** **izole** **edilmiş** **Linux** **ortamının** **çalışmasını**
sağlayan bir **işletim** **sistemi** **düzeyinde** **sanallaştırma** **tekniğine**
**dönüştü.**

- **Ancak**, **konteynerlerin** Linux platformlarında çalışması kullanım
alanlarını genişletse de; **birleşik** **yönetim**, **gerçek** **taşınabilirlik**,
**uyumluluk** ve **ölçeklendirme** kontrolü gibi önemli sorunlar hâlâ
çözülmeyi bekliyordu.


#### • Apache Mesos, Google Borg ve Facebook Tupperware, konteynerlerin Linux sistemler üzerindeki kullanımında önemli bir ilerlemeyi temsil etmiştir. • Bu sistemlerin her biri, farklı seviyelerde konteyner düzenleme (orchestration) ve küme yönetimi (cluster management) yetenekleri sunarak konteyner tabanlı **altyapıların verimli bir şekilde yönetilmesini** mümkün kılmıştır.


#### • Docker konteynerlerinin tanıtılmasının ardından, konteynerleştirme (containerization) kavramı bilgi teknolojileri dünyasında ana akım haline gelmeye **başlamıştır.** • Docker’ın yükselişi, Marathon, Kubernetes ve Docker Swarm gibi gelişmiş konteynerleştirme platformlarının **doğmasına zemin hazırlamıştır.**


## **Konteynerleştirme ve Bulut Bilişim**

##### • Bulut bilişim, sanallaştırma teknolojisinin **yaygınlaşmasına öncülük etmiştir.** • Bulut teknolojisindeki daha sonraki gelişmeler ise **günümüzdeki modern konteynerleştirme** teknolojisinin hayata geçirilmesini sağlamıştır. • Artık konteynerleştirme, bulut bilişim altyapısının temel bir parçası haline gelmiştir.


## **Konteynerleştirme ve Bulut Bilişim**

##### Konteynerleştirme ile sağlanan sadeleştirilmiş ve esnek dağıtım mimarisi; **-maliyetleri azaltma (Cost Reduction)** -iş çevikliğini artırma (Business Agility) gibi, bulut bilişimin temel iş hedeflerini doğrudan **destekleyebilir.**


## **Temel Sanallaştırma ve Konteynerleştirme**

**Konteyner** **teknolojisini** **anlamak** **için** **bazı** **temel**
**kavramları bilmek gerekir.**
**İşletim Sistemi Temelleri**

   - **Uygulamaların** **çalışmasını** ve **etkin** **şekilde** **işlem**
**görmesini** sağlayan **işletim** **sistemi** **programları**,
genel olarak **çalışma** **zamanı** **(runtime)** olarak
adlandırılır.

   - Konteynerleştirmeyi en iyi şekilde anlayabilmek için
önce **sanallaştırma** ile ilgili **bazı** **temel** **kavramları**
**netleştirmek gerekir.**


##### **Fiziksel Sunucular** • En yaygın sanallaştırılan fiziksel BT kaynağı fiziksel **sunucudur.** • Fiziksel bir sunucu; uygulamalar, hizmetler ve **diğer yazılım programlarının barındırılabileceği** bir işletim sistemi ortamı sağlar.

**Sanal Sunucular**

- Fiziksel sunucunun sunduğu işletim sistemi barındırma
ortamı **bir veya birden fazla sanal sunucuya** soyutlanabilir.

- Her bir sanal sunucu, işletim sistemi ortamının yeni ve
ayrılmış bir kopyasını (veya görüntüsünü) sağlayabilir.

- Bu ortama **konuk işletim sistemi (guest OS)** adı verilir.



Fiziksel Sunucu
Temsili


Sanal Sunucu
Temsili


##### • Her bir sanal sunucu, farklı kullanıcı uygulamaları veya hizmet kümelerine sanallaştırılmış bir işletim sistemi ortamı sunabilir. • Bu uygulama veya hizmetler, altında çalışan fiziksel sunucunun nasıl çalıştığına dair herhangi bir bilgiye **ihtiyaç duymaz.** • Bireysel sanal sunuculardan sorumlu yöneticilere, altında yatan **fiziksel sunucuya erişim verilmez!**


- **Hipervizör**
**Fiziksel bir sunucudan** **birden fazla sanal**
**sunucu oluşturup** **çalıştırmaktan sorumlu**
bileşene **hipervizör (hypervisor)** denir.
**Sanal** **sunucular,** **hipervizör** **tarafından**
**kendilerine** sunulan **taklit (emüle edilmiş)**
**donanımı gerçek donanım olarak algılar.**
**Her sanal sunucunun**, **içinde kurulu ve**
**çalıştırılması gereken** **kendi işletim sistemi**
**(konuk işletim sistemi) vardır.**
**Konuk işletim sistemi, fiziksel bir sunucuya**
**kurulmuş** gibi **yönetilmeli** ve **bakım işlemleri**
**yapılmalıdır.**



Hipervizör sembolü


- **Sanallaştırma Türleri**
Sanallaştırma ortamları, temel olarak **fiziksel**
**sunucuda bir işletim sisteminin kurulu olup**
**olmamasına göre ikiye ayrılır.**
**-Tip 1 Sanallaştırma Ortamı:**
**fiziksel sunucuda herhangi bir işletim**
**sistemi kurulu değildir.**
Bunun yerine, fiziksel sunucuya yalnızca
**hipervizör** yüklenir.
**Hipervizör**, **sanal sunucuları oluşturmak** ve
onlara **sanallaştırılmış** **işletim** **sistemi**
**ortamları sağlamakla** sorumludur.


**-Tip 2 Sanallaştırma Ortamı:**
fiziksel sunucuda bir **işletim sistemi kurulu**

**durumdadır** ve bunun üzerine bir **hipervizör**
**de yüklenebilir.**

- Bu durumda, fiziksel sunucuya **işletim**
**sistemi aracılığıyla erişim sağlanabilir** .

- Yine de, **sanal sunucuların oluşturulması** ve
onlara **sanallaştırılmış** **işletim** **sistemi**
**ortamlarının** **sağlanması**, **hipervizörün**
**sorumluluğundadır**


#### **Konteynerleştirme Temelleri**

Bir konteyner, **barındırdığı yazılım programları** için **yalnızca**
**ihtiyaç duyulan kaynakları** **sağlayacak şekilde optimize**
**edilebilen** **sanallaştırılmış** bir **barındırma** **(hosting)**
**ortamıdır.**


- **Konteyner İmajları**
Bir konteyner imajı, dağıtılmış konteynerlerin
oluşturulmasında kullanılan **önceden tanımlanmış bir**
**şablona** benzer.

- **Konteyner Motorları**
**-Önceden tanımlanmış konteyner imajlarına dayanarak**

**konteynerleri oluşturmaktan sorumludur.**


**işletim sistemi üzerine kurulur** ve buradan, **belirli bir**
**konteynerin ihtiyaç duyduğu kaynakları soyutlayarak** sağlar.



Konteyner
motorunun

sembolik
gösterimi



Konteyner

sembolik
gösterimi


❖ **Konteyner motorun uygulanışı** (mimarisi), yanda belirtildiği gibi **iki**

**“katman” (plane)** halinde düzenlenmiştir:
**1. Yönetim Katmanı (Management Plane):**
Yöneticilerin konteyner motoru ortamını **yapılandırıp bakımını**
**yapabilmesini sağlayan** grafiksel kullanıcı arayüzü (GUI) ve komut
satırı araçlarını içerir.
**2. Kontrol Katmanı (Control Plane):**
**Yönetim katmanı aracılığıyla verilen ayarlara** ve **komutlara yanıt**
**olarak konteyner motorunun** otomatik olarak gerçekleştirdiği **tüm**
**diğer işlev ve özellikleri kapsar.**


###### • Pod’lar

**Tek bir konteyneri** ya da **ortak depolama ve/veya ağ**
**kaynaklarını** **paylaşan**, **aynı** **zamanda** **nasıl**
**çalıştırılacaklarını** **belirleyen** **ortak**
**yapılandırmalara sahip** **birden fazla konteyner**
**grubunu** **barındırabilen** **özel bir sistem konteyneri**
**türüdür.**
Pod’lar
###### -Konteyner’ları tek bir yerden yönetimi, -Ortak Kaynak Paylaşımı -İlişkili Uygulama Bileşenlerini Gruplama (web sunucu +yan uygulamalar vb.) gibi çeşitli avantajlar sağlar.


###### • Host (Barındırıcı) Host, bir konteynerin dağıtıldığı (çalıştırıldığı) **ortamdır.** Bu ortam, sunucu (server) ya da düğüm (node) olarak da adlandırılabilir. Host, konteynerin barındırdığı yazılımları çalıştırabilmesi için ihtiyaç duyduğu kaynakları soyutladığı bir işletim sistemi ortamı sağlar. • Birden fazla konteyner, tek bir host üzerinde dağıtılabilir ve çalıştırılabilir.


**Farklı konteyner** ve **pod kombinasyonları**, **farklı host'lar (sunucular)**

**üzerinde dağıtılabilir.**


**Tek bir pod birden fazla host’a** yayılacak **şekilde çalıştırılamaz.**
**Her pod yalnızca tek bir host üzerinde bulunabilir.**


❖ **Konteynerler,** **kullanılan** **konteyner** **motoru**
**podları** **desteklemiyorsa,** **bir** **pod** **içinde**
**olmadan da bir host üzerinde çalışabilir.**
❖ **Bir** **konteyner**, **sanal** **bir** **sunucu** **üzerine**
**dağıtıldığında,** bu durum **iç** **içe** **geçmiş**
**sanallaştırma** **(nested** **virtualization)** olarak
değerlendirilir.


### **Host Kümeleri (Host Clusters)**

- **Host sunucular,** **birlikte çalışacak şekilde** “küme”
(cluster) olarak **birleştirilebilir.**

- Bu şekilde, **daha yüksek işlem kapasitesine sahip**
ve anında **kullanılabilir kaynaklardan oluşan** bir
**havuz oluşturulmuş olur.**

- Hem **sanal** hem de **fiziksel hostlar**, bu tür kümelerde
bir araya getirilebilir .

- Kümeleme (clustering) ortamlarında **host sunucular**
**genellikle “düğüm (node)”** olarak adlandırılır.





(a) Fiziksel **(b)** Sanal host

kümeleme


### **Yaygın Host Küme Türleri**

❖ **Yük Dengelemeli Küme (Load-Balanced Cluster):**


- **İş yüklerini host'lar** arasında **dağıtarak** kaynak kapasitesini
artırmakta uzmandır.

- Aynı zamanda **kaynak yönetiminin merkezileşmesini** sağlar.

- Genellikle, ya bir **küme yönetim platformuna gömülü** olarak ya
da **ayrı bir kaynak** olarak yapılandırılmış bir **yük dengeleyici (load**
**balancer)** içerir.


### **Yaygın Host Küme Türleri**

❖ **Yüksek Erişilebilirlik Kümesi (High Availability – HA Cluster):**

- **Birden fazla host arızalansa** bile **sistemin çalışır** durumda
**kalmasını sağlar** .

- Genellikle, **kümelenmiş kaynakların çoğunun veya tamamının**
**yedekli (redundant)** **sürümlerini içerir** ve **failover sistemi**
sayesinde **arızaları izleyerek iş yüklerini otomatik** olarak sorunlu
host'lardan çalışır durumda olanlara yönlendirir.


### **Yaygın Host Küme Türleri**

❖ **Ölçeklenebilir Küme (Scaling Cluster):**
Bu tür küme, **hem dikey ölçekleme** (mevcut host’un kaynaklarını
artırmak) hem de **yatay ölçekleme** (sisteme yeni host'lar eklemek)
**desteği sağlar.**


**Konteynerleştirme** **platformları**, **yüksek** **performans** ve
dayanıklılık (resiliency) **gereksinimlerini karşılamak** için yukarıda
belirtilen **tüm host küme modellerinden faydalanır** .
Aynı zamanda bu yapılar, konteynerlerin **optimum şekilde**
**dağıtılması** açısından da **kritik öneme sahiptir.**


## **Host Ağları ve Overlay (Kaplamalı) Ağlar**

❖ Her host, üzerinde çalışan konteyner motoruna sahiptir.
❖ Bu **konteyner motoru**, **konteyner imajlarını oluşturmak**,

konteynerleri **dağıtmak** ve **çalıştırmak** ile sorumludur.
❖ **Aynı host üzerindeki** **ilişkili konteynerler**, **yerel host ağı (local**

**host network)** aracılığıyla birbirleriyle iletişim kurabilir.
❖ **Farklı host’lar** üzerindeki **ilişkili konteynerler** ve **konteyner**


**birbirleriyle iletişim kurabilir.**
❖ **Bu iki ağ türü konteyner ağlar olarak adlandırılır.**


Konteyner Ağlar


## **Host Ağları ve Overlay (Kaplamalı) Ağlar**

❖ **Konteyner ağları, yöneticiler tarafından:**

- **Ölçeklenebilirlik** (scalability),

- **Dayanıklılık** (resiliency) gibi yetenekleri destekleyecek şekilde

yapılandırılabilir.

- Ayrıca, barındırılan programların konteyner ağı dışındaki
kaynaklara **erişimini kontrol etmek amacıyla da ayarlanabilir.**


## **Sanallaştırma ve Konteynerleştirme**

**Sanal sunucu** ile **konteyner** arasındaki **temel fark şudur:**

- **Sanal sunucu**, fiziksel bir sunucunun **tüm işletim sisteminin**
**sanal bir kopyasını** sunar.

- **Konteyner** ise, yalnızca barındırdığı yazılım(lar)ın ihtiyaç duyduğu
**işletim sistemi kaynaklarının bir alt kümesini** sağlar.
**Bu nedenle, konteynerler:**

- Daha az yer kaplar,

- Daha hızlı başlar ve

- Sanal sunuculara kıyasla daha verimli çalışır.


## **Fiziksel Sunucularda Konteynerleştirme**


- **Konteynerler** **fiziksel bir sunucu üzerinde**
**dağıtıldığında**, **sanal** **sunuculara** **ihtiyaç**
**olmadığından** dolayı herhangi bir **sanallaştırma**
**ortamına da gerek yoktur.**

- **Altta yatan fiziksel** sunucuda **bir işletim**
**sistemi yüklüdür.**

- **Konteynerleştirme** platformu, **her** **biri yalnızca**
**barındırdığı yazılımlar** için gerekli olan **işletim**
**sistemi** **kaynaklarının** **bir** **alt** **kümesini**
**soyutlayan konteynerler** oluşturabilir.


## **Sanal Sunucularda Konteynerleştirme**

##### Konteynerler bir veya birden fazla sanal sunucu üzerinde dağıtıldığında, konteynerleştirme platformu: • Tip 1 sanallaştırma ortamı ve Tip 2 sanallaştırma ortamı üzerinde bir hipervizör ile birlikte uygulanabilir. • Her iki sanallaştırma ortamı da, konteynerleştirme motorlarının (container engine) çalışabileceği sanal **sunucuların oluşturulmasına olanak tanır.**


- **Hipervizör**, her biri kendi işletim
sistemine sahip **sanal** **sunucular**
**oluşturur** .

- **Her** **sanal** **sunucu**, üzerinde bir
**konteynerleştirme** **platformu**
**barındırır.**

- Bu platform, yalnızca ilgili yazılım
programları için **gerekli olan işletim**
**sistemi** **kaynaklarının** **bir** **alt**
**kümesini** **içeren** **konteynerler**
**oluşturabilir.**


**TİP 2: İşletim Sistemi Kurulu Fiziksel Sunucuda Konteynerleştirme**

❖ Bir **işletim sistemi yüklü fiziksel sunucu**,

üzerinde bir **hipervizör** barındırır.
❖ Bu hipervizör, **kendi işletim sistemlerine**

**sahip sanal sunucu ortamları** oluşturur.

- **Her** **bir** **sanal** **sunucu**, bir
**konteynerleştirme platformu** barındırır ve
bu platform, yalnızca ilgili yazılımların ihtiyaç
duyduğu **işletim sistemi kaynaklarının bir**
**alt kümesini** içeren **konteynerler** oluşturur.


### **Konteynerlerin Sanal Sunucular Üzerinde** **Dağıtılmasının Nedenleri**


- **Fiziksel sunucuda bir işletim sistemi**
**kurulu** **olduğunda** **ortaya** **çıkabilecek**
**güvenlik açıklarıdır** .

- **Bu tür açıklar,** **konteynerlerin doğrudan**
**fiziksel sunucuda** çalıştırılmasını **bazı**
**durumlarda riskli hale getirebilir.**


### **Geliştirme Ortamlarında Tercih: Tip 2 Sanallaştırma**
##### • Geliştirme ve test ortamlarında, konteyner tabanlı çözümler inşa edilirken, sistemlerin hızlı kurulup denenmesinin gerektiği durumlarda kullanılır. • Daha küçük ölçekli çözümler ya da küçük işletmeler için de tercih edilebilir.


### **Üretim Ortamlarında Tercih: Tip 1 Sanallaştırma**

##### • Çoğu üretim ortamında (production environment), işletim sistemi yerine doğrudan bir hipervizörün kurulu olduğu Tip 1 sanallaştırma ortamı tercih edilir. • Bu yapı, daha izole, güvenli ve kaynak açısından verimli bir konteyner çalıştırma ortamı sunar.


## **Konteynerleştirme Teknolojisinin Faydaları**


- **Çözüm Optimizasyonu:**
İzole edilmiş bir ortamın, **yalnızca çözümün ihtiyaç duyduğu** kadar
**kaynakla özelleştirilebilmesi** sayesinde, sistemin kaynak tüketimi
en aza indirilir.

- **Artırılmış** **Ölçeklenebilirlik** :
Konteynerlerin **daha az CPU**, **bellek ve depolama** alanı
kullanması, **onların kullanım taleplerine hızlı** ve etkili şekilde
**ölçeklenmesini mümkün** kılar.


## **Konteynerleştirme Teknolojisinin Faydaları**


- **Artırılmış Dayanıklılık (Resiliency):**
Konteyner ortamlarının özel özellikleri sayesinde, **sistemde bir hata**
**meydana geldiğinde** y **eni çözüm örnekleri (instance) otomatik**
**olarak oluşturularak**, **sistemin çalışmaya devam etmesi**
**sağlanır.**

- **Artırılmış Dağıtım Hızı:**
Konteynerler, **sanal sunuculara göre çok daha hızlı bir şekilde**
**oluşturulabilir** ve **dağıtılabilir** .
Bu da, hızlı dağıtım ihtiyacını karşılayarak, **sürekli entegrasyon (CI)**
**gibi DevOps** yaklaşımlarını destekler.


## **Konteynerleştirme Teknolojisinin Faydaları**


- **Sürüm Desteği (Version Support):**
Konteynerler, **yazılım kodunun ve ona bağlı bağımlılıkların**
**sürümlerinin izlenmesini sağlar.**
Bazı platformlar, geliştiricilerin bir çözümün **farklı sürümlerini**
**takip etmesine**, **sürüm farklarını incelemesine** ve gerektiğinde
önceki sürümlere **geri dönmesine imkân tanır.**

- **Artırılmış Taşınabilirlik (Portability):**
Konteynerleştirilmiş bir çözüm, **farklı** **sunucu** **barındırma**
**ortamları arasında kolayca taşınabilir.**
Bu süreçte, **konteyner içindeki yazılıma herhangi bir değişiklik**
yapılmasına gerek kalmaz.


## **Konteynerleştirmenin Riskleri ve Zorlukları**


- **Host İşletim Sisteminden Yalıtım Eksikliği:**
**Aynı** **fiziksel** **sunucu** **üzerinde** **birden** **fazla** **konteyner**
**dağıtıldığında,** bu konteynerler **aynı host işletim sistemini**
**paylaşır** .


Bu durum, **altta yatan fiziksel sunucunun** **çökmesi** ya da **ele**
**geçirilmesi** (siber saldırı, güvenlik ihlali) hâlinde, üzerinde çalışan
tüm konteynerlerin **etkilenme olasılığını artırır** .


## **Konteynerleştirmenin Riskleri ve Zorlukları**

- **Konteynerleştirme Saldırı Tehdidi:**
Sanal sunucularda, **sanal sunucunun yöneticisi** **alttaki fiziksel**
**sunucunun işletim sistemine erişemez** veya **onu değiştiremez.**
**Ancak konteynerlerde durum farklıdır:**
Aynı fiziksel sunucu üzerinde çalışan tüm konteynerler, **aynı işletim**
**sistemi çekirdeğini (kernel) paylaşır.**
Bu nedenle, bir konteynerin yöneticisi çekirdeğe dolaylı erişim
sağlayabilir.
Bu durum, **sanal sunucular kullanılmadan** konteynerleştirme
platformları **dağıtıldığında, önemli bir güvenlik açığı ortaya**
**çıkarabilir.**


## **Konteynerleştirmenin Riskleri ve Zorlukları**

- **Artan Karmaşıklık:**
Konteynerleştirme teknolojisinin altyapıya eklenmesi, **yeni katmanlar**
**ve tasarım gereksinimleri** getirir.
Bu durum, hem çözüm altyapısının **karmaşıklığını artırabilir**, hem de
**maliyetleri yükseltebilir** .
**Bu karmaşıklık;**

- **Sistemin kurulması** ve **yönetilmesi** için **daha fazla çaba** gerektirir,

- Yeni riskler doğurabilir,

- **Altyapıyı kurmak ve yönetmekle sorumlu kişiler** için **öğrenme**
**eğrisini (learning curve)** uzatabilir.

- Ayrıca, konteynerleştirmenin getirdiği **ek işlem katmanı**, bazı
durumlarda çözümün **performansı üzerinde olumsuz etki** yaratabilir.


## **Konteynerleştirmenin Riskleri ve Zorlukları**

- **Artan Yönetimsel Yük:**
Bir konteyner, yalnızca belirli bir çözüm sürümü için gerekli olan
**işletim sistemi kaynaklarını** sağladığından, **ileride ortaya**
**çıkabilecek yeni çözüm sürümlerine** uyum sağlamak amacıyla
**yeni konteyner sürümlerinin oluşturulması ve yönetilmesi**
gerekebilir.
Bu durum, **sürekli bir yönetimsel çaba** gerektirebilir.

- Oysa **sanal sunucu ortamlarında**, işletim sisteminin tamamı her
zaman çözümle birlikte sunulduğu için, **yeni sürümler için ek**
**yapılandırmalarla uğraşmak** genellikle **daha az önem taşır** .


## **Konteynerleri Anlamak**

Bir konteyner, **her** **türden** **yazılım** **programını**
**içerebilse** de, **en yaygın kullanım alanı**, **daha büyük**
**bir otomasyon çözümünü oluşturan ya da** **onun**
**parçası** **olan** **uygulamaları** **veya** **hizmetleri**
**barındırmaktır.**
❖ **Konteyner Barındırma (Container Hosting)**
Bir konteyner, **tek** **bir** **yazılım** **programını**
**barındırabilir** ve **birden fazla konteyner**, **aynı**
**ortamda yan yana** var olabilir.
Bu durumda her konteyner bağımsız
çalışabilir.


## **Konteynerleri Anlamak**

❖ **Konteynerler ve Podlar**
Bireysel konteynerlerin bir **pod** içinde

**gruplanması**, **ilişkili** **yazılım**
**programlarının** **bir** **arada tutulmasına**
olanak tanır.

- **Ortak bellek (shared memory)** gibi
standart **prosesler arası iletişim (IPC)**
yöntemleriyle haberleşebilir

- **Aynı dosya sistemi**, **veri kümesi**
**(dataset)** veya **veri depolama birimini**
de **ortaklaşa kullanabilirler** .


## **Konteynerleri Anlamak**

❖ **Pod Ortamının Sağladığı Yapı**

- **Özel çalışma ortamını** sağlar;

- yazılım programlarının **birbirlerinden izole kalmasını** garanti eder.
**Podlar**

- **konteyner zincirleri** (container chains),

- **orkestrasyon**

- **ölçekleme (scaling)**
gibi gelişmiş konteynerleştirme yeteneklerini de destekler.
Bu nedenlerle, **birçok konteynerleştirme platformu** tarafından **pod**
**kullanımı zorunlu tutulur.**
Bundan dolayı, çoğu zaman **tek bir konteyner bile bir tekil pod** içinde
barındırılır.


#### Bir yönetici(administrator), yapılandırır, pod içerisine eklenir.


##### ❖ Podların Ortak Depolama Özelliği


##### Podların yaygın bir özelliği, içinde barındırdığı **konteynerlere ortak bir depolama alanı** sağlayabilmesidir . Bu depolama genellikle bir dosya sistemi şeklindedir ve volume (birim) olarak adlandırılır. Bu tür ortak depolama, yüksek hızlı erişim sağladığı için özellikle cazip bir çözümdür.


**Volume içinde saklanabilecek dosya türleri** şunlar olabilir:

- Log (kayıt) dosyaları

- Medya dosyaları

- Yapılandırma (config) dosyaları
Yönetici (administrator), pod’u bu volume’a erişim sağlayacak
şekilde **yapılandırabilir**


##### **Sanal Sunucu Üzerine Dağıtılan Pod’larda Gecikme Riski**

Bir **pod, sanal bir sunucu üzerinde dağıtıldığında**, araya giren **ek**

**sanallaştırma katmanı**, çalışma anında **işlem gecikmesine (latency)**
yol açabilir.
Bazı dağıtım senaryolarında, **aynı fiziksel host üzerinde çalışan** **diğer**

**sanal sunucuların** **yükü** de **performansı olumsuz etkileyebilir.**

- Pod’un **nerede dağıtılacağına karar vermeden önce**, **performans ve**
**gecikme ölçümleri** yapılması önerilir.


### **Konteyner Örnekleri (Instance'ları) ve Kümeleri**

**Aynı yazılım programını barındıran** **birden fazla konteyner örneği**

**(instance)** oluşturulabilir.
Bu durum genellikle, **birden fazla kullanıcı programının aynı anda**

**(eşzamanlı olarak)** bu **yazılımı kullanması gerektiğinde** tercih edilir.

- Bu tür konteyner örneklerine yaygın olarak **"replika (replica)"** adı verilir.


### **Konteyner Örnekleri (Instance'ları) ve Kümeleri**

**Konteyner kümeleri,** **kullanılmadan önce önceden**

**oluşturulmuş** **konteyner örneklerinden** (instance) oluşan
**havuzlardır** .
Bu kümeler:

- **Manuel olarak** oluşturulabilir

- Veya **otomatik olarak** sistem tarafından üretilebilir.

- **Konteyner kümeleri**, **belleğe yüklenir** ve **çağrılana kadar**
**pasif (boşta)** şekilde bekler.

- Ayrıca, **belirli zaman aralıklarında bellekte** yer alacak şekilde
**zamanlanabilirler** .
Örneğin, **yoğun kullanımın beklendiği zaman dilimlerinde**
**aktif tutulabilirler.**


### **Konteyner Örnekleri (Instance'ları) ve Kümeleri**

❖ Konteyner kümeleri, **özellikle** **hizmet** **(service)-tabanlı**
**çözümler** için, **yüksek** **performans** **gereksinimlerini**


(provisioning).
❖ **Konteyner** **küme** **ortamları** aynı zamanda **otomatik**
**ölçekleme (auto-scaling) yetenekleri** sunar.
❖ Bu sayede sistem, **kullanım talebine göre dinamik olarak**

**büyüyüp küçülebilir.**


### **Konteyner Paket Yönetimi (Container Package** **Management)**



**Konteyner** **paket** **yönetimi**, **konteynerleştirilmiş**
**uygulamalar** içindeki **yazılım** **paketlerinin** **ve**
**bağımlılıkların yönetilmesi** sürecini ifade eder.
Bu yönetim süreci, bir **uygulamanın ve onun çalışması için**

**gereken tüm bağımlılıkların** **tek bir taşınabilir birim**
**(package)** içinde bir araya getirilmesini sağlar.

- **Bu sayede, oluşturulan paket**, **konteyner teknolojisini**
**destekleyen herhangi bir sistemde** sorunsuz şekilde
dağıtılabilir ve çalıştırılabilir.



Paket


### **Konteyner Paket Yönetimi (Container Package** **Management)**



**Konteyner paket yöneticisi**, konteynerleştirilmiş uygulamaların



**paketlenmesini ve dağıtımını kolaylaştıran bir araçtır** .
**Konteyner paket yöneticileri genellikle şu özellikleri içerir:**

- **Konteyner imajlarını oluşturma, etiketleme (tagging) ve bir**
**kayıt deposuna (container registry) gönderme** işlemleri için
**komut satırı araçları**

- **İmajları** ve **bağımlılıkları** **oluşturma ve yönetme**

- **Paket içeriğini** ve **bağımlılıklarını tanımlamak** için **şablonlar**
**(templates)** veya **yapılandırma dosyaları** kullanma

- Paketi **sürümleme (versioning)** ve zaman içinde **yönetme**
**imkânı**



Paket
deposu



Konteyner paket
yöneticisi


### **Konteyner Paket Yönetimi (Container Package** **Management)**
##### ❖ Konteyner paket yöneticisi, konteynerlerin önceden tanımlı bir dağıtım iş akışı mantığı (deployment workflow logic) çerçevesinde ilk dağıtımını koordine etmek için kullanılır . ❖ Bu iş akışı, genellikle bir konteyner dağıtım dosyası (container deployment file) içinde tanımlanır.


### **Konteyner Paket Yönetimi (Container Package** **Management)**



❖ **Dağıtım** **iş** **akışını** **(deployment** **workflow)**
gerçekleştirmeden önce, özel bir **dağıtım optimize edici**
**program (deployment optimizer)** devreye girer.

- Bu program, **paket içeriğini önceden analiz eder** ve
**küme (cluster) içindeki** uygun hostları değerlendirerek,
konteynerlerin dağıtılması için en uygun hedefleri
belirler.

##### **Paket → Dağıtın Optimize Edici → Ideal Host Seçimi**



Dağıtım
optimize
edici


**Dağıtım Optimize Edicinin Dikkate Alabileceği Faktörler:**

- **Donanım ve yazılım politikası sınırlamaları:**
Belirli host’larda yalnızca belirli donanım türlerinin (örneğin GPU) ya
da lisanslı yazılımların kullanılması gibi koşullar.

- **Yakınlık ve uzaklık kuralları (affinity / anti-affinity):**
Bazı konteynerlerin birlikte, bazılarının ise ayrı host’larda çalışması
gerektiği durumlar.

- **Veri yakınlığı (data locality):**
Konteynerin, ihtiyaç duyduğu verinin bulunduğu fiziksel konuma yakın
çalışması gerekebilir.

- **İş yükü çakışması (inter-workload interference):**
Aynı host’ta çalışan diğer iş yüklerinin, yeni yerleştirilecek
konteynerin performansını olumsuz etkileyip etkilemeyeceği.


❖ **Konteyner Paketleri ve Sürüm Yönetimi**
Bir **paket**, genellikle **bir çözümü oluşturan tüm konteynerleri temsil**

**eder** .
Bu nedenle, **konteyner paket yöneticileri** genellikle **birbiriyle ilişkili**
**konteynerlerden oluşan bir grup** için oluşturulur.

- Bu bağlamda, **paket deposu (package repository)**, aynı zamanda
**uygulama sürüm yönetimi** için de bir yöntem sunar.
**Bir pakette tanımlanabilecek öğelere örnekler:**

- Belirli bir konteynerin **hangi host üzerine dağıtılacağı**

- Belirli bir konteynerin **hangi pod içinde çalıştırılacağı**

- Birden fazla konteynerin **hangi sırayla dağıtılacağı**


❖ **Paketlerin Yeniden Kullanımı:**
**Dağıtımdan sonra,** bu paketler **genellikle paket deposunda**
**tutulmaya** devam eder.
**Çünkü yeniden kullanılabilir durumdadırlar.**
Örneğin, **bir konteyner grubu yeni bir host’a taşınacaksa**,
**aynı konteyner dağıtım dosyası (deployment file)**
sadece **yeni host bilgileriyle güncellenip tekrar kullanılabilir** .


**Yönetici,**

- bir paket hazırlar,

- bunu paket deposuna
kaydeder

- konteynerlerin **dağıtılma**
**zamanı geldiğinde**,

- paketi konteyner **paket**
**yöneticisine** atar.
❖ **Docker Compose** ve **Helm**,

en yaygın kullanılan konteyner
paket yöneticilerinden
bazılarıdır.


## **KAYNAKLAR**


 - Thomas Erl, Eric Monroy - Cloud Computing_ Concepts,
Technology, Security, and Architecture (The Pearson Digital
Enterprise Series from Thomas Erl)-Pearson (2023)


