# Email Cleaner Pro – Assets (GitHub Storage)

Ce dépôt contient les fichiers statiques utilisés par le notebook Colab « Email Cleaner Pro ».

## 🎯 Objectif
- Héberger le logo, la base GeoLite2 et les exemples de bounces
- Fournir des URLs directes et stables consommées par le notebook

## 📁 Structure
```
Email-Cleaner-Assets/
├── logo/
│   └── logo-kalel.png
├── geolite/
│   └── GeoLite2-Country.mmdb
└── bounces/
    ├── hard_bounce_example.eml
    ├── soft_bounce_full_example.eml
    └── soft_bounce_temp_example.eml
```

## 🔗 URLs Directes (prêtes à l’emploi)
- Logo: `https://raw.githubusercontent.com/Hai-Elkaim/Email-Cleaner-Assets/main/logo/logo-kalel.png`
- GeoLite2: `https://raw.githubusercontent.com/Hai-Elkaim/Email-Cleaner-Assets/main/geolite/GeoLite2-Country.mmdb`
- Bounces:
  - Hard: `https://raw.githubusercontent.com/Hai-Elkaim/Email-Cleaner-Assets/main/bounces/hard_bounce_example.eml`
  - Soft (full): `https://raw.githubusercontent.com/Hai-Elkaim/Email-Cleaner-Assets/main/bounces/soft_bounce_full_example.eml`
  - Soft (temp): `https://raw.githubusercontent.com/Hai-Elkaim/Email-Cleaner-Assets/main/bounces/soft_bounce_temp_example.eml`

## 🚀 Utilisation dans le Notebook Colab
Dans la cellule de configuration, les URLs sont déjà construites ainsi:
```python
GITHUB_USERNAME = "Hai-Elkaim"
LOGO_URL = f"https://raw.githubusercontent.com/{GITHUB_USERNAME}/Email-Cleaner-Assets/main/logo/logo-kalel.png"
GEOLITE_URL = f"https://raw.githubusercontent.com/{GITHUB_USERNAME}/Email-Cleaner-Assets/main/geolite/GeoLite2-Country.mmdb"
BOUNCES_URLS = {
    "hard": f"https://raw.githubusercontent.com/{GITHUB_USERNAME}/Email-Cleaner-Assets/main/bounces/hard_bounce_example.eml",
    "soft_full": f"https://raw.githubusercontent.com/{GITHUB_USERNAME}/Email-Cleaner-Assets/main/bounces/soft_bounce_full_example.eml",
    "soft_temp": f"https://raw.githubusercontent.com/{GITHUB_USERNAME}/Email-Cleaner-Assets/main/bounces/soft_bounce_temp_example.eml"
}
```

## 🛠️ Mise à jour des assets
1. Remplacez un fichier localement (ex: nouveau logo)
2. Poussez la mise à jour via le script d’upload (token requis)
   - Variable d’environnement (Windows PowerShell):
     ```powershell
     $env:GITHUB_TOKEN = "VOTRE_TOKEN_GITHUB"
     python upload_to_github.py
     ```
3. Vérifiez le statut HTTP 200 des URLs ci-dessus

## 🧩 Notes GeoLite (licence MaxMind)
- Assurez‑vous de respecter la licence MaxMind pour `GeoLite2-Country.mmdb`
- Si le téléchargement échoue, uploadez le fichier `.mmdb` manuellement ici

## 🧪 Test rapide
```bash
curl -I https://raw.githubusercontent.com/Hai-Elkaim/Email-Cleaner-Assets/main/logo/logo-kalel.png
```
Réponse attendue: `HTTP/2 200`

---
Mainteneur: Hai Elkaim – hai@kal-el.group

Ce repository contient tous les assets nécessaires pour le notebook Email Cleaner Pro.

## 📁 Structure

```
EmailCleanerPro-Assets/
├── README.md                    # Ce fichier
├── logo/                        # Logos
│   └── logo-kalel.png
├── geolite/                     # Base de données GeoIP
│   └── GeoLite2-Country.mmdb
├── bounces/                     # Exemples de bounces
│   ├── hard_bounce_example.eml
│   ├── soft_bounce_full_example.eml
│   └── soft_bounce_temp_example.eml
└── config/                      # Configuration
    └── urls.json
```

## 🔗 URLs Directes

### Logo
```
https://raw.githubusercontent.com/VOTRE_USERNAME/EmailCleanerPro-Assets/main/logo/logo-kalel.png
```

### GeoLite2
```
https://raw.githubusercontent.com/VOTRE_USERNAME/EmailCleanerPro-Assets/main/geolite/GeoLite2-Country.mmdb
```

### Exemples de Bounces
```
https://raw.githubusercontent.com/VOTRE_USERNAME/EmailCleanerPro-Assets/main/bounces/hard_bounce_example.eml
https://raw.githubusercontent.com/VOTRE_USERNAME/EmailCleanerPro-Assets/main/bounces/soft_bounce_full_example.eml
https://raw.githubusercontent.com/VOTRE_USERNAME/EmailCleanerPro-Assets/main/bounces/soft_bounce_temp_example.eml
```

## 📋 Instructions d'utilisation

1. **Forkez ce repository** dans votre compte GitHub
2. **Remplacez VOTRE_USERNAME** dans les URLs ci-dessus
3. **Uploadez vos assets** dans les dossiers correspondants
4. **Utilisez les URLs** dans votre notebook Colab

## 🔄 Mise à jour des assets

Pour mettre à jour les assets :
1. Modifiez les fichiers dans ce repository
2. Les URLs restent les mêmes
3. Colab téléchargera automatiquement la nouvelle version

## 📝 Notes

- Les URLs `raw.githubusercontent.com` sont permanentes
- Pas d'authentification requise
- CDN global de GitHub (rapide partout)
- Versioning automatique avec Git
