 Maquette complète des pages du CRM

## Projet

CRM pour entreprise d'entretien ménager avec :

* gestion clients
* gestion employés
* gestion interventions
* notifications automatiques
* paiements clients
* recrutement payant des candidats
* liste d'attente
* portail client
* portail employé
* portail candidat

---

# 1. Architecture générale

## Rôles utilisateurs

### A. Administrateur

Accès complet à tous les modules.

### B. Répartiteur / gestionnaire

Accès aux clients, employés, calendrier, interventions, notifications.

### C. Employé / préposé

Accès à son horaire, ses interventions, son profil, ses statuts, ses preuves de service.

### D. Client

Accès à son portail de suivi, factures, historique, notifications.

### E. Candidat

Accès à son inscription payante, son statut, ses documents, la liste d'attente.

---

# 2. Navigation principale

## Barre latérale CRM

1. Tableau de bord
2. Calendrier
3. Interventions
4. Clients
5. Employés
6. Candidats
7. Paiements
8. Notifications
9. Rapports
10. Paramètres

## Barre supérieure

* recherche globale
* bouton création rapide
* centre de notifications
* profil utilisateur
* sélecteur de rôle / succursale si nécessaire

---

# 3. Design system recommandé

## Palette

* bleu nuit : navigation, titres, zones système
* turquoise : actions principales, statuts positifs
* vert doux : disponible, payé, terminé
* jaune ambré : en attente, en route, attention
* rouge léger : retard, échec paiement, annulation
* gris clair : fonds de cartes

## Composants récurrents

* cartes KPI
* tableaux filtrables
* calendrier drag-and-drop
* fiches détaillées avec panneau latéral
* badges de statut
* boutons d'action rapide
* timeline d'activité
* modales de confirmation
* formulaires multi-étapes

---

# 4. Pages du CRM Admin

## PAGE 1. Tableau de bord principal

### Objectif

Donner une vue immédiate de l'activité du jour.

### Sections

#### 1. En-tête

* titre : Tableau de bord
* date du jour
* sélecteur de période : aujourd'hui / semaine / mois
* bouton : Nouvelle intervention
* bouton : Nouveau client

#### 2. KPI haut de page

* interventions aujourd'hui
* employés disponibles
* employés en route
* services terminés
* paiements reçus aujourd'hui
* candidats payés en attente
* taux de ponctualité
* satisfaction moyenne

#### 3. Carte planning en direct

* liste des prochaines interventions
* heure
* client
* employé assigné
* statut
* retard éventuel

#### 4. Journal système

* SMS envoyés
* paiements confirmés
* assignations
* changements de statut
* erreurs ou alertes

#### 5. Carte “interventions urgentes”

* retards
* annulations
* employé absent
* paiement échoué

#### 6. Mini carte géographique

* employés en déplacement
* zones d'intervention

### Actions rapides

* assigner un employé
* envoyer une notification manuelle
* marquer une intervention prioritaire
* ouvrir une fiche client

---

## PAGE 2. Calendrier / Planification

### Objectif

Planifier toutes les interventions.

### Vue principale

* calendrier jour / semaine / mois
* colonnes par employé ou par zone
* cartes d'intervention déplaçables

### Filtres

* secteur géographique
* type de service
* employé
* statut
* client VIP
* nouvelle demande

### Carte intervention dans le calendrier

* nom client
* adresse
* durée prévue
* heure prévue
* employé
* badge statut
* couleur selon type de service

### Panneau latéral détail rapide

Quand on clique sur une intervention :

* fiche client résumé
* employé assigné
* durée
* heure arrivée prévue
* notes spéciales
* prix
* bouton replanifier
* bouton annuler
* bouton notifier client

### Actions

* drag-and-drop pour déplacer
* duplication d'intervention récurrente
* création récurrente hebdomadaire ou mensuelle

---

## PAGE 3. Liste des interventions

### Objectif

Voir et filtrer toutes les interventions.

### Tableau principal

Colonnes :

* no intervention
* date
* heure prévue
* client
* adresse
* type de service
* durée prévue
* employé assigné
* heure arrivée réelle
* heure départ réelle
* statut
* montant
* paiement
* actions

### Filtres avancés

* date début / fin
* statut
* employé
* client
* type de service
* payé / non payé
* en retard

### Onglets recommandés

* Aujourd'hui
* À venir
* En cours
* Terminées
* Annulées

### Fiche intervention détaillée

En cliquant sur une ligne :

* résumé complet
* timeline : assigné > en route > arrivé > début > terminé > facturé
* heure prévue d'arrivée
* heure réelle d'arrivée
* heure prévue de départ
* heure réelle de départ
* durée prévue
* durée réelle
* checklist de tâches
* photos avant/après
* notes du préposé
* signature client
* historique notifications
* détail paiement

