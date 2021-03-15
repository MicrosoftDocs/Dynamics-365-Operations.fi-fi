---
title: Toimipaikan rekisterikilpien paikannus
description: Toimipaikan rekisterikilpien paikannuksen avulla voit nähdä, missä rekisterikilpi sijaitsee monilavaisessa kokoonpanossa, kuten paikoissa, joissa käytetään syviä lavahyllyjä.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlate, WHSLocationProfile, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6d94d37368b8fc3ff7dbe4c1845acd52bf2a64ee
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004674"
---
# <a name="location-license-plate-positioning"></a>Toimipaikan rekisterikilpien paikannus

[!include [banner](../includes/banner.md)]

Toimipaikan rekisterikilpien paikannuksen avulla voit nähdä, missä rekisterikilpi sijaitsee monilavaisessa kokoonpanossa, kuten paikoissa, joissa käytetään syviä lavahyllyjä.

Toiminto lisää järjestysnumeron kuhunkin varastointipaikkaan sijoitettavaan rekisterikilpeen. Tämän järjestysnumeron avulla voidaan tilata varastointipaikkaan rekisterikilpiä. Niinpä toiminto tukee älykkäästi tilanteita, joissa asiakkaan käyttävät painovoimaan perustuvaa hyllyjärjestelmää ja heidän on tavaroiden varastosta noutoa varten tiedettävä, mikä rekisterikilpi näkyy pakkauksen edestä päin.

Tässä aiheessa esitellään esimerkkitilanne tämän toiminnon määrittämisestä ja käytöstä.

## <a name="turn-on-the-location-license-plate-positioning-feature"></a>Ota Toimipaikan rekisterikilpien paikannustoiminto käyttöön

Ennen kuin voit käyttää rekisterikilpien paikannusta, toiminnon pitää olla otettu käyttöön järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [Toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) työtilaa tarkistaakseen toiminnon tilan sekä laittaa sen päälle, jos sitä vaaditaan. Tässä tapauksessa toiminto näkyy seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Toiminnon nimi:** *Toimipaikan rekisterikilpien paikannus*

## <a name="example-scenario"></a>Esimerkkiskenaario

### <a name="make-sample-data-available"></a>Ota mallitiedot käyttöön

Jos haluat käsitellä tätä skenaariota käyttämällä tässä ehdotettuja arvoja, sinun on työskenneltävä järjestelmässä, johon on asennettu mallitiedot. Sinun on myös valittava **USMF**-yritys ennen aloittamista.

### <a name="set-up-the-feature-for-this-scenario"></a>Määritä toiminto tälle skenaariolle

Määritä *Toimipaikan rekisterikilpien paikannus* tässä aiheessa käsiteltävää skenaariota varten suorittamalla seuraavassa esitetyt toimenpiteet.

#### <a name="location-profiles"></a>Sijaintiprofiilit

Toiminto on otettava käyttöön kaikkien niiden toimipaikkojen sijaintiprofiileissa, joissa toimintoa käytetään.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varasto \> Sijaintiprofiilit**.
1. Valitse vasemmassa ruudussa olevasta sijaintiprofiilien luettelosta **BULKKI-06**.
1. **Yleinen**-pikavälilehdessä näkyviin tulee kaksi uutta vaihtoehtoa toiminnon viereen. Määritä seuraavat arvot:

    - **Ota rekisterikilven paikannus käyttöön:** *Kyllä*

        Kun tämä asetus on *Kyllä*, rekisterikilven sijainti pidetään samana kaikille toimipaikan rekisterikilville.

    - **Näytä mobiililaitteen LP-asema:** *Kyllä*

        Kun tämä asetus on *Kyllä*, rekisterikilven sijainti näkyy mobiililaitteen käyttäjille kilven säädön ja laskennan aikana. Voit muuttaa tätä asetusta vain, kun toiminto on käytössä.

1. Valitse **Tallenna**.

#### <a name="location-directives"></a>Sijaintidirektiivit

1. Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.
1. Varmista, että vasemman ruudun **Työtilauksen tyyppi** -kentän arvo on *Myyntitilaukset*.
1. Valitse sijaintidirektiivien luettelosta **61 SO tilauksen kerääminen**.
1. Valitse toimintoruudussa **Muokkaa**.
1. Valitse **Rivit**-pikavälilehdessä rivi, jonka **Järjestysluku** on *2*.
1. Valitse **Sijaintidirektiivin toiminnot** -pikavälilehdessä rivi, jonka **Nimi**-arvo on *Keräys, kun < kuormalava* (tämän pitäisi olla ainoa rivi), ja muuta sen **Järjestysnumeron** arvoksi *2*.
1. Lisää uusi sijaintidirektiivin toiminto valitsemalla yllä olevassa ruudukossa kohta **Uusi**.
1. Määritä uudelle riville seuraavat arvot:

    - **Järjestysnumero:** *1*
    - **Nimi:** *Keräilysijainti 1*

