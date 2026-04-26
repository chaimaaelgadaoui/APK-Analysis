README – LAB 4 : Analyse Statique d’un APK
Auteur

Chaimaa ELGADAOUI
Étudiante en 
## Description du projet

Ce projet s’inscrit dans le cadre d’un laboratoire pratique dédié à l’analyse statique des applications Android (APK).

L’objectif principal est d’examiner une application Android sans l’exécuter, afin d’identifier :

sa structure interne
ses composants
ses permissions
et d’éventuelles vulnérabilités de sécurité

Cette analyse a été réalisée dans un environnement contrôlé à des fins pédagogiques uniquement.

## Objectifs du LAB
-Comprendre la structure d’un fichier APK (DEX, Manifest, ressources…)
-Analyser le fichier AndroidManifest.xml
-Décompiler une application avec JADX GUI
-Convertir des fichiers DEX → JAR avec dex2jar
-Explorer le code avec JD-GUI
-Identifier des vulnérabilités potentielles :
     -clés API exposées
     -données sensibles en clair
     -configurations dangereuses

## Structure du projet
APK-Analysis/
│
├── app-debug.apk          # APK analysé
├── dex_out/               # Fichiers DEX extraits
├── app.jar                # Fichier converti
├── results/
│   ├── rapport.md         # Rapport d’audit
│
└── README.md              # Ce fichier
## Étapes réalisées
![Préparation de l'environnement](images/preparation.png)