---

## PAGE 4. Création / édition d'une intervention

### Formulaire en étapes

#### Étape 1. Informations client

* client existant ou nouveau client
* adresse du service
* téléphone
* instructions d'accès

#### Étape 2. Détails du service

* type de service
* description
* durée prévue
* nombre de préposés requis
* fréquence
* matériel inclus ou non
* notes importantes

#### Étape 3. Planification

* date
* heure d'arrivée prévue
* heure de départ estimée automatique
* employé assigné
* zone de service

#### Étape 4. Tarification et paiement

* prix du service
* taxes
* acompte
* mode de paiement
* statut de paiement
* envoi de facture automatique

#### Étape 5. Communication

Cases à cocher :

* envoyer SMS confirmation
* envoyer carte identité du préposé
* envoyer lien portail client
* envoyer rappel avant arrivée

### Boutons

* enregistrer brouillon
* confirmer et assigner
* enregistrer et facturer

---

## PAGE 5. Fiche client

### En-tête

* nom du client
* téléphone
* courriel
* adresse
* statut : actif / occasionnel / VIP / suspendu
* bouton nouvelle intervention
* bouton facture

### Onglets

#### Onglet 1. Profil

* informations personnelles
* préférences de service
* accès immeuble
* animaux
* allergies / produits à éviter
* note interne

#### Onglet 2. Historique des interventions

* tableau chronologique
* durée moyenne
* employé habituel
* incidents ou annulations

#### Onglet 3. Paiements

* factures
* reçus
* soldes dus
* remboursements

#### Onglet 4. Communications

* SMS envoyés
* courriels
* appels notés

#### Onglet 5. Évaluations

* notes données
* commentaires
* plaintes

### Bloc latéral

* valeur client totale
* fréquence moyenne
* prochain rendez-vous
* satisfaction moyenne

---

## PAGE 6. Liste des clients

### Tableau

Colonnes :

* nom
* téléphone
* courriel
* ville
* dernier service
* prochain service
* nombre d'interventions
* total dépensé
* statut
* actions

### Filtres

* actif / inactif
* secteur
* fréquence de service
* paiement en retard
* VIP

### Actions de masse

* envoyer un rappel
* exporter
* assigner une campagne
* créer une tournée

---

## PAGE 7. Liste des employés

### Tableau

Colonnes :

* photo
* nom
* no employé
* rôle
* secteur
* statut
* disponibilité aujourd'hui
* note moyenne
* interventions cette semaine
* actions

### Filtres

* disponible
* en intervention
* en congé
* secteur
* compétence

### Carte résumé employé

* photo
* nom
* badge disponible / en route / en service
* nombre d'heures cette semaine
* ponctualité
* évaluation moyenne

---

## PAGE 8. Fiche employé complète

### En-tête

* photo
* nom complet
* numéro employé
* rôle
* statut
* bouton voir carte identité
* bouton assigner service

### Onglets

#### Onglet 1. Profil

* coordonnées
* date d'entrée
* bio courte
* langues parlées
* spécialités
* disponibilités
* véhicule / transport

#### Onglet 2. Identité interne

* carte identité avec photo
* code QR
* statut vérifié
* documents validés
* contact urgence

#### Onglet 3. Horaire

* planning semaine
* disponibilités
* absences
* vacances

#### Onglet 4. Historique de services

* liste des interventions
* durée cumulée
* annulations
* retards

#### Onglet 5. Performance

* note moyenne client
* ponctualité
* services terminés
* commentaires positifs
* incidents signalés

#### Onglet 6. Documents

* contrat
* pièce d'identité
* formation
* documents RH

---

## PAGE 9. Carte identité employé

### Format

Prévoir une version écran et une version imprimable.

### Face avant

* photo portrait
* nom complet
* rôle
* no employé
* compagnie
* statut vérifié
* QR code ou code d'identification

### Face arrière ou bloc descriptif

* courte description
* expérience
* spécialités
* langues
* zone desservie
* date de validité interne

### Exemple de texte

"Sophie Tremblay, préposée en entretien ménager senior. 4 ans d'expérience en entretien résidentiel, grand ménage, nettoyage de départ et entretien récurrent. Reconnue pour sa ponctualité et son souci du détail."

---

## PAGE 10. Portail employé / application employé

### Accueil employé

* prochain service
* heure de départ recommandée
* adresse client
* coordonnées du client si autorisé
* bouton En route
* bouton Arrivé
* bouton Début du service
* bouton Terminé

