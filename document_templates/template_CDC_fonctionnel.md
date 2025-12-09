# Template CDC fonctionnel

# Cahier des charges fonctionnel

## Projet : [Nom du projet]

- **Version du document** : v0.1
- **Date** : [JJ/MM/AAAA]
- **Auteur·ices** : [Nom(s)]
- **Validateur·ices** : [Nom(s)]

---

## 0. Historique des versions

| Version | Date | Auteur | Commentaires |
| --- | --- | --- | --- |
| v0.1 | JJ/MM/AAAA | [Nom] | Première rédaction |

---

## 1. Contexte & objectifs

### 1.1 Contexte

Décrire :

- La situation actuelle
- Le problème ou l’opportunité
- Les équipes / utilisateurs concernés

> Exemple :
> 
> 
> Le système actuel ne permet pas de détecter efficacement les fraudes liées à [...].
> 
> Les équipes impactées sont : [...].
> 

### 1.2 Enjeux

- Enjeux business :
    - [Augmenter / réduire / optimiser ...]
- Enjeux opérationnels :
    - [Ex : réduire le temps de traitement d’un dossier de X%]
- Enjeux réglementaires / conformité :
    - [Ex : RGPD, conformité interne, etc.]

### 1.3 Objectifs du projet

Lister les objectifs principaux, idéalement en mode SMART :

- Objectif 1 :
- Objectif 2 :
- Objectif 3 :

### 1.4 Hors périmètre (Out of scope)

Ce que le projet **ne couvre pas** :

- [Ex : pas de refonte du système de paiement]
- [Ex : la gestion des comptes utilisateurs reste dans le SI existant]

---

## 2. Périmètre fonctionnel & utilisateurs

### 2.1 Typologie des utilisateurs / acteurs

Pour chaque type d’utilisateur :

| Acteur | Rôle métier | Objectifs principaux | Droits (lecture/écriture/validation) |
| --- | --- | --- | --- |
| [Acteur A] | [Ex : Caissier·e] | [Encaisser, enregistrer une transaction...] | [Ex : lecture + écriture] |
| [Acteur B] | [Ex : Responsable magasin] | [Suivre les indicateurs, valider des actions...] | [Ex : validation + lecture globale] |

### 2.2 Processus métier principaux

Décrire les grands processus sous forme de texte ou de liste numérotée.

> Exemple de processus :
> 
> - P1 : Enregistrement d’une transaction
> - P2 : Analyse d’une alerte de fraude
> - P3 : Clôture de la journée / génération de rapports

---

## 3. Données & règles de gestion

### 3.1 Entités de données

Lister les principales entités manipulées par le système.

| Entité | Description | Attributs principaux |
| --- | --- | --- |
| [Entité A] | [Ex : Transaction] | [id, date, montant, type, magasinId, clientId...] |
| [Entité B] | [Ex : Magasin] | [id, nom, adresse, région...] |
| [Entité C] | [Ex : Client] | [id, anonymiséOuiNon, segment, ...] |

### 3.2 Règles de gestion

Décrire les règles métier qui s’appliquent aux données et aux processus.

| ID règle | Description de la règle métier | Impact / Action attendue |
| --- | --- | --- |
| RG-001 | [Ex : Une transaction > 500€ doit être validée par un responsable magasin.] | Blocage en caisse + demande de validation |
| RG-002 | [Ex : Les données nominatives de plus de 2 ans sont anonymisées.] | Anonymisation automatique |

---

## 4. Exigences fonctionnelles

Chaque exigence fonctionnelle décrit **ce que le système doit faire**.

> Format suggéré :
> 
> - ID : F-XXX
> - Titre
> - Acteur concerné
> - Description
> - Préconditions
> - Scénario nominal
> - Cas d’exception
> - Règles de gestion associées
> - Priorité (MoSCoW : Must / Should / Could / Won’t)

---

### 4.1 Liste des fonctionnalités

