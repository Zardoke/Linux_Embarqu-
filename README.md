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







