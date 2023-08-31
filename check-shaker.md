# Check Shaker

## Présentation

Check Shaker est une application de gestion de checklists.
Elle est axée autour de 3 fonctionnalités principales :

- création de templates de checklist accessibles au sein d'une bibliothèque de templates
- partage et complétion de checklist entre les utilisateurs
- contrôle et archivage des checklists

L'objectif principal de l'application est de permettre de mettre en oeuvre des checklists partagées afin de valider, par exemple, un déploiement dont les différentes étapes de validation sont réparties entre les développeurs, les devops, les PO, le marketing, la Direction, etc.

Chaque checklist serait instanciée à partir d'un template présent dans la bibliothèque. Les templates seront construits autour de composants de validation.

Les composants pourront être :

- une case à cocher,
- une valeur numérique avec des limites optionnelles (par exemple la taille d'un bundle),
- une liste déroulante,
- une zone de texte.

Chaque composant comportera optionellement ses conditions de validation afin de pouvoir définir si une checklist est valide ou non.

Par exemple, un composant "Lighthouse Score" de type numérique ne sera valide que si sa valeur minimum définie est supérieure à 95.

Une fois le template créé, il sera possible de l'instancier et de le partager.
La checklist aura un "propriétaire" (celui qui l'a créée) et un ou plusieurs "responsables" (en charge de la compléter).

Un responsable pourra transférer la responsabilité à un autre responsable.

Une fois la checkist valide, le propriétaire pourra l'archiver et conserver.

La checklist enregistrée sera en readonly, pourra être désarchivée selon le rôle de l'utilisateur.
Elle conservera ces informations ainsi que les changements de chaque composant et l'utilisateur qui les aura réalisés.

Les templates seront organisées par catégorie(s).
Les checklists possèderont en plus des tags et un état (pending, in progress, valid, archived).

Il sera possible de rechercher les checklists par croisement multiple des données suivantes :

- catégorie
- tags
- état
- propriétaire
- responsable
- date range

Dans les idées en vrac :

- un chat pourra être attaché à chaque checklist pour échanger si besoin.
- les checklists pourraient comporter des étapes de validation intermédiaires
- etc.

## Technos à mettre en oeuvre

- travail collaboratif / git / review / pair et mob
- authentification des utilisateurs
- roles
- base de données (sql, nosql, temps réel type supabase/firebase ?)
- notifications
- drag and drop pour la composition de template à partir de composants
- formulaires
- champs de recherche
- UX / UI
- themes
- accessibilité
- internationalisation
- TU et e2e

## Roadmap (?)

- todolist simple
- authentification des utilisateurs
- rattachement todolist à utilisateur
- création de groupe d'utilisateurs
- création de composants pour les todolists
- instanciation de checklist avec des composants
- validation de checklist
- responsables de checklist
- recherche de checklist par responsable
- template de checklist
- bibliothèque de checklists
- recherche de checklists multi critères
- notifications
- état de checklists
- gestion des roles

Pour finir, ceci est une proposition non impérative donc ouverte à toute bonne idée !!!
N'hésitez pas..
