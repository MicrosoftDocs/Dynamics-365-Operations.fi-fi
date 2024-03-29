---
title: ER Määritä muoto suorittamaan laskenta ja summaus (Osa 2 – Laskentojen konfigurointi)
description: Tässä artikkelissa käsitellään sähköisen raportoinnin muodon määrittämistä aiemmin luotuun tekstiin perustuvaa laskentaa ja summien tuottamista. (Osa 2)
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
ms.openlocfilehash: f7cdfff15ac157d69f0b60de8b36acc870a9cf49
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290661"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a>ER Määritä muoto suorittamaan laskenta ja summaus (Osa 2 – Laskentojen konfigurointi)

[!include [banner](../../includes/banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) muodon suorittamaan laskennan ja summauksen luodun tekstin tietojen perusteella. Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.

Jotta voit suorittaa nämä toimet, sinun on ensin suoritettava "ER Konfiguroi muoto suorittamaan laskenta ja summaaminen (osa 1: Luo muoto)" -menettelyn vaiheet.

Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a>Luo muotokonfiguraaio, jossa lisätään laskennan ja summauksen tiedot
1. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.
2. Valitse Raportointikonfiguraatiot.
3. Laajenna puussa solmu "Intrastat model".
4. Valitse puusta "Intrastat model\Intrastat (DE)"
    * Oletetaan, että sinun on mukautettava Microsoftin toimittamaa muotoa lisäämällä rivejä, jotka sisältävät yhteenvetotietoja Intrastat-raportin loppuun. Muokkauksia voit tehdä johtamalla oman Intrastat-kokoonpanon Microsoftin tarjoamasta esiintymästä.  
5. Avaa valintaikkuna napsauttamalla Luo konfigurointi.
6. Kirjoita Uusi-kenttään "Derive from Name: Intrastat (DE), Microsoft".
7. Kirjoita Nimi-kenttään Intrastat (DE) with counting & summing.
8. Valitse Luo konfiguraatio.

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a>Määritä raportin suorittamaan laskenta ja summaus tuotoksen perusteella
1. Valitse Suunnittelutoiminto.
2. Valitse Kerää tulostiedot -kentässä Kyllä.
    * Tämä merkintä aktivoituu Intrastat-tiedoston luonnin tulostustietojen keräysprosessin suorituksen aikana.  
    * Laskenta on suoritettava useisiin Intrastat-suuntiin, joten lisää kohdistettu mallin luettelointi tämän muotokonfiguraation tietolähteiden luetteloon.  
3. Valitse Yhdistämismääritys-välilehti.
4. Avaa valintaikkuna valitsemalla Lisää juuri.
5. Valitse puussa solmu "Data model\Enumeration".
6. Kirjoita Nimi-kenttään "Suunta".
7. Syötä tai valitse arvo Mallin luettelointi -kentässä.
    * Valitse arvoksi Siirtosuunta.  
8. Valitse OK.
9. Avaa valintaikkuna valitsemalla Lisää juuri.
10. Valitse puussa solmu Functions\Calculated field.
11. Kirjoita Nimi-kenttään "$BlockName".
12. Valitse Muokkaa kaavaa.
13. Kirjoita Kaava-kenttään "block".
14. Valitse Tallenna.
15. Sulje sivu.
16. Valitse OK.
17. Avaa valintaikkuna valitsemalla Lisää juuri.
18. Valitse puussa solmu Functions\Calculated field.
19. Kirjoita Nimi-kenttään "$RecName".
20. Valitse Muokkaa kaavaa.
21. Kirjoita Kaava-kenttään "record".
22. Valitse Tallenna.
23. Sulje sivu.
24. Valitse OK.
25. Avaa valintaikkuna valitsemalla Lisää juuri.
26. Valitse puussa solmu Functions\Calculated field.
27. Kirjoita Nimi-kenttään "$InvName".
28. Valitse Muokkaa kaavaa.
29. Kirjoita Kaava-kenttään "InvoicedAmountEUR".
30. Valitse Tallenna.
31. Sulje sivu.
32. Valitse OK.
33. Valitse puussa "Intrastat\Data".
34. Valitse Kerätyn tietoavaimen nimi -kentän Muokkaa-painike
35. Valitse Lisää tietolähde.
    * $BlockName  
36. Valitse Tallenna.
37. Sulje sivu.
38. Valitse Kerätyn tietoavaimen arvo -kentän Muokkaa-painike.
39. Kirjoita Kaava-kenttään "IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")".
    * IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")  
