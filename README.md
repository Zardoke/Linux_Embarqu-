# Linux_Embarqué
<h1>1 Prise en main</h1>
<h2>1.1 Préparation de la carte SD</h2>
- Téléchargement "TP_linux.zip"
- Zipper "TP_linux.zip"
- Installation du logiciel Win32DiskImager </br>
Nous disposons d'une carte microSD de 4GB. Le disquede la microSD est partition en 3. On utilise l'image VEEK_MT2S_LXDE/VEEK_MT2S_LXDE.img  </br>

![image](https://github.com/Zardoke/Linux_Embarqu-/assets/144770542/1f6053ec-41dd-4afa-be3a-8c92fd944776) </br>
![image](https://github.com/Zardoke/Linux_Embarqu-/assets/144770542/9e8b31c6-0956-4057-8ef4-cc0123fdee48) </br>

<h2>1.2 Démarrage</h2>
Maintenant qu'on a flasher la carte SD.On insérez la carte SD fraichement programmée, branchez la carte VEEK-MT2S et
allumez-la : bouton rouge ! Ça clignote de partout et un linux se lance.

<h2>1.3 Connexion au système</h2>
<h3>1.3.1 Liaison série</h3>
On configure le port série sur le pc fixe de l'école sur linux.
- Branchement du port USB sur le PC fixe
- Démarage du noyaux linux
- Récupération de l'adresse IP de notre carte

<h3>1.3.2 Utilisez un logiciel de liaison série</h3>
<h3>1.3.3 Configuration réseau</h3><br>
- Après avoir Brancher la carte VEEK sur le switch via un câble réseau.
L'adresse IP est "192.168.88.72". Nous avons besoin de l'adresse IP de la carte pour nous connecter en SSH du réseau de la salle D060 (2HZ ou 5HZ).
On ouvre Tera Term.

![image](https://github.com/Zardoke/Linux_Embarqu-/assets/144770542/5665eab8-6811-42dd-86a6-b7cada56544c)<br>
![image](https://github.com/Zardoke/Linux_Embarqu-/assets/144770542/a5a9b624-bfd7-4bd0-9772-5420f4a0f3ef)<br>
![image](https://github.com/Zardoke/Linux_Embarqu-/assets/144770542/c5bd599b-0f6d-4339-aae7-954378bfbf9a)<br>
On tape alors la commande "ifconfig" pour connaitre la configuration de notre carte.
![image](https://github.com/Zardoke/Linux_Embarqu-/assets/144770542/966db5c2-3f93-4b2b-9bd9-f28907c7c337)<br>

![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/180d23c4-79fd-47d7-9958-b551fc8cf1ab)<br>
![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/fb17fbc8-00bf-42fa-92bf-650f3d0cc1ee)<br>
![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/f320432e-5cea-404d-aca7-c24141492d44)<br>
On reboot avec la commande "reboot"
Après avoir reboot la carte, on vérifie l'adresse IP sur le PC fixe avec la commande "ifconfig" (bien branché la carte en USB)<br>
![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/a8fc653e-26e4-45ee-9fb6-21453af92674)<br>
On a bien dans le fichier /etc/ssh/sshd_config, la ligne suivante est
présente :"PermitEmptyPasswords yes"<br>
![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/a16ba886-490e-417f-b066-9c8da6a39a7d)<br>
Pour quitter le fichier on fait ":wq" puis on appuie sur entrer. <br>

On est déjà loggé en ssh sur la carte VEEK, avec Tera Term dans notre cas, et donc on utilise pas non plus le port série.


<h2>1.4 Découverte de la cible</h2>
<h3>1.4.1 Exploration des dossiers /sys/class et /proc</h3>
Explorons un peu votre environnement:
- Répertoires présent sous la racine

![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/52103ce8-0883-4c2a-9447-7ee739392c68)<br>

<h3>1.4.2 Compilation croisée</h3>
Après avoir téléchargé Oracle VM VirtualBox (V7.0.18), on importe la VM "VM-SOC-2019.ova" dans le dossier dizzipé de moodle.
Avant de lancer la VM on viens la configurer et cloner le github créer avec Github Destop.

![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/a9722051-a116-49f3-a14e-6ce5fe3f9064)<br>
![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/33dec82b-66ed-4845-9ad7-e1ef13ee2a26)<br>
On vient alors lancer la VM <br>
![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/95fd4ab4-f110-4c74-8b3e-be09f61660ae)<br>
![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/f5872c33-846f-4bac-a750-534d83b937f9)<br>

![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/26c54f30-909e-4b07-8f11-3621e9b28c3d)<br>
![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/8fc5bbaa-7916-4ba7-ba0c-597620695427)<br>

<h3>1.4.3 Hello world !</h3>

![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/73c5c860-bc86-4a96-b569-c9eb5c361192)<br>










