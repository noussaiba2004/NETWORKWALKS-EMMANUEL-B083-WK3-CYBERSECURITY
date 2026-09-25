# Test d'Intrusion : Cassage de Mot de Passe & Extraction de Hash (Semaine 3)

## 📌 Présentation du Projet
Ce dépôt contient la documentation des laboratoires pratiques de la Semaine 3 du programme de cybersécurité Networkwalks. L'objectif était de démontrer les vulnérabilités des mots de passe faibles en extrayant des empreintes cryptographiques (hashes) à partir de documents PDF verrouillés et en récupérant les mots de passe en clair via des attaques par dictionnaire.

## 🚀 Modules Complétés
*   **W3-PM1 (Password Cracking avec JTR) :** Utilisation de l'outil standard John the Ripper (JTR) via l'interface graphique Johnny installée nativement sur Kali Linux.
*   **W3-PM2 (Password Cracking avec les outils NW) :** Utilisation du calculateur de hash et de l'environnement d'attaque par dictionnaire web de Networkwalks.

## 🛠️ Outils & Technologies
*   **Environnement :** Machine physique Kali Linux.
*   **Outils Locaux :** Terminal Linux, John the Ripper, interface graphique Johnny.
*   **Outils Web :** OnlineHashCrack.com, Networkwalks Hash Calculator & Password Cracker.
*   **Cible :** Fichier protégé `My-Locked-PDF1.pdf`.

## 📝 Étapes d'Exécution et Méthodologie

### Approche 1 : Cassage Local avec John the Ripper & Johnny GUI (W3-PM1)
1.  **Extraction du Hash :** Le fichier PDF a été soumis à un outil d'extraction, générant une empreinte compatible avec le format `$pdf$`.
2.  **Préparation du Fichier :** Création du fichier `hash1.txt` contenant l'empreinte via le terminal.
3.  **Cassage :** L'interface Johnny a été configurée pour cibler l'exécutable natif de John the Ripper. L'attaque par dictionnaire a testé une liste de mots courants et a révélé le mot de passe en clair : `password1`.

### Approche 2 : Cassage Web (W3-PM2)
1.  **Analyse du Hash :** Importation du PDF dans le calculateur de hash de Networkwalks.
2.  **Attaque par Dictionnaire :** Soumission du hash dans l'outil Password Cracker. La correspondance a confirmé le mot de passe `password1`.

### 🏁 Capture du Flag
En utilisant le mot de passe faible récupéré, la protection d'accès du document PDF a pu être contournée avec succès.

![Saisie du mot de passe](unlock.png)

L'ouverture du document a révélé le message de félicitations et le flag caché validant l'exercice.

![Flag capturé](Done.png)

**Flag capturé :** `nw{networkwalks_flag1_jtr_270521_1}`

## 📊 Conclusion
Cet exercice démontre de manière pratique la vulnérabilité critique des mots de passe basés sur le dictionnaire. En tant qu'étudiante en Master de Cryptographie et Sécurité de l'Information, ce laboratoire illustre concrètement que même les normes de chiffrement mathématiques les plus robustes sont instantanément rendues inutiles si le mot de passe sous-jacent (le facteur humain) manque d'entropie et de complexité.

## ⚠️ Clause de Non-Responsabilité
Toutes les activités documentées dans ce projet ont été réalisées strictement à des fins éducatives dans le cadre d'un environnement de laboratoire autorisé et simulé.
