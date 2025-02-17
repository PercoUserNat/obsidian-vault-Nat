---
created: 2025-02-10T11:39
updated: 2025-02-10T11:39
---
D'accord ! Je vais te guider étape par étape pour utiliser **GitHub** afin de synchroniser tes notes Obsidian avec **Git**. Si tu n'as pas l'habitude d'utiliser GitHub, il y a quelques étapes à suivre, mais ne t'inquiète pas, je vais détailler tout le processus pour toi.

### Étape 1 : Créer un compte GitHub

1. Va sur [GitHub.com](https://github.com/).
2. Clique sur **Sign up** (S'inscrire) et remplis les informations nécessaires pour créer ton compte.
3. Une fois que ton compte est créé, connecte-toi à GitHub.

### Étape 2 : Créer un dépôt (repository) GitHub

4. Sur ta page d'accueil GitHub, clique sur le bouton **+** dans le coin supérieur droit, puis sur **New repository** (Nouveau dépôt).
5. Remplis les informations suivantes :
    - **Repository name** : Donne un nom à ton dépôt, par exemple "obsidian-vault".
    - **Description** : Tu peux mettre une brève description de ton projet, mais ce n'est pas obligatoire.
    - **Privacy** : Choisis **Private** (Privé) pour garder tes notes privées.
6. Clique sur **Create repository** pour créer ton dépôt.

### Étape 3 : Installer Git sur ton ordinateur

Si tu n'as pas encore installé Git sur ton PC, voici comment faire :

7. Va sur [Git-scm.com](https://git-scm.com/) et télécharge la dernière version de Git pour ton système d'exploitation (Windows, macOS ou Linux).
8. Suis les instructions d'installation. Une fois l'installation terminée, vérifie si Git est installé en ouvrant un terminal (ou une invite de commande) et en tapant cette commande :
    
    ```bash
    git --version
    ```
    
    Si Git est bien installé, tu devrais voir une version s'afficher.

### Étape 4 : Initialiser ton dépôt Git local

9. Ouvre un terminal ou une invite de commande.
10. Navigue jusqu’au dossier de ton Vault Obsidian. Par exemple, si ton Vault se trouve dans le dossier **Documents/Obsidian**, tape cette commande :
    
    ```bash
    cd Documents/Obsidian
    ```
    
11. Initialise un dépôt Git local :
    
    ```bash
    git init
    ```
    
12. Ajoute tous les fichiers dans le dépôt local :
    
    ```bash
    git add .
    ```
    
13. Fais un premier commit pour enregistrer l'état actuel de ton Vault :
    
    ```bash
    git commit -m "Premier commit de mon Vault Obsidian"
    ```
    

### Étape 5 : Lier ton dépôt local à GitHub

Maintenant que tu as un dépôt Git local, tu dois le connecter à ton dépôt GitHub.

14. Sur GitHub, tu devrais voir une page avec des instructions pour connecter ton dépôt local à GitHub. Sous la section "…or push an existing repository from the command line", copie l'URL du dépôt distant (cela ressemble à quelque chose comme `https://github.com/ton_nom_utilisateur/obsidian-vault.git`).
    
15. Dans ton terminal, ajoute l'URL de ton dépôt GitHub comme dépôt distant avec la commande suivante :
    
    ```bash
    git remote add origin https://github.com/ton_nom_utilisateur/obsidian-vault.git
    ```
    
16. Ensuite, pousse ton dépôt local vers GitHub :
    
    ```bash
    git push -u origin master
    ```
    
    Si tout va bien, tes notes Obsidian devraient maintenant être stockées sur GitHub.
    

### Étape 6 : Cloner ton dépôt sur un autre appareil

Si tu veux synchroniser tes notes Obsidian sur un autre appareil, tu dois cloner ton dépôt GitHub.

17. Sur ton autre appareil, installe Git si ce n'est pas déjà fait.
18. Ouvre un terminal et va dans le dossier où tu veux cloner ton dépôt (par exemple **Documents**).
19. Utilise cette commande pour cloner ton dépôt GitHub :
    
    ```bash
    git clone https://github.com/ton_nom_utilisateur/obsidian-vault.git
    ```
    
    Remplace l'URL par l'URL exacte de ton dépôt sur GitHub.

Cela va télécharger toutes tes notes Obsidian sur ton nouvel appareil.

### Étape 7 : Synchroniser tes modifications entre appareils

20. Sur l'appareil où tu as effectué des modifications, ouvre un terminal dans ton dossier **Vault** et ajoute les fichiers modifiés :
    
    ```bash
    git add .
    ```
    
21. Fais un commit avec un message décrivant tes changements :
    
    ```bash
    git commit -m "Ajout de nouvelles notes"
    ```
    
22. Pousse les changements sur GitHub :
    
    ```bash
    git push
    ```
    
23. Sur ton autre appareil, ouvre un terminal dans ton dossier Vault et récupère les dernières modifications :
    
    ```bash
    git pull
    ```
    

Tu peux répéter ces étapes à chaque fois que tu veux synchroniser tes notes entre les appareils.

---

### Résumé des commandes principales :

- **Initialiser un dépôt Git** dans ton Vault :
    
    ```bash
    git init
    ```
    
- **Ajouter tous les fichiers** au dépôt Git :
    
    ```bash
    git add .
    ```
    
- **Faire un commit** pour enregistrer les modifications :
    
    ```bash
    git commit -m "Message de ton choix"
    ```
    
- **Pousser les changements vers GitHub** :
    
    ```bash
    git push
    ```
    
- **Tirer les dernières modifications depuis GitHub** :
    
    ```bash
    git pull
    ```
    

---

Cela peut sembler un peu complexe au début, mais avec ces étapes, tu vas pouvoir synchroniser tes notes Obsidian sur tous tes appareils avec GitHub. Si tu rencontres des problèmes ou si tu as besoin d'éclaircissements, n'hésite pas à demander !