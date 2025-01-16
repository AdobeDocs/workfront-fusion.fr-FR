---
title: Jetons pour le formatage de la date et de l’heure
description: Les jetons de mise en forme de la date et de l’heure suivants sont disponibles dans le panneau  [!DNL Adobe Workfront Fusion mapping] .
author: Becky
feature: Workfront Fusion
exl-id: 4a7f288e-d563-4c37-a8bf-efc7e6b759d4
source-git-commit: 24a6c1558fd6349c022df8a1847a7f39fafddd67
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 91%

---

# Jetons pour le formatage de la date et de l’heure

## Jetons d’année, de mois et de jour

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Jeton </th> 
   <th>Sortie </th> 
   <th> <p>Description</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>YY </code> </td> 
   <td><code>70 71 ... 29 30</code> </td> 
   <td> <p> Année à 2 chiffres</p> </td> 
  </tr> 
  <tr> 
   <td><code>YYYY </code> </td> 
   <td><code>1970 1971 ... 2029 2030 </code> </td> 
   <td> <p>Année à 4 chiffres</p> </td> 
  </tr> 
  <tr> 
   <td><code>Y</code> </td> 
   <td><code>1970 1971 ... 9999 +10000 +10001</code> </td> 
   <td> <p>[!UICONTROL Year with any number of digits and sign]</p> </td> 
  </tr> 
  <tr> 
   <td><code>Q</code> </td> 
   <td><code>1 2 3 4 </code> </td> 
   <td> <p> Trimestre de l’année</p> </td> 
  </tr> 
  <tr> 
   <td><code>Qo</code> </td> 
   <td><code>1st 2nd 3rd 4th </code></td> 
   <td> <p>Trimestre de l’année avec ordinal</p> </td> 
  </tr> 
  <tr> 
   <td><code>M</code> </td> 
   <td><code>1 2 ... 11 12</code></td> 
   <td> <p>Nombre associé au mois</p> </td> 
  </tr> 
  <tr> 
   <td><code>Mo </code> </td> 
   <td><code>1st 2nd ... 11th 12th</code> </td> 
   <td> <p>[!UICONTROL Month] avec ordinal</p> </td> 
  </tr> 
  <tr> 
   <td><code>MM</code> </td> 
   <td><code>01 02 ... 11 12 </code> </td> 
   <td> <p> Nombre associé au mois précédé d’un zéro</p> </td> 
  </tr> 
  <tr> 
   <td><code>MMM</code> </td> 
   <td><code>Jan Feb ... Nov Dec</code></td> 
   <td> <p> Abréviation du mois</p> </td> 
  </tr> 
  <tr> 
   <td><code>MMMM</code> </td> 
   <td><code> January February ... November December</code> </td> 
   <td> <p> Nom du mois</p> </td> 
  </tr> 
  <tr> 
   <td><code>D</code> </td> 
   <td><code>1 2 ... 30 31 </code></td> 
   <td> <p>Jour du mois</p> </td> 
  </tr> 
  <tr> 
   <td><code>Do</code> </td> 
   <td><code>1st 2nd ... 30th 31st</code></td> 
   <td> <p> Jour du mois avec ordinal</p> </td> 
  </tr> 
  <tr> 
   <td><code>DD</code> </td> 
   <td><code>01 02 ... 30 31</code></td> 
   <td> <p> Jour du mois précédé d’un zéro</p> </td> 
  </tr> 
  <tr> 
   <td><code>DDD</code> </td> 
   <td><code>1 2 ... 364 365 </code></td> 
   <td> <p>Jour de l’année</p> </td> 
  </tr> 
  <tr> 
   <td><code>DDDo</code> </td> 
   <td><code>1st 2nd ... 364th 365th</code> </td> 
   <td> <p>[!UICONTROL Day of year] avec ordinal</p> </td> 
  </tr> 
  <tr> 
   <td><code>DDDD </code> </td> 
   <td><code>001 002 ... 364 365</code> </td> 
   <td> <p> Jour de l’année précédé d’un zéro</p> </td> 
  </tr> 
 </tbody> 
