---
title: Varastotapahtumien arkistointi
description: Tässä aiheessa kuvataan, miten voit arkistoida varastotapahtumien tietoja järjestelmän suorituskyvyn parantamiseksi.
author: sherry-zheng
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 8b61e65d3a641a1e3d73192853c832d57ed17401
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021267"
---
# <a name="archive-inventory-transactions"></a>Varastotapahtumien arkistointi

[!include [banner](../../includes/banner.md)]

Ajan mittaan varastotapahtumien taulukko (`InventTrans`) kasvaa ja kuluttaa enemmän tietokannan tilaa. Tästä syystä taulukolle tehdyt kyselyt hidastuvat ajan myötä. Tässä aiheessa kuvataan, kuinka voit käyttää *Varastotapahtumien arkisto* -ominaisuutta varastotapahtumien tietojen arkistoimiseksi ja järjestelmän suorituskyvyn parantamiseksi.

> [!NOTE]
> Vain kirjanpidollisesti päivityt varastotapahtumat voidaan arkistoida valitulta suljetulta kirjanpitokaudelta. Jotta kirjanpidollisesti päivitetyt lähtevät varastotapahtumat voidaan arkistoida, niiden varasto-oton tilan täytyy olla *Myyty*, ja saapuvien maksutapahtumien vastaanoton tilan täytyy olla *Ostettu*.

Kun arkistoit varastotapahtumia, kaikki niihin liittyvät tapahtumat siirretään `InventTransArchive`-taulukkoon. Varasto-ottotapahtumat ja varaston vastaanottotapahtumat arkistoidaan erikseen nimikkeen tunnuksen (`itemId`) ja varastodimension tunnuksen (`inventDimId`) yhdistelmän perusteella, ja ne asetetaan varasto-ottotapahtumien ja vastaanottotapahtumien yhteenvetoihin.

Jos `itemId`- ja `inventDimId`-yhdistelmä sisältää vain yhden vastaanotto- tai varasto-ottotapahtuman, tapahtumaa ei arkistoida.

## <a name="turn-on-the-feature-in-your-system"></a>Toiminnon ottaminen käyttöön järjestelmässä

Jos järjestelmäsi ei vielä sisällä tässä aiheessa kuvattuja ominaisuuksia, avaa [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja ota *Varastotapahtumien arkisto* -ominaisuus käyttöön. Huomaa, että tätä toimintoa ei voi poistaa käytöstä, kun se on otettu käyttöön.

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a>Ennen varastotapahtumien arkistointia huomioitavat asiat

Huomioi seuraavat liiketoimintaskenaariot ennen varastotapahtumien arkistoimista, koska arkistointi vaikuttaa niihin:

- Kun tarkastat varastotapahtumia niihin liittyvistä asiakirjoista, kuten ostotilausriveiltä, ne näkyvät arkistoituina. Jos haluat tarkastaa arkistoidut tapahtumat, sinun täytyy valita **Varastonhallinta \> Kausittaiset tehtävät \> Puhdista \> Varastotapahtumien arkisto**.
- Varaston sulkemista ei voi peruuttaa arkistoiduilta kausilta. Ennen kuin voit peruuttaa varaston sulkemisen, sinun täytyy peruuttaa varastotapahtumien arkistointi asiaankuuluvalta kaudelta.
- Standardikustannusten muunnosta ei voi suorittaa arkistoiduille kausille. Ennen kuin voit suorittaa standardikustannusten muunnoksen, sinun täytyy peruuttaa varastotapahtumien arkistointi asiaankuuluvalta kaudelta.
- Varastotapahtumien arkistointi vaikuttaa varastotapahtumista saatuihin varastoraportteihin. Nämä raportit sisältävät varaston erääntymisraportin ja varaston arvon raportit.
- Arkistointi saattaa vaikuttaa varastoennusteisiin, jos ne suoritetaan arkistoitujen kausien aikahorisontin aikana.

## <a name="prerequisites"></a>Edellytykset

Varastotapahtumia voidaan arkistoida vain kausina, jotka täyttävät seuraavat ehdot:

- Kirjanpitokauden on oltava suljettu.
- Varaston sulkeminen on suoritettava arkiston päättymispäivänä tai sen jälkeen.
- Kauden on oltava vähintään vuosi ennen arkiston alkamispäivää.
- Varaston uudelleenlaskentoja ei sallita.

## <a name="archive-inventory-transactions"></a>Varastotapahtumien arkistointi

Arkistoi varastotapahtumia noudattamalla seuraavia ohjeita.

1. Avaa **Varastonhallinta** \> **Kausittaiset tehtävät** \> **Puhdista** \> **Varastotapahtumien arkisto**.

    **Varastotapahtumien arkisto** -sivu avautuu ja näyttää arkistoitujen prosessitietueiden luettelon.

    ![Varastotapahtumien arkisto -sivu](media/archive-inventory-empty.png "Varastotapahtumien arkisto -sivu")

1. Valitse toimintoruudusta **Varastotapahtumien arkisto** luodaksesi varastotapahtumien arkiston.
1. Määritä **Varastotapahtumien arkisto** -valintaikkunan **Parametrit**-pikavälilehdessä seuraavat kentät:

    - **Suljetun kirjanpitokauden alkamispäivä** – Valitse aikaisin tapahtumapäivä, joka sisällytetään arkistoon.
    - **Suljetun kirjanpitokauden päättymispäivä** – Valitse myöhäisin tapahtumapäivä, joka sisällytetään arkistoon.

    ![Varastotapahtumien arkisto -valintaikkuna](media/archive-inventory-dates.png "Varastotapahtumien arkisto -valintaikkuna")

    > [!NOTE]
    > Voit valita vain kausia, jotka täyttävät [edellytykset](#prerequisites).

1. Määritä eräkäsittelyn tiedot tarpeen mukaan **Suorita taustalla** -pikavälilehdestä. Noudata erätöiden tavallisia ohjeita Microsoft Dynamics 365 Supply Chain Managementissa.
1. Valitse **OK**.
1. Näet viestin, joka pyytää sinua vahvistamaan, että haluat jatkaa. Lue viesti huolellisesti ja valitse **Kyllä**, jos haluat jatkaa.

    Näet viestin, jonka mukaan varastotapahtumien arkistointityösi on lisätty eräjonoon. Työ aloittaa nyt varastotapahtumien arkistoinnin valitulta kaudelta.

## <a name="view-archived-inventory-transactions"></a>Näytä arkistoidut varastotapahtumat

**Varastotapahtumien arkisto** -sivu näyttää koko arkistointihistoriasi. Ruudukon jokaisella rivillä näytetään tietoja, kuten arkiston luontipäivä, arkiston luonut käyttäjä ja arkiston tila.

![Arkistointihistoria Varastotapahtumien arkisto -sivulla](media/archive-inventory-full.png "Arkistointihistoria Varastotapahtumien arkisto -sivulla")

Valitse sivun ylälaidan avattavasta luettelosta jokin seuraavista arvoista suodattaaksesi ruudukossa näytettäviä arkistoja:

- **Aktiiviset** – Näytä vain aktiiviset arkistot, älä peruutettuja arkistoja.
- **Kaikki** – Näytä kaikki arkistot, sekä aktiiviset että peruutetut.

Jokainen ruudukossa näytetty artikkeli sisältää seuraavat tiedot:

- **Aktiivinen** – Valintamerkki osoittaa, että arkisto on aktiivinen.
- **Päivämäärästä** – Vanhimman arkistoon sisällytettävissä olevan tapahtuman päivämäärä.
- **Päivämäärään** – Uusimman arkistoon sisällytettävissä olevan tapahtuman päivämäärä.
- **Ajoittaja** – Arkiston luonut käyttäjätili.
- **Suoritettu** – Arkiston luontipäivä.
- **Peruuta** – Valintamerkki osoittaa, että arkisto on peruutettu.
- **Pysäytä tämänhetkinen päivitys** – Valintamerkki osoittaa, että arkisto on käynnissä, mutta se on keskeytetty.
- **Tila** – Arkiston käsittelytila. Mahdolliset arvot ovat *Odottaa*, *Käynnissä* ja *Valmis*.

Ruudukon yllä oleva työkalurivi sisältää seuraavat painikkeet, joita voit käyttää valitun arkiston työstämiseen:

- **Arkistoidut tapahtumat** – Katso valitun arkiston kaikki tiedot. **Arkistoidut tapahtumat** -sivu näyttää arkiston kaikki tapahtumat.

    ![Arkistoidut tapahtumat -sivu](media/archive-inventory-transactions.png "Arkistoidut tapahtumat -sivu")

    Jos haluat lisätietoja tietystä **Arkistoidut tapahtumat** -sivulla olevasta tapahtumasta, valitse se ruudukosta ja valitse sitten toimintoruudusta **Arkistoidun tapahtuman tiedot**. **Arkistoidun tapahtumat tiedot** -sivulla näytetään esimerkiksi kirjanpidon kirjaus, asiaan liittyvät alareskontran viitteet ja taloushallinnon dimensiot.

- **Keskeytä arkistointi** – Keskeytä valittu arkisto, jota käsitellään tällä hetkellä. Keskeytys astuu voimaan vasta, kun arkistointitehtävä on luotu. Tästä syystä ennen keskeytyksen alkamista voi olla lyhyt viive. Jos arkisto on keskeytetty, sen **Pysäytä tämänhetkinen päivitys** -kenttään ilmestyy valintamerkki.
- **Jatka arkistointia** – Jatka valitun keskeytetyn arkiston käsittelyä.
- **Peruuta** – Peruuta valittu arkisto. Voit peruuttaa arkiston vain, jos sen **Tila**-kentän arvo on *Valmis*. Jos arkisto on peruutettu, sen **Peruuta**-kenttään ilmestyy valintamerkki.
