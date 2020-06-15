# zenbot1624

## Utilisation
Cette page contient le mode d'utilisation de la zenbot 1624 de l'espace menuiserie.

![1624_large_wide_belts](https://user-images.githubusercontent.com/65183668/84680473-10e72c80-af33-11ea-8ef3-dd0355b792fc.jpg)

Lien constructeur: [[http://www.zenbotcnc.com/cnc-routers/zenbot-1624-cnc-router]]

## Fabrication d'un circuit imprimé à l'aide de la zenbot1624

Le flow que je décris ici utilise les logiciels suivants:

  * Eagle PCB Design 7.6 [[https://cadsoft.io/]] pour la création du circuit
  * PCB GCode 3.6.2.4 [[http://www.pcbgcode.org/]] pour la génération du GCode
  * Universal Gcode Sender 1.0.9 [[http://winder.github.io/ugs_website/]]

Ces logiciels sont compatibles Windows et Mac OS X. Je t'invite à lire leur documentation respective pour ce qui est de leur installation.

### Création du GCode

Une fois ton circuit créé, il faut l'exporter en GCode pour qu'il soit interprétable par la CNC.

  - Dans Eagle, menu File > Run ULP
  - Sélectionne pcg-gcode-setup.ulp, se trouvant dans le dossier d'installation de PCB GCode.
  - Renseigne les données suivantes:

![generation](https://user-images.githubusercontent.com/65183668/84680676-56a3f500-af33-11ea-89a4-2f46d8c64c9b.png)
![machines](https://user-images.githubusercontent.com/65183668/84680678-573c8b80-af33-11ea-8994-de4594fa51a6.png)

En appuyant sur "Accept and make my board", en attendant un peu en fonction de la complexité de la board, tu obtiendra une preview du travail généré.

Le fichier GCode (portant l'extension ".tap") se trouve alors dans le dossier du projet Eagle.

### Préparation de la CNC

Même si l'echofab possède des forets (ou mèches, ou "bits", ou encore "mills"), il est préférable que tu t'en achètes pour tes besoins. C'est une pièce d'usure qui s'abime et se casse très facilement.

  * [[http://www.ebay.com/itm/10x-Titanium-Coated-Carbide-PCB-Engraving-CNC-Bit-Router-Tool-30-Degree-0-2mm-/131124487494?ssPageName=ADME:X:EAC:FR:3160|10x Titanium Coated Carbide PCB Engraving CNC Bit Router Tool 30 Degree]]

Les formes de mèches varient en fonction des approches, personnellement je préfère les 30 degrés qui permettent des travaux de précision.

Pour le circuit en lui même, il est nécessaire de s'acheter du FR1, ou papier phénolique. Moins courant que l'époxy du FR4, il est moins abrasif pour tes mèches et surtout ne génère pas (ou peu) de particules fines. Intéressant pour ceux qui tiennent à leurs poumons. Au Canada, il y a 2 sources d'approvisionnement à ma connaissance:

  * [[https://www.inventables.com/technologies/circuit-board-blanks|Inventables]]
  * [[https://www.digikey.ca/product-detail/en/mg-chemicals/675/473-1018-ND/559714|Digikey]]

Digikey gives you a 12'x18' (216si) for 26CAD, Inventables 25x6'x6' (900si) for 24CAD
