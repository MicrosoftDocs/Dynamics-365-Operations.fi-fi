---
title: Konsernin sisäiset tilaukset ja palautustilaukset
description: Tässä aiheessa käsitellään konsernin sisäisiä tilauksia ja palautustilauksia
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 103225595e82bdedec6d97e5ebe5b61498377065
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548248"
---
# <a name="intercompany-orders-and-return-orders"></a>Konsernin sisäiset tilaukset ja palautustilaukset

[!include [banner](../../includes/banner.md)]

Tässä aiheessa käsitellään konsernin sisäisten ostotilausten, myyntitilausten, palautustilausten, ostosopimusten ja myyntisopimukset luontia ja päivitystä.

## <a name="about-intercompany-orders"></a>Tietoja konsernin sisäisistä tilauksista

Kun konsernin sisäinen myyntitilaus luodaan, Microsoft Dynamics 365 Supply Chain Management luo automaattisesti sitä vastaavan ostotilauksen. Samalla tavoin konsernin sisäisen ostotilauksen luonti johtaa automaattisesti vastaavan konsernin sisäisen myyntitilauksen luontiin.

Tämä koskee kahden osapuolen välisiä tilauksia (kahden toisiinsa liittyvän yrityksen välisiä tapahtumia) ja useimpia kolmen osapuolen yrityksiä (kun ulkoiselle asiakkaalle luodaan konsernin sisäisen tapahtuman lisäksi myyntitilaus).

## <a name="intercompany-order-example"></a>Esimerkki konsernin sisäisestä tilauksesta

Kyse on kahdesta toisiinsa liittyvästä yrityksestä. Yritys A on myynnin tytäryhtiö ja yritys B on jakeluyksikkö. Konsernin sisäiset myyntitilaukset ja ostotilaukset luodaan automaattisesti seuraavissa tilanteissa:

- Kun yritys A luo ostotilauksen ja toimittajana on yritys B, konsernin sisäinen myyntitilaus luodaan automaattisesti yritykselle B. Kahden osapuolen tilausketju muodostuu yrityksen A ostotilauksesta ja yrityksen B konsernin sisäisestä myyntitilauksesta.
- Kun yritys B luo myyntitilauksen ja asiakkaana on yritys A, konsernin sisäisen ostotilaus luodaan automaattisesti yritykselle A. Kahden osapuolen tilausketju muodostuu yrityksen B myyntitilauksesta ja yrityksen A konsernin sisäisestä ostotilauksesta.
- Kun yritys A luo ensimmäisen kerran myyntitilauksen ulkoiselle asiakkaalle, ostotilaus voidaan luoda automaattisesti yrityksessä A. Tällöin konsernin sisäinen myyntitilaus luodaan automaattisesti yrityksessä B. Kolmen osapuolen tilausketju muodostuu yrityksen A myyntitilauksesta ja ostotilauksesta sekä yrityksen B konsernin sisäisestä myyntitilauksesta.

## <a name="about-intercompany-return-orders"></a>Tietoja konsernin sisäisistä palautustilauksista

Konsernin sisäiset nimikkeet voidaan palauttaa muiden palautusten tavoin. Konsernin sisäisten nimikkeiden yhteydessä ulkoisen asiakkaan palautustilaus luo kuitenkin konsernin sisäiseen ostotilauksen. Se puolestaan aiheuttaa automaattisesti konsernin sisäisen myynnin palautustilauksen luonnin. Konsernin sisäisen nimikkeen voi palauttaa myös ilman ulkoisen asiakkaan palautustilausta.

Tavallisia palautustilauksia vastaavat konsernin sisäiset palautustilaukset aloitetaan **Luo palautustilaus** -sivulla.

Konsernin sisäiset myynti- ja ostosopimukset päivittyvät Microsoft Dynamics 365 Supply Chain Managementissa automaattisesti palautettua nimekettä vastaavaksi. Kyseisen nimikkeen myynti- tai ostosopimussitoumus muutetaan automaattisesti vastaamaan määrän tai summan muutosta, kun nimike palautetaan.

## <a name="intercompany-return-order-example"></a>Esimerkki konsernin sisäisestä palautustilauksesta

Yritys A luo ostotilauksen, joka on linkitetty konsernin sisäiseen nimikkeen ostosopimukseen. Konsernin sisäinen myyntitilaus luodaan automaattisesti yrityksessä B, joka on linkitetty vastaavaan myyntisopimukseen. Osto- ja myyntisopimus yhdistetään konsernin sisäisiksi sopimuksiksi.

Yritys A palauttaa konsernin sisäisen nimikkeen yritykselle B. Yritys B luo palautustilauksen nimikkeelle ja yritys A luo automaattisesti oston palautustilauksen. Sekä ostosopimuksen että myyntisopimuksen sitoumukset, jotka on linkitetty alkuperäisiin tilauksiin, oikaistaan automaattisesti vastaamaan määrän tai summan muutosta.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
