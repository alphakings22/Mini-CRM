Mini-CRM — Pipeline commercial

Application de gestion de contacts et d'opportunités commerciales (deals),
avec pipeline de vente et dashboard de suivi.

Installation

```bash
pip install -r requirements.txt
```

Lancer l'application

```bash
streamlit run app.py
```

Une base de données SQLite (`crm.db`) est créée automatiquement au premier lancement,
dans le même dossier. Les données sont sauvegardées en local.

Fonctionnalités

- **Contacts** : ajout, consultation, suppression de clients/prospects
- **Deals** : création d'opportunités commerciales liées à un contact, avec valeur et étape
  (Prospect → Qualification → Négociation → Gagné/Perdu)
- **Dashboard** : valeur totale et active du pipeline, valeur gagnée, taux de conversion,
  répartition des deals par étape

Structure

```
mini-crm/
├── app.py              interface Streamlit (3 onglets)
├── database.py          couche d'accès à la base SQLite (CRUD)
├── crm_analysis.py       calculs et agrégations pour le dashboard
├── requirements.txt
└── crm.db                créé automatiquement au premier lancement
```

Pour aller plus loin
Developper par JOHNSON Kwueku Bentsi Jucal
- Ajouter une date de clôture prévue par deal, avec relances automatiques
- Export CSV du pipeline
- Historique des changements d'étape (audit trail)
