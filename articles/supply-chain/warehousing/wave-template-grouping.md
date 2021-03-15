---
title: Aallon mallipohjan ryhmittely
description: Aaltomalliryhmityksen avulla järjestelmä voi käyttää aaltomalliasetelmia määrittämään, perustuen määrittämiisi kriteereihin miten se pitäisi jakaa vapautetut rivit ja liittää ne uusiin tai olemassa oleviin aaltoihin. Tämä ominaisuus voi olla hyödyllinen varastoissa, joissa aallot luodaan tiettyjen kriteerien perusteella, mutta jossa esimiehet luovat mieluummin aallot automaattisesti manuaalisen sijaan.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b422eb432e579d4ae914fbc0efa79aaa15f1de27
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998375"
---
# <a name="wave-template-grouping"></a>Aallon mallipohjan ryhmittely

[!include [banner](../includes/banner.md)]

Aaltomalliryhmityksen avulla järjestelmä voi käyttää [aaltomalli](tasks/configure-wave-processing.md)-asetelmia määrittämään, perustuen määrittämiisi kriteereihin miten se pitäisi jakaa vapautetut rivit ja liittää ne uusiin tai olemassa oleviin aaltoihin. Tämä ominaisuus voi olla hyödyllinen varastoissa, joissa aallot luodaan tiettyjen kriteerien perusteella, mutta jossa esimiehet luovat mieluummin aallot automaattisesti manuaalisen sijaan. Sen avulla järjestelmä voi lisätä jokaisen vastikään vapautetun lähetyksen ensimmäiseen aaltoon, joka havaitsee, että se vastaa ryhmittelykenttien arvoja. Jos vastaavuutta ei löydy, järjestelmä luo uudelle siirrolle uuden aallon.

> [!IMPORTANT]
> Aaltomallin ryhmittelyä ei tueta *tuotannon raaka-aineiden keräily*- tai *Kanban-keräily*-työtyypeille. Tämä johtuu siitä, että aaltoryhmittely perustuu toimituksiin, eivätkä nämä työlajit käytä toimituksia.

## <a name="turn-on-the-wave-template-grouping-feature"></a>Aaltomallin ryhmittelytoiminnon ottaminen käyttöön

Ennen kuin voit käyttää *Aaltomallin ryhmittely* -toimintoa, sen pitää olla otettu käyttöön järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön, jos sitä vaaditaan. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Toiminnon nimi:** *Aaltomallin ryhmittely*

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a>Aaltomallin määrittäminen käyttämään aaltomallin ryhmittelyä

Voit määrittää aaltomalliryhmittelyn seuraavien [aaltomalli](tasks/configure-wave-processing.md)-ohjeiden avulla.

1. Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aaltomallit**.
1. Valitse vasemmasta ruudusta aaltomalli, jonka haluat määrittää. Jos valmistelet työskentelyä tämän ohjeaiheen mukaan myöhemmin tässä aiheessa käyttämällä demotietoja, valitse **62 toimituksen oletus** -malli.
1. Valitse **Muokkaa**, jotta saat sivun muokkaustilaan.
1. Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:

    - **Automatisoi aallonluonti:** *Kyllä*
    - **Määritä avoimiin aaltoihin:** *Kyllä*
    - **Käsittele aalto, kun se vapautetaan varastoon:** *Ei*

1. Valitse toimintoruudussa **Muokkaa kyselyä**, jotta voit avata kyselyvalintaikkunan.
1. Tarkista lajitteluehdot kyselyvalintaikkunan **Lajittelu**-välilehdessä ja varmista, että sääntö sisältää kentän, jota haluat käyttää aaltojen ryhmittelemiseen.

    Jos valmistelet toimintaskenaarion käyttöä demotietojen avulla, lisää rivi, jolla on seuraavat arvot:

    - **Taulukko:** *Lähetykset*
    - **Johdettu taulu:** *Lähetykset*
    - **Kenttä:** *Rahdinkuljetuspalvelu*

        > [!NOTE]
        > Kun olet valinnut tämän arvon, näyttöön saattaa tulla seuraava sanoma: "Rahdinkuljetuspalvelukenttä ei ole indeksikenttä. Haluatko lisätä lajittelun tähän? " Lisää lajittelu valitsemalla **Kyllä**.

    - **Hakusuunta:** *Laskeva*

1. Valitse **OK**, tallenna muutokset ja sulje kyselyvalintaikkuna.
1. Valitse Toimintoruudussa **Aaltomallinryhmittely**.
1. Valitse **Aaltomallin ryhmittely** -sivulla **Ryhmän mukaan** -valintaruutu jokaiselle riville, jota haluat käyttää tilausrivien ryhmittelyyn tarpeen mukaan. Jos valmistelet skenaarion käyttöä demotietojen avulla, valitse *Rahdinkuljetuspalvelu*-rivin **Ryhmittele**-valintaruutu.
1. Valitse **Tallenna**.
1. Lopeta **Aaltomallin ryhmittely** -sivu.
1. Tallenna mallit valitsemalla **Tallenna**.

