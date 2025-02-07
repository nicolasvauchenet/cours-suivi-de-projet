# 3. Préparer le déploiement d’une application sécurisée

Avant la mise en production d’une application, il est essentiel d’effectuer une série de tests pour garantir son bon
fonctionnement et sa sécurité. La qualité du code et sa robustesse sont vérifiées grâce à des plans de tests rigoureux
et des environnements dédiés.

---

## 3.9 Préparer et exécuter les plans de tests d’une application

Les tests permettent d’identifier d’éventuelles anomalies, d’améliorer la fiabilité de l’application et de garantir une
expérience utilisateur optimale.

### 3.9.1 Le plan de tests couvre l'ensemble des fonctionnalités retenues pour l’application

Un plan de tests bien structuré définit l’ensemble des cas d’usage à tester pour vérifier la conformité de
l’application. Il comprend des tests unitaires, des tests fonctionnels, des tests d’intégration et des tests de
sécurité.  
**Exemple** : Pour une application e-commerce, le plan de tests inclut des scénarios comme la gestion du panier, le
paiement sécurisé et l’authentification des utilisateurs.

### 3.9.2 Un environnement de tests est créé

L’environnement de tests doit être indépendant de l’environnement de production et contenir des données fictives. Il
permet d’effectuer les tests en toute sécurité, sans impacter les utilisateurs réels.  
**Exemple** : Une base de données de test est utilisée avec des jeux de données anonymisées pour simuler des
transactions sans affecter les données de production.

### 3.9.3 L’intégralité des tests exécutés est conforme au plan de tests défini

Chaque test défini dans le plan doit être exécuté de manière méthodique et les résultats doivent être comparés aux
attentes. Les tests automatisés permettent de s’assurer qu’aucune régression n’est introduite.  
**Exemple** : Une suite de tests automatisés avec PHPUnit (PHP), Jest (JavaScript) ou PyTest (Python) est exécutée après
chaque mise à jour du code.

### 3.9.4 Les résultats obtenus sont cohérents avec les résultats attendus

Chaque test doit produire un résultat conforme à ce qui est prévu dans le cahier des charges. Si des écarts sont
détectés, ils doivent être analysés et corrigés avant la mise en production.  
**Exemple** : Lors d’un test de connexion utilisateur, une tentative avec des identifiants incorrects doit afficher un
message d’erreur spécifique et empêcher l’accès à l’application.

### 3.9.5 Le plan de tests tient compte des évolutions technologiques et des problèmes de sécurité liés aux tests logiciels

Le plan de tests doit être régulièrement mis à jour pour s’adapter aux nouvelles technologies et aux menaces de sécurité
émergentes. Des tests de sécurité doivent être intégrés pour prévenir les failles potentielles.  
**Exemple** : Une analyse statique de code est réalisée pour détecter des vulnérabilités telles que les injections SQL
ou les failles XSS, en utilisant des outils comme SonarQube ou OWASP ZAP.

---

## 3.10 Préparer et documenter le déploiement d’une application

Avant de mettre une application en production, il est essentiel de formaliser le processus de déploiement pour garantir
une transition fluide et reproductible.

### 3.10.1 La procédure de déploiement est rédigée

La documentation du processus de déploiement permet aux équipes techniques d’effectuer les mises en production en
suivant un protocole précis, évitant ainsi les erreurs humaines.  
**Exemple** : Une procédure écrite décrit les étapes à suivre pour déployer une application Symfony, incluant la mise à
jour de la base de données, le redémarrage des services et la gestion des permissions.

### 3.10.2 Les scripts de déploiement sont écrits et documentés

L’automatisation du déploiement via des scripts permet de réduire les erreurs et d’accélérer la mise en production.  
**Exemple** : Un script Bash ou Ansible est mis en place pour déployer l’application sur un serveur distant, incluant
l’installation des dépendances et la configuration des variables d’environnement.

### 3.10.3 Les environnements de tests sont définis et la procédure d’exécution des tests d’intégration, système et d’acceptation client est rédigée

Un environnement de préproduction est utilisé pour exécuter les tests avant le déploiement final en production. Ces
tests permettent de valider que l’ensemble du système fonctionne comme prévu.  
**Exemple** : Un serveur de staging est mis en place avec une copie des données de production anonymisées pour valider
la compatibilité des mises à jour avant leur déploiement.

### 3.10.4 Le système de veille permet de suivre les évolutions technologiques et les problématiques de sécurité liées au déploiement d’une application

Une veille technologique est réalisée pour identifier les nouvelles pratiques en matière de déploiement et de
sécurité.  
**Exemple** : Une équipe suit les mises à jour des outils de déploiement comme Docker et Kubernetes pour s’assurer
qu’aucune faille de sécurité n’est exploitée.

---

## 3.11 Contribuer à la mise en production dans une démarche DevOps

L’approche DevOps vise à automatiser les processus de développement, de test et de déploiement pour améliorer la qualité
logicielle et accélérer les cycles de livraison.

### 3.11.1 Les outils de qualité de code sont utilisés

Des outils d’analyse statique permettent de détecter les erreurs potentielles et d’assurer la maintenabilité du code.  
**Exemple** : SonarQube est utilisé pour analyser la complexité du code et détecter les vulnérabilités.

### 3.11.2 Les outils d’automatisation de tests sont utilisés

Les tests doivent être exécutés automatiquement à chaque modification du code pour éviter les régressions.  
**Exemple** : GitHub Actions ou GitLab CI/CD exécutent des tests PHPUnit après chaque commit sur la branche principale.

### 3.11.3 Les scripts d’intégration continue s’exécutent sans erreur

L’intégration continue permet de tester automatiquement l’application après chaque modification du code.  
**Exemple** : Un pipeline CI/CD est mis en place pour exécuter les tests unitaires et fonctionnels avant de valider une
mise à jour.

### 3.11.4 Le serveur d’automatisation est paramétré pour les livrables et les tests

Un serveur d’automatisation est utilisé pour exécuter les tâches de compilation, de test et de déploiement.  
**Exemple** : Jenkins ou GitLab Runner est configuré pour exécuter les tests et générer des artefacts de déploiement.

### 3.11.5 Les rapports de l’Intégration Continue sont interprétés

Les résultats des tests et des analyses de qualité doivent être examinés pour identifier les erreurs avant de passer en
production.  
**Exemple** : Un rapport de couverture de code indique quelles parties du code ne sont pas suffisamment testées et
nécessitent des ajustements.

### 3.11.6 La documentation technique des différents outils est comprise, en langue française ou anglaise

La compréhension des documentations officielles est essentielle pour utiliser efficacement les outils DevOps.  
**Exemple** : Un ingénieur DevOps consulte la documentation officielle de Docker pour optimiser le déploiement des
conteneurs.

### 3.11.7 La démarche structurée de résolution de problème est adaptée en cas de dysfonctionnement

Lorsqu’une erreur survient en production, une méthodologie de diagnostic est appliquée pour identifier rapidement la
cause et y remédier.  
**Exemple** : En cas de plantage d’un service, les logs sont analysés pour identifier la cause du problème et proposer
une solution rapide.

### 3.11.8 Le système de veille permet de suivre les évolutions technologiques et les problématiques de sécurité liées à la démarche DevOps

Une veille régulière permet d’anticiper les changements et de maintenir une infrastructure sécurisée et performante.  
**Exemple** : L’équipe suit les évolutions des pratiques DevOps via des conférences comme KubeCon ou DevOps World.
