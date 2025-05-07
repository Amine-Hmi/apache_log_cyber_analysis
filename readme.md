# Analyse des journaux Apache avec détection de menaces et enrichissement géographique

<img src="images/header.png" width="600"/>

## Objectif du projet

Ce projet vise à analyser des fichiers de logs Apache à l'aide de **PySpark** dans une optique **cybersécurité**. L'objectif est de :

- Détecter les IP suspectes à fort trafic.
- Identifier les tentatives d'attaques (brute force, injection SQL, etc.).
- Enrichir les logs avec des informations de géolocalisation via la base **GeoLite2**.
- Visualiser les résultats dans un mini dashboard interactif.

## Technologies utilisées

- **PySpark** : traitement distribué de grands volumes de logs.
- **GeoIP2** : enrichissement géographique des adresses IP.
- **Matplotlib** : génération de graphiques et dashboards.
- **Regex** : extraction des informations depuis les logs bruts.

## Étapes suivies

1. **Chargement des données** depuis un fichier de logs Apache (format CLF).
2. **Parsing** des lignes à l’aide d’expressions régulières.
3. **Agrégation Spark** pour identifier :
   - les IPs les plus actives,
   - les codes d’erreur fréquents,
   - les requêtes suspectes.
4. **Détection de menaces** (403/401 répétées, SQLi, traversée de répertoires).
5. **Géolocalisation des IPs** grâce à GeoLite2.
6. **Création d’un tableau de bord interactif** avec Streamlit.

## Idées d’amélioration

- Ajouter un lien automatique vers une base **threat intelligence** (ex: AbuseIPDB).
- Support d'autres formats de logs (Nginx, FTP, firewall).
- Générer des alertes en temps réel avec Kafka.
- Créer une interface web plus complète avec Grafana ou Kibana.

## Exécution rapide

1. Clonez le dépôt :
   ```bash
   git clone https://github.com/votre-utilisateur/apache-log-cyber-analysis.git
   cd apache-log-cyber-analysis