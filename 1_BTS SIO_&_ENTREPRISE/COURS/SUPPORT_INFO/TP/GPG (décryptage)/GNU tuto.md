---
created: 2025-02-06T08:33
updated: 2025-02-06T11:10
---

lien dl : [GnuPG - Download](https://www.gnupg.org/download/)
___
Download Tarball and Signature

==**cmd:**== tar -xzf gnupg-2.4.7.tar.bz2

==**powershell (install scoop):**==  iwr -useb get.scoop.sh | iex 

==**cmd powershell:**== gpg --version
               scoop install gpg

___
![[Pasted image 20250206090106.png]]
J'ai crée mon fichier.txt dans l'arboresence que je voulais =>
Aller dans l'arborescence avec "cd..."
ensuite taper: *gpg --symmetric --armor textecrypt.txt

- `--symmetric` : Indique que vous souhaitez utiliser la cryptographie symétrique.
- `--armor` : Crée une sortie ASCII (texte) au lieu de binaire, ce qui est plus facile à partager.

___
screen: 
![[Pasted image 20250206092120.png]]
choisir mot de passe:   c89f7oiwh3cy7yy1gea47dq3c11uja

pour déchiffrer: ```
gpg --output textecrypt_decrypted.txt --decrypt textecrypt.txt.asc

bien changer name fichier.txt
