# Format des données et Tests

## Structure d'entrée attendue
Le workflow s'attend à recevoir des objets standardisés par le trigger Gmail n8n.
Consultez `examples/gmail_payload.json` pour la structure exacte.

Les clés critiques lues par le workflow :
- `$json.subject`
- `$json.snippet`
- `$json.from.value[0].address`
- `$json.attachments` (tableau de binaires)