1. Kun uusi rivi on vielä valittuna, valitse ruudukon yläpuolelle **Muokkaa kyselyä**.
1. Valitse **Liitokset**-väli lehti kyselyeditorissa.
1. Laajenna **Toimipaikat**-taulun liitos niin, että se tuo näkyviin **Varaston dimensiot** -taulun liitokset.
1. Laajenna **Varaston dimensiot**-taulun liitos niin, että se tuo näkyviin **Käytettävissä oleva varasto** -taulun liitokset.
1. Valitse **Varaston dimensiot** ja valitse sitten **Lisää taulun liitos**.
1. Valitse näyttöön tulevan taululuettelon **Suhde**-sarakkeesta **Rekisterikilpi (Rekisterikilpi)**. Lisää sitten kohta **Rekisterikilpi** taulukon **Varaston dimensiot** liitokseen valitsemalla **Valitse**.
1. Kun **Rekisterikilpi** on valittuna, valitse **Lisää taulun liitos**.
1. Valitse näyttöön tulevan taululuettelon **Suhde**-sarakkeesta **Toimipaikan rekisterikilpien paikannus (Rekisterikilpi)**. Lisää sitten kohta **Toimipaikan rekisterikilpien paikannus** taulukon **Varaston dimensiot** liitokseen valitsemalla **Valitse**.

    ![Taulun liitokset](media/LpTableJoin.png "Taulun liitokset")

1. Vahvista päivitetyt liitetyt taulut valitsemalla **OK** ja sulje kyselyeditori.
1. Avaa kyselyeditori uudelleen valitsemalla **Sijaintidirektiivin toiminnot** -pikavälilehdessä **Muokkaa kyselyä**.
1. Valitse **Alue**-välilehdessä **Lisää**, jos haluat lisätä uuden rivin ruudukkoon.
1. Määritä uudelle riville seuraavat arvot:

    - **Taulukko:** *Toimipaikan rekisterikilpien paikannus*
    - **Johdettu taulukko:** *Toimipaikan rekisterikilpien paikannus*
    - **Kenttä:** *LP-sijainti*
    - **Ehdot:** *1*

    ![Uusi alue](media/LpPositionCriteria.png "Uusi alue")

1. Vahvista muutokset valitsemalla **OK** ja sulje kyselyeditori.

### <a name="set-up-sample-data-for-this-scenario"></a>Mallitietojen määrittäminen tälle skenaariolle

Tässä skenaariossa käyttäjän on kirjauduttava varastoinnin mobiilisovellukseen työntekijänä, joka on määritetty työskentelemään varastolla *61*. Myös käyttäjän on suoritettava tapahtumia.

Koska *Toimipaikan rekisterikilven paikannus* -toiminto lisää uuden tunnisteen rekisterikilpien paikoille toimipaikoissa, sinun on ensin luotava joitakin tietoja skenaarion tueksi.

#### <a name="spot-count-the-first-location"></a>Ensimmäisen sijainnin pisteinventointi

1. Avaa in varastointisovellus ja kirjaudu siihen varastossa *61*.
1. Siirry kohtaan **Varasto \>Pisteinventointi**.
1. Aseta **Pisteinventointi**-sivulla kentän **Sijainti** arvoksi *01A01R1S1B*.
1. Valitse **OK**.

    Sivulla näkyy antamasi sijainti. Sivulla näkyy myös seuraava viesti: "Sijainti valmis, lisätäänkö uusi LP tai nimike?"

1. Lisää luku sijaintiin valitsemalla **Päivitä**.
1. Valitse **Syklin laskenta: Lisää uusi LP tai nimike** -sivulla **Nimike**-kenttä ja kirjoita siihen arvo *A0001*.
1. Valitse **OK**.
1. Valitse **Syklin laskenta: Lisää uusi LP tai nimike** -sivulla **LP**-kenttä ja kirjoita siihen arvo *LP1001* (tai mikä tahansa muu haluamasi rekisterinumero).

    **Syklin laskenta: Lisää uusi LP tai nimike** -sivulla näkyy **Rekisterikilven sijainti 1**.

1. Valitse **OK**.

    Sinun on nyt asetettava rekisterikilvessä mainittujen nimikkeiden lukumäärä.

1. Aseta **Määrä**-kentän arvoksi *10*.
1. Valitse **OK**.

    Sivulla näkyy antamasi sijainti. Sivulla näkyy myös seuraava viesti: "Sijainti valmis, lisätäänkö uusi LP tai nimike?"

