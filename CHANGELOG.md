# Sürüm Geçmişi — DKMP Saha Denetim Asistanı

Bu dosya uygulamanın gelişimini belgeler. Sürüm damgası uygulama menüsünün altında görünür.

## v79 — Ana ekran tür sayacı
- "Tür Veritabanı" kartının alt yazısı "4.213 tür · 161 detaylı kart" yapıldı; toplam aranabilir tür sayısı öne çıkarılarak uygulamanın yalnızca 161 türle sınırlı olduğu izlenimi giderildi. Sayı `TUR_DB` ve `CITES_DB` üzerinden dinamik üretilir.

## v78 — Görsel arama butonu düzeltmesi
- Tür kartlarındaki fotoğraf (Google Görseller) butonu; mobilde "harici bağlantı" uyarısına yol açan `window.open(..., 'noopener')` yerine gerçek bir bağlantı tıklamasıyla (`<a target="_blank">`) açılacak şekilde değiştirildi. Bağlantı artık doğrudan, uyarısız açılıyor.

## v77 — Arama sayacı ve fotoğraf ikonu
- Tür veritabanı arama sayacı "161 detaylı kart · toplam 4.213 tür" biçiminde düzeltildi; CITES sorgu sonuç satırlarına, türü Google Görseller'de aratan fotoğraf ikonu eklendi.

## v76 — CITES kapsam dışı türler ve filtre
- 27 CITES kapsam dışı tür, "Kapsam Dışı" rozetiyle sorgu katmanına eklendi; "CITES Dışı" filtresi, arama kutusuna temizleme (X) butonu ve bir yazım düzeltmesi eklendi.

## v75 — Çelişki düzeltmeleri
- Özel not taşıyan türlerde çelişkili "tanımlı değil, GM'ye sor" uyarısı gizlendi; kartında güncel GM notu bulunan türlerde eski mükerrer not satırı gizlendi.

## v74 — Hobi bulundurma yeşil notları (GM görüşü 16.07.2026)
- GM görüşü doğrultusunda 52 sürüngen türüne "hobi amaçlı bulundurulabilir" bilgi notu ile Türkçe/İngilizce ad eklendi; listede yer almayan türlerde mutlaka GM'ye danışılması gerektiği vurgulandı.

## v73 — Çevrimdışı çalışma vaadinin kaldırılması
- Service Worker (blob) ile güvenilir çevrimdışı önbellekleme mümkün olmadığından, çalışmayan mekanizma ve "çevrimdışı çalışır" ibareleri sürümden çıkarıldı. Ana ekrana ekleme (ikon + manifest) korundu.

