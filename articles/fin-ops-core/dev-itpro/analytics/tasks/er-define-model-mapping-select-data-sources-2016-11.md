---
title: Määritä ER-mallin yhdistämismääritys ja valitse niille tietolähteet
description: Tässä artikkelissa käsitellään, miten järjestelmänvalvoja tai sähköisen raportoinnin kehittäjä voi valita sähköisen raportoinnin tietomallille tietolähteitä.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 40fe0c8453aa9e22bb170bad24993c64f8a3ee78
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883535"
---
# <a name="define-er-model-mappings-and-select-data-sources-for-them"></a>Määritä ER-mallin yhdistämismääritys ja valitse niille tietolähteet

[!include [banner](../../includes/banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi valita sähköisen raportoinnin (ER) tietomallille tietolähteitä. Tietolähteet sidotaan valittujen tietomallien yksittäisiin komponentteihin suunnittelun yhteydessä. Tietomallin liiketoimintatiedot täytetään suorituksen aikana. Tässä esimerkissä valitaan Litware, Inc. -malliyritykselle aiemmin luodun tietomallin tietolähteet. Voit suorittaa nämä vaiheet, jos Luo uusi tietomalli -menettelyn vaiheet ovat valmiit.


## <a name="open-the-electronic-reporting-configurations-tree"></a>Sähköinen raportointi -määritysten puurakenteen avaaminen
1. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.
2. Valitse Raportointikonfiguraatiot.

## <a name="insert-a-new-model-mapping"></a>Uuden malliyhdistämismäärityksen lisääminen
1. Valitse puussa solmu Payments (simplified model).
2. Valitse Suunnittelutoiminto.
3. Valitse Yhdistä malli tietolähteeseen.
4. Valitse Uusi.
    * Näin luodaan uusi tietue, joka yhdistää tietomallin tietolähteisiin. Tässä esimerkissä tietomalli yhdistetään halutun maksutyypin eli tilisiirron tietolähteisiin.     Tietylle tietomallille voidaan suunnitella useita yhdistämismäärityksiä. Voit luoda yhdistämismäärityksen esimerkiksi erityyppisille maksuille, kuten suoraveloitukselle tai tilisiirroille. Tässä esimerkissä luodaan tilisiirtojen yhdistämismääritys.  
5. Syötä Nimi-kenttään Tilisiirron yhdistämismääritys.
    * Tilisiirron yhdistämismääritys  
6. Syötä Kuvaus-kenttään Maksumallin yhdistämismääritys, tilisiirto.
    * Maksumallin yhdistämismääritys, tilisiirto  
7. Kirjoita Kuvaus-kenttään CustomerCreditTransferInitiation.
    * CustomerCreditTransferInitiation  
8. ResolveChanges, määritelmä.
9. Valitse Tallenna.

## <a name="define-required-data-sources-for-the-current-model-mapping"></a>Pakollisten tietolähteiden määrittäminen nykyiselle malliyhdistämismääritykselle
1. Valitse Suunnittelutoiminto.
2. Valitse puussa Dynamics 365 for Operations\Table records.
3. Valitse Lisää juuri.
    * Syötä tämä tietolähde, kun haluat käyttää maksutapahtumia.  
4. Kirjoita Nimi-kenttään Tapahtumat.
    * Tapahtumat  
5. Syötä Etiketti-kenttään Tapahtumat.
    * Tapahtumat  
6. Syötä Ohje-kenttään Kirjanpidon kirjauskansion rivit.
    * Kirjanpidon kirjauskansiorivit  
7. Valitse Kysy kyselyä -kentässä Kyllä.
    * Valitse Kyllä.  
8. Syötä Taulu-kenttään LedgerJournalTrans.
    * LedgerJournalTrans  
9. Valitse OK.
    * Valitse nykyisen tietomallin tietolähteeksi LedgerJournalTrans-taulu.  
10. Valitse puussa solmu Functions\Calculated field.
11. ValitseLisää.
    * Lisää uusi laskettu kenttä valitsemalla Lisää.  
12. Syötä Nimi-kenttään $EndToEndID.
    * $EndToEndID  
13. Valitse Muokkaa kaavaa.
14. Valitse puussa solmu String\CONCATENATE.
15. Valitse Lisää toiminto.
16. Laajenna puussa solmu Transactions.
17. Valitse puussa solmu Transactions\Voucher.
18. Valitse Lisää tietolähde.
19. Kirjoita Kaava-kenttään CONCATENATE(Transactions.Voucher, "-",.
    * Kirjoita [ , “-“, ] kaavan loppuun.  
20. Valitse puussa solmu String\TEXT.
21. Valitse Lisää toiminto.
22. Valitse puussa solmu Transactions\Record-ID(RecId).
23. Valitse Lisää tietolähde.
24. Kirjoita Kaava-kenttään CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId)).
    * Kirjoita kaavan loppuun [))].  
