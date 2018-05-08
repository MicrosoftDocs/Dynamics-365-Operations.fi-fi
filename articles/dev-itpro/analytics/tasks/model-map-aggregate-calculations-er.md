--- 
title: "Koontilaskelmien mallin yhdistämismäärityksen konfiguraation käyttäminen tietokantatasolla (ER)"
description: "Tämä menettely sisältää tietoja siitä, miten voit suunnitella uuden sähköisen raportoinnin (ER) mallin yhdistämismäärityksen konfiguraation ja käyttää sisäänrakennettuja ER-toimintoja laskelmien tehokkaassa koostamisessa."
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7be3e9970e2599c159e7c9d414b54876d0116350
ms.openlocfilehash: 869a23b992f1d6dccf9327b66b3e4d611728efce
ms.contentlocale: fi-fi
ms.lasthandoff: 03/09/2018

---
# <a name="use-a-model-mapping-configuration-for-aggregate-calculations-at-the-database-leveler"></a>Koontilaskelmien mallin yhdistämismäärityksen konfiguraation käyttäminen tietokantatasolla (ER) 

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tämä menettely sisältää tietoja siitä, miten voit suunnitella uuden sähköisen raportoinnin (ER) mallin yhdistämismäärityksen konfiguraation ja käyttää sisäänrakennettuja ER-toimintoja laskelmien tehokkaassa koostamisessa. Tässä menettelyssä luodaan konfiguraatio malliyritykselle Litware, Inc. 

Tämä menettely on luotu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli. Nämä vaiheet voidaan suorittaa minkä tahansa tietojoukon avulla.

 Voit suorittaa nämä vaiheet, jos suoritat ensin vaiheet menettelystä ER parantaa koontilaskentojen tehokkuutta suorittamalla laskennat tietokannan tasolla (Osa 1: Konfiguraatioiden valmisteleminen).

1. Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.
2. Laajenna puussa solmu "Intrastat model".
3. Valitse puussa Intrastat model\Intrastat sample mapping.
4. Valitse Suunnittelutoiminto.
5. Valitse Suunnittelutoiminto.
6. Valitse puussa Dynamics 365 for Operations\Table records.
7. Valitse Lisää juuri.
    * Lisää uusi tietolähde, joka edustaa ryhmiteltäviä tietueita.  
8. Kirjoita Nimi-kenttään Tapahtumat.
    * Tapahtumat  
9. Syötä Taulu-kenttään Intrastat.
    * Intrastat  
10. Valitse OK.
11. Valitse valikkopuussa Toiminnot\Ryhmittely.
    * Tätä tietolähteen tyyppiä käytetään uuden tietolähteen esittelemisessä suorituksen aikana ryhmätietueille sekä vaadittujen koosteiden laskemisessa.  
12. Valitse Lisää juuri.
13. Kirjoita Nimi-kenttään TransactionsGroups.
    * TransactionsGroups  
14. Napsauta Muokkaa ryhmittelyä.
15. Valitse puussa solmu Transactions.
    * Valitse lisätty tietolähde, jonka tyyppi on Tietueluettelo ja joka edustaa ryhmiteltäviä tietueita.  
16. Napsauta Lisää kenttä kohteeseen.
17. Napsauta Mitä ryhmään.
18. Laajenna puussa solmu Transactions.
19. Valitse puussa Transactions\Direction.
20. Napsauta Lisää kenttä kohteeseen.
21. Napsauta Ryhmitellyt kentät.
    * Valitse kenttä ja määritä ryhmittelytaso. Tämän valinnan perusteella tietolähde palauttaa suorituksen aikana niin monta tapahtumaryhmää Intrastat-taulukkoa vastaavia suuntakoodeja löytyy.  
22. Valitse puussa Transactions\Invoice amount(AmountMST).
    * Valitse kenttä, kun haluat määrittää koontilaskelman lähteen.  
23. Napsauta Lisää kenttä kohteeseen.
24. Napsauta Koostekentät.
25. Merkitse valittu rivi luettelossa.
26. Valitse Menetelmä-kentässä Summa.
    * Valitse koontityyppi.  
