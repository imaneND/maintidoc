
# MaintiDoc — Assistant documentaire multimodal et agentique pour la maintenance

## 1. Présentation du projet

MaintiDoc est un assistant documentaire multimodal et agentique destiné aux techniciens et responsables de maintenance.

Il permet de poser des questions sur des équipements industriels à partir de documents techniques et de photographies.

L'assistant recherche les informations pertinentes dans le corpus documentaire et fournit des réponses accompagnées de références précises : document, page et figure.

Il peut également consulter l'historique des interventions via un outil MCP et préparer des tickets de maintenance. La création d'un ticket nécessite obligatoirement une validation humaine.

## 2. Objectifs du projet

- Faciliter la recherche d'informations dans les documents techniques.
- Comprendre les questions accompagnées de photographies.
- Retrouver les informations pertinentes dans les manuels et procédures.
- Fournir des réponses justifiées par des sources vérifiables.
- Consulter les historiques de maintenance.
- Préparer des tickets de maintenance avec approbation humaine.
- Garantir le contrôle des accès aux documents.

## 3. Familles d'équipements étudiées

Le corpus documentaire couvre deux familles :

- **Famille 1 :** Pompes centrifuges.
- **Famille 2 :** Groupes électrogènes diesel.

## 4. Structure du dépôt

```text
maintidoc/
│
├── README.md
├── .gitignore
│
├── docs/
│   └── diagrammes/
│
└── corpus/
    ├── inventaire.csv
    ├── prompts_corpus.md
    │
    ├── documents/
    │   ├── famille_1/
    │   └── famille_2/
    │
    └── images/
```

## 5. Corpus documentaire

Le corpus est constitué de 30 à 50 documents portant sur les deux familles d'équipements étudiées.

Il comprend :
- Des manuels techniques.
- Des procédures de maintenance.
- Des fiches de sécurité.
- Des schémas techniques.
- Des tableaux de codes d'alarme.
- Des photographies de panneaux et de voyants.
- Des historiques d'interventions fictifs.

Le fichier `inventaire.csv` contient les métadonnées de chaque document : identifiant, titre, famille d'équipement, format, provenance, licence, vérification et groupe d'accès.

Le fichier `prompts_corpus.md` assure la traçabilité des prompts utilisés pour rechercher ou générer les documents.

Les documents sont vérifiés et corrigés par les membres de l'équipe avant leur intégration au corpus.

## 6. Architecture cible

L'architecture envisagée repose sur plusieurs blocs fonctionnels :

- Interface utilisateur.
- API et authentification.
- Orchestration des requêtes.
- Ingestion documentaire et OCR.
- Recherche documentaire multimodale (RAG).
- Modèle vision-langage (VLM).
- Client et serveur MCP.
- Vérification des citations.
- Validation humaine.
- Stockage documentaire et index.

## 7. Sécurité et contrôle d'accès

Le projet prévoit :

- Une authentification des utilisateurs.
- Une séparation des accès selon les familles d'équipements.
- Une vérification des autorisations avant la recherche documentaire.
- Une protection contre les injections de prompt.
- Une vérification des sources avant la génération de la réponse.
- Une validation humaine obligatoire avant la création d'un ticket.

Les données utilisées dans le projet sont fictives ou publiques et vérifiées. Aucune donnée personnelle réelle n'est intégrée au corpus.

## 8. Organisation de l'équipe

**Membres de l'équipe :**
- Bikikre Rania
- Imane Nadif

**Module :** IA générative multimodale  
**Établissement :** EMSI  
**Année universitaire :** 2026–2027

## 9. État du projet

Le livrable 1 porte sur le cadrage, la constitution du corpus documentaire, la définition de l'architecture cible, les flux de données, l'analyse des risques et l'organisation de l'équipe.

