---
title: ER Taloushallinnon dimensioiden käyttö tietolähteenä (Osa 2 – Mallin yhdistäminen).
description: Tässä aiheessa käsitellään sähköisen raportoinnin (ER) mallin määrittämistä käyttämään taloushallinnon dimensioita ER-raporttien tietolähteenä. (Osa 2)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 02c730d08c411e736a7f8b9e7bad3d6a18cb8e6a
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093234"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a>ER Taloushallinnon dimensioiden käyttö tietolähteenä (Osa 2 – Mallin yhdistäminen).

[!include [banner](../../includes/banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooliin määritetty käyttäjä voi konfiguroida sähköisen raportoinnin (ER) tietomallin käyttämään taloushallinnon dimensioita tietolähteenä ER-raporteissa. Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.

Jotta voisit suorittaa nämä vaiheet, "ER Taloushallinnon dimensioiden käyttäminen tietolähteenä (Osa 1: tietomallin suunnittelu)" -menettelyn vaiheiden on oltava suoritettuna.


## <a name="add-required-data-sources-to-model-mapping"></a>Lisää vaaditut tietolähteet mallin yhdistämismäärityksiin
1. Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.
2. Valitse puussa "Taloushallinnon dimensioiden esimerkkimalli".
3. Valitse Suunnittelutoiminto.
4. Valitse Yhdistä malli tietolähteeseen.
5. Valitse Uusi.
6. Valitse Määritelmä-kentässä Kirjaus.
7. Kirjoita Nimi-kenttään "Dimensioiden tietojen yhdistäminen".
8. Kirjoita Kuvaus-kenttään "Dimensioiden tietojen yhdistäminen".
9. Valitse Tallenna.
10. Valitse Suunnittelutoiminto.
11. Valitse puussa Dynamics 365 for Operations\Table.
12. Valitse Lisää juuri.
13. Syötä Nimi-kenttään Yritys.
14. Syötä Taulu-kenttään CompanyInfo.
15. Valitse OK.
16. Valitse puussa "Functions\Financial dimensions details".
17. Valitse Lisää juuri.
    * Tämä tietolähde määrittää, miten taloushallinnon dimensioiden laajuus määritellään raporteille, jotka käyttävät tätä mallia tietolähteenä.  
18. Kirjoita arvo Nimi-kenttään.
19. Valitse Kysy dimensioita -kentässä Kyllä.
    * Valitse Kyllä, jos haluat sallia käyttäjän valita dimensiot suorituksen aikana käyttäjän valintalomakkeelta. Jos arvo on ei, kaikkia nykyisen ilmentymän taloushallinnon dimensioita käytetään oletuksena.  
20. Valitse Taloushallinnon dimensioiden valinta -kentässä "Yritys".
    * Valitse Kaikki, jos haluat sallia käyttäjien valita haluamansa dimensiot nykyiselle ilmentymälle hakukentässä.  Valitse Yritys, jos haluat sallia käyttäjien valita haluamansa dimensiot yritykselle hakukentässä.  Valitse Dimensio, jos haluat, että käyttäjät voivat valita dimensiot yhdestä dimensiojoukosta.  
21. Valitse Kysy päätiliä -kentässä Kyllä.
    * Aseta "Kysy päätiliä" -asetuksen arvoksi Kyllä, jotta käyttäjät valita päätilin osaksi dimensioluetteloa.   Jos arvo on Ei, päätiliä ei sisällytetä dimensioluetteloon ja "Päätili on pakollinen" -asetus on käytössä. Jos "Onko päätili pakollinen" -asetuksen arvoksi on määritetty Kyllä, päätili luetaan dimensioluetteloon käyttäjän valinnasta huolimatta.  
22. Valitse OK.
![ER-mallimäärityksen suunnittelun sivu](../media/er-financial-dimensions-guides-model-mapping1.png)
23. Valitse puussa Dynamics 365 for Operations\Table records.
24. Valitse Lisää juuri.
25. Kirjoita Nimi-kenttään LedgerJournal.
26. Valitse Kysy kyselyä -kentässä Kyllä.
27. Kirjoita Taulu-kenttään LedgerJournalTable.
28. Valitse OK.
![ER-mallimäärityksen suunnittelun sivu](../media/er-financial-dimensions-guides-model-mapping2.png)

## <a name="map-data-model-elements-to-added-data-sources"></a>Yhdistä tietomallielementit lisättyihin tietolähteisiin
1. Laajenna puussa "Journal".
2. Laajenna puussa "Journal\Transaction".
3. Laajenna puussa "Journal\Transaction\Dimensions data".
4. Laajenna puussa "Dimensioiden asetus".
5. Laajenna puussa solmu "LedgerJournal".
6. Laajenna puussa LedgerJournal\<Relations.
7. Laajenna puussa LedgerJournal\<Relations\LedgerJournalTrans.
8. Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Voucher.
9. Valitse puussa solmu "Journal\Transactions\Voucher".
10. Valitse Sido.
11. Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension).
    * Huomaa, että kaikille viittauksille taloushallinnon dimensioihin, jotka on määritetty esimerkiksi arvolle LedgerDimension, on saatavilla vastaava tietolähdenimike (LedgerDimension.Dimension). Tämä tietolähdenimike tarjoaa kyseisen dimensiojoukon taloushallinnon dimensiot tietueen luettelona.  
12. Laajenna puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension).
13. Laajenna puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions.
14. Laajenna puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value.
15. Laajenna puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition.
16. Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name.
17. Valitse puussa "Journal\Transaction\Dimensions data\Name".
18. Valitse Sido.
19. Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description.
20. Valitse puussa "Journal\Transaction\Dimensions data\Description".
21. Valitse Sido.
22. Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code.
23. Valitse puussa "Journal\Transaction\Dimensions data\Code".
24. Valitse Sido.
25. Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions.
26. Valitse puussa "Journal\Transaction\Dimensions data".
27. Valitse Sido.
![ER-mallimäärityksen suunnittelun sivu](../media/er-financial-dimensions-guides-model-mapping3.png)
28. Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit).
29. Valitse puussa solmu "Journal\Transactions\Debit".
30. Valitse Sido.
31. Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate).
32. Valitse puussa solmu "Journal\Transactions\Date".
33. Valitse Sido.
34. Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode).
35. Valitse puussa solmu "Journal\Transactions\Currency".
36. Valitse Sido.
37. Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit).
38. Valitse puussa solmu "Journal\Transactions\Credit".
39. Valitse Sido.
40. Valitse puussa LedgerJournal\<Relations\LedgerJournalTrans.
41. Valitse puussa solmu "Journal\Transactions".
42. Valitse Sido.
43. Valitse puussa solmu "LedgerJournal\Journal batch number(JournalNum)".
44. Valitse puussa solmu "Journal\Batch".
45. Valitse Sido.
46. Valitse puussa "LedgerJournal".
47. Valitse puussa "Journal".
48. Valitse Sido.
49. Laajenna puussa "Dimensions".
50. Laajenna puussa "Dimensions\Main account and dimensions".
51. Laajenna puussa "Dimensions\Main account and dimensions\Definition".
52. Valitse puussa "Dimensions\Main account and dimensions\Definition\Name".
53. Valitse puussa "Dimensioiden asetus\Code".
54. Valitse Sido.
55. Valitse puussa "Dimensions\Main account and dimensions\Definition\Report column name".
56. Valitse puussa "Dimensioiden asetus\Name".
57. Valitse Sido.
58. Valitse puussa "Dimensions\Main account and dimensions".
59. Valitse puussa "Dimensioiden asetus".
60. Valitse Sido.
61. Valitse puussa "Yritys".
62. Valitse Muokkaa.
63. Kirjoita expressionAsStringText-kenttään "Company.'find()'.'name()".
    * Company.'find()'.'name()'  
64. Valitse Tallenna.
![ER-mallimäärityksen suunnittelun sivu](../media/er-financial-dimensions-guides-model-mapping4.png)
65. Sulje sivu.
66. Valitse Tallenna.
67. Sulje sivu.

## <a name="complete-this-draft-models-version"></a>Viimeistele malliluonnoksen versio
1. Sulje sivu.
2. Sulje sivu.
3. Voit muuttaa tilaa valitsemalla Muuta.
4. Valitse Valmis.
5. Valitse OK.
![ER-mallimäärityksen suunnittelun sivu](../media/er-financial-dimensions-guides-model-mapping5.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]