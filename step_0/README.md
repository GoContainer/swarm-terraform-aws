# Cluster Swarm avec Terraform et Scaleway

## Description

Le projet permet en quelques secondes de monter une base d'un cluster swarm avec le provider scaleway et terraform.

## Prérequis
- Docker
- Make
- Un compte Scaleway

## Installation du projet
  
```
git clone git@github.com:GoContainer/swarm-terraform-scaleway.git
cd swarm-terraform-scaleway
cp terraform.tfvars.example terraform.tfvars 
```

Modifier les valeurs du fichier terraform.tfvars 

## Utilisations 

``make apply`` : Lance la création du cluster swarm selon le fichier de configuration.   
``make destroy`` : Supprime le cluster créé.  
``make output`` : Donne l'IP du swarm manager.  
``make validate`` : Permet de validé les valeurs mise en conf.
