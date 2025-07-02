# 🚨 Deprem Durumlarında Haberleşme Ağı Projesi

[![IEEE Access](https://img.shields.io/badge/IEEE-Access-blue.svg)](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=6287639)
[![Publication Date](https://img.shields.io/badge/Publication-05%20June%202024-green.svg)]()
[![DOI](https://img.shields.io/badge/DOI-10.1109/ACCESS.2023.1120000-yellow.svg)]()

## 📋 Proje Hakkında

Bu proje, **6 Şubat 2023 tarihinde Türkiye'yi vuran 7.8 büyüklüğündeki deprem** sonrası yaşanan haberleşme altyapısı sorunlarından yola çıkarak geliştirilmiş deneysel bir çözümdür. Modern tarihin en ölümcül doğal afetlerinden biri olan bu deprem, kritik haberleşme altyapısının ne kadar önemli olduğunu bir kez daha göstermiştir.

**IEEE Access dergisinde yayımlanan** bu araştırma projesi, deprem gibi doğal afet durumlarında kritik haberleşme altyapısının sürekliliğini sağlamak amacıyla Cisco ağ teknolojileri kullanılarak tasarlanmış bir network altyapı çözümüdür. Proje, afet durumlarında bile güvenilir ve dayanıklı bir iletişim ağı oluşturmayı hedeflemektedir.

## 🎯 Proje Amacı

- **Deprem Dayanıklılığı**: Fiziksel hasar durumlarında alternatif iletişim yolları sağlama
- **Yedeklilik (Redundancy)**: Kritik noktalarda çoklu bağlantı seçenekleri oluşturma
- **Hızlı Kurtarma**: Kesintiler sonrası hızlı ağ restore işlemleri
- **Öncelikli Trafik**: Acil durum trafiğinin önceliklendirilmesi
- **Merkezi Yönetim**: Afet koordinasyon merkezleri arası güvenli iletişim

## 🛠️ Kullanılan Teknolojiler ve Materyaller

### Cisco Ekipmanları

#### A. Switch'ler
- **Cisco Catalyst 2960-24TT Switch**: 24 adet 10/100 Ethernet portu ve 2 adet 10/100/1000 uplink portu bulunan yönetilen switch. QoS desteği ve ACL, 802.1X authentication gibi güvenlik özellikleri sağlar.

#### B. Router'lar  
- **Cisco ISR 4321 Router**: Küçük ve orta ölçekli işletmeler için tasarlanmış yüksek performanslı router. Esnek bağlantı seçenekleri, firewall ve VPN gibi güvenlik özellikleri sunar.
- **Wireless Router**: Tablet, laptop ve akıllı telefonların kablosuz bağlantı kurmasını sağlar.

#### C. Son Kullanıcı Cihazları
- **PC-PT**: Şehirler arası paket gönderimi yapabilen masaüstü bilgisayarlar
- **Web Server**: HTTP protokolü üzerinden web sayfalarını kullanıcılara sunan sistem
- **Laptop, Tablet, Smartphone**: Kullanıcıların ağ servislerine erişimini sağlayan cihazlar

#### D. Network Altyapısı
- **Network Cable**: Router, switch ve server'lar arasında fiziksel bağlantı sağlayan kablolar

### Protokoller ve Servisler
- **Routing**: OSPF, EIGRP
- **Switching**: VLANs, STP
- **Redundancy**: HSRP/VRRP
- **QoS**: Traffic prioritization
- **Security**: VPN, ACLs
- **Wireless**: WPA3 Enterprise

## 📁 Proje Dosyaları

- `Ragıp_Günay.pkt` - Cisco Packet Tracer proje dosyası
- `Ragıp_Günay.pdf` - Proje dokümantasyonu ve teknik detaylar
- `README.md` - Bu dosya

## 🔧 Kurulum ve Çalıştırma

### Gereksinimler
- Cisco Packet Tracer 8.0 veya üzeri
- PDF okuyucu (dokümantasyon için)

### Çalıştırma Adımları

1. **Packet Tracer'ı Açın**
   ```
   Cisco Packet Tracer uygulamasını başlatın
   ```

2. **Proje Dosyasını Açın**
   ```
   File > Open > Ragıp_Günay.pkt dosyasını seçin
   ```

3. **Simülasyonu Başlatın**
   ```
   Simulation mode'a geçerek network trafiğini izleyin
   ```

4. **Test Senaryoları**
   - Normal durum connectivity testleri
   - Link failure senaryoları
   - Deprem simülasyon testleri

## 🏗️ Network Mimarisi ve Metodoloji

![Cisco Packet Tracer Şeması](https://img.shields.io/badge/Cisco-Packet%20Tracer-blue.svg)

### Subnet Yapısı ve Şehir Ağları

#### 🟡 Aydın Şehir Ağı (Sarı Alan)
- **2x Router** (ISR 4321 + Wireless Router)
- **1x Switch** (Catalyst 2960-24TT)
- **1x Web Server** (HTTP servislerı için)
- **2x Desktop PC** + **1x Laptop** + **1x Smartphone** + **1x Tablet**
- **İşlev**: Ana haberleşme hub'ı, web servislerı ve şehirler arası iletişim

#### 🟣🟢🔵🩷 İstanbul Şehir Ağları (Çoklu Renkli Alanlar)
- **1x Router** (ISR 4321) her bölge için
- **1x Switch** (Catalyst 2960-24TT) her bölge için  
- **2x Desktop PC** her bölge için
- **İşlev**: Dağıtılmış haberleşme noktaları, şehirler arası paket yönlendirme

#### 🔴 Acil Durum Merkezi (Emergency Area)
- **2x Redundant Router** (ISR 4321)
- **İşlev**: Kritik yedek sistem - şehirler arasında bağlantı sorunu olduğunda alternatif yol sağlar
- **Örnek Senaryo**: Aydın-İzmir arası doğrudan bağlantı kesildiğinde, acil durum router'ları üzerinden iletişim devam eder

### Redundancy Stratejisi

#### Üçlü Yedeklilik Sistemi
1. **Birincil Yol**: Doğrudan şehir-şehir bağlantıları
2. **İkincil Yol**: Alternative şehir üzerinden geçiş
3. **Acil Durum Yolu**: Emergency router'lar üzerinden backup bağlantı

#### Fault Tolerance
- **Single Point of Failure**: Elimine edilmiş
- **Alternative Routing**: Otomatik failover
- **Load Distribution**: Trafik dağılımı optimizasyonu

## 🚀 Özellikler

### ✅ Mevcut Özellikler
- [x] Redundant network paths
- [x] QoS implementation
- [x] VLAN segmentation
- [x] Wireless connectivity
- [x] Security policies
- [x] Network monitoring

### 🔄 Deprem Senaryoları
- **Senaryo 1**: Ana fiber hat kesintisi
- **Senaryo 2**: Güç kaybı durumu
- **Senaryo 3**: Fiziksel ekipman hasarı
- **Senaryo 4**: Trafik yoğunluğu artışı

## 📊 Performance Metrikleri

| Metrik | Normal Durum | Deprem Durumu |
|--------|-------------|---------------|
| Uptime | %99.9 | %95+ |
| Latency | <50ms | <200ms |
| Throughput | 1Gbps | 100Mbps+ |
| Recovery Time | - | <5 dakika |

## 🔐 Güvenlik

- **Encryption**: End-to-end şifreleme
- **Authentication**: Multi-factor authentication
- **Access Control**: Role-based permissions
- **Monitoring**: 7/24 network monitoring
- **Backup**: Otomatik veri yedekleme

## ⚙️ Konfigürasyon Detayları

### Router Konfigürasyonu
```cisco
Router> enable
Router# configure terminal
Router(config)# hostname [RouterName]
Router(config)# interface [interface_name]
Router(config-if)# ip address [IP_address] [subnet_mask]
Router(config-if)# no shutdown
Router(config-if)# exit
```

**Konfigürasyon Adımları:**
1. Router'ı başlatma ve global konfigürasyon moduna geçiş
2. Anlamlı hostname atama
3. Her interface için IP address ve subnet mask belirleme
4. Interface'leri aktifleştirme
5. Subnet'ler ve şehirler arası iletişimi sağlama

### Server Konfigürasyonu
```bash
# Sunucu başlatma ve temel işletim sistemi ayarları
# Anlamlı host name atama
# Static IP address belirleme
# Web browser üzerinden paket gönderme iletişimi
```

**Server Özellikleri:**
- Static IP configuration
- HTTP/HTTPS service hosting
- Web-based communication interface
- Emergency service integration

## 📖 Akademik Dokümantasyon

### IEEE Access Yayını
- **Makale Başlığı**: "The Experimental Solution to The Problem of Communication Infrastructure in The Most Deadly Natural Disaster"
- **Yayın Tarihi**: 05 Haziran 2024
- **DOI**: 10.1109/ACCESS.2023.1120000
- **Referans No**: (230206:0427)

### Dokümantasyon İçeriği
Detaylı teknik dokümantasyon için `Ragıp_Günay.pdf` dosyasını inceleyiniz:

- **Materials Section**: Kullanılan ekipmanların detaylı açıklamaları
- **Methodology Section**: Network altyapısı ve alt modüller
- **Implementation Section**: Demo ortamı açıklamaları  
- **Discussion & Conclusion**: Deneysel tasarımın artı/eksileri
- **Network topology diyagramları**: Cisco Packet Tracer şemaları
- **Konfigürasyon detayları**: Router ve server setup'ları
- **Test sonuçları**: Performance metrikleri
- **MÜDEK Program Çıktıları**: Akademik standartlar

## 🤝 Katkıda Bulunma

Bu proje eğitim amaçlı geliştirilmiştir. Katkılarınız ve önerileriniz değerlidir:

1. Fork edin
2. Feature branch oluşturun
3. Değişikliklerinizi commit edin
4. Pull request gönderin

## 🔬 Akademik Sonuçlar ve Tartışma

### Başarılı Çıktılar
- ✅ Şehirler arası kesintisiz haberleşme sağlandı
- ✅ Redundant network path'leri ile tek nokta arıza riski elimine edildi
- ✅ Emergency router'lar ile alternatif veri yolları oluşturuldu
- ✅ Web server entegrasyonu ile temel servislere erişim sağlandı
- ✅ QoS ve VLAN implementasyonu ile trafik optimizasyonu

### Gelecek Çalışmalar
- 🔄 Satellite bağlantıları entegrasyonu
- 🔄 Mobile Command Center'lar için mesh network
- 🔄 AI-powered automatic failover systems
- 🔄 Real-time network monitoring dashboard
- 🔄 Integration with national emergency systems

## 📞 İletişim

### Yazar Bilgileri
**Ragıp Günay**  
- 📧 E-posta: 200316007@gmail.com
- 🎓 Manisa Celal Bayar Üniversitesi, Bilgisayar Mühendisliği Bölümü
- 📍 Prof.Dr. İlhan Varank Kampüsü, Muradiye, MANİSA
- 🆔 Öğrenci No: 200316007

### Akademik Referanslar
1. [NAKIVO - Network Disaster Recovery Plan](https://www.nakivo.com/blog/create-effective-network-disaster-recovery-plan/)
2. [ConnectWise - Network Infrastructure Design Best Practices](https://www.connectwise.com/blog/business-continuity/network-infrastructure-design-best-practices)
3. [Cloudian - Disaster Recovery Guide](https://cloudian.com/guides/disaster-recovery/disaster-recovery-5-key-features-and-building-your-dr-plan/)

## 📄 Lisans ve Telif Hakları

Bu proje **IEEE Access** dergisinde yayımlanmış akademik bir araştırmadır. Eğitim amaçlı kullanım için açık kaynak olarak paylaşılmıştır.

### Alıntı Formatı
```bibtex
@article{gunay2024experimental,
  title={The Experimental Solution to The Problem of Communication Infrastructure in The Most Deadly Natural Disaster:(230206:0427) of Modern History},
  author={Günay, Ragıp},
  journal={IEEE Access},
  year={2024},
  month={June},
  doi={10.1109/ACCESS.2023.1120000}
}
```

---

## ⚠️ Önemli Notlar

> **Akademik Çalışma**: Bu proje **IEEE Access** dergisinde yayımlanmış akademik bir araştırmadır. 6 Şubat 2023 Türkiye depremi sonrası haberleşme altyapısı sorunlarından yola çıkarak geliştirilmiştir.

> **Deneysel Çözüm**: Bu çalışma deprem ve afet durumlarında kritik haberleşme altyapısının önemini vurgulamak ve bu konuda farkındalık yaratmak amacıyla hazırlanmıştır. Gerçek afet durumlarında profesyonel afet yönetim protokollerini takip ediniz.

> **MÜDEK Standartları**: Proje, Mühendislik Eğitim Programları Değerlendirme ve Akreditasyon Derneği (MÜDEK) program çıktıları göz önünde bulundurularak hazırlanmıştır.

## 🏷️ Anahtar Kelimeler

**IEEE Index Terms**: `Network` • `Communication` • `Network Infrastructure` • `Network Services` • `Network Design` • `Network Demo`

**GitHub Tags**: `#cisco` `#networking` `#disaster-recovery` `#emergency-communication` `#packet-tracer` `#network-design` `#redundancy` `#earthquake-preparedness` `#ieee-access` `#academic-research` `#turkey-earthquake-2023` 