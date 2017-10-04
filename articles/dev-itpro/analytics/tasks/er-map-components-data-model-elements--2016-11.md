--- 
title: "Tietomallielementtien määrittäminen luodun muodon komponentit sähköistä raportointia (ER) varten"
description: "Seuraavassa menettelyssä selitetään, miten käyttäjä, jolla on joko järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi yhdistää tietomallielementtejä sellaisen luodun sähköisen raportoinnin (ER) -konfiguraation osiin, joka määrittää maksujen liiketoimintatoimialueen sähköisen asiakirjamuodon."
author: NickSelin
manager: AnnBe
ms.date: 02/27/2017
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
ms.openlocfilehash: df3dcd6d5242c516f254450a727d8a754bd74f6a
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="map-components-of-the-created-format-to-data-model-elements-for-electronic-reporting-er"></a>Tietomallielementtien määrittäminen luodun muodon komponentit sähköistä raportointia (ER) varten

[!include[task guide banner](../../includes/task-guide-banner.md)]

Seuraavassa menettelyssä selitetään, miten käyttäjä, jolla on joko järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi yhdistää tietomallielementtejä sellaisen luodun sähköisen raportoinnin (ER) -konfiguraation osiin, joka määrittää maksujen liiketoimintatoimialueen sähköisen asiakirjamuodon. Tällä muodolla luodaan myöhemmin sähköisiä asiakirjoja maksujen käsittelyä varten. Tässä esimerkissä luodaan muotokonfiguraatio malliyritykselle Litware Inc. Nämä vaiheet voidaan suorittaa mille tahansa yritykselle, koska kaikki yritykset jakavat ER-konfiguraatiot. Voit suorittaa nämä vaiheet, jos Uuden muotokonfiguraation luominen- tehtäväoppaan vaiheet on suoritettu.


## <a name="select-a-format-configuration"></a>Muotokonfiguraation valitseminen
1. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.
2. Valitse Raportointikonfiguraatiot.
3. Laajenna puussa solmu Payments (simplified model).
4. Valitse puussa solmu Payments (simplified model)\BACS (UK fictitious).
5. Valitse Suunnittelutoiminto.

## <a name="map-format-components-to-data-model-elements"></a>Muotokomponenttien yhdistäminen tietomallielementteihin
1. Valitse Laajenna tai tiivistä.
2. Valitse Yhdistämismääritys-välilehti.
3. Laajenna puussa solmu model.
4. Valitse puussa Xml\Sanoma\ProcessingDate\DateTime.
5. Valitse puussa malli\ProcessingDateTime.
6. Valitse Sido.
7. Valitse puussa Xml\Sanoma\MessageId\Merkkijono.
8. Valitse puussa malli\MessageIdentification.
9. Valitse Sido.
10. Laajenna puussa solmu model\Payments.
11. Valitse puussa Xml\Sanoma\Maksut\Nimike\Summa\Merkkijono.
12. Valitse puussa malli\Maksut\InstructedAmount.
13. Valitse Sido.
14. Valitse puussa Xml\Sanoma\Maksut\Nimike\TransDate\DateTime.
15. Valitse puussa malli\Maksut\TransactionDate.
16. Valitse Sido.
17. Valitse puussa Xml\Sanoma\Maksut\Nimike\Kuvaus\Merkkijono.
18. Valitse puussa solmu model\Payments\Description.
19. Valitse Sido.
20. Valitse puussa Xml\Sanoma\Maksut\Nimike\Valuutta\Merkkijono.
21. Valitse puussa solmu Malli\Maksut\Kuvaus.
22. Valitse Sido.
23. Valitse puussa Xml\Sanoma\Maksut\Nimike\Tunnus.
24. Valitse puussa malli\Maksut\End2EndID'.
25. Valitse Sido.
26. Laajenna puussa solmu model\Payments\Creditor.
27. Laajenna puussa solmu model\Payments\Creditor\Account.
28. Laajenna puussa solmu expand 'model\Payments\Creditor\Agent.
29. Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja\Nimi\Merkkijono.
30. Valitse puussa solmu model\Payments\Creditor\Name.
31. Valitse Sido.
32. Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja\Pankki\RoutingNumber\String.
33. Valitse puussa malli\Maksut\Laskuttaja\Edustaja\RoutingNumber.
34. Valitse Sido.
35. Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja\Pankki\AccountNumber\Merkkijono.
36. Valitse puussa solmu model\Payments\Creditor\Account\Number.
37. Valitse Sido.
38. Valitse puussa Xml\Sanoma\Maksut\Nimike\Maksaja\Nimi\Merkkijono.
39. Laajenna puussa solmu model\Payments\Debtor.
40. Laajenna puussa solmu model\Payments\Debtor\Account.
41. Laajenna puussa solmu model\Payments\Debtor\Agent.
42. Valitse puussa solmu model\Payments\Debtor\Name.
43. Valitse Sido.
44. Valitse puussa Xml\Sanoma\Maksut\Nimike\Maksaja\Pankki\RoutingNumber\Merkkijono.
45. Valitse puussa malli\Maksut\Maksaja\Edustaja\RoutingNumber.
46. Valitse Sido.
47. Valitse puussa Xml\Sanoma\Maksut\Nimike\Maksaja\Pankki\AccountNumber\Merkkijono.
48. Valitse puussa solmu model\Payments\Debtor\Account\Number.
49. Valitse Sido.
50. Valitse puussa Xml\Sanoma\Maksut\Nimike.
51. Laajenna puussa solmu model\Payments.
52. Valitse Sido.
53. Valitse Tallenna.

