# Objectif 

Développer un application web PHP qui distribue un montant total X de manière aléatoire chaque jour entre 2 dates, excluant les jours de la fin de semaine. L'application doit accepter un paramètre qui définie le pourcentage de distribution (baseline) sur chaque jour de la semaine. Le programme doit retourner un tableau dont les clés sont les dates et les valeurs est le montant aléatoire distribué pour chaque date.  
  
# Paramètres de l'application
- **Total**: Montant à distribuer
- **Baseline**: Pourcentage de distribution: un pourcentage de 100% signifie que le montant total sera distribué équitablement sur chaque jour de la semaine. Un pourcentage de 20% signifie qu'une différence de 80% est acceptable entre la distribution de 2 dates.
- **Date début**
- **Date de fin**

# Requis
- Le montant doit être distribué seulement parmis les jours de la semaine, excluant les jours de fin de semaine
- Le code backend doit être fait en PHP
- Le code frontend est à la discrétion du développeur, point bonus si l'application est adapté pour mobile également

# Livrable
- Le développeur doit envoyer un lien pour que l'évaluateur puisse tester l'application
- Le développeur doit également envoyer un fichier .zip concernant le code source

# Exemples
```
$baseline=100;
$total=100;
$start_date='2021-01-03';
$end_date='2021-01-27';

array(
  'YYYY-mm-dd' => 0.00,
  'YYYY-mm-dd' => 0.00,
  'YYYY-mm-dd' => 0.00,
  'YYYY-mm-dd' => 0.00,
  'YYYY-mm-dd' => 0.00,
);
```

Objective: Distribute a total amount randomly (within certain parameters) in a range of dates, excluding weekends. There should be a baseline that will define the minimum amount of the value assigned to a specific date. The returned result should be a unidimensional array with the following structure: Array( [YYYY-mm-dd]=>0.00, // The value should be a float value (with two decimal places) corresponding to the date used as key [YYYY-mm-dd]=>0.00, [YYYY-mm-dd]=>0.00, ... )

