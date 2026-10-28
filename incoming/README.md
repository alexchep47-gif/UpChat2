# Dossier `incoming/`

## Limite GitHub : 25 Mo via le navigateur

Si ton ZIP fait **plus de 25 Mo** (ex. 62 Mo), **ne l’uploade pas** ici.

### Option A — Lien de téléchargement (recommandé)

1. Mets le ZIP sur Google Drive, Dropbox, WeTransfer, MediaFire, etc.
2. Obtient un **lien de téléchargement direct** (pas seulement une page de preview)
3. GitHub → **Actions** → **Import ZIP & merge features** → **Run workflow**
4. Colle l’URL dans le champ **`zip_url`**
5. Laisse `zip_path` vide

### Option B — ZIP allégé &lt; 25 Mo

Avant de zipper, **supprime** ces dossiers s’ils sont dedans :

- `build/`
- `.dart_tool/`
- `.idea/`
- `android/.gradle/`
- `ios/Pods/`
- `**/Generated.xcconfig` lourds inutiles

Un projet source Flutter fait souvent **5–15 Mo** sans ces dossiers.

Puis uploade `incoming/upchat2-source.zip` (&lt; 25 Mo).

### Option C — Release GitHub (jusqu’à 2 Go)

1. Crée une **Release** sur UpChat2 (tag `source-1`)
2. Joins le ZIP comme asset de la release
3. Lance le workflow avec l’URL de l’asset  
   (`https://github.com/alexchep47-gif/UpChat2/releases/download/source-1/tonfichier.zip`)
