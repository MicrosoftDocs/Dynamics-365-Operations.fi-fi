---
title: Asettaminen seinälle – asettaminen myymälään
description: Tässä ohjeaiheessa käsitellään Asettaminen seinälle – asettaminen myymälään -toimintoa. Tällä toiminnolla voi käsitellä skenaarioita, joissa tuote on konsolidoitava esipakkauksen valmistelualueelle määritettävien ehtojen perusteella. Se auttaa lyhentämään keräilyaikaa, koska keräyksen voi tehdä sen avulla yhden kohderekisterikilven mukaan ja koska siinä voi käyttää enemmän asetuspaikkoja kuin klusterikeräilyssä.
author: Mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationType, WHSLocationProfile, WHSLocation, WHSPackProfile, WHSWaveStepCode, WHSOutboundSortTemplate, WHSPostMethod, WHSWaveTemplateTable, WHSLocDirTable, WHSWorkClass, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: d8c88b742c1dccb169e47fe96a5c9d9aac35e605be685cc1a0f010826c959db5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712859"
---
# <a name="put-to-wall---put-to-store"></a>Asettaminen seinälle – asettaminen myymälään

[!include [banner](../includes/banner.md)]

*Asettaminen seinälle – asettaminen myymälään* -toiminnolla voi käsitellä skenaarioita, joissa tuote on konsolidoitava esipakkauksen valmistelualueelle määritettävien ehtojen perusteella. Koska keräilyn voi tehdä toiminnolla yhden rekisterikilven mukaan ja koska käytettävissä on enemmän asettamispaikkoja kuin klusterikeräilyssä, myymälöihin toimittaville yrityksillä tai pieniä nimikkeitä käsitteleville yrityksille on hyötyä keräilyajan lyhenemisestä.

Tämän toiminnon työnkulku ohjaa kerätyn tuotteen lajittelusijaintiin jaettavaksi eri tyyppisiin kontteihin. Yleistäen voisi sanoa, että kukin lajittelusijainti sisältää useita lajittelupaikkoja. Kukin lajittelupaikka määritetään liiketoimintaprosessin määrittämien ehtojen mukaisesti. Tavallisia ehtoja ovat lopullinen määränpää, lähetys tai kuorma. Tuote jaetaan saapumisen jälkeen kuhunkin lajittelupaikkaan tilaukseen, määränpäähän, lähetykseen tai kuormaan liitetyn määrän mukaan. Kun kontti on täynnä tai valmis, se siirretään liiketoimintaprosessin mukaan väliaikaiseen sijaintiin tai lähetyssijaintiin lisäkäsittelyä varten.

Tätä varastointitoimintoa kutsutaan myös valo-ohjatuksi keräilyksi.

## <a name="turn-on-the-outbound-sorting-feature"></a>Lähtevän lajittelutoiminnon ottaminen käyttöön

Ennen *Asettaminen seinälle – asettaminen myymälään* -toiminnon käyttöä *Lähtevä lajittelu* on otettava käyttöön järjestelmässä. Järjestelmänvalvojat voivat käyttää [Toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) työtilaa tarkistaakseen toiminnon tilan sekä laittaa sen päälle, jos sitä vaaditaan. Tässä tapauksessa toiminto näkyy seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Toiminnon nimi:** *Lähtevä lajittelu*

*Lähtevä lajittelu* -toimintoa voidaan käyttää yhdessä *Organisaationlaajuinen aallon vaihekoodi* -toiminnon kanssa, jos se on otettu käyttöön. Tämä toiminto on otettava käyttöön myös siinä tapauksessa, että käytät aallon vaihekoodeissa määritettäviä esimääritettyjä koodeja. **Ominaisuuksien hallinta** -työtilassa tämä ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Toiminnon nimi:** *Organisaationlaajuinen aallon vaihekoodi*

## <a name="setup"></a>Luo perustiedot

Tässä esittelyssä käytetään Contoso-vakiotietoja ja varastoa *62*. Lisäksi käytetään joitakin myöhemmin mainittavia lisäyksiä.

### <a name="location-type"></a>Sijainnin tyyppi

1. Valitse **Varastonhallinta \> Asetukset \> Varasto \> Sijaintityypit**.
1. Luo lajittelun sijaintityyppi valitsemalla toimintoruudussa **Uusi**.
1. Määritä seuraavat arvot:

    - **Sijaintityyppi:** *LAJITTELU*
    - **Kuvaus:** *Lajittelu*

1. Valitse **Tallenna**.

