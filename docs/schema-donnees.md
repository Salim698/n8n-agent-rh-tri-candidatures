# Schéma des données

Respectez scrupuleusement la casse et les espaces (évitez les espaces parasites à la fin des noms de colonnes).

### Table "Candidats"
- Prénom (String)
- Nom (String)
- Email (String)
- Résumé (String)
- CV (Array d'URLs)
- Score global (Number)
- Score détail (String)
- Statut (Options : `revue en cours`, `ok étape suivante`)
- Description poste (Link to record)

### Table "Description poste"
- Titre poste (String)
- Description poste (String)
- Assigné à (String)
- Statut (String - ex: `poste ouvert`)
- Candidats (Array/Link)
