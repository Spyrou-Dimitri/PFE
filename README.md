Plateforme de Gestion et Coordination d'Équipe E-Sport
1. Contexte de l'application
Cette plateforme est une application web conçue pour les équipes e-sport compétitives. Le but est de centraliser tous les outils de gestion d'équipe, améliorer la communication interne et professionnaliser l'organisation des structures e-sport de niveau amateur à semi-professionnel.
L'application répond à une problématique concrète : actuellement, les équipes utilisent des outils disparates et non adaptés (Discord pour la communication, Google Sheets pour les plannings, Trello pour les tâches, etc.). Cette fragmentation entraîne une perte d'information, des difficultés de coordination et un manque de visibilité sur l'organisation globale.
Le projet propose une solution unique et centralisée, spécifiquement pensée pour les besoins des structures e-sport compétitives, en offrant :

Une gestion complète du roster avec attribution de rôles
Un système de disponibilités pour faciliter la planification
Un calendrier centralisé pour les scrims, matchs officiels et jours de repos
Une checklist pré-match pour assurer la préparation
Un système de devoirs assignés par le coach
Un suivi des objectifs individuels et collectifs
Une communication interne en temps réel
Un historique des résultats et performances

2. Gestion des accès (rôles et permissions)
Rôles
Coach : gestion complète de l'équipe (roster, événements, devoirs, objectifs, validation des tâches, accès au dashboard complet).
Joueur : accès opérationnel et consultation (disponibilités, devoirs assignés, objectifs personnels, chat, calendrier personnel, résultats), avec des droits limités.
Staff (optionnel) : accès partiel selon les besoins (consultation du calendrier, accès au chat, suivi des résultats).
Principe
Le rôle détermine :