## <a name="validate-format-mapping"></a>Muotoyhdistämismäärityksen tarkistaminen
1. Valitse Vahvista.
    * Varmista, että kaikki sidokset ovat kunnossa tarkistamalla uudet yhdistämismääritykset.  
2. Sulje sivu.

## <a name="change-status-of-the-current-version-of-format-configuration"></a>Muotokonfiguraation nykyisen version tilan muuttaminen
    * Seuraavissa vaiheissa muutetaan muotokonfiguraation tila Luonnos-tilasta Valmis-tilaksi. Tällöin sitä voi käyttää maksuasiakirjojen luontiin.  
1. Voit muuttaa tilaa valitsemalla Muuta.
2. Valitse Valmis.
3. Kirjoita arvo Kuvaus-kenttään.
    * Esimerkki: versio 1.  
4. Valitse OK.
5. Valitse nykyisen konfiguraation valmis versio.
    * Huomaa, että konfiguraatio tallennetaan suoritettuna versiona 1.1: tietomallin versioon 1 perustuva muodon versio 1.  

## <a name="define-effective-date-for-completed-version-of-format"></a>Muodon valmiin version voimaantulopäivämäärän määrittäminen
    * Jokainen muotoversio voidaan määrittää käytettäväksi tietystä päivämäärästä alkaen. Kun tiettynä päivänä on useita aktiivisia muotoversioita, käyttöön valitaan uusin muoto (versionumeron perusteella). Oikean version valinnassa käytetään istunnon päivämääräarvoa.  

## <a name="restrict-access-to-created-format-from-companies"></a>Luodun muodon käytön rajoittaminen yrityksiltä
1. Laajenna ISO maa-/aluekoodit -osa.
    * Kunkin muodon käyttöoikeutta voidaan rajoittaa määrittämällä maat/alueet, joissa muoto on käytettävissä. Kun tietyn muodon maiden ja alueiden luettelo on tyhjä, muotoa voi käyttää missä tahansa yrityksessä. Kun ISO-maa- ja -aluekoodeja lisätään maiden ja alueiden luetteloon, muotoa voi käyttää yrityksissä vain, jos niiden ensisijainen osoite on kyseisessä maassa tai kyseisellä alueella.  

