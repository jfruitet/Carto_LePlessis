# Applet Carto_LePlessis.apk

### D�velopp�e par JF sous MIT App Inventor.
(cc) jean.fruitet@free.fr
Cette applet affiche la carte de l'�tang du Plessis � Sainte Luce / Loire.

### Fonctionnalit�s

- Placement des bou�es fixes.
- Trac� de la zone de navigation.
- Saisie de la direction du vent  TWD en �
- Saisie de la vitesse du vent : TWS en km/h
- Saisie d'un parcours en mode texte et enregistrement dans une base de donn�es locale TinyDB

### Ce qui reste � faire
Saisie le parcours en cliquant des bou�es � l'�cran. Cela permettra de r�cup�rer les positions g�ographique pour tracer le parcours...

### Difficult�s rencontr�es
Initialement la liste des bou�es (markers) devait �tre lue dans un fichier geoJSON, ainsi que le polygone d�finissant la zone de navigation.

Si les positions sont charg�es, pour des raisons inconnues les propri�t�s de type des markers ne s'affichent pas dans l'applet MIT App Inventor et le fichier geojson des limites de navigation provoque une erreur.

J'ai fini par modifier � la main les propri�tes des markers et de la zone de navigation... P�nible.

## Liens
MIT App Inventor http://ai2.appinventor.mit.edu/

GeoJSON https://geojson.io/

JSON Editor OnLine https://jsoneditoronline.org/

## License

Pour les sources **MIT** *Free Software, Hell Yeah!* https://github.com/pandao/editor.md/blob/master/LICENSE

Pour les documents **Creative Commons** http://creativecommons.org/licenses/by-sa/4.0/


