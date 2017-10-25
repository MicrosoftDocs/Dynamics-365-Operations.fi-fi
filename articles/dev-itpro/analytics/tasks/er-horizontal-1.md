--- 
title: "Muodon suunnitteleminen käyttämään vaakasuuntaisesti laajennettavia alueita sarakkeiden lisäämiseksi dynaamisesti sähköistä raportointia (ER) varten"
description: "Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi määrittää sähköisen raportoinnin (ER) muodon luomaan raportteja OPENXML-työkirjamuodossa (Excel), joissa pakolliset sarakkeet voi lyödä dynaamisesti vaakasuunnassa laajenevilla alueilla."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 0cd1de95630d0f7c40c3b9948015892623a93686
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="design-a-format-to-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-for-electronic-reporting-er"></a>Muodon suunnitteleminen käyttämään vaakasuuntaisesti laajennettavia alueita sarakkeiden lisäämiseksi dynaamisesti sähköistä raportointia (ER) varten

[!include[task guide banner](../../includes/task-guide-banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi määrittää sähköisen raportoinnin (ER) muodon luomaan raportteja OPENXML-työkirjamuodossa (Excel), joissa pakolliset sarakkeet voi lyödä dynaamisesti vaakasuunnassa laajenevilla alueilla. Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.

Näiden vaiheiden edellytyksenä on seuraavien kolmen tehtäväoppaan suorittaminen: 

ER Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi

ER Taloushallinnon dimensioiden käyttö tietolähteenä (osa 1: tietomallin suunnittelu)

ER Taloushallinnon dimensioiden käyttö tietolähteenä (osa 2: malliyhdistämismääritys).

Lataa ja tallenna myös paikallinen kopio mallista sekä esimerkkiraportti osoitteesta http://msdynamics.blob.core.windows.net/media/2016/09/SampleFinDimWsReport.xlsx

Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.


## <a name="create-a-new-report-configuration"></a>Uuden raporttikonfiguraation luominen
1. Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.
2. Valitse puussa "Taloushallinnon dimensioiden esimerkkimalli".
3. Avaa valintaikkuna napsauttamalla Luo konfigurointi.
4. Syötä Uusi-kenttään Muoto perustuu tietomalliin Taloushallinnon dimensioiden esimerkkimalli.
    * Käytä etukäteen luotua mallia uuden raportin tietolähteenä.  
5. Kirjoita Nimi-kenttään "Malliraportti, joka sisältää vaakasuunnassa laajennettavat alueet".
    * Malliraportti, joka sisältää vaakasuunnassa laajennettavat alueet  
6. Kirjoita Kuvaus-kenttään "Excel-tuotoksen luonti lisäämällä sarakkeita dynaamisesti".
    * Excel-tuotoksen luonti lisäämällä sarakkeita dynaamisesti  
7. Valitse Tietomallin määritelmä -kentässä Kirjaus.
8. Valitse Luo konfiguraatio.

## <a name="design-the-report-format"></a>Suunnittele raporttimuoto
1. Valitse Suunnittelutoiminto.
2. Ota käyttöön "Näytä tiedot" -painike.
3. Valitse toimintoruudussa Tuo.
4. Napsauta Tuo Microsoft Excelissä.
5. Napsauta Liitteet.
    * Tuo raportin malli. Käytä siihen lataamaasi Excel-tiedostoa.  
6. Valitse Uusi.
7. Napsauta Tiedosto.
8. Sulje sivu.
9. Syötä tai valitse Malli-kentän arvo.
    * Valitse ladattu malli.  
10. Valitse OK.
    * Lisää uusi alue, josta luodaan dynaamisesti Excel-tuotos, jossa on (käyttäjän valintanäytöllä) valitsemasi määrä taloushallinnon dimensiosarakkeita. Jokaisen sarakkeen jokainen solu edustaa yhden taloushallinnon dimension nimeä.  
11. Avaa valintaikkuna valitsemalla Lisää.
12. Valitse puussa solmu "Excel\Range".
13. Kirjoita Excel-alue -kenttään "DimNames".
    * DimNames  
14. Valitse Vaakasuuntainen-vaihtoehto kentässä Replikointisuunta.
15. Valitse OK.
16. Valitse puussa Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal.
17. Valitse Siirrä ylöspäin.
18. Valitse puussa Excel = "SampleFinDimWsReport"\Cell<DimNames>.
19. Valitse Leikkaa.
20. Valitse puussa Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal.
21. Valitse Liitä.
22. Laajenna puussa Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal.
23. Laajenna puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical.
24. Laajenna puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical.
25. Valitse puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical.
    * Lisää uusi alue, josta luodaan dynaamisesti Excel-tuotos, jossa on (käyttäjän valintanäytöllä) valitsemasi määrä taloushallinnon dimensiosarakkeita. Jokaisen sarakkeen jokainen solu edustaa yhden taloushallinnon dimension arvoa kullekin raportoinnin tapahtumalle.  
26. Valitse Lisää alue.
27. Kirjoita Excel-alue -kenttään "DimValues".
    * DimValues  
28. Valitse Vaakasuuntainen-vaihtoehto kentässä Replikointisuunta.
29. Valitse OK.
30. Valitse puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>.
31. Valitse Leikkaa.
32. Valitse puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal.
33. Valitse Liitä.
34. Laajenna puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal.

## <a name="map-format-elements-to-data-sources"></a>Yhdistä muodon osat tietolähteisiin
1. Valitse Yhdistämismääritys-välilehti.
2. Laajenna puussa "model: Data model Financial dimensions sample model".
3. Laajenna puussa "model: Data model Financial dimensions sample model\Journal: Record list".
4. Laajenna puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list".
5. Laajenna puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list".
6. Valitse puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>.
7. Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String".
8. Valitse Sido.
9. Valitse puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal.
10. Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list".
11. Valitse Sido.
12. Valitse puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>.
13. Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real".
14. Valitse Sido.
15. Valitse puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>.
16. Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real".
17. Valitse Sido.
18. Valitse puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>.
19. Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String".
20. Valitse Sido.
21. Valitse puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>.
22. Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date".
23. Valitse Sido.
24. Valitse puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>.
25. Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String".
26. Valitse Sido.
27. Valitse puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>.
28. Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Batch: String".
29. Valitse Sido.
30. Valitse puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical.
31. Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list".
32. Valitse Sido.
33. Valitse puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>.
34. Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Batch: String".
35. Valitse Sido.
36. Valitse puussa Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical.
37. Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list".
38. Valitse Sido.
39. Laajenna puussa "model: Data model Financial dimensions sample model\Dimensions setting: Record list".
40. Valitse puussa "model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String".
41. Valitse puussa Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>.
42. Valitse Sido.
43. Valitse puussa "model: Data model Financial dimensions sample model\Dimensions setting: Record list".
44. Valitse puussa Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal.
45. Valitse Sido.
46. Valitse puussa Excel = "SampleFinDimWsReport"\Cell<CompanyName>.
47. Valitse puussa "model: Data model Financial dimensions sample model\Company: String".
48. Valitse Sido.
49. Valitse Tallenna.
50. Sulje sivu.

