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

## 🤵🏽‍♂️ Route serveur

```

| Méthode | URL                          | Description                      |
| ------: | ---------------------------- | -------------------------------- |
|  `POST` | `/register`                  | Enregistrement                   |
|  `POST` | `/login`                     | Connexion                        |
|  `POST` | `/update_ip`                 | Mise à jour IP + port            |
|  `POST` | `/add_friend`                | Demande d’ami                    |
|  `POST` | `/accept_friend`             | Accepter une demande             |
|   `GET` | `/get_ip/<username>`         | Obtenir IP/port d’un utilisateur |
|   `GET` | `/get_public_key/<username>` | Obtenir la clé publique d’un ami |

```

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

