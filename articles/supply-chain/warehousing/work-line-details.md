---
title: Työrivin tiedot
description: Tässä artikkelissa on tietoja Työrivin tiedot -sivusta, joka sisältää kattavan, lajiteltavissa olevan luettelon sekä suodatettavissa olevan luettelon järjestelmäsi yksittäisistä työriveistä.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkLocationChange, WHSWorkLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 1017527419acc2e4cb42b2bcb83131339d82b665
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218879"
---
# <a name="work-line-details"></a>Työrivin tiedot

[!include [banner](../includes/banner.md)]

**Työrivin tiedot** -sivu sisältää kattavan, lajiteltavissa olevan luettelon sekä suodatettavissa olevan luettelon järjestelmäsi yksittäisistä työriveistä. Se sisältää kattavan yhteenvedon työstä, jota suunnitellaan ja suoritetaan varastossa. Voit helposti vaihtaa kaikkien työrivien tarkastelemisen ja vain avointen työrivien tarkastelemisen välillä. Kunkin rivin tietoihin sisältyvät työn tila, nimiketunnus, sijainti, työmäärä, kuormituksen tunnus ja lähetystunnus.

## <a name="turn-on-the-work-line-details-feature"></a>Työrivin erittelytoiminnon ottaminen käyttöön

Supply Chain Managementin versiosta 10.0.21 alkaen tämä ominaisuus on poistettu oletusarvoisesti käytöstä. Järjestelmänvalvojat voivat tarkistaa [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -sivulla toiminnon tilan sekä ottaa sen käyttöön tai poistaa sen käytöstä tarvittaessa. Toiminto näkyy seuraavasti:

- **Moduuli:** *Varastonhallinta*
- **Ominaisuuden nimi:** *Työrivin tiedot*

## <a name="open-and-use-the-work-line-details-page"></a>Työrivin tiedot -sivun avaaminen ja käyttäminen

Jos haluat tarkastella työrivin tietojen luetteloa, siirry kohtaan **Varastonhallinta \> Työ \> Työrivin tiedot**. Tässä voit myös tehdä seuraavia toimenpiteitä:

- **Suodatin**-kentän avulla voit etsiä rivejä, joilla on tietty arvo mille tahansa käytettävissä olevalle parametrille. (Käytettävissä olevat parametrit sisältävät useita parametreja, joita ei näytetä ruudukon sarakkeina.)
- **Näytä suljettu** -valintaruudun avulla voit näyttää tai piilottaa suljetut rivit.
- Valitsemalla **Näytä dimensiot** voit avata **Dimensioiden näyttö** -valintaikkunan, jossa voit halutessasi näyttää tai piilottaa ruudukon eri dimensiosarakkeet.
- Valitse mikä tahansa sarakeotsikko, jos haluat avata valikon, jossa voit lajitella tai suodattaa luettelon kyseisen sarakkeen arvojen mukaan.
- Valitse työrivi ja avaa sitten valintaikkuna, jossa voit muuttaa kyseisen työrivin sijaintia, valitsemalla **Vaihda sijainti**. Määrittämäsi sijainti korvaa sijaintidirektiivin määritykset.
- Valitse työrivi ja valitse sitten **Peruuta työrivi**, niin näyttöön tulee valintaikkuna, jossa voit vähentää kyseisen työrivin määrää osittain tai kokonaan.
- Oikaise määrät.
- Näytä minkä tahansa työrivin takana olevat tapahtumat.

## <a name="try-out-the-feature"></a>Kokeile toimintoa

Tässä osassa on kolmiosainen esittely, jossa kerrotaan, miten työrivin tietoja käsitellään.

### <a name="make-sample-data-available"></a>Ota mallitiedot käyttöön

Tämän demon käyttäminen tässä määritettyjen mallitietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon vakio-[demotiedot](../../fin-ops-core/fin-ops/get-started/demo-data.md) on asennettu. Sinun on myös valittava **USMF**-yritys ennen kuin aloitat.

Voit hyödyntää tätä esittelyä myös ohjeena, kun työskentelet tuotantojärjestelmän parissa. Sinun on kuitenkin korvattava omat arvosi, ja sinulta saattaa puuttua joitakin pakollisia tietoja, joita vakiodemotiedot sisältävät.

### <a name="verify-that-the-scenario-setup-includes-enough-available-inventory"></a>Vahvista, että tilanteen määrittämiseen on riittävästi käytettävissä olevaa varastoa

Jos käytät **USMF**-esittelytietoja, sinun tulisi ensin varmistaa järjestelmäsi asetukset ja se, että kaikissa oleellisissa poimintasijanneissa on saatavilla tarpeeksi varastoa. Tätä esittelyä varten seuraavan varastomäärän on oltava sinulla vapaana varastossa:

- **Nimike M9200:** 45 kpl. (tai enemmän)
- **Nimike M9202:** 10 kpl. (tai enemmän)

Tarkista, että käytettävissä on riittävästi varastoa, ja tee tarvittavat oikaisut noudattamalla näitä ohjeita.

1. Siirry kohtaan **Varaston hallinta \> Asetukset \> Sijaintidirektiivit** ja määritä, mitä poimintasijainteja käytetään myyntitilausten keräilyyn varastossa 51. (Lisätietoja on kohdassa [Varastotyön valvonta työmallien ja sijaintidirektiivien avulla](control-warehouse-location-directives.md).)
1. Tarkista varastotasot asianmukaisissa sijainneissa.
1. Oikaise varasto tarpeen mukaan. Voit luoda manuaalisia siirtoja tai hyödyntää täydennystä tai käyttää mitä tahansa muuta virtausta oikaistaksesi varastoa.

### <a name="part-1-create-picking-work"></a>Osa 1: Luo poimintatyö

Ennen kuin aloitat töiden luomisen, varmista, että varastosi on määritetty vastaamaan työpyyntöihin odotetulla tavalla.

Seuraa seuraavia ohjeita luodaksesi poimintatyön.

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Valitse **Uusi** ja avaa **Luo myyntitilaus**-valintaikkuna.
1. Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:

    - Aseta **Asiakas**-pikavälilehdessä **Asiakastili**-kentän arvoksi _US-001_.
    - Aseta **Yleinen**-pikavälilehden **Varasto**-kentässä arvoksi _51_.

1. Valitse **OK** luodaksesi ostotilauksen ja sulje valintaikkuna.
1. Uusi myyntitilauksesi avataan. **Myyntitilausrivit**-ruudukko sisältää uuden, tyhjän rivin. Määritä seuraavat arvot tällä tilausrivillä:

    - **Nimiketunnus:** _M9200_
    - **Määrä** _20_
    - **Yksikkö:** _ea_

1. Valitse uusi tilausrivi ja valitse sitten ruudukon yläpuolella olevasta **Varasto**-valikosta **Varaus** avataksesi **Varaus**-sivun.
1. Valitse **Varaus**-sivulla **Varaa erä**, jos haluat varata koko valitun rivin määrän varastosta.
1. Palaa myyntitilaukseen sulkemalla **Varaus**-sivun.
1. Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**. Järjestelmä luo lähetyksen, lisää sen uuteen kuormitukseen ja luo tarvittavat työt.
1. Luo toinen myyntitilaus samalle asiakastilille ja varastolle, jota käytettiin ensimmäisessä tilauksessa. Lisää seuraavat kaksi tilausriviä tälle tilaukselle:

    - **Rivi 1:** Aseta **Nimiketunnus**-kentän arvoksi _M9200_, **Määrä**-kentän arvoksi _25_ ja **Yksikkö**-kentän arvoksi _kpl_.
    - **Rivi 2:** Aseta **Nimiketunnus**-kentän arvoksi _M9202_, **Määrä**-kentän arvoksi _10_ ja **Yksikkö**-kentän arvoksi _kpl_.

1. Toista vaiheet 6-8, kun haluat varata varaston kullekin tilausriville (yksi kerrallaan) ja vapauttaa sitten tilauksen varastoon toistamalla vaiheen 9.

### <a name="part-2-change-the-location-for-a-work-line"></a>Osa 2: Työrivin sijainnin muuttaminen

1. Valitse **Varastonhallinta \> Työ \> Työrivin tiedot**.
1. Etsi ja valitse jokin tälle demokohteelle luoduista työriveistä.
1. Avaa **Valitse uusi sijainti** -valintaikkuna valitsemalla **Vaihda sijainti**.
1. Valitse **Uuden sijainnin valitseminen** -valintaikkunan **Sijainti**-kentästä työriville uusi sijainti.
1. Ota muutokset käyttöön valitsemalla **OK** ja sulje valintaikkuna.

> [!IMPORTANT]
> Voit lähettää sijainnin muutoksia vain, jos uudessa sijainnissa on riittävästi käytettävissä olevaa varastoa (poimintaa varten) tai jos se läpäisee sijaintityypin vahvistuksen (käyttöön).

### <a name="part-3-change-the-quantity-of-a-work-line-or-cancel-a-work-line"></a>Osa 3: Työrivin määrän muuttaminen tai työrivin peruuttaminen

1. Valitse **Varastonhallinta \> Työ \> Työrivin tiedot**.
1. Etsi ja valitse jokin tälle demokohteelle luoduista työriveistä. Huomaa, että voit peruuttaa tai muuttaa määriä vain työriveille, joilla työtyyppi on _poiminta_.
1. Avaa **Peruutettava määrä** -valintaikkuna valitsemalla **Peruuta työrivi**.
1. Muuta **Peruutettava määrä** -valintaikkunassa **Määrä**-kentän arvoa ja määritä määrä, joka *vähennetään* riville määritettynä määränä. Oletusarvon mukaan **Määrä**-kentässä näkyy koko määrä.

    - Jos peruutat koko määrän, **Työtilan** arvoksi tulee _peruutettu_, mutta **Työmäärä**-kentässä näkyy edelleen alkuperäinen arvo.
    - Jos peruutat vain osan määrästä, **Työmäärä**-kenttä päivitetään uuden arvon näyttämiseksi, mutta **työn tila** -arvo ei muutu.

1. Ota muutokset käyttöön valitsemalla **OK** ja sulje valintaikkuna.

> [!IMPORTANT]
> Jos peruutat vain osan työrivin määrästä, myös vanhentunut määrä on poistettava kuormarivistä. Muussa tapauksessa kuormariviä ei voi vahvistaa, ellei alitoimitus ole määritetty oikein.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]