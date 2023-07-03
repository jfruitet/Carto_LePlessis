# Carto_LePlessis
Positionnement de bouées de régate radiocommandée
**Applet** *CartoLePlessis.apk* 

### Développée par JF sous MIT App Inventor 2.
(cc) jean.fruitet@free.fr
Cette applet affiche les bouées fixes de la carte OpenStreetMap de l'étang du Plessis à Sainte Luce / Loire, 44980.
Elle est destinée à tester mes capacités en programmation d'applet de géolocalisation et de gestion graphique de positions GPS.
Elle entrera comme composant logiciel  dans le projet RoBoNav mené depuis février 2023 avec l'ICAM de Nantes.

## Ecran 1
Affichage de la carte du plan d'eau du Plessis avec les bouées fixes.

Affichage du périmètre de navigation

Saisie et affichage d'un parcours de régate.

### Fonctionnalités

Cartographie de l'étang du Plessis réservé au modélisme. Les bouées fixes ne peuvent être déplacées dans cette interface. Les bouées mobiles seront gérées dans une version ultérieure de l'application.

- Menu du bas de page :
  1. Saisie de la direction d'où soufle le vent : entrer la valeur TWD en degrés ;
  2. Saisie et vitesse du vent : entrer la valeur TWS en km/h ; cliquer sur "Go" ;
- Menu droite
  1. "?" : Aide, ouvre un second écran ;
  2. Affiche une flèche indiquant la **direction vers laquelle soufle le vent**, TWD : true wind direction en  ° et la force du vent TWS : true wind speed en km/h ;
  3. Bouton "BF" : affiche / masque les bouées fixes dans leur couleur d'origine ;
  4. Bouton "ZN" : affiche / masque la zone de navigation réservée à l'Association Radiomodéliste des Bords de Loire ;
  5. Bouton "AP" : affiche / masque le parcours courant
  6. Bouton "NP" : Affiche / masque le formulaire de création / modification du parcours courant

#### Affichage du parcours  
La ligne de départ est en bleu, la ligne d'arrivée en magenta. Quand le départ et l'arrivée sont identiques c'est la couleur magenta qui s'impose ;

Le départ, l'arrivée et les portes sont franchies en leur milieu ;

La couleur des bouées est adaptée au franchissement :
- Bouées verte : la bouée est laissée à tribord
- Bouée rouge : la bouée est laissée à bâbord
Noter que si une bouée est franchie à différentes reprises sur le même parcours c'est la couleur du dernier franchissement qui s'impose...
    
#### Saisie et affichage du parcours courant
- Menu "AP" : Titre "Parcours" ; afficher et sauvegarder le parcours courant
  1. Nom du parcours 
  2. Sauvegarde du parcours dans un fichier texte type Texte avec séparateur ","
  3. Liste à l'écran les bouées du parcours :
  
Pour chaque bouée sont affichés le Nom, le Franchissement (B|T) et le Type (Départ|Arrivée|Gate| ) 
<Nom bouée> B|T D|A|G|<espace blanc>

- Menu "NP" : "Créer / Modifier un parcours"
   
C'est le parcours courant qui est modifié.

La saisie des bouées doit être faite dans l'ordre du parcours en cochant d'abord  le mode de franchissement (bâbord / tribord), le type de bouée (Départ, Arrivée, Porte, Autre) puis en cliquant sur la carte à la position de la bouée à intégrer dans le parcours.

  1.  Parcours saisi en italique : liste de bouées sous forme de chaînes de caractères avec séparateur ",". 
Chaque bouée est affichée dans le format  
      <code>BOUEE;B|T;D|A|G|<SPACE>;Latitude;Longitude</code>
      
  2. Le bouton "Importer" récupère un fichier de parcours au format texte décrit ci-dessus. 
  3. Le bouton "Retirer" ouvre un écran de sélection pour désigner une bouée à retirer du parcours ;
  5. Le bouton "Vider" vide le parcours de son contenu ;
  6. Le bouton "Enregistrer" sauvegarde le parcours courant dans un stockage TinyDB persistant. Ceci est indispensable pour valider correctement la saisie... et la transmission de données d'une page à l'autre de l'applet.

## Ecran 2
Accès aux données stockées dans la BD persistente, aux fichiers sauvegardés et export au format JSON vers un serveur de traitement externe à l'applet.
- Menu "Fichiers"
  1. Affichage réscursif des fichiers et des dossiers de l'espace de stockage attribué à l'application
  2. Supprimer un fichier. Nous n'autorisons que la suppression de fichiers du dossier racine... sans contrôler qu'ils appartiennent à l'applet... A améliorer !;>(
  3. Afficher le contenu d'un fichier
- Menu "Exporter"
  1. Données chargées en mémoire pérenne : TWD / TWS / Nom du parcours et Parcours
- Menu "JSON"
  1. Transmission des données JSON en mémoire vers un serveur de traitement externe.
Ceci afin de proposer des traitements de type optimisation de parcours, etc.

- Menu "A propos"
  1. Page GitHub de l'applet.
- Menu "Retour"
  1. Retour à l'écran n°1

## Ce qui reste à faire
- Importer un plan d'eau différent et les bouées fixes de celui-ci au format geoJSON...
- Intégrer l'application au projet RoBoNav de positionnement de bouées de régate avec ancrage virtuel par GPS

## Difficultés rencontrées
Initialement la liste des bouées (markers) devait être lue dans un fichier geoJSON, ainsi que le polygone définissant la zone de navigation.
Si les positions sont chargées, pour des raisons inconnues les propriétés de type des markers ne s'affichent pas dans l'applet MIT App Inventor et le fichier geojson des limites de navigation provoque une erreur.
J'ai fini par modifier à la main les propriétes des markers et de la zone de navigation... Pénible.

J'ai aussi eu pas mal de difficulté à appeler un serveur externe en PHP mais ce n'est pas dû à MIT AI2.

Enfin je pense être allé au maximum de ce qu'il est raisonable deprogrammer avec MIT AI2 car plus le programme enfle plus il est difficile de s'y retrouver.

Je regrette que AI2 ne bénéficie pas d'un mécanisme de fichiers inclus qui permettrait d'alléger le code du programme principal.

L'adaptation à une langue différente ne me paraît pas simple non plus...

## Liens
MIT App Inventor http://ai2.appinventor.mit.edu/

GeoJSON https://geojson.io/

JSON Editor OnLine https://jsoneditoronline.org/

## License
Pour le code source : **MIT** *Free Software, Hell Yeah!* https://github.com/pandao/editor.md/blob/master/LICENSE

Pour les documents : **Creative Commons** http://creativecommons.org/licenses/by-sa/4.0/
