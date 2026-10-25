# Aqui Portail Client

Extension WordPress de **portail client sécurisé** : chaque client suit l'avancement de ses projets, phase par phase, consulte ses documents confidentiels et échange avec l'équipe, depuis une page de son espace sur le site.

Développée par **AGIR-SXO** pour Aqui Ingénierie (bureau d'études, maîtrise d'œuvre, AMO).

## Fonctionnalités

### Projets et avancement
- Menu **Projets** dans l'administration, sous Pages.
- **Modèles de phases** créés par l'équipe (ex. maîtrise d'œuvre loi MOP, AMO) : ajout, modification, activation / désactivation, suppression.
- Phases par projet : ordre modifiable, statut (à venir, en cours, terminée), avancement calculé automatiquement ou saisi manuellement.
- Un projet peut être partagé avec un ou plusieurs comptes clients.

### Documents confidentiels
- Dépôt par glisser-déposer, contrôle du format et de la taille.
- Fichiers stockés **hors de la médiathèque**, dans un dossier protégé et inaccessible directement depuis Internet.
- Téléchargement uniquement par un client autorisé et connecté, via un lien à usage contrôlé ; chaque téléchargement est journalisé.

### Espace client
- Page **Compte** : connexion, mot de passe oublié et choix du mot de passe, aux couleurs du site, sans passer par les pages WordPress.
- Mot de passe provisoire à remplacer obligatoirement à la première connexion.
- Lien d'invitation (24 h, usage unique) à transmettre au client par sa propre messagerie ou par SMS.
- Échanges client / équipe par projet (activables projet par projet).

### Alertes et notifications (sans SMTP)
- Pastille et bandeau « nouveaux messages » dans l'administration ; étiquette « Nouvelle réponse » côté client.
- Notifications Windows / navigateur (norme Web Push) activées par chaque personne sur son appareil. Le contenu des messages n'est jamais transmis aux services de notification.

### Mises à jour
- Mises à jour proposées directement dans **Extensions** du back-office WordPress, à partir des Releases de ce dépôt.
- L'archive n'est acceptée que si elle provient de ce dépôt **et** si son empreinte SHA-256 correspond au fichier `.sha256` publié avec la Release.

## Sécurité

Conçue selon le référentiel **OWASP ASVS niveau 2** :
- cloisonnement strict : un client ne voit que ses propres projets et documents ;
- politique de mots de passe robuste, blocage temporaire après échecs répétés, messages d'erreur génériques ;
- protection anti-robot hCaptcha (optionnelle), compatible avec une adresse de connexion personnalisée ;
- compatibilité avec la double authentification de Security Optimizer ;
- déconnexion automatique après inactivité ;
- contrôle réel du type des fichiers déposés, noms de stockage aléatoires ;
- jetons anti-falsification (nonces) sur tous les formulaires et actions ;
- journal d'activité (connexions, téléchargements, échanges) avec durée de conservation réglable ;
- espace client exclu des moteurs de recherche et du cache.

Pour signaler une faille de sécurité, **n'ouvrez pas de ticket public** : écrivez à contact@agir-sxo.fr.

## RGPD

- Export et effacement des données personnelles via les outils WordPress (Outils → Exporter / Effacer les données personnelles).
- Texte suggéré pour la politique de confidentialité (Réglages → Confidentialité).
- Option de suppression complète des données à la désinstallation.

## Prérequis

- WordPress 6.4 ou plus
- PHP 8.2 ou plus (8.5.12 ou plus recommandé)
- Site en HTTPS

## Installation

1. Télécharger `aqui-portail-client.zip` depuis la dernière Release.
2. WordPress → Extensions → Ajouter → Téléverser une extension.
3. Activer, puis régler dans **Projets → Réglages**.

## Licence

GPL-2.0-or-later.