| ID | Titre de la fonctionnalité | Acteur principal | Priorité (M/S/C/W) |
| --- | --- | --- | --- |
| F-001 | [Ex : Enregistrer une transaction] | [Ex : Caissier·e] | Must |
| F-002 | [Ex : Consulter la liste des transactions] | [Ex : Responsable] | Must |
| F-003 | [Ex : Visualiser les alertes de fraude] | [Ex : Analyste fraude] | Should |

### 4.2 Fiches détaillées (exemple de structure à répéter)

### F-001 – [Titre de la fonctionnalité]

- **Acteur** : [Acteur principal]
- **Description** :
    
    [Décrire en langage métier ce que permet cette fonctionnalité.]
    
- **Préconditions** :
    - [Ex : L’utilisateur est authentifié.]
    - [Ex : Le magasin est ouvert.]
- **Scénario nominal** :
    1. [Étape 1…]
    2. [Étape 2…]
    3. [Étape 3…]
- **Cas d’exception / erreurs** :
    - [Ex : montant non valide → message d’erreur]
    - [Ex : problème de connexion → affichage d’un message et journalisation]
- **Règles de gestion associées** :
    - RG-001, RG-002
- **Priorité** : Must

*(Répéter ce bloc pour F-002, F-003, etc.)*

---

## 5. Parcours utilisateur & interfaces

### 5.1 Parcours utilisateur clés

Décrire 2–3 parcours majeurs.

> Exemple :
> 
> - Parcours 1 : [Acteur X] se connecte, consulte [liste], filtre selon [critères], puis réalise [action].
> - Parcours 2 : [...]

### 5.2 Maquettes / wireframes (si disponibles)

Insérer ou référencer les maquettes :

- Écran 1 : [Nom]
- Écran 2 : [Nom]

*(Lien Figma / Miro / PDF si besoin.)*

### 5.3 Contraintes d’UX / accessibilité

- Doit être utilisable sur : [desktop / tablette / mobile]
- Contraintes d’accessibilité : [contraste, lisibilité, navigation clavier, etc.]

---

## 6. Interfaces avec les autres systèmes

Lister les systèmes externes avec lesquels le projet doit communiquer.

| Système externe | Description | Type d’échange | Fréquence / volumétrie |
| --- | --- | --- | --- |
| [SI A] | [Ex : Système de caisse] | [Ex : envoi de transactions] | [Ex : temps réel, 10k/jour] |

> Ici on décrit le quoi (informations échangées), pas encore le comment technique (API, format exact, etc.).
> 

---

## 7. Exigences non fonctionnelles (vue fonctionnelle)

### 7.1 Performance

- Temps de réponse cible : [Ex : 95% des consultations < 2 secondes]
- Volumétrie :
    - [Ex : X transactions / jour, Y utilisateurs simultanés]

### 7.2 Disponibilité

- Plages de disponibilité :
    - [Ex : 7j/7, 6h–23h]
- Tolérance aux pannes / reprise :
    - [Ex : RPO/RTO indicatifs si connus]

### 7.3 Sécurité & confidentialité

- Gestion des accès :
    - [Ex : authentification nominative, rôles par profil]
- Données sensibles :
    - [Ex : règles sur les données personnelles (RGPD), anonymisation, logs]

### 7.4 Compatibilité

- Navigateurs / OS supportés :
    - [Ex : dernières versions Chrome, Firefox, Edge]
- Autres contraintes :
    - [Langues, résolution écran minimale, etc.]

---

## 8. Critères d’acceptation & validation

### 8.1 Critères d’acceptation par fonctionnalité

| ID fonction | Critères d’acceptation |
| --- | --- |
| F-001 | [Ex : l’utilisateur peut enregistrer une transaction valide] |
| F-002 | [Ex : la liste est filtrable par date et magasin] |

### 8.2 Types de tests prévus

- Tests fonctionnels
- Tests de recette utilisateur (UAT)
- Tests de non-régression (si applicable)

---

## 9. Annexes

### 9.1 Glossaire

| Terme | Définition |
| --- | --- |
| [Terme 1] | [Définition] |
| [Terme 2] | [Définition] |

### 9.2 Documents de référence

- [Doc 1 : lien ou emplacement]
- [Doc 2 : lien ou emplacement]

---