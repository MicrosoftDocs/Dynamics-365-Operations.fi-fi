---
title: ER Suunnittele toimialueen erityistietomalli
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda uuden sähköiselle raportoinnin (ER) konfiguraation lähteen, joka sisältää sähköisen maksun asiakirjojen tietomallin.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0debb7276c4f3e41c2e85ce6bc63b8df5bc159f8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551519"
---
# <a name="er-design-domain-specific-data-model"></a>ER Suunnittele toimialueen erityistietomalli

[!include [task guide banner](../../includes/task-guide-banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda uuden sähköiselle raportoinnin (ER) konfiguraation lähteen, joka sisältää sähköisen maksun asiakirjojen tietomallin. Tietomallia käytetään myöhemmin tietolähteenä, kun maksuasiakirjojen muoto määritetään.



Tässä esimerkissä luodaan konfiguraatio malliyritykselle Litware, Inc. Nämä vaiheet voidaan suorittaa mille tahansa yritykselle, koska kaikki yritykset jakavat ER-konfiguraatiot. Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.

1. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.
    * Valitse malliyrityksen Litware, Inc:n konfiguraation lähde. Jos lähde ei ole näkyvissä, suorita ensin Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet.  
2. Valitse Raportointikonfiguraatiot.
    * Luodaan konfiguraatio, joka sisältää tietomallin sähköisen maksun asiakirjoja varten. Tietomallia käytetään myöhemmin tietolähteenä, kun maksujen asiakirjojen muoto määritetään.  

## <a name="create-a-new-data-model-configuration"></a>Uuden tietomallin konfiguraation luominen
1. Avaa valintaikkuna napsauttamalla Luo konfigurointi.
2. Syötä Nimi-kenttään Maksut (yksinkertaistettu malli).
    * Maksut (yksinkertaistettu malli)  
3. Syötä Kuvaus-kenttään Maksumallin konfiguraatio.
    * Maksumallin konfiguraatio  
    * Aktiivinen konfiguraation lähde syötetään tässä automaattisesti. Tämä lähde voi ylläpitää tätä konfiguraatiota. Muut lähteet voivat käyttää tätä konfiguraatiota, mutta eivät ylläpitää sitä.  
4. Suorita konfiguraation luontitehtävä valitsemalla Luo konfiguraatio

## <a name="create-a-data-model"></a>Tietomallin luominen
    * Olet luomassa valitulle määritykselle uutta tietomallia. Konfiguraation version tilaksi tulee Luonnos.  
1. Valitse Suunnittelutoiminto.

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a>Maksuprosessiin osallistuvan osapuolen rakenteen määrittäminen
1. Avaa valintaikkuna valitsemalla Uusi.
2. Kirjoita Nimi-kenttään Osapuoli.
    * Osapuoli  
3. ValitseLisää.
4. Avaa valintaikkuna valitsemalla Uusi.
5. Syötä Nimi-kenttään Nimi.
    * Nimi  
6. Valitse Nimiketyyppi-kentässä Merkkijono.
7. ValitseLisää.
8. Kirjoita Etsi-kenttään "Osapuoli".
    * Osapuoli  
9. Valitse Etsi edellinen.

## <a name="define-the-bank-structure-for-this-model"></a>Pankkirakenteen määrittäminen tälle mallille
1. Avaa valintaikkuna valitsemalla Uusi.
2. Syötä Nimi-kenttään Agentti.
    * Edustaja  
3. Valitse Nimiketyyppi-kentässä Tietue.
4. ValitseLisää.
5. Kirjoita Kuvaus-kenttään "Rahoituslaitos (esimerkiksi pankki), joka hoitaa osapuolen (maksajan tai laskuttajan) tiliä".
    * Rahoituslaitos (esimerkiksi pankki), joka hoitaa osapuolen (maksajan tai laskuttajan) tiliä.  
6. Avaa valintaikkuna valitsemalla Uusi.
7. Syötä Nimi-kenttään Nimi.
    * Nimi  
8. Valitse Nimiketyyppi-kentässä Merkkijono.
9. ValitseLisää.
10. Avaa valintaikkuna valitsemalla Uusi.
11. Syötä Nimi-kenttään SWIFT.
    * SWIFT-koodi  
12. ValitseLisää.
13. Kirjoita Kuvaus-kenttään "BIC-koodi".
    * BIC-koodi  
14. Avaa valintaikkuna valitsemalla Uusi.
15. Syötä Nimi-kenttään RoutingNumber.
    * RoutingNumber  
16. ValitseLisää.
17. Kirjoita Kuvaus-kenttään "Pankkikoodi".
    * Pankkikoodi  
18. Valitse Etsi edellinen.

## <a name="define-the-bank-account-structure-for-this-model"></a>Pankkitilirakenteen määrittäminen tälle mallille
1. Avaa valintaikkuna valitsemalla Uusi.
2. Syötä Nimi-kenttään Tili.
    * Tili  
3. Valitse Nimiketyyppi-kentässä Tietue.
4. ValitseLisää.
5. Kirjoita Kuvaus-kenttään "Osapuolen tilin tunnus rahoituslaitoksessa (kuten pankissa)".
    * Osapuolen tilin tunnus rahoituslaitoksessa (kuten pankissa).  
6. Avaa valintaikkuna valitsemalla Uusi.
7. Syötä Nimi-kenttään Valuutta.
    * Valuutta  
8. Valitse Nimiketyyppi-kentässä Merkkijono.
9. ValitseLisää.
10. Kirjoita Kuvaus-kenttään "Valuuttakoodi".
    * Valuuttakoodi  
11. Avaa valintaikkuna valitsemalla Uusi.
12. Syötä Nimi-kenttään Numero.
    * Numero  
13. ValitseLisää.
14. Avaa valintaikkuna valitsemalla Uusi.
15. Syötä Nimi-kenttään IBAN.
    * IBAN-tilinumero  
16. ValitseLisää.
17. Kirjoita Kuvaus-kenttään "Kansainvälinen tilinumero (IBAN)".
    * Kansainvälinen tilinumero (IBAN)  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a>Tilisiirtomaksun tyypin maksuviestirakenteen määrittäminen
1. Avaa valintaikkuna valitsemalla Uusi.
2. Kirjoita Uusi solmu muodossa -kenttään "Mallin juuri".
3. Syötä Nimi-kenttään CustomerCreditTransferInitiation.
    * CustomerCreditTransferInitiation  
4. ValitseLisää.
5. Kirjoita Etsi--kenttään CustomerCreditTransferInitiation.
    * CustomerCreditTransferInitiation  
6. Valitse Etsi edellinen.
7. Avaa valintaikkuna valitsemalla Uusi.
8. Syötä Nimi-kenttään MessageIdentification.
    * MessageIdentification  
9. ValitseLisää.
10. Kirjoita Kuvaus-kenttään "Osoitetaan pisteviitteeseen ohjaavan osapuolen määrityksen mukaisesti (ja lähetetään seuraavalle osapuolelle) viestin tunnistamista varten".
    * Pisteestä pisteeseen -viite, jonka ohjaava osapuoli on määrittänyt (ja lähettänyt seuraavalle osapuolelle) viestin tunnistamista varten.  
11. Avaa valintaikkuna valitsemalla Uusi.
12. Syötä Nimi-kenttään ProcessingDateTime.
    * ProcessingDateTime  
13. Valitse Nimiketyyppi-kentässä DateTime.
14. ValitseLisää.
15. Kirjoita Kuvaus-kenttään "Päivämäärä ja kellonaika, jolloin maksun viesti luotiin".
    * Päivämäärä ja kellonaika, jolloin maksun viesti luotiin.  
16. Avaa valintaikkuna valitsemalla Uusi.
    * Pankkitapahtumarakenteen määrittäminen tälle mallille.  
17. Syötä Nimi-kenttään Maksut.
    * Maksut  
18. Valitse Nimiketyyppi-kentässä Tietueluettelo.
19. ValitseLisää.
20. Syötä Kuvaus-kenttään Nykyisen viestin maksurivi.
    * Nykyisen viestin maksurivit  
21. Avaa valintaikkuna valitsemalla Uusi.
22. Syötä Nimi-kenttään Laskuttaja.
    * Laskuttaja  
23. Valitse Nimiketyyppi-kentässä Tietue.
24. ValitseLisää.
25. Kirjoita Kuvaus-kenttään "Osapuoli, jolle rahasumma on maksettava".
    * Osapuoli, jolle rahasumma on maksettava.  
26. Valitse Muuta nimikkeen viitettä.
27. Kirjoita Etsi-kenttään "Osapuoli".
    * Osapuoli  
28. Valitse Etsi seuraava.
29. Valitse OK.
30. Kirjoita Etsi-kenttään "Maksut".
    * Maksut  
31. Valitse Etsi seuraava.
32. Avaa valintaikkuna valitsemalla Uusi.
33. Syötä Nimi-kenttään Maksaja.
    * Maksaja  
34. ValitseLisää.
35. Kirjoita Kuvaus-kenttään "Osapuoli, joka on rahasumman velkaa (lopulliselle) laskuttajalle".
    * Osapuoli, joka on rahasumman velkaa (lopulliselle) laskuttajalle.  
36. Valitse Muuta nimikkeen viitettä.
37. Kirjoita Etsi-kenttään "Osapuoli".
    * Osapuoli  
38. Valitse Etsi seuraava.
39. Valitse OK.
40. Valitse Etsi seuraava.
41. Avaa valintaikkuna valitsemalla Uusi.
42. Syötä Nimi-kenttään kuvaus.
    * kuvaus  
43. Valitse Nimiketyyppi-kentässä Merkkijono.
44. ValitseLisää.
45. Avaa valintaikkuna valitsemalla Uusi.
46. Syötä Nimi-kenttään Valuutta.
    * Valuutta  
47. ValitseLisää.
48. Kirjoita Kuvaus-kenttään "Valuuttakoodi".
    * Valuuttakoodi  
49. Avaa valintaikkuna valitsemalla Uusi.
50. Syötä Nimi-kenttään TransactionDate.
    * TransactionDate  
51. Valitse Nimiketyyppi-kentässä Päivämäärä.
52. ValitseLisää.
53. Kirjoita Kuvaus-kenttään "Tapahtumapäivä".
    * Tapahtuman päivämäärä  
54. Avaa valintaikkuna valitsemalla Uusi.
55. Syötä Nimi-kenttään InstructedAmount.
    * InstructedAmount  
56. Valitse Nimiketyyppi-kentässä Reaaliluku.
57. ValitseLisää.
58. Kirjoita Kuvaus-kenttään "Maksajan ja laskuttajan välillä siirrettävä rahasumma ennen maksupidätyksiä. Summa ilmaistaan aloittavan osapuolen määrittämänä valuuttana.
    * Maksajan ja laskuttajan välillä siirrettävä rahasumma ennen maksupidätyksiä. Summa ilmaistaan aloittavan osapuolen määrittämänä valuuttana.  
59. Avaa valintaikkuna valitsemalla Uusi.
60. Syötä Nimi-kenttään End2EndID.
    * End2EndID  
61. Valitse Nimiketyyppi-kentässä Merkkijono.
62. ValitseLisää.
63. Kirjoita Kuvaus-kenttään "Aloittavan osapuolen määrittämä yksilöivä tunnus. Tunnus välitetään muuttumattomana koko päästä päähän -ketjun läpi.
    * Aloittavan osapuolen määrittämä yksilöivä tunnus. Tunnus välitetään muuttumattomana koko päästä päähän -ketjun läpi.  
64. Syötä Nimi-kenttään PaymentModel.
    * PaymentModel-nimi on linjassa maksulomakkeiden ennalta määritettyjen käyttöliittymien kanssa.  
65. Valitse Tallenna.
66. Sulje sivu.

