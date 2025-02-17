---
created: 2025-02-13T15:32
updated: 2025-02-13T15:34
---
script en bash qui tourne sur debian et qui s'exe 1 par semaine par le biai cron objectif: 
- donner liste de paquets à ignorer 
- faire un apt update / apt_upgrade (IGNORER LA LISTE PAQUET A IGNORER)/ apt_autoremove
- recuperer liste de ce qui a été upgrade 
- informer les applications ignorer qui sont dans la liste apt_update
- envoyer un mail récap de tout (all)