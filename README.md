# Déploiement Stack ELK

## À propos

Ce document décrit l'architecture et la configuration d'un docker compose produisant un cluster WordPress utilisant HAProxy comme équilibreur de charge 

## Table des matières

- 🪧 [À propos](#à-propos)
- 📦 [Prérequis](#prérequis)
- 🌳 [Arborescence](#arborescence)
- 🚀 [Installation](#installation)
- 🛠️ [Utilisation](#utilisation)

## Prérequis

Docker compose (https://docs.docker.com/compose/install/)

## Arborescence

``` text

.
└── Wordpress
    ├── haproxy #load balancer
    │   ├── .gitkeep
    │   └──  haproxy.cfg #configuration haproxy
    ├── .env #fichier de variables pour docker-compose.yml
    ├── .gitkeep
    ├── docker-compose.yml #compose contenant le haproxy & les 3 conteneurs Wordpress
    └── README.md
```
## Installation

1. Copier le repo
2. Modifier le .env en fonction de l'adressage ip

## Utilisation

1. Ouvrir un terminal à la racine du projet
2. Monter le compose avec (`docker compose up`)
