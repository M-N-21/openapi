#Projet open-api avec admin app

Etant donné que c'est un projet springboot avec la version `2.7.3` et avec un java `1.8`, il est necessaire d'ajouter la dépendance suivante au niveau du pom.xml pour qu'on puisse accéder à `open-api`.
```
<dependency>
  <groupId>org.springdoc</groupId>
	<artifactId>springdoc-openapi-ui</artifactId>
	<version>1.7.0</version> <!-- Assurez-vous de vérifier la dernière version disponible -->
</dependency>

```
En suite une fois que maven met à jour les dépendances, nous pouvons exécuter notre application et trouver les descriptions OpenAPI dans `/v3/api-docs`. Mais nous avons modifié le port en `8081` et le chemin des descriptions de `OpenApi` dans `application.yml`
```
springdoc:
  api-docs:
    path: /api-docs

server:
  port: 8081

```
Ce qui fait pour y accéder on tape l'url suivante: `http://localhost:8081/api-docs`. En plus de ça nous pouvons intégrer springdoc-openapi à Swagger UI pour interagir avec notre spécification API et exercer les points de terminaison (tester les endpoints) avec l'url suivante: `http://localhost:8081/swagger-ui/index.html`

### Capture de api-docs

![image1jkhkghjkhjkhk](https://github.com/M-N-21/GestionImpotSpringBoot/blob/master/src/main/resources/captures/apidocs.PNG)

### Capture de swagger

![image1jkhkghjkhjkhk](https://github.com/M-N-21/GestionImpotSpringBoot/blob/master/src/main/resources/captures/swagger.PNG)

