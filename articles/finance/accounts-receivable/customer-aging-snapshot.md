---
title: Asiakkaan erääntymistilannevedokset
description: Tässä ohjeaiheessa on tietoja asiakkaan erääntymistilannevedoksista. Erääntymistilannevedos laskee asiakasryhmän erääntyneet saldot kyseisenä ajankohtana.
author: JodiChristiansen
ms.date: 05/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a768b2508988c77d669bac2ac443d69a995a5617971693caed8e0563a146f853
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769104"
---
# <a name="customer-aging-snapshots"></a>Asiakkaan erääntymistilannevedokset

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja asiakkaan erääntymistilannevedoksista. Erääntymistilannevedos laskee asiakasryhmän erääntyneet saldot kyseisenä ajankohtana. Voit luoda erääntymistilannevedostietueita joko kaikkia asiakkaita tai asiakaspoolin asiakkaita varten.

Erääntymistilannevedostiedot näytetään **Erääntyneet saldot** -luettelosivulla ja **Perintä**-sivulla. Erääntymistilannevedos on luotava, ennen kuin **Erääntyneet saldot** -luettelosivua voi käyttää. Luettelosivulla näkyvät vain ne asiakkaat, joita varten on luotu erääntymistilannevedos.

**Asiakkaan luotonvalvonta** -työtilassa näkyvät myös asiakkaan erääntymistiedot. Lisätietoja on kohdassa [Luotonvalvonnan hallinnan Power BI -sisältö](credit-collections-power-bi.md).

> [!NOTE]
> Voit lyhentää erääntymistilannevedoksen luomiseen tarvittavaa aikaa ottamalla käyttöön **Asiakkaan erääntymisen suorituskyvyn parannus** -ominaisuuden **Ominaisuuksien hallinta** -työtilassa. Älä kuitenkaan käytä asiakaspooleja, kun tämä ominaisuus on käytössä. Jos asiakaspooli on valittuna, toiminto ei toimi, mutta voit silti luoda erääntymistilannevedoksen.

Kun luot asiakkaan erääntymistilannevedoksen, voit kirjoittaa sen tiedot seuraaviin kenttiin:

- **Erääntymiskauden määritys** – Valitse erääntymiskauden määritys erääntymistilannevedokselle. Kullakin erääntymiskauden määrityksellä voi olla yksi erääntymistilannevedos. Erääntymistilannevedoksen ja erääntymiskauden määritys on luotava erikseen.
- **Ryhmän tunniste** – Tämä kenttä ei ole pakollinen. Poolin avulla voit määrittää asiakasjoukon, joka tulisi käsitellä erääntymistilannevedoksessa. Jos valitset asiakaspoolin tässä kentässä, erääntymistilannevedos luodaan vain niissä asiakastileissä, jotka ovat osa asiakaspoolia. Valitun asiakaspoolin tyypin on oltava **Erääntymistilannevedos**. Jos jätät tämän kentän tyhjäksi, kaikille asiakastileille luodaan erääntymistilannevedos.

    > [!NOTE]
    > Jos **Asiakkaan erääntymisen suorituskyvyn parannus** -ominaisuus on käytössä, älä valitse asiakaspoolia.

- **Ehdot** – Erääntymistilannevedos erääntyy valitun päivämäärän perusteella:

    - **Tapahtumapäivä** – Kukin tapahtuma erääntyy tapahtuman päivämäärän perusteella.
    - **Eräpäivä** – Kukin tapahtuma erääntyy eräpäivän perusteella.
    - **Asiakirjan päivämäärä** – Kukin tapahtuma erääntyy asiakirjan päivämäärän perusteella.

- **Erääntyy** – Valitse päivämäärä, jota käytetään erääntymistilannevedoksen **Kuluva päivämäärä** -kentässä. Erääntymiskaudet lasketaan sitten tämän päivämäärän perusteella. 

    - **Tämän päivän päivämäärä** – Käytä järjestelmän päivämäärää. Valitse tämä vaihtoehto, jos käsittely on määritetty tapahtumaan toistuvana eränä. Tämän jälkeen käytetään aina kyseisen suorituksen järjestelmän päivämäärää, kun erä suoritetaan.
    - **Valittu päivämäärä** – Käytä määrittämääsi päivämäärää. Jos valitset tämän vaihtoehdon, määritä myös erääntymispäivämäärä.

    Nykyinen erääntymiskausi on esimerkiksi 30 päivää. Jos valitset tämän kentän arvoksi **Tämän päivän päivämäärä**, nykyinen erääntymisjakso alkaa kuluvasta päivämäärästä ja sisältää sen jälkeen edelliset 29 päivää. Jos valitset **Valittu päivämäärä** ja syötät päivämäärän, nykyinen erääntymisjakso alkaa määritetystä päivämäärästä ja sisältää sen jälkeen edelliset 29 päivää.

- **Määritä perintätila** – Määritä tämän asetuksen arvoksi **Kyllä**, jos haluat päivittää tapahtumien perintätilan **Perinnät**-sivulla tilasta **Maksulupaus** tilaan **Maksulupaus rikottu**, jos erääntymispäivä ylittää **Maksulupauksen päivämäärä** -kentän arvon. Valitse vaihtoehdoksi **Ei**, jos haluat jättää kokoelman tilan ennalleen **Kokoelmat**-sivulla.
- **Sisällytä asiakkaat, joiden saldo on nolla** – Määritä tämän asetuksen arvoksi **Kyllä**, jos haluat sisällyttää kaikki asiakkaat asiakkaiden saldosta riippumatta. Jos sisällytät kaikki asiakkaat, suosittelemme, että otat **Asiakkaan erääntymisen suorituskyvyn parannus** -ominaisuuden käyttöön ja et käytä asiakaspooleja. Valitse vaihtoehdoksi **Ei**, jos haluat sisällyttää vain asiakkaat, joilla on saldo. Tämä asetus nopeuttaa suorituskykyä, koska asiakkaat, joilla ei ole saldoa, ohitetaan.
- **Yritysalue** – Valitse **Yritysalue**-välilehdestä erääntymistilannevedokseen sisällytettävät yritykset. Vain yritykset, jotka on määritetty keskitettyihin maksuihin, ovat valittavissa. Valittujen yrityksen tapahtumat sisällytetään niiden asiakkaiden erääntymiskausiin, joilla on sama osapuolen tunnus kaikissa näissä yrityksissä. Valuuttasummat muunnetaan sen yrityksen kirjanpitovaluuttaan, johon olet kirjautunut, kun luot erääntymistilannevedoksen.

On suositeltavaa ajoittaa tämä prosessi suoritettavaksi eräkäsittelyssä.

> [!NOTE]
> Voit parantaa erän suorituskykyä erääntymistilannevedoksia luotaessa kirjoittamalla numeron **Erätehtävien enimmäismäärä** -kenttään **Perinnän oletukset** -pikavälilehdelle **Kokoelmat**-välilehdellä **Myyntireskontran parametrit** -sivulla. **Eräännytä asiakkaan saldot** -kentässä on suositeltavaa aloittaa oletusarvolla **100** ja säätää sitten arvoa tilanteen käsittelyn optimoimiseksi.

