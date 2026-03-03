──(root㉿peace)-[/home/peace/Desktop/Recon101]
└─# curl -sk \
-H "Host: sinistres.saarassurancesci.com" \
https://5.189.160.190/robots.txt
User-agent: *
Disallow:
                                                                               
┌──(root㉿peace)-[/home/peace/Desktop/Recon101]
└─# curl -sk \
-H "Host: sinistres.saarassurancesci.com" \
https://5.189.160.190/manifest.json      
{
  "name": "SAARCISinistres - Gestion des sinistres",
  "short_name": "SAARCISinistres",
  "description": "Application de gestion des sinistres pour SAAR Assurances Côte d'Ivoire. Déclarez et suivez vos sinistres en ligne.",
  "start_url": "/",
  "scope": "/",
  "display": "standalone",
  "orientation": "portrait-primary",
  "background_color": "#ffffff",
  "theme_color": "#dc2626",
  "categories": ["business", "finance", "productivity"],
  "lang": "fr",
  "dir": "ltr",
  "icons": [
    { "src": "/icons/icon-16x16.png", "sizes": "16x16", "type": "image/png" },
    { "src": "/icons/icon-32x32.png", "sizes": "32x32", "type": "image/png" },
    { "src": "/icons/icon-48x48.png", "sizes": "48x48", "type": "image/png" },
    { "src": "/icons/icon-72x72.png", "sizes": "72x72", "type": "image/png" },
    { "src": "/icons/icon-96x96.png", "sizes": "96x96", "type": "image/png" },
    { "src": "/icons/icon-128x128.png", "sizes": "128x128", "type": "image/png" },
    { "src": "/icons/icon-144x144.png", "sizes": "144x144", "type": "image/png" },
    { "src": "/icons/icon-152x152.png", "sizes": "152x152", "type": "image/png" },
    { "src": "/icons/icon-192x192.png", "sizes": "192x192", "type": "image/png", "purpose": "any maskable" },
    { "src": "/icons/icon-384x384.png", "sizes": "384x384", "type": "image/png" },
    { "src": "/icons/icon-512x512.png", "sizes": "512x512", "type": "image/png", "purpose": "any maskable" }
  ],
  "shortcuts": [
    {
      "name": "Nouveau sinistre",
      "short_name": "Déclarer",
      "description": "Déclarer un nouveau sinistre",
      "url": "/declaration",
      "icons": [ { "src": "/icons/icon-96x96.png", "sizes": "96x96", "type": "image/png" } ]
    },
    {
      "name": "Mes sinistres",
      "short_name": "Sinistres",
      "description": "Voir mes sinistres",
      "url": "/assures/dashboard",
      "icons": [ { "src": "/icons/icon-96x96.png", "sizes": "96x96", "type": "image/png" } ]
    }
  ]
}                                                                                
┌──(root㉿peace)-[/home/peace/Desktop/Recon101]
└─# curl -sk -I \
-H "Host: sinistres.saarassurancesci.com" \
https://5.189.160.190/storage/
HTTP/2 403 
server: nginx/1.24.0 (Ubuntu)
date: Tue, 03 Mar 2026 12:25:34 GMT
content-type: text/html
content-length: 162
x-frame-options: SAMEORIGIN
x-xss-protection: 1; mode=block
x-content-type-options: nosniff
referrer-policy: strict-origin-when-cross-origin

                                                                               
┌──(root㉿peace)-[/home/peace/Desktop/Recon101]
└─# curl -sk -I \
-H "Host: sinistres.saarassurancesci.com" \
https://5.189.160.190/password/forgot    
HTTP/2 200 
server: nginx/1.24.0 (Ubuntu)
content-type: text/html; charset=utf-8
vary: Accept-Encoding
cache-control: no-cache, private
date: Tue, 03 Mar 2026 12:25:59 GMT
set-cookie: XSRF-TOKEN=eyJpdiI6Im5mZ3cyWVE4L2xWZm9pTE8rQmtFOEE9PSIsInZhbHVlIjoibVhLbWJBSGp1SDM0RmtWOU5JcTQ1V2dJNk40VCsyaGJMN3Rwb0ROUEFWQTl4UVRzMHMyT2swYU5MSGM4djBYbHJ2ZHZYYWVIUUU3bUtKaWN4QU1zNUcrQjJTdEVQRkkvbnVzd1JJbkRTZUY4TW44U01CY0F3aWJxTjlla3hYbGoiLCJtYWMiOiI0NmY0MTlmOWIxOWNkNzdmMmMxMzk3MTc5YjNlYzhiMTUzNGIxNzYxMTQ0NzU0YTQ0Nzk0ODllNzAzZDM1MGU1IiwidGFnIjoiIn0%3D; expires=Tue, 03 Mar 2026 21:05:59 GMT; Max-Age=31200; path=/; secure; samesite=lax
set-cookie: saar_sinistre_session=eyJpdiI6ImEwZzdraXd4cTZxT0RWVHlZSVFmalE9PSIsInZhbHVlIjoidCtCSWhwZWJ5MEFTN0JzWTZqNTJJN3phNC83L3psZ3J2cWxMZHR6MENGNFVkK05TUEtPQi92Mkc1VWhnUCtJZnVmSEwwaU5TVExlT3EwaE4wdklyblFtVEdmWk9ZODk0UzJqU00xekw2Vnd5UnFhbEVMUnRoYmtzM0pWZERqaUMiLCJtYWMiOiIxZTNiZGQyNTk1NWY2YjE3ZGMzM2ZlNDA3ZWM2MzIxNmNiMjYxOTU1ZGNkODY1MTAyNjNiYjg5MzgwMzUxYjU5IiwidGFnIjoiIn0%3D; expires=Tue, 03 Mar 2026 21:05:59 GMT; Max-Age=31200; path=/; secure; httponly; samesite=lax
cache-control: no-cache, no-store, must-revalidate

                                                                               
┌──(root㉿peace)-[/home/peace/Desktop/Recon101]
└─# for ep in \
  "password/forgot" \
  "password/reset" \
  "storage/app" \
  "storage/logs" \
  ".env" \
  "config" \
  "telescope" \
  "horizon" \
  "livewire" \
  "broadcasting/auth"; do
    code=$(curl -sk -o /dev/null -w "%{http_code}" \
    -H "Host: sinistres.saarassurancesci.com" \
    https://5.189.160.190/$ep)
    echo "$code → /$ep"
    sleep 1
done
200 → /password/forgot
200 → /password/reset
404 → /storage/app
404 → /storage/logs
403 → /.env
404 → /config
404 → /telescope
404 → /horizon
404 → /livewire
403 → /broadcasting/auth
