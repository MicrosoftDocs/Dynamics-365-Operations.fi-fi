---
title: Nimikkeen konsolidointi – sijainnin käyttöaste
description: Tässä aiheessa käsitellään toimintoja, joiden avulla varastopäälliköiden on helppo tarkastella ja suodattaa varaston sijaintien tilavuusperusteista käyttöastetta. Päälliköt voivat valita sijainteja ja luoda varaston siirtotyön suoraan Nimikkeen konsolidointi -sivulla nimikkeiden konsolidointi varten, mikä parantaa varastotilan käyttöä.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM, WHSMovementType, WHSItemConsolidationForm, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6a328b20c1cfb2fc376ab4656c64cf585a5aa015
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4427398"
---
# <a name="item-consolidation---location-utilization"></a>Nimikkeen konsolidointi – sijainnin käyttöaste

[!include [banner](../includes/banner.md)]

Tässä aiheessa käsitellään toimintoja, joiden avulla varastopäälliköiden on helppo tarkastella ja suodattaa varaston sijaintien tilavuusperusteista käyttöastetta. Päälliköt voivat valita sijainteja ja luoda varaston siirtotyön suoraan **Nimikkeen konsolidointi** -sivulla nimikkeiden konsolidointi varten, mikä parantaa varastotilan käyttöä.

## <a name="turn-on-the-features"></a>Toimintojen ottaminen käyttöön

