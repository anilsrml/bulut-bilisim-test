# Bulut Güvenliği ve Siber Güvenliğe Giriş — Notlar

> **Kaynak:** Thomas Erl, Eric Monroy - *Cloud Computing: Concepts, Technology, Security, and Architecture* (Pearson, 2023)

---

## 1. Temel Güvenlik Terminolojisi

**Bilgi Güvenliği:** Sistemlerin ve verilerin bütünlüğünü ve erişimini korumak için çalışan karmaşık **teknikler, teknolojiler, düzenlemeler ve davranışlar bütünüdür.**

### CIA Üçlüsü

| İlke | Tanım | Buluttaki Karşılığı |
|---|---|---|
| **Gizlilik** (Confidentiality) | Bilgiye yalnızca yetkili tarafların erişmesi | Taşınan ve depolanan veriye erişimin sınırlandırılması |
| **Bütünlük** (Integrity) | Bilginin yetkisiz tarafça değiştirilmemiş olması | Veri depolama, işleme ve erişim süreçlerini kapsar |
| **Erişilebilirlik** (Availability) | Sistemin belirli zaman diliminde kullanılabilir olması | Sağlayıcı ile taşıyıcı arasında **paylaşılan sorumluluk** |

**Doğruluk (Authenticity):** Bilginin **yetkili kaynaktan geldiğini** kanıtlar; **inkâr edilemezlik (non-repudiation)** ilkesini de kapsar. İnkâr edilemez işlemlerde erişim **zorunlu olarak kaydedilmelidir.**

### Güvenlik Kontrolleri ve Mekanizmalar

- **Güvenlik kontrolleri:** Tehditleri önlemek veya riskleri azaltmak amacıyla kullanılan önlemlerdir. Nasıl uygulanacağı **güvenlik politikasında** belirtilir.
- **Güvenlik politikası:** Kritik BT kaynaklarını korumak için sistemin nasıl işletileceğini belirten **kural ve uygulamalar bütünüdür.**
- **Güvenlik mekanizmaları:** Savunma altyapısının bileşenleridir. Örnekler: Hashing, Dijital İmzalar, VPN, MFA.

| Kontrol | Açıklama |
|---|---|
| **IAM** | Kimlik ve erişim yönetimi |
| **MFA** | Çok faktörlü doğrulama |
| **Firewall** | Ağ trafiği kontrolü |
| **Encryption** | Veri koruma (şifreleme) |
| **SIEM** | Güvenlik olayı izleme ve analiz |

---

## 2. Temel Tehdit Terimleri

| Terim | Açıklama |
|---|---|
| **Risk** | Belirli bir eylem sonucunda ortaya çıkabilecek **istenmeyen kayıpların olasılığı.** Dış tehditler, içsel zafiyetler, insan hatası ve teknolojik arızaları kapsar. |
| **Zafiyet** (Vulnerability) | BT ortamındaki **kusur, açıklık ya da zayıflık.** Fiziksel ya da dijital olabilir; saldırganlar sömürmeye, kuruluşlar gidermeye çalışır. |
| **Sömürme** (Exploit) | Saldırganın mevcut bir zafiyetten **kendi çıkarı için faydalanması.** |
| **Zero-Day** | Kuruluşun henüz **farkında olmadığı ya da yamalayamadığı** zafiyet. |
| **Security Breach** | Bilgiye veya sistemlere **yetkisiz erişimle** sonuçlanan olay; saldırgan güvenlik kontrollerini **aşmayı başardığında** gerçekleşir. |
| **Data Breach** | Saldırganın **gizli bilgileri ele geçirdiği** ihlal. Önlem: **CIEM** (bulutta kim-hangi kaynağa-hangi yetkiyle erişiyor denetler). |
| **Data Leak** | Herhangi bir saldırı olmadan hassas bilgilerin **yetkisizlere açık hale gelmesi.** Önlem: **DLP** sistemleri (Google Cloud DLP, AWS Macie). |
| **Tehdit** | Kuruluşa yönelik bilinen/potansiyel saldırı; tüm tehditler = **tehdit ortamı (threat landscape).** |
| **Saldırı** | Tehdidin saldırgan tarafından **fiilen gerçekleştirilmesidir.** |

### Saldırgan Türleri

| Tür | Açıklama |
|---|---|
| **Siber Suçlular** | Kâr/yasa dışı faaliyet amacıyla gizli bilgi çalar. |
| **Kötü Niyetli Kullanıcılar** | Ayrıcalıklarını kötüye kullanan yetkili kişiler (art niyetli çalışanlar). |
| **Siber Aktivistler** | Politik, dini veya sosyal amaçla kötü amaçlı faaliyet yürütür. |
| **Devlet Destekli Saldırganlar** | Bir devlet tarafından görevlendirilen/finanse edilen saldırganlardır. |

