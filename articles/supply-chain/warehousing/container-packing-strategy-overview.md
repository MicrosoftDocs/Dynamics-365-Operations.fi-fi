---
title: Konttien pakkausstrategiat
description: Tässä aiheessa kuvataan konttien pakkausstrategioiden eroja ja annetaan esimerkkejä.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: article
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f481f6ca047ee0285fe0e81d8fa96665e9d27cee
ms.sourcegitcommit: 8e846b52763f90d2232ec7d427839f4722570bce
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/22/2021
ms.locfileid: "6292758"
---
# <a name="container-packing-strategies"></a>Konttien pakkausstrategiat

*Kontin pakkausstrategia* on strategia, jonka avulla voidaan määrittää nimikkeiden kohdistukset konttien välillä. Tässä aiheessa kerrotaan *Pakkaa kaikkiin avoimiin kontteihin* -strategian ja *Pakkaa vain nykyiseen konttiin* -strategian eroista.

- **Pakkaa kaikkiin avoimiin kontteihin** - Järjestelmän on tarkistettava kaikki avoimet kontit, jotka on jo luotu konttisyklin aikana, jotta voidaan varmistaa, että nimike sopii yhteen niistä. Pakkauksen aikana järjestelmä tarkistaa kunkin nimikkeen ja määrittää, sopiiko se aiemmin luotuihin kontteihin. Jos nimike ei mahdu aiemmin luotuun konttiin, järjestelmä luo uuden kontin ja jatkaa sitä, kunnes koko tilaus on pakattu valmiiksi.

    Esimerkiksi *n* tilattua nimikettä edellyttää konttiinpakkaamista. Pahimmassa tapauksessa joka kerta, kun järjestelmä käsittelee nimikkeen, joka ei sovi mihinkään konttiin, sen on arvioitava, sopiiko nimike aiemmin luotuihin kontteihin, ja tekee yhteensä (\[(*n* – 1) × (*n* + 1)\] ÷ 2) tarkistusta.

- **Pakkaa vain nykyiseen konttiin** – Järjestelmä on tarkistettava vain, sopiiko nimike viimeksi luotuun konttiin. Pakkauksen aikana järjestelmä tarkistaa kunkin nimikkeen ja määrittää, sopiiko se viimeisimmäksi luotuun konttiin. Jos nimike ei mahdu kyseiseen konttiin, järjestelmä luo uuden kontin ja jatkaa sitä, kunnes koko tilaus on pakattu valmiiksi.

    Esimerkiksi *n* tilattua nimikettä edellyttää konttiinpakkaamista. Pahimmassa tapauksessa järjestelmä tekee (*n* – 1) tarkistusta arvioidakseen, sopiiko nimike kontteihin.

## <a name="example-of-the-flow-for-container-packing-strategies"></a>Esimerkki konttien pakkausstrategioiden työnkulusta

Konttiinpakkaukselle määritetään seuraavat nimikkeet.

| Nimike | Fyysiset dimensiot (leveys × syvyys × korkeus) | Paino |
|---|---|---|
| HDMI-kaapeli 6' | 1 × 1 × 1 | 1 |
| HDMI-kaapeli 12' | 2 × 1 × 1 | 1 |
| HDMI-kaapeli 18' | 3 × 1 × 1 | 2 |

Pakkausta varten määritetään myös seuraava laatikko.

| Säilö | Fyysiset dimensiot (pituus × leveys × korkeus) | Paino | Tilavuus |
|---|---|---|---|
| Keskikokoinen laatikko | 6 × 3 × 2 | 10 | 100 |

Lopuksi määritetään tilaus, jossa on seuraavat tuotteet ja määrät.

| Myyntitilausrivi | Määrä |
|---|---|
| HDMI-kaapeli 12' | 9 |
| HDMI-kaapeli 18' | 8 |
| HDMI-kaapeli 6' | 13 |

Seuraavassa taulukossa on yhteenveto siitä, miten konttiin pakkaaminen toimii, kun käytät *Pakkaa kaikkiin avoimiin kontteihin* -strategiaa ja kun käytät *Pakkaa vain nykyiseen konttiin* -strategiaa.

| Pakkaa kaikkiin avoimiin kontteihin | Pakkaa nykyiseen konttiin |
|---|---|
| <p>HDMI-kaapeli 12':</p><ol><li>Luo uusi kontti, CONT0001.</li><li>Aseta 9 kpl konttiin CONT0001.</li></ol> | <p>HDMI-kaapeli 12':</p><ol><li>Luo uusi kontti, CONT0001.</li><li>Aseta 9 kpl konttiin CONT0001.</li></ol> |
| <p>HDMI-kaapeli 18':</p><ol><li>Tarkista, sopiiko nimike konttiin CONT0001.</li><li>Luo uusi kontti, CONT0002.</li><li>Aseta 5 kpl konttiin CONT0002.</li><li>Luo uusi kontti, CONT0003.</li><li>Aseta 3 kpl konttiin CONT0003.</li></ol> | <p>HDMI-kaapeli 18':</p><ol><li>Tarkista, sopiiko nimike konttiin CONT0001.</li><li>Luo uusi kontti, CONT0002.</li><li>Aseta 5 kpl konttiin CONT0002.</li><li>Luo uusi kontti, CONT0003.</li><li>Aseta 3 kpl konttiin CONT0003.</li></ol> |
| <p>HDMI-kaapeli 6':</p><ol><li>Tarkista, sopiiko nimike konttiin CONT0001.</li><li>Aseta 1 kpl konttiin CONT0001.</li><li>Tarkista, sopiiko nimike konttiin CONT0002.</li><li>Tarkista, sopiiko nimike konttiin CONT0003.</li><li>Aseta 4 kpl konttiin CONT0003.</li><li>Luo uusi kontti, CONT0004.</li><li>Aseta 8 kpl konttiin CONT0004.</li></ol> | <p>HDMI-kaapeli 6':</p><ol><li>Tarkista, sopiiko nimike konttiin CONT0003.</li><li>Aseta 4 kpl konttiin CONT0003.</li><li>Luo uusi kontti, CONT0004.</li><li>Aseta 9 kpl konttiin CONT0004.</li></ol> |

## <a name="example-scenario-pack-single-orders-per-container"></a>Esimerkki: Yksittäisten tilausten pakkaaminen konttia kohden

Tässä osassa esitetään skenaario, jossa järjestelmä on määritetty konsolidoimaan useita tilauksia yhdeksi lähetykseksi. Siksi konttiinpakkaus tehdään myyntitilauksesta, jotta jokainen useaa tuotetta sisältävä tilaus pakataan omaan konttiinsa.

Tämän toiminnon avulla voit käsitellä skenaarioita, joissa kuhunkin konttiin on pakattava vain yksi myyntitilaus, jotta jakelukeskus voi cross dock -käsitellä täysiä kontteja vähittäismyyntiliikkeiden välillä. Vähittäismyyntiskenaarioiden (myymäläkohtainen tilaus ja cross dockingia varten jakelukeskukseen lähettäminen) lisäksi tätä menetelmää käytetään usein lean-toimitusketjuissa (myyntitilaus just-in-time -tuotantoriviä kohden).

Tässä skenaariossa kerrotaan, miten pakkausten aikana arvioitujen konttien määrää voidaan vähentää käyttämällä *Pakkaa vain nykyiseen konttiin* -strategiaa.

### <a name="prerequisites"></a>Edellytykset

#### <a name="turn-on-the-consolidate-shipments-feature-in-your-system"></a>Lähetysten konsolidointiominaisuuden käyttöön ottaminen järjestelmässä

Tässä skenaariossa käytetään *Konsolidoi lähetykset* -toimintoa. Jos tämä toiminto ei ole vielä käytettävissä järjestelmässä, se on otettava käyttöön käyttämällä [Ominaisuuksien hallintaa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

#### <a name="make-demo-data-available"></a>Demotietojen ottaminen käyttöön

Tässä skenaariossa viitataan arvoihin ja tietueisiin, jotka sisältyvät Microsoft Dynamics 365 Supply Chain Managementin vakiodemotietoihin. Jos haluat käyttää harjoituksissa näitä annettuja arvoja, varmista, että demotiedot on asennettu työskentely-ympäristöön ja että yritykseksi on valittu **USMF** ennen aloittamista.

### <a name="inspect-or-create-container-types"></a>Konttityyppien tarkastaminen tai luominen

Noudattamalla seuraavia ohjeita voit tarkistaa konttityypit tai luoda tarvittaessa uusia konttityyppejä.

1. Valitse **Varastonhallinta** \> **Asetukset** \> **Kontit** \> **Konttityypit**.
1. Varmista, että esittelytiedoissa on käytettävissä kukin seuraavista konttityypeistä. Muokkaa tai luo konttityyppejä tarpeen mukaan.

    - Konttityyppi 1:

        - **Konttityypin koodi:** *Laatikko-suuri*
        - **Kuvaus:** *Suuri laatikko*
        - **Enimmäisnettopaino:** *100*
        - **Tilavuus:** *400*
        - **Pituus:** *4*
        - **Leveys:** *10*
        - **Korkeus:** *10*

    - Konttityyppi 2:

        - **Konttityypin koodi:** *Laatikko-keskisuuri*
        - **Kuvaus:** *Keskikokoinen laatikko*
        - **Enimmäisnettopaino:** *50*
        - **Tilavuus:** *200*
        - **Pituus:** *2*
        - **Leveys:** *10*
        - **Korkeus:** *10*

    - Konttityyppi 3:

        - **Konttityypin koodi:** *Laatikko-pieni*
        - **Kuvaus:** *Pieni laatikko*
        - **Enimmäisnettopaino:** *20*
        - **Tilavuus:** *100*
        - **Pituus:** *1*
        - **Leveys:** *10*
        - **Korkeus:** *10*

### <a name="inspect-or-create-container-groups"></a>Konttiryhmien tarkastaminen tai luominen

Noudattamalla seuraavia ohjeita voit tarkistaa konttiryhmät tai luoda tarvittaessa uusia konttiryhmiä.

1. Valitse **Varastonhallinta** \> **Asetukset** \> **Kontit** \> **Konttiryhmät**.
1. Varmista, että esittelytiedoissa on käytettävissä seuraavat konttiryhmät. Jos se ei ole käytettävissä, luo se valitsemalla **Uusi**.

    - **Konttiryhmän tunnus:** *Laatikot*
    - **Kuvaus:** *Laatikoiden koot*

1. Varmista *Laatikot*-konttiryhmän **Erittely**-pikavälilehdessä, että seuraavat rivit ovat olemassa. Jos niitä ei ole, lisää ne valitsemalla **Uusi**.

    - Rivi 1:

        - **Järjestysnumero:** *1*
        - **Kontin tyyppi:** *Laatikko-suuri*
        - **Kontin käyttöasteprosentti:** *100*

    - Rivi 2:

        - **Järjestysnumero:** *2*
        - **Konttityyppi:** *Laatikko-keskisuuri*
        - **Kontin käyttöasteprosentti:** *100*

    - Rivi 3:

        - **Järjestysnumero:** *3*
        - **Konttityyppi:** *Laatikko-pieni*
        - **Kontin käyttöasteprosentti:** *100*

### <a name="create-a-new-container-build-template"></a>Luo uusi kontin rakennusmalli

Voit luoda uuden kontin muodostusmallin noudattamalla seuraavia ohjeita.

1. Valitse **Varastonhallinta** \> **Asetukset** \> **Kontit** \> **Kontin koontimalli**.
1. Valitse **Uusi**, jos haluat luoda kontin rakennusmallin, jolla on seuraavat asetukset:

    - **Järjestysnumero:** *1*
    - **Konttimallin tunnus:** *Laatikko*
    - **Konttiryhmän tunnus:** *Laatikot*
    - **Peruskyselytyypit:** *Myynnin kohdistusrivi*
    - **Aallon vaihekoodi:** *234*
    - **Salli jaetut valinnat:** *Kyllä*
    - **Kontin pakkausstrategia:** *Pakkaa vain nykyiseen konttiin*
    - **Pakkaaminen direktiiviyksikön mukaan:** *Ei*

1. Kun uuden mallin rivi on vielä valittuna, valitse **Muokkaa kyselyä** toimintoruudusta.
1. Näyttöön tulee vakiokyselyeditorin valintaikkuna. Lisää seuraavat asetukset sisältävä rivi valitsemalla **Lajittelu**-välilehdessä **Lisää**:

    - **Taulukko:** *Väliaikaiset työtapahtumat*
    - **Johdettu taulukko:** *Väliaikaiset työtapahtumat*
    - **Kenttä:** *Tilausnumero*
    - **Hakusuunta:** *Laskeva*

    > [!IMPORTANT]
    > Kun haluat välttää kierrättämisen muiden avoimien konttien kautta ja nopeuttaa prosessia tarkistamalla yhden kontin kerrallaan, käytä *Pakkaa vain nykyiseen konttiin* -strategiaa tilausnumeron mukaan lajittelun lisäksi. Tämä yhdistelmä toimii kuten työmallin työtauko.

1. Sulje kyselyeditorin valintaikkuna valitsemalla **OK**.
1. Kun uuden mallin rivi on vielä valittuna, valitse **Kontin yhdistämisrajoitukset** toimintoruudusta.

    Lisäät nyt rajoitus, joka asettaa nimikkeet yksittäisestä tilauksesta yhteen konttiin. Minkä tahansa tilauksen nimikkeet laitetaan erilliseen konttiin.

1. Valitse **Uusi**, jos haluat luoda yhdistämisrajoituksen, jolla on seuraavat asetukset:

    - **Taulu:** *Myyntitilaukset*
    - **Kentän valinta:** *SalesId* (kenttä näkyy ruudukossa *myyntitilauksena*.)

1. Valitse **OK** lisätäksesi rajoituksen.
1. Sulje sivu.

### <a name="set-up-a-wave-template-for-containerization"></a>Aseta aaltomalli konttiinpakkausta varten

Määritä aaltomalli noudattamalla seuraavia ohjeita.

1. Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aaltomallit**.
1. Aseta luetteloruudussa **Aaltomallityyppi**-kentän arvoksi *Lähetys*.
1. Valitse luettelosta **63 - konttiinpakkaus** -malli.
1. Valitse toimintoruudussa **Muokkaa**.
1. Etsi **Menetelmät**-välilehden **Valitut menetelmät**-sarakkeesta seuraava rivi:

    - **Menetelmän nimi:** *konttiinpakkaus*
    - **Nimi:** *Konttiinpakkaus*

1. Määritä **Aallon vaihekoodi** -kentän arvoksi riville *234*.

### <a name="set-up-a-work-template"></a>Määritä työmalli

Määritä työmalli noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työmallit**.
1. Määritä **Työtilaustyyppi**-kentän arvoksi *Myyntitilaukset*.
1. Etsi ja valitse **Yleiskatsaus**-ruudukossa työmalli, jota pitää käyttää yksittäisten tilausten pakkaamiseen yhteen konttiin. Valitse tässä skenaariossa **63 – poimi konttiin** -malli.
1. Valitse toimintoruudussa **Muokkaa kyselyä**.
1. Näyttöön tulee vakiokyselyeditorin valintaikkuna. Lisää **Lajittelu**-välilehdelle seuraavat rivit:

    - Rivi 1:

        - **Taulukko:** *Väliaikaiset työtapahtumat*
        - **Johdettu taulukko:** *Väliaikaiset työtapahtumat*
        - **Kenttä:** *Lähetyksen tunnus*
        - **Hakusuunta:** *Laskeva*

    - Rivi 2:

        - **Taulukko:** *Väliaikaiset työtapahtumat*
        - **Johdettu taulukko:** *Väliaikaiset työtapahtumat*
        - **Kenttä:** *Tilausnumero*
        - **Hakusuunta:** *Laskeva*

    - Rivi 3:

        - **Taulukko:** *Väliaikaiset työtapahtumat*
        - **Johdettu taulukko:** *Väliaikaiset työtapahtumat*
        - **Kenttä:** *Kontin tunnus*
        - **Hakusuunta:** *Laskeva*

1. Sulje kyselyeditorin valintaikkuna valitsemalla **OK**.
1. Seuraava sanoma avautuu: Ryhmittely nollataan. Haluatko jatkaa? Jatka valitsemalla **Kyllä**.
1. Kun **63 – poimi konttiin** -malli on yhä valittuna, valitse **Työn otsikoiden katkaisut** toimintoruudusta.

    Työn katkaisemiseen käytetään nyt asetuksia, jotta tilauksen kukin kontti linkitetään yhteen työtilaukseen.

1. Valitse **Työn otsikoiden katkaisut** -sivun jokaisen rivin **Ryhmittele tämän kentän mukaan** -valintaruutu (**lähetystunnus**, **tilausnumero** ja **kontin tunnus**).
1. Sulje sivu.

### <a name="set-up-shipment-consolidation-policies"></a>Määritä lähetyksen konsolidoinnin käytännöt

Lähetyksen konsolidointikäytäntö määritetään seuraavasti.

1. Valitse **Varastonhallinta \> Asetukset \> Vapauta varastoon \> Lähetyksen konsolidointikäytännöt**.
1. Määritä luetteloruudussa **Käytännön tyyppi**-kentän arvoksi *Myyntitilaukset*.
1. Valitse luettelosta **Oletus**-käytäntö.
1. Valitse toimintoruudussa **Muokkaa**.
1. Valitse **Konsolidointikentät**-pikavälilehden **Valitut kentät** -luettelossa rivi, jossa **Kentän nimi** -kentän asetuksena *Tilausnumero*.
1. Siirrä kenttä **Jäljellä olevat kentät** -luetteloon valitsemalla **Poista**-painike ![vasen nuoli](media/backward-button.png).
1. Valitse toimintoruudussa **Tallenna**.

### <a name="set-up-physical-dimensions-for-the-product"></a>Määritä tuotteen fyysiset mitat

Noudattamalla seuraavia ohjeita voit määrittää tässä skenaariossa käytettävät tuotteiden fyysiset mitat.

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Valitse tuote, jossa **Nimiketunnus**-kentän arvoksi on määritetty *A0001*.
1. Valitse toimintoruudun **Varastonhallinta**-välilehden **Varasto**-ryhmässä **Fyysiset mitat**.
1. **Fyysiset mitat** -sivulla ruudukossa on seuraava rivi:

    - **Yksikkö:** *kpl*
    - **Bruttopaino:** *3,00*
    - **Leveys:** *2,00*
    - **Syvyys:** *2,00*
    - **Korkeus:** *4,00*
    - **Tilavuus:** *16,00*

1. Sulje sivu.
1. Valitse tuote, jossa **Nimiketunnus**-kentän arvoksi on määritetty *A0002*.
1. Valitse toimintoruudun **Varastonhallinta**-välilehden **Varasto**-ryhmässä **Fyysiset mitat**.
1. **Fyysiset mitat** -sivulla ruudukossa on seuraava rivi:

    - **Yksikkö:** *kpl*
    - **Bruttopaino:** *4,00*
    - **Leveys:** *3,00*
    - **Syvyys:** *1,00*
    - **Korkeus:** *3,00*
    - **Tilavuus:** *9,00*

### <a name="create-sales-order-1"></a>Luo myyntitilaus 1

Luo myyntitilaus seuraavien ohjeiden mukaisesti.

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Valitse toimintoruudussa **Uusi**.
1. Näyttöön tulee valintaikkuna, jossa voit luoda uuden myyntitilauksen. Määritä seuraavat arvot:

    - **Asiakastili:** *US-001*
    - **Varasto**: *63*

1. Valitse **OK** luodaksesi ostotilauksen ja sulje valintaikkuna.
1. Uusi myyntitilaus avataan. Lisää seuraavat myyntirivit **Myyntitilausrivit**-pikavälilehdessä:

    - Rivi 1:

        - **Nimiketunnus:** *A0001*
        - **Määrä** *2*

    - Rivi 2:

        - **Nimiketunnus:** *A0002*
        - **Määrä** *2*

1. Valitse ensimmäinen rivi ja valitse sitten **Varasto \> Varaus**.
1. Valitse **Varaus**-sivun kohta **Varaa erä**. Sulje sitten sivu.
1. Toista kaksi edellistä vaihetta toiselle riville.
1. Sulje sivu.

### <a name="create-sales-order-2"></a>Luo myyntitilaus 2

Luo toinen myyntitilaus seuraavasti.

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Valitse toimintoruudussa **Uusi**.
1. Näyttöön tulee valintaikkuna, jossa voit luoda uuden myyntitilauksen. Määritä seuraavat arvot:

    - **Asiakastili:** *US-001*
    - **Varasto**: *63*

1. Valitse **OK** luodaksesi ostotilauksen ja sulje valintaikkuna.
1. Uusi myyntitilaus avataan. Lisää seuraavat myyntirivit **Myyntitilausrivit**-pikavälilehdessä:

    - Rivi 1:

        - **Nimiketunnus:** *A0001*
        - **Määrä** *4*

    - Rivi 2:

        - **Nimiketunnus:** *A0002*
        - **Määrä** *4*

1. Valitse ensimmäinen rivi ja valitse sitten **Varasto \> Varaus**.
1. Valitse **Varaus**-sivun kohta **Varaa erä**. Sulje sitten sivu.
1. Toista kaksi edellistä vaihetta toiselle riville.
1. Sulje sivu.

### <a name="create-the-load"></a>Kuorman luominen

Luo jokaiselle tähän skenaarioon luodulle tilaukselle kuorma ja vapauta se sitten varastoon näiden ohjeiden avulla.

1. Valitse **Varastonhallinta \> Kuormat \> Kuormasuunnittelun työtila**.
1. Etsi ja valitse **Myyntirivit**-välilehdessä kaikki myyntitilausrivit yhdestä tätä skenaariota varten luoduista myyntitilauksista.
1. Valitse toimintoruudun **Tarjonta ja kysyntä** -välilehden **Lisää**-ryhmässä kohta **Uuteen kuormaan**. Valitut tilausrivit lisätään uuteen kuormaan.
1. Valitse **Kuormamallin määritys** -valintaikkunan **Kuorman mallitunnus** -kentässä kuormamalli, kuten *40' kontti*.
1. Sulje valintaikkuna valitsemalla **OK**.
1. Etsi ja valitse juuri luotu kuorma **Kuormat**-osassa.
1. Valitse **Vapauta \> Vapauta varastoon**.
1. Vapauta valittu kuorma varastoon valitsemalla **Vapauta varastoon** -valintaikkunassa **OK**.

### <a name="verify-the-shipments-and-containers"></a>Lähetysten ja konttien tarkistaminen

Seuraavalla toiminnolla voit vahvistaa luodut lähetykset. Tarkista sen avulla tätä skenaariota varten luomasi tilaus ja varmista, että olet saanut odotetut tulokset.

1. Valitse **Varastonhallinta \> Lähetykset \> Kaikki lähetykset**.
1. Etsi ja valitse juuri vapautetulle kuormalle luotu lähetys.
1. Valitse toimintoruudun **Kuljetus**-välilehdessä **Näytä kontit**.
1. Vahvista, että myyntitilausten nimikkeet on pakattu kahteen eri konttiin.

## <a name="additional-resources"></a>Lisäresurssit

- [Konttiinpakkaus](wave-containerization.md)