## v71–v72 — Depo dosyaları ve footer düzenlemesi
- Depo için LICENSE, CHANGELOG ve README dosyaları hazırlandı; footer telif satırından geliştirici adı kaldırıldı (ad "Hakkında" bölümünde ve LICENSE'ta korundu).

## v70 — Hakkında ve geliştirici beyanı
- "Hakkında" bölümü, footer telif satırı ve sorumluluk reddi eklendi.

## v69 — Arama düzeltmesi
- İki kelimeli latince aramada tam eşleşen türün öne çıkmaması hatası giderildi (ad eşleşmeleri önceliklendirildi).

## v68 — Ağaç varanları (GM görüşü 16.07.2026)
- Varanus prasinus / macraei / beccarii / reisingeri için "hobi bulundurulamaz; yalnız hayvanat bahçesi ve yeniden ihracat ithalatı" kuralı tür veritabanına ve Ek-18 akışına işlendi.

## v67 — El koyma sonrası mülkiyet ve muhasebe zinciri
- İdari (4915) / adli (5607) yol ayrımı, emanet kaydı, iz bedel, demirbaş kodu (255.06.12), 3 aylık raporlama. Mevcut canlı hayvan el koyma zinciriyle çakışmayacak biçimde eklendi.

## v66 — Vaka bankası genişletme
- Petshop üzerinden hobi bireyinin ticari zincire sokulması (izlenebilirlik kırılması) vakası eklendi.

## v65 — Ürün bulundurma Ek-18
- Trofe / tahnit / deri gibi hayvansal ürünler için Ek-18 akışı (canlı hayvandan ayrı çatal): amaç, adet eşiği (29/30), yasal kaynak kontrolü, koleksiyoncu (Ek-14) yönlendirmesi.

## v63–v64 — Ek-18 ve denetim ağacı buton düzeltmesi
- onclick'e gömülen etiketteki apostrof (ör. "Md. 82'ye") metni erken kapatıp butonu bozuyordu; etiket artık veriden indeksle okunuyor. Düzeltme hem Ek-18 sihirbazına hem denetim karar ağacına uygulandı.

## v61 — Belge ücretleri (2026 tarifesi)
- Ek-3, Ek-6, Ek-9 ücretleri güncellendi; "2026 tarifesi" etiketi ve kaynak notu eklendi.

## v59 — Ek-18 başvuru rehberi
- Bulundurma belgesi başvurusu için adım adım sihirbaz (denetim akışından ayrı, 5 kaynak dallanması).

## v50–v58 — Görsel sistem ve arayüz sadeleştirme
- Tek tasarım dili: gradyan/gölge/tipografi ölçeği sadeleştirildi; ikon seti tekleştirildi; alt navigasyon ve başlık düzeni yenilendi.

> **Not:** v49'a kadarki girdiler, o oturumların doğrudan kayıtlarından (komut çıktıları, doğrulama testleri) derlenmiştir — yüksek güvenilirlik. v32 öncesi tek bir özet girdide toplanmıştır; sürüm sürüm doğrulanmamıştır.

## v49 — Kart derinliği ve tipografik hiyerarşi
- Ana sayfa kartları çerçeveden katmanlı yumuşak gölgeye geçirildi; ikonlar tonlu kap içine alındı (42px, açık yeşil/mor zemin).
- Başlık/alt-metin ağırlık farkı geri getirildi (14.5px/600 – 11px/400); global gölge ve çizgi değişkenleri (`--shadow`, `--line`) tür kartları dahil tüm yüzeylere yayıldı.

## v48 — Tür ikonu düzeltmesi
- "Türler" simgesi kuş silüetinden pençe izine değiştirildi — kuş ikonu bacaksız/asılı duruyordu; ayrıca kapsam yalnızca kuş değil (sürüngen/memeli/eklem bacaklı da var).

## v47 — İkon ve tipografi sadeleştirmesi
- İkon seti Phosphor Light'ta tekleştirildi (dolu geometri, 256×256 ızgara, ~7,8 KB gömülü sprite); gradyanlı renkli kart kutuları kaldırıldı, tek vurgu rengi (Yapay Zekâ – mor) bırakıldı.
- Arayüz tipografisi 700/800 ağırlıklarından 500/600'e indirildi (yazdırma şablonları hariç).

## v46 — Veri kurtarma
- v45'teki bir düzenlemede kullanılan regex blok sınırını yanlış hesaplayıp `SINIRLAR`, `BULUNDURMA_LISTESI` ve `BULUNDURMA_NOTLAR` sabitlerini silmişti; eski yedekten birebir doğrulanarak geri yüklendi. Kod doğrulama rutinine "tüm veri sabitlerinin tek geçişte var olduğunu doğrula" adımı ve düzenleme öncesi zorunlu yedekleme kuralı eklendi.

## v44 — Arama ve belge başlığı iyileştirmeleri
- Tür arama motoruna taksonomi tabanlı grup eşleştirmesi eklendi (ör. "timsah" → Crocodylia takımındaki tüm CITES kayıtları; önceki halde yalnız tam Latince ad aranabiliyordu).
- Belge Zinciri başlığı "Vatandaşa Ulaşan İki Yol" → "Bir Hayvan Vatandaşa Nasıl Yasal Ulaşır?" yapıldı; Ek-18 kartındaki tekrarlı ücret satırı kaldırıldı.

## v43 — Filtre arayüzü sadeleştirmesi
- 20 taksonomik takım çipi, sınıflara göre gruplanmış (Kuşlar / Memeliler / Sürüngenler / Eklem Bacaklılar / Yetki Dışı) tek bir açılır listeye indirildi.

## v42 — Sülük ve yılan balığı
- Tıbbi sülük (*Hirudo verbana/medicinalis*) ve Avrupa yılan balığı (*Anguilla anguilla*) kartları eklendi — ikisi de CITES ihracat kotalı Türkiye türleri, ikisi de 🚫 Yetki Dışı (Balıkçılık ve Su Ürünleri GM).

## v41 — Zehirli tür yeniden sınıflandırması
- Tarantula (*Brachypelma*, *Poecilotheria*) ve İmparator Akrep, GM Bulundurma Listesi Not 1 ("zehirli türlerin hobi bulundurması yasaktır") kapsamında ⚠️ Belirsiz'den ⛔ Yasak'a çekildi; zehirsiz Apollo Kelebeği Belirsiz'de bırakıldı.

## v40 — Eklem bacaklı katmanı
- 117 eklem bacaklı (örümcek, akrep, kelebek) CITES sorgu katmanına eklendi; Apollo Kelebeği (Türkiye'nin tek yerli CITES eklem bacaklısı) küratörlü kart olarak eklendi.

## v39 — Amfibi katmanı ve arama düzeltmeleri
- 384 amfibi (aksolot dahil) 🚫 Yetki Dışı işaretiyle CITES katmanına eklendi.
- "İ" harfiyle başlayan aramaların hiç sonuç vermediği hata giderildi (Türkçe büyük İ'nin JS'te normalize sorunu); Türkçe karaktersiz arama ve alaka sıralaması eklendi.

## v38 — Yönetim mercii ve deniz memelisi yetkisi
- Mevzuat ekranına "Yönetim Mercii — Kim Neye Bakar?" tablosu eklendi (4 Genel Müdürlük, DKMP vurgulu); deniz memelileri (109 kayıt) yetki dışı işaretlendi, deniz kaplumbağalarının sürüngen olarak DKMP yetkisinde kaldığı netleştirildi.

## v36–v37 — CITES sorgu katmanı ve yeniden doğrulama
- 3.685 kayıtlık resmî CITES tür listesi (kuş/sürüngen/memeli) gömülü sorgu katmanı olarak eklendi; küratörlü kart yoksa "GM görüşü sorulmalı" uyarısıyla ayrı gösteriliyor.
- 153 küratörlü türün CITES eki resmî listeye karşı tek tek doğrulandı; popülasyona göre bölünen 4 türe (kurt/ayı/aslan/karakulak) menşe ülke uyarısı eklendi.

## v34–v35 — Hata düzeltmesi ve tür genişletmesi
- Resmî CITES Ekleri metniyle karşılaştırılarak 10 hatalı/eski kayıt düzeltildi; Ek-III rozet/filtre desteği eklendi (önceki kodda "Ek-III" dizgesi "Ek-II" ile başladığından yanlış sınıflanıyordu).
- 18 yeni küratörlü kart (135→153): büyük etçiller, yaban keçisi, kaplumbağalar, çakırkuşu, yerli bukalemun, çöl varanı.

## v33 — Gömülü emoji ikon seti
- Karakter tabanlı emojiler yerine Google Noto emoji'nin resmî SVG dosyaları gömüldü (aynı görünüm, cihazdan bağımsız keskinlik). Elle çizilmiş çizgi ikon denemesi (v32) bu adımda terk edildi.

## v32 ve öncesi — Çekirdek ve erken tasarım (özet)
- Tek dosyalık mimari; CITES tür veritabanının ilk hali, akıllı denetim karar ağacı, tutanak oluşturma, belge zinciri, mevzuat ve vaka bankası bu dönemde kuruldu.
- Organik dalga arka planı eklendi; ilk ikon denemeleri (karakter emoji) bu döneme ait.
