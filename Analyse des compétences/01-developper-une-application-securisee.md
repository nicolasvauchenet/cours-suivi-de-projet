# Développer une application sécurisée

## 1.1 Installer et configurer son environnement de travail en fonction du projet

Avant de commencer un projet de développement, il est essentiel d'installer et de configurer un environnement adapté
pour assurer un travail efficace et sécurisé.

### 1.1.1 Les outils de développement nécessaires sont installés

Un environnement de développement comprend un éditeur de code (VS Code, PHPStorm, IntelliJ), des interpréteurs ou
compilateurs (PHP, Node.js, Python), ainsi que des gestionnaires de dépendances (Composer, npm, pip).  
**Exemple** : Un développeur PHP installe PHP 8.2, Composer et un serveur local comme Symfony CLI ou Docker avec Nginx
et MySQL.

### 1.1.2 Les outils de gestion des versions et de collaboration sont installés

Un outil comme Git permet de versionner le code et d'assurer une collaboration fluide. Les plateformes comme GitHub,
GitLab ou Bitbucket permettent le travail en équipe.  
**Exemple** : Un projet est géré sur GitHub, avec des branches distinctes pour le développement, les fonctionnalités et
les correctifs.

### 1.1.3 Les conteneurs implémentent les services requis

L’utilisation de Docker permet d'assurer la compatibilité des environnements entre les développeurs. Chaque service (
base de données, serveur web, cache) est exécuté dans un conteneur distinct.  
**Exemple** : Un projet Symfony utilise Docker avec des services MySQL, Redis et Nginx.

### 1.1.4 La documentation technique de l’environnement de travail est comprise, en langue française ou anglaise

Un développeur doit pouvoir lire et comprendre la documentation des outils qu'il utilise, qu'elle soit en français ou en
anglais.  
**Exemple** : Lire la documentation officielle de Symfony pour configurer correctement les services requis.

---

## 1.2 Développer des interfaces utilisateur

L’interface utilisateur (UI) est essentielle pour offrir une expérience agréable et accessible.

### 1.2.1 L’interface est conforme au dossier de conception

L’UI doit correspondre aux maquettes validées en amont et respecter l'expérience utilisateur (UX).  
**Exemple** : Un développeur intègre une interface avec Bootstrap en respectant les maquettes fournies par un designer.

### 1.2.2 L’interface s’adapte au type d’utilisation de l’application et notamment à la taille, au type et à la disposition du support

L’adaptabilité aux différents écrans (responsive design) est indispensable.  
**Exemple** : Un site web ajuste son affichage grâce à CSS Grid et Flexbox pour s’adapter aux mobiles et tablettes.

### 1.2.3 La charte graphique est respectée

Les couleurs, typographies et styles définis doivent être respectés.  
**Exemple** : Une application mobile utilise la palette de couleurs et les composants UI spécifiés dans le design system
de l’entreprise.

### 1.2.4 La réglementation en vigueur est respectée

L’UI doit se conformer aux normes d’accessibilité (WCAG) et respecter les obligations légales (RGPD).  
**Exemple** : Une application propose un mode contrasté pour les malvoyants et un consentement explicite pour
l'utilisation des cookies.

### 1.2.5 Le code est documenté

Chaque composant UI doit être documenté pour faciliter sa maintenance.  
**Exemple** : Un fichier README explique l’utilisation des composants React d’un projet.

### 1.2.6 Les tests unitaires ont été réalisés pour les composants concernés

Chaque composant doit être testé individuellement pour éviter les régressions.  
**Exemple** : Un développeur exécute des tests Jest pour valider le bon fonctionnement des composants React.

### 1.2.7 Le jeu d’essai fonctionnel est complet

Un ensemble de scénarios de test est préparé pour vérifier le bon comportement de l’interface.  
**Exemple** : Un QA teste les différents parcours utilisateur sur un formulaire de connexion.

### 1.2.8 Les tests de sécurité sont réalisés

Les failles courantes (XSS, CSRF) doivent être prévenues et testées.  
**Exemple** : Un test de pénétration est réalisé pour identifier les potentielles injections malveillantes.

### 1.2.9 La documentation technique des interfaces utilisateur est comprise, en langue française ou anglaise

Un développeur doit être capable de lire les spécifications techniques des interfaces.  
**Exemple** : Comprendre la documentation des Web Components pour les intégrer correctement dans un projet.

### 1.2.10 La démarche structurée de résolution de problème est adaptée en cas de dysfonctionnement

Une approche logique et méthodique permet d'identifier et résoudre les erreurs rapidement.  
**Exemple** : Un bug sur un menu déroulant est reproduit en local, analysé via les DevTools et corrigé.

### 1.2.11 Le système de veille permet de suivre les évolutions technologiques et les problématiques de sécurité en lien avec les interfaces utilisateur

