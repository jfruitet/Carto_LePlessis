# Carto_LePlessis
Positionnement de bouées de régate radiocommandée sur l'étang du Plessis (44980)

**Applet** *Carto_LePlessis.apk* 

### Développée par JF sous MIT App Inventor.
(cc) jean.fruitet@free.fr
Cette applet affiche la carte OpenStreetMap de l'étang du Plessis à Sainte Luce / Loire, 44980.

### Fonctionnalités
- Cartographie de l'étang du Plessis réservé au modélisme. Les bouées fixes ne peuvent être déplacées dans cette interface. Les bouées mobiles seront gérées dans la prochaine version de l'application.
- Menu du bas de page :
  1. Saisie de la direction d'où soufle le vent : entrer la valeur TWD en degrés ;
  2. Saisie et vitesse du vent : entrer la valeur TWS en km/h ;
- Menu droite
  1. "?" : Aide, ouvre un écran sur cette page ci ;
  2. Affiche une flèche opposée à la direction d'où soufle le vent, TWD : true wind direction en  ° et la force du vent TWS : true wind speed en km/h ;
  3. Bouton "BF" : affiche / masque les bouées fixes ;
  4. Bouton "ZN" : affiche / masque la zone de navigation réservée à l'Association Radiomodéliste des Bords de Loire ;
  5. Bouton "AP" : affiche / masque le parcours ; la ligne de départ est en bleu, la ligne d'arrivée en magenta. Les portes sont franchies en leur milieu
  6. Bouton "NP" : Affiche / masque le formulaire de création / modification du parcours courant
- Menu "AP" :
  1. Affiche le parcours, le nom et le nombre de tours du parcours. 
  2. Sauvegarde du parcours dans un fichier geoJSON (non implanté)
- Menu "NP" : Créer / Modifier le parcours courant :
  1. La saisie des bouées dans l'ordre se fait en cochant le mode de franchissement (bâbord / tribord), le type de bouée (Départ, Arrivée, Porte, Autre) puis en cliquant sur la carte à la position de la bouée à intégrer dans le parcours.
  2. Le bouton "Importer" récupère un fichier geoJSON du parcours (non implanté)
  3. Le bouton "Retirer" ouvre une liste de sélection pour désigner une bouée à retirer du parcours ;
  4. Le bouton "Vider" vide le parcours de son contenu ;
  5. Le bouton "Enregistrer" sauvegarde le parcours courant dans un stockage TinyDB

## Ce qui reste à faire
- Afficher le franchissement (bâbord / tribord) avec des marqueurs rouge ou vert.
- Importer le parcours en geoJSON...
- Exporter le parcours en geoJSON...

## Difficultés rencontrées
Initialement la liste des bouées (markers) devait être lue dans un fichier geoJSON, ainsi que le polygone définissant la zone de navigation.
Si les positions sont chargées, pour des raisons inconnues les propriétés de type des markers ne s'affichent pas dans l'applet MIT App Inventor et le fichier geojson des limites de navigation provoque une erreur.
J'ai fini par modifier à la main les propriétes des markers et de la zone de navigation... Pénible.

## Liens
MIT App Inventor http://ai2.appinventor.mit.edu/

GeoJSON https://geojson.io/

JSON Editor OnLine https://jsoneditoronline.org/

## License
Pour le code source : **MIT** *Free Software, Hell Yeah!* https://github.com/pandao/editor.md/blob/master/LICENSE

Pour les documents : **Creative Commons** http://creativecommons.org/licenses/by-sa/4.0/