1. Lisää toinen luku sijaintiin valitsemalla **Päivitä**.
1. Valitse **Syklin laskenta: Lisää uusi LP tai nimike** -sivulla **Nimike**-kenttä ja kirjoita siihen arvo *A0002*.
1. Valitse **OK**.
1. Valitse **Syklin laskenta: Lisää uusi LP tai nimike** -sivulla **LP**-kenttä ja kirjoita sitten arvo *LP1002* (tai mikä tahansa muu haluamasi rekisterinumero, joka eroaa aiemmin määrittämästäsi rekisterinumerosta).
1. Muuta rekisterikilven paikkaa asettamalla **LP-sijainti**-kentän arvoksi *2*.
1. Valitse **OK**.
1. Määritä rekisterikilvessä mainittujen nimikkeiden lukumäärä asettamalla **Määrä**-kentän arvoksi *10*.
1. Valitse **OK**.

    Sivulla näkyy antamasi sijainti. Sivulla näkyy myös seuraava viesti: "Sijainti valmis, lisätäänkö uusi LP tai nimike?"

1. Valitse **OK**.

Työ on nyt valmis.

#### <a name="spot-count-the-second-location"></a>Toisen sijainnin pisteinventointi

1. Aseta **Pisteinventointi**-sivulla kentän **Sijainti** arvoksi *01A01R1S2B*.
1. Valitse **OK**.

    Sivulla näkyy antamasi sijainti. Sivulla näkyy myös seuraava viesti: "Sijainti valmis, lisätäänkö uusi LP tai nimike?"

1. Lisää luku sijaintiin valitsemalla **Päivitä**.
1. Valitse **Syklin laskenta: Lisää uusi LP tai nimike** -sivulla **Nimike**-kenttä ja kirjoita siihen arvo *A0002*.
1. Valitse **OK**.
1. Valitse **Syklin laskenta: Lisää uusi LP tai nimike** -sivulla **LP**-kenttä ja kirjoita sitten arvo *LP1003* (tai mikä tahansa muu haluamasi rekisterinumero, joka eroaa aiemmassa toimenpiteessä määrittämistäsi rekisterinumeroista).

    **Syklin laskenta: Lisää uusi LP tai nimike** -sivulla näkyy **Rekisterikilven sijainti 1**.

1. Valitse **OK**.
1. Määritä rekisterikilvessä mainittujen nimikkeiden lukumäärä asettamalla **Määrä**-kentän arvoksi *10*.
1. Valitse **OK**.

    Sivulla näkyy antamasi sijainti. Sivulla näkyy myös seuraava viesti: "Sijainti valmis, lisätäänkö uusi LP tai nimike?"

1. Valitse **OK**.

Työ on nyt valmis.

#### <a name="work-details"></a>Työn tiedot

> [!NOTE]
> Mobiilisovelluksen pisteinventoinnit luovat inventoinnin arvoksi Microsoft Dynamics 365. Työ edellyttää, että inventoinnit hyväksytään, ennen kuin ne kirjataan varastoon.

1. Kirjaudu sisään Dynamics 365 Supply Chain Management -järjestelmään.
1. Valitse **Varastonhallinta \> Työ \> Työn tiedot**.
1. Etsi **Yleiskatsaus**-välilehdestä rivit, joilla on seuraavat arvot:

    - **Työtilauksen tyyppi:** *Inventointi*
    - **Varasto**: *61*
    - **Työn tila:** *Odottaa arvostelua*

    Näille riveille pitäisi olla luotuna kaksi työtunnusta. Näiden molempien työtunnusten määrät on hyväksyttävä.

1. Valitse ruudukossa ensimmäinen työtunnus *Inventointi*-työtilauksen tyypiksi.
1. Valitse toimintoruudun **Työ**-välilehden **Työ**-ryhmässä **Inventointi**.

    Näkyviin tulee kaksi riviä, yksi kullekin nimikkeelle ja rekisterikilvelle. **Inventoitu määrä**-, **Toimipiste**-, **Rekisterikilpi**- ja **Nimike**-kenttien arvojen on vastattava mobiililaitteella luotuja arvoja. Jos jokin näistä kentistä ei ole näkyvissä, lisää ne ruudukkoon valitsemalla toimintoruudussa **Näytä dimensiot**.

1. Valitse molemmat rivit.
1. Valitse toimintoruudussa **Hyväksy määrä**.
1. Näyttöön tulee viesti "Lähetetään – kirjauskansio". Voit tarkastella kirjattua kirjauskansion numeroa valitsemalla **Viestin tiedot**.
1. Sulje viestin tiedot.
1. Päivitä **Työ**-sivu.

    Ensimmäinen työtunnus on suljettu, eikä se enää näy.

    > [!TIP]
    > Jos haluat tarkastella suljettua työtä, valitse ruudukon yläpuolella oleva **Näytä suljetut** -valintaruutu.

    Voit nyt hyväksyä työn rekisterikilvelle toimipaikassa *01A01R1S2B*.

