# Auto-évaluation ShowTime

Barrouillet Margaux  
Chevillotte Thomas  
Garcia Anthony  
Soutric Tanguy  
  
  ING2 GSI Groupe 1

## Présentation

- Nous avons développé notre application ShowTime en utilisant **Spring Boot**, avec **Spring Data JPA**, **H2 Database** et **Thymeleaf**.

- Nous avons utlisé l'architecture **MVC** pour séparer le traitement des données et leur affichage.

- Notre modèle comporte **5 entités** différentes, avec des relations :
  - **Media** (séparée en 2 sous entités **Movie** et **TVShow**), modélisant les films et les séries affichées sur notre site
  - **MediaList**, modélisant toutes les listes présentes sur le site (détaillé dans les parties suivantes) 
  - **Actor**, représentant les Acteurs associés aux films et aux séries.
  - **Rating**, représentant les notes et les commentaires des utilisateurs pour les films et les séries.
  - **User**, représentant les comptes utilisateur
  
- Ces entités sont liés avec plusieurs relations : 
  - **One To One** : 
  - **One To Many** :
    - Media avec Rating, pour afficher les évaluations des utilisateurs pour ce Media.
    - MediaList avec User, pour afficher les Listes de chaque Utilisateur.
    - Rating avec User, pour afficher les évaluations de chaque Utilisateur.
  - **Many To Many** : 
    - Actor avec MediaList, pour afficher les Medias dans lequel l'Acteur à joué, et inversement pour afficher tous les Acteurs d'un Media.
    - Media avec MediaList, pour créer des Listes de Medias.
    
- L'interface du site permet d'associer et de dissocier graphiquement ces entités, avec une page pour les informations des Medias (Film et Serie), une page pour les informations des Actors, une page pour le profil Utilisateur, et des listes et des ratings intégrées dans les pages du site.
  
- Nous avons aussi implémenté des fonctionnalités CRUD en suivant notre **logique métier** spécifique : 
  - Création & Suppression de profil utilisateur 
  - Ajout & Suppresion de Rating
  - Ajout et Suppresion de Media à des listes 
  - Modification des informations Utilisateur
  - (Création de listes personnalisées) /// A DELETE DUCOUP

---

## Grille d'évaluation

### Fonctionnalités : **5 points**

- L'application contient bien les fonctionnalités demandées :  *5 entités, associations graphiques, logique métier de l'appliction.*
  
- L'application permet d'insérer, mettre à jour, supprimer, chercher une entité en BDD : *Création d'Utilisateur, modification des informations de connexion, barre de recherche de Media et d'Actor.*
  
- L'application permet de lier deux entités en BDD / permet, pour une entité donnée, de créer un lien à une autre entité en BDD : *Ajout de Rating, lié à un User et à un Media, ajout d'un Media à une Liste, lié à un User.*

### Technique : **5 points**

- L'application utilise le design pattern MVC pour chaque fonctionnalité : *Séparation de l'implémentation en 3 couches, Model, Vue et Controller.*
  
- Les contrôleurs utilisent les méthodes HTTP : GET, POST, PUT, DELETE : *Méthode Get pour afficher les pages et Post pour ajouter, supprimer et modifier des informations (préférées a Put et Delete pour éviter les erreurs et pouvoir vérifier avnt d'effectuer une action).*
  
- Chaque vue manipule des données transmises par son contrôleur : *les vues affichent uniquement les données transmises par les contrôleurs (listes de Media, détails d'Acteurs/de Media, informations de profil, résultats de recherche, etc.*

### Qualité : **4/5 points**

- L'application est jolie / utilise un framework CSS : *Tailwind CSS a été utilisé pour créer une interface utilisateur minimaliste et simple à utiliser pour garantir la meilleur expérience utilisateur possible.*
  
- Le code source est livré dans un repo GitHub/GitLab. Il est de bonne qualité : *Le projet est hébergé sur GitHub avec un code organisé (branches, packages, dossiers) et des commentaires explicatifs.*
  
- Le repo comporte des commits réguliers de chaque membre du groupe. | ⚠️ | *Bien que les commits soient réguliers, ils proviennent principalement de quelques membres actifs.*   // A EDIT MDR

---

## Grille d'évaluation

### Fonctionnalités : **5 points**

| Critère | Évaluation | Justification |
|---------|------------|---------------|
| L'application contient bien les fonctionnalités demandées. | ✅ | Les fonctionnalités demandées sont implémentées : gestion des entités, logique métier, associations graphiques. |
| L'application permet d'insérer, mettre à jour, supprimer, chercher une entité en BDD. | ✅ | Création d'Utilisateur, modification des informations de connexion, barre de recherche de Media et d'Actor. |
| L'application permet de lier deux entités en BDD. | ✅ | Les relations entre entités (1-1, 1-N, N-N) sont établies et manipulables via l'interface. |
| L'application permet, pour une entité donnée, de créer un lien à une autre entité en BDD. | ✅ | Ajout de Rating, lié à un User et à un Media. Ajout d'un Media à une Liste, lié à un User. |

### Technique : **5 points**

| Critère | Évaluation | Justification |
|---------|------------|---------------|
| L'application utilise le design pattern MVC pour chaque fonctionnalité. | ✅ | Chaque fonctionnalité suit l'architecture MVC avec une séparation en 3 couches Model, Vue et Controller. |
| Les contrôleurs utilisent les méthodes HTTP : GET, POST, PUT, DELETE. | ✅ | Les contrôleurs utilisent les méthodes Get pour afficher les pages et Post pour ajouter, supprimer et modifier des informations (préférées a Put et Delete pour éviter les erreurs et pouvoir vérifier avnt d'effectuer une action). |
| Chaque vue manipule des données transmises par son contrôleur. | ✅ | Les vues affichent uniquement les données transmises par les contrôleurs (listes de Media, détails d'Acteurs/de Media, informations de profil, résultats de recherche, etc. |

### Qualité : **4/5 points**

| Critère | Évaluation | Justification |
|---------|------------|---------------|
| L'application est jolie / utilise un framework CSS. | ✅ | Tailwind CSS a été utilisé pour créer une interface utilisateur minimaliste et simple à utiliser pour garantir la meilleur expérience utilisateur possible. |
| Le code source est livré dans un repo GitHub/GitLab. Il est de bonne qualité. | ✅ | Le projet est hébergé sur GitHub avec un code organisé (branches, packages, dossiers) et des commentaires explicatifs. |
| Le repo comporte des commits réguliers de chaque membre du groupe. | ⚠️ | Bien que les commits soient réguliers, ils proviennent principalement de quelques membres actifs. |

---

## Conclusion

### Points forts
- Toutes les fonctionnalités demandées ont été intégrées avec succès.  
- L'application respecte l'architecture MVC et utilise pleinement la BDD.  
- Chaque entité est visiellement dissociable des autres et facile à utliser.
- Nous avons utilisé l'[API TMDB](https://developer.themoviedb.org/reference/intro/getting-started) pour remplir notre base de données de films, de séries et d'acteurs.

### Points à améliorer
- Une meilleure répartition des tâches au sein de l'équipe aurait permis d'équilibrer les contributions (commits Git).    /// !!!!

### Auto-évaluation finale : **14/15**
