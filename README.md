# Carto_LePlessis
Positionnement de bouées de régate radiocommandées sur l'étang du Plessis (44980)

**Applet** *Carto_LePlessis.apk* 

### Développée par JF sous MIT App Inventor.
(cc) jean.fruitet@free.fr
Cette applet affiche la carte de l'étang du Plessis à Sainte Luce / Loire.

### Fonctionnalités
- Placement des bouées fixes.
- Tracé de la zone de navigation.
- Saisie de la direction du vent  TWD en °
- Saisie de la vitesse du vent : TWS en km/h
- Saisie d'un parcours en mode texte et enregistrement dans une base de données locale TinyDB

### Ce qui reste à faire
Saisie le parcours en cliquant des bouées à l'écran. Cela permettra de récupérer les positions géographique pour tracer le parcours...

### Difficultés rencontrées
Initialement la liste des bouées (markers) devait être lue dans un fichier geoJSON, ainsi que le polygone définissant la zone de navigation.
Si les positions sont chargées, pour des raisons inconnues les propriétés de type des markers ne s'affichent pas dans l'applet MIT App Inventor et le fichier geojson des limites de navigation provoque une erreur.
J'ai fini par modifier à la main les propriétes des markers et de la zone de navigation... Pénible.

## Liens
MIT App Inventor http://ai2.appinventor.mit.edu/

GeoJSON https://geojson.io/

JSON Editor OnLine https://jsoneditoronline.org/

## License
**MIT** *Free Software, Hell Yeah!* https://github.com/pandao/editor.md/blob/master/LICENSE

**Creative Commons** http://creativecommons.org/licenses/by-sa/4.0/