### <a name="warehouse-management-parameters"></a>Varastonhallinnan parametrit

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**.
1. Anna **Yleiset**-välilehden **Sijaintityypit**-pikavälilehden **Lajittelun sijaintityyppi** -kentän arvoksi *LAJITTELU*.
1. Valitse **Tallenna**.

### <a name="location-profile"></a>Sijaintiprofiili

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varasto \> Sijaintiprofiilit**.
1. Luo lajittelusijainnin sijaintiprofiili valitsemalla toimintoruudussa **Uusi**.
1. Aseta otsikkorivillä seuraavat arvot:

    - **Sijaintiprofiilin tunnus:** *Lajittelu*
    - **Nimi:** *Lajittelu*

1. Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:

    - **Sijainnin muoto:** *PAKKAUS*
    - **Sijaintityyppi:** *LAJITTELU*
    - **Käytä rekisterikilven seurantaa:** *Kyllä*
    - **Salli yhdistetyt nimikkeet:** *Kyllä*
    - **Salli yhdistetyt varastotilat:** *Kyllä*

1. Valitse **Tallenna**.

### <a name="locations"></a>Sijainnit

1. Valitse **Varastonhallinta \> Asetukset \> Varasto \> Sijainnit**.
1. Poista **Luo tarkistusnumeroita sijaintiin** -valintaruudun valinta.
1. Valitse toimintoruudussa **Uusi** ja määritä sitten seuraavat arvot:

    - **Varasto**: *62*
    - **Sijainti:** *Lajittelu*
    - **Sijaintiprofiilin tunnus:** *Lajittelu*

1. Valitse **Tallenna**.

### <a name="packing-profiles"></a>Pakkausprofiilit

1. Valitse **Varastonhallinta \> Asetukset \> Pakkaus \> Pakkausprofiilit**.
1. Valitse toimintoruudussa **Uusi** ja määritä sitten seuraavat arvot:

    - **Pakkausprofiilin tunnus:** *Lajitteli*
    - **Kuvaus:** *Lajittelu*
    - **Kontin pakkauskäytäntö:** jätä tämä kenttä tyhjäksi.
    - **Konttitunnuksen tila:** *Automaattinen*
    - **Kontin tyyppi:** *KUORMALAVA 48X48*
    - **Luo kontti automaattisesti kontin sulkemisessa:** jätä tämä kenttä tyhjäksi.

1. Valitse **Tallenna**.

### <a name="wave-step-codes"></a>Aallon vaihekoodit

Jos *Organisaationlaajuinen aallon vaihekoodi* -toiminto on otettu käyttöön, määritä seuraava koodi:

1. Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aallon vaihekoodit**.
1. Valitse toimintoruudussa **Uusi** ja määritä sitten seuraavat arvot:

    - **Aallon vaihekoodi:** *Lajittelu*
    - **Aallon vaihekuvaus:** *Lajittelu*
    - **Aalto vaihetyyppi:** *Lajittelumalli*

1. Valitse **Tallenna**.

### <a name="outbound-sorting-template"></a>Lähtevien lajittelumalli

Lajittelumalli määrittää, luodaanko lajittelupaikat, mitä ehtoja käytetään ja mitkä ovat lajitteluprosessin muut määritteet.

1. Valitse **Varastonhallinta \> Asetukset \> Pakkaus \> Lähtevä lajittelumalli**.
1. Valitse toimintoruudussa **Uusi** ja luo lajittelumalli.
1. Määritä uuden mallin ylätunnisteessa seuraavat arvot:

    - **Lähtevän lajittelumallin tunnus:** *Aaltolajittelu*
    - **Kuvaus:** *Aaltolajittelu*
    - **Lajittelumallin tyyppi:** *Aallon kysyntä*

        Tämä kenttä määrittää käsittelyn, jossa lajittelumallia käytetään. Käytettävissä ovat seuraavat arvot:

        - **Aallon kysyntä** – Lajittelumallia käytetään *Asettaminen seinälle* -prosessissa. Tätä mallityyppiä käytetään ohittamaan pakkausasema ja käsittelemään varastoa suoraan aallosta. Tätä tyyppiä voi käyttää vain, jos **lajittelu** sisältyy aallon käsittelymenetelmänä aaltomalliin.
        - **Kontti** – Tätä lajittelumallia käytetään *Kuormalavan luonti pakkauksen jälkeen* -prosessissa. Tätä mallityyppiä käytetään pakkausasemalla suljettujen ja kuormalavoille lajiteltavien konttien käsittelyyn.

    - **Varasto**: *62*
    - **Sijainti:** *Lajittelu*

1. Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:

    - **Lajittelun tarkistus:** *Sijainnin tarkistus*.

        Tämä kenttä määrittää lajittelun aikana tehtävän tarkistuksen. Käytettävissä ovat seuraavat arvot:

        - None
        - Rekisterikilven skannaus
        - Toimen skannaus

    - **Luo työ paikkaan suljettaessa:** *Kyllä*

        Jos tämän vaihtoehdon arvona on *Kyllä*, kun paikka luodaan, työ luodaan siirtämään varasto lopulliseen lähetyssijaintiin. Jos vaihtoehdon arvona on *Ei*, varasto kerätään tilaukseen heti, kun paikka suljetaan.

    - **Paikan määritys:** *Manuaalinen*

        Tämä kenttä määrittää paikan määrityksen tyypin. Käytettävissä ovat seuraavat arvot:

        - **Manuaalinen** – käyttäjän on aina ilmaistava, mihin paikkaan varasto lajitellaan.
        - **Automaattinen** – järjestelmä ohjaa mahdollisuuksien mukaan varaston automaattisesti paikkaan lajittelumallin keskeytysten perusteella.

    - **Määritä lajittelupaikan ehdot:** *Käytä vian tyhjää paikkaa*

        Tämä kenttää määrittää, otetaanko lajittelupaikoissa jo oleva varasto otetaan huomioon, kun paikka määritetään kysynnälle. Käytettävissä ovat seuraavat arvot:

        - **Käytä vain tyhjää paikkaa** – paikkoja, joihin on jo liitetty varastoa, ei oteta huomioon.
        - **Oletetaan paikka tyhjäksi** – Paikassa jo oleva varasto ohitetaan määrityksen aikana. Kaikkia käytettävissä olevia paikkoja käytetään.

    - **Aallon vaihekoodi:** *Lajittelu*

        Jos *Organisaationlaajuinen aallon vaihekoodi* -toiminto on otettu käyttöön, myös *Lajittelu*-aallon vaihekoodi on määritettävä aallon vaihekoodeissa.

    - **Sulje lajittelupaikka automaattisesti:** *Kyllä*

        Jos tässä vaihtoehdossa on valittu *Kyllä*, lajittelupaikka suljetaan automaattisesti, kun kaikki sijaintiin tulevat työt on suoritettu.

    - **Lajittelusijaintien määrä:** *3*

        Tämä kenttää määrittää suurimman lajittelupaikkojen määrän, jonka järjestelmän voi luoda.

    - **Lajittelupaikan etuliite:** *SP-*

        Tämä kenttää määrittää etuliitteen, jonka järjestelmä määrittää edeltämään paikkanumeroa.

    - **Pakkaa lajittelupaikka automaattisesti:** *Kyllä*

        Jos tämä vaihtoehto on *Kyllä*, lajittelupaikan varasto pakataan konttiin, kun paikka suljetaan.

    - **Pakkausprofiilin tunnus:** *Lajitteli*

        Tämä kenttä määrittää pakkausprofiilin, jota käytetään, kun lajittelupaikka pakataan konttiin.

1. Määritä tässä lajittelumallissa käytettävät ehdot valitsemalla toimintoruudussa **Muokkaa kyselyä**.
1. Lisää rivi valitsemalla kyselyn valintaikkunan **Lajittelu**-välilehdessä **Uusi** ja määritä sitten seuraavat arvot:

    - **Taulukko:** *Kuorman tiedot*
    - **Johdettu taulukko:** *Kuorman tiedot*
    - **Kenttä:** *Lähetyksen tunnus*
    - **Hakusuunta:** *Laskeva*

1. Valitse **OK**.
1. Näyttö voi tulla seuraava sanoma: Ryhmittely nollataan. Haluatko jatkaa?" Valitse **Kyllä**.

    **Lähtevän lajittelun mallivaihdot** -painike tulee näkyviin toimintoruudussa.

1. Valitse toimintoruudussa **Lähtevän lajittelun mallivaihdot**.
1. Käytä ryhmitykseen lähetyksen tunnusta valitsemalla **Ryhmittele kentän mukaan** -valintaruutu.

    Tämä asetus luo kullekin lähetykselle yhden sijainnin, joka on aallon kontti.

1. Valitse **OK**.

### <a name="wave-process-methods"></a>Aallon käsittelymenetelmät

1. Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aallon käsittelymenetelmät**.
1. Valitse toimintoruudussa **Luo menetelmät uudelleen**.

    **Lajittelumenetelmä** lisätään käytettävissä olevien menetelmien luetteloon ja sille valitaan *Lähetys*-aallon mallityyppi.

### <a name="wave-templates"></a>Aaltomallit

Muokkaa aallon kysynnän lajittelussa käytettävää aaltomallia.

1. Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aaltomallit**.
1. Valitse **Aaltomallin tyyppi** -kentässä *Lähetys*.
1. Valitse aiemmin luotu **62 Lähetysoletus** -malli.
1. Valitse toimintoruudussa **Muokkaa**.
1. Tee **Yleiset**-pikavälilehdessä seuraavat muutokset:

    - Määritä **Käsittele aalto, kun se vapautetaan varastoon** -asetuksen arvoksi *Ei*.
    - Määritä **Määritä avoimiin aaltoihin** -vaihtoehdon arvoksi *Kyllä*.

1. Määritä **Lajittelu**-menetelmä **Menetelmät**-pikavälilehdessä:

    1. Valitse **Jäljellä olevat menetelmät** -ruudukossa **lajittelu**.
    2. Siirrä **lajittelu**-menetelmä **Valitut menetelmät** -ruudukkoon oikealla nuolipainikkeella.
    3. Valitse **Valitut menetelmät** -ruudukossa **lajittelu**.
    4. Määritä **Aallon vaihekoodi** -kentän arvoksi *Lajittelu*.

1. Valitse **Tallenna**.

### <a name="mobile-device-menu-items"></a>Mobiililaitteen valikkovaihtoehdot

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Valitse toimintoruudussa **Uusi**.
1. Aseta otsikkorivillä seuraavat arvot:

    - **Valikkovaihtoehdon nimi:** *Lajittelu*
    - **Otsikko:** *Lajittelu*
    - **Tila:** *Epäsuora*
    - **Käytä aiemmin luotua työtä:** *Ei*

1. Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:

    - **Tehtäväkoodi:** *Lähtevä lajittelu*
    - **Käytä prosessiopasta:** *Kyllä* (oletusarvo)
    - **Lähtevän lajittelumallin tunnus:** *Aaltolajittelu*

1. Valitse **Tallenna**.

### <a name="mobile-device-menu"></a>Mobiililaitevalikko

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikko**.
1. Valitse valikkoluettelosta **Lähtevä**.
1. Valitse toimintoruudussa **Muokkaa**.
1. Etsi ja valitse **Käytettävissä olevat valikot ja valikkovaihtoehdot** -ruudukossa juuri luotu **Lajittelu**-valikkovaihtoehto.
1. Siirrä **Lajittelu** oikealla nuolipainikkeella **Valikon rakenne** -ruudukkoon. Voit lisätä tällä tavoin valikkovaihtoehdon **Lähtevä**-valikkoon.
1. Valitse **Tallenna**.

### <a name="location-directives"></a>Sijaintidirektiivit

Sijaintidirektiivejä on luotava ohjaamaan lajittelun valmistelun jälkeen luotua työtä.

1. Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.
1. Valitse **Työtilaustyyppi**-kentässä *Lajiteltu varastokeräily*.
1. Valitse toimintoruudussa **Uusi**.
1. Aseta otsikkorivillä seuraavat arvot:

    - **Järjestys:** *1*
    - **Nimi:** *Aseta lastausovelle*

1. Määritä **Sijaintidirektiivit**-pikavälilehdessä seuraavat arvot:

    - **Työtyyppi:** *Aseta*
    - **Toimipaikka:** *6*
    - **Varasto**: *62*
    - **Direktiivikoodi:** Jätä tämä kenttä tyhjäksi.
    - **Useita varastointiyksiköitä:** *Ei*

1. Valitse **Tallenna**, jos haluat, että **Rivit**-pikavälilehti on käytettävissä.
1. Valitse **Rivit**-pikavälilehdessä **Uusi** ja määritä sitten seuraavat arvot. Hyväksy kaikkien muiden kenttien oletusarvot.

    - **Järjestysnumero:** *1*
    - **Määrästä:** *0*
    - **Määrälle:** *1000000*

1. Valitse **Tallenna**, jos haluat, että **Paikkadirektiivitoimenpiteet**-pikavälilehti on käytettävissä.
1. Valitse **Sijaintidirektiivitoiminnot**-pikavälilehdessä **Uusi** ja määritä sitten seuraavat arvot. Hyväksy kaikkien muiden kenttien oletusarvot.

    - **Järjestysnumero:** *1*
    - **Nimi:** *Baydoor*

