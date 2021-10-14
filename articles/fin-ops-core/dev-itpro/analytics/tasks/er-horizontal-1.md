---
title: ER Käytä vaakasuunnassa laajennettavia alueita sarakkeiden dynaamiseen lisäämiseen Excel-raportteihin (Osa 1 – Muodon suunnittelu)
description: Tässä aiheessa käsitellään sähköisen raportoinnin (ER) muodon määrittämistä luomaan raportteja OPENXML-laskentataulukkomuotoisina Excel-tiedostoina. (Osa 1)
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab360c259af37ce3995d3cd2560bc2e765e0bceb
ms.sourcegitcommit: e3290eb58ae569a59d6ae2e6922e7d8be8f1980f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/24/2021
ms.locfileid: "7551773"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-1---design-format"></a>ER Käytä vaakasuunnassa laajennettavia alueita sarakkeiden dynaamiseen lisäämiseen Excel-raportteihin (Osa 1 – Muodon suunnittelu)

[!include [banner](../../includes/banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi määrittää sähköisen raportoinnin (ER) muodon luomaan raportteja OPENXML-työkirjamuodossa (Excel), joissa pakolliset sarakkeet voi lyödä dynaamisesti vaakasuunnassa laajenevilla alueilla. Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.

Näiden vaiheiden edellytyksenä on seuraavien kolmen tehtäväoppaan suorittaminen:

ER Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi

ER Taloushallinnon dimensioiden käyttö tietolähteenä (Osa 1: Tietomallin suunnittelu)

ER Taloushallinnon dimensioiden käyttö tietolähteenä (Osa 2: Mallin yhdistäminen).

Sinun on myös ladattava ja tallennettava mallin paikallinen kopio malliraportin kanssa kohdasta [Mallin taloushallinnon dimensioiden verkkopalveluraportti](https://download.microsoft.com/download/3/1/3/313e2090-bc0a-421f-bf96-c58da9bc0dea/SampleFinDimWsReport.xlsx).

Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.

## <a name="create-a-new-report-configuration"></a>Uuden raporttikonfiguraation luominen

1. Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.
2. Valitse puussa `Financial dimensions sample model`.
3. Avaa valintaikkuna napsauttamalla Luo konfigurointi.
4. Kirjoita Uusi-kenttään `Format based on data model Financial dimensions sample model`.
    * Käytä etukäteen luotua mallia uuden raportin tietolähteenä.  
5. Syötä Nimi-kenttään `Sample report with horizontally expandable ranges`.
    * Malliraportti, joka sisältää vaakasuunnassa laajennettavat alueet  
6. Kirjoita Kuvaus-kenttään `To make Excel output with dynamically adding columns`.
    * Excel-tuotoksen luonti lisäämällä sarakkeita dynaamisesti  
7. Valitse Tietomallin määritelmä -kentässä Kirjaus.
8. Valitse Luo konfiguraatio.

## <a name="design-the-report-format"></a>Suunnittele raporttimuoto

1. Valitse Suunnittelutoiminto.
2. Ota `Show details` -vaihtopainike käyttöön.
3. Valitse toimintoruudussa Tuo.
4. Napsauta Tuo Excelissä.
5. Napsauta Liitteet.
    * Tuo raportin malli. Käytä siihen lataamaasi Excel-tiedostoa.  
6. Valitse Uusi.
7. Napsauta Tiedosto.
8. Sulje sivu.
9. Syötä tai valitse Malli-kentän arvo.
    * Valitse ladattu malli.  
10. Valitse OK.
    * Lisää uusi alue, josta luodaan dynaamisesti Excel-tuotos, jossa on (käyttäjän valintanäytöllä) valitsemasi määrä taloushallinnon dimensiosarakkeita. Jokaisen sarakkeen jokainen solu vastaa yhtä taloushallinnon dimension nimeä.  
11. Avaa valintaikkuna valitsemalla Lisää.
12. Valitse puussa `Excel\Range`.
13. Kirjoita Excel-alue-kenttään `DimNames`.
    * DimNames  
14. Valitse Replikointisuunta-kentässä `Horizontal`.
15. Valitse OK.
16. Valitse puussa `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`.
17. Valitse Siirrä ylöspäin.
18. Valitse puussa `Excel = "SampleFinDimWsReport"\Cell<DimNames>`.
19. Valitse Leikkaa.
20. Valitse puussa `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`.
21. Valitse Liitä.
22. Laajenna puussa kohde `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`.
23. Laajenna puussa kohde `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical`.
24. Laajenna puussa kohde `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical`.
25. Valitse puussa `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical`.
    * Lisää uusi alue, josta luodaan dynaamisesti Excel-tuotos, jossa on (käyttäjän valintanäytöllä) valitsemasi määrä taloushallinnon dimensiosarakkeita. Jokaisen sarakkeen kukin solu vastaa yhtä kunkin raportointitapahtuman taloushallinnon dimension arvoa.  
26. Valitse Lisää alue.
27. Kirjoita Excel-alue-kenttään `DimValues`.
    * DimValues  
28. Valitse Replikointisuunta-kentässä `Horizontal`.
29. Valitse OK.
30. Valitse puussa `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>`.
31. Valitse Leikkaa.
32. Valitse puussa `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal`.
33. Valitse Liitä.
34. Laajenna puussa kohde `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal`.

## <a name="map-format-elements-to-data-sources"></a>Yhdistä muodon osat tietolähteisiin

1. Valitse Yhdistämismääritys-välilehti.
2. Laajenna puussa kohde `model: Data model Financial dimensions sample model`.
3. Laajenna puussa kohde `model: Data model Financial dimensions sample model\Journal: Record list`.
4. Laajenna puussa kohde `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list`.
5. Laajenna puussa kohde `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list`.
6. Valitse puussa `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>`.
7. Valitse puussa `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String`.
8. Valitse Sido.
9. Valitse puussa `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal`.
10. Valitse puussa `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list`.
11. Valitse Sido.
12. Valitse puussa `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>`.
13. Valitse puussa `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real`.
14. Valitse Sido.
15. Valitse puussa `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>`.
16. Valitse puussa `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real`.
17. Valitse Sido.
18. Valitse puussa `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>`.
19. Valitse puussa `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String`.
20. Valitse Sido.
21. Valitse puussa `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>`.
22. Valitse puussa `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date`.
23. Valitse Sido.
24. Valitse puussa `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>`.
25. Valitse puussa `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String`.
26. Valitse Sido.
27. Valitse puussa `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>`.
28. Valitse puussa `model: Data model Financial dimensions sample model\Journal: Record list\Batch: String`.
29. Valitse Sido.
30. Valitse puussa `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical`.
31. Valitse puussa `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list`.
32. Valitse Sido.
33. Valitse puussa `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>`.
34. Valitse puussa `model: Data model Financial dimensions sample model\Journal: Record list\Batch: String`.
35. Valitse Sido.
36. Valitse puussa `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical`.
37. Valitse puussa `model: Data model Financial dimensions sample model\Journal: Record list`.
38. Valitse Sido.
39. Laajenna puussa kohde `model: Data model Financial dimensions sample model\Dimensions setting: Record list`.
40. Valitse puussa `model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String`.
41. Valitse puussa `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>`.
42. Valitse Sido.
43. Valitse puussa `model: Data model Financial dimensions sample model\Dimensions setting: Record list`.
44. Valitse puussa `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`.
45. Valitse Sido.
46. Valitse puussa `Excel = "SampleFinDimWsReport"\Cell<CompanyName>`.
47. Valitse puussa `model: Data model Financial dimensions sample model\Company: String`.
48. Valitse Sido.
49. Valitse Tallenna.
50. Sulje sivu.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
