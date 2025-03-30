#Image de base
FROM amazoncorretto:17-alpine

#Copier tous les fichiers .jar du dossier target dans le fichier app.jar
COPY target/*.jar app.jar 

# Exposer le port 8080
EXPOSE 8080

#Exécute la commande java -jar app.jar
ENTRYPOINT [ "java", "-jar", "app.jar" ]