### Écran service en cours

* chronomètre de durée
* checklist
* notes vocales ou écrites
* ajout de photos
* bouton incident

### Écran fin de service

* heure de départ enregistrée
* durée réelle
* checklist complétée
* commentaire du préposé
* signature client optionnelle

---

## PAGE 11. Module candidats

### Objectif

Gérer les personnes qui veulent rejoindre l'entreprise.

### Tableau principal

Colonnes :

* nom
* téléphone
* courriel
* ville
* expérience
* date inscription
* paiement inscription
* statut
* score priorité
* actions

### Filtres

* payé
* paiement échoué
* liste d'attente
* sélectionné
* refusé
* ville / secteur
* niveau d'expérience

### Actions

* voir dossier
* valider paiement
* demander documents
* déplacer dans liste d'attente
* sélectionner
* convertir en employé

---

## PAGE 12. Formulaire public d'inscription candidat

### Étape 1. Informations de base

* nom complet
* téléphone
* courriel
* ville
* adresse

### Étape 2. Profil professionnel

* expérience en entretien ménager
* types de services maîtrisés
* disponibilités
* moyens de transport
* langues parlées
* zones desservies

### Étape 3. Documents

* CV
* photo
* pièce d'identité
* preuve complémentaire si nécessaire

### Étape 4. Paiement d'inscription

* montant à payer
* mode de paiement
* résumé des conditions
* bouton payer et soumettre

### Étape 5. Confirmation

* reçu
* numéro de dossier
* message d'ajout à la liste d'attente
* lien vers portail candidat

---

## PAGE 13. Fiche candidat

### En-tête

* photo
* nom
* date d'inscription
* statut
* paiement confirmé ou non
* bouton sélectionner
* bouton refuser
* bouton convertir en employé

### Onglets

#### Onglet 1. Profil

* coordonnées
* bio
* expérience
* secteurs
* disponibilité

#### Onglet 2. Paiement

* montant payé
* date
* référence transaction
* reçu
* remboursement si applicable

#### Onglet 3. Documents

* CV
* pièce d'identité
* photo
* autres pièces

#### Onglet 4. Notes RH

* commentaires internes
* score
* étape de recrutement

#### Onglet 5. Historique

* messages envoyés
* demandes de documents
* modifications de statut

---

## PAGE 14. Liste d'attente candidats

### Vue kanban ou tableau

Colonnes recommandées :

* nouveaux payés
* en attente
* à évaluer
* prioritaires
* sélectionnés
* refusés

### Données visibles sur carte candidat

* photo
* nom
* ville
* expérience
* date de paiement
* disponibilité
* score priorité

### Actions rapides

* glisser-déposer de statut
* demande d'entrevue
* demande de documents
* conversion employé

---

## PAGE 15. Module paiements

### Sous-modules

1. Paiements clients
2. Paiements candidats
3. Factures
4. Remboursements

### Tableau paiements

Colonnes :

* date
* type paiement
* personne liée
* référence
* montant
* taxes
* mode
* statut
* reçu
* actions

### Filtres

* client / candidat
* payé / échoué / remboursé
* période
* mode de paiement

### KPI paiements

* total encaissé aujourd'hui
* total mensuel
* paiements en attente
* paiements échoués
* remboursement total

---

## PAGE 16. Fiche facture / reçu

### Contenu

* logo entreprise
* numéro facture
* client ou candidat
* détails de la prestation ou frais d'inscription
* montant avant taxes
* taxes
* total
* statut
* date de paiement
* mode de paiement
* bouton télécharger PDF
* bouton renvoyer par courriel

---

## PAGE 17. Centre de notifications

### Objectif

Configurer et suivre toutes les communications automatiques.

### Sous-sections

#### A. Modèles de messages

* confirmation réservation
* assignation employé
* employé en route
* employé arrivé
* service terminé
* rappel paiement
* confirmation inscription candidat
* candidat ajouté à liste d'attente
* candidat sélectionné

#### B. Journal d'envoi

Colonnes :

* date / heure
* type
* destinataire
* message
* canal SMS / email
* statut envoyé / échec

#### C. Règles d'automatisation

* quand intervention assignée → envoyer SMS
* quand employé clique En route → envoyer lien portail
* quand paiement candidat confirmé → changer statut à payé

---

## PAGE 18. Portail client

### Écran accueil client

* bienvenue
* prochaine intervention
* nom du préposé
* photo du préposé
* mini carte identité
* heure d'arrivée prévue
* durée estimée
* heure de départ estimée
* statut en direct

### Onglets

#### Onglet 1. Suivi en temps réel

* assigné
* en route
* arrivé
* en cours
* terminé

