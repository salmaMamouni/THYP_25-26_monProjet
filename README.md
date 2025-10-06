 Mini Bibliothèque Numérique
 Contexte du projet:

L’objectif de ce projet est de concevoir une mini bibliothèque numérique capable de gérer, décrire et consulter des documents numériques tels que des livres articles ou fichiers PDF.

L’application permet à un utilisateur d’ajouter des documents d’y associer des métadonnées (informations descriptives comme la date, la catégorie, la langue, etc.) et de les afficher via une interface web simple.

 Objectifs:

Créer un petit système de gestion de documents 

Stocker les informations dans une base SQL relationnelle

Décrire les documents avec des métadonnées RDF/Turtle

Fournir une API PHP pour accéder aux données

Afficher les résultats en JavaScript


 Diagramme entité–relation (ER):

Ce diagramme représente la structure logique de la bibliothèque :

UTILISATEUR : gère la bibliothèque et ajoute des documents.

DOCUMENT : correspond à un livre ou un fichier.

METADONNEE : contient les informations descriptives du document.

Les relations indiquent qu’un utilisateur peut ajouter plusieurs documents, et qu’un document peut avoir plusieurs métadonnées.

erDiagram:
    UTILISATEUR ||--o{ DOCUMENT : "ajoute"
    DOCUMENT    ||--o{ METADONNEE : "possède"

    UTILISATEUR {
        int id
        string nom
        string email
    }
    DOCUMENT {
        int id
        string titre
        string auteur
        string type
        string langue
        text contenu
    }
    METADONNEE {
        int id
        string cle
        string valeur
    }

 Technologies utilisées:
SQL	Création des tables et relations entre entités
RDF / Turtle	Description sémantique des documents et métadonnées
PHP	API pour récupérer les données depuis la base
JavaScript	Affichage dynamique côté navigateur
Mermaid	Diagramme entité–relation dans le README
HTML/CSS	Structure et présentation de la page web
