# Pitch Deck Ntp Int Pi Game  

Concept d’un projet pour un client, utilisable dans un cours sur Unity3D, utilisant 4+ Quest 3 et un Raspberry Pi en local.  

Dans le cadre du concept proposé pour un client, nous allons développer un **serious game** sous Unity3D.  
Ce projet est permettre, aussi, la réalisation d’un atelier d’apprentissage Unity3D orienté game design et développement, en créant un jeu en réseau **sans nécessiter l’apprentissage préalable de la partie réseau**.  

Ce document est un pitch deck décrivant le concept.  

Ce pitch deck est public et sert de base pour un Game Concept Document (GCD) technique de l’idée.  
Cependant, il ne contient et ne contiendra pas de données spécifiques au projet actuellement en cours.  

Sur ce, si vous souhaitez réaliser cet atelier de votre côté pour apprendre Unity3D sur Quest 3 à travers un jeu **partiellement en réseau**, vous êtes le bienvenu !  

----------------------



**Matériel nécessaire :**  
- Un Raspberry Pi 5: 75€ ou 150€ ([Info](https://github.com/EloiStree/HelloInput/issues/308))
- Un routeur Wi-Fi 6 de bonne qualité: 70€  ([Info](https://github.com/EloiStree/HelloInput/issues/310))
- Quatre Quest 3 ou Quest 3S pour l'atelier 330€ x 4  ([Info](https://github.com/EloiStree/HelloInput/issues/311))
  - Une pour le développeur
- Quatre BoboVR pour faire tenir le casque en QR: 70€ x 4 ([Info](https://github.com/EloiStree/HelloInput/issues/312))
- Un mini PC Window pour le moniteur de l'atelier: 200€ ([Info](https://github.com/EloiStree/HelloInput/issues/313))
- Optionnel: Un grand écran pour afficher la vue d'un des joueurs.
- Pas de manette en jeu pour éviter les risques de casse avec les enfants
- Une Flybox pour transporter le matériel : environ 400€.

Coût approximatif : 2500€.

**Code nécessaire**:
- Sur le Raspberry Pi 5:
  - Un serveur NTP local sur Raspberry Pi pour syncroniser le temps des casques
  - Un serveur Flask permettant de débugger le Raspberry Pi
  - Un serveur Websocket IID pour permettre la transmission des évènements en jeu entre les casques
- Sur le Quest3, hors code dédier au Quest3:
  - Un code pour se synchroniser sur le NTP
  - Un code pour envoyé et recevoir des évènements entier avec IID
  - Un code de stoquage de clé RSA
    - pour identifier les casques si plusieurs jeux sur le même réseaux e
    - pour éviter des saboteurs extérieurs à la partie en cours


**Concept de base du jeu:**

Le méchanisme du jeu est un mélange de [22 Minutes pour sauver l'univers](https://www.youtube.com/watch?v=Ss6vLmLcCbU&t=471s) et [Keep Talking And Nobody Explodes](https://www.youtube.com/results?search_query=Keep+Talking+And+Nobody+Explodes) avec une touche de [Starship Home](https://www.youtube.com/results?search_query=Starship+home).   

Le jeu "multi-joueur" en réalité semi-augmentée est un groupe d'énigmes à résoudre à travers des mini-jeux liés par le temps qui s'écoule, d'où l'utilisation d'un serveur NTP.   
Les joueurs ont la capacité d'interagir via une transmission d'événements sans paramètres.   

Recommencez autant de fois que nécessaire les niveaux de 5 minutes avec le groupe pour permettre de résoudre les énigmes et la trame de fond.  
Chaque mini-jeu permet de tester les aptitudes des joueurs.    

Si vous connaissez la solution et que vous travaillez en groupe, vous devriez être capable de finir le jeu.  
(Être solitaire permet d'explorer la majorité des énigmes, mais la solution finale nécessite un travail de groupe).  

Comme pour **22 Minutes pour sauver l'univers**, c'est la capacité à comprendre ces énigmes qui permet de finir le jeu.

**Warning** :  
- On va éviter les portails, par contre, car c'est un sujet qui peut vite devenir compliqué pour de nombreuses raisons.  
  - Vous pouvez ajouter des portails si :  
    - Ceux-ci ne nécessitent pas de changer les paramètres du projet Unity3D.  
    - Ceux-ci sont fournis dans la bibliothèque de Quest 3.  
      - Attention, avec le temps, le portail sera l'une des premières choses à devenir obsolètes avec Unity3D.


Si vous désirez "modder" le code de base pour apprendre Unity3D.
- Un menu développeur vous est disponible pour simuler les évènements d'autres joueurs.
- Votre niveau doit se calquer sur le temps du jeu que vous modder
- votre niveau doit savoir se jouer en solitaire pour résoudre l'énigme de votre niveau.
  - Il peut contenir des énigmes secondaires (utilisant la partie multijoueur évènementiel)
  - Défit: Permetter d'amicalement mettre en avant une aptitude naturel du joueur.
- Il n'y a pas de fichier mémorie dans le jeu, c'est le joueur qui doit apprendre

# Vidéo d'inspiration

22 Minutes pour souver le monde  
[![image](https://github.com/user-attachments/assets/1ae016ba-7135-4b04-9b9b-5328e0651d04)](https://www.youtube.com/results?search_query=22+minute+pour+sauver+le+monde)  
[https://www.youtube.com/results?search_query=22+minute+pour+sauver+le+monde](https://www.youtube.com/results?search_query=22+minute+pour+sauver+le+monde)  

Keep Talking and Nobody Explodes  
[![image](https://github.com/user-attachments/assets/eaa83481-03d9-4cd9-90a4-9da44b224949)](https://www.youtube.com/results?search_query=Keep+Talking+And+Nobody+Explodes)  
[https://www.youtube.com/results?search_query=Keep+Talking+And+Nobody+Explodes](https://www.youtube.com/results?search_query=Keep+Talking+And+Nobody+Explodes)  

Spaceship Home   
[![image](https://github.com/user-attachments/assets/b8d71117-c9f0-464e-91ae-95580c632b1b)](https://youtu.be/6fTJKnT8neA?t=167)  
[https://youtu.be/6fTJKnT8neA?t=167](https://youtu.be/6fTJKnT8neA?t=167)  


# Calibration d'une pièce

Si le projet est dédié à une pièce unique :  
[![image](https://github.com/user-attachments/assets/49bd1545-c7b5-4668-a4d5-3970b6176d72)](https://youtu.be/0k1kqoNi4UM?t=272)  
https://youtu.be/0k1kqoNi4UM?t=272  
- Vous pouvez utiliser la triangulation, comme montré dans cette vidéo.

Si le projet est dédié à une pièce avec des murs, des tables, des sols et un scan de la pièce :  
- Vous pouvez calibrer le niveau avec les meshes de la pièce fournis par le Quest 3.

Sans scan de la pièce :  
- Vous pouvez demander au joueur de charger le niveau en posant ses mains sur le sol, la table ou le mur.  
- La distance entre les mains détermine le niveau à charger par rapport à la position des mains.

Au plus simple :  
- Le joueur choisit le niveau qu'il veut essayer de résoudre en attendant que le moniteur lance le jeu.  
- Le niveau se charge sur un élément flottant dans un rayon maximal de 2 mètres
  - Il est peut-être déplacé, mais comme l'atelier est destiné à des développeurs juniors, il n'est pas agrandissable.
  - Voir [Bam](https://youtu.be/mX9UK0FXwaE?t=1)  
[![image](https://github.com/user-attachments/assets/9585a99c-2752-4893-a5e9-b8163cd4fddd)](https://youtu.be/mX9UK0FXwaE?t=1)  
https://youtu.be/mX9UK0FXwaE?t=1  



# Video d'inspiration AR

|  |  |  |  |
|---|---|---|---|
| [![image](https://github.com/user-attachments/assets/33c47314-b461-4e87-87eb-8c962a3bbffb)](https://www.youtube.com/watch?v=8hozDugbX28) | [![image](https://github.com/user-attachments/assets/1a1b0c53-dff0-47ae-8687-44f1b0463b94)](https://www.youtube.com/shorts/y1Nl9WE2AMw) | [![image](https://github.com/user-attachments/assets/60021dd9-f38d-4db2-9afa-ee89bd372526)](https://www.youtube.com/shorts/ur_StzmHeFE) | [![image](https://github.com/user-attachments/assets/a96ca00e-6e04-44b1-98a6-2ead2d48f29a)](https://www.youtube.com/shorts/Tq9d2DeCXyc?t=26&feature=share) |

# Quest 3 SDK

Le projet est dédié au Quest3.
Vous pouvez utiliser des codes du SDK disponibles sur l'Asset Store.
[![image](https://github.com/user-attachments/assets/f93ae190-6a12-4c02-991b-700dd3a4a90f)](https://assetstore.unity.com/packages/tools/integration/meta-xr-all-in-one-sdk-269657)

Dans le projet, l'XR Interaction Toolkit est également installé.
[[https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@3.0/manual/index.html](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@3.0/manual/index.html)
![image](https://github.com/user-attachments/assets/adccfeb6-98e4-4827-b6b9-f6b5c812283a)](https://youtu.be/dCVAYB2jkEY?t=17)
[https://youtu.be/dCVAYB2jkEY?t=17](https://youtu.be/dCVAYB2jkEY?t=17)


Pour intéragir avec les objets du jeu, si vous n'avez pas un développeur senior en XR dans l'équipe, je vous conseille d'utiliser:

🤖 Unity’s **`UnityEngine.EventSystems`** namespace includes a variety of interfaces, classes, and enums designed to handle input and UI interactions in Unity.

1. **Pointer Events**:
   - `IPointerEnterHandler`: Called when the pointer enters the object.
   - `IPointerExitHandler`: Called when the pointer exits the object.
   - `IPointerDownHandler`: Called when the pointer is pressed down on the object.
   - `IPointerUpHandler`: Called when the pointer is released on the object.
   - `IPointerClickHandler`: Called when the object is clicked with the pointer.
   - `IBeginDragHandler`: Called when a drag operation starts on the object.
   - `IDragHandler`: Called continuously during a drag operation.
   - `IEndDragHandler`: Called when a drag operation ends.
   - `IDropHandler`: Called when another object is dropped on this object.
   - `IScrollHandler`: Called when scrolling (e.g., mouse scroll wheel) occurs over this object.

2. **Focus Events**:
   - `ISelectHandler`: Called when the object is selected.
   - `IDeselectHandler`: Called when the object is deselected.
   - `IMoveHandler`: Called when movement input (e.g., arrow keys or gamepad) is detected.

3. **Keyboard and Submit Events**:
   - `IUpdateSelectedHandler`: Called every frame for the currently selected object.
   - `ISubmitHandler`: Called when the submit action (e.g., pressing Enter or a controller button) is performed.
   - `ICancelHandler`: Called when the cancel action (e.g., pressing Escape or a controller button) is performed.

