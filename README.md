┌──(root㉿peace)-[/home/peace/Desktop/Recon101]
└─# for ep in \
  "declaration" \
  "assures/dashboard" \
  "assures/sinistres" \
  "assures/profil" \
  "gestionnaire/dashboard" \
  "admin/dashboard" \
  "expert/dashboard" \
  "api/sinistres" \
  "api/declarations" \
  "api/assures"; do
    code=$(curl -sk -o /dev/null -w "%{http_code}" \
    -H "Host: sinistres.saarassurancesci.com" \
    https://5.189.160.190/$ep)
    echo "$code → /$ep"
    sleep 1
done
404 → /declaration
302 → /assures/dashboard
404 → /assures/sinistres
404 → /assures/profil
404 → /gestionnaire/dashboard
404 → /admin/dashboard
404 → /expert/dashboard
404 → /api/sinistres
404 → /api/declarations
404 → /api/assures
                                                                               
┌──(root㉿peace)-[/home/peace/Desktop/Recon101]
└─# curl -sk \
-H "Host: sinistres.saarassurancesci.com" \
-H "Content-Type: application/json" \
-X POST \
--data '{"email":"test@test.com","_token":"D3ngm8nTSmqTfIwnVsNHG6ey6JM7uiyb2oswIuSl"}' \
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
