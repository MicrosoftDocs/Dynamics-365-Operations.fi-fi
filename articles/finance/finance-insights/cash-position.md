---
title: Kassatilanne (esiversio)
description: Tässä ohjeaiheessa kerrotaan, miten kassavirtaennustetoiminto ennustaa organisaation kassatilenteen tiettyinä aikoina. Se kuvaa myös vaihtoehdot, joiden avulla eri kausien ennusteet voidaan näyttää.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 5cf1ac4de07cb6357493a0b2c84f6a6ee591d4bc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990561"
---
# <a name="cash-position-preview"></a>Kassatilanne (esiversio)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Kassatilanne on kassavirran ennuste. Se perustuu kassakuittien ennusteeseen niiltä asiakkailta, jotka maksavat maksamattomia laskuja ja tilauksia ja myös ennusteen käteissuorituksiin, jotka on maksettu toimittajille ostolaskuja ja -tilauksia varten.

Kun järjestelmä ennustaa asiakasmaksut, se käyttää maksuennusteita asiakkaan maksuennustetoiminnosta. Ilman maksuennusteita maksupäivämäärän laskemisessa käytetään keskimääräistä aika, joka vaaditaan myyntilaskun muuntamiseksi maksuksi kullekin asiakkaalle. Avoimissa asiakastilauksissa järjestelmä laskee laskupäivämäärän käyttämällä päivien keskimääräistä määrää tilausriveillä laskutettavaa asiakasta kohti. Tämän jälkeen se käyttää laskupäivämäärää syötteenä maksuennustetoiminnossa. Asiakkaan maksuennustetoiminto laskee maḱsupäivämäärän jokaiselle tilausriville. 

<*Tarvitaanko Jarekilta ja Davelta tekstiä siitä, miten maksuennusteet muunnetaan tähän päivään*> Maksamattoman laskun maksupäivämäärä on [*arvioitu*] maksuennusteista valitsemalla päivämäärä, joka vastaa viidettäkymmenettä osaa kumulatiivisesta jakelutoiminnosta, joka saavutetaan ennustetun säilön todennäköisyyksistä.

Samankaltaista menetelmää käytetään toimittajille suoritettavien maksujen ennustamiseen. Järjestelmä laskee kullekin toimittajalle keskimääräisen ajan, joka vaaditaan toimittajan laskun muuntamiseen maksuksi. Tätä päivien määrää käytetään maksupäivämäärän laskemisessa. Järjestelmä laskee avoimille toimittajan tilauksille laskupäivämäärän ottamalla huomioon keskimääräisen päivien määrän, joka vaaditaan tilausrivien muuntamiseksi laskuksi kullekin toimittajalle. Järjestelmä laskee sitten maksupäivämäärän käyttämällä keskimääräistä aikaa, jonka avulla toimittajan lasku muunnetaan maksuksi.

**Kassatilanne**-välilehden yläosassa on kassatilannekaavio. Tässä kaaviossa näkyvät saapuvat ja lähtevät kassavirrat ja niiden vaikutus kokonaismaksuvalmiussaldoon. Kassatilannekaavion tiedot voidaan katsoa päivän, viikon, kuukauden tai neljännesvuoden kauden mukaan. Kun valitset **Päivittäin**, näkyvissä on seuraavien 21 päivän ennusteet. Kun valitset **Viikoittain**, näkyvissä on seuraavien 20 viikon ennusteet. Kun valitset **Kuukausittain**, näkyvissä on seuraavien 12 kuukauden ennusteet. Kun valitset **Neljännesvuosittain**, näkyvissä on seuraavien 12 neljännesvuoden ennusteet. Voit piilottaa kaavion, jos tarvitset lisä tilaa näytössä, kun haluat tarkastella **Kassatilanne**-välilehden sisältöä.

**Kassatilanne**-välilehden alaosassa ovat tiedot tilanteesta, kassavirrasta, ennustetuista maksuista ja pankkitilistä.

- **Tilanteen tiedot** -ruudukossa on kolme osaa: rahatilien luettelo, saapuvien kassavirtojen asiakirjojen luettelo ja lähtevien kassavirtojen asiakirjojen luettelo. Ruudukossa näkyvät myös kassatilanteen saldot. Ensimmäinen tarkasteltava kausi sisältää rahatilien saldon, joka on avaussaldo. Seuraavissa kausissa rahatilien saldot lasketaan saapuvien kassavirtojen lisäyksen ja edellisten kausien lähtevien kassavirtojen vähennyksen perusteella. Jos haluat tarkastella niiden tapahtumien tietoja, jotka muodostavat saldon, valitse **Saldo**-linkki.
- **Kassavirta**-ruudukossa näkyvät saapuvat ja lähtevät kassavirrat koottuna kauden mukaan sekä niiden vaikutus rahatilien saldoihin. Ensimmäinen kausi sisältää rahatilien saldon, joka on avaussaldo. Seuraavissa kausissa rahatilien saldot lasketaan saapuvien kassavirtojen lisäyksen ja edellisten kausien lähtevien kassavirtojen vähennyksen perusteella.
- **Ennustettu pankkitilin saldo** -ruudukossa on odotetut lähtevät kassavirrat ja niiden vaikutus rahatileihin.
- **Pankkitili**-ruudukossa on odottujen saapuvien ja lähtevien kassavirtojen vaikutus pankkitilin saldoon.

Jos haluat tallentaa ja muokata kassatilannetta, luo tilannevedos. Lisätietoja tilannevedosten käsittelemisestä on kohdassa [Tilannevedosten yleiskatsaus](payment-snapshots.md).

#### <a name="privacy-notice"></a>Tietosuojatiedot
Esiversiot (1) voivat käyttää vähemmän tietosuojaa ja suojaustoimenpiteitä kuin Dynamics 365 Finance and Operations -palvelu, (2) eivät sisälly tämän huoltotilauksen palvelutasosopimukseen, (3) niitä ei ole tarkoitettu henkilötietojen tai muiden sellaisten tietojen käsittelemiseen, joihin liittyy lainsäädännön tai määräysten vaatimustenmukaisuusvaatimuksia ja (4) niillä on rajoitettu tuki.
