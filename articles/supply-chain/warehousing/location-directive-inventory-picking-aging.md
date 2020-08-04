---
title: Sijaintidirektiivin varastonkeräilyn erääntyminen
description: Tässä ohjeaiheessa käsitellään FIFO- ja LIFO-sijaintidirektiivistrategioita keräilyn aikana.
author: mirzaab
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 56a3a838374bb1cd0f4b839124ada7114205c1e7
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597285"
---
# <a name="location-directive-inventory-picking-aging"></a>Sijaintidirektiivin varastonkeräilyn erääntyminen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään FIFO- ja LIFO-sijaintidirektiivistrategioita keräilyn aikana. Näitä strategioita käytetään yhdessä sijainnille kirjattujen erääntymispäivämäärien kanssa ja niiden avulla seurataan, milloin varasto saapui varastoon ensimmäisen kerran. *Sijaintidirektiivin varastonkeräilyn erääntyminen* -toiminto määrittää erääntymisen sijainnin päivämäärän perusteella. *Varastosijainnin tila* -toiminto päivittää sijainnin päivämäärän rekisterikilven päivämäärän perusteella.

FIFO- ja LIFO-strategioita voi käyttää sekä eräseurattujen nimikkeiden että ei-eräseurattujen nimikkeiden lähettämiseen sen päivämäärän perusteella, jolloin varastoa saapui fyysiseen varastoon. Tätä ominaisuus voi kätevä etenkin ei-eräseuratun varaston osalta, jos vanhentumispäivä ei ole käytettävissä lajittelun varten.

Kun varasto vastaanotetaan tai luodaan ensimmäisen kerran fyysisessä varastossa, järjestelmä päivittää liittyvän rekisterikilven siten, että kuluva päivä näkyy erääntymispäivämääränä. Sijaintidirektiivistrategiat tunnistavat sitten tämän päivämäärän perusteella fyysisen varaston vanhimman tai uusimman varaston. Jos varasto siirretään sijaintiin, jota ei seurata rekisterikilven avulla, itse sijainti päivitetään erääntymistiedoilla ja strategiat käyttävät sitten näitä tietoja.

## <a name="turn-on-the-feature"></a>Toiminnon ottaminen käyttöön

Voit käyttää tätä toimintoa ottamalla seuraavat toiminnot käyttöön [ominaisuuksien hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) seuraavassa järjestyksessä:

1. Varastosijainnin tila
1. Sijaintidirektiivin varastonkeräilyn erääntyminen

## <a name="feature-requirements"></a>Toiminnon vaatimukset

Tämän toiminnon käyttö edellyttää, että **Ota sijainnin tila käyttöön** -asetukseksi on valittu *Kyllä* jokaisessa [sijaintiprofiilissa](tasks/create-location-profile.md), jota käytetään myymälän varastona. Tämä asetus määritetään sijaintiprofiilissa valitsemalla ensin **Varastonhallinta \> Asetukset \> Varasto \> Sijaintiprofiilit** ja sitten sijaintiprofiili. Tämä asetus sijaitsee **Yleiset**-pikavälilehdessä.

## <a name="feature-scenarios"></a>Toiminnon skenaariot

Tässä osan esimerkit osoittavat, miten FIFO-ja LIFO-strategioita määritetään ja käytetään.

> [!TIP]
> Tässä on kaksi skenaariota: yksi FIFO- ja yksi LIFO-skenaario. Käytetyissä menettelyissä oletetaan, että kumpikin skenaario tehdään annetussa järjestyksessä. Kumpikin skenaario kannattaa tehdä, sillä silloin kahden strategian väliset erot nousevat esille.

### <a name="make-sample-data-available"></a>Ota mallitiedot käyttöön

Näiden skenaarioiden käyttäminen tässä määritettyjen mallitietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon vakio-[demotiedot](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) on asennettu. Sinun on myös valittava **USMF**-yritys ennen kuin aloitat.

Voit käyttää näitä skenaarioita ohjeena toiminnon käytöstä tuotantojärjestelmässä. Siinä tapauksessa tässä kuvatut arvot on kuitenkin korvattava omilla arvoilla.

### <a name="set-up-the-scenarios"></a><a name="demo-set-up"></a>Skenaarioiden määrittäminen

Esittelytiedot on määritettävä ja varastoissa on tehtävä oikaisuja skenaarioita varten. Luo FIFO- ja LIFO-skenaarioissa tarvittavat varastotiedot seuraavasti:

1. Kirjaudu järjestelmään, johon esittelytiedot on asennettu ja valitse **USMF**-yritys.
1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varasto \> Sijaintiprofiilit**.
1. Valitse toimintoruudussa **Muokkaa**.
1. Valitse sijaintiprofiililuettelossa **KERROS-05**.
1. Määritä **Yleinen**-pikavälilehdessä **Ota sijainnin tila käyttöön**-asetukseksi *Kyllä*.
1. Valitse **Tallenna**.
1. Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.
1. Valitse sijaintidirektiivien luettelossa **63 Keräilyn konttiinpakkaus**.
1. Valitse **Muokkaa**, jotta saat sivun muokkaustilaan.
1. Etsi **Sijaintidirektiivitoiminnot**-välilehdessä rivi, jonka **Järjestysnumero**-kentän arvo on *1*, ja toimi seuraavasti:

    - Jos määritettävänä on FIFO-skenaario, mutta **Strategia**-kentän arvoksi *Sijainnin erääntyminen FIFO*.
    - Jos määritettävänä on LIFO-skenaario, mutta **Strategia**-kentän arvoksi *Sijainnin erääntyminen LIFO*.

1. Valitse **Sijaintidirektiivitoiminnot**-pikavälilehdessä **Muokkaa kyselyä**.
1. Lisää rivi valitsemalla kyselyn valintaruudun **Alue**-välilehdessä **Lisää** ja määritä sitten seuraavat arvot:

    - **Taulu:** *Sijainnit*
    - **Johdettu taulu:** *Sijainnit*
    - **Kenttä:** *Alueen tunnus*
    - **Kriteerit:** *Kerros*

1. Ota asetukset käyttöön valitsemalla **OK** ja sulje kyselyn valintaikkuna.
1. Tallenna sijaintidirektiivin muutokset valitsemalla **Tallenna**.
1. Poista skenaariota varten aiemmin luoto varasto varastosijainnista toimimalla seuraavasti mobiililaitteessa tai tietokoneen *Dynamics 365 for Finance and Operations – Warehousing* -sovelluksessa:

    1. Kirjaudu varastoon *63* soveltuvalla käyttäjätunnuksella ja salasanalla.
    1. Valitse päävalikossa **Laatu**.
    1. Valitse **Laadunhallinta**-valikossa **Hävikki**.
    1. Valitse **Hävikki**-sivulla **Sijainti/rekisterikilpi**-kenttä ja anna *63\_1*.
    1. Paina **Enter**-näppäintä tai valitse **OK**.
    1. Vahvista **Hävikki**-tiedot **Oikaisu ulos** painamalla **Enter**-näppäintä tai valitsemalla **OK**.

    Kun rekisterikilven varaston oikaistu ulos, Työ on valmistunut -sanoma tulee näkyviin.

    Esittelytiedoissa on nyt varastoa on kahdessa sijainnissa. Kummallakin sijainnilla on oma erääntymispäivä. Sijainnin *KR-001* erääntymispäivä on 15. huhtikuuta 2017 ja sijainnin *KR-002* 29. tammikuuta 2017. Molemmissa sijainneissa on nimike *A0001*.

    Voit tarkastella näitä tietoja valitsemalla **Inventoinnin- ja varastonhallinta \> Kyselyt ja raportit \> Varastoluettelo** ja tekemällä sitten suodatuksen varaston *63* ja nimikkeen *A0001* perusteella. Valitse riveillä, joiden **Sijainti**-kenttä on *KR-001* tai *KR-002*, rivi, jolla on positiivinen **Fyysinen varasto** -arvo, ja valitse sitten toimintoruudussa **Tapahtumat**. **Fyysinen pvm** -kentässä on päivämäärä, joka vastaa jotakin aiemmin mainittua erääntymispäivää.

### <a name="scenario-1-set-up-and-use-fifo-location-aging"></a><a name="fifo-demo"></a>Skenaario 1: Sijainnin FIFO-erääntymisen määrittäminen ja käyttäminen

FIFO-strategia etsii vanhimman erääntymispäivämäärän sisältävän sijainnin ja kohdistaa keräilyn kyseisen päivämäärän perusteella.

1. Jos sitä ei ole vielä tehty, [valmistele tässä skenaariossa tarvittavat näytetiedot](#demo-set-up).
1. Valitse **Myynti ja markkinointi \> Myyntitilaus \> Kaikki myyntitilaukset**.
1. Valitse **Uusi**.
1. Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:

    - Aseta **Asiakas**-pikavälilehdessä **Asiakastili**-kentän arvoksi *US-001*.
    - Aseta **Yleinen**-pikavälilehden **Varasto**-kentässä arvoksi *63*.

1. Valitse **OK** luodaksesi ostotilauksen ja sulje valintaikkuna.
1. Uusi myyntitilaus avataan. **Myyntitilausrivit**-pikavälilehden ruudukossa pitäisi olla uusi tyhjä rivi. Määritä tämän tilausrivin **Nimiketunnus**-kentän arvoksi *A0001* ja **Määrä**-kentän arvoksi *1*.
1. Valitse ruudukon yläpuolella olevasta **Varasto**-valikosta kohta **Varaus**.
1. Varaa valitun varaston varastosta tilattu määrä nimikettä valitsemalla **Varaus**-sivulla **Varaa erä**.
1. Sulje **Varaus**-sivu.
1. Valitse **Myyntitilaus**-sivun toimintoruudun **Varasto**-välilehden **Toiminnot**-ryhmässä **Vapauta varastoon**. Näyttöön avautuu tietosanomia. Järjestelmä luo lähetyksen, lisää sen uuteen kuormitukseen ja luo tarvittavat työt.
1. Avaa tälle myyntitilaukselle luotu työ valitsemalla **Myyntitilausrivit**-pikavälilehden **Varasto**-valikossa **Työn tiedot**. Huomaa, että rivillä, jonka **Työtyyppi**-arvo on *Keräily*, **Sijainti**-arvo on *KR-002*. Tässä sijainnissa on rekisterikilpi, jossa on vanhin erääntymispäivä (FIFO).
1. Valitse **Varasto \> Lähetyksen tiedot**.
1. ***Yleiset**-pikavälilehdessä on aallon tunnus. Kirjoita se muistiin, jotta voit käyttää sitä skenaariossa 2.

### <a name="scenario-2-set-up-and-use-lifo-location-aging"></a>Skenaario 2: Sijainnin LIFO-erääntymisen määrittäminen ja käyttäminen

LIFO-strategia etsii uusimman erääntymispäivämäärän sisältävän sijainnin ja kohdistaa keräilyn kyseisen päivämäärän perusteella. Skenaariossa 2 muokataan skenaarion 1 (FIFO) asetuksia sekä käytetään skenaariossa luotua myyntilausta ja aaltoa.

1. Määritä ja suorita ennen tämän skenaarion aloittamista koko FIFO-skenaario [edellisessä osassa](#fifo-demo) kuvatulla tavalla. Tässä skenaariossa käytetään kyseiseen skenaarioon luotua aaltoa ja suurinta osaa sen asetuksista.
1. Muokkaa **63 Keräilyn konttiinpakkaus** -sijaintidirektiivi käyttämään *Sijainnin erääntyminen LIFO* -strategiaa [Skenaarioiden määrittäminen](#demo-set-up) -menettelyn ensimmäisessä osassa kuvatulla tavalla.

    Seuraavaksi muokataan skenaariossa 1 myyntitilaukseen luotu aalto käyttämään *Sijainnin erääntyminen LIFO* -strategiaa.

1. Valitse **Varastonhallinta \> Lähtevät aallot \> Lähetysaallot \> Kaikki aallot**.
1. Valitse ja avaa FIFO-skenaarioon luodun tilauksen sisältävä aalto.
1. peruuta FIFO-skenaariota varten työ valitsemalla toimintoruudun **Työ**-välilehdessä **Peruuta**.
1. Valitse toimintoruudun **Aalto**-välilehden **Aalto**-ryhmässä **Käsittele**.
1. Kun käsittely on valmis, avaa tähän aaltoon luotu työ valitsemalla toimintoruudun **Aalto**-välilehden **Liittyvät tiedot** -ryhmässä **Työ**.
1. **Työ**-sivun **Yleiskatsaus**-välilehdessä pitäisi olla kaksi riviä. Valitse rivi, jonka **Työn tila**-kentän arvoksi on määritetty *Avoin*.
1. Huomaa, että rivillä, jonka **Työtyyppi**-arvo on *Keräily*, **Sijainti**-arvo on *KR-001*. Tässä sijainnissa on rekisterikilpi, jossa on uusin erääntymispäivä (LIFO).

Näissä skenaarioissa on näytetty, miten sijainnin erääntymisstrategia ohjaa työn varastosijaintiin, jossa on joko vanhin tai uusin varasto valitun strategian mukaan.
