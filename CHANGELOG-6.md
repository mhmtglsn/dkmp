# Değişiklik Günlüğü (CHANGELOG)

DKMP Saha Denetim Asistanı — tek dosyalık HTML uygulaması.
Biçim: [Keep a Changelog](https://keepachangelog.com/tr/) esaslı. 1.0.0 öncesi kayıtlar geliştirme sayacıdır (vNN).

Tüm hukuki içerik, alan uzmanı (DKMP veteriner hekimi) onayından geçmiştir. Mevzuat değiştikçe içerik güncellenir.

---

## [1.9.3] — 2026-07
### Düzeltildi
- **Kart–sihirbaz köprüsü tamamlandı.** Küratörlü kartların hukuki metni, Ek-18 sihirbazının bazı yollarında (tanımsız tür, yırtıcı kuş, GM 16.07.2026 görüşü) görünmüyordu — 14 kart etkileniyordu. Örnek: Gökdoğan kartındaki "ruhsatlı üretim" şartı sihirbazda kayboluyordu. Kart metni tek değişkende toplandı, dört yolun tamamına bağlandı. Sonuç: 161/161 kart, sıfır kayıp.
### Eklendi
- **`t_kartkopru.js` denetim betiği:** her kartın hukuki metninin sihirbazda görünüp görünmediğini tarar; kayıp varsa hangi yolda kaybolduğunu raporlar.

## [1.9.2] — 2026-07
### Düzeltildi
- **Sihirbazda çelişkili GM ifadesi.** Aynı kutuda "Genel Müdürlüğe görüş sorulmaz" ile "Genel Müdürlük görüşü alınmalıdır" yan yana çıkıyordu. İzin kararı (il şube müdürlüğü verir) ile Ek-I kısıtları (ithalatta TÜBİTAK görüşü, W kodlu örnekte GM'ye sorma) ayrıştırıldı.
- Küratörlü kartın hukuki metni sihirbazın grup yolunda gösterilmeye başlandı; tekrarı önlemek için kart varsa Ek-I uyarısı kısa denetim notuna düşer.

## [1.9.1] — 2026-07
### Düzeltildi
- **CITES Ek-I esaret üretimi (C/D) ticareti — 17 kart.** Önceki metin "Ticari satış yalnız esaret üretimi + özel izinle" derken DİKKAT alanı "Ticari amaçla tutulamaz" diyordu; ikisi çelişiyordu. Md.60'ın tam metnine göre düzeltildi: yasak **doğadan alınmış (W)** örneklere özgüdür — *"Kategori (A) da yer alan türlerin doğadan alınmış örnekleri ticari amaçlarla kullanılamaz, hayvan satış yerlerinde bulundurulamaz."* Esaret üretimi (C/D kaynak) örneklerin ticareti CITES belgesiyle mümkündür.
- Etkilenen kartlara açık `durum:"sartli"` alanı eklendi: yeni metindeki "bulundurulamaz" kelimesi statü çıkarımını tetikleyip 17 papağanı hatalı biçimde "yasak" göstermişti.

## [1.9.0] — 2026-07
### Düzeltildi — Ürün bulundurma rehberi (Md.49 uyumu)
- **Üretim tesisi / ruhsatlı işletme seçeneği eklendi.** Md.49 bu ürünleri başvuru zorunluluğundan açıkça hariç tutar; uygulamada karşılığı yoktu. Sonuç: **Ek-18 gerekmez** + Ek-9 zinciri (Md.68 üç nüsha, ikincisi alıcıda), ambalajda Türkçe/Latince ad ve üretici kodu (Md.69), Ek-9'un nakliye belgesi yerine geçmesi (Md.72), hayvan satış yerlerinde satış (Md.70).
- **Av turizmi ürünleri ayrı rapora alındı.** Md.56: "Trofe Belirleme ve Bulundurma ile İhraç Sertifikası, bulundurma belgesi yerine geçeceğinden ayrıca bulundurma belgesi düzenlenmez." Önceden başvuru akışına yönlendiriliyordu.
- **Koruma altı tür trofesi hükmü düzeltildi.** Önceki metin "koruma altı olması yolu KAPATMAZ, sadece ek belge gerektirir" diyordu. Md.63 ve Md.66 aksini söyler: koruma altındaki ve avı yasak türlerin tahnit/trofelerinin ev ve iş yerinde bulundurulması, alımı ve satımı — hangi amaçla olursa olsun — yasaktır; tek istisna av turizmi kapsamında avlananlardır.

## [1.8.0] — 2026-07
### Eklendi
- **Petshop / hayvan satış yeri kaynak dalı.** Vatandaş genellikle ithalatçıdan değil petshoptan alır; bu yol sihirbazda yoktu. Ek-4 ruhsatlı işletme → Ek-15 satış belgesi → Ek-18 zinciri kuruldu (Md.59-60). Ruhsatsız işletmeden alım için ayrı rapor: Md.60 son fıkra uyarınca ticaret yapılamaz, alıcıya Ek-18 düzenlenmez, Md.85 işler, işletme hakkında denetim başlatılır.
### Düzeltildi
- Sihirbaz adım sayacı 7/6 gösteriyordu (tür adımı eklendiğinde toplam güncellenmemişti).

## [1.7.1] — 2026-07
### Düzeltildi
- **Tür veritabanı arama çubuğu kayboluyordu.** Kutu `static` konumdaydı ve sayfa ~43.000 px uzunluğundaydı. Çubuk yapışkan yapıldı (header yüksekliği çalışma anında ölçülür), sayfanın en üstüne alındı, büyüteç ikonu ve sonuç sayacı eklendi.

## [1.7.0] — 2026-07
### Düzeltildi
- **GM 16.07.2026 yazısıyla hükme bağlanan 54 tür sihirbazda görünmüyordu.** 50 tür (iguana, bukalemun, geko, tosbağa) "hobi bulundurmasında sakınca yoktur" görüşüne sahipken sihirbaz "tanımsız, GM'ye sor" diyordu; 4 Varanus türü ise yasak olmasına rağmen tanımsız görünüyordu.
- **Amfibi ve deniz memelileri** (Su Ürünleri GM yetkisi) sihirbazda tanımsız çıkıyordu.
- **Evcil ırklar** (muhabbet kuşu, kanarya, zebra ispinozu) sihirbazda "değerlendirilebilir" görünüyordu; artık "Ek-18 gerekmez" diyor.
- Bu hükümler `metaHukmu()` ortak fonksiyonuna taşındı.
### Eklendi
- **`YASAK_TAX`** — uygulamanın kendi yasak tür kategorilerinin (timsah, primat, boa/piton, tarantula, istilacılar) taksonomik karşılığı. Küratörlü kartı olmayan türlerde de kesin hüküm verilir.
- Sihirbaz tür araması `CITES_GRUP` anahtarlarını da tarar (timsah, akrep, kertenkele… artık sonuç verir).

## [1.6.0] — 2026-07
### Düzeltildi
- **Tür araması ile Ek-18 sihirbazı farklı hüküm veriyordu.** Statü türetme mantığı arama fonksiyonunun içine gömülüydü; sihirbaz erişemiyordu. Örnek: *Python regius* aramada "hobi amaçlı bulundurulamaz", sihirbazda "gruplara girmiyor, GM'ye sor" çıkıyordu. Mantık `kartDurumu()` ortak fonksiyonuna çıkarıldı; 161 kartta denetlendi, uyuşmazlık sıfıra indi.

## [1.5.2] — 2026-07
### Düzeltildi
- **Puhu ve Kukumav kartları** hâlâ "2023/8 Yönerge kapsamında izne tabidir" diyordu. Yönerge Md.3 tanımına göre baykuşgiller kapsam dışıdır. Gerçek yırtıcı kartları (Şahin, Kaya Kartalı, Bozkır Kartalı) etkilenmedi.

## [1.5.1] — 2026-07
### Değişti
- **Kart yoğunluğu azaltıldı.** Md.85 ve Ek-18 her kartta iki kez geçiyordu; belge yolu tek satıra indirildi, "Not 1" karttan çıkarılıp bölüm altına bir kez alındı. Kuğu/flamingo 514→389 px, Caretta 655→514 px.

## [1.5.0] — 2026-07
### Eklendi
- **2023/8 Yırtıcı Kuşlar Yönergesi tam metni işlendi** (26.05.2023 tarihli onaylı nüsha; kurum içi düzenleme, kamuya açık değil).
  - **Kapsam kesinleşti (Md.3/e):** yırtıcı kuş = yalnız **Accipitridae, Falconidae, Pandionidae**. Baykuşgiller kapsam dışıdır — önceki Strigidae/Tytonidae/Cathartidae/Sagittariidae eşlemesi hatalıydı.
  - **Zorunlu belgeler:** eğitim sertifikası (Md.8), Yırtıcı Kuş Kimlik Belgesi (Md.9), bulundurma izni = Ek-18 (Md.3/a).
  - **Eğitim (Md.6-7):** il şube müdürlüğü veya asgari 5 yıl faaliyetli dernek; 4 saat teorik + 4 saat pratik; sınavda 100 üzerinden 70 ve üstü başarılı.
  - **Barınak (Md.5):** açık alan asgari 3 m yükseklik, tek hayvana 40 m², ilave her yırtıcıya +8 m², uçuş için 4×10 m; kapalı alan 2 m yükseklik, hayvan başına 2 m².
  - **Barındırma (Md.4):** kilitli kapı, ayrı karantina alanı, %70-80 gölgelik, 25 °C üstünde gölge erişimi.
  - **Atmaca (Md.11):** ayrıca Geleneksel Atmacacılık Esas ve Usulleri — Usta Atmacacılık Belgesi.

## [1.4.0 – 1.4.2] — 2026-07
### Eklendi
- **Ek-18 sihirbazı tür-önce girişe geçti.** Önceki ilk soru "İthal — CITES türü mü, CITES dışı mı?" idi; kullanıcının cevabı zaten bilmesini gerektiriyordu. Artık tür adı yazılır; uygulama CITES durumunu, yaban hayvanı kaydını, izin grubunu ve Md.45 sayı sınırını kendisi belirler. Geriye tek soru kalır: hayvan nereden geldi.
- Kaynak adımı türe göre uyarlanır (CITES türünde CITES belgesi, değilse Ek-16/A).
- **`r_kaynak_yok`** raporu: doğadan alınan/kaynağı belgelenemeyen birey → Ek-18 düzenlenmez, Md.85. "Belge eksik" ile "yasal kaynak yok" ayrımı netleşti.

## [1.3.0] — 2026-07
### Düzeltildi
- **Türkçe grup araması tek taraflı çalışıyordu.** "kuğu" yerli kuğuları buluyor ama CITES'teki *Cygnus melancoryphus* ve *Coscoroba coscoroba*'yı bulamıyordu. Arama `BULUNDURMA_TAX` grup adlarına bağlandı, cins düzeyinde eşleşiyor. Kuğu 3→5, flamingo 2→6, saka 7→16, papağan 94→119.

## [1.2.0] — 2026-07
### Eklendi
- **`BULUNDURMA_TAX`** — GM 04.05.2026 listesindeki 25 iznin taksonomik karşılığı.
### Düzeltildi
- **1.044 tür hatalı biçimde "bulundurma statüsü TANIMLI DEĞİL" gösteriyordu.** Uyarı, türün grubunun izin listesinde olup olmadığına bakmadan yalnız "küratörlü kartı yok" diye tetikleniyordu. Statü artık katmanlı: grup + CITES Ek-I uyarısı (Md.60, Md.47) + yerli tür uyarısı.

## [1.1.0] — 2026-07
### Eklendi
- **Türkiye Yaban Hayvanları Listesi — 785 tür** (R.G. 10.08.2022/31919): 154 memeli, 490 kuş, 141 sürüngen. Sabitler `YHL_DB`, `YHL_ACK`, `YHL_BERN`, `YHL_TARIH`.
- **670 yerli tür ilk kez aranabilir oldu** — tilki, porsuk, sansar, yaban tavşanı, kuğular, yaban kazları, bıldırcın, çilkeklik dâhil.
- **Birleşik kart:** CITES ve YHL'de birlikte yer alan 110 türde her iki statü tek kartta (ör. Kelaynak: CITES Ek-I + Bern EK-II + tam koruma).
- Karar dipnotları (I–VIII) açık metne çevrildi; her kayıtta "avlanma izni bulundurma izni anlamına gelmez" uyarısı.
### Düzeltildi
- Türkçe ad araması CITES+YHL ortak türlerinde çalışmıyordu ("kelaynak" sonuç vermiyordu).
- Tür sayacı yalnız CITES'i sayıyordu → 4.888 (tekilleştirilmiş toplam).

## [1.0.0] — 2026-07
İlk resmî sürüm (geliştirme sayacındaki v94 ile aynı yapı).
### Eklendi
- **MADDE_DB — 5199 maddeleri:** `k5199_10` (Md.10 – Hayvanların Ticareti), `k5199_ek2` (Ek Md.2 – Sirk ve Yunus Parkı Yasağı); link sabiti `_MEVZ_5199`.
- `linkifyMevzuat` 5199 referanslarını ve "Ek Md.N" formatını tanır.

---

### 1.0.0 öncesi (geliştirme sayacı)

**v93** — Sirk soruları sınavdan kaldırıldı (5199 Ek Md.2: yeni sirk yasak, mevcutlar 10 yılda tasfiye; kanun hükmü yönetmeliğin üzerindedir). 100→98 soru. Lama/alpaka evcil-hariç. Tüm madde numaraları Yönetmelik tam metniyle doğrulandı.

**v92** — Dinamik sınav rozeti. **v91** — Sınav 50→100. **v90** — Md.54 sözlüğe; şık karıştırma. **v89** — Ticari sergileme düzeltmesi (Md.54). **v88** — Sınav/Eğitim modu. **v85–v87** — İnteraktif mevzuat (`MADDE_DB`, `linkifyMevzuat`). **v84** — El koyma butonu. **v80–v83** — Modal linkleri, pinch-zoom. **v78–v79** — Foto arama, tür rozeti.

**Pre-v78** — Çekirdek motorlar: CITES veritabanı, tür teşhis kartları, denetim karar ağacı, Ek-18 sihirbazı, el koyma prosedürü, GPS'li tutanak.