</table>

## Jetons d’année, de semaine et de jour

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Jeton </th> 
   <th>Sortie </th> 
   <th> <p>Description</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>d</code> </td> 
   <td><code>0 1 ... 5 6 </code> </td> 
   <td> <p> Jour de la semaine</p> </td> 
  </tr> 
  <tr> 
   <td><code>do</code> </td> 
   <td><code>0th 1st ... 5th 6th </code> </td> 
   <td> <p>[!UICONTROL Day of week with ordinal]</p> </td> 
  </tr> 
  <tr> 
   <td><code>dd </code> </td> 
   <td><code>Su Mo ... Fr Sa </code> </td> 
   <td> <p>Abréviation du jour</p> </td> 
  </tr> 
  <tr> 
   <td><code>ddd</code> </td> 
   <td><code>Sun Mon ... Fri Sat </code> </td> 
   <td> <p> Abréviation du jour</p> </td> 
  </tr> 
  <tr> 
   <td><code>dddd </code> </td> 
   <td><code>Sunday Monday ... Friday Saturday</code> </td> 
   <td> <p> Nom du jour</p> </td> 
  </tr> 
  <tr> 
   <td><code>E</code> </td> 
   <td><code>1 2 ... 6 7 </code> </td> 
   <td> <p> Jour de la semaine (ISO)</p> </td> 
  </tr> 
  <tr> 
   <td><code>w </code> </td> 
   <td><code>1 2 ... 52 53 </code> </td> 
   <td> <p>Semaine de l’année</p> </td> 
  </tr> 
  <tr> 
   <td><code>wo </code> </td> 
   <td><code>1st 2nd ... 52nd 53rd</code> </td> 
   <td> <p>[!UICONTROL Week of year with ordinal]</p> </td> 
  </tr> 
  <tr> 
   <td><code>ww </code> </td> 
   <td><code>01 02 ... 52 53 </code> </td> 
   <td> <p>Semaine de l’année précédée d’un zéro</p> </td> 
  </tr> 
  <tr> 
   <td><code>W</code></td> 
   <td><code>1 2 ... 52 53 </code> </td> 
   <td> <p>Semaine de l’année (ISO)</p> </td> 
  </tr> 
  <tr> 
   <td><code>Wo</code> </td> 
   <td><code>1st 2nd ... 52nd 53rd </code> </td> 
   <td> <p> Semaine de l’année avec ordinal (ISO)</p> </td> 
  </tr> 
  <tr> 
   <td><code>WW</code> </td> 
   <td><code>01 02 ... 52 53 </code> </td> 
   <td> <p> Semaine de l’année précédée d’un zéro (ISO)</p> </td> 
  </tr> 
  <tr> 
   <td><code>gg</code></td> 
   <td><code>70 71 ... 29 30 </code> </td> 
   <td> <p>Semaine de l’année</p> </td> 
  </tr> 
  <tr> 
   <td><code>gggg </code> </td> 
   <td><code>1970 1971 ... 2029 2030</code> </td> 
   <td> <p> Semaine de l’année</p> </td> 
  </tr> 
  <tr> 
   <td><code>GG </code> </td> 
   <td><code>70 71 ... 29 30 </code> </td> 
   <td> <p>Semaine de l’année (ISO)</p> </td> 
  </tr> 
  <tr> 
   <td><code>GGGG </code> </td> 
   <td><code>1970 1971 ... 2029 2030</code> </td> 
   <td> <p> Semaine de l’année (ISO)</p> </td> 
  </tr> 
 </tbody> 
</table>

