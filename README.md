# Configuration Docker Compose Firezone

Configuration Docker Compose pour déployer Firezone avec PostgreSQL et Caddy.

## Description

Ce dépôt contient la configuration Docker Compose pour déployer Firezone avec :
- **Firezone** : serveur VPN WireGuard
- **PostgreSQL** : base de données
- **Caddy** : reverse proxy pour l'interface web

### Ports exposés

- **51820/udp** : WireGuard VPN
- **80/tcp** : HTTP (Caddy)
- **443/tcp et 443/udp** : HTTPS (Caddy)
