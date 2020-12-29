---
title: Järjestelmäohjattu työjärjestys
description: Tässä ohjeaiheessa on tietoja järjestelmän ohjaamien töiden jaksotuksesta. Tämän toiminnon avulla voit lajitella ja suodattaa ne työtilaukset, jotka järjestelmä esittää käyttäjille suorittamista varten. Se on hyödyllinen tilanteissa, joissa fyysisen varastoinnin poimintaprosessin ajo edellyttää lisäehtoja.
author: Mirzaab
manager: tfehr
ms.date: 07/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFSystemDirectedWorkSequenceQuery, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-03
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 86d396b069a354b8fa7e15793372a8293273d238
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4427462"
---
# <a name="system-directed-work-sequencing"></a>Järjestelmäohjattu työjärjestys

[!include [banner](../includes/banner.md)]

Järjestelmäohjatun työjärjestyksen avulla voit lajitella ja suodattaa ne työtilaukset, jotka järjestelmä esittää käyttäjille suorittamista varten. Se on hyödyllinen tilanteissa, joissa fyysisen varastoinnin poimintaprosessi edellyttää lisäehtoja (kuten lähetysaikaa, poimintavyöhykettä, sijaintiprofiilia tai useiden ehtojen yhdistelmää).

Tämä toiminto laajentaa nykyisiä järjestelmän ohjaamien keräilyn toimintoja lisäämällä järjestelmään perustuvan kyselyjärjestyksen, jossa käyttäjät voivat määrittää sarjan ja vähintään yhden kyselyn, joka arvioi kaikki luodut työtilaukset. Vain ne työtilaukset, jotka täyttävät mobiililaitteen valikkovaihtoehdon määrityksessä määritetyt ehdot, tallennetaan ja esitetään.

Tämän vuoksi tämän toiminnon avulla voidaan edelleen optimoida varaston poimintaprosesseja, koska se tunnistaa määritettyjä ehtoja vastaavat työtilaukset, liittää ne oikeaan mobiililaitteen valikkokohteeseen ja näyttää ne sitten työntekijälle tietyn osaamisalueen, poimintalaitteiden tai muun tarpeen perusteella.

> [!NOTE]
> Jos tarvitaan eri ehtoja, on käytettävä useita mobiililaitteiden valikkokohteita.

## <a name="turn-on-the-organization-wide-system-directed-work-sequencing-feature"></a>Ota käyttöön organisaation laajuinen järjestelmäohjattu työjärjestysominaisuus

Ennen kuin voit käyttää järjestelmäohjattua työjärjestystoimintoa, sen pitää olla otettu käyttöön järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [Toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) työtilaa tarkistaakseen toiminnon tilan sekä laittaa sen päälle, jos sitä vaaditaan. Tässä tapauksessa toiminto näkyy seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Toiminnon nimi:** *Organisaation laajuinen järjestelmäsuunnattu työn sekvensointi*

## <a name="setup"></a>Määritys

### <a name="make-demo-data-available"></a>Demotietojen ottaminen käyttöön

Jos haluat käsitellä skenaariota käyttämällä tässä aiheessa esitettyjä arvoja, sinun on työskenneltävä järjestelmässä, johon on asennettu vakiodemotiedot. Sinun on myös valittava **USMF**-yritys. Skenaario käyttää varastoa *51* demotiedoista.

> [!IMPORTANT]
> Ennen kuin vapautat tilaukset varastoon, varmista, että poiminnan sijainneissa on tarpeeksi varastoa tilausten kaikille nimikkeille.
>
> Oletusarvoiset USMF-tiedot tukevat tätä skenaariota. Mikäli et käytä demodataa, tarkista **Toimipaikkadirektiivi**-asetus nähdäksesi mitä keräilysijainteja myyntitilausten keräilyyn käytetään. Jos sinun on muokattava varastoa, voit luoda manuaalisia siirtoja tai hyödyntää täydennystä tai mitä tahansa muuta virtausta.