Une veille régulière permet d’adopter les meilleures pratiques.  
**Exemple** : Un développeur suit les mises à jour de Bootstrap et Material UI pour optimiser ses interfaces.

---

## 1.3 Développer des composants métier

Les composants métier contiennent la logique applicative et doivent être robustes et sécurisés.

### 1.3.1 Les bonnes pratiques de la programmation orientée objet (POO) sont respectées

L’application suit des principes comme SOLID pour une meilleure maintenabilité.  
**Exemple** : Un service de gestion des utilisateurs est structuré selon le principe de responsabilité unique (SRP).

### 1.3.2 Les composants métier sont sécurisés

Les accès aux données et traitements doivent être protégés.  
**Exemple** : Une API filtre les entrées utilisateurs pour éviter les injections SQL.

### 1.3.3 Les règles de nommage sont conformes aux normes de qualité de l'entreprise

Un code lisible et standardisé améliore la compréhension.  
**Exemple** : Les méthodes suivent la convention `camelCase` et les classes `PascalCase`.

### 1.3.4 Le code source est documenté

Des commentaires et une documentation claire facilitent la maintenance.  
**Exemple** : Une classe métier contient des docstrings explicites décrivant ses méthodes.

### 1.3.5 Les traitements répondent aux fonctionnalités décrites dans le dossier de conception

Les règles métier sont correctement implémentées.  
**Exemple** : Une commande client est validée uniquement si le stock est suffisant.

### 1.3.6 Les tests unitaires sont réalisés

Chaque méthode critique doit être testée isolément.  
**Exemple** : Un test PHPUnit vérifie le comportement d’un calcul de prix.

### 1.3.7 Les tests de sécurité sont réalisés

Les composants critiques doivent être testés pour éviter toute faille.  
**Exemple** : Un pentest est effectué pour s’assurer qu’un service d’authentification est sécurisé.

### 1.3.8 La démarche structurée de résolution de problème est adaptée en cas de dysfonctionnement

L’identification rapide des causes permet de limiter les impacts.  
**Exemple** : Un bug de performance est analysé avec un profilage du code.

### 1.3.9 Le système de veille permet de suivre les évolutions technologiques et les problématiques de sécurité en lien avec les composants métier

Une veille technique régulière permet d’anticiper les évolutions et améliorations possibles.  
**Exemple** : Un développeur suit les changements apportés aux frameworks et bibliothèques utilisées dans son projet.

---

## 1.4 Contribuer à la gestion d’un projet informatique

Le développement d'une application ne se limite pas à l'écriture du code. Il est essentiel d'assurer une bonne gestion
du projet pour respecter les délais, garantir la qualité et optimiser le travail d'équipe.

### 1.4.1 Les tâches de conception et de développement sont planifiées en fonction du délai défini

Une bonne planification permet d'assurer une progression fluide du projet et d'anticiper les risques de retard.  
**Exemple** : Un projet est découpé en sprints de 2 semaines selon la méthode Scrum. Chaque sprint inclut des tâches
bien définies avec des objectifs clairs.

### 1.4.2 Le suivi des tâches est mis en rapprochement avec la planification, les éventuels retards sont identifiés et les acteurs concernés sont alertés

L’avancement du projet est comparé aux prévisions pour détecter les écarts et ajuster les priorités.  
**Exemple** : Un chef de projet utilise un tableau Kanban (Jira, Trello) pour visualiser l’état d’avancement des tâches
et identifier celles en retard.

### 1.4.3 Les procédures qualité sont mises en œuvre

L’adoption de standards et de processus de contrôle qualité garantit un développement fiable et maintenable.  
**Exemple** : Chaque mise à jour du code est soumise à une revue par les pairs avant d’être fusionnée dans la branche
principale.

### 1.4.4 L'environnement de développement défini est en adéquation avec l’architecture du projet

L’architecture logicielle du projet influence le choix des outils et configurations.  
**Exemple** : Une application en microservices nécessite un environnement Docker avec plusieurs conteneurs dédiés aux
différents services.

### 1.4.5 Les outils collaboratifs sont choisis en fonction de la méthode de développement

Le choix des outils de communication et de gestion du travail dépend de la méthodologie adoptée (Agile, DevOps, cycle en
V).  
**Exemple** : Une équipe Agile utilise Slack pour la communication instantanée et Confluence pour la documentation
technique.

### 1.4.6 Les comptes rendus de réunion sont structurés, rédigés dans un style adapté, dans le respect des règles orthographiques et grammaticales, et contiennent les informations nécessaires

Un compte rendu bien rédigé permet de suivre les décisions prises et les actions à entreprendre.  
**Exemple** : Après chaque réunion hebdomadaire, un résumé est envoyé à l’équipe, mentionnant les points discutés, les
décisions prises et les tâches attribuées.
