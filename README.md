# Configuration Docker Compose Firezone

Configuration Docker Compose pour déployer Firezone avec PostgreSQL et Caddy.

## Description

Ce dépôt contient la configuration Docker Compose pour déployer Firezone avec :
- **Firezone** : serveur VPN WireGuard
- **PostgreSQL** : base de données
- **Caddy** : reverse proxy pour l'interface web

## Prérequis

- Docker et Docker Compose installés
- Accès à un domaine (configuré ici pour `vpn.davincicode.fr`)

## Installation

1. Clonez ce dépôt :
```bash
git clone https://github.com/VOTRE_USERNAME/config-docker-compose-firezone.git
cd config-docker-compose-firezone
```

2. Créez votre fichier `.env` à partir de l'exemple :
```bash
cp env.example .env
```

3. Modifiez le fichier `.env` avec vos paramètres :
```bash
nano .env
```

4. Lancez les services :
```bash
docker-compose up -d
```

## Configuration

### Variables d'environnement

Ajustez les variables dans le fichier `.env` :
- `DATABASE_USER` : utilisateur PostgreSQL
- `DATABASE_PASSWORD` : mot de passe PostgreSQL
- `DATABASE_DB` : nom de la base de données

### Ports exposés

- **51820/udp** : WireGuard VPN
- **80/tcp** : HTTP (Caddy)
- **443/tcp et 443/udp** : HTTPS (Caddy)

## Commandes utiles

```bash
# Démarrer les services
docker-compose up -d

# Voir les logs
docker-compose logs -f

# Arrêter les services
docker-compose down

# Arrêter et supprimer les volumes
docker-compose down -v
```

