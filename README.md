# 🔐 Secure P2P Messaging

Secure P2P Messaging est une application de messagerie sécurisée et décentralisée développée en Python. Elle permet à deux utilisateurs de discuter directement en pair-à-pair (P2P), sans intermédiaire, tout en assurant la confidentialité grâce au chiffrement RSA.

## 🚀 Fonctionnalités

- 🔐 Chiffrement RSA des messages (2048 bits)
- 🔄 Échange direct entre pairs via sockets TCP
- 🌐 Serveur Flask pour l’authentification et la gestion des connexions
- 🧑‍🤝‍🧑 Système d’amis pour échanger les clés publiques en toute sécurité
- 📡 Mise à jour automatique de l’IP publique à chaque lancement

## Mise en situation
Face à la généralisation de la surveillance numérique, la confidentialité des échanges est devenue un enjeu éthique majeur. Les solutions centralisées sont vulnérables aux intrusions et aux violations de vie privée.  
➡️ D'où la nécessité de développer une application P2P sécurisée, respectueuse de la vie privée, permettant une communication directe chiffrée entre utilisateurs.

---

## Objectif
Créer une plateforme de messagerie instantanée décentralisée :
- Basée sur une architecture P2P
- Avec chiffrement RSA
- Utilisant SHA-256 pour la signature
- Résistante aux attaques de type Man-in-the-Middle (MITM)

---

### 📅 Mars : Conception, recherche et infrastructure

- **Analyse de la problématique**
- **Étude des solutions techniques existantes**
  - Protocoles P2P (ex : BitTorrent Chat, Tox)
  - Chiffrement RSA (asymétrique)
  - SHA-256 pour les empreintes numériques
- **Choix des technologies**
  - Backend : Flask (Python)
  - Base de données : SQLite
- **Développement du serveur REST API**
  - Fonctionnalités : création de compte, connexion, ajout d'ami, envoi/récupération d’adresse IP
- **Problèmes rencontrés**
  - Conflits sur SQLite en accès concurrent → gestion manuelle des transactions en Python

---

### 📅 Avril : Développement serveur et premiers tests

- **Finalisation du backend**
  - Test des fonctionnalités : création de compte, login, récupération d’adresse IP
  - Déploiement du serveur Flask sur Render
- **Début du client P2P**
  - Connexion à l’API Flask pour identification & découverte d’amis
  - Développement de la communication par sockets TCP
- **Cryptographie**
  - Génération des paires de clés RSA
  - Début de l’échange de clés publiques entre utilisateurs

---

### 📅 Mai : Sécurisation, finalisation client et interface CLI

- **Sécurisation**
  - Intégration de SHA-256 pour signatures numériques
  - Empreinte numérique pour lutter contre les attaques MITM
- **Client P2P**
  - Communication bilatérale via sockets
  - Protocole de synchronisation & chiffrement des messages
- **Interface CLI**
  - Interface terminal : login, ajout d’amis, envoi de message
  - Tests, débogage et robustesse
- **Préparation finale**
  - Structuration du code sur GitHub
  - Documentation technique
  - Préparation de la soutenance (exemples d’attaque/défense, démonstration)

---

## 🔄 Fonctionnement du projet

```

          [Alice]                                [Bob]
             |                                      |
             |         📡 Demande d'IP de Bob       |
             |────────▶ Serveur central ◀───────────|
             |         📡 Envoie son IP à Alice    |
             |                                     |
     (Échange P2P direct établi grâce aux IPs récupérées)
             |                                     |
             |=========== Connexion TCP ===========|
             |                                     |
             |        🔐 Échange de clés publiques |
             | <─────────────────────────────────> |
             |                                     |
             |        💬 Échange de messages       |
             | <─────────────────────────────────> |
             |    (chiffrés avec les clés RSA)     |


```

## 📁 Structure du projet

```
Secure-P2P-Messaging/
│
├── P2PClient.py          # Client P2P pour l'envoi de messages sécurisés
├── P2PServer.py          # Serveur P2P qui attend la connexion client pour la réception des messages sécurisés
├── Flaskserver.py        # Serveur Flask (API REST) pour la gestion des requêtes
└── README.md             # Documentation du projet
```


---

## ⚙️ Prérequis

- Python ≥ 3.8
- Modules Python :
  - `flask`
  - `requests`
  - `pycryptodome`


## 🔧 Améliorations prévues

- Interface graphique
- Chiffrement hybride RSA + AES
- Authentification 2FA ou via clé publique
- Base de données sécurisée
- Transfert de fichiers entre pairs

## 📄 Licence

Ce projet est disponible gratuitement sous la licence **Secure P2P Messaging License (Non-Commercial)**.  
Toute utilisation commerciale est strictement interdite sans l'autorisation explicite de l’auteur.  
Voir le fichier [LICENSE](./LICENSE) pour plus d'informations.

