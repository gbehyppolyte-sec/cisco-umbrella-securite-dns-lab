# Sécurité DNS avec Cisco Umbrella

![Cisco Umbrella](https://img.shields.io/badge/Solution-Cisco%20Umbrella-blue) ![DNS](https://img.shields.io/badge/Protocole-DNS-green) ![Statut](https://img.shields.io/badge/Statut-%C3%A0%20compl%C3%A9ter-yellow)

Ce projet présente, à ce stade de façon théorique, la mise en œuvre d'une protection DNS avec Cisco Umbrella, une solution de sécurité cloud de type Secure Internet Gateway (SIG). L'objectif est de bloquer les domaines malveillants et les tentatives de phishing dès la résolution DNS, avant même qu'une connexion ne soit établie avec le site visé.

## Sommaire

1. [Objectifs](#objectifs)
2. [Présentation de Cisco Umbrella](#présentation-de-cisco-umbrella)
3. [Architecture](#architecture)
4. [Prérequis](#prérequis)
5. [Déploiement](#déploiement)
6. [Politiques de filtrage](#politiques-de-filtrage)
7. [Scénarios de test prévus](#scénarios-de-test-prévus)
8. [Compétences visées](#compétences-visées)
9. [Avertissement](#avertissement)
10. [Auteur](#auteur)

## Objectifs

- Mettre en place une protection DNS avec Cisco Umbrella
- Comprendre le fonctionnement d'un Secure Internet Gateway
- Définir des politiques de sécurité adaptées à un environnement d'entreprise
- Tester et valider le blocage de domaines malveillants

## Présentation de Cisco Umbrella

Cisco Umbrella est une solution de sécurité cloud qui agit au niveau de la résolution DNS. Chaque requête DNS d'un poste client est analysée avant qu'une connexion IP ne soit établie, ce qui permet de bloquer une menace de façon proactive, sans attendre qu'elle atteigne le poste.

## Architecture

1. Les postes clients génèrent des requêtes DNS
2. Les requêtes sont envoyées vers les résolveurs Cisco Umbrella
3. Umbrella analyse les domaines demandés
4. Les domaines légitimes sont résolus normalement
5. Les domaines identifiés comme malveillants sont bloqués et journalisés

## Prérequis

- Un compte Cisco Umbrella
- Un accès Internet fonctionnel
- Des droits administrateur sur la console Umbrella
- La possibilité de configurer la résolution DNS du réseau testé

## Déploiement

Les serveurs DNS du réseau sont reconfigurés pour pointer vers les résolveurs Cisco Umbrella, ce qui permet l'inspection et le filtrage de l'ensemble du trafic DNS sortant.

## Politiques de filtrage

Les politiques de sécurité définies dans Umbrella visent à :

- bloquer les domaines malveillants connus
- empêcher l'accès aux sites de phishing
- appliquer des règles de conformité propres à l'organisation

## Scénarios de test prévus

- Tentative d'accès à des domaines malveillants connus
- Observation de la page de blocage affichée par Cisco Umbrella
- Vérification des journaux de sécurité dans la console Umbrella

## Compétences visées

Sécurité réseau, sécurité DNS, sécurité cloud, conception de politiques de sécurité, documentation technique.

## Avertissement

Ce dépôt décrit la démarche et l'architecture d'un lab Cisco Umbrella, mais ne contient pas encore de captures d'écran ni de compte rendu de déploiement réel. Il sera complété avec les preuves de mise en œuvre (captures, journaux, résultats de test) dès qu'elles seront disponibles.

## Auteur

Hyppolyte Gbedo
Licence Informatique, Université de Rennes 1
Orienté SOC et cybersécurité
GitHub [gbehyppolyte-sec](https://github.com/gbehyppolyte-sec)
