README – LAB 4 : Analyse Statique d’un APK
Auteur

Chaimaa ELGADAOUI
Étudiante en 2ème année – Génie Cyberdéfense et Systèmes de Télécommunications Embarqués
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
├
│
│
└── README.md              # Ce fichier
## Étapes réalisées
Création de l’environnement de travail
![Préparation de l'environnement](images/preparation1.png)
Vérification de l’intégrité de l’APK (signature ZIP)
![vérification PK](images/preparation2.png)
Lister le contenu de l'APK
![vérification PK2](images/preparation3.png)
Calcul du hash SHA-256
![commande SHA256](images/preparation4.png)

## 2. Analyse de la structure

Identification des fichiers clés :

  -AndroidManifest.xml
  -classes.dex
  -resources.arsc
  -META-INF
![Structure de l'APK](images/apk_structure.png)
## 3. Analyse avec JADX GUI

Étude du manifeste (permissions, composants)
Vérification des attributs critiques :

android:exported
android:debuggable
usesCleartextTraffic

Exploration du code source
Image 1 (interface globale) :
![Interface JADX](images/jadx_interface.png)
Image 2 (manifest) :
![Analyse du manifest](images/manifest_analysis.png)

## 4. Recherche de données sensibles

Analyse basée sur des mots-clés :

    -API keys, tokens, passwords
    -URLs (HTTP/HTTPS)
    -Configurations debug/test
![Recherche de données sensibles](images/sensitive_search.png)
## 5. Conversion DEX → JAR

Extraction des fichiers DEX
Conversion avec dex2jar
Analyse complémentaire avec JD-GUI

Image 1 (dex) :
![Extraction des fichiers DEX](images/dex_files.png)

Image 2 (JD-GUI) :

![Analyse avec JD-GUI](images/jd_gui.png)

## 6. Comparaison des outils
![Comparaison des outils](images/comparaison_outils.png)