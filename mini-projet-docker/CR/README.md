Conteneurisation des micro services backend Spring Boot et la bdd MySQL.

![alt text](image.png)

Après un docker images on a bien l’image créée.

![alt text](image-1.png)

Après un docker-compose up -d

![alt text](image-2.png)

Après un docker ps

![alt text](image-3.png)


On voit que les micro-services tournent.

Quand on regarde les logs du container on voit que le service a bien démarré.

![alt text](image-4.png)

On teste le conteneur via un navigateur c’est ok.

![alt text](image-5.png)

J’ai créé un profil avec les coordonnées suivantes :
m.dubois@test.fr
Marianne

![alt text](image-6.png)

Je viens de créer un nouveau profil.

![alt text](image-7.png)

![alt text](image-8.png)

![alt text](image-9.png)

Ceci valide la première partie conteneurisation et test des micro services.

Registre Docker :
Création d’un registre privé : 
J’ai créé un registre privé nommé registry qui tourne sur localhost:6565.

![alt text](image-10.png)

Création des images backend et MySQL :
-Backend :

![alt text](image-11.png)

![alt text](image-12.png)

Pousse de l’image dans le registre privé :

![alt text](image-13.png)

-MySQL
Avec un docker tag mysql:8.0 localhsot:6565/mysql, on taggue l’image pour le registre privé.

![alt text](image-14.png)
![alt text](image-15.png)

Quand on consulte le registre privé on voit qu’on a bien les deux images présentes.

![alt text](image-16.png)

Après avoir mis en place un registre privé avec les deux images paymybuddy-backend et mysql, on va les utiliser dans notre docker-compose pour builder et déployer l’application.

![alt text](image-17.png)

Si on regarde les logs des conteneurs paymybuddy-backend et mysql, on voit que tout est ok.

![alt text](image-18.png)

![alt text](image-19.png)

Après test sur le navigateur le build et le déploiement sont ok.

![alt text](image-20.png)

![alt text](image-21.png)