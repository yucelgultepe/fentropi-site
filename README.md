# fentropi.com — Fentropi marka sitesi

Bu depo, GitHub Pages ile yayınlanacak statik sitedir.

## Mevcut durum

- **Ana sayfa (`index.html`)** bilerek boştur — yalnızca "Fentropi" yazar.
  (Site sahibinin isteği: içerik hazır olmadan yayında bir şey görünmesin.)
- **Tüm içerik taslakları `_drafts/` klasöründedir.** `_` ile başlayan
  klasörler GitHub Pages tarafından yayınlanmaz; orada güvenle çalışılır.
- **`/mic/`** rehber sayfası yerinde duruyor.

Ayrıntılar: [`_drafts/README.md`](_drafts/README.md) ve
[`_drafts/site-plani.md`](_drafts/site-plani.md)

## Yayına alma (hazır olunca)

### 1) GitHub Pages

1. github.com → repo → Settings → Pages
2. Source: Deploy from a branch
3. Branch: `main` / folder `/ (root)` → Save
4. Custom domain: `fentropi.com` → Save (CNAME dosyası depoda zaten var)
5. DNS oturunca "Enforce HTTPS" işaretle

### 2) GoDaddy DNS

GoDaddy → fentropi.com → DNS yönetimi:

| Tip | Host/Name | Değer | TTL |
|-----|-----------|--------|-----|
| A | @ | 185.199.108.153 | 3600 |
| A | @ | 185.199.109.153 | 3600 |
| A | @ | 185.199.110.153 | 3600 |
| A | @ | 185.199.111.153 | 3600 |
| CNAME | www | yucelgultepe.github.io | 3600 |

DNS yayılması 5 dk – birkaç saat sürebilir.

### 3) Yayın öncesi son adımlar

1. Yayınlanacak taslakları `_drafts/` içinden köke taşı.
2. Ana sayfadaki `<meta name="robots" content="noindex">` satırını kaldır.

## Adresler (yayın sonrası)

| Adres | Rol |
|-------|-----|
| https://fentropi.com | Ana sayfa (marka çatısı) |
| https://fentropi.com/uygulama | Android uygulaması tanıtımı |
| https://fentropi.com/muzik | Müzik çalışmaları |
| https://fentropi.com/makaleler | Makaleler |
| https://fentropi.com/mic/ | Telefondan kısa rehber (mevcut) |
| https://fentropi.com/gizlilik | Gizlilik / KVKK |
| https://mic.fentropi.com | PC alıcısı (Cloudflare Tunnel, sunucu açıkken) |
