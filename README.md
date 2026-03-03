─# curl -sk \
-H "Host: sinistres.saarassurancesci.com" \
https://5.189.160.190/login
<!DOCTYPE html>
<html lang="fr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Connexion - SAAR Assurances</title>
    <meta name="csrf-token" content="D3ngm8nTSmqTfIwnVsNHG6ey6JM7uiyb2oswIuSl">
    <link rel="preload" as="style" href="https://sinistres.saarassurancesci.com/build/assets/app-CJgBFmMc.css" /><link rel="modulepreload" as="script" href="https://sinistres.saarassurancesci.com/build/assets/app-jcWQAc2V.js" /><link rel="stylesheet" href="https://sinistres.saarassurancesci.com/build/assets/app-CJgBFmMc.css" /><script type="module" src="https://sinistres.saarassurancesci.com/build/assets/app-jcWQAc2V.js"></script></head>

<body class="bg-gradient-to-br from-red-50 via-white to-green-50 min-h-screen">
    <div class="min-h-screen flex items-center justify-center py-12 px-4 sm:px-6 lg:px-8">
        <div class="max-w-md w-full space-y-8">
            <!-- Bouton retour à l'accueil -->
            <div class="text-left">
                <a href="https://sinistres.saarassurancesci.com" class="inline-flex items-center text-saar-blue hover:text-saar-red transition-colors duration-200">
                    <svg class="w-5 h-5 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 19l-7-7m0 0l7-7m-7 7h18"></path>
                    </svg>
                    Retour à l'accueil
                </a>
            </div>
            
            <!-- Logo et titre -->
            <div class="text-center">
                <div class="mx-auto w-32 h-32 rounded-2xl flex items-center justify-center mb-4">
                    <img src="https://sinistres.saarassurancesci.com/logo.png" alt="SAAR Assurances" class="w-32 h-32 object-contain">
                </div>
                <h2
                    class="text-3xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-saar-red to-saar-green">
                    SAAR ASSURANCES
                </h2>
                <p class="mt-2 text-sm text-gray-600">
                    Connectez-vous à votre espace de gestion
                </p>
            </div>

            <!-- Messages de succès/erreur -->
            
            
            <!-- Formulaire de connexion -->
            <form class="mt-8 space-y-6" action="https://sinistres.saarassurancesci.com/login" method="POST">
                <input type="hidden" name="_token" value="D3ngm8nTSmqTfIwnVsNHG6ey6JM7uiyb2oswIuSl" autocomplete="off">                <div class="space-y-4">
                    <div>
                        <label for="email" class="block text-sm font-medium text-gray-700 mb-2">
                            Adresse email
                        </label>
                        <input id="email" name="email" type="email" autocomplete="email" required
                            value=""
                            class="appearance-none relative block w-full px-3 py-3 border border-gray-300 placeholder-gray-500 text-gray-900 rounded-lg focus:outline-none focus:ring-2 focus:ring-saar-blue focus:border-saar-blue focus:z-10 sm:text-sm"
                            placeholder="votre@email.com">
                    </div>

                    <div>
                        <label for="password" class="block text-sm font-medium text-gray-700 mb-2">
                            Mot de passe
                        </label>
                        <input id="password" name="password" type="password" autocomplete="current-password" required
                            class="appearance-none relative block w-full px-3 py-3 border border-gray-300 placeholder-gray-500 text-gray-900 rounded-lg focus:outline-none focus:ring-2 focus:ring-saar-blue focus:border-saar-blue focus:z-10 sm:text-sm"
                            placeholder="Votre mot de passe">
                    </div>
                </div>

                <div class="flex items-center justify-between">
                    <div class="flex items-center">
                        <input id="remember-me" name="remember" type="checkbox"
                            class="h-4 w-4 text-saar-blue focus:ring-saar-blue border-gray-300 rounded">
                        <label for="remember-me" class="ml-2 block text-sm text-gray-900">
                            Se souvenir de moi
                        </label>
                    </div>
                    <div class="text-sm">
                        <a href="https://sinistres.saarassurancesci.com/password/forgot" class="font-medium text-saar-blue hover:text-blue-800 transition-colors duration-200">
                            Mot de passe oublié ?
                        </a>
                    </div>
                </div>

                <div>
                    <button type="submit"
                        class="group relative w-full flex justify-center py-3 px-4 border border-transparent text-sm font-medium rounded-lg text-white bg-gradient-to-r from-saar-blue to-blue-600 hover:from-blue-700 hover:to-blue-800 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-saar-blue transition-all duration-200">
                        <span class="absolute left-0 inset-y-0 flex items-center pl-3">
                            <svg class="h-5 w-5 text-blue-300 group-hover:text-blue-400"
                                xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor"
                                aria-hidden="true">
                                <path fill-rule="evenodd"
                                    d="M5 9V7a5 5 0 0110 0v2a2 2 0 012 2v5a2 2 0 01-2 2H5a2 2 0 01-2-2v-5a2 2 0 012-2zm8-2v2H7V7a3 3 0 016 0z"
                                    clip-rule="evenodd" />
                            </svg>
                        </span>
                        Se connecter
                    </button>
                </div>
            </form>
        </div>
    </div>
</body>

</html>
                                                                               
┌──(root㉿peace)-[/home/peace/Desktop/Recon101]
└─# curl -sk -I \
-H "Host: sinistres.saarassurancesci.com" \
https://5.189.160.190/login
HTTP/2 200 
server: nginx/1.24.0 (Ubuntu)
content-type: text/html; charset=utf-8
vary: Accept-Encoding
cache-control: no-cache, private
date: Tue, 03 Mar 2026 12:21:33 GMT
set-cookie: XSRF-TOKEN=eyJpdiI6InJzMjZFTDZvU1l6NkEzTlJLV3JVYlE9PSIsInZhbHVlIjoiK1NoSEc5U3p0bGVzaTg4N3V5VHk3V0lqWFBNRUVKRUNGRmgzMVVvaW1EQlZIZjdYYnZldndxcTVrakZacTA1UkhhenZacHpUS25RZmtqREMraEZNaURXWTJkR0RqdWVLZXo0Rk5vQm53L0VUL2VpdmY1b1BtR2EyZ2pLVGpSanEiLCJtYWMiOiIyOGJlZjBhZDU1YjE3YzM5NmNiNWI4ZGRlODk4Zjc2OGFkZGQ0YmIyY2FjZWRiMmVlYTE2ZGE4NmZmZGE4ZjJiIiwidGFnIjoiIn0%3D; expires=Tue, 03 Mar 2026 21:01:33 GMT; Max-Age=31200; path=/; secure; samesite=lax
set-cookie: saar_sinistre_session=eyJpdiI6IjU0SmRJOTMzcGhwbkxWaU0xN0thUUE9PSIsInZhbHVlIjoiZ3ptMFljWmlGR2R6ZkEyTDdCK2loc29QbnEzcHA1QktaQjEydHZ1bVRBYkgrNEdSUkd3N1lyeCtSWDd0Qy92d3BITktvNktGZ0h1SzNkRXNlOW90V3VJRmtSbUNza1dsVEZleVU5VHFjd2tldmdEQzF3QklxNXJLcVU0VmZuTm8iLCJtYWMiOiJlMTgwMzQxM2RiZGVlZjAyOGY4YTEzMjY0MzkwMThiOGU2MWI5ODY0OWE5YmU1NWU3YjkwZTQwYzg5YzgwZWQ5IiwidGFnIjoiIn0%3D; expires=Tue, 03 Mar 2026 21:01:33 GMT; Max-Age=31200; path=/; secure; httponly; samesite=lax
cache-control: no-cache, no-store, must-revalidate

                                                                               
┌──(root㉿peace)-[/home/peace/Desktop/Recon101]
└─# for ep in \
  "register" \
  "forgot-password" \
  "reset-password" \
  "dashboard" \
  "admin" \
  "api" \
  "logout" \
  "profile" \
  "declaration" \
  "sinistre" \
  "nouveau-sinistre" \
  "sw.js" \
  "manifest.json" \
  "robots.txt" \
  "storage" \
  "public"; do
    code=$(curl -sk -o /dev/null -w "%{http_code}" \
    -H "Host: sinistres.saarassurancesci.com" \
    https://5.189.160.190/$ep)
    echo "$code → /$ep"
    sleep 1
done
404 → /register
404 → /forgot-password
404 → /reset-password
404 → /dashboard
404 → /admin
404 → /api
405 → /logout
404 → /profile
404 → /declaration
404 → /sinistre
404 → /nouveau-sinistre
200 → /sw.js
200 → /manifest.json
200 → /robots.txt
301 → /storage
404 → /public
