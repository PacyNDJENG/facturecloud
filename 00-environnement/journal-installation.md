# Journal d'installation - S1

Binôme: [BIADOU DJIKE Donny, NDJENG Marthe Patience]
Date: [05/11/2026]
Système: Linux Ubuntu.

## Versions

- Python: Python 3.12.3
- Flask: Flask 3.1.3

## Ce qui a ete fait
1. Création du dossier `~/TVL501` et copie du projet `facturecloud` dans `~/TVL501/facturecloud`.
2. Ouverture du projet dans l'éditeur et vérification de la route `/sante` dans `api-factures/main.py`.
3. Création et activation de l'environnement virtuel `.venv` (`python3 -m venv .venv` puis `source .venv/bin/activate`).
4. Installation de Flask (`pip install flask`) et d'autres bibliotheques requises (`gunicorn`, `pytest`) 
5. Lancement de `api-factures` sur le port 8080 (Terminal 1) et de `service-calcul` sur le port 8081 (Terminal 2).
6. Vérification des routes `/sante`, `/factures/...` et `/tva` (cas valides et erreurs 404/400), puis test des erreurs d'arrêt et de mauvais dossier.


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
