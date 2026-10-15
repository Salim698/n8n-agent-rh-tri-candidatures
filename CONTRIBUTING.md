# Contribuer au projet

Merci de l'intérêt que tu portes à l'amélioration de cet agent RH n8n !

## Processus
1. Fais un fork du dépôt.
2. Crée une branche avec le nom de ta fonctionnalité (`git checkout -b feature/amelioration-score`).
3. Propose une Pull Request (PR) claire et détaillée.

## ✅ Checklist d'export sécurisé d'un workflow n8n (OBLIGATOIRE)

Avant de soumettre le fichier `workflow.json`, vérifie **absolument** les points suivants :
- [ ] Aucun bloc `credentials` complet (supprime-les).
- [ ] Aucun `webhookId` laissé en clair dans les nœuds Webhook / Services (Gmail, Telegram...).
- [ ] Le champ `meta` à la racine doit être vide `{}`.
- [ ] Aucun ID privé (Base de données, Google Sheet, Folder ID) : utilise les placeholders `YOUR_ID_HERE` ou des variables d'environnement `{{ $env.VAR }}`.
- [ ] Aucun email, nom ou numéro de téléphone personnel en dur dans le code.
- [ ] Retire les balises `cachedResultUrl` et `cachedResultName` des nœuds Airtable/Google Sheets.
- [ ] Le workflow doit être désactivé (`active: false`).
- [ ] Si tu ajoutes des captures d'écran, floute toutes les données réelles (noms, emails, contenus de messages).

Reportez-vous à notre [Code de Conduite](CODE_OF_CONDUCT.md).
