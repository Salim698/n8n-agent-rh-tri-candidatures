# Guide d'Installation

## 1. Prérequis
- Une instance n8n fonctionnelle.
- Un projet Google Cloud avec les API Gmail et Drive activées, et un compte de service/OAuth.
- Un compte Airtable avec un Personal Access Token.
- Une clé API Google Gemini.

## 2. Configuration des variables
Copiez le fichier `.env.example` en `.env` dans le contexte de votre instance n8n et remplissez :
- `DELAI_REPONSE_JOURS`, `NOM_ENTREPRISE`, `EMAIL_RH`
- `GOOGLE_DRIVE_FOLDER_ID`

## 3. Base de données Airtable
Créez une base Airtable avec deux tables exactement identiques aux modèles fournis dans `data/candidats_template.csv` et `data/description_poste_template.csv`.
Notez votre `Base ID` et vos `Table IDs`.

## 4. Import n8n
1. Ouvrez n8n, créez un nouveau workflow.
2. Menu -> Import from File -> Sélectionnez `workflow.json`.
3. Parcourez chaque nœud Airtable et Drive pour remplacer `YOUR_AIRTABLE_...` par vos IDs réels.
4. Configurez vos Credentials n8n et assignez-les aux nœuds appropriés (les connexions ont été purgées pour la sécurité).
5. Activez le workflow !
