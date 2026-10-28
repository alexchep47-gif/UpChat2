# UpChat2

Deuxième base UpChat. Reçoit un **ZIP** de ton projet, puis **importe les fonctionnalités manquantes** depuis [`alexchep47-gif/upchat`](https://github.com/alexchep47-gif/upchat).

## ZIP trop gros (ex. 62 Mo) — limite navigateur 25 Mo

**Ne force pas l’upload** sur GitHub (max ~25 Mo via le site).

### Méthode 1 — URL (la plus simple)

1. Envoie le ZIP sur **Google Drive / Dropbox / WeTransfer**
2. Récupère un **lien de téléchargement direct**
3. Repo **UpChat2** → onglet **Actions**
4. Workflow **Import ZIP & merge features** → **Run workflow**
5. Champ **`zip_url`** : colle le lien
6. Valide — le runner télécharge le fichier (jusqu’à plusieurs centaines de Mo)

Astuce Google Drive : lien du type  
`https://drive.google.com/uc?export=download&id=FILE_ID`  
(remplace `FILE_ID` par l’id du fichier dans l’URL partage).

### Méthode 2 — ZIP allégé &lt; 25 Mo

Supprime avant compression : `build/`, `.dart_tool/`, `.idea/`, `android/.gradle/`, `ios/Pods/`.  
Puis **Add file → Upload files** dans `incoming/`.

### Méthode 3 — Release GitHub

Crée une Release, attache le ZIP (limite bien plus haute), puis utilise l’URL de l’asset dans `zip_url`.

## Secrets

Recopie depuis `upchat` : `FIREBASE_*`, keystore, `GOOGLE_SERVER_CLIENT_ID`, etc.

## Auteur

**NEMMEGNE CHEPING ALEXANDRE MERVIN** — Nationalité : Camerounaise.