40. Valitse Tallenna.
41. Sulje sivu.
    * Laske tämän sarjan rivit.. Tuloksia käytetään nimellä "lohko" erikseen eri suunnille. "Tuonti"-arvoa käytetään kaikille saapuville Intrastat-tapahtumille. "Vienti"-arvoa käytetään kaikille lähteville Intrastat-tapahtumille. Ajattele tätä virtuaalisena Excel-taulukkona. Kullakin tapahtumalla on rivi, jonka ensimmäisessä sarakelohkossa on vastaavasti arvot "Vienti" ja "Tuonti".  
42. Laajenna puussa solmu "Intrastat\Data: Sequence".
43. Valitse puussa solmu "Intrastat\Data Sequence\Arrivals?".
44. Valitse Kerätyn tietoavaimen nimi -kentän Muokkaa-painike.
    * Laske tämän sarjan rivit.. Tulokset tallennetaan nimellä "tietue".  
45. Valitse puussa "$RecName".
46. Valitse Lisää tietolähde.
47. Valitse Tallenna.
48. Sulje sivu.
49. Valitse Kerätyn tietoavaimen arvo -kentän Muokkaa-painike.
50. Kirjoita Kaava-kenttään 'Intrastat.CommodityRecord.CommodityCode'.
51. Valitse Tallenna.
52. Sulje sivu.
    * Laske tämän sarjan rivit.. Tuloksia käytetään nimellä "tietue" erikseen eri kauppatavarakoodeille. Ajattele tätä virtuaalisena Excel-taulukkona. Kullakin tapahtumalla on rivi, jossa ensimmäinen sarakelohko täytetään vastaavasti arvoilla "Tuonti" ja "Vienti" vastaavasti ja toinen lohkotietue täytetään kauppatavarakoodeilla.  
53. Valitse puussa solmu "Intrastat\Data Sequence\Dispatches?".
54. Valitse Kerätyn tietoavaimen nimi -kentän Muokkaa-painike
55. Valitse puussa "$RecName".
56. Valitse Lisää tietolähde.
57. Valitse Tallenna.
58. Sulje sivu.
59. Valitse Kerätyn tietoavaimen arvo -kentän Muokkaa-painike.
60. Kirjoita Kaava-kenttään 'Intrastat.CommodityRecord.CommodityCode'.
61. Valitse Tallenna.
62. Sulje sivu.
63. Laajenna puussa solmu "Intrastat\Data: Sequence\Dispatches: Sequence?".
64. Laajenna puussa solmu "Intrastat\Data: Sequence\Dispatches: Sequence?\Record = Intrastat.CommodityRecord".
65. Valitse Muoto-välilehti.
66. Valitse puussa "Intrastat\Data\Dispatches\Record\Invoice amount EUR".
67. Valitse Yhdistämismääritys-välilehti.
68. Valitse Kerätyn tietoavaimen nimi -kentän Muokkaa-painike.
69. Valitse puussa "$InvName".
70. Valitse Lisää tietolähde.
71. Valitse Tallenna.
72. Sulje sivu.
    * Tee yhteenveto tämän sarjan riveillä laskutetuille summille. Tuloksia käytetään nimellä "InvoicedAmountEUR" erikseen eri Intrastat-suunnille ja kauppatavarakoodeille. Ajattele tätä virtuaalisena Excel-taulukkona. Kullakin tapahtumalla on rivi, jonka ensimmäisessä sarakelohkossa on vastaavasti arvot "Vienti" ja "Tuonti". Toiseen tietuelohkoon täytetään kauppatavarakoodin arvo ja kolmanteen sarakkeeseen, "InvoicedAmountEUR" tulee laskutussumman arvo.  
73. Laajenna puussa solmu "Intrastat\Data\Arrivals?".
74. Laajenna puussa "Intrastat\Data\Arrivals?\Record = Intrastat.CommodityRecord".
75. Valitse Muoto-välilehti.
76. Valitse puussa "Intrastat\Data\Arrivals\Record\Invoice amount EUR".
77. Valitse Yhdistämismääritys-välilehti.
78. Valitse Kerätyn tietoavaimen nimi -kentän Muokkaa-painike.
79. Valitse puussa "$InvName".
80. Valitse Lisää tietolähde.
81. Valitse Tallenna.
82. Sulje sivu.
83. Valitse Tallenna.
84. Sulje sivu.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
