# 💬 Organisation et gestion des canaux de communication — Mattermost

> Outil de communication interne auto-hébergé de RAID-A-PORTER, destiné à centraliser à la fois les échanges d'équipe et les remontées automatisées de supervision/sécurité.

## Statut

🚧 **Documentation à compléter** — Mattermost est identifié comme brique du socle collaboratif du homelab, avec des intégrations prévues depuis Zabbix, Wazuh et GLPI. Le déploiement et la structuration détaillée des canaux restent à formaliser dans ce dépôt.

## Rôle dans l'architecture

Dans le scénario d'entreprise RAID-A-PORTER, Mattermost joue le rôle de l'outil de communication interne (équivalent Slack/Teams auto-hébergé), avec deux usages distincts :

1. **Communication d'équipe** : canaux organisés par service métier ou par projet.
2. **Canal d'astreinte technique** : réception centralisée des alertes de supervision (`zabbix-notifications-mattermost`) et de sécurité (`wazuh-notifications-mattermost`), ainsi que des notifications GLPI (`glpi-notifications-mattermost`).

## Organisation des canaux envisagée

| Canal | Vocation |
|---|---|
| `#supervision-zabbix` | Alertes de disponibilité/performance |
| `#soc-wazuh` | Alertes de sécurité |
| `#glpi-tickets` | Notifications de tickets support |
| Canaux par service | Communication d'équipe (Finance, Commerce, Technique, RH, Logistique, IT) |

## Aperçu

<img width="946" height="757" alt="channel1" src="https://github.com/user-attachments/assets/420696e8-f34f-429c-b35d-525521132f60" /> <img width="939" height="535" alt="channel2" src="https://github.com/user-attachments/assets/37bebbcd-adb8-4522-8946-e889c56fc2b1" />



## Prochaines étapes

- [x] Déployer le serveur Mattermost (Docker)
- [x] Authentification unifiée via l'annuaire Active Directory
- [x] Créer l'arborescence de canaux ci-dessus
- [ ] Brancher les webhooks entrants Zabbix/Wazuh/GLPI

## Repos liés

- `zabbix-notifications-mattermost`
- `wazuh-notifications-mattermost`
- `glpi-notifications-mattermost`

## Auteur

**Lilian Vertueux** — [LinkedIn](https://www.linkedin.com/in/lilian-vertueux/)