#### Onglet 2. Détail du service

* type de service
* tâches prévues
* durée prévue
* durée réelle après fin

#### Onglet 3. Facturation

* montant
* reçu
* statut payé

#### Onglet 4. Historique

* interventions passées
* notes
* évaluations

#### Onglet 5. Support

* envoyer message
* signaler problème

---

## PAGE 19. Portail candidat

### Écran principal

* message de bienvenue
* numéro de dossier
* statut actuel
* paiement confirmé
* message RH

### Sections

* documents transmis
* prochaines étapes
* position ou phase sur liste d'attente
* bouton téléverser document
* bouton contacter le recrutement

---

## PAGE 20. Rapports

### Rapports opérationnels

* interventions par jour / semaine / mois
* taux de services terminés
* durée moyenne réelle vs prévue
* ponctualité des employés
* zones les plus demandées

### Rapports financiers

* chiffre d'affaires
* revenus par type de service
* paiements candidats
* factures impayées
* remboursements

### Rapports RH

* employés les plus demandés
* satisfaction moyenne
* temps moyen avant embauche d'un candidat
* taux de conversion candidats → employés

### Options

* export PDF
* export Excel
* filtres dynamiques

---

## PAGE 21. Paramètres

### Sous-sections

* informations entreprise
* utilisateurs et rôles
* tarifs
* types de services
* taxes
* passerelles de paiement
* paramètres SMS / email
* zones desservies
* horaires d'ouverture
* statuts personnalisés
* modèle de carte identité
* conditions d'inscription candidat

---

# 5. Parcours utilisateur détaillé

## Parcours A. Client vers service terminé

1. création fiche client
2. création intervention
3. assignation employé
4. notification client avec photo + identité + heure prévue
5. employé clique En route
6. notification automatique client
7. employé clique Arrivé
8. début du service
9. fin du service
10. enregistrement heure départ
11. facture + reçu + demande d'évaluation

## Parcours B. Candidat vers employé

1. candidat remplit formulaire
2. paiement inscription
3. dossier créé automatiquement
4. statut payé
5. placement en liste d'attente
6. évaluation interne
7. sélection
8. conversion en fiche employé
9. émission carte identité interne

---

# 6. Règles fonctionnelles à donner au programmeur

## Gestion du temps

* l'heure de départ estimée se calcule automatiquement à partir de l'heure d'arrivée prévue + durée prévue
* les heures réelles doivent être conservées séparément des heures prévues
* le système doit calculer la durée réelle automatiquement

## Gestion des statuts

* chaque changement de statut doit être historisé
* chaque changement critique peut déclencher un SMS ou un courriel

## Paiements

* un paiement candidat confirmé doit verrouiller l'inscription comme “dossier actif”
* un paiement client peut être lié à une facture ou à un acompte

## Traçabilité

* journal d'audit pour chaque action administrateur
* journal d'événements pour notifications et paiements

---

# 7. Recommandations UX utiles

* toujours afficher le statut avec badge coloré
* prévoir un bouton d'action principal visible sur chaque fiche
* permettre la recherche globale par nom, téléphone, adresse, numéro dossier
* éviter des formulaires trop longs sur une seule page
* prévoir un mode mobile pour employés et clients
* rendre la timeline de service visible partout

---

# 8. Livrables à demander au programmeur

## Front-end

* interface admin responsive
* portail client responsive
* portail candidat responsive
* espace employé mobile-first

## Back-end

* gestion rôles et permissions
* API clients
* API interventions
* API employés
* API candidats
* API paiements
* API notifications
* historique et logs

## Base de données

Tables minimales :

* users
* roles
* clients
* client_addresses
* employees
* employee_documents
* employee_id_cards
* candidates
* candidate_documents
* waiting_list
* services
* service_types
* interventions
* intervention_status_history
* intervention_checklists
* payments
* invoices
* notifications
* reviews
* audit_logs

---

# 9. Résumé final à remettre au développeur

Le CRM doit être conçu comme une plateforme à 4 espaces :

* Admin
* Employé
* Client
* Candidat

Les modules essentiels sont :

* planification des services
* suivi des heures d'arrivée et de départ
* durée prévue et durée réelle
* notifications automatiques
* paiements clients
* inscription payante des candidats
* gestion de la liste d'attente
* carte identité avec photo et description
* portail de suivi client
* traçabilité complète des actions

L'interface doit permettre une gestion simple, rapide et visuelle, avec des tableaux filtrables, des timelines de statut, des paiements intégrés et un suivi complet des dossiers.
# Projet-final-Mod-les-d-affaire-pour-l-innovation-et-la-r-silience_S1B
