# Objectif 

Développer un application web PHP qui distribue un montant total X de manière aléatoire chaque jour entre 2 dates, excluant les jours de la fin de semaine. L'application doit accepter un paramètre qui définie le pourcentage de distribution (**baseline**) sur chaque jour de la semaine. Le programme doit retourner un tableau dont les clés sont les dates et les valeurs est le montant aléatoire distribué pour chaque date.  
  
# Paramètres de l'application
- **Total**: Montant à distribuer
- **Baseline**: Paramètre qui contrôle la "randomness" de la distribution du montant total pour chaque date. C'est un nombre entre 0 et 100. Un nombre de 0 signifie que le montant total peut être distribué *très* aléatoirement entre chaque date. Donc une date peut avoir une valeur de 0, et une autre date une valeur de 100. Si le baseline est de 100, le total devrait être distribué *équitablement* sur chaque date.
- **Date début**
- **Date de fin**

# Requis
- Le montant doit être distribué seulement parmis les jours de la semaine, excluant les jours de fin de semaine
- Le code backend doit être fait en PHP
- Le code frontend est à la discrétion du développeur, point bonus si l'application est adapté pour mobile également

# Livrable
- Le développeur doit envoyer un fichier .zip concernant le code source
- *Bonus*: un lien pour que l'évaluateur puisse tester l'application directement sur internet

# Exemples
```
// Exemple 1 

$baseline=100; // un baseline de 100 indique que le total de 100 doit être distribué équitablement sur chaque date, donc une valeur de 20 pour chaque jour
$total=100;
$start_date='2022-01-03';
$end_date='2022-01-07';

// Résultat
array(
  '2022-01-03' => 20.00,
  '2022-01-04' => 20.00,
  '2022-01-05' => 20.00,
  '2022-01-06' => 20.00,
  '2022-01-07' => 20.00,
);
```
```
// Exemple 2

$baseline=20;
$total=100;
$start_date='2021-01-03';
$end_date='2021-01-07';

// Résultat
array(
  '2022-01-03' => 12.00,
  '2022-01-04' => 4.22,
  '2022-01-05' => 34.53,
  '2022-01-06' => 19.47,
  '2022-01-07' => 29.78,
);
```
```
// Exemple 3 

$baseline=20;
$total=100;
$start_date='2021-01-02';
$end_date='2021-01-08';

// Résultat
array(
  '2022-01-02' => 0, // dimanche
  '2022-01-03' => 10.54,
  '2022-01-04' => 7.10,
  '2022-01-05' => 20.00,
  '2022-01-06' => 37.40,
  '2022-01-07' => 24.96,
  '2022-01-08' => 0, // samedi
);
```