Ennen tässä aiheessa käsiteltyjen toimintojen käyttöä ne on otettava käyttöön järjestelmässä. Järjestelmänvalvojat voivat tarkistaa näiden toimintojen tilan ja ottaa ne tarvittaessa käyttöön [Toimintojen hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilassa. Ota seuraavat toiminnot käyttöön ilmoitetussa järjestyksessä. (Molemmat toiminnot ovat **Varastonhallinta**-moduulissa.)

1. Varastosijainnin tila
2. Nimikkeen konsolidointisijainnin käyttöaste

## <a name="warehouse-location-status"></a>Varastosijainnin tila

*Varastosijainnin tila* -toiminto lisää **Sijainnit**-sivulle neljä uutta kenttää, joilla voi seurata lisätietoja sijainnin nykyisestä tilasta:

- **Nimiketunnus** – Nimike, joka on tällä hetkellä sijainnissa. Jos sijainnissa on useita nimikkeitä, tämä kenttä on tyhjä.
- **Viimeinen tehtävän päivämäärä ja kellonaika** – Viimeistä varastopaikkaa vasten suoritetun fyysisen varastoinnin tapahtuman aikaleima.
- **Erääntymispäivämäärä** – Päivämäärä, jolloin varastosijainti tuotiin varastoon. Tämä päivämäärä lasketaan rekisterikilven erääntymispäivämäärän perusteella. Vaikka tämä päivämäärä tarkka sellaisissa sijainneissa, joissa on rekisterikilpiseuranta, se ei ehkä ole tarkka sellaisissa sijainneissa, jotka eivät ole rekisterikilpiseurannassa.
- **Sijainnin tila** – Sijainnin tila. Käytettävissä on neljä arvoa:

    - **Määrittelemätön** – Sijaintiprofiili ei voi jäljittää tilaa. Näin ollen nykyistä tilaa ei tunneta.
    - **Tyhjä** – sijainnissa ei ole varastoa.
    - **Keräys** – lähtevät tapahtumat on suoritettu sijainnille sen jälkeen, kun se oli viimeksi tyhjä.
    - **Varasto** – Vain saapuvat tapahtumat on suoritettu sen jälkeen, kun sijainti oli viimeksi tyhjä.

Näiden kenttien avulla varastopäälliköt saavat paremman yleiskuvan varaston sijaintien tilasta. Ne mahdollistavat myös kehittyneet raportointi- ja suodatusasetukset.

## <a name="set-up-item-consolidation-and-location-utilization"></a>Nimikkeen konsolidointi ja sijainnin käyttöasteen määrittäminen

Tässä osassa käsitellään järjestelmän valmistelemista käyttämään nimikkeen konsolidointia ja sijainnin käyttöastetta. Menettelyssä käytetään vakioesittelytietojen näytearvoja. Jos aiot käyttää myöhemmin tässä ohjeaiheessa käsiteltyä esimerkkiskenaariota, valitse **USMF**-yritys (joka sisältää vakioesittelytiedot) ja luo jokainen tässä osassa kuvattu tietue. Jos et aio käyttää esimerkkiskenaariota, tässä annettuja arvoja voi pitää esimerkkeinä asetustyypeistä, jotka on tehtävä toimintojen käyttöä varten.

### <a name="released-product"></a>Vapautettu tuote

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Valitse **Nimiketunnus**-kentässä *M9201* ja avaa tietosivu.
1. Valitse toimintoruudun **Varastonhallinta**-välilehden **Varasto**-ryhmässä **Fyysiset mitat**.
1. Valitse **Fyysiset mitat** -sivun toimintoruudussa **Uusi**.

    Uusi rivi lisätään ruudukkoon. **Nimiketunnus**-kenttä on määritetty valmiiksi.

1. Valitse **Yksikkö**-kentässä *kpl*. Muut rivin kentät määritetään automaattisesti.
1. Valitse **Tallenna** ja sulje sivu.

### <a name="location-profile"></a>Sijaintiprofiili

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varasto \> Sijaintiprofiilit**.
1. Valitse sijaintiprofiililuettelossa **KERROS-05**.
1. Valitse toimintoruudussa **Muokkaa**.
1. Varmista **Yleiset**-pikavälilehdessä seuraavissa asetuksissa on valittu *Kyllä*:

    - Ota käyttöön nimike sijainnissa
    - Ota käyttöön sijaintitila

1. Valitse **Tallenna**.

    > [!IMPORTANT]
    > Jos **Ota nimike sijainnissa käyttöön**- ja **Ota käyttöön sijaintitila** -asetusten arvo on jo *Kyllä*, siirry vaiheeseen 10, jossa on **Dimensiot**-pikavälilehden määritysohjeet. Jos asetusten arvona ei ole vielä *Kyllä*, tee **Varastonhallinta**-moduulin yhdenmukaisuustarkistus sen jälkeen, kun asetukset on määritetty manuaalisesti. Jatka siinä tapauksessa Jatka seuraavaan vaiheeseen.

1. Suorita yhdenmukaisuustarkistus valitsemalla **Järjestelmän hallinta \> Kausittaiset tehtävät \> Tietokanta \> Yhdenmukaisuustarkistus**.
1. Määritä seuraavat arvot **Yhdenmukaisuustarkistus**-valintaikkunassa:

    - **Moduuli:** *Varastonhallinta*
    - **Tarkista/korjaa:** *Tarkista*
    - **Päivämäärästä:** Jätä tämä kenttä tyhjäksi.
    - **Varaston sijainnin tilan yhdenmukaisuustarkistus:** Valitse tämä valintaruutu.

1. Valitse **OK**.

    > [!TIP]
    > Saat ilmoituksen, kun yhdenmukaisuustarkistus on valmis. Voit lukea viestin avaamalla [toimintokeskuksen](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications). Voit katsoa tiedot valitsemalla **Sanoman tiedot**.
    >
    > Jos yhdenmukaisuustarkistuksen sanoma on Virheelliset sijaintitilatiedot löydetty sijainnille XXXX varastossa XX, yhdenmukaisuustarkistus on suoritettava uudelleen. Valitse tällä kertaa **Tarkista/korjaa**-kentässä *Korjaa virhe*. Tarkista sanomista, että virheitä ei löytynyt.

1. Viimeistele sijaintiprofiilin määritykset. Valitse taas **Varastonhallinta \> Asetukset \> Varasto \> Sijaintiprofiilit**, valitse sitten sijaintiprofiili **KERROS-05** ja valitse lopuksi toimintoruudussa **Muokkaa**.
1. Määritä **Dimensiot**-pikavälilehdessä seuraavat arvot:

    - **Tilavuuden käyttöasteprosentti:** *100*
    - **Varastosijainnissa käytettävä tilavuuden mittausmenetelmä:** *Käytä sijainnin tilavuutta*
    - **Sijainnin todellinen korkeus:** *10*
    - **Sijainnin todellinen leveys:** *10*
    - **Sijainnin todellinen syvyys:** *10*
    - **Enimmäispaino;** *100*

1. Valitse **Tallenna**.

### <a name="mobile-device-menu-items"></a>Mobiililaitteen valikkovaihtoehdot

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Luo lajittelun valikkovaihtoehto valitsemalla toimintoruudussa **Uusi**.
1. Aseta otsikkorivillä seuraavat arvot:

    - **Valikkovaihtoehdon nimi:** *Oikaisu sisään*
    - **Otsikko:** *Oikaisu sisään*
    - **Tila:** *Työ*
    - **Käytä aiemmin luotua työtä:** *Ei*

1. Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:

    - **Työn luontiprosessi:** *Oikaisu sisään*
    - **Varasto-oikaisutyypit:** *Oikaisu sisään*

1. Valitse **Tallenna**.

### <a name="mobile-device-menu"></a>Mobiililaitevalikko

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikko**.
1. Valitse valikkoluettelosta **Varasto**.
1. Valitse toimintoruudussa **Muokkaa**.
1. Etsi ja valitse **Käytettävissä olevat valikot ja valikkovaihtoehdot** -luettelosta **Oikaisu sisään** -valikkovaihtoehto.
1. Siirrä **Oikaisu sisään** oikealla nuolipainikkeella **Valikon rakenne** -luetteloon. Uusi valikkovaihtoehto lisätään tällä tavoin valittuun valikkoon.
1. Valitse **Tallenna**.

### <a name="movement-types"></a>Siirtotapahtuman tyypit

1. Valitse **Varastonhallinta \> Määritys \> Varasto \> Siirtotapahtuman tyypit**.
1. Valitse toimintoruudussa **Uusi** ja määritä sitten seuraavat arvot:

    - **Siirtotapahtumatyypin koodi:** *KONSOLIDOI*
    - **Kuvaus:** *Konsolidoi sijainnit*
    - **Työluokan tunnus:** *InvMov*

1. Valitse **Tallenna**.

## <a name="example-scenario"></a>Esimerkkiskenaario

Seuraavassa skenaariossa käytetään varastosovellusta mobiililaitteessa tekemään varaston *oikaisu sisään* varaston kahdessa sijainnissa.

### <a name="add-inventory-to-locations"></a>Varaston lisääminen sijainteihin

1. Kirjaudu mobiililaitteeseen käyttäjänä, joka on määritetty varastoon *51*.
1. Valitse **Varasto \> Oikaisu sisään**.

    Anna nyt ensimmäinen varaston oikaisu.

1. Valitse **Oikaisu sisään** -tehtävässä sijainti, jonka varastoa oikaistaan. Valitse **SIJAINTI**-kentässä *RK-001*.
1. Vahvista sijainti.
1. Luo sijaintiin lisättävälle nimikkeelle rekisterikilpitunnus. Anna **RK**-kentässä *RK00101*.
1. Vahvista rekisterikilpi.
1. Kirjoita rekisterikilpeen lisättävä nimike. Kirjoita **ITEM**-kenttään *M9201*.
1. Vahvista nimike.
1. Anna lisättävän nimikkeen määrä. Anna **MÄÄRÄ**-kentässä *10*.
1. Vahvista määrä.

    Näyttöön tulee Työ valmis -sanoma. Anna nyt toinen varaston oikaisu.

1. Valitse **Oikaisu sisään** -tehtävässä sijainti, jonka varastoa oikaistaan. Valitse **SIJAINTI**-kentässä *RK-002*.
1. Vahvista sijainti.
1. Luo sijaintiin lisättävälle nimikkeelle rekisterikilpitunnus. Anna **RK**-kentässä *LP00201*.
1. Vahvista rekisterikilpi.
1. Kirjoita rekisterikilpeen lisättävä nimike. Kirjoita **ITEM**-kenttään *M9201*.
1. Vahvista nimike.
1. Anna lisättävän nimikkeen määrä. Anna **MÄÄRÄ**-kentässä *15*.
1. Vahvista määrä.

    Näyttöön tulee Työ valmis -sanoma.

1. Valitse valikkopainike (jossa on allekkain useita viivoja) ja lopeta **Oikaisu sisään** -tehtävä valitsemalla **Peruuta**.

### <a name="consolidate-locations"></a>Sijaintien konsolidointi

1. Valitse **Varastonhallinta \> Kausittaiset tehtävät \> Nimikkeen konsolidointi**.
1. Valitse ylätunnisteessa konsolidoitava varasto. Anna **Varasto**-kentässä *51*.

    Tietue näytetään jokaiselle sijainnille, jossa nimikettä *M9201* säädettiin. **Käyttöasteprosentti**-sarake näyttää kunkin sijainnin tilavuusperusteisen käyttöasteen.

1. Varasto konsolidoidaan valitsemalla kaikki konsolidoitavat sijainnit ja valitsemalla sitten toimintoruudussa **Konsolidoi varasto**.
1. Määritä **Konsolidoi varasto** -valintaikkunassa sijainti ja siirtotapahtuman tyyppi, joiden avulla varaston siirtotapahtuman työ on luotava. Määritä seuraavat arvot:

    - **Sijainti:** *RK-001*
    - **Siirtotapahtumatyypin koodi:** *KONSOLIDOI*

1. Valitse **OK**.
1. Saat työn siirtotapahtumatyön luonnista ilmoittavan tietosanoman. Kirjoita siirtotapahtumatyön tunnus muistiin.

### <a name="view-movement-work"></a>Siirtotapahtumatyön näyttäminen

1. Valitse **Varastonhallinta \> Työ \> Työn tiedot**.
1. Näytä luotu työ. Suodata työruudukkoa tai tee siinä haku käyttämällä varaston konsolidoinnin siirtotapahtumatyön tunnusta.

    Tässä skenaariossa aiemmin luotua sijaintia, jossa oli varastoa, käytetään varaston konsolidointisijaintina. Tämän vuoksi vain yksi työtunnus luotiin.

    > [!NOTE]
   > Järjestelmä luo kullekin suoritettavalle siirrolle yhden työtunnuksen. Jos määrität jo varastoa sisältävän sijainnin, vain yksi työtunnus luodaan. Jos määritä uuden sijainnin, työtunnuksia luodaan kaksi.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]