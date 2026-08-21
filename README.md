Fentropi Mic — fentropi.com (şimdilik yalnızca mikrofon)

Bu klasör GitHub Pages ile yayınlanacak statik sitedir.
GitHub Desktop ile repo oluşturup push etmen yeterli.

## 1) GitHub Desktop

1. GitHub Desktop → File → Add local repository
2. Klasör: `fentropi-site` (yoksa Create repository burada)
3. Repo adı önerisi: `fentropi-site` (public)
4. Publish repository (GitHub.com hesabın)

## 2) GitHub Pages

1. github.com → repo → Settings → Pages
2. Source: Deploy from a branch
3. Branch: `main` / folder `/ (root)` → Save
4. Custom domain: `fentropi.com` → Save
5. “Enforce HTTPS” işaretle (DNS oturunca)

## 3) Domain DNS (alan adı panelin)

Aşağıdakileri ekle (GitHub Pages):

| Tip | Host/Name | Değer | TTL |
|-----|-----------|--------|-----|
| A | @ | 185.199.108.153 | 3600 |
| A | @ | 185.199.109.153 | 3600 |
| A | @ | 185.199.110.153 | 3600 |
| A | @ | 185.199.111.153 | 3600 |
| CNAME | www | SENIN_GITHUB_KULLANICI.github.io | 3600 |

`SENIN_GITHUB_KULLANICI` yerine GitHub kullanıcı adını yaz.

DNS yayılması 5 dk – birkaç saat sürebilir.

## 4) Sabit mikrofon adresi (isteğe bağlı, önerilir): mic.fentropi.com

Rastgele `*.trycloudflare.com` yerine her zaman aynı adres için Cloudflare Tunnel:

1. https://dash.cloudflare.com → siteye fentropi.com ekle (nameserver’ları Cloudflare’e taşıman istenebilir)
2. Zero Trust → Networks → Tunnels → Create
3. Public hostname: `mic` → `http://127.0.0.1:8765`
4. PC’de `cloudflared tunnel run` (veya `fentropi-mic/start-named-tunnel.ps1`)

Detay: `../fentropi-mic/CLOUDFLARE.md`

## Ne işe yarar?

| Adres | Rol |
|-------|-----|
| https://fentropi.com | Tanıtım + kullanım (bu site) |
| https://fentropi.com/mic/ | Telefondan kısa rehber |
| https://mic.fentropi.com | Senin PC alıcın (sunucu açıkken, named tunnel) |
