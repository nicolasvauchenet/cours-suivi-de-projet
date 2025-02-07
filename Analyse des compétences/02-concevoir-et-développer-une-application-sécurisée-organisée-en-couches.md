# 2. Concevoir et développer une application sécurisée organisée en couches

Une architecture logicielle en couches permet d’assurer la modularité, la maintenabilité et la sécurité d’une
application en séparant les préoccupations métier, de présentation et de persistance.

---

## 2.5 Analyser les besoins et maquetter une application

Avant de commencer le développement, il est essentiel d’analyser les besoins des utilisateurs et de définir des
maquettes pour visualiser l’application.

### 2.5.1 Les besoins recensés couvrent l'ensemble des exigences utilisateur exprimées dans le cahier des charges

L’analyse des besoins repose sur des échanges avec les parties prenantes pour s’assurer que toutes les fonctionnalités
essentielles sont bien prises en compte.  
**Exemple** : Lors de la conception d’un logiciel de gestion des tâches, on identifie que les utilisateurs veulent une
gestion de priorités, un système de rappels et un partage des tâches avec d’autres utilisateurs.

### 2.5.2 Les maquettes sont réalisées conformément au cahier des charges en langue française ou anglaise

Les maquettes UI/UX doivent refléter les exigences décrites dans le cahier des charges et tenir compte de l’expérience
utilisateur.  
**Exemple** : Un designer utilise Figma ou Adobe XD pour créer des maquettes interactives qui seront validées par le
client.

### 2.5.3 L’enchaînement des maquettes est formalisé par un schéma

Le parcours utilisateur (user flow) est modélisé pour représenter l’enchaînement logique des écrans et interactions.  
**Exemple** : Pour une application de commerce en ligne, un schéma représente les étapes allant de la sélection d’un
produit au paiement final.

### 2.5.4 Le dossier de conception est structuré, en conformité avec la démarche de conception

Le dossier de conception regroupe les documents relatifs aux spécifications fonctionnelles, maquettes et règles de
gestion.  
**Exemple** : Un document Word ou un wiki Confluence rassemble toutes les informations nécessaires au développement.

---

## 2.6 Définir l’architecture logicielle d’une application

L’architecture d’une application définit sa structure logicielle, ses composants et leurs interactions.

### 2.6.1 Définir l’architecture logicielle en identifiant les Framework et ORM à utiliser

Le choix du framework et de l’ORM doit être adapté aux besoins fonctionnels et techniques du projet.  
**Exemple** : Pour une application Symfony, l’ORM Doctrine est choisi pour interagir avec la base de données.

### 2.6.2 Adapter l’architecture logicielle aux besoins des utilisateurs et à la stratégie de sécurité selon les recommandations de l’ANSSI

L’architecture doit intégrer des mesures de sécurité dès la conception, en tenant compte des recommandations
officielles.  
**Exemple** : Pour protéger une API REST, on applique les bonnes pratiques de l’ANSSI, comme l’authentification forte et
le chiffrement des communications via HTTPS.

### 2.6.3 Utiliser les patrons de conception (design patterns) et les patrons de sécurité (Security pattern)

Les design patterns assurent une structure de code flexible et évolutive, tandis que les security patterns préviennent
les vulnérabilités courantes.  
**Exemple** : L’utilisation du pattern Factory permet de centraliser la création d’objets et de limiter les
instanciations directes, renforçant ainsi la maintenabilité du code.

---

## 2.7 Concevoir et mettre en place une base de données relationnelle

Une base de données bien conçue garantit la cohérence et la sécurité des données manipulées par l’application.

### 2.7.1 Le schéma conceptuel respecte les règles du relationnel

La modélisation des données suit les principes de la normalisation pour éviter les redondances et assurer une bonne
organisation.  
**Exemple** : Dans un système de gestion de commandes, une relation `Commande` - `Client` est modélisée en respectant
les règles de normalisation.

### 2.7.2 Le schéma physique est conforme aux besoins exprimés dans le cahier des charges

Le schéma physique représente la structure finale de la base avec la définition des tables, types de données et
contraintes.  
**Exemple** : Une table `Utilisateurs` contient des colonnes `id`, `nom`, `email`, avec des contraintes `NOT NULL` et
`UNIQUE` sur `email`.

### 2.7.3 Les règles de nommage ont été respectées

Les conventions de nommage doivent être cohérentes et respectées pour assurer la lisibilité du modèle de données.  
**Exemple** : On adopte une convention `snake_case` pour nommer les colonnes (`date_creation` au lieu de
`dateCreation`).

