──(root㉿peace)-[/home/peace/Desktop/Recon101]
└─# curl -sk -I \
-H "Host: sinistres.saarassurancesci.com" \
https://5.189.160.190/assures/dashboard  
HTTP/2 302 
server: nginx/1.24.0 (Ubuntu)
content-type: text/html; charset=utf-8
location: https://sinistres.saarassurancesci.com/login
cache-control: no-cache, private
date: Tue, 03 Mar 2026 12:31:10 GMT
set-cookie: XSRF-TOKEN=eyJpdiI6IldiRjgzNHhmUUR6SUFVcSs3QmUzUVE9PSIsInZhbHVlIjoiWWhna1UrRHQ1YkFQWHdUV1lXVEVndHd4R1NOdERPUy9JcGxVZVJRZTVuL2xUNFVVYVFPU0V2N3ZRVG1yRE1ad2wrU3duTU1BZG9DTUVZaExJRThRNVI4cUwreVBxV0UrTU5ETEVwaGFqN1Rsc2dTSnpCcEpDYjdPVUZrOFZNTWoiLCJtYWMiOiIxNzEzNmZmMGUxM2RlMDk0ZDkxN2NmYzVkMzJmNWZhMWVlMDBmNWJmZjk0NmJmMTI3Y2UzNGQzNmQ3YjlhYmRkIiwidGFnIjoiIn0%3D; expires=Tue, 03 Mar 2026 21:11:10 GMT; Max-Age=31200; path=/; secure; samesite=lax
set-cookie: saar_sinistre_session=eyJpdiI6ImorbVVrdUxGcFhnaXJ1a2FQL0Vvc3c9PSIsInZhbHVlIjoidENWQS8vSTQwcGFYZy9JdEttektSTVpPcnF0NitnYnQ5d0t6MTB2VkZuOHp0c1pzT1hrbXpzLzdHZE9KWG9hZnJGcldjV2J2c003V3NWK21CRjQxc3N2RFdrN05mbm5KMnhGcEpQSjIxaUhmVk5GQVlNSVp4N1g4Si9FR1FyZCsiLCJtYWMiOiI4NWUxMGRhMDFiMWZmNWU4YTZkZmY2YTQ1NGNiN2FhZjBlZGE3YTQxY2FmMWU3YTkzOWUwMmU5OWYzYjQ1NjBjIiwidGFnIjoiIn0%3D; expires=Tue, 03 Mar 2026 21:11:10 GMT; Max-Age=31200; path=/; secure; httponly; samesite=lax
cache-control: no-cache, no-store, must-revalidate

                                                                               
┌──(root㉿peace)-[/home/peace/Desktop/Recon101]
└─# TOKEN=$(curl -sk \
-H "Host: sinistres.saarassurancesci.com" \
https://5.189.160.190/password/forgot \
| grep -oP '(?<=name="_token" value=")[^"]+')
echo "Token: $TOKEN"
Token: gvA4u001tti05WFEAqeeCsEhSDUopWBYF68dLqL2
                                                                               
┌──(root㉿peace)-[/home/peace/Desktop/Recon101]
└─# curl -sk \
-H "Host: sinistres.saarassurancesci.com" \
-H "Content-Type: application/x-www-form-urlencoded" \
-X POST \
-c cookies.txt \
--data "_token=$TOKEN&email=inexistant@test.com" \
https://5.189.160.190/password/forgot
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="robots" content="noindex,nofollow,noarchive" />
    <title>An Error Occurred: Method Not Allowed</title>
    <link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 128 128%22><text y=%221.2em%22 font-size=%2296%22>❌</text></svg>" />
    <style>body { background-color: #fff; color: #222; font: 16px/1.5 -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; margin: 0; }
.container { margin: 30px; max-width: 600px; }
h1 { color: #dc3545; font-size: 24px; }
h2 { font-size: 18px; }</style>
</head>
<body>
<div class="container">
    <h1>Oops! An Error Occurred</h1>
    <h2>The server returned a "405 Method Not Allowed".</h2>

    <p>
        Something is broken. Please let us know what you were doing when this error occurred.
        We will fix it as soon as possible. Sorry for any inconvenience caused.
    </p>
</div>
</body>
</html>                                                                               
┌──(root㉿peace)-[/home/peace/Desktop/Recon101]
└─# curl -sk \
-H "Host: sinistres.saarassurancesci.com" \
-H "Content-Type: application/x-www-form-urlencoded" \
-X POST \
-c cookies.txt \
--data "_token=$TOKEN&email=admin@saarassurancesci.com" \
https://5.189.160.190/password/forgot
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="robots" content="noindex,nofollow,noarchive" />
    <title>An Error Occurred: Method Not Allowed</title>
    <link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 128 128%22><text y=%221.2em%22 font-size=%2296%22>❌</text></svg>" />
    <style>body { background-color: #fff; color: #222; font: 16px/1.5 -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; margin: 0; }
.container { margin: 30px; max-width: 600px; }
h1 { color: #dc3545; font-size: 24px; }
h2 { font-size: 18px; }</style>
</head>
<body>
<div class="container">
    <h1>Oops! An Error Occurred</h1>
    <h2>The server returned a "405 Method Not Allowed".</h2>

    <p>
        Something is broken. Please let us know what you were doing when this error occurred.
        We will fix it as soon as possible. Sorry for any inconvenience caused.
    </p>
</div>
</body>
</html>   
