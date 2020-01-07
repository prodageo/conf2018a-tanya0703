# Premiers pas avec un microcontrôleur et Google Cloud IoT Core

## Cartouche d'identification

 - Manifestation : CodeursEnSeine 2019
 - Lieu : Kindarena - Palais des sports de Rouen
 - Conférence : Premiers pas avec un microcontrôleur et Google Cloud IoT Core
 - Horaire de la conférence : 10h00
 - Durée de la conférence : 1h
 - Conférencier :
   - Gautier Mechling (https://twitter.com/Nilhcem : Twitter, https://github.com/Nilhcem : GitHub)
 - Mots-clés : Google Cloud, Cloud IoT Core, Demo, Prototypage, MQTT, Arduino, CArduino, Capteur de température, Capteur de humidité, Site statique
 - URL de l'illustration : ![Cloud IoT Core Logo](cloudIotCoreLogo.png)

## Support
 - Plan du support : Démo

## Résumé

La conférence a été constituée par un démo dont le but était de récupérer la température ambiante et de l’envoyer vers google cloud. Pour arriver à faire cela, Gautier Mechling a montré d’abord comment connecter un Arduino avec un capteur de température sur une plaque de prototypage. Il a utilisé la feuille des spécifications pour trouver le schéma correspondant. Après il a écrit le code qui affiche la température et l'humidité chaque seconde à l’aide de l’IDE Arduino. Les données , récupérées par le capteur étaient ensuite envoyés vers Google Cloud à l’aide d’un service, appelé Google Cloud IoT Core. C’est un service de google qui nous fournit des interfaces HTTP et MQTT pour envoyer des données facilement dans le cloud. Notre appareil est enregistré dans un registry, ensuite une clé publique et une clé privée sont générées, la clé publique est indiqué à la Google Cloud Plateforme. Pour envoyer les données, un web token en format est utilisé. Gautier Mechling pouvait utiliser une simple requête HTTP POST vers le cloud avec le token et le message, mais il a décidé d’utiliser le protocole MQTT, parce qu’il est plus optimisé. Au final il envoyait chaque 5 secondes la température et l'humidité vers le cloud. Ces données sont envoyées en json, mais les types simples peuvent marcher aussi. Sur Google Cloud, il a stocké les données chez Cloud FireStore, depuis lequel il peut les utiliser dans des programmes google. Pour illustrer cela, il a créé un site statique avec un diagramme qui montre l'évolution de la température dans le temps réel.  Il a montré aussi comment créer un package joli à l’aide d’un PCB imprimé et une boîte, imprimée par une imprimante 3D.


## Architecture et facteur qualité

