# ProjetFASE
Projet RaspberryPi Assistant de conduite

# Description du projet : 

Notre projet a pour but de reproduire des dispositifs présents dans la plupart des voitures récentes. Il est composé de deux dispositifs : un système anti-collision avant composé d’un capteur de distance à ultrason pour détecter un obstacle, un buzzer qui s’activera quand l’obstacle seras proche et trois leds de couleur qui représenteront les différents niveaux de distance avec l’obstacle. Le système fonctionne de la manière suivante : le capteur de distance mesure toutes les 5 secondes, on affiche la distance à l’écran. En dessous de 5 centimètres, on allume les 3 LEDs et le buzzer sonne, entre 5 et 15 centimètres, on allume 2 LEDs et au-delà de 15 centimètres, on allume une LED. Le deuxième dispositif consiste à automatiser un système de phare de telle sorte à ce qu’en fonction de la luminosité, le bon type de phare soit utilisé. Pour simuler cela, nous utiliserons un détecteur de lumière ainsi qu’une lampe à intensité réglable qui simule les feux de la voiture  : si une forte luminosité est détecté,on éteint la lampe, si une faible luminosité est détecté, on règle la lampe sur une luminosité intermédiaire qui correspond aux feux de croisement et si aucune luminosité n’est détectée, on règle la luminosité de lampe au maximum, ce qui correspond aux pleins phares. Une difficulté que nous pourrions rencontrer serait la détection de la luminosité, pour différencier une luminosité forte d’une luminosité faible, notamment pour simuler le croisement de nuit de deux véhicules qui aurait pour effet de faire passer nos “phares” de pleins phares à feux de croisements. Nous afficherons à l’écran différentes informations comme le nombre de fois où le buzzer a sonné, la distance entre la voiture et un obstacle devant ainsi que le nombre de voitures croisé lorsque les phares fonctionnent.
  
 # Scénarios d'utilisation : 
 
 ## Scénario nominal : 
 
 On place le dispositif sur une table, on utilise un objet faisant environ la taille du dispositif en tant qu’obstacle, on le rapproche progressivement de l’avant du dispositif (avant de la voiture) et les leds s’allument progressivement au fur et à mesure que l’on rapproche l’obstacle de l’avant de la voiture et le buzzer sonne lorsque l’obstacle touche presque la voiture. Ensuite, on se place dans une pièce sombre, la lumière à intensité réglable s’allume complètement, on utilise le flash d’un téléphone pour simuler une voiture qui arrive en face, la lumière baisse de moitié d’intensité et pour finir, on allume la pièce et la lampe s’éteint.

 
 ## Scénario dégradé : 
 
 On place le dispositif sur une table, on utilise un objet faisant environ la taille du dispositif en tant qu’obstacle, on le rapproche progressivement de l’avant du dispositif (avant de la voiture) cependant, les leds ne s’allument pas correctement mais le buzzer fonctionne. Ce problème aurait pu être causé par la surface de l’obstacle que l’on a choisi car les matériaux souples dégradent la précision d’un capteur à ultrason. On s’assure donc de choisir un objet fait d’un matériau dur comme le bois ou le métal pour éviter ce genre de problème . Ensuite, on se place dans une pièce sombre, la lumière à intensité réglable s’allume complètement, on utilise le flash d’un téléphone pour simuler une voiture qui arrive en face mais en raison du manque de précision dans la détection de la lumière, la lumière s’éteint complètement. Pour que le système fonctionne correctement, il faudra avoir un capteur d’intensité lumineuse suffisamment précis pour différencier la luminosité du jour et celle d’une lampe dans le noir.
 