Ce qui est visible (dashboards, sections, menus)
Ce qui est modifiable (événements, devoirs, objectifs)
Ce qui est validable (actions sensibles comme la validation des devoirs, suppression d'événements)

Exemples :

Un Joueur peut marquer un devoir comme complété, mais seul le Coach peut le valider définitivement.
Le Coach voit le dashboard complet avec statistiques d'équipe et vue globale des disponibilités ; le Joueur voit une version simplifiée centrée sur ses tâches personnelles.
Seul le Coach peut créer, modifier ou supprimer des événements du calendrier et attribuer des devoirs.

3. Personas et parcours utilisateurs
🎮 Thomas — Coach d'une équipe semi-professionnelle
Rôle : Coach
🧩 Parcours utilisateur 1 — Planifier un scrim d'entraînement
Thomas souhaite organiser un scrim contre une équipe adverse pour préparer un tournoi. Il se connecte à la plateforme, ouvre la rubrique "Calendrier", puis crée un nouvel événement de type "Scrim". Il sélectionne la date, l'heure, ajoute l'équipe adverse et des notes tactiques. Le système vérifie automatiquement les disponibilités des joueurs et signale si certains ne sont pas disponibles. Thomas enregistre l'événement et tous les joueurs reçoivent une notification.
🧩 Parcours utilisateur 2 — Attribuer des devoirs après un match
Après avoir analysé un match perdu, Thomas identifie des points d'amélioration. Il ouvre la section "Devoirs", crée une nouvelle tâche de type "Visionnage de replay" pour son ADC, définit une date limite et ajoute des commentaires sur les erreurs à corriger. Le joueur reçoit une notification instantanée et peut consulter le devoir depuis son dashboard personnel. Lorsque le joueur marque le devoir comme terminé, Thomas reçoit une notification et peut le valider après vérification.
🧩 Parcours utilisateur 3 — Suivre les objectifs de l'équipe
En début de mois, Thomas consulte le dashboard coach. Il voit la progression des objectifs collectifs (ex. "Atteindre 70% de winrate en scrim") et individuels de chaque joueur. Il identifie que certains objectifs ne progressent pas et décide d'organiser une réunion d'équipe pour ajuster la stratégie. Il peut directement créer un événement "Réunion" depuis cette vue.
🎮 Lucas — Joueur ADC
Rôle : Joueur
🧩 Parcours utilisateur 1 — Indiquer sa disponibilité pour la semaine
Lucas se connecte le dimanche soir pour mettre à jour ses disponibilités. Il ouvre la section "Disponibilités", sélectionne les jours où il ne sera pas disponible (mercredi pour un examen), et confirme. Le coach reçoit une notification du changement et peut adapter le planning des entraînements en conséquence.
🧩 Parcours utilisateur 2 — Compléter un devoir assigné
Lucas voit une notification indiquant qu'il a un nouveau devoir. Il ouvre son dashboard, consulte le devoir "Visionnage de replay" avec les commentaires du coach. Après avoir visionné le replay et noté ses erreurs, il marque le devoir comme complété et ajoute un commentaire sur ce qu'il a appris. Le coach reçoit une notification et peut valider le devoir.
🧩 Parcours utilisateur 3 — Vérifier le planning avant un match
Le jour d'un match officiel, Lucas ouvre la section "Calendrier" depuis son téléphone. Il consulte l'horaire exact, vérifie la checklist pré-match (setup vérifié, échauffement fait, stratégie revue) et coche les items au fur et à mesure. Il voit également que tous ses coéquipiers sont disponibles et que la checklist est presque complète.
4. Fonctionnalités (MVP)
4.1 Authentification et gestion des profils

Inscription et connexion sécurisée
Gestion du profil utilisateur
Attribution des rôles (Coach, Joueur, Staff)
Système de permissions basé sur les rôles

4.2 Gestion du roster

Création et modification des profils de joueurs
Attribution et modification des rôles
Affichage de la composition de l'équipe
Gestion des remplaçants
Suppression de membres (réservée au Coach)

4.3 Système de disponibilités

Interface de saisie des disponibilités par joueur (jour/semaine/mois)
Vue d'ensemble des disponibilités de toute l'équipe (Coach uniquement)
Notifications automatiques en cas de changement de disponibilité
Filtres par période et par joueur

4.4 Calendrier centralisé

Création, modification et suppression d'événements (réservé au Coach)
Types d'événements : Scrims, Matchs officiels, Jours de repos, Réunions
Code couleur par type d'événement
Vues multiples : journalière, hebdomadaire, mensuelle
Synchronisation avec les disponibilités (alerte si joueur indisponible)
Notifications automatiques pour les événements à venir

4.5 Checklist pré-match

Création de templates de checklist par le Coach
Items personnalisables (setup, échauffement, stratégie, etc.)
Validation des items par les joueurs
Suivi de la progression en temps réel
Historique des checklists complétées par match

4.6 Section résultats

Enregistrement des résultats de matchs (victoire/défaite)
Statistiques basiques : nombre de victoires, défaites, ratio
Historique complet des performances
Filtres par période, type de match (scrim/officiel), adversaire
Graphiques de progression (optionnel pour le MVP)

4.7 Système de devoirs

Création et attribution de devoirs par le Coach
Types de devoirs : Visionnage de replay, Entraînement spécifique, Théorie, Autre
Date limite et niveau de priorité
Attribution à un ou plusieurs joueurs
Marquage comme "complété" par le joueur
Validation et ajout de commentaires par le Coach
Notifications à chaque étape du processus

4.8 Suivi des objectifs

Définition d'objectifs individuels et collectifs par le Coach
Suivi de la progression (pourcentage ou étapes)
Dates d'échéance
Statuts : En cours, Complété, Échoué, Reporté
Historique des objectifs atteints

4.9 Communication interne

Chat en temps réel entre membres de l'équipe
Création de canaux de discussion (général, stratégie, off-topic)
Notifications instantanées de nouveaux messages
Historique complet des conversations
Mentions de joueurs (@pseudo)

4.10 Dashboards personnalisés
Dashboard Coach :

Vue d'ensemble de l'équipe (disponibilités, prochains événements)
Statistiques de performance récentes
Liste des devoirs en attente de validation
Progression des objectifs collectifs et individuels
Alertes (joueurs indisponibles, devoirs non complétés)
Actions rapides (créer événement, attribuer devoir, définir objectif)

Dashboard Joueur :

Vue personnelle (mes prochains événements, mes disponibilités)
Liste de mes devoirs (à faire, en attente de validation, validés)
Mes objectifs personnels et progression
Statistiques personnelles récentes
Notifications non lues
Accès rapide au chat et au calendrier

5. Technologies utilisées
Back end : Laravel 12
Front end : Laravel 12 - Tailwind css - javascript

Vite : Build tool et serveur de développement
Figma : Design et prototypage UI/UX
Git : Versioning du code