1. Valitse **Tallenna**, jos haluat, että **Sijaintidirektiivin toiminnot** -pikavälilehden **Muokkaa kyselyä** -painike on käytettävissä.
1. Valitse **Sijaintidirektiivitoiminnot**-pikavälilehdessä **Muokkaa kyselyä**.
1. Etsi kyselyeditorin valintaikkunan **Alue**-välilehdessä rivi, jonka **Kenttä**-kentän asetuksena on *Sijainti*. Määritä tämän rivin **Ehdot**-kentän arvoksi *Lastauspaikan ovi*.
1. Vahvista muokkaus valitsemalla **OK**.

### <a name="work-classes"></a>Työluokat

1. Valitse **Varastonhallinta \> Asetukset \> Työ \> Työluokka**.
1. Valitse toimintoruudussa **Uusi**.
1. Aseta otsikkorivillä seuraavat arvot:

    - **Työluokan tunnus:** *Lajittelu*
    - **Kuvaus:** *Lajittelu*
    - **Työtilauksen tyyppi:** *Lajiteltu varastokeräily*

1. Valitse **Tallenna**.

### <a name="work-templates"></a>Työmallit

1. Valitse **Varastonhallinta \> Työ \> Työmallit**.
1. Valitse **Työtilaustyyppi**-kentässä *Myyntitilaukset*.
1. Valitse ruudukossa **62 Kerää pakettiin** -työmalli.
1. Valitse toimintoruudussa **Työn otsikoiden katkaisut**.
1. Valitse toimintoruudussa **Muokkaa**.
1. Poista **Ryhmittele tämän kentän mukaan** -valintaruudun valinta sillä rivillä, jossa **Kentän nimi** -kentän asetuksena *Lähetyksen tunnus*.
1. Valitse **Tallenna** ja sulje sitten **Työn otsikoiden katkaisut** -valintaikkuna.
1. Valitse **Työtilaustyyppi**-kentässä *Lajiteltu varastokeräily*.
1. Luo työmalli valitsemalla **Uusi**.
1. Määritä **Yleiset**-osassa seuraavat arvot. Hyväksy kaikkien muiden kenttien oletusarvot.

    - **Työmalli:** *Lajiteltu keräily*
    - **Työmallin kuvaus:** *Lajiteltu keräily*

1. Valitse **Tallenna**, jos haluat, että **Työmallin tiedot** -osa on käytettävissä.
1. **Työmallin tiedot** -osassa luodaan kaksi riviä. Valitse **Uusi** ja määritä sitten seuraavat arvot riville 1:

    - **Työtyyppi:** *Poiminta*
    - **Pakollinen:** valittu (= *Kyllä*)
    - **Työluokan tunnus:** *Lajittelu*

1. Valitse **Uusi** uudelleen ja määritä sitten seuraavat arvot riville 2:

    - **Työtyyppi:** *Aseta*
    - **Pakollinen:** valittu (= *Kyllä*)
    - **Työluokan tunnus:** *Lajittelu*

1. Valitse **Tallenna**.

## <a name="example-scenario"></a>Esimerkkiskenaario

Tässä skenaariossa simuloidaan tilanne, jossa pieniä nimikkeitä varastoidaan varastossa sijainteihin ja jotka on pakattava laatikoihin ennen lähetystä, sekä tilannetta, johon pakkausasematoiminto ei sovi hyvin. Työntekijät keräävät samalla kertaa tilauksia useille asiakkaille ja eri osoitteisiin keräilyn nopeuttamiseksi. Kun keräily on valmis, työntekijät saapuvat lajittelusijaintiin, jossa kerätyt nimikkeet lajitellaan oikeaan laatikkoon vaadittujen ehtojen mukaisesti. Tässä esimerkissä oikea laatikko määritetään lähetyksen tunnuksen avulla, sillä jokaisella toimituksella on eri osoite. Kun kaikki kuorman nimikkeet on pakattu ja lajiteltu lähetyksen mukaan, laatikot siirretään valmistelualueelle ja lastataan lopuksi ajoneuvoon.

Varmista ennen tämän skenaarion aloittamista, että varaston kaikki vakiotoiminnot on määritetty oikein varastossa. Tätä tarkoitusta varten käytetään Contoson vakiovarastoa *62*. Vakiomäärityksiä ei ole muutettu lukuun ottamatta asetuksissa kuvattuja tilanteita.

### <a name="create-demand"></a>Luo kysyntää

Ennen kuin toimintoa voidaan esitellä, sitä varten on luotava kysyntää. Tässä skenaariossa luodaan kolme myyntitilausta kolmelle eri asiakkaalle. Tällä tavoin voidaan simuloida eri toimitusosoitteita. Tällä tavoin luoda kolme eri lähetystä.

Varmista ennen myyntitilausten ja lähetysten luontia, että keräilysijaintien varasto riittää kaikkien tilattujen nimikkeiden osalta. Vahvista myyntitilauksen keräilyssä käytetyt keräilysijainnit tarkistamalla sijaintidirektiivin asetukset. Jos sinun on muokattava varastoa, voit luoda manuaalisia siirtoja tai hyödyntää täydennystä tai mitä tahansa muuta virtausta. Varaa sitten varastoa.

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Luo tilauksen 1 myyntitilaus valitsemalla **Uusi**.
1. Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:

    - **Asiakas:** *US-001*
    - **Varasto**: *62*

1. Valitse **OK**.
1. **Myyntitilausrivit**-pikavälilehdelle lisätään uusi rivi. Määritä seuraavat arvot:

    - **Nimiketunnus:** *A0001*
    - **Määrä** *5*

1. Lisää toinen rivi valitsemalla **Lisää rivi** ja määritä seuraavat arvot:

    - **Nimiketunnus:** *A0002*
    - **Määrä** *10*

1. Varaa varastoa toistamalla seuraavat vaiheet tilauksen kunkin tilausrivin osalta:

    1. Valitse **Myyntitilausrivit**-pikavälilehdellä **Varasto**-valikosta **Varaus**.
    1. Valitse **Varaus**-sivulla **Varaa erä** ja sulje sitten sivu.
    1. Valitse **Tallenna**.

1. Luo tilauksen 2 myyntitilaus valitsemalla **Uusi**.
1. Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:

    - **Asiakas:** *US-004*
    - **Varasto**: *62*

1. Valitse **OK**.
1. **Myyntitilausrivit**-pikavälilehdelle lisätään uusi rivi. Määritä seuraavat arvot:

    - **Nimiketunnus:** *A0001*
    - **Määrä** *7*

1. Lisää toinen rivi valitsemalla **Lisää rivi** ja määritä seuraavat arvot:

    - **Nimiketunnus:** *A0002*
    - **Määrä** *3*

1. Varaa varastoa toistamalla seuraavat vaiheet tilauksen kunkin tilausrivin osalta:

    1. Valitse **Myyntitilausrivit**-pikavälilehdellä **Varasto**-valikosta **Varaus**.
    1. Valitse **Varaus**-sivulla **Varaa erä** ja sulje sitten sivu.
    1. Valitse **Tallenna**.

1. Luo tilauksen 3 myyntitilaus valitsemalla **Uusi**.
1. Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:

    - **Asiakas:** *US-007*
    - **Varasto**: *62*

1. Valitse **OK**.
1. **Myyntitilausrivit**-pikavälilehdelle lisätään uusi rivi. Määritä seuraavat arvot:

    - **Nimiketunnus:** *A0001*
    - **Määrä** *8*

1. Varaa myyntirivin mukainen varasto seuraavasti:

    1. Valitse **Myyntitilausrivit**-pikavälilehdellä **Varasto**-valikosta **Varaus**.
    1. Valitse **Varaus**-sivulla **Varaa erä** ja sulje sitten sivu.
    1. Valitse **Tallenna**.

Vapauta kukin myyntitilaus varastoon seuraavien ohjeiden mukaan. Erillisiä lähetyksiä luodaan kolme. Kaikki kolme lähetystä lisätään sitten yhteen uuteen aaltoon.

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Valitse ruudukossa ensimmäinen luotu myyntitilaus.
1. Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.

    Näyttöön tulevat tietosanomat ilmaisevat luodun aallon tunnuksen ja lähetyksen tunnuksen.

1. Vapauta myyntilaukset 2 ja 3 varastoon toistamalla edelliset vaiheet. Huomaa, että saamasi tietosanoma ilmaisee, aaltoon on lisätty lähetys, joka luotiin, kun myyntitilaus 1 vapautettiin.
1. Valitse **Varastonhallinta \> Lähtevät aallot \> Lähetysaallot \> Kaikki aallot**.
1. Avaa **Aallot**-sivu valitsemalla aallon tunnus, joka luotiin myyntitilausten vapauttamisesta. Aallon tiedot ovat tällä sivulla. Luodut lähetykset näkyvät **Aallon rivit** -pikavälilehdessä.

    Nyt on luotava työ, jolla nimikkeet tuodaan keräilysijainneista lajittelusijaintiin.

1. Valitse toimintoruudussa **Käsittely**.

    Lajittelumenetelmä määrittää aallon käsittelyn aikana varaston lajittelupaikkoihin lajittelumallien avulla. Kun aalto on käsitelty, avautuva tietosanoma ilmoittaa, että aalto on kirjattu ja työ on luotu.

1. Voit tarkastella luotua työtä valitsemalla toimintoruudun **Aalto**-välilehden **Liittyvät tiedot** -ryhmässä **Työ**. Kirjoita työn tunnus muistiin.
1. Valitse **Varastohallinta \> Pakkaus ja konttiinpakkaus \> Lähtevän lajittelupaikan määritykset**.
1. Vasemmassa sarakkeessa voi tarkastella kullekin lähetykselle luotua lähtevää lajittelupaikkaa.
1. Voit tarkastella **Lajittelupaikan ehdot** -pikavälilehdessä kyseisen paikan lähetystunnusta.

Yksi työtunnus on luotu tuomaan varasto keräilysijainneista lajittelusijaintiin. Työn viimeistelyyn tarvitaan työtunnus, joka luotiin aallon käsittelyn aikana.

### <a name="sales-order-picking-to-the-sorting-location"></a>Myyntitilauksen keräys lajittelusijaintiin

1. Kirjaudu mobiilisovellukseen työntekijänä varastossa *62*.
1. Valitse päävalikossa **Lähtevä**.
1. Valitse **Lähtevä**-valikossa **Myynnin keräily**.
1. Valitse **Tunnus**-kenttä ja anna sitten aallon käsittelystä saatu työtunnus.
1. Vahvista kirjaus.

    Seuraavaksi sinua pyydetään antamaan kohderekisterikilpi (RK). Huomaa, että myyntilauksen 1 rivi 1 ilmaisee, mitä on kerättävä ja lisättävä kohderekisterikilpeen. Näkyvissä on nimiketunnus, määrä, nimikkeen kuvaus ja keräilysijainti.

1. Anna kohderekisterikilpi **Kohde-RK**-kenttään.

    Voit kerätä kaikki käsitellystä aallosta luodut rivit samaan kohderekisterikilpeen.

1. Vahvista kirjaus.

    Mobiilisovelluksessa on nyt sarja **Keräily**-sivuja, jotka ohjaavat keräilysijaintiin sekä kerättävään nimikkeeseen ja keräysmäärään. Kun kerätty nimike on rekisterikilpeen, keräilytyö vahvistetaan. Viimeinen sivu on työ, jolla kerätyt nimikkeet asetetaan lajittelusijaintiin.

1. Vahvista ensimmäinen keräilytyö.
1. Seuraava keräilytyö näytetään. Vahvista keräily.
1. Jatka jäljellä olevan keräilytyön vahvistamiseen.
1. Viimeisenä vaiheena suoritetaan asettamistyö valmiiksi. Vahvista hyllytys lajittelusijaintiin.

    Näyttöön tulee Työ valmis -sanoma.

1. Lopeta **Myynnin keräily** mobiilisovelluksessa.

### <a name="sortingput-to-wall"></a>Lajittelu / asettaminen seinälle

Nyt kun varasto on asetettu lajittelusijaintiin, se on lajiteltava oikeaan lajittelupaikkaan.

1. Kirjaudu mobiilisovellukseen.
1. Valitse päävalikossa **Lähtevä**.
1. Aloita nimikkeiden lajittelu valitsemalla **Lähtevät**-valikossa **Lajittelu**.
1. Anna **Rekisterikilpi/kontti**-kentässä valitun myyntitilaustyön kohderekisterikilpi.
1. Vahvista kirjaus.
1. Anna ensimmäinen lajiteltava nimiketunnus.
1. Järjestelmä määrittää ensimmäisen näytettävän lajittelupaikan. Vahvista lajittelupaikka.
1. Sinua pyydetään määrittämään rekisterikilpi lajittelupaikkaan. Valitse **Rekisterikilpi**-kenttä, anna rekisterinumero ja vahvista merkintä sitten.

    Koska lajittelupaikka liittyy lähetyksen tunnukseen, kerätyt nimikkeet lajitellaan lähtevää lähetystä ja myyntitilausta koskevaan rekisterikilpeen.

    Seuraavalla sivulla näkyy nimiketunnus, määrä, lajittelupaikan tunnus sekä lähtevän (keräilyn) ja saapuvan (lajittelun) rekisterikilven tunnukset. Tämän sivut ohjaavat lajittelemaan määritetyn nimikkeen määrät keräilyn rekisterikilvestä lajittelun rekisterikilpeen.