### <a name="set-up-a-mobile-device-menu-item"></a>Määritä varaston mobiililaitteen valikkonimike

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Valitse mobiililaitteen valikkovaihtoehtojen luettelosta **Myyntikeräily – Järjestelmä**. Tarvittava valikkovaihtoehto on jo olemassa. 
1. Vahvista seuraavat asetukset:

    - **Yleinen**-pikavälilehdessä **Ohjaus**-kentän arvoksi tulee määrittää *Järjestelmäohjattu*.
    - **Työluokat**-pikavälilehdessä pitäisi näkyä seuraavat asetukset.

        | Työluokan tunnus | Työtilaustyyppi |
        |---|---|
        | Sales | Myyntitilaukset |
        | Myyntitilauksen keräily | Myyntitilaukset |

1. Valitse Toimintoruudussa **Järjestelmäohjattu työsarjakysely**.
1. Valitse **Muokkaa**.
1. Poista aiemmin luotu rivi ja vahvista toiminto valitsemalla **Kyllä**.
1. Valitse toimintoruudussa **Uusi** ja luo rivi.
1. Määritä uudelle riville seuraavat arvot:

    - **Järjestysnumero:** *1*
    - **Kuvauskenttä:** *Työn määrä alle 20 ja laskeva*

1. Valitse **Tallenna**.
1. Valitse toimintoruudussa **Muokkaa kyselyä**.
1. Laajenna **Liitokset**-välilehdessä liitoshierarkia näyttämään **Työrivit**-taulu.
1. Valitse **Työrivit**-taululiitos.
1. Valitse **Lisää taulun liitos**.
1. Etsi näyttöön tulevasta luettelosta rivi, jolla on seuraavat asetukset, ja valitse se:

    - **Liitostila:** *n:1*
    - **Suhde:** *Sijainnit (sijainti)*

1. Valitse **Valitse**.

    Sijainnit lisätään taululiitokseen.

1. Valitse **Lajittelu**-välilehdessä **Lisää**, jos haluat lisätä rivin.
1. Määritä uudelle riville seuraavat arvot:

    - **Taulu:** *Työrivit*
    - **Johdettu taulu:** *Työrivit*
    - **Kenttä:** *Työmäärä* (Valitse näkyviin tulevassa sanomaruudussa **Kyllä**, jos haluat lisätä lajittelun tähän kenttään.)
    - **Hakusuunta:** *Nouseva*

1. Valitse **Alue**-välilehti.

    Jos sekvensointi-kohtaan sisällytetään vain tietyt työehdot, voit määrittää ne **Alue**-välilehdessä. Tässä esimerkissä haluat sisällyttää vain työn, jonka määrä on pienempi kuin 20 kpl (alin mittayksikkö).

    Huomaa, että jotkin rivit ovat jo mukana. Näitä rivejä ei saa poistaa.

1. Lisää rivi valitsemalla **Lisää**.
1. Määritä uudelle riville seuraavat arvot:

    - **Taulu:** *Työrivit*
    - **Johdettu taulu:** *Työrivit*
    - **Kenttä:** *Varastotyön määrä*
    - **Kriteerit:** *\<20* (alle 20)

1. Lisää toinen rivi valitsemalla **Lisää**.
1. Määritä uudelle riville seuraavat arvot:

    - **Taulu:** *Työrivit*
    - **Johdettu taulu:** *Työrivit*
    - **Kenttä:** *Työtyyppi*
    - **Ehdot:** *Keräily*

1. Lisää toinen rivi valitsemalla **Lisää**.
1. Määritä uudelle riville seuraavat arvot:

    - **Taulu:** *Sijainnit*
    - **Johdettu taulu:** *Sijainnit*
    - **Kenttä:** *Sijaintiprofiilin tunnus*
    - **Ehdot:** *!VAIHE*

        > [!IMPORTANT]
        > Muista sisällyttää huutomerkki (*!*) *VAIHE*-ehdon eteen.

1. Valitse **OK** tallentaaksesi ja sulkeaksesi kyselyn.
1. Valitse **Tallenna**.
1. Palaa **Mobiililaitteen valikkokohteet** -sivulle sulkemalla sivu.

> [!NOTE]
> Tämä asetus määrittää kriteerit, joita käytetään tukikelpoisen työn syöttämisille mobiililaitteen valikkokohteeseen. Jos lisäät kyselyyn ehtoja, järjestelmä käyttää kyselyriviä, jonka järjestysnumero on pienin. Toisin sanoen kaikki sarjanumeron 1 tukikelpoiset työt esitetään käyttäjälle ensin ja kaikki järjestysnumeron 2 työt sen jälkeen. Näin ollen, jos tiettyä aluetta ja lajittelua on käytettävä yhdessä, ne on määritettävä samassa järjestelmäohjatussa työsarjakyselyssä.
>
> Tämä asetus poimii kaikki työt, joilla on vähintään yksi rivi, jonka määrä on pienempi kuin 20 kpl:tta. Jos työssä on rivi, jossa määrä on tasan 20 kpl:tta tai yli 20 kpl:tta, se on voimassa, jos sillä on myös vähintään yksi rivi, jossa määrä on pienempi kuin 20 kpl:tta.

### <a name="location-directives"></a>Sijaintidirektiivit

Jos käytät Contoso-oletustietoja, sijaintidirektiivitoiminnon kysely ei edellytä muutoksia. Voit kuitenkin varmistaa, että sijaintidirektiivit keräävät myyntitilausten nimikkeet, kun käytät ominaisuutta muussa kuin Contoso-ympäristössä, luomalla uuden sijaintidirektiivin. Voit tarkistaa asetukset demoympäristössä noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Varastonhallinta** \> **Asetukset** \> **Sijaintidirektiivit**.
1. Valitse **Työtilaustyyppi**-kentässä *Myyntitilaukset*.
1. Valitse sijaintidirektiivi, jonka nimi on *Poiminta 51*.
1. Valitse **Sijaintidirektiivin toiminnot** -pikavälilehdessä rivi **Poiminta**-toiminnolle.
1. Valitse ruudukon yläpuolelta **Muokkaa kyselyä**.
1. Tarkista **Alue**-kysely.

    1. Etsi rivi, jonka **Kenttä**-kentän arvoksi on määritetty *Sijainti*.
    2. Varmista, että **Ehto**-kenttä on tyhjä (rajoituksia ei ole).

## <a name="scenario"></a>Skenaario

### <a name="create-sales-order-picking-work"></a>Myyntitilauksen keräystyön luominen

Ennen järjestelmän ohjaamaa keräilyä on luotava jokin lähtevä työ. Tässä skenaariossa luodaan neljä myyntitilausta, jotka perustuvat määritettyihin järjestelmäohjattuihin työsarjakyselyihin.

Kullekin myyntitilaukselle varataan varastomäärät. Tästä syystä varattua varastoa ei voida käyttää varastosta muita tilauksia varten, jollei varausta tai osaa siitä peruta.

Tämän jälkeen kukin myyntitilaus vapautetaan varastoon, jotta lähtevä työ voidaan luoda.

#### <a name="sales-order-1"></a>Myyntitilaus 1

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Valitse toimintoruudussa **Uusi** ja luo myyntitilaus 1.
1. Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:

    - Aseta **Asiakas**-osassa **Asiakastili**-kentän arvoksi *US-004*.
    - Aseta **Yleinen**-osassa **Varasto**-kentässä arvoksi *51*.

1. Sulje valintaikkuna valitsemalla **OK**. Kirjoita myyntitilauksen numero muistiin.
1. Lisää rivi uuteen myyntitilaukseen ja määritä seuraavat arvot:

    - **Nimiketunnus:** *M9200*
    - **Määrä** *20*

1. Valitse ruudukon yläpuolella olevasta **Varasto**-valikosta kohta **Varaus**.
1. Valitse **Varaus**-sivulla **Varaa erä** voidaksesi tehdä varauksia varastosta.
1. Sulje **Varaus**-sivu.
1. Luo työ varastolle valitsemalla toimintoruudun **Varasto**-välilehdessä **Vapauta varastoon**.

    Näyttöön tulee tiedotteita, joissa kerrotaan, että tilaukselle on luotu aallon tunnus ja lähetystunnus.

#### <a name="sales-order-2"></a>Myyntitilaus 2

1. Valitse toimintoruudussa **Uusi** ja luo myyntitilaus 2.
1. Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:

    - **Asiakastili:** *US-007*
    - **Varasto**: *51*

1. Sulje valintaikkuna valitsemalla **OK**. Kirjoita myyntitilauksen numero muistiin.
1. Lisää rivi uuteen myyntitilaukseen ja määritä seuraavat arvot:

    - **Nimiketunnus:** *M9200*
    - **Määrä** *5*

1. Lisää toinen rivi valitsemalla **Lisää rivi** ja määritä seuraavat arvot:

    - **Nimiketunnus:** *M9201*
    - **Määrä** *1*

1. Molempien rivien varausvarasto.
1. Tilauksen vapauttaminen varastoon.

#### <a name="sales-order-3"></a>Myyntitilaus 3

1. Valitse toimintoruudussa **Uusi** ja luo myyntitilaus 3.
1. Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:

    - **Asiakastili:** *US-009*
    - **Varasto**: *51*

1. Sulje valintaikkuna valitsemalla **OK**. Kirjoita myyntitilauksen numero muistiin.
1. Lisää rivi uuteen myyntitilaukseen ja määritä seuraavat arvot:

    - **Nimiketunnus:** *M9200*
    - **Määrä** *7*

1. Lisää toinen rivi valitsemalla **Lisää rivi** ja määritä seuraavat arvot:

    - **Nimiketunnus:** *M9202*
    - **Määrä** *8*

1. Molempien rivien varausvarasto.
1. Tilauksen vapauttaminen varastoon.

#### <a name="sales-order-4"></a>Myyntitilaus 4

1. Valitse toimintoruudussa **Uusi** ja luo myyntitilaus 4.
1. Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:

    - **Asiakastili:** *US-010*
    - **Varasto**: *51*

1. Sulje valintaikkuna valitsemalla **OK**. Kirjoita myyntitilauksen numero muistiin.
1. Lisää rivi uuteen myyntitilaukseen ja määritä seuraavat arvot:

    - **Nimiketunnus:** *M9200*
    - **Määrä** *25*

1. Lisää toinen rivi valitsemalla **Lisää rivi** ja määritä seuraavat arvot:

    - **Nimiketunnus:** *M9202*
    - **Määrä** *10*

1. Molempien rivien varausvarasto.
1. Tilauksen vapauttaminen varastoon.

### <a name="get-work-ids-for-the-work-that-was-created"></a>Hanki luotujen töiden työtunnukset

1. Valitse **Varastonhallinta \> Työ \> Työn tiedot**.
1. Suodata **Varasto**-kenttä niin, että vain varasto *51* on näkyvissä.
1. Luotuja työtunnuksia on oltava neljä. Merkitse kunkin myyntitilauksen työtunnus muistiin.

    | Myyntitilauksen tunnus | Työ tunnus | Työn määrä |
    |---|---|---|
    | Myyntitilaus 1 | Työtunnus 1 | 20 kpl:tta |
    | Myyntitilaus 2 | Työtunnus 2 | 6 kpl:tta (molempien rivien summa) |
    | Myyntitilaus 3 | Työtunnus 3 | 15 kpl:tta (molempien rivien summa) |
    | Myyntitilaus 4 | Työtunnus 4 | 35 kpl:tta (molempien rivien summa) |

Ennen kuin suoritat työnkulun mobiililaitteessa, varmista, että vain luomasi työ on *Avoin*-tilassa varastossa *51* ja työtilaustyyppi on *Myyntitilaus*. Muussa tapauksessa testin tulokset voivat vaihdella, koska järjestelmän suora poiminta sisältää kaikki tukikelpoiset työt.

1. Siirry kohtaan **Varaston hallinta \> Työ \> Lähtevä \> Avoin myyntityö**.
1. Suodata **Avoin myyntityö** -ruudukossa **Varasto**-kenttä niin, että vain varasto *51* on näkyvissä.
1. Vahvista, että vain aiemmin luomasi neljä työtunnusta näytetään.
1. Sulje **Työ**-sivu.

### <a name="mobile-device-flow-execution"></a>Mobiililaitteen työnkulun suoritus

Järjestelmä syöttää asetusten perusteella käyttäjän työt, jotka lajitellaan suurimmasta työrivin määrästä pienimpään. Jokaisella rivillä oleva määrä on pienempi kuin 20 kpl:tta.

Muista, että tämä asetus poimii kaikki työt, joilla on vähintään yksi rivi, jonka määrä on pienempi kuin 20 kpl:tta. Jos työllä on toinen rivi, jossa määrä on tasan 20 kpl:tta tai yli 20 kpl:tta, se on myös voimassa.

#### <a name="mobile-app"></a>Mobiilisovellus

1. Kirjaudu varastosovellukseen käyttäjänä varastossa *51*.
1. Siirry kohtaan **Lähtevä \> Myynnin keräys - Järjestelmä**.

    Poimintavaihe työtunnukselle *4* on esitetty. Tämä työtunnus esitetään ensimmäisenä, koska järjestelmän ohjaama kyselyjärjestys on määritetty ja määrität, että työ on jaksotettava laskeutuvan työrivin määrän perusteella.

1. Täytä vaadittu poiminta ja aseta työtunnus suljettaessa.

    Seuraavaksi esitetään työtunnus *3*. Yksi sen työriveistä on seuraava järjestyksessä työrivin määrän perusteella.

1. Täytä poiminta ja aseta työtunnus suljettaessa.

    Seuraavaksi esitetään työtunnus *2*. Tämän työn poimintarivi on seuraava järjestyksessä.

1. Täytä poiminta ja aseta työtunnus suljettaessa.

    Lisätyötä ei tule esittää teille. Työtunnus *1* ei ole oikeutettu tähän mobiililaitteen valikkokohteeseen, koska kysely määrittää, että työotsikot otetaan huomioon vain, jos työrivien määrä on alle 20 kpl:tta.

## <a name="tips"></a>Vihjeitä

Järjestelmän ohjaamat työsarjakyselyt ovat *sisältyviä*. On tärkeää, että muistat tämän seikan joissakin asennuksissa. Haluat esimerkiksi, että tietty valikkovaihtoehto käsittelee vain työtä, jossa työyksikkö on *kpl*, ja määrität rajoituksen kyselyn **Alue**-välilehdessä. Tässä tapauksessa kaikki työt, joissa vähintään yhden työrivin työyksiköksi on määritetty *kpl* syötetään työntekijälle. Tämän vuoksi työhön voi kuulua myös työ, jossa työriveillä on jokin muu työyksikkö kuin *kpl* (esimerkiksi *laatikko* tai *kuormalava*). Kysely jättää pois vain sellaiset työt, joissa työyksiköksi ei ole määritetty *kpl*.

Tämän skenaarion esimerkissä myös kysely kaappasi työtunnuksen *4*. Kun se luotiin, lisättiin kaksi riviä: yksi 25 kpl:tta ja toinen 10 kpl:tta varten. Työ on vielä esitetty käyttäjälle, koska vähintään yhden työrivin määrä on pienempi kuin 20 kpl:tta.

Skenaarion mukaan voit estää tämän ongelman käyttämällä työtaukoja.
