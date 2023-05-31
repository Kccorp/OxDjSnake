# OxDjSnake
Ce challenge est orienté stéganographie. Il consiste à retrouver et décoder un message caché dans un contenu audio.

## Scénario

J'adore la musique regarde un peu ma dernière compo. Ecoute-moi ça dans les détails tu vas voir ça décoiffe. Ah et je ne maitrise pas encore bien les percussions j'espère que ça ne va pas trop te déranger.

## Writ-up
L'utilisateur devra télécharger le fichier son il entend un Rick Roll et dans le fond des touches de téléphone mais rick roll est trop fort pour que les touches soient audibles.

On va alors devoir séparer les touches de la musique.

Après un premier passage dans audacity nous obtenons ça 

![image](https://user-images.githubusercontent.com/85285247/232776624-6fda6c04-b4ac-4976-8f60-8cdf26d4c7d5.png)

Nous essayons donc de le séparer en téléchargeant Rick Roll de base sur youtube et en soustraiyant les deux pistes audio comme ceci :
- ajouter les deux pistes dans audacity 
- sélectionner la piste fraichement télécharger 
- Aller dans effet>spécial>inversé 
- Sélectionner maintenant les deux pistes 
- Aller dans Pistes>Mix>Mixage et rendu 

Voilà les deux pistes sont soustraites, cependant, nous devons au préalable modifier le gains de la piste téléchargée sur Youtube et après plusieurs tests nous trouvons que le gain doit être de +15db 

Nous obtenons alors le spectre suivant

![image](https://user-images.githubusercontent.com/85285247/232773543-f1c8dd59-a9aa-4ca1-859d-daca736c6eb8.png)

Il ne nous reste plus qu'a décoder le message 
Après recherche nous savons que le code est généré en DTMF et donc uniquement des chiffres possitifs.
Nous analysons chaque numéro et nous trouvons qu'il n'y a que des 0 et des 1.

Nous relevons alors chaque numéro comme cela :
![image](https://user-images.githubusercontent.com/85285247/232788607-8fcdc2f1-67ce-49d3-a5a2-3b5144119705.png)

Et nous trouvons alors cette suite binaire : 01 0000 11 00 1101 00 01 1011 00 01 1011 00 00 1100 10 01 0000 01 01 1000 11 01 0101 00 01 1010 01 01 1011 11 01 1011 10 
Qui une fois convertie en asci nous obtenons : C4ll2AcTion

Et alors ce qui nous donne notre flag : 0xD{C4ll2AcTion}