## <a name="scenario"></a>Skenaario

Tässä osassa on skripti, jonka avulla voit selvittää, mitä toiminto tekee ja miten sitä käytetään.

### <a name="make-sample-data-available"></a>Ota mallitiedot käyttöön

Tämän skenaarion käyttäminen tässä määritettyjen mallitietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon vakio-[demotiedot](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) on asennettu. Sinun on myös valittava **USMF**-yritys ennen kuin aloitat.

Voit hyödyntää tätä skenaariota myös ohjeena, kun työskentelet tuotantojärjestelmän parissa ja käytät toimintoa. Tässä tapauksessa sinun on kuitenkin korvattava omat arvosi, ja sinulta saattaa puuttua joitakin pakollisia tietoja, joita vakiodemotiedot sisältävät.

### <a name="scenario-wave-template-grouping"></a>Skenaario: Aallon mallipohjan ryhmittely

Tämä skenaario näyttää, miten Aaltomalli-ryhmittelyä käytetään luomaan automaattisesti useita aaltoja aaltomallissa määritettyjen kriteerien mukaan. Tässä skenaariossa aaltomalli määritetään järjestelmään, jolloin luodaan yksi aalto operaattoripalvelua kohden.

Ennen kuin aloitat, valmistele aaltomalli [Määritä aaltomalli käyttääksesi aaltomallin ryhmittelyä](#set-up-template) -kohdassa aiemmin tässä ohjeaiheessa kuvatulla tavalla. Jos aiot käyttää tämän skenaarion demotietoja, varmista, että käytät tässä toimintosarjassa ehdotettuja demotietoarvoja. Tämän asetuksen avulla voit ryhmitellä aallot kullekin myyntitilaukselle määritetyn rahdinkuljetuspalvelun mukaan.

#### <a name="create-sales-order-1"></a>Luo myyntitilaus 1

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Luo uusi myyntitilaus valitsemalla **Uusi**.
1. Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:

    - Aseta **Asiakas**-pikavälilehdessä **Asiakastili**-kentän arvoksi *US-004*.
    - Aseta **Yleinen**-pikavälilehden **Varasto**-kentässä arvoksi *62*.

1. Valitse **OK** luodaksesi uuden myyntitilauksen ja sulje **Luo myyntitilaus** -valintaikkuna.
1. Uusi myyntitilaus avataan **Rivit**-näkymässä. Kirjoita myyntitilauksen numero muistiin.
1. Vaihda **Otsikko**-näkymään.
1. Määritä **Toimitus**-pikavälilehden **Kuljetus**-osassa seuraavat arvot:

    - **Rahdinkuljettaja:** *Lentorahti*
    - **Rahdinkuljetuspalvelu:** *Ilma*

1. Siirry takaisin **Rivit**-näkymään.
1. Valitse **Myyntitilausrivit**-osasta **Lisää rivi** lisätäksesi ruudukkoon rivin.
1. Määritä uudelle riville seuraavat arvot:

    - **Nimiketunnus:** *A0002*
    - **Määrä** *2*

1. Valitse uusi tilausrivi ja valitse sitten ruudukon yläpuolella olevasta **Varasto**-valikosta **Varaus**.
1. Valitse **Varaus**-sivun toimintoruudusta **Varaa erä**, jos haluat varata koko valitun rivin määrän varastosta.
1. Palaa myyntitilaukseen sulkemalla **Varaus**-sivun.
1. Valitse toimintoruudussa **Varasto**-välilehden **Toiminnot**-ryhmässä **Vapauta varastoon**.
1. Näyttöön tulee tietosanoma, jossa näkyy tämän tilauksen lähetys ja aalto. Kirjoita muistiin aallon tunnusnumero ja lähetyksen tunnusnumerot.

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a>Näytä myyntitilauksesta 1 luotu aalto

1. Valitse **Varastonhallinta \> Lähtevät aallot \> Lähetysaallot \> Kaikki aallot**.
1. Valitse myyntitilauksesta luodun aallon tunnus.
1. Valitse aallon tunnus -linkki ja avaa aallon tiedot -sivu.
1. Huomaa, että lähetys on lisätty **Aallon rivit** -pikavälilehteen.

#### <a name="create-sales-order-2"></a>Luo myyntitilaus 2

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Luo uusi myyntitilaus valitsemalla **Uusi**.
1. Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:

    - Aseta **Asiakas**-pikavälilehdessä **Asiakastili**-kentän arvoksi *US-005*.
    - Aseta **Yleinen**-pikavälilehden **Varasto**-kentässä arvoksi *62*.

1. Valitse **OK** luodaksesi uuden myyntitilauksen ja sulje **Luo myyntitilaus** -valintaikkuna.
1. Uusi myyntitilaus avataan **Rivit**-näkymässä. Kirjoita myyntitilauksen numero muistiin.
1. Vaihda **Otsikko**-näkymään.
1. Määritä **Toimitus**-pikavälilehden **Kuljetus**-osassa seuraavat arvot:

    - **Lähetyksen rahdinkuljettaja:** *Kukkakuljetus*
    - **Rahdinkuljetuspalvelu:** *Standardi*

1. Siirry takaisin **Rivit**-näkymään.
1. Valitse **Myyntitilausrivit**-osasta **Lisää rivi** lisätäksesi ruudukkoon rivin.
1. Määritä uudelle riville seuraavat arvot:

    - **Nimiketunnus:** *A0001*
    - **Määrä** *1*

1. Valitse uusi tilausrivi ja valitse sitten ruudukon yläpuolella olevasta **Varasto**-valikosta **Varaus**.
1. Valitse **Varaus**-sivun toimintoruudusta **Varaa erä**, jos haluat varata koko valitun rivin määrän varastosta.
1. Palaa myyntitilaukseen sulkemalla **Varaus**-sivun.
1. Valitse toimintoruudussa **Varasto**-välilehden **Toiminnot**-ryhmässä **Vapauta varastoon**.
1. Näyttöön tulee tietosanoma, jossa näkyy tämän tilauksen lähetys ja aalto. Kirjoita muistiin aallon tunnusnumero ja lähetyksen tunnusnumerot. Huomaa, että aallon tunnus eroaa ensimmäisen myyntitilauksen aallon tunnuksesta.

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a>Näytä myyntitilauksesta 2 luotu aalto

1. Valitse **Varastonhallinta \> Lähtevät aallot \> Lähetysaallot \> Kaikki aallot**.
1. Valitse toisesta myyntitilauksesta luodun aallon tunnus.
1. Valitse aallon tunnus -linkki ja avaa aallon tiedot -sivu.
1. Huomaa, että lähetys on lisätty **Aallon rivit** -pikavälilehteen.

Tälle siirrolle on luotu uusi aalto, koska se käyttää eri rahdin kuljetuspalvelua kuin ensimmäinen myyntitilaus.

#### <a name="create-sales-order-3"></a>Luo myyntitilaus 3

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Luo uusi myyntitilaus valitsemalla **Uusi**.
1. Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:

    - Aseta **Asiakas**-pikavälilehdessä **Asiakastili**-kentän arvoksi *US-006*.
    - Aseta **Yleinen**-pikavälilehden **Varasto**-kentässä arvoksi *62*.

1. Valitse **OK** luodaksesi uuden myyntitilauksen ja sulje **Luo myyntitilaus** -valintaikkuna.
1. Uusi myyntitilaus avataan **Rivit**-näkymässä. Kirjoita myyntitilauksen numero muistiin.
1. Vaihda **Otsikko**-näkymään.
1. Määritä **Toimitus**-pikavälilehden **Kuljetus**-osassa seuraavat arvot:

    - **Rahdinkuljettaja:** *Lentorahti*
    - **Rahdinkuljetuspalvelu:** *Ilma*

1. Siirry takaisin **Rivit**-näkymään.
1. Valitse **Myyntitilausrivit**-osasta **Lisää rivi** lisätäksesi ruudukkoon rivin.
1. Määritä uudelle riville seuraavat arvot:

    - **Nimiketunnus:** *A0001*
    - **Määrä** *1*

1. Valitse uusi tilausrivi ja valitse sitten ruudukon yläpuolella olevasta **Varasto**-valikosta **Varaus**.
1. Valitse **Varaus**-sivun toimintoruudusta **Varaa erä**, jos haluat varata koko valitun rivin määrän varastosta.
1. Palaa myyntitilaukseen sulkemalla **Varaus**-sivun.
1. Valitse toimintoruudussa **Varasto**-välilehden **Toiminnot**-ryhmässä **Vapauta varastoon**.
1. Näyttöön tulee tietosanoma, jossa näkyy tämän tilauksen lähetys ja aalto. Kirjoita muistiin aallon tunnusnumero ja lähetyksen tunnusnumerot. Lähetys on määritetty ensimmäisestä myyntitilauksesta olemassa olevalle aallolle.

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a>Näytä myyntitilausten 1 ja 3 aalto

1. Valitse **Varastonhallinta \> Lähtevät aallot \> Lähetysaallot \> Kaikki aallot**.
1. Valitse kolmannesta myyntitilauksesta luodun aallon tunnus.
1. Valitse aallon tunnus -linkki ja avaa aallon tiedot -sivu.
1. Huomaa, että lähetys on lisätty **Aallon rivit** -pikavälilehteen yhdessä ensimmäisen myyntitilauksen toimituksen kanssa.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]