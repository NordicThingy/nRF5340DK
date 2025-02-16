# Connexion entre entre le Thingy:91 et le nRF5340DK pour transmettre les données vers un serveur flask

Ce dossier permet de configurer une carte nRF5340DK pour recevoir les données de n'importe quel Thingy:91 et de les transmettre à un ordinateur

**Matériel nécessaire:**
- nRF5340DK
- Thingy:91
- Visual Studio Code

**Installation et Configuration:**
Pour exécuter ce projet, vous devez installer et configurer Visual Studio Code (VS Code). 

Note : Assurez-vous que la chaîne d'outils (Toolchain) et le SDK sont installés sur le disque C:\ de l'ordinateur, dans un dossier dédié. Le dossier contenant le code pour le Thingy:91 doit également être placé dans un dossier de programmation sur le disque C:\.

Suivez les étapes ci-dessous pour la configuration :
1. Installation des outils en ligne de commande nRF
  - Téléchargez et installez les nRF Command Line Tools depuis le lien suivant : https://www.nordicsemi.com/Products/Development-tools/nRF-Command-Line-Tools/Download.
  - Les nRF Command Line Tools incluent nrfjprog, un outil essentiel pour flasher le firmware sur vos kits de développement Nordic.

2. Installation de Visual Studio Code
  - Rendez-vous sur https://code.visualstudio.com/download et installez la version de VS Code correspondant à votre système d'exploitation.

3. Installation du nRF Connect Extension Pack dans VS Code
  - Dans la barre d'activités de VS Code, cliquez sur l'icône Extensions.
  - Recherchez nRF Connect for VS Code Extension Pack, puis cliquez sur Installer.

Le nRF Connect Extension Pack dans VS Code permet de :
  - Développer, créer, déboguer et déployer des applications embarquées basées sur le SDK nRF Connect.
  - Interagir avec le compilateur, l'éditeur de liens, le système de construction complet, un débogueur compatible RTOS, et le SDK nRF Connect.
  - Utiliser un éditeur visuel pour les fichiers Devicetree et un terminal série intégré.

4. Installation de la chaîne d'outils (Toolchain) sur VS Code
- Lors du premier lancement de l'extension nRF Connect for VS Code (cliquez sur l'extension dans la barre de gauche), vous serez invité à installer une Toolchain. Si aucune n'est détectée, procédez ainsi :
    - Cliquez sur Installer la Toolchain.
    - Choisissez une version compatible avec la version du SDK nRF Connect que vous utiliserez (la dernière version recommandée).
    - L'installation peut prendre quelques minutes.

5. Installation du SDK nRF Connect
Dans nRF Connect pour VS Code, cliquez sur Gérer le SDK.
Dans cette section, vous pourrez installer, désinstaller et sélectionner la version active du SDK.
- Cliquez sur Installer le SDK pour afficher les versions disponibles et choisir celle que vous souhaitez utiliser et installer la, le mieux est de sélectionner la dernière sans parenthèse.
- Une fois ces étapes terminées, votre environnement est prêt pour le développement avec le SDK nRF Connect et Visual Studio Code.


**Utilisation du code:**
1. Chargement du code
- Ouvrir VS Code
- Télécharger et décompresser le dossier, puis ouvrez le dossier contenant le code dans VS Code (nRF5340DK).

2. Build du code :
- Dans l'extension nRF Connect dans la barre d'activité, cliquez sur Add Build Configuration.
- Dans Board Target, choisissez nrf5340dk/nrf5340/cpuapp/ns.
- Cliquez sur Build Configuration et attendez la fin du processus de compilation.

**Envoi du code au nRF5340DK**
- Connectez la carte Thingy:91 à votre ordinateur via un câble micro-USB en le branchant sur le port situé sur la largeur du module.
- Allumez la carte avec le bouton ON/OFF.
- Dans VS Code => Section nRF Connect, vérifiez que le module est bien détecté dans "Connected Devices"
- Appuyez dans la catégorie Actions => Flash
- Vous avez maintenant accès aux données via le nRF5340DK