1. Valitse **Yleiskatsaus**-välilehdessä toinen työtunnus *Inventointi* -työtilauksen tyypiksi.
1. Valitse toimintoruudun **Työ**-välilehden **Työ**-ryhmässä **Inventointi**.

    Näkyviin tulee yksi rivi, jossa on nimike ja rekisterikilpi. **Inventoitu määrä**-, **Toimipiste**-, **Rekisterikilpi**- ja **Nimike**-kenttien arvojen on vastattava mobiililaitteella luotuja arvoja.

1. Valitse rivi.
1. Valitse toimintoruudussa **Hyväksy määrä**.
1. Näyttöön tulee viesti "Lähetetään – kirjauskansio". Voit tarkastella kirjattua kirjauskansion numeroa valitsemalla **Viestin tiedot**.
1. Sulje viestin tiedot.
1. Päivitä **Työ**-sivu.

    Toinen työtunnus on suljettu, eikä se enää näy.

    > [!TIP]
    > Jos haluat tarkastella suljettua työtä, valitse ruudukon yläpuolella oleva **Näytä suljetut** -valintaruutu.

#### <a name="on-hand-by-location"></a>Varastosaldo sijainnin mukaan

1. Siirry kohtaan **Varastonhallinta \> Kyselyt ja raportit \> Varastosaldo sijainnin mukaan**.
1. Määritä seuraavat arvot:

    - **Toimipaikka:** *6*
    - **Varasto**: *61*
    - **Päivitä kaikissa sijainneissa:** *Kyllä*

1. Huomaa, että toimipaikassa *01A01R1S1B* on käytössä kaksi rekisterikilpeä:

    - **A0001**, jossa **LP-sijainti**-kentän arvo on *1*
    - **A0002**, jossa **LP-sijainti**-kentän arvo on *2*

1. Huomaa, että toimipaikassa *01A01R1S2B* on käytössä yksi rekisterikilpi:

    - **A0002**, jossa **LP-sijainti**-kentän arvo on *1*

### <a name="sales-order-scenario"></a>Myyntitilausskenaario

Kun *Toimipaikan rekisterikilven paikannus* -toiminto on määritetty ja varasto on vaiheistettu, luo myyntitilaus, joka luo keräilytyön, jossa varastotyöntekijä kerää nimikkeen *A0002* varastopaikasta, jossa kuormalavan tunnus on paikassa *1*.

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Valitse toimintoruudussa **Uusi**.
1. Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:

    - **Asiakastili:** *US-004*
    - **Varasto**: *61*

1. Valitse **OK**.
1. **Myyntitilausrivit**-pikavälilehden ruudukkoon lisätään uusi rivi. Määritä tälle uudelle riville seuraavat arvot:

    - **Nimiketunnus:** *A0002*
    - **Määrä** *1*

1. Valitse ruudukon yläpuolella olevasta **Varasto**-valikosta kohta **Varaus**.
1. Varaa varastossa olevat nimikkeet tilausriviä varten **Varaus**-sivun toimintoruudussa valitsemalla **Varaa erä**.
1. Sulje **Varaus**-sivu.
1. Valitse toimintoruudussa **Varasto**-välilehden **Toiminnot**-ryhmässä **Vapauta varastoon**.

    Näyttöön tulee tiedote, jossa kerrotaan, että tilaukselle on luotu aallon tunnus ja lähetystunnus.

1. Valitse **Myyntitilausrivit**-pikavälilehden ruudukon yläpuolella olevasta **Varasto**-valikosta **Työn tiedot**.
1. Näkyviin tulee **Työ**-sivu, jossa näkyy myyntiriville luotu työ. Kirjoita näytössä näkyvä työn tunnus muistiin.

### <a name="sales-picking-scenario"></a>Myynnin keräilyskenaario

1. Avaa mobiilisovellus ja varastoon *61*.
1. Siirry kohtaan **Lähtevän \>myynnin keräys**.
1. Valitse **Skannaa työn tunnus/rekisterikilven tunnus** sivulla **Tunnus**-kenttä ja kirjoita siihen työn tunnus myyntiriviltä.
1. Huomaa, että keräystyö ohjaa sinut keräämään nimikkeen *A0002* toimipaikasta *01A01R1S2B*. Tämä ohje tulee näyttöön, koska nimike *A0002* on kirjattu rekisterikilpeen, joka on tämän toimipaikan sijainnissa *1*.

    ![Sijainti 1 toimipaikassa](media/LocationLicensePlatePositioning.png "Sijainti 1 toimipaikassa")

1. Kirjoita toimipaikalle luomasi rekisterikilven tunnus ja kerää myyntitilaus noudattamalla kehotteita.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]