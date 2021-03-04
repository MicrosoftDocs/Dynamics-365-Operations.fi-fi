---
title: ER Luodun muodon osien yhdistäminen tietomallielementteihin (marraskuu 2016)
description: Seuraavassa menettelyssä selitetään, miten käyttäjä, jolla on joko järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi yhdistää tietomallielementtejä sellaisen luodun sähköisen raportoinnin (ER) -konfiguraation osiin, joka määrittää maksujen liiketoimintatoimialueen sähköisen asiakirjamuodon.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 109a6736196b6ed3d1445a9f1a70c5f2b9d5af58
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684328"
---
# <a name="er-map-components-of-the-created-format-to-data-model-elements-november-2016"></a>ER Luodun muodon osien yhdistäminen tietomallielementteihin (marraskuu 2016)

[!include [banner](../../includes/banner.md)]

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
Seuraavissa vaiheissa muutetaan muotokonfiguraation tila Luonnos-tilasta Valmis-tilaksi. Tällöin sitä voi käyttää maksuasiakirjojen luontiin.  
1. Voit muuttaa tilaa valitsemalla Muuta.
2. Valitse Valmis.
3. Kirjoita arvo Kuvaus-kenttään.
    * Esimerkki: versio 1.  
4. Valitse OK.
5. Valitse nykyisen konfiguraation valmis versio.
    * Huomaa, että konfiguraatio tallennetaan suoritettuna versiona 1.1: tietomallin versioon 1 perustuva muodon versio 1.  

## <a name="define-effective-date-for-completed-version-of-format"></a>Muodon valmiin version voimaantulopäivämäärän määrittäminen
Jokainen muotoversio voidaan määrittää käytettäväksi tietystä päivämäärästä alkaen. Kun tiettynä päivänä on useita aktiivisia muotoversioita, käyttöön valitaan uusin muoto (versionumeron perusteella). Oikean version valinnassa käytetään istunnon päivämääräarvoa.  

## <a name="restrict-access-to-created-format-from-companies"></a>Luodun muodon käytön rajoittaminen yrityksiltä
1. Laajenna ISO maa-/aluekoodit -osa.
    * Kunkin muodon käyttöoikeutta voidaan rajoittaa määrittämällä maat/alueet, joissa muoto on käytettävissä. Kun tietyn muodon maiden ja alueiden luettelo on tyhjä, muotoa voi käyttää missä tahansa yrityksessä. Kun ISO-maa- ja -aluekoodeja lisätään maiden ja alueiden luetteloon, muotoa voi käyttää yrityksissä vain, jos niiden ensisijainen osoite on kyseisessä maassa tai kyseisellä alueella.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]