## Jetons d’heure, de minute, de seconde, de milliseconde et de décalage

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th> <p>Jeton </p> </th> 
   <th>Sortie </th> 
   <th>Description</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>H</code> </td> 
   <td><code>0 1 ... 22 23</code></td> 
   <td> <p>Heure au format 24 heures</p> </td> 
  </tr> 
  <tr> 
   <td><code>HH</code> </td> 
   <td><code>00 01 ... 22 23</code></td> 
   <td> <p> Heure au format 24 heures précédée d’un zéro</p> </td> 
  </tr> 
  <tr> 
   <td><code>h</code> </td> 
   <td><code>1 2 ... 11 12</code></td> 
   <td> <p> Heure au format 12 heures</p> </td> 
  </tr> 
  <tr> 
   <td><code>hh </code> </td> 
   <td><code>01 02 ... 11 12</code> </td> 
   <td> <p> Heure au format 12 heures précédée d’un zéro</p> </td> 
  </tr> 
  <tr> 
   <td><code>k</code> </td> 
   <td><code>1 2 ... 23 24</code></td> 
   <td> <p> Heure au format 24 heures</p> </td> 
  </tr> 
  <tr> 
   <td><code>kk</code></td> 
   <td><code>01 02 ... 23 24</code> </td> 
   <td> <p> Heure au format 24 heures précédée d’un zéro</p> </td> 
  </tr> 
  <tr> 
   <td><code>A</code></td> 
   <td><code>AM PM </code> </td> 
   <td> <p>Post ou ante meridiem (majuscules)</p> </td> 
  </tr> 
  <tr> 
   <td><code>a</code> </td> 
   <td><code>am pm </code> </td> 
   <td> <p> Post ou ante meridiem (minuscules)</p> </td> 
  </tr> 
  <tr> 
   <td><code>m</code> </td> 
   <td><code> 0 1 ... 58 59</code> </td> 
   <td> <p> Minutes</p> </td> 
  </tr> 
  <tr> 
   <td><code>mm</code> </td> 
   <td><code>00 01 ... 58 59</code> </td> 
   <td> <p>[!UICONTROL Minutes with] zéro en début</p> </td> 
  </tr> 
  <tr> 
   <td><code>s</code> </td> 
   <td><code>0 1 ... 58 59</code> </td> 
   <td> <p> Secondes</p> </td> 
  </tr> 
  <tr> 
   <td><code>ss</code> </td> 
   <td><code>00 01 ... 58 59</code></td> 
   <td> <p>Secondes précédées d’un zéro</p> </td> 
  </tr> 
  <tr> 
   <td><code>S</code> </td> 
   <td><code>0 1 ... 8 9 </code> </td> 
   <td> <p> Fractions de seconde</p> </td> 
  </tr> 
  <tr> 
   <td><code>SS</code> </td> 
   <td><code>00 01 ... 98 99</code> </td> 
   <td> <p> Fractions de seconde précédées d’un zéro</p> </td> 
  </tr> 
  <tr> 
   <td><code>SSS</code> </td> 
   <td><code>000 001 ... 998 999</code> </td> 
   <td> <p> Franctions de seconde précédées de deux zéros</p> </td> 
  </tr> 
  <tr> 
   <td><code>SSSS ... SSSSSSSSS</code> </td> 
   <td><code>000[0..] 001[0..] ... 998[0..] 999[0..] </code> </td> 
   <td> <p> Fractions de seconde</p> </td> 
  </tr> 
  <tr> 
   <td><code>Z</code> </td> 
   <td><code>-07:00 -06:00 ... +06:00 +07:00 </code></td> 
   <td> <p>Fuseau horaire</p> </td> 
  </tr> 
  <tr> 
   <td><code>ZZ</code> </td> 
   <td><code>-0700 -0600 ... +0600 +0700 </code></td> 
   <td> <p>Fuseau horaire</p> </td> 
  </tr> 
  <tr> 
   <td><code>X</code> </td> 
   <td><code>1360013296</code> </td> 
   <td> <p> Date et heure Unix</p> </td> 
  </tr> 
  <tr> 
   <td><code>x</code> </td> 
   <td><code>1360013296123</code></td> 
   <td> <p> Date et heure Unix en millisecondes</p> </td> 
  </tr> 
 </tbody> 
</table>
