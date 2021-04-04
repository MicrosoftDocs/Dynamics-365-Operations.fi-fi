---
title: ER Taloushallinnon dimensioiden käyttö tietolähteenä (Osa 3 – Raportin suunnittelu)
description: Tässä aiheessa käsitellään sähköisen raportoinnin (ER) mallin määrittämistä käyttämään taloushallinnon dimensioita ER-raporttien tietolähteenä. (Osa 3)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
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
ms.openlocfilehash: a9594a12c28109d80c6ee07a9ee38f4923963dca
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565235"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a>ER Taloushallinnon dimensioiden käyttö tietolähteenä (Osa 3 – Raportin suunnittelu)

[!include [banner](../../includes/banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) tietomallin käyttämään taloushallinnon dimensioita tietolähteenä ER-raporteissa. Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.

Jotta voisit suorittaa nämä vaiheet, "ER Taloushallinnon dimensioiden käyttäminen tietolähteenä (Osa 2: mallin yhdistämismääritykset)" -menettelyn vaiheiden on oltava suoritettuna.


## <a name="design-a-report-to-present-financial-dimensions"></a>Suunnittele raportti, jossa esitetään taloushallinnon dimensioita
1. Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.
2. Valitse puussa "Taloushallinnon dimensioiden esimerkkimalli".
3. Avaa valintaikkuna napsauttamalla Luo konfigurointi.
4. Syötä Uusi-kenttään Muoto perustuu tietomalliin Taloushallinnon dimensioiden esimerkkimalli.
    * Käytä etukäteen luotua mallia uuden raportin tietolähteenä.  
5. Kirjoita Nimi-kenttään Kirjauskansioraportti.
6. Valitse Tietomallin määritelmä -kentässä Kirjaus.
7. Valitse Luo konfiguraatio.
8. Valitse Suunnittelutoiminto.
9. Avaa valintaikkuna valitsemalla Lisää juuri.
10. Valitse puussa solmu XML\Element.
11. Kirjoita Nimi-kenttään "Juuri".
12. Valitse OK.
13. Avaa valintaikkuna valitsemalla Lisää.
14. Valitse puussa solmu XML\Attribute.
15. Syötä Nimi-kenttään Yritys.
16. Valitse OK.
17. Avaa valintaikkuna valitsemalla Lisää.
18. Valitse puussa solmu XML\Element.
19. Kirjoita Nimi-kenttään "Kirjauskansio".
20. Valitse OK.
21. Valitse puussa "Root: XML Element\Journal: XML Element".
22. Avaa valintaikkuna valitsemalla Lisää.
23. Valitse puussa solmu XML\Attribute.
24. Kirjoita Nimi-kenttään "Erä".
25. Valitse OK.
26. Avaa valintaikkuna valitsemalla Lisää.
27. Valitse puussa solmu XML\Element.
28. Kirjoita Nimi-kenttään "Tapahtuma".
29. Valitse OK.
30. Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element".
31. Avaa valintaikkuna valitsemalla Lisää.
32. Valitse puussa solmu XML\Attribute.
33. Kirjoita Nimi-kenttään "Tosite".
34. Valitse OK.
35. Valitse Lisää määrite.
36. Kirjoita Nimi-kenttään "Päivämäärä".
37. Valitse OK.
38. Valitse Lisää määrite.
39. Syötä Nimi-kenttään Valuutta.
40. Valitse OK.
41. Valitse Lisää määrite.
42. Kirjoita Nimi-kenttään "Dt".
43. Valitse OK.
44. Valitse Lisää määrite.
45. Kirjoita Nimi-kenttään "Ct".
46. Valitse OK.
47. Avaa valintaikkuna valitsemalla Lisää.
48. Valitse puussa solmu XML\Element.
49. Kirjoita Nimi-kenttään "Dimensiot".
50. Valitse OK.
51. Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element".
52. Avaa valintaikkuna valitsemalla Lisää.
53. Valitse puussa solmu XML\Attribute.
54. Kirjoita Nimi-kenttään "Koodi".
55. Valitse OK.
56. Valitse Lisää määrite.
57. Kirjoita Nimi-kenttään "Arvo".
58. Valitse OK.
59. Valitse Lisää määrite.
60. Kirjoita Nimi-kenttään. "Kuv."
61. Valitse OK.
![ER-toimintojen suunnittelutoiminnon sivu](../media/er-financial-dimensions-guides-format1.png)

## <a name="map-report-elements-to-data-sources"></a>Yhdistä raportin osat tietolähteisiin
1. Valitse Yhdistämismääritys-välilehti.
2. Laajenna puussa "model: Data model Financial dimensions sample model".
3. Laajenna puussa "model: Data model Financial dimensions sample model\Journal: Record list".
4. Laajenna puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list".
5. Laajenna puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list".
6. Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute".
7. Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String".
8. Valitse Sido.
9. Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute".
10. Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String".
11. Valitse Sido.
12. Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute".
13. Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String".
14. Valitse Sido.
15. Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list".
16. Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element".
17. Valitse Sido.
18. Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute".
19. Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real".
20. Valitse Sido.
21. Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute".
22. Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real".
23. Valitse Sido.
24. Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute".
25. Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String".
26. Valitse Sido.
27. Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute".
28. Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date".
29. Valitse Sido.
30. Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute".
31. Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String".
32. Valitse Sido.
33. Valitse puussa "Root: XML Element\Journal: XML Element\Transaction: XML Element".
34. Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list".
35. Valitse Sido.
36. Valitse puussa "Root: XML Element\Journal: XML Element\Batch: XML Attribute".
37. Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list\Batch: String".
38. Valitse Sido.
39. Valitse puussa "Root: XML Element\Journal: XML Element".
40. Valitse puussa "model: Data model Financial dimensions sample model\Journal: Record list".
41. Valitse Sido.
42. Valitse puussa "Root: XML Element\Company: XML Attribute".
43. Valitse puussa "model: Data model Financial dimensions sample model\Company: String".
44. Valitse Sido.
45. Valitse Tallenna.
46. Sulje sivu.
![ER-toimintojen suunnittelutoiminnon sivu](../media/er-financial-dimensions-guides-format2.png)



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]