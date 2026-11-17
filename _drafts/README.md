# Taslaklar klasörü (`_drafts/`)

Bu klasördeki sayfalar **yayınlanmaz.** GitHub Pages, adı `_` (alt çizgi) ile
başlayan klasörleri siteye dahil etmez. Dosyalar burada güvenle durur, üzerinde
istediğimiz kadar çalışırız; kimse görmez.

## Nasıl çalışır?

1. Taslak sayfalar burada hazırlanır ve güncellenir.
2. Bir sayfa yayınlanmaya hazır olunca, `_drafts/` içinden **köke taşınır**
   (örn. `_drafts/uygulama.html` → `uygulama/index.html` veya `uygulama.html`).
3. Ana sayfa (`/index.html`) şu an bilerek boştur — sadece "Fentropi" yazar.
   Yayına geçerken `_drafts/ana-sayfa.html` köke taşınır ve içindeki
   `noindex` etiketi kaldırılır.

## Mevcut taslaklar

| Dosya | Ne olacak? |
|-------|-----------|
| `ana-sayfa.html` | Geleceğin ana sayfası — marka çatısı: uygulama, müzik, makaleler |
| `uygulama.html` | Fentropi Android uygulaması tanıtım sayfası (Play Store) |
| `muzik.html` | Müzik çalışmaları sayfası |
| `makaleler.html` | Makaleler/yazılar sayfası |
| `gizlilik.html` | Gizlilik politikası / KVKK (Play Store için zaten gerekli) |
| `mic-landing.html` | Eski Mic tanıtım sayfasının arşiv kopyası (yedek) |
| `site-plani.md` | Site planı ve senden gereken malzemeler listesi |

Taslaklardaki `TODO:` işaretleri, senden bilgi/onay gereken yerleri gösterir.

## Yayınlama kontrol listesi (hazır olunca, acele yok)

1. GoDaddy DNS kayıtları (ana README'deki tablo) eklenir.
2. GitHub → repo → Settings → Pages → Source: `main` / root seçilir.
3. Custom domain: `fentropi.com` yazılır, kaydedilir (CNAME dosyası zaten var).
4. DNS oturunca "Enforce HTTPS" açılır.
5. Ana sayfadaki `noindex` etiketi kaldırılır.
