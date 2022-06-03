mettre le php -> <?php ?>

ecrire un truc -> echo

variable = $variable
($variable = "la variable";)

interpolation = "."
ex : $message = "Bonjour" . $name . ", comment ça va ?";

--- variables

$x = 10;
$y = 20;

$average = ($x + $y)/2;

=

      function average($x, $y) {
       return ($x + $y)/2;
    }
    $resultat = average(10, 20);
    echo $resultat;

--- conditions

      $hour = 18;

    if($hour >= 0 & $hour < 7) {
       echo "c'est la nuit, il faut dormir.";
    }

if($hour >= 7 & $hour < 18)  {
       echo "c'est le jour !";
    }
   if($hour >= 18 & $hour < 24) {
echo "c'est le soir !";
}

--- heure et dates

dates :

    symbole         signification
    %d              numéro du jour 01 à 31
    %A              nom complet du jour (Lundi à Dimanche)
    %m              numéro du mois 01 à 12
    %B              nom complet du mois (Janvier à Décembre)
    %y              année sur deux chiffres (21 pour 2021)
    %Y              année sur quatre chiffres (2021)
    %H              heure (00 à 23)
    %M              minute (00 à 59)

        code                         résultat
    strftime("%d/%m/%y")         28/12/21
    strftime("%A %d %B")         Mardi 28 Décembre

setlocale(LC_TIME, "fr.utf8"); -> Mettre l'heure en fr
echo strftime("%d %B %Y"); -> afficher l'heure

--- html et php

On peut integrer du php dans du code html

ex :

<?php
  $title = "Mon super site";
  $name = "Luke";
  $day = strftime("%d");
  $time = strftime("%H h %M");
?>

<!doctype html>
<html lang="fr">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title><?php echo $title; ?></title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Bienvenue sur le site de <?php echo $name ?> </h1>
  <p>Nous sommes le <?php echo $day ?> et il est <?php echo $time ?>.</p>
</body>
</html>

--- boucles for (exemple table de multiplication)

function table_multiplication($number){
    for($i = 1; $i <= 10; $i++){
$result = $number \* $i;
echo $number . " x " . $i . " = " . $result . "<br>";
}
}
table_multiplication(5);
