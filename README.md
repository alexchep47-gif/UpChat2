# UpChat2

Deuxième base UpChat. Ce dépôt est conçu pour **recevoir un ZIP** de ton projet, puis **récupérer automatiquement** les fonctionnalités manquantes depuis le dépôt principal [`alexchep47-gif/upchat`](https://github.com/alexchep47-gif/upchat).

## Comment envoyer ton ZIP

### Méthode recommandée (téléphone / navigateur)

1. Ouvre https://github.com/alexchep47-gif/UpChat2  
2. Clique **Add file** → **Upload files**  
3. Dépose ton fichier dans le dossier **`incoming/`**  
   - Nom conseillé : `incoming/upchat2-source.zip`  
4. Commit sur la branche **`main`**  
5. Va dans l’onglet **Actions** → workflow **Import ZIP & merge features**  
6. Quand c’est vert, lance **Build Android** si besoin  
7. Télécharge l’artefact **upchat2-apk**

### Méthode manuelle (workflow)

1. **Actions** → **Import ZIP & merge features** → **Run workflow**  
2. Indique le chemin du ZIP déjà présent dans le repo (ex. `incoming/upchat2-source.zip`)

## Ce que le workflow fait

1. Décompresse le ZIP (racine Flutter attendue : `pubspec.yaml` + `lib/`)  
2. Clone le dépôt **upchat** (source des fonctionnalités)  
3. Copie / écrase les modules manquants ou corrigés :  
   - Auth Google + login  
   - Mode internet / signalisation  
   - Chat (réception messages, conversationId)  
   - Glassmorphisme (`AppGlass`, `GlassSurface`)  
   - Fiche contact  
   - Thème, routes, `StorageService.setUserId`, etc.  
4. Commit le résultat sur `main`  
5. (Optionnel) déclenche le build APK

## Secrets GitHub à recopier depuis `upchat`

Dans **Settings → Secrets and variables → Actions**, ajoute au minimum :

| Secret | Rôle |
|--------|------|
| `FIREBASE_ANDROID_JSON_BASE64` | `google-services.json` |
| `FIREBASE_OPTIONS_DART_BASE64` | `lib/firebase_options.dart` |
| `UPCHAT_KEYSTORE_BASE64` | Keystore release |
| `UPCHAT_KEYSTORE_PASSWORD` | Mot de passe store |
| `UPCHAT_KEY_ALIAS` | Alias (souvent `upchat`) |
| `UPCHAT_KEY_PASSWORD` | Mot de passe clé |
| `GOOGLE_SERVER_CLIENT_ID` | Client OAuth **Web** Firebase |

## Auteur

Créé par **NEMMEGNE CHEPING ALEXANDRE MERVIN** — Nationalité : Camerounaise.