### 2.7.4 L’intégrité, la sécurité et la confidentialité des données sont assurées

Des mécanismes comme les contraintes d’intégrité, l’authentification et le chiffrement doivent être mis en place.  
**Exemple** : Une base de données PostgreSQL chiffre les mots de passe avec `bcrypt` avant de les stocker.

### 2.7.5 La base de données de test est créée avec un jeu d’essai complet et peut être restaurée en cas d’incident

Un environnement de test avec des données fictives permet de valider le bon fonctionnement de l’application.  
**Exemple** : Une base SQLite est utilisée pour exécuter des tests unitaires sans impacter la base de production.

### 2.7.6 La documentation technique des bases de données est comprise, en langue française ou anglaise

Une bonne documentation permet aux développeurs et administrateurs de comprendre la structure et l’usage de la base de
données.  
**Exemple** : Un fichier `schema.sql` documente la structure de la base et les relations entre les tables.

---

### 2.8 Développer des composants d’accès aux données SQL et NoSQL

L'accès aux bases de données est un élément clé du développement d'une application. Que ce soit avec une base SQL (
relationnelle) ou NoSQL (non relationnelle), les bonnes pratiques doivent être respectées pour garantir la cohérence, la
sécurité et les performances.

#### 2.8.1 Les traitements relatifs aux manipulations des données répondent aux fonctionnalités décrites dans le dossier de conception

Les opérations sur les données doivent respecter les exigences du projet, assurer l'intégrité des informations et
optimiser les performances.  
**Exemple** : Dans une application de gestion de commandes, un composant d’accès aux données doit permettre de récupérer
les commandes par client, en optimisant les requêtes pour éviter les performances médiocres.

#### 2.8.2 Les cas d'exception sont pris en compte

Toute erreur pouvant survenir lors de l'accès aux données doit être anticipée et gérée proprement pour éviter les
comportements indésirables.  
**Exemple** : Une tentative d'accès à une base SQL dont la connexion échoue doit renvoyer un message clair et ne pas
planter l'application.

#### 2.8.3 L'intégrité et la confidentialité des données sont maintenues

L’application doit garantir que les données ne sont ni altérées involontairement ni accessibles par des personnes non
autorisées.  
**Exemple** : Les mots de passe stockés dans la base de données sont hashés avec `bcrypt` au lieu d’être enregistrés en
clair.

#### 2.8.4 Les conflits d'accès aux données sont gérés

Lorsqu’un même enregistrement peut être modifié par plusieurs utilisateurs, il faut éviter les conflits et garantir la
cohérence des données.  
**Exemple** : Une stratégie d’optimistic locking est mise en place avec un champ `version` pour s’assurer que deux
utilisateurs ne modifient pas simultanément la même donnée sans être avertis.

#### 2.8.5 Toutes les entrées sont contrôlées et validées dans les composants serveurs sécurisés

Les entrées utilisateur doivent être filtrées et validées avant toute manipulation pour éviter les failles de sécurité
comme les injections SQL.  
**Exemple** : Une API REST valide les paramètres d’une requête avant d’exécuter une requête SQL pour empêcher toute
tentative d’injection malveillante.

#### 2.8.6 Les tests unitaires et de sécurité sont associés à chaque composant

Chaque composant d’accès aux données doit être couvert par des tests pour garantir son bon fonctionnement et prévenir
les failles de sécurité.  
**Exemple** : Des tests unitaires sont écrits avec PHPUnit pour vérifier que les requêtes renvoient bien les résultats
attendus.

#### 2.8.7 La démarche structurée de résolution de problème est adaptée en cas de dysfonctionnement

En cas d'erreur, une approche méthodique permet d'identifier rapidement la cause du problème et de le corriger.  
**Exemple** : Une base NoSQL comme MongoDB devient soudainement inaccessible ; les logs sont analysés pour identifier la
cause du problème (problème réseau, surcharge, mauvaise configuration).

#### 2.8.8 Le système de veille permet de suivre les évolutions technologiques et les problématiques de sécurité liées aux bases de données SQL et NoSQL

Le paysage des bases de données évolue rapidement ; il est essentiel de rester informé des nouvelles versions, des
meilleures pratiques et des nouvelles menaces.  
**Exemple** : Une équipe suit les mises à jour de PostgreSQL et MongoDB pour s’assurer qu’elles incluent des
optimisations de performance et des correctifs de sécurité.
