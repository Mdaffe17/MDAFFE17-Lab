
# MDAFFE17-Lab

Ce dépôt documente la construction et l'évolution de mon homelab dédié aux réseaux, à l'administration système et à la cybersécurité.

J'utilise des équipements Cisco, un switch TP-Link, des ordinateurs physiques et, à terme, des environnements virtualisés pour reproduire différentes situations rencontrées dans les infrastructures informatiques.

Mon objectif est de comprendre comment ces infrastructures fonctionnent, de savoir les configurer et surtout de développer mes capacités de diagnostic et de dépannage.

Mes notes de cours et exercices sont regroupés dans [learning-journey](https://github.com/Mdaffe17/learning-journey).

## État actuel

Le laboratoire est en cours de mise en place. Une partie des équipements est déjà disponible et les premières expérimentations réseau ont été réalisées.

- Serveur Dell sous Ubuntu Server 24.04 LTS, accessible par SSH.
- Switch TP-Link TL-SG1016DE utilisé pour les premiers tests réseau.
- Cisco Catalyst 2960-X et 3750-X disponibles pour les prochains labs.
- Câbles Ethernet Cat6 et câbles console Cisco reçus.
- Installation de Proxmox VE prévue sur le Beelink.
- Architecture réseau segmentée et pare-feu dédiés encore à mettre en place.

Les premières expérimentations ont porté sur l'installation d'Ubuntu Server sur le Dell et les tests de connectivité réseau avec le switch TP-Link. Les comptes rendus publics des prochains laboratoires seront ajoutés progressivement à ce dépôt.

## Matériel

| Équipement | Utilisation | État |
|---|---|---|
| MacBook Pro M4 | Poste d'administration et de documentation | Actif |
| Beelink Ryzen 7, 32 Go RAM | Futur serveur Proxmox VE | Actif sous Windows |
| Dell, 8 Go RAM, SSD 256 Go | Serveur Ubuntu Server 24.04 LTS | Opérationnel |
| TP-Link TL-SG1016DE | Switch manageable | Fonctionnel |
| Cisco Catalyst 2960-X, 48 ports PoE | Switch d'accès, couche 2 | Reçu |
| Cisco Catalyst 3750-X, 48 ports PoE+ | Switching et routage, couche 3 | Reçu |
| Câbles Ethernet Cat6 et 2 câbles console | Connexion des équipements | Reçus |
| Mini-PC x86 pour pfSense | Pare-feu dédié | Prévu |
| Routeurs Cisco 1841/2811 | Expérimentations WAN | Prévus |
| Raspberry Pi 5 | Clients et services supplémentaires | Prévus |

## Architecture envisagée

L'architecture ci-dessous représente la cible du laboratoire. Elle évoluera selon les équipements disponibles et les besoins des différents projets.

```text
                  Internet
                     |
             Routeur domestique
                     |
                pfSense
                     |
              Cisco 3750-X
               (coeur L3)
              /     |     \
             /      |      \
     Cisco 2960-X  TP-Link  Beelink
       (acces)     (L2)    (Proxmox)
          |          |
       Clients      Dell
                    |
               Autres services
```

Un réseau WAN expérimental avec plusieurs routeurs Cisco est également envisagé pour étudier l'interconnexion de sites.

## Évolution du laboratoire

Le projet progressera à travers plusieurs environnements :

1. Réseau local et administration des équipements.
2. Réseau de petite entreprise avec VLAN et routage.
3. Services réseau et administration Linux/Windows.
4. Virtualisation et déploiement de services.
5. Sécurité réseau, segmentation et pare-feu.
6. Supervision, détection et investigations SOC.
7. Architectures multisites et scénarios de dépannage avancés.

Ces étapes représentent les orientations du projet et non des travaux déjà terminés.

## Documentation

Les dossiers contiendront les topologies, les configurations utiles, les commandes, les tests et les problèmes rencontrés lors des manipulations.

Un [modèle de compte rendu](_template/README.md) est disponible pour les futurs laboratoires.

Les fichiers publiés ne doivent contenir aucun mot de passe, clé privée, token, licence ou autre information sensible.
