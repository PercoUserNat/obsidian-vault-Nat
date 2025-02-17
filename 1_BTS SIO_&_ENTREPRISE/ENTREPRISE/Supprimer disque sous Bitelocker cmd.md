---
created: 2025-02-14T14:38
updated: 2025-02-14T14:48
---
Accès menu réparation: accès CMD
### Étapes pour tenter de formater le disque sans BitLocker :

1. **Accéder à l'invite de commande en mode réparation** (comme décrit précédemment).
    
2. **Lancer Diskpart** :
    
    - Tapez :
        
        ```bash
        diskpart
        ```
        
3. **Lister les disques** :
    
    - Tapez :
        
        ```bash
        list disk
        ```
        
    - Identifiez le disque qui contient la partition protégée par BitLocker.
4. **Sélectionner le disque à formater** :
    
    - Tapez :
        
        ```bash
        select disk 0  (remplacez 0 par le numéro du disque à formater)
        ```
        
5. **Effacer le disque** :
    
    - Tapez la commande suivante pour effacer toutes les partitions du disque, y compris celles protégées par BitLocker :
        
        ```bash
        clean   ou   clean all (plus pousser mais long)
        ```
        
    
    Cette commande effacera tout sur le disque et permettra de le formater comme neuf. Attention, **toutes les données seront perdues** !
    
6. **Pour format si besoin** :
    
    - Tapez :
        
        ```bash
        format fs=ntfs quick OVERRIDE (pour format)
        ```

7. **Quitter Diskpart** :
    
    - Tapez :
        
        ```bash
        exit
        ```
        

Une fois que vous avez utilisé la commande `clean`, vous pouvez essayer de créer de nouvelles partitions et d'installer Windows à partir de zéro.