27. Kirjoita Nimi-kenttään SumOfAmountMST.
    * Määritä tälle koonnille nimi määritetyssä tietolähteessä.  
28. Valitse Tallenna.
    * Huomaa, että Suoritus-kenttä osoittaa tämän ryhmittelyn tapahtuvan suorituksen aikana SQL-tietokannassa.  
29. Sulje sivu.
30. Valitse OK.
31. Laajenna puussa 'Totals'.
32. Laajenna puussa 'TransactionsGroups'.
33. Laajenna puussa TransactionsGroups\aggregated.
34. Valitse puussa TransactionsGroups\aggregated\SumOfAmountMST.
35. Valitse puussa Totals\Total invoice value(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded').
36. Valitse Sido.
    * Tämän asetuksen perusteella tietoläde laskee AmountMST-kentän arvojen summan kaikille tapahtumaryhmille. Tämä koontilaskelma on käytettävissä TransactionsGroups.aggregated.TotalAmount-nimikkeenä.  
37. Laajenna puussa 'TransactionsGroups'.
38. Valitse puussa 'TransactionsGroups'.
39. Valitse Muokkaa.
40. Napsauta Muokkaa ryhmittelyä.
41. Laajenna puussa solmu Transactions.
42. Valitse puussa Transactions\Invoice amount(AmountMST).
43. Napsauta Lisää kenttä kohteeseen.
44. Napsauta Koostekentät.
45. Merkitse valittu rivi luettelossa.
46. Valitse Menetelmä-kentässä Enintään.
47. Kirjoita Nimi-kenttään MaxOfAmountMST.
48. Valitse Tallenna.
    * Tällä hetkellä GROUPBY-tietolähteiden suoritus voidaan kääntää SQL-tietokannan tasolle tietyin rajoituksin. Käännökset voidaan tehdä joko Tietueluettelo-tyypin tietolähteille tai FILTER-toimintoa käyttävää lauseketta edustaville tietolähteille. Se voidaan tehdä myös, kun ryhmittelytietueiden yhdelle kentälle on määritetty yksi koonti.  
    * Huomaa, että AmountMST-kentälle määritettiin useita koosteita, Suoritus:-kenttä ilmaisee edelleen, että tämä ryhmittely suoritetaan ajoaikana SQL-tietokannassa. Tämä johtuu siitä, että vain yksi kooste on sidottu tietomallinimikkeeseen ja vain sillä noudetaan ajoaikana tietoja tästä tietolähteestä.  
49. Sulje sivu.
50. Valitse OK.
51. Laajenna puussa 'TransactionsGroups'.
52. Laajenna puussa TransactionsGroups\aggregated.
53. Valitse puussa TransactionsGroups\aggregated\MaxOfAmountMST.
54. Valitse puussa Totals\Total statistical value(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded').
55. Valitse Sido.
56. Laajenna puussa 'TransactionsGroups'.
57. Valitse puussa 'TransactionsGroups'.
58. Valitse Muokkaa.
59. Napsauta Muokkaa ryhmittelyä.
    * Huomaa, että Suoritus-kenttä osoittaa, että tämä ryhmittely tehdään suorituksen aikana muistissa, koska molemmat saman kentän koonnit on sidottu tietomallin nimikkeisiin.   
60. Merkitse kaikki rivit tai poista kaikkien rivien merkinnät luettelossa.
61. Valitse Poista.
62. Valitse Kyllä.
63. Valitse Poista.
64. Valitse Kyllä.
65. Napsauta Lisää kenttä kohteeseen.
66. Napsauta Mitä ryhmään.
67. Laajenna puussa 'Commodity record(Intrastat)'.
68. Valitse Tallenna.
    * Huomaa, että Suoritus-kenttä osoittaa tämän ryhmittelyn tapahtuvan suorituksen aikana muistissa, vaikka koonteja ei ole määritetty ja valittu Taulukkotietueet-tyyppinen tietolähde viittaa samaan Intrastat-taulukkoon. Tämä johtuu siitä, että tietolähde sisältää joitakin laskettuja kenttiä, joita ei voi vielä kääntää SQL-tietokannan tasolle.  