25. Valitse Tallenna.
    * Varmista, että luodussa kaavassa ei ole virheitä. Katso kaavaeditorin hallinnan Virheet-välilehti.  
26. Sulje sivu.
27. Valitse OK.
    * Lisää laskettu kenttä tähän tietolähteeseen.  
28. ValitseLisää.
    * Lisää uusi laskettu kenttä valitsemalla Lisää.  
29. Syötä Nimi-kenttään $Amount.
    * Summa (€)  
30. Valitse Muokkaa kaavaa.
31. Laajenna puussa solmu Transactions.
32. Valitse puussa solmu Transactions\Debit(AmountCurDebit).
33. Valitse Lisää tietolähde.
34. Kirjoita Kaava-kenttään Transactions.AmountCurDebit - .
    * Kirjoita kaavan loppuun [ - ].  
35. Valitse puussa solmu Transactions\Credit(AmountCurCredit).
36. Valitse Lisää tietolähde.
37. Valitse Tallenna.
38. Sulje sivu.
39. Valitse OK.
    * Nyt lasketun kentän summa (€) lisätään nykyisen tietomallin valittuun tietolähteeseen.  
40. Valitse puussa Transactions\$Amount.
41. Laajenna puussa solmu Transactions.
42. Laajenna tai tiivistä puussa Transactions\$Amount.
43. Laajenna ta tiivistä puussa Tapahtumat.
44. Valitse puussa Dynamics 365 for Operations\Table records.
45. Valitse Lisää juuri.
    * Syötä tämä tietolähde, kun haluat käyttää yrityksen pankkitilin tietoja.  
46. Syötä Nimi-kenttään BankAccount.
    * BankAccount  
47. Syötä Etiketti-kenttään Pankkitili.
    * Pankkitili  
48. Syötä Ohje-kenttään Pankkitili.
    * Pankkitili  
49. Valitse Kysy kyselyä -kentässä Kyllä.
    * Valitse Kyllä.  
50. Syötä Taulu-kenttään BankAccountTable.
    * BankAccountTable  
51. Valitse OK.
    * Valitse nykyisen tietomallin tietolähteeksi BankAccountTable-taulu.  
52. Valitse Lisää juuri.
    * Syötä tämä tietolähde, kun haluat käyttää yrityksen pankkitilin edellytyksiä.  
53. Syötä Nimi-kenttään Yritys.
    * Yritys   
54. Syötä Etiketti-kenttään arvo.
    * Yrityksen tiedot  
55. Syötä Ohje-kenttään Yrityksen tiedot.
    * Yrityksen tiedot  
56. Valitse Kysy kyselyä -kentässä Kyllä.
    * Valitse Kyllä.  
57. Syötä Taulu-kenttään CompanyInfo.
    * CompanyInfo  
58. Valitse OK.
    * Valitse nykyisen tietomallin tietolähteeksi CompanyInfo-taulu.  
59. Valitse puussa solmu Functions\Calculated field.
60. Valitse Lisää juuri.
    * Lisää laskettu kenttä uutena tietolähteenä.  
61. Syötä Nimi-kenttään ProcessingDateTime.
    * ProcessingDateTime  
62. Syötä Etiketti-kenttään Käsittelypäivämäärä ja -aika.
    * Käsittelypäivämäärä ja -aika  
63. Valitse Muokkaa kaavaa.
64. Valitse puussa Päivämäärä/aika\SESSIONNOW.
65. Valitse Lisää toiminto.
66. Valitse Tallenna.
67. Sulje sivu.
68. Valitse OK.
    * Lisää laskettu ProcessingDateTime-kenttä nykyisen tietomallin tietolähteeksi.  
69. Valitse Tallenna.
70. Sulje sivu.
71. Sulje sivu.
72. Sulje sivu.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]