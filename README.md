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
(https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/)

Helm Charts
(https://helm.sh/docs/intro/install/)

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
2. rajouter le repo elastic (`helm repo add elastic https://helm.elastic.co`)
3. installer elasticsearch (`helm upgrade --install elk-elasticsearch elastic/elasticsearch -n elk -f ./elasticsearch/values.yml`)
4. installer kibana (`helm upgrade --install elk-kibana elastic/kibana -n elk -f ./kibana/values.yml`)
5. installer logstash (`helm upgrade --install elk-logstash elastic/logstash -n elk -f ./logstash/values.yml`)
6.  installer filebeat (`helm upgrade --install elk-filebeat elastic/filebeat -n elk -f ./filebeat/values.yml`)
