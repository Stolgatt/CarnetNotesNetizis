# CarnetNotesNetizis
Document journalisation travail Netizis Stage 2A



## Migration Sites Internet

### OVH vs O2switch

- Plus accessible (CPanel plus clair, plus facile d'utilisation et plus fournis)
- Coûts plus faibles
- création de lunes pour isoler les site avec des versions PHP incompatibles

### Protocole migration sites Joomla!

-> Sites vitrine 

1. se connecter au BO du site et désactiver les accès utilisateur pour éviter les modifications pendant la migration
2. se connecter à Plesk (le CPanel d'OVH) et télécharger la base de données du site
3. Télécharger les fichiers source du site :
   a. soit en allant chercher sur Plesk les informations de connexion en FTP et en utilisant FileZilla (majorité des sites traités comme ça)
   b. soit en créant une archive des dossiers et fichiers, directement sur Plesk et en téléchargant cette archive, qui est ensuite uploadée comme simple fichier sur O2switch
4. se connecter sur O2switch à la bonne lune (déterminée par Laurine selon le site)
5. crééer le domaine associé au site internet à migrer sur le nouveau serveur ainsi que la base de données de ce site, avec un user associé
6. uploader les fichiers sur O2switch, soit via filezilla soit via l'upload de l'archive puis son extraction
7. modifier le fichier de configuration pour y renseigner les informations de la nouvelles base de données ainsi que les nouveaux chemins des fichiers de log et tmp
8. se connecter sur un navigateur au serveur de test et ouvrir le site migré
9. effectuer sur le back office la réinstallation de la versiona ctuelle de Joomla! ou sa mise à niveau selon le site, et mettre à jour les extensions (SPPage Builder par exemple)
10. Effectuer toutes les corrections nécéssaires (fichier corrompus (très fréquents avec Filezilla), jamais avec les archives, problèmes de version, de template, d'images, etc.)
11. mettre le site en prod et demander à Laurine de changer les DNS et le SSL
12. Dès que les DNS se sont propagés, retourner sur le BO du site pour réactiver les utilisateurs
13. Résoudre les éventuels problèmes restants visible ou rapportés par les clients

### Protocole migration sites Prestashop

-> Sites e-commerce

