# OxDjSnake
Ce challenge est orienté stéganographie. Il consiste a retrouver et décoder un message cacher dans un contenu audio.

## Scénario

J'adore la musique regarde un peu ma dernière compo. Ecoute-moi ça dans les détails tu va voir ça décoiffe. Ah et je ne maitrise pas encore bien les percussions j'espère que ça ne va pas trop de deranger.

## Writ-up
L'utilisateur devra télécharger le fichier son il entent un Rick Roll et dans le fond des touches de téléphone mais rick roll est trop ford pour que les touches soit audible 

On va alors devoir séparer les touches de la musique.

Apres un premier passage dans audacity nous obtenons ça 

![image](https://user-images.githubusercontent.com/85285247/232776624-6fda6c04-b4ac-4976-8f60-8cdf26d4c7d5.png)

Nous essayons donc de le séparer en téléchargeant Rick Roll de base sur youtube et soustraire les deux pistes audio comme ceci :
- ajouter les deux pistes dans audacity 
- sélectionner la piste fraichement télécharger 
- Allez dans effet>spécial>inversé 
- Sélectionner maintenant les deux pistes 
- Allez dans Pistes>Mix>Mixage et rendu 

Voila les deux pistes sont soustraite, cependant, nous devons au préalable modifier le gains de la piste téléchargé sur Youtube et apres des test nous trouvons qu'il dois être de +15db 

Nous obtenons alors le spectre suivant

![image](https://user-images.githubusercontent.com/85285247/232773543-f1c8dd59-a9aa-4ca1-859d-daca736c6eb8.png)

Il ne nous reste plus qu'a décoder le message 

