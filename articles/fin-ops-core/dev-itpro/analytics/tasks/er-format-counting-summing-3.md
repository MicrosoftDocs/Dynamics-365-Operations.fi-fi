---
title: ER Määritä muoto suorittamaan laskenta ja summaus (Osa 3 – Tuotoksen luonti laskentojen avulla)
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon suorittamaan laskennan ja summauksen luodun tekstin tietojen perusteella.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7bbef7048488056f50ec8967a9af53d468666856
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550760"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a>ER Määritä muoto suorittamaan laskenta ja summaus (Osa 3 – Tuotoksen luonti laskentojen avulla)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon suorittamaan laskennan ja summauksen luodun tekstin tietojen perusteella. Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.

Jotta voit suorittaa nämä toimet, sinun on ensin suoritettava "ER Konfiguroi muoto suorittamaan laskenta ja summaaminen (osa 2: Määritä laskelmat)" -menettelyn vaiheet.

Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.


## <a name="configure-this-report-to-use-counting-and-summing-info"></a>Määritä raportti käyttämään laskenta- ja summaustietoja
1. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.
2. Valitse Raportointikonfiguraatiot.
3. Laajenna puussa solmu "Intrastat model".
4. Laajenna puusta "Intrastat model\Intrastat (DE)"
5. Valitse puussa Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.
6. Valitse Suunnittelutoiminto.
7. Valitse Yhdistämismääritys-välilehti.
8. Avaa valintaikkuna valitsemalla Lisää juuri.
    * Lisää uusi tietolähde, joka noutaa tallennettujen lohkojen luettelon.  
9. Valitse puussa solmu Functions\Calculated field.
10. Kirjoita Nimi-kenttään "$BlocksList".
    * $BlocksList  
11. Valitse Muokkaa kaavaa.
12. Valitse puussa "Data collection functions\COLLECTEDLIST".
13. Valitse Lisää toiminto.
14. Valitse Lisää tietolähde.
15. Kirjoita Kaava-kenttään "COLLECTEDLIST('$BlockName', ".
    * COLLECTEDLIST('$BlockName',  
16. Kirjoita Kaava-kenttään "COLLECTEDLIST('$BlockName', "*")".
    * COLLECTEDLIST('$BlockName', "*")  
17. Valitse Tallenna.
    * Kuvio "*" tarkoittaa, että kaikki lohkot lisätään tämän tietueen luetteloon.  
18. Sulje sivu.
19. Valitse OK.
20. Valitse Muoto-välilehti.
21. Valitse puussa "Intrastat\Data".
22. Avaa valintaikkuna valitsemalla Lisää.
23. Valitse puussa "Text\Sequence".
24. Syötä Nimi-kenttään "Summat lohkoittain".
    * Kokonaissummat lohkon mukaan  
25. Valitse Erikoismerkit-kentässä "Uusi rivi - Windows (CR-LF)".
26. Valitse OK.
27. Valitse puussa solmu "Intrastat\Data\Totals by blocks".
28. Avaa valintaikkuna valitsemalla Lisää.
29. Valitse puussa solmu Text\String.
30. Kirjoita Nimi-kenttään "Lohkokoodi".
    * Lohkon koodi  
31. Valitse OK.
32. Valitse Lisää merkkijono.
33. Syötä Nimi-kenttään "Rivien laskenta".
    * Rivien laskenta  
34. Valitse OK.
35. Valitse Lisää merkkijono.
36. Syötä Nimi-kenttään "Kokonaissumma".
    * Kokonaismäärä  
37. Valitse OK.
38. Valitse Yhdistämismääritys-välilehti.
39. Valitse puussa '$BlocksList'.
40. Valitse Sido.
    * Luo yhteenveto kullekin tallennetulle lohkolle.  
41. Valitse Muoto-välilehti.
42. Valitse puussa solmu "Intrastat\Data\Totals by blocks\Block code".
43. Valitse Yhdistämismääritys-välilehti.
44. Valitse Muokkaa kaavaa.
45. Kirjoita kaava-kenttään "Block id: " & .
    * "Block id: " &  
46. Laajenna puussa '$BlocksList'.
47. Valitse puussa '$BlocksList\Value'.
48. Valitse Lisää tietolähde.
49. Valitse Tallenna.
50. Sulje sivu.
51. Valitse Muoto-välilehti.
52. Valitse puussa solmu "Intrastat\Data\Totals by blocks\Lines counting".
53. Valitse Yhdistämismääritys-välilehti.
54. Valitse Muokkaa kaavaa.
    * Luo tuotos kullekin tässä raportissa esitetyn lohkon rivimäärälle.  
55. Kirjoita Kaava-kenttään "Number of lines in this block: " & .
    * "Number of lines in this block: " &  
56. Kirjoita Kaava-kenttään "Number of lines in this block: " & TEXT(.
    * "Number of lines in this block: " & TEXT(  
57. Valitse puussa "Data collection functions\COUNTIFS".
58. Valitse Lisää toiminto.
59. Valitse Lisää tietolähde.
60. Kirjoita Kaava-kenttään "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', .
    * "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',  
61. Laajenna puussa '$BlocksList'.
62. Valitse puussa '$BlocksList\Value'.
63. Valitse Lisää tietolähde.
64. Kirjoita Kaava-kenttään "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, .
    * "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,  
65. Valitse puussa "$RecName".
66. Valitse Lisää tietolähde.
67. Kirjoita Kaava-kenttään "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*")).
    * "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))  
68. Valitse Tallenna.
69. Sulje sivu.
70. Valitse Muoto-välilehti.
71. Valitse puussa solmu "Intrastat\Data\Totals by blocks\Total amount".
72. Valitse Yhdistämismääritys-välilehti.
73. Valitse Muokkaa kaavaa.
    * Luo tuotos, joka on kunkin tässä raportissa esitetyn lohkon yhteenlaskettu laskutussumma.  
74. Kirjoita Kaava-kenttään "Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*")).
    * "Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))  
75. Valitse Tallenna.
76. Sulje sivu.
77. Valitse Tallenna.
78. Sulje sivu.

