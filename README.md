# Linux_Embarqué
<h1>1 Prise en main</h1>
<h2>1.1 Préparation de la carte SD</h2>
- Téléchargement "TP_linux.zip"
- Zipper "TP_linux.zip"
- Installation du logiciel Win32DiskImager </br>
Nous disposons d'une carte microSD de 4GB. Le disque de la microSD est partition en 3. On utilise l'image VEEK_MT2S_LXDE/VEEK_MT2S_LXDE.img  </br>

![image](https://github.com/Zardoke/Linux_Embarqu-/assets/144770542/1f6053ec-41dd-4afa-be3a-8c92fd944776) </br>
![image](https://github.com/Zardoke/Linux_Embarqu-/assets/144770542/9e8b31c6-0956-4057-8ef4-cc0123fdee48) </br>

<h2>1.2 Démarrage</h2>
Maintenant qu'on a flashé la carte SD. On insère la carte SD fraichement programmée, branchez la carte VEEK-MT2S et
Allumez-la : bouton rouge ! Ça clignote de partout et un linux se lance.

<h2>1.3 Connexion au système</h2>
<h3>1.3.1 Liaison série</h3>
On configure le port série sur le pc fixe de l'école sur linux.
- Branchement du port USB sur le PC fixe
- Démarrage du noyau linux
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

On est déjà logué en ssh sur la carte VEEK, avec Tera Term dans notre cas, et donc on n’utilise pas non plus le port série.


<h2>1.4 Découverte de la cible</h2>
<h3>1.4.1 Exploration des dossiers /sys/class et /proc</h3>
Explorons un peu votre environnement:
- Répertoires présent sous la racine

![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/52103ce8-0883-4c2a-9447-7ee739392c68)<br>

<h3>1.4.2 Compilation croisée</h3>
Après avoir téléchargé Oracle VM VirtualBox (V7.0.18), on importe la VM "VM-SOC-2019.ova" dans le dossier dizzipé de moodle.
Avant de lancer la VM on vient la configurer et cloner le Github créé avec Github Destop.

![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/a9722051-a116-49f3-a14e-6ce5fe3f9064)<br>
![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/33dec82b-66ed-4845-9ad7-e1ef13ee2a26)<br>
On vient alors lancer la VM <br>
![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/95fd4ab4-f110-4c74-8b3e-be09f61660ae)<br>
![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/f5872c33-846f-4bac-a750-534d83b937f9)<br>

![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/26c54f30-909e-4b07-8f11-3621e9b28c3d)<br>
![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/8fc5bbaa-7916-4ba7-ba0c-597620695427)<br>

<h3>1.4.3 Hello world !</h3>

![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/73c5c860-bc86-4a96-b569-c9eb5c361192)<br>

<h3>Séance 2</h3>  <br>

![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/fc21cf7c-28c7-499c-a131-82f07ca01480)<br>

On vient maintenant créer un fichier "hello.c" avec Notpad++ dans notre dossier de la VM <br>
![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/cf88ce02-2d82-4d57-8808-f38e98ddd897)<br>

L'adresse IP de notre carte SOC ayant changer. On utilise la commande "ip -a" pour récupérer notre nouvelle adresse IP"192.168.88.63" dans Tera Term VT.<br>
Pour compiler sur la VM le fichier "hello.c", on utilise le cross-compilateur :
"arm-linux-gnueabihf-gcc hello.c -o hello.o"
On n’oublie pas avant d'exécuter la commande de se mettre dans le dossier "src"<br>
On vérifie dans Tera Term qu'affiche bien "Hello world !" avec la commande ".\hello.o"<br>
![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/2d9a25e3-fde9-4b79-8e9b-f832d9989632)<br>

<h3>1.4.4 Accès au matériel</h3>
Un certain nombre de drivers sont fournis. Comme tous les drivers sous Linux,
ils sont accessible sous forme de fichiers. Par exemple pour allumer l’une des LED
rouge de la carte, il suffit d’écrire un ’1’ dans le fichier brightness.
La commande "echo "1" > /sys/class/leds/fpga_led4/brightness" allume la LED 4.
Tester d’allumer et d’éteindre d’autres LED.<br>

![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/a9d841ba-0c2b-4cec-90dc-70a0ddeda049)<br>

<h3>1.4.5 Chenillard (Et oui, encore !)</h3>

![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/bfb81c54-05b0-4a6e-aa13-7530846e7082)<br>
![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/437f1856-ac37-4acc-8725-019c5d916df5)<br>

![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/5f00212e-64b4-4890-963c-6462730416b3)<br>

![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/99706b2e-5dae-4864-b185-70ae006ddca6)<br>

<h1>2 Modules kernel (TP2)</h1>
<h2>2.0 Reprise du TP1</h2>
<h2>2.1 Accès aux registres</h2>
Le but de cettte partie du TP  est de créer un programme qui accède directement aux registres depuis l’espace utilisateur.
On veut directement accéder aux registres depuis l’espace utilisateur.
Il faut en effet remapper la mémoire pour demander à l’OS de nous fournir une adresse virtuelle.
Tout les adresses son virtuelles mais vont être convertie en Hardware par le MMU.
Pour cela, on utilisera la fonction mmap()

Les limites sont tout d'abord d'un point de vu Sécurité puisqu'un utilisateur peut accéder directement aux registres matériels. Les utilisateurs malveillants ou mal informés peuvent corrompre des données, provoquer des pannes système, ou endommager le matériel.

<h2>2.2 Compilation de module noyau sur la VM</h2>

![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/de1312c7-43d0-4868-8dfe-0c71ce28e3df)<br>
![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/135b028c-f7d6-4f88-9566-dc208568dd1e)<br>
Voici le Code qui crée un effet chenillard en contrôlant les LEDs à l'aide des registres mémoire mappés.
![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/302dfc25-8c3c-46c3-af82-258e76033ce3)<br>

<h2>2.3 CrossCompilation de modules noyau</h2>

Pour compiler des modules noyau dans la VM, nous avons installé les paquets suivant :
"sudo apt install linux-headers-amd64"<br>
"sudo apt install bc"<br>
On vient aussi creer un dossier dans lequel on à dézippé le module fourni sur module.
La commande make permet de compiler notre module à partir de son code source.
![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/f5c44aff-2236-4ae2-9938-2292bd8e077a)<br>
La comamnde "modinfo": Affiche des informations sur un module du noya (sa version, son auteur, ses dépendances).<br>
lsmod: permet de lister les modules actuellement chargés dans le noyau Linux. Cela vous permet de voir quels modules sont en cours d'exécution sur votre système à un moment donné.<br>
![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/1a09121f-d355-40f9-91ae-7e68209d3684)<br>

La commannde "insmod" est utilisée pour insérer un module dans le noyau Linux.
![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/2b55d8fb-7fe9-4e15-96f3-fdfe0ac793d5)<br>

Commande "sudo rmmod" mmod est utilisée pour retirer un module du noyau Linux.<br>
![image](https://github.com/Zardoke/Linux_Embarque/assets/144770542/71abaeb9-28b7-49d8-9e5d-67f669db0d29)<br>

<h3>2.3.0 Récupération du Noyau Terasic (c’est déjà fait dans la VM !)</h3>
En ce début de séance on vérifie l'adresse IP de notre carte.
En plus d'alimenter ma carte, je l'a connecte en USB.
Puis on ouvre Tera Term, on se connecte au port série 
<h3>2.3.1 Préparation de la compilation</h3>
















