--- 
title: "Tietomallin yhdistäminen valittuihin tietolähteisiin sähköistä raportointia (ER) varten"
description: "Seuraavissa vaiheissa selitetään, miten käyttäjä, jolla on järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi yhdistää sähköisen raportoinnin (ER) tietomallin valittuihin Dynamics 365 for Finance and Operations, Enterprise Editionin tietolähteisiin."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5a7d55a5cfb890490315d45d67745ce65b7ab374
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="map-a-data-model-to-selected-data-sources-for-electronic-reporting-er"></a>Tietomallin yhdistäminen valittuihin tietolähteisiin sähköistä raportointia (ER) varten

[!include[task guide banner](../../includes/task-guide-banner.md)]

Seuraavissa vaiheissa selitetään, miten käyttäjä, jolla on järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi yhdistää sähköisen raportoinnin (ER) tietomallin valittuihin Dynamics 365 for Finance and Operations, Enterprise Editionin tietolähteisiin. Tätä malliyhdistämismääritystä käytetään myöhemmin tietolähteenä sähköisten maksuasiakirjojen hallinnan muotokonfiguraatiossa. Tässä esimerkissä yhdistetään Litware, Inc. -esimerkkiyrityksen tietomalli tietolähteisiin. Voit tehdä nämä vaiheet, jos Valitse tietomallit mallin yhdistämismääritystä varten -menettelyn vaiheet on jo tehty.


## <a name="open-er-configurations-tree"></a>ER-konfiguraatioiden puurakenteen avaaminen
1. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.
2. Valitse Konfiguraatiot.

## <a name="select-created-model-mapping"></a>Luodun malliyhdistämisvastaavuuden valitseminen
1. Valitse puussa solmu Payments (simplified model).
    * Varmista, että Maksut (yksinkertaistettu malli) -mallikonfiguraatio on luotu etukäteen. Pysähdy muussa tapauksessa ja palaa Uuden määrityksen luonti valitun toimialueen tietomallilla -tehtäväoppaan suorittamisen jälkeen.  
2. Valitse Mallin suunnittelu.
3. Valitse Yhdistä malli tietolähteeseen.
4. Valitse Tilisiirron yhdistämismääritys -tietue.
    * Tilisiirron yhdistämismääritys  

