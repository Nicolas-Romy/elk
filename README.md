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

Kubectl

Helm Charts

## Arborescence

``` text

.
└── elk
    ├── elasticsearch 
    │   ├── .gitkeep
    │   └──  values.yml
    ├── filebeat
    │   ├── .gitkeep
    │   └──  values.yml
    ├── kibana
    │   ├── .gitkeep
    │   └──  values.yml
    ├── logstash
    │   ├── .gitkeep
    │   └──  values.yml
    └── README.md
```
## Installation

1. Copier le repo
2. Modifier les fichier values.yml en fonction de vos besoins

## Utilisation

1. Ouvrir un terminal à la racine du projet
2. Monter le compose avec (`docker compose up`)
