---
title: Kassatilanne
description: Tässä artikkelissa kerrotaan, miten kassavirtaennustetoiminto ennustaa organisaation kassatilanteen tiettyinä aikoina. Se kuvaa myös vaihtoehdot, joiden avulla eri kausien ennusteet voidaan näyttää.
author: ShivamPandey-msft
ms.date: 12/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 7581142348d91b3a37cc75cf801e7bfc098cd604
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870246"
---
# <a name="cash-position"></a>Kassatilanne

[!include [banner](../includes/banner.md)]

Kassatilanne on kassavirran ennuste. Se perustuu kassakuittien ennusteeseen niiltä asiakkailta, jotka maksavat maksamattomia laskuja ja tilauksia ja myös ennusteen käteissuorituksiin, jotka on maksettu toimittajille ostolaskuja ja -tilauksia varten.

Kun järjestelmä ennustaa asiakasmaksut, se käyttää maksuennusteita asiakkaan maksuennustetoiminnosta. Ilman maksuennusteita maksupäivämäärän laskemisessa käytetään keskimääräistä aika, joka vaaditaan myyntilaskun muuntamiseksi maksuksi kullekin asiakkaalle. Avoimissa asiakastilauksissa järjestelmä laskee laskupäivämäärän käyttämällä päivien keskimääräistä määrää tilausriveillä laskutettavaa asiakasta kohti. Tämän jälkeen se käyttää laskupäivämäärää syötteenä maksuennustetoiminnossa. Asiakkaan maksuennustetoiminto laskee maḱsupäivämäärän jokaiselle tilausriville. 

Maksamattoman laskun maksupäivämäärä on arvioitu maksuennusteista valitsemalla päivämäärä, joka vastaa viidettäkymmenettä osaa kumulatiivisesta jakelutoiminnosta, joka saavutetaan ennustetun säilön todennäköisyyksistä.

Samankaltaista menetelmää käytetään toimittajille suoritettavien maksujen ennustamiseen. Järjestelmä laskee kullekin toimittajalle keskimääräisen ajan, joka vaaditaan toimittajan laskun muuntamiseen maksuksi. Tätä päivien määrää käytetään maksupäivämäärän laskemisessa. Järjestelmä laskee avoimille toimittajan tilauksille laskupäivämäärän ottamalla huomioon keskimääräisen päivien määrän, joka vaaditaan tilausrivien muuntamiseksi laskuksi kullekin toimittajalle. Järjestelmä laskee sitten maksupäivämäärän käyttämällä keskimääräistä aikaa, jonka avulla toimittajan lasku muunnetaan maksuksi.

**Kassatilanne**-välilehden yläosassa on kassatilannekaavio. Tässä kaaviossa näkyvät saapuvat ja lähtevät kassavirrat ja niiden vaikutus kokonaismaksuvalmiussaldoon. Kassatilannekaavion tiedot voidaan katsoa päivän, viikon, kuukauden tai neljännesvuoden kauden mukaan. Kun valitset **Päivittäin**, näkyvissä on seuraavien 21 päivän ennusteet. Kun valitset **Viikoittain**, näkyvissä on seuraavien 20 viikon ennusteet. Kun valitset **Kuukausittain**, näkyvissä on seuraavien 12 kuukauden ennusteet. Kun valitset **Neljännesvuosittain**, näkyvissä on seuraavien 12 neljännesvuoden ennusteet. Voit piilottaa kaavion, jos tarvitset lisä tilaa näytössä, kun haluat tarkastella **Kassatilanne**-välilehden sisältöä.

**Kassatilanne**-välilehden alaosassa ovat tiedot tilanteesta, kassavirrasta, ennustetuista maksuista ja pankkitilistä.

- **Tilanteen tiedot** -ruudukossa on kolme osaa: rahatilien luettelo, saapuvien kassavirtojen asiakirjojen luettelo ja lähtevien kassavirtojen asiakirjojen luettelo. Ruudukossa näkyvät myös kassatilanteen saldot. Ensimmäinen tarkasteltava kausi sisältää rahatilien saldon, joka on avaussaldo. Seuraavissa kausissa rahatilien saldot lasketaan saapuvien kassavirtojen lisäyksen ja edellisten kausien lähtevien kassavirtojen vähennyksen perusteella. Jos haluat tarkastella niiden tapahtumien tietoja, jotka muodostavat saldon, valitse **Saldo**-linkki.
- **Kassavirta**-ruudukossa näkyvät saapuvat ja lähtevät kassavirrat koottuna kauden mukaan sekä niiden vaikutus rahatilien saldoihin. Ensimmäinen kausi sisältää rahatilien saldon, joka on avaussaldo. Seuraavissa kausissa rahatilien saldot lasketaan saapuvien kassavirtojen lisäyksen ja edellisten kausien lähtevien kassavirtojen vähennyksen perusteella.
- **Ennustettu pankkitilin saldo** -ruudukossa on odotetut lähtevät kassavirrat ja niiden vaikutus rahatileihin.
- **Pankkitili**-ruudukossa on odottujen saapuvien ja lähtevien kassavirtojen vaikutus pankkitilin saldoon.

Jos haluat tallentaa ja muokata kassatilannetta, luo tilannevedos. Lisätietoja tilannevedosten käsittelemisestä on kohdassa [Tilannevedosten yleiskatsaus](payment-snapshots.md).

## <a name="details-of-the-cash-position-capability"></a>Kassatilanneominaisuuden tiedot 

Kassatilanneominaisuus sisältää seuraavat toiminnot. 

- Kassatilannetoiminto näyttää kassavirran järjestelmässä aiemmin luotujen asiakirjojen sekä ulkoisista järjestelmistä tuotavien kassavirta- ja ulosvirtausrivien perusteella.
- Kassavirtatietojen helppo integroiminen ulkoisista järjestelmistä Dynamics 365 Financeen. Kassatilanne voi käyttää myös tietojen tuonti- ja vientikehystä. Tämän kehyksen avulla on helppo integroida tiedot Excel ODatan kanssa. Voit yhdistää tietoja useista lähteistä ja luoda kattavan kassatilanneratkaisun.
- Esittelee älykkään kassatilanteen. Kassatilanne luodaan asiakkaan maksutoiminnan perusteella. Sen avulla ennustetaan, milloin yritys voi odottaa rahojen tulevan tilille.
- Asiakastilausten ja laskujen yhteydessä asiakkaan maksujen ennusteen tekoälytoimintojen avulla määritetään asiakkaan historiallinen maksutoiminta tilauksen tai laskun maksamisen yhteydessä.
- Toimittajatilauksissa ja laskuissa käytetään keskimääräistä aikaa lähetyksen ja laskun välillä sekä toimittajalaskun maksamista. Näin määritetään, milloin toimittajatilaus tai lasku maksetaan, mikä tekee kassavirroista tarkempia.

Tämä luo kassavirran tarkemman näkymän, joka perustuu asiakkaiden historiallisiin maksutoimintoihin. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
