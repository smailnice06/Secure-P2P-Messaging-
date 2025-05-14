# Secure-P2P-Messaging-

# 🔐 Secure P2P Messaging

Secure P2P Messaging est une application de messagerie sécurisée et décentralisée développée en Python. Elle permet à deux utilisateurs de discuter directement en pair-à-pair (P2P), sans intermédiaire, tout en assurant la confidentialité grâce au chiffrement RSA.

## 🚀 Fonctionnalités

- 🔐 Chiffrement RSA des messages (2048 bits)
- 🔄 Échange direct entre pairs via sockets TCP
- 🌐 Serveur Flask pour l’authentification et la gestion des connexions
- 🧑‍🤝‍🧑 Système d’amis pour échanger les clés publiques en toute sécurité
- 📡 Mise à jour automatique de l’IP publique à chaque lancement

---

## 📁 Structure du projet

Secure-P2P-Messaging/
│
├── P2PClient.py          # Client P2P pour l'envoi de messages sécurisés
├── P2PServer.py          # Serveur P2P local pour la réception des messages
├── Flaskserver.py        # Serveur Flask (API REST) pour la gestion des requêtes
├── rsa_utils.py          # Utilitaires pour la gestion des clés RSA
└── README.md             # Documentation du projet
