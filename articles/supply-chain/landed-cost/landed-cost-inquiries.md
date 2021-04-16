---
title: Aiheutuneiden kustannusten kyselyt
description: Tässä aiheessa kuvataan, miten Aiheutunut kustannus -moduulissa käytettävissä olevia erilaisia kyselyitä löytyy ja käytetään.
author: sherry-zheng
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMLine, ITMItemTracking, ITMContainerActivityTracking, ITMContainerTracking
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-21
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 22a2e76780adb43b053b6cf7fd08411a4a60aeac
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823358"
---
# <a name="landed-cost-inquiries"></a>Aiheutuneiden kustannusten kyselyt

[!include [banner](../../includes/banner.md)]

## <a name="voyage-line-inquiries"></a>Merikuljetuksen rivien kyselyt

**Merikuljetuksen rivit** -kysely näyttää kaikki varastoa koskevat merikuljetuksen rivit. Tätä kyselyä voidaan käyttää suodattimena nimikkeen, ostotilauksen tai muun hyödylliset tiedon etsimiseen. Sen avulla voidaan myös tunnistaa odotettu toimituspäivä nimikkeelle, joka voi olla yhdessä tai useammassa merikuljetuksessa. Näin se auttaa hallitsemaan odotettua varaston vastaanottoa.

Voit avata kyselyn kohdassa **Aiheutunut kustannus \> Kyselyt \> Merikuljetuksen rivit**.

### <a name="overview-tab"></a>Yleiskatsaus-välilehti

**Yleiskatsaus**-välilehti **Merikuljetuksen rivit** -kyselysivulla sisältää ruudukon, jossa on näkyvissä perustiedot kustakin asianmukaisesta merikuljetuksen rivistä. Ruudukon sarakkeet esitellään seuraavassa taulukossa.

| Pylväskaavio | kuvaus |
|---|---|
| **Nimiketunnus** | Merikuljetuksen rivin nimike. |
| **Viite** | Tilauksen tyyppi (ostotilaus tai siirtotilaus). |
| **Numero** | Ostotilauksen numero tai siirtotilauksen numero. |
| **Lasku** | Merikuljetuksen riviin liittyvän pakkauksen nimi. |
| **Lähetyskontti** | Merikuljetuksen riviin liittyvän kuljetuskontin nimi. |
| **Matka** | Merikuljetuksen riviin liittyvän merikuljetuksen nimi. |
| **Määrä** | Merikuljetuksen rivillä olevan nimikkeen määrä. |
| (Muut dimensiot) | Voit näyttää sarakkeita lisädimensioille tarpeen mukaan. Näitä dimensioita ovat esimerkiksi eränumero, varastotila ja varasto. Valitse toimintoruudussa **Varasto \> Näytä dimensiot** ja avaa valintaikkuna, jossa voit valita sisällytettävät dimensiot. |

### <a name="general-tab"></a>Yleinen-välilehti

Valitse **Yleinen**-välilehti, jos haluat lisätietoja **Yhteenveto**-välilehdessä valittuna olevalta riviltä.

### <a name="dimensions-tab"></a>Dimensiot-välilehti

Valitse **Dimensiot**-välilehti, jos haluat tarkastella **Yhteenveto**-välilehdessä valittuna olevan rivin kaikkien käytettävissä olevien dimensioiden arvoja riippumatta siitä, mitkä dimensiot olet valinnut näkymään tässä välilehdessä.

## <a name="cost-estimate-inquiries"></a>Kustannusarviokyselyt

Joka kerta, kun kustannusarvio luodaan, arvio lisätään **Kustannusarviot**-kyselysivulle. Yksityiskohtaisia tietoja kustannusarvioiden luomisesta, tarkastelemista ja suorittamisesta (mukaan lukien arvioit kyselysivulla) on kohdassa [Aiheutuneiden kustannusten arviointi ja hallinta](estimate-manage-landed-costs.md).

## <a name="item-tracking"></a>Nimikkeen seuranta

**Nimikkeen seuranta** -sivulla voit tarkastella avoimia ostotilausrivejä ja niiden nykyistä tilaa. Rivien ei täydy olla liitettynä merikuljetukseen, jotta ne näkyvät tässä. Jos nimike kuitenkin on liitetty merikuljetukseen, nimikkeen seurannan tietuerivi ilmaisee merikuljetuksen tunnuksen.

Voit avata tämän sivun valitsemalla **Aiheutunut kustannus \> Kyselyt \> Seuranta \> Nimikkeen seuranta**.

Koska järjestelmäsi sisältää todennäköisesti hyvin suuren määrän ostotilausrivejä, **Nimikkeen seuranta** -sivulla ei aluksi ole tietueita. Aloita käyttämällä sivun yläosan suodatuskenttiä, kun haluat määrittää etsimiesi ostotilausrivien joukon. Luo sitten luettelo valitsemalla toimintoruudusta **Päivitä**. Voit käyttää tähteä (\*) yleismerkkinä missä tahansa suodatinkentässä. Jos esimerkiksi haluat etsiä niiden nimikkeiden kaikki ostotilausrivit, joissa on sana "DVD", määritä **Tyyppi**-kentän arvoksi **Tuotenimi** ja kirjoita *\*DVD\** **Kentän arvo** -kenttään.

> [!NOTE]
> Tällä hetkellä jälkitoimitukset sisältävät vain myyntitilauksia. Myyntitarjouksia ei näytetä eikä niitä pidetä jälkitoimituksina.

Seuraavassa taulukossa kuvataan **Nimikkeen seuranta** -sivun ruudukon sarakkeet.

| Pylväskaavio | kuvaus |
|---|---|
| **Satamaan** | Lopullinen kohde. |
| **Vahvistettu** | Ostotilauksen rivin vahvistettu päivämäärä. |
| **Toimituspäivämäärä** | Ostotilauksen rivin toimituspäivämäärä. |
| **Matka** | Jos rivi liittyy merikuljetukseen, merikuljetuksen tunnus. |
| **Lähetyskontti** | Jos rivi on liitetty kuljetuskonttiin, kontin tunnus. |
| **Lähetyssatama** | Nykyinen satama, joka perustuu seurantalomakkeen ensimmäiseen etappiin, jossa ostotilausriviin liittyvälle kuljetuskontille ei ole määritetty todellista päivämäärää. |
| **Tehtävä** | Nykyinen tehtävä, joka perustuu seurantalomakkeen ensimmäiseen etappiin, jossa ostotilausriviin liittyvälle kuljetuskontille ei ole määritetty todellista päivämäärää. |
| **Arvoitu päättymispäivä** | Päivämäärä, jolloin kohdevarastoon odotetaan merikuljetuksen vastaanottoa. |
| **Nimi** | Toimittajan nimi. |
| **Merikuljetuksen tila** | Ostotilausriviin liitetty lähetyksen tila. |
| **Nimiketunnus** | Ostotilausrivin nimikenumero. |
| **Ulkoinen** | Toimittajan nimikkeen nimi. |
| **Tuotteen nimi** | Ostotilausrivin nimikkeen nimi. |
| **Määrä** | Ostotilausriviin liittyvä ostotilausrivin määrä. |
| **Yksikkö** | Ostotilausrivin mittayksikkö. |
| **Viite** | Tilauksen tyyppi (ostotilaus tai siirtotilaus) |
| **Viitenumero** | Ostotilauksen numero tai siirtotilauksen numero. |
| **Jälkitoimitus** | Symboli ilmaisee, että nimikkeellä on myynnin jälkitoimituksia. |
| (Muut dimensiot) | Voit näyttää sarakkeita lisädimensioille tarpeen mukaan. Näitä dimensioita ovat esimerkiksi eränumero, varastotila ja varasto. Valitse toimintoruudussa **Näytä dimensiot** ja avaa valintaikkuna, jossa voit valita sisällytettävät dimensiot. |

### <a name="related-information-about-backorders"></a>Jälkitoimitusten aiheeseen liittyviä tietoja

Jos haluat lisätietoja jälkitoimituksista, valitse **Aiheeseen liittyviä tietoja** -välilehti sivun oikeasta reunasta ja valitse sitten **Jälkitoimitukset**. Voit tarkastella tarkempia tietoja tietystä jälkitoimituksesta valitsemalla sen rivin ja valitsemalla sitten **Lisää**-linkin.

## <a name="individual-shipping-container-tracking"></a>Yksittäisen lähetyskontin seuranta

**Yksittäisen kuljetuskontin seuranta** -kysely tarjoaa suodattimen, jonka avulla voit etsiä kuljetuskontin ja määrittää sitten kaikki kontin merikuljetuksen rivit.

Voit avata tämän kyselyn valitsemalla **Aiheutunut kustannus \> Kyselyt \> Seuranta \> Yksittäisen kuljetuskontin seuranta**.

## <a name="multiple-shipping-container-tracking"></a>Usean lähetyskontin seuranta

**Usean kuljetuskontin seuranta** -kysely tarjoaa suodattimen, jonka avulla voit etsiä useita kuljetuskontteja ja määrittää sitten kaikki konttien merikuljetuksen rivit.

Voit avata tämän kyselyn valitsemalla **Aiheutunut kustannus \> Kyselyt \> Seuranta \> Usean kuljetuskontin seuranta**.
