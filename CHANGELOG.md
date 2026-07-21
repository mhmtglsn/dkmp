# Değişiklik Günlüğü (CHANGELOG)

DKMP Saha Denetim Asistanı — tek dosyalık HTML uygulaması.
Biçim: [Keep a Changelog](https://keepachangelog.com/tr/) esaslı. Sürümleme uygulama içi `vNN` damgasıyla eşleşir.

Tüm hukuki içerik, alan uzmanı (DKMP veteriner hekimi) onayından geçmiştir. Mevzuat değiştikçe ilgili maddeler ve sorular güncellenir.

---

## [v94] — 2026-07
### Eklendi
- **MADDE_DB — 5199 sayılı Kanun maddeleri:** `k5199_10` (Madde 10 – Hayvanların Ticareti) ve `k5199_ek2` (Ek Madde 2 – Sirk ve Yunus Parkı Yasağı). Her ikisi de kanunun tam metninden birebir doğrulandı. Yeni link sabiti `_MEVZ_5199`.
- **`linkifyMevzuat` genişletildi:** artık "5199" referanslarını (`k5199_`) ve **"Ek Md.N"** madde formatını tanıyıp tıklanabilir çipe çeviriyor. Mevcut `yon_`/`k4915_` çözümlemesi ve yanlış-pozitif önlemleri korundu.
### Etki
- Denetim motorundaki "5199 Ek Md.2" notu ve sınavdaki "5199 Md.10" referansları artık canlı mevzuat kaynağına bağlı.

## [v93] — 2026-07
### Değişti / Düzeltildi
- **Sirk soruları kaldırıldı** (5199 Ek Md.2 gereği yeni sirk yasak, mevcutlar 10 yılda tasfiye — kanun hükmü yönetmeliğin üzerinde): teşhir-fazlası satış ve "sirk el konulan hayvan alamaz" soruları çıkarıldı; kaçış-sorumluluğu sorusu sirk çerçevesinden çıkarılıp **Md.47** temelli genel forma dönüştürüldü; bir senaryo açıklamasındaki sirk cümlesi sadeleştirildi. Soru sayısı 100 → **98** (dinamik rozet otomatik güncellenir).
- **Lama/alpaka sorusu** uygulamanın kendi bulundurma listesiyle uyumlu hâle getirildi: evcil Lama glama ve Vicugna pacos "evcil — hariç" (Ren Geyiği örüntüsü).
- **Madde numaraları tam Bulundurma Yönetmeliği metniyle doğrulandı.** Md.47'nin hibe/satış limitleri (5/50) ve Kategori-A ithalat donanım görüşünü de kapsadığı teyit edildi; ilgili sorulara doğru atıf korundu. Md.53 (koleksiyonculuk/Ek-14), Md.76 (ithalat/Ek-16A), Md.9 (üretim/Ek-3), Md.3 (Bilimsel Merci) atıfları doğrulandı.

## [v92] — 2026
- Ana ekran sınav rozeti **dinamik** (`sinavCountBadge` ← `SINAV.length`).

## [v91] — 2026
- Sınav **50 → 100 soru** (ayırt edici çeldiricilerle).

## [v90] — 2026
- Md.54 (ticari sergileme yasağı) madde sözlüğüne eklendi (tam metin teyidiyle).
- Sirk içeriği ilk kez gözden geçirildi (5199 Ek Md.2 yasağı).
- Sınav şıkları çalışma anında karıştırılmaya başlandı (konum önyargısı çözümü).

## [v89] — 2026
- **Kritik hukuki düzeltme:** Bulundurma (Ek-18) hayvanının ticari sergilenmesi konusundaki hatalı "GM onayı ile olur" ifadesi kaldırıldı; doğrusu Md.54 — yasak → belge iptali + el koyma.

## [v88] — 2026
- **Sınav / Eğitim modu** eklendi (50 soru, 7 kategori, anında geri bildirim + açıklama + skor).

## [v85–v87] — 2026
- **İnteraktif mevzuat sistemi:** `MADDE_DB` madde sözlüğü, madde-modal, `linkifyMevzuat` ile metin içi "Md.XX" çipleri. Dayanak kutusu taşma düzeltmesi.

## [v84] — 2026
- El koyma sonuçlarına "El Koyma Prosedürü (Md.85)" butonu.

## [v80–v83] — 2026
- Denetim ağacına bulundurma listesi / tür veritabanı / örnek CITES belgesi modal linkleri; belge okuma için pinch-zoom (viewport toggle).

## [v78–v79] — 2026
- Foto arama mobil dış-link düzeltmesi; ana ekran tür kartı rozeti.

---

### Daha eski (pre-v78)
Çekirdek motorlar ve veri yapıları: CITES veritabanı (~4.213 tür), tür teşhis kartları (161), denetim karar ağacı, Ek-18 başvuru sihirbazı, el koyma prosedürü (idari/adli ayrımı), GPS'li tutanak üretimi. Ayrıntı için HANDOVER.md §13.
