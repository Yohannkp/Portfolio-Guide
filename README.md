# Guide des projets — Yendi Yohann

Élève ingénieur Big Data & IA à l'ECE Paris, orienté **MLOps et data engineering** : affiner un modèle, le servir derrière une API, le conteneuriser et le déployer de façon reproductible. **Je cherche un stage de 4 à 6 mois à partir d'avril 2027.**

Les projets sont classés par ce qu'ils démontrent, comme sur [mon portfolio](https://v0-junior-developer-portfolio-bay.vercel.app/projects). Pour chacun : le problème posé, ce qui a été fait, et la preuve quand elle est chiffrable.

## Sommaire

- [Mettre des modèles en production](#mettre-des-modèles-en-production) — 3 projets
- [Affiner et entraîner des modèles](#affiner-et-entraîner-des-modèles) — 4 projets
- [Mesurer et prouver](#mesurer-et-prouver) — 5 projets
- [Construire des applications](#construire-des-applications) — 5 projets

## Mettre des modèles en production

_Servir, conteneuriser, rendre fiable : qu'un modèle serve à quelqu'un, pas seulement dans un notebook._

| Projet | Le problème | Preuve | Stack | Lien |
|---|---|---|---|---|
| **RAG-Local** <br/> _assistant documentaire_ | Un assistant utile sur ses documents, sans envoyer un seul fichier à un service externe. | **0** requête réseau sortante : tout reste sur la machine | FastAPI · Chroma · Ollama · Next.js · Docker Compose · RAGAS | [Code](https://github.com/Yohannkp/RAG-Local) |
| **SELF_DEV_AGENT** <br/> _agent de développement_ | Un modèle local de 7 milliards de paramètres n'est pas fiable : on ne peut pas croire ses réponses. | **7 Md** de paramètres : peu fiable seul, vérifié par les tests | Ollama · Tool calling · AST · Python | [Code](https://github.com/Yohannkp/Claude-local) |
| **Prédiction de productivité** <br/> _modèle servi par une API_ | Prédire la productivité d'une équipe, et que la prédiction serve dans une application. | — | FastAPI · Flutter · Python · Machine Learning | [Code](https://github.com/Yohannkp/Application-prediction-de-productivit-) |

## Affiner et entraîner des modèles

_Comprendre ce qu'on entraîne : la donnée, l'environnement, l'architecture, et ce qui manque quand rien n'existe._

| Projet | Le problème | Preuve | Stack | Lien |
|---|---|---|---|---|
| **Mina-Translator** <br/> _traduction français ↔ mina_ | Le mina n'a aucun corpus parallèle public : sur une langue peu dotée, la difficulté est la donnée, pas l'entraînement. | **360** paires retenues après audit, sur 500 générées | QLoRA · Whisper · FastAPI · Streamlit | [Code](https://github.com/Yohannkp/mina-translator) |
| **Snake RL** <br/> _apprentissage par renforcement_ | Apprendre à jouer à Snake sans aucune règle écrite à la main. | **0** règle écrite à la main : l'agent apprend seul | PyTorch · Gymnasium · DQN | [Code](https://github.com/Yohannkp/Apprentissage-par-renforcement-Snake-Game) |
| **Détection d'émotions** <br/> _vision par ordinateur_ | Reconnaître des émotions image par image, en temps réel, sur un flux webcam. | — | PyTorch · OpenCV · CNN | [Code](https://github.com/Yohannkp/D-tection-des-motions) |
| **Détection de fausses actualités** <br/> _classification de texte_ | Distinguer les vrais des faux articles de presse. | — | Keras · LSTM · NLP | [Code](https://github.com/Yohannkp/Fake-News-Detection-with-Machine-Learning) |

## Mesurer et prouver

_Ne pas s'arrêter à « ça marche » : choisir le bon test, quantifier l'effet, expliquer la décision._

| Projet | Le problème | Preuve | Stack | Lien |
|---|---|---|---|---|
| **Optimisation des ventes** <br/> _impact d'un agencement en magasin_ | Mesurer l'effet d'un nouvel agencement quand on ne peut pas tirer les magasins au sort. | **1 : 1** un magasin contrôle apparié à chaque magasin test | pandas · Inférence causale · Tests statistiques | [Code](https://github.com/Yohannkp/Optimisation-des-ventes) |
| **Scoring de risque crédit** <br/> _classification déséquilibrée_ | Prévoir le défaut sur des données bancaires fortement déséquilibrées, en limitant les faux négatifs. | **0,88** d'AUC sur le jeu de test | XGBoost · SHAP · SMOTE | [Code](https://github.com/Yohannkp/Finance-Analytics---Credit-Scoring) |
| **Départ des employés** <br/> _rétention des salariés_ | Identifier les salariés à risque de départ, et ce qui les retient avant qu'ils démissionnent. | **0,94** d'AUC sur le jeu de test | Random Forest · Scikit-learn · Power BI | [Code](https://github.com/Yohannkp/Projet-Salifort-Motors.) |
| **Ventes en supermarché** <br/> _analyse SQL_ | Savoir ce qui rapporte et ce qui coûte dans les ventes d'un supermarché : plus de 878 000 lignes de vente, prix de gros et taux de perte. | **878 000** lignes de vente analysées en SQL | SQL · CTE · Fonctions de fenêtrage | [Code](https://github.com/Yohannkp/Supermarket-Sales-Analysis-SQL-Driven-Business-Insights) |
| **Test A/B d'une page** <br/> _expérimentation_ | Décider laquelle de deux versions d'une page convertit le mieux. | — | scipy · pandas · Streamlit | [Code](https://github.com/Yohannkp/Tests-Statistiques-Landing-Page) |

## Construire des applications

_Le socle de développement : backend, authentification, bases de données, interfaces._

| Projet | Le problème | Preuve | Stack | Lien |
|---|---|---|---|---|
| **Le Bon Coin** <br/> _plateforme d'annonces_ | Authentifier sans stocker de mot de passe en clair, et garantir qu'un utilisateur ne modifie que ses propres annonces. | **MongoDB → SQLite** migration : modèles et contrôleurs réécrits | Node.js · Express · JWT · Sequelize · React | [Code](https://github.com/Yohannkp/React-MERN-Project) · [Étude de cas](https://v0-junior-developer-portfolio-bay.vercel.app/projects/leboncoin-mern) |
| **ApplyFlow** <br/> _SaaS de suivi de candidatures_ | Ne plus perdre le fil de dizaines de candidatures dans des tableurs. | — | Next.js · TypeScript · Supabase · Tailwind CSS | [Démo](https://v0-apply-flow-saa-s-app.vercel.app/) · [Étude de cas](https://v0-junior-developer-portfolio-bay.vercel.app/projects/applyflow) |
| **Recommandation de films** <br/> _base de graphes_ | Naviguer les relations entre films, acteurs, réalisateurs et genres, avec une recherche tolérante aux erreurs. | — | Neo4j · FastAPI · React · Docker Compose | [Code](https://github.com/fayesarah555/movies-webapp) (projet d'équipe) · [Étude de cas](https://v0-junior-developer-portfolio-bay.vercel.app/projects/movies-database) |
| **CloudUs** <br/> _API de stockage cloud_ | Stocker des fichiers, gérer les quotas d'espace et facturer automatiquement. | — | Symfony · PHP · JWT · MySQL | [Code](https://github.com/Batyeste/CloudUs) (projet d'équipe) · [Étude de cas](https://v0-junior-developer-portfolio-bay.vercel.app/projects/cloudus-api) |
| **MiniSearch** <br/> _moteur de recherche interne_ | Retrouver l'information pertinente parmi des milliers de documents, vite, avec des filtres. | — | PostgreSQL · React · TypeScript · Supabase | [Démo](https://find-all-finder.lovable.app/) · [Étude de cas](https://v0-junior-developer-portfolio-bay.vercel.app/projects/minisearch) |

## Me contacter

- Portfolio : https://v0-junior-developer-portfolio-bay.vercel.app
- LinkedIn : [linkedin.com/in/yohannkp](https://www.linkedin.com/in/yohannkp)
- E-mail : yendiyohann@gmail.com

_Les anciens travaux de formation (TP, exercices de cours) sont archivés sur mon profil GitHub : ils restent consultables mais ne figurent pas ici._