> Yetkisiz erişim sağlayan saldırgan artık **"intruder (izinsiz giriş yapan)"** olarak adlandırılır.

### Saldırı Vektörü vs. Saldırı Yüzeyi

- **Saldırı vektörü:** Saldırganın zafiyeti sömürmek için **izlediği yol** (e-posta ekleri, pop-up'lar, anlık mesajlar).
- **Saldırı yüzeyi:** Bir sisteme erişmek için kullanılabilecek **tüm saldırı vektörlerinin toplamıdır.** Vektör, yüzeyin bir parçasıdır.

---

## 3. Tehdit Aktörleri (Threat Agents)

Tehdit aktörü; saldırı kapasitesine sahip olduğu için tehdit oluşturan varlıktır. Tehditler **iç/dış kaynaklı**, **insan ya da yazılım** tabanlı olabilir.

| Aktör | Temel Özellik |
|---|---|
| **Anonim Saldırgan** | Yetkisiz, güvenilmeyen harici kullanıcı/program. Genel ağlardan saldırır; hesap atlatma ve kimlik bilgisi çalmaya odaklanır. |
| **Kötü Niyetli Hizmet Aracısı** | Bulut içindeki ağ trafiğini **yakalar ve yönlendirir.** İletilerin içeriğini bozabilir. |
| **Güvenilir Saldırgan** (Kötü Niyetli Kiracı) | Aynı bulut ortamını paylaşan, **meşru kimlik bilgilerini kötüye kullanan** kişi. Saldırıları bulutun **güven sınırları içinden** gelir. Zayıf auth hackler, şifre kırar, DoS başlatır. |
| **Kötü Niyetli İç Tehdit** (Malicious Insider) | Bulut sağlayıcısı adına/ilişkili hareket eden, **mevcut veya eski çalışanlar** ya da 3. taraflar. Yönetici ayrıcalıklarına sahip olabilir. |

---

## 4. Yaygın Tehditler (Common Threats)

| Tehdit | Açıklama |
|---|---|
| **Trafik Dinleme** (Eavesdropping) | Kötü niyetli hizmet aracısının bulut trafiğini **pasif olarak yakalaması.** |
| **Kötü Niyetli Aracı** (Malicious Intermediary) | İletinin **yakalanıp değiştirilmesi;** gizliliği ve/veya bütünlüğü tehlikeye atar. |
| **DoS** (Hizmet Dışı Bırakma) | BT kaynaklarını **sahte istekler, yoğun trafik veya aşırı kaynak tüketimiyle** devre dışı bırakır. Meşru kullanıcılar hizmete erişemez. |
| **Yetersiz Yetkilendirme** | Saldırgana **yanlışlıkla veya aşırı geniş** yetkiyle erişim verilmesi. Zayıf parola/paylaşımlı hesap riski artırır. |
| **Sanallaştırma Saldırısı** | Sanallaştırma platformundaki zafiyetler sömürülerek **alttaki fiziksel kaynaklara** saldırı. Farklı kiracıların kaynakları **çakışan güven sınırları** oluşturur. |
| **Konteyner Saldırısı** | Konteynerler aynı ana OS'u paylaştığı için ana sistem ele geçirilirse **tüm konteynerler etkilenir.** Azaltma: Konteynerleri sanal sunucu içinde çalıştır → diğer sanal sunucular etkilenmez. |

---

## 5. Kötü Amaçlı Yazılım (Malware) ve Saldırı Türleri

**Malware:** Sisteme zarar vermek amacıyla tasarlanan yazılımdır (veri çalma, silme, dinleme, bilgi toplama).

| Tür | Açıklama |
|---|---|
| **Virüs** | Dosyalara bulaşarak yayılan, kendini çoğaltan yazılım. |
| **Trojan** | Meşru uygulama gibi görünen; arka kapı, kod enjeksiyonu gibi zararlı faaliyetler yapar. |
| **Adware** | İstenmeyen reklam/pop-up gösterir; hassas bilgi toplayabilir, sistemi yavaşlatır. |
| **Ransomware** | Verilere erişimi kısıtlar, fidye talep eder. RCE yoluyla da başlatılabilir. |
| **Rogue Antivirus** | Antivirüs gibi davranır; sahte uyarılarla "tam sürüm" satın aldırmaya çalışır. |
| **Crypto Jacking** | Web'e gömülü script'lerle kullanıcı habersiz **kripto para madenciliği** yaptırır. |
| **Worm** | Kendi kendini çoğaltan, ağ üzerinden yayılan program. Doğrudan zarar vermez, kaynak tüketir. |

### Diğer Önemli Saldırı Türleri

| Saldırı | Açıklama |
|---|---|
| **Sosyal Mühendislik / Phishing** | Bireyleri kandırarak hassas bilgi ifşa ettirme veya zararlı eylem yaptırma. |
| **Botnet** | Farklı cihazlardaki botların oluşturduğu eşgüdümlü ağ. DDoS, crypto jacking, spam, veri hırsızlığı, yeni bot devşirme için kullanılır. Dark web'den **satın alınabilir veya kiralanabilir.** |
| **Privilege Escalation** | Sınırlı yetkili hesap ele geçirildikten sonra **yönetici yetkisi kazanmaya** çalışma. |
| **Brute Force** | Çok sayıda kullanıcı adı/parola kombinasyonu deneyerek erişim. **Credential Stuffing:** önceki ihlallerden ele geçirilen bilgilerin başka sistemlerde yeniden kullanımı. |
| **RCE** (Uzaktan Kod Yürütme) | Saldırganın uzaktaki cihazda **komut çalıştırması.** Malware indirme veya tunneling ile gerçekleşir. Botnet/ransomware/trojan tarafından da kullanılır. Bilgi toplama aşamasıyla başlar. |
| **SQL Injection** | Web uygulaması giriş alanına **kötü amaçlı SQL kodu** yerleştirerek sunucuda çalıştırma. |
| **Tunneling** | Veriyi yetkili bir protokol içine gömerek **güvenlik duvarı kontrollerini atlatma.** Veri dışarı çıkabilir / zararlı veri içeri girebilir; uyarı tetiklenmez. |
| **APT** (Gelişmiş Kalıcı Tehdit) | Uzun zaman dilimine yayılmış, eşgüdümlü saldırı. Temel hedef: sisteme sızdıktan sonra **kalıcı olarak yerleşmek.** |

---

## 6. İç Tehdit (Insider Threat) ve Ek Hususlar

**İç tehdit:** Personel veya tesislere erişimi olan kişilerden kaynaklanır. Fiziksel donanım, web siteleri, sosyal medya ve bilgi varlıklarını tehlikeye atabilir.

| Tür | Açıklama |
|---|---|
| **Kötü Niyetli** | Memnuniyetsiz çalışanın sisteme zarar verme girişimi. |
| **Kazara** | Bilgisizlik/insan hatası (dosya silme, gizli veri paylaşımı). |
| **İhmalkâr** | Güvenlik standartlarına uymama isteksizliği. |

**Hatalı Uygulamalar:** Yetersiz tasarım/yapılandırma → BT kaynaklarının gizliliğini, bütünlüğünü ve kullanılabilirliğini tehlikeye atar.  
**Sözleşmeler:** Bulut sağlayıcısının sorumluluğu ne kadar fazlaysa, kullanıcının riski o kadar azdır.

---

## 7. Risk Yönetimi (Döngüsel Süreç)

`Risk Değerlendirmesi → Riskin Bertaraf Edilmesi → Riskin Kontrolü → (döngü)`

| Aşama | İçerik |
|---|---|
| **1. Risk Değerlendirmesi** | Bulut ortamı zayıflık/eksiklikler için analiz edilir. Sağlayıcıdan geçmiş saldırı istatistikleri istenebilir. |
| **2. Riskin Bertaraf Edilmesi** | Azaltma politikaları geliştirilir. Seçenekler: tamamen kaldırma, azaltma, dış kaynak, sigorta, bütçeye dahil etme. |
| **3. Riskin Kontrolü** | **(A)** Olayları gözlemle → **(B)** Önceki değerlendirmelerle karşılaştır → **(C)** Bertaraf etkinliğini ölç, gerekirse politikayı güncelle. Sağlayıcı veya kullanıcıyla ortak yürütülebilir. |

---

## Hızlı Referans

| Kavram | Özet |
|---|---|
| CIA Üçlüsü | Gizlilik · Bütünlük · Erişilebilirlik |
| Authenticity / Non-repudiation | Yetkili kaynaktan gelme kanıtı + inkâr edilemezlik |
| Zero-Day | Bilinmeyen/yamalanmamış zafiyet |
| CIEM | Bulutta erişim yetkisi denetimi (Data Breach önlemi) |
| DLP | Veri kaybı önleme (Data Leak önlemi — AWS Macie, Google Cloud DLP) |
| IAM / MFA / SIEM | Erişim yönetimi / Çok faktörlü doğrulama / Olay izleme |
| Threat Landscape | Kuruluşa yönelik tüm tehditler bütünü |
| Intruder | Yetkisiz erişim sağlayan saldırgan |
| APT | Uzun vadeli kalıcı tehdit |
| RCE | Uzaktan kod/komut çalıştırma |
| Tunneling | Trafiği protokol içinde gizleyerek taşıma |
| Botnet | Eşgüdümlü bot ağı (kiralanabilir/satın alınabilir) |