1. Vahvista lajittelupaikka.
1. Lajittele ensimmäisen lajittelupaikan nimikkeet. Kun olet valmis, järjestelmä ohjaa sinut seuraavaan lajittelupaikkaan.
1. Toista tämä prosessi kaikkien työtilauksen keräiltyrivien osalta. Tässä prosessia on syytä käyttää myös silloin, kun useilla keräilyriveillä on sama nimiketunnus.

    Kun tämä prosessi toistetaan kaikkien nimikkeiden kohdalla, järjestelmä arvioi seuraavan luetun nimikkeen (työrivin) ehdot ja määrittää, mihin lajittelupaikkaan se asetetaan. Sinut ohjataan automaattisesti asettamaan nimike oikeaan lajittelupaikkaan. Vahvistuksen asetusten mukaan sinut ohjataan myös vahvistamaan tämä toiminto antamalla paikkanumero tai rekisterikilven tunnus.

    > [!NOTE]
    > Jos automaattinen lajittelu on otettu käyttöön, manuaalinen ohitus ei ole käytettävissä.

1. Kun olet valmis, tarkista paikkojen tila avaamalla Microsoft Dynamics 365 Supply Chain Managementissa **Lähtevät lajittelutoimimääritykset** -sivu.

    - Jos paikat on suljettu automaattisesti, tuo suljetut paikat näkyviin valitsemalla **Näytä suljetut**.
    - Huomaa, että lajittelupaikkatapahtumat ovat näkyvissä. Paikassa käsitelty nimi ja määrä näytetään.

    Kun määrität lähtevien lajittelumallin, **Sulje lajittelupaikka automaattisesti** -asetukseksi valitaan *Kyllä*. Tämän vuoksi paikka suljetaan automaattisesti, kun viimeinen odotettu varasto on asetettu siihen. Lajittelupaikkojen tila on **Suljettu** ja työ on luotu siirtämään lajiteltu varasto *Lastausovi*-sijaintiin.

1. Viimeistely lajiteltu varaston keräilytyö siirtämällä varasto lähetyssijaintiin. Kun varasto on valmis, tee sen lähetysvahvistus.

> [!NOTE]
> Lajitellun varaston keräilytyön käsittelemisen onnistuminen edellyttää, että mobiililaitteen valikkovaihtoehtoa, jossa työn luokkatunnuksen **Työtilauksen tyyppi** -kentäksi on valittu *Lajiteltu varaston keräily*, käytetään varastonsiirto- ja lastausprosessissa.

### <a name="manually-close-a-position-optional"></a>Paikan sulkeminen manuaalisesti (valinnainen)

Jos lajittelupaikat on suljettava manuaalisesti lähtevien lajittelumallin **Sulje lajittelupaikka automaattisesti** -asetuksena on oltava *Ei* ja sulkeminen on tehtävä, ennen kuin varastoa voidaan siirtää lastausovialueelle. Paikat voidaan sulkea eri tavoin:

- Varastonhallinnan mobiilisovelluksen kautta:

    - Käyttäjä voi lukea jonkin jo paikassa olevan nimikkeet ja sulkea sitten paikan valitsemalla **Sulje**.
    - Jos käyttäjä lukee kontin, joka on jo lajiteltu kontti, näyttöön tulee virhesanoma. Käyttäjä voi kuitenkin jatkaa paikan sulkemista.

- Microsoft Dynamics 365 Supply Chain Managementin **Lähtevät lajittelutoimimääritykset** -sivulla:

    - Käyttäjä voi valita ensin lähtevien lajittelupaikkatietueen ja sitten toimintoruudussa **Sulje paikka**.

## <a name="tips"></a>Vihjeitä

- Nimikkeitä ei voi siirtää paikkojen välillä sen jälkeen, kun ne on määritetty johonkin paikkaan. Järjestelmä arvioi, kuinka monta kappaletta kutakin nimikettä viedään tiettyyn paikkaan.
- Lajittelumalli voidaan määrittää luomaan kontit automaattisesti, kun paikat suljetaan. Tällä menetelmällä luodaan määritettyyn pakkausprofiiliin perustuva konttitunnuksen vakiorakenne.

> [!IMPORTANT]
> Kun varastosiirtotyö on luotu lajittelusijainnista, työtä ei saa peruuttaa. Muussa tapauksessa paikka ja kontit poistetaan järjestelmästä eikä niiden käsittely ole enää mahdollista. Myös varasto poistetaan.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]