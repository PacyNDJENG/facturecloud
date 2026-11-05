# Journal d'installation - S1

Binôme: [BIADOU DJIKE Donny, NDJENG Marthe Patience]
Date: [05/11/2026]
Système: Linux Ubuntu.

## Versions

- Python: Python 3.12.3
- Flask: Flask 3.1.3

## Ce qui a ete fait

1. Création de l'arborescence du projet `facturecloud` et de l'environnement virtuel (`python3 -m venv .venv`).
2. Installation des bibliothèques requises (`flask`, `gunicorn`, `pytest`).
3. Écriture et validation des tests unitaires (`pytest` avec 4 tests réussis).
4. Lancement des microservices `api-factures` (port 8080), `service-calcul` (port 8081) et `service-notification` (port 8082).
5. Vérification des routes de santé (`/sante`) et de calcul de la TVA (`/tva`) via `curl`.

## Ce que j'ai observé

- La fonction sante renvoie: {"statut":"ok"} avec le code 200
- TVA pour 1000: 193 ; TVA pour 200 que j'attendais: 39, obtenue: 39

## Problèmes rencontrés

1.  Etre place dans le mauvais repertoire 
Message d'erreur: python: can't open file '.../main.py': [Errno 2] No such file or directory
Cause: Mauvais repertoire courant dans le terminal                                     Correction: Se placer dans le bon dossier avec `cd api-factures` ou `cd service-calcul` 

2. Service non demarre mais s'attendant a un resultat different d'une erreure
Message d'erreur:  curl: (7) Failed to connect to localhost port 8080 
Cause: Service non démarré sur ce port
correction: Lancer le script `python3 main.py` dans le terminal dédié 


## Autoévaluation

| Je sais                                            | Seul | Avec aide | Pas encore |
| -------------------------------------------------- | ---- | --------- | ---------- |
| Expliquer ce qu'est un service web                 | X    |           |            |
| Utiliser un terminal                               | X    |           |            |
| Installer Python et créer un environnement virtuel | X    |           |            |
| Lancer deux services et les vérifier               | X    |           |            |
| Lire un message d'erreur                           | X    |           |            |