## <a name="bind-created-data-sources-to-data-model-elements"></a>Luotujen tietolähteiden sitominen tietomallielementteihin
1. Valitse Suunnittelutoiminto.
2. Valitse puussa solmu Processing date & time(ProcessingDateTime).
3. Valitse puussa solmu Processing date(ProcessingDateTime).
4. Valitse Sido.
5. Valitse puussa solmu Payment message identification(MessageIdentification).
6. Laajenna puussa solmu Transactions.
7. Valitse puussa solmu Transactions\Journal batch number(JournalNum).
8. Valitse Sido.
9. Valitse puussa solmu Payments.
10. Valitse puussa solmu Transactions.
11. Valitse Sido.
12. Laajenna puussa solmu Payments= Transactions.
13. Laajenna puussa solmu Payments= Transactions\Creditor.
14. Laajenna puussa solmu Payments= Transactions\Creditor\Account.
15. Valitse puussa solmu Payments= Transactions\Creditor\Account\Currency code(Currency).
16. Laajenna puussa solmu Transactions\vendBankAccountInTransactionCompany().
17. Valitse puussa solmu Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode).
18. Valitse Sido.
19. Valitse puussa solmu Payments= Transactions\Creditor\Account\IBAN code(IBAN).
20. Valitse puussa solmu Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN).
21. Valitse Sido.
22. Valitse puussa solmu Payments= Transactions\Creditor\Account\Number.
23. Valitse puussa solmu Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum).
24. Valitse Sido.
25. Valitse puussa solmu Payments= Transactions\Creditor\Agent.
26. Valitse puussa solmu Payments= Transactions\Creditor\Agent\Name.
27. Valitse puussa solmu Transactions\vendBankAccountInTransactionCompany()\Name.
28. Valitse Sido.
29. Valitse puussa solmu Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber).
30. Valitse puussa solmu Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum).
31. Valitse Sido.
32. Valitse puussa solmu Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT).
33. Valitse puussa solmu Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo).
34. Valitse Sido.
35. Valitse puussa solmu Payments= Transactions\Creditor\Name.
36. Laajenna puussa solmu Transactions\findVendTable().
37. Valitse puussa solmu Transactions\findVendTable()\name().
38. Valitse Sido.
39. Valitse puussa solmu Payments= Transactions\Currency code(Currency).
40. Laajenna puussa Transactions\>Relations.
41. Laajenna puussa Transactions\>Relations\Currency table(Currency).
42. Valitse puussa Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO).
43. Valitse Sido.
44. Laajenna puussa solmu Payments= Transactions\Debtor.
45. Laajenna puussa solmu Payments= Transactions\Debtor\Account.
46. Valitse puussa solmu Payments= Transactions\Debtor\Account\Currency code(Currency).
47. Valitse puussa solmu Bank Account(BankAccount).
48. Valitse puussa solmu Bank Account(BankAccount).
49. Valitse puussa solmu Bank Account(BankAccount)\Currency(CurrencyCode).
50. Valitse Sido.
51. Valitse puussa solmu Bank Account(BankAccount)\IBAN.
52. Valitse puussa solmu Payments= Transactions\Debtor\Account\IBAN code(IBAN).
53. Valitse Sido.
54. Valitse puussa solmu Payments= Transactions\Debtor\Account\Number.
55. Valitse puussa solmu Bank Account(BankAccount)\Bank account number(AccountNum).
56. Valitse Sido.
57. Laajenna puussa solmu Payments= Transactions\Debtor\Agent.
58. Valitse puussa solmu Payments= Transactions\Debtor\Agent\Name.
59. Valitse puussa solmu Bank Account(BankAccount)\Name.
60. Valitse Sido.
61. Valitse puussa solmu Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber).
62. Valitse puussa solmu Bank Account(BankAccount)\Routing number(RegistrationNum).
63. Valitse Sido.
64. Valitse puussa solmu Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT).
65. Valitse puussa solmu Bank Account(BankAccount)\SWIFT code(SWIFTNo).
66. Valitse Sido.
67. Valitse puussa solmu Payments= Transactions\Debtor\Name.
68. Valitse puussa solmu Company information(Company).
69. Laajenna puussa solmu Company information(Company).
70. Valitse puussa solmu Company information(Company)\Name.
71. Valitse Sido.
72. Valitse puussa solmu Payments= Transactions\Description.
73. Valitse puussa solmu Transactions\Description(Txt).
74. Valitse Sido.
75. Valitse puussa solmu Payments= Transactions\End to end identification code(End2EndID).
76. Laajenna puussa Transactions\$EndToEndID.
77. Valitse Sido.
78. Valitse puussa solmu Payments= Transactions\Instructed amount(InstructedAmount).
79. Valitse puussa Transactions\$Amount.
80. Valitse Sido.
81. Valitse puussa solmu Payments= Transactions\Transaction date(TransactionDate).
82. Valitse puussa solmu Transactions\Date(TransDate).
83. Valitse Sido.

## <a name="validate-created-mapping"></a>Luodun yhdistämismäärityksen tarkistaminen
1. Valitse Vahvista.
    * Varmista, että kaikki sidokset ovat kunnossa tarkistamalla uudet yhdistämismääritykset.  
2. Laajenna tai tiivistä Virheluettelo-osa napsauttamalla nuolta.
3. Valitse Tallenna.
4. Sulje sivu.
5. Sulje sivu.
6. Sulje sivu.

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a>Muuta mallikonfiguraation nykyisen version tilaa
1. Voit muuttaa tilaa valitsemalla Muuta.
    * Muuta suunnitellun mallimäärityksen tila Luonnos-tilasta Valmis-tilaan. Tällöin se on käytettävissä maksumuotoilurakenteessa.  
2. Valitse Valmis.
    * Valitse Valmis.  
3. Kirjoita arvo Kuvaus-kenttään.
    * Esimerkki: versio 1.  
4. Valitse OK.
5. Valitse nykyisen konfiguraation valmis versio.
    * Huomaa, että luotu konfiguraatio tallennetaan valmiina versiona 1.  


