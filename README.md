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
  - **Many To Many** :
- L'interface du site permet d'associer et de dissocier graphiquement ces entités, avec une page pour les Media (Film et Serie), une page pour les Actor, une page pour le profil Utilisateur, et des listes et des ratings intégrées dans les pages du site.
- Nous avons aussi implémenté des fonctionnalités CRUD en suivant notre **logique métier** spécifique : 
  - Création de profil utilisateur 
  - Ajout & Suppresion de Rating
  - Ajout et Suppresion de Media à des listes 
  - Modification des informations Utilisateur
  - (Création de listes personnalisées)

---

## Grille d'évaluation

### Fonctionnalités : **5 points**

| Critère | Évaluation | Justification |
|---------|------------|---------------|
| L'application contient bien les fonctionnalités demandées. | ✅ | Les fonctionnalités demandées sont implémentées : gestion des entités, logique métier, associations graphiques. |
| L'application permet d'insérer, mettre à jour, supprimer, chercher une entité en BDD. | ✅ | Les opérations CRUD sont intégrées pour chaque entité avec des formulaires validés. |
| L'application permet de lier deux entités en BDD. | ✅ | Les relations entre entités (1-1, 1-N, N-N) sont établies et manipulables via l'interface. |
| L'application permet, pour une entité donnée, de créer un lien à une autre entité en BDD. | ✅ | Des interfaces permettent de créer et dissocier des liens entre entités avec des contrôles adaptés. |

### Technique : **5 points**

| Critère | Évaluation | Justification |
|---------|------------|---------------|
| L'application utilise le design pattern MVC pour chaque fonctionnalité. &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| ✅ | Chaque fonctionnalité suit l'architecture MVC avec une séparation claire des couches. |
| Les contrôleurs utilisent les méthodes HTTP : GET, POST, PUT, DELETE. | ✅ | Les contrôleurs exploitent les méthodes HTTP en fonction des actions (exemple : création avec POST, suppression avec DELETE). |
| Chaque vue manipule des données transmises par son contrôleur. | ✅ | Les vues affichent dynamiquement les données transmises via les modèles des contrôleurs. |

### Qualité : **4/5 points**

| Critère | Évaluation | Justification |
|---------|------------|---------------|
| L'application est jolie / utilise un framework CSS. | ✅ | Tailwind CSS a été utilisé pour créer une interface utilisateur minimaliste et simple à utiliser pour garantir la meilleur expérience utilisateur possible. |
| Le code source est livré dans un repo GitHub/GitLab. Il est de bonne qualité. &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| ✅ | Le projet est hébergé sur GitHub avec un code organisé et des commentaires explicatifs. |
| Le repo comporte des commits réguliers de chaque membre du groupe. | ⚠️ | Bien que les commits soient réguliers, ils proviennent principalement de quelques membres actifs. |

---

## Conclusion

### Points forts
- Toutes les fonctionnalités demandées ont été intégrées avec succès.  
- L'application respecte l'architecture MVC et utilise pleinement les méthodes HTTP.  
- Les relations entre entités sont bien gérées et manipulables graphiquement.  

### Points à améliorer
- Une meilleure répartition des tâches au sein de l'équipe aurait permis d'équilibrer les contributions (commits Git).  

### Auto-évaluation finale : **14/15**
