---
title: Tuotedimensioiden yhdistäminen sijainnissa
description: Tässä ohjeaiheessa on tietoja tuotteiden useiden eri mittojen yhtäaikaisesta käytöstä samassa toimipaikassa. Tämä toimipaikkaprofiilin toiminto auttaa parantamaan toimipaikan varastonhallintaa, kun tuotteesta on varastossa useita variantteja tai tuotteiden ominaisuudet vaihtelevat, kuten muotiteollisuudessa. Sen avulla voit määrittää, voidaanko toimipaikkaprofiilissa sekoittaa tuotteita kokoonpanon, värin, tyylin ja värin mukaan vai voidaanko samassa toimipaikassa varastoida vain yhtä tietyn ominaisuuden tai ominaisuusyhdistelmän tuotetta.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 20085c51230d3ceca46c5119fecbc3cf3291ecd4
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578557"
---
# <a name="location-product-dimension-mixing"></a>Tuotedimensioiden yhdistäminen sijainnissa

[!include [banner](../includes/banner.md)]

Tuotedimensioiden yhdistäminen sijainnissa on toimipaikkaprofiilin toiminto, joka auttaa parantamaan toimipaikan varastonhallintaa, kun tuotteesta on varastossa useita variantteja tai tuotteiden mitat vaihtelevat, kuten muotiteollisuudessa. Sen avulla voit määrittää, voidaanko toimipaikkaprofiilissa sekoittaa tuotteita kokoonpanon, värin, tyylin ja värin mukaan vai voidaanko samassa toimipaikassa varastoida vain yhtä tietyn ominaisuuden tai ominaisuusyhdistelmän tuotetta.

## <a name="turn-on-the-location-product-dimension-mixing-feature"></a>Ota Tuotedimensioiden yhdistäminen sijainnissa käyttöön

Ennen kuin voit käyttää tuotedimensioiden sekoitusta, toiminnon pitää olla otettu käyttöön järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [Toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) työtilaa tarkistaakseen toiminnon tilan sekä laittaa sen päälle, jos sitä vaaditaan. Tässä tapauksessa toiminto näkyy seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Toiminnon nimi:** *Tuotedimensioiden yhdistäminen sijainnissa*

## <a name="setup"></a>Määritys

Jokaisella varastosijainnilla on oltava oma sijaintiprofiili, joka määrittää sijainnin ominaisuudet. Tämän vuoksi kaikissa samaa sijaintiprofiilia käyttävissä sijainneissa voidaan sallia tuotedimensioiden yhdistäminen, kun se on määritetty sijaintiprofiiliin.

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a>Salli tuotedimensioiden yhdistäminen määrittämällä sijaintiprofiilit

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varasto \> Sijaintiprofiilit**.
1. Valitse sijaintiprofiilien luettelosta **BULKKI**.
1. Valitse toimintoruudussa **Muokkaa**.
1. Määritä **Yleinen**-pikavälilehdessä **Ota käyttöön tuotedimensioiden yhdistäminen sijainnissa** -asetukseksi *Kyllä*.

    > [!NOTE]
    > Voit määrittää tämän asetuksen arvoksi *Kyllä* vain, jos **Salli yhdistetyt nimikkeet** -asetuksen arvoksi on määritetty *Ei*.

1. Määritä **Sallitut tuotedimensioiden yhdistämiset** -pikavälilehdessä asetuksen **Koko** arvoksi *Kyllä*. Tässä ohjeaiheessa kuvatussa skenaariossa voidaan yhdistää vain tuotteita, joiden **Koko**-dimensiot eroavat toisistaan. Myös muita asetuksia on käytettävissä.
1. Valitse **Tallenna**.

### <a name="create-a-new-product-master-and-product-variants"></a>Luo uusi päätuote ja tuotevariantit

1. Valitse **Tuotetietojen hallinta \> Tuotteet \> Päätuotteet**.
1. Valitse toimintoruudussa **Uusi** ja luo päätuote.
1. Aseta **Uusi tuote** -valintaikkunassa seuraavat arvot:

    - **Tuotetyyppi:** *Nimike*
    - **Tuotteen alatyyppi:** *Päätuote*
    - **Tuotenumero:** *B0001*
    - **Tuotenimi:** *B0001 Koko*
    - **Tuotedimensioryhmä:** *Koko*
    - **Määritysmenetelmä:** *Ennalta määritetty variantti*

1. Valitse **OK**.
1. Määritä **Tuotteen tiedot** -sivun **Yleinen**-pikavälilehdessä seuraavat arvot:

    - **Luo variantit automaattisesti:** *Kyllä*
    - **Kokoryhmä:** *CASUALDHIR*

1. Voit tarkastella ennalta määritettyjä variantteja valitsemalla toimintoruudussa **Tuotevariantit**.

    Näkyviin tulee **Tuotevariantit**-sivu, jossa näkyy luettelo kokoryhmälle määritetyistä varianteista.

### <a name="release-products-to-the-usmf-company"></a>Vapauta tuotteet USMF-yritykselle

1. Valitse toimintoruudussa **Vapauta tuotteet**.
1. Tarkista **Valitse vapautettavat tuotteet** -sivulla, että tuotenumero *B0001* on luettelossa ja valitse sitten **Seuraava**.
1. Vahvista vapautettavat tuotevariantit valitsemalla **Seuraava**.
1. Valitse **Valitse yritykset, joihin vapautetaan** -sivulla *USMF* ja vahvista valinta valitsemalla **Seuraava**.
1. Viimeistele vapauttaminen valitsemalla **Vahvista valinta** -sivulla **Valmis**.

    Näyttöön tulee Toiminto valmis -ilmoitus.

### <a name="update-a-released-product-in-the-usmf-company"></a>Vapautetun tuotteen päivittäminen USMF-yrityksessä

1. Varmista, että olet kirjautunut **USMF**-yritykseen.
1. Viimeistele vapautetun tuotteen luominen valitsemalla **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Etsi ja valitse nimikenumero *B0001*, joka avaa **Vapautetun tuotteen tiedot** -sivun.
1. Valitse toimintoruudussa **Muokkaa**.
1. Varmista **Yleinen**-pikavälilehdessä, että **Nimikemalliryhmä**-kentän arvoksi on määritetty *FIFO*.
1. Valitse toimintoruudun **Tuote**-välilehden **Asetukset**-ryhmässä **Dimensioryhmät**.
1. Määritä seuraavat arvot:

    - **Varastodimensioryhmä:** *Kauppatavara*
    - **Seurantadimensioryhmä:** *Ei mitään*

1. Valitse **OK**.
1. Valitse toimintoruudun **Tuote**-välilehden **Asetukset**-ryhmässä **Varaushierarkia**.
1. Määritä **Varaushierarkia**-kentän arvoksi *Oletus* ja valitse sitten **OK**.
1. Tarkista, että valintasi ovat päivittyneet **Yleinen**-pikavälilehden **Hallinta**-osaan.
1. Kirjoita **Osto**-pikavälilehden **Hinta** -kenttään *10*.
1. Kirjoita **Kustannusten hallinta** -pikavälilehden **Nimikeryhmä**-kenttään *Audio*.
1. Kirjoita **Osto**-pikavälilehden **Hinta** -kenttään *10*.
1. Kirjoita **Varasto**-pikavälilehden **Yksikön sarjaryhmän tunnus** -kenttään *ea*.
1. Valitse **Tallenna**.

### <a name="create-a-location-directive"></a>Luo toimipaikkadirektiivi

1. Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.
1. Valitse vasemman ruudun **Työtilaustyyppi**-kentässä *Ostotilaukset*.
1. Valitse luettelosta sijaintidirektiivi, jonka nimi on *24 PO Direct*.
1. Lisää uusi rivi ruudukkoon **Sijaintidirektiivin toiminnot** -pikavälilehdessä **Uusi**.
1. Määritä uudelle riville seuraavat arvot:

    - **Järjestysnumero:** *1*

        Uuden rivin on oltava aiemmin luodun rivin edessä. Voit tehdä muutoksen käyttämällä työkalurivin **Siirry ylös** - ja **Siirry alas** -painikkeita tai muuttamalla aiemmin luodun rivin **Järjestysnumero**-kentän arvoksi *2*.

    - **Nimi:** *Siirrä BULKKI-sijaintiprofiiliin*
    - **Kiinteän sijainnin käyttö:** *Kiinteät ja muut kuin kiinteät sijainnit*
    - **Salli negatiivinen varasto:** *Tyhjennä tämä valinta ruutu (= ei)*
    - **Erä käytössä:** *Tyhjennä tämä valinta ruutu (= ei)*
    - **Strategia:** *Ei mitään*

1. Kun uusi rivi on vielä valittuna, valitse ruudukon yläpuolelle **Muokkaa kyselyä**.
1. Lisää ruudukkoon rivi valitsemalla kyselyn valintaruudun **Alue**-välilehdessä **Lisää**.
1. Määritä uudelle riville seuraavat arvot:

    - **Taulu:** *Sijainnit*
    - **Johdettu taulu:** *Sijainnit*
    - **Kenttä:** *Sijaintiprofiilin tunnus*
    - **Kriteerit:** *BULKKI*

1. Valitse **OK**.
1. Valitse **Sijaintidirektiivit**-sivun toimintoruudussa **Tallenna**.

> [!NOTE]
> Jos käytät **Sijaintidirektiivin toiminnot** -pikavälilehden **Strategia**-kentässä asetusta *Konsolidoi*, **Sallitut tuotedimensioiden yhdistämiset** -välilehden **Sijaintiprofiilit**-asetus ohitetaan ja nimikkeet sijoitetaan samaan sijaintiin, vaikka tätä ei ole sallittu asetuksissa.

### <a name="create-a-mobile-device-menu-item"></a>Luo mobiililaitteen valikkovaihtoehto

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Luo lajitteluun käytettävä valikkonimike valitsemalla toimintoruudussa **Uusi**.
1. Aseta otsikkorivillä seuraavat arvot:

    - **Valikkokohteen nimi:** *Ostotilausrivien vastaanotto*
    - **Otsikko:** *Ostotilausrivien vastaanotto*
    - **Tila:** *Työ*
    - **Käytä aiemmin luotua työtä:** *Ei*

1. Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:

    - **Työn luomisprosessi:** *Ostotilausrivien vastaanotto ja hyllytys*
    - **Luo rekisterikilpi:** *Kyllä*

1. Valitse **Tallenna**.

### <a name="configure-the-mobile-device-menu"></a>Mobiililaitteen valikon määrittäminen

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikko**.
1. Valitse valikkoluettelosta **Saapuvat**.
1. Valitse toimintoruudussa **Muokkaa**.
1. Etsi ja valitse **Käytettävissä olevat valikot ja valikkokohteet** -luettelosta **Ostotilausrivien vastaanotto** -valikkokohta.
1. Siirrä **Ostotilausrivien vastaanotto** -valikkokohta **Valikkorakenne** -luetteloon painamalla oikeaa nuolipainiketta. Tällä tavoin voit lisätä uuden valikkokohdan valittuun valikkoon.
1. Valitse **Tallenna**.

## <a name="scenario"></a>Skenaario

Tässä esimerkkiskenaariossa esitellään, kuinka kaksi eri tuotevarianttia voidaan sijoittaa samaan sijaintiin, vaikka sijaintiprofiili ei salli yhdistettyjä nimikkeitä, mutta *Tuotedimensioiden yhdistäminen sijainnissa* -toiminto on käytössä. Tässä tapauksessa ehtona käytetään **Koko**-varianttia.

Varmista ennen aloittamista, että varastossa *24* on tyhjiä sijainteja, joissa käytetään *BULKKI*-sijaintiprofiilia.

### <a name="create-a-purchase-order"></a>Ostotilauksen luominen

Luot ostotilauksen, jossa on kolme riviä: kaksi riviä samalle tuotenumerolle, mutta eri **Koko**-varianteille, ja kolmas rivi eri tuotteelle, jolla ei ole variantteja.

1. Valitse **Ostoreskontra \> Ostotilaukset \> Kaikki ostotilaukset**.
1. Valitse toimintoruudussa **Uusi**.
1. Aseta **Luo ostotilaus** -valintaikkunassa seuraavat arvot:

    - **Toimittajan tili:** *1001*
    - **Varasto**: *24*

1. Valitse **OK**.
1. Ostotilaus luodaan ja uusi rivi lisätään **Ostotilausrivit**-pikavälilehteen. Kirjoita ostotilauksen numero muistiin.
1. Määritä uudelle riville seuraavat arvot:

    - **Nimiketunnus:** *B0001*
    - **Koko** *L*
    - **Määrä** *2*

1. Lisää toinen ostotilausrivi valitsemalla ruudukon yläpuolelta **Lisää rivi** ja määritä seuraavat arvot:

    - **Nimiketunnus:** *B0001*
    - **Koko** *XL*
    - **Määrä** *2*

1. Lisää kolmas ostotilausrivi valitsemalla **Lisää rivi** ja määritä seuraavat arvot:

    - **Nimiketunnus:** *A0001*
    - **Määrä** *1*

1. Valitse **Tallenna**.

### <a name="receive-purchase-order-lines-in-the-warehouse-management-mobile-app"></a>Ostotilausrivien vastaanottaminen varastonhallinnan mobiilisovelluksessa

1. Kirjaudu varastonhallinnan mobiilisovellukseen käyttäjänä, joka on otettu käyttöön varastolle *24*.
1. Valitse **Saapuvat**-valikko.
1. Valitse **Ostotilausrivien vastaanotto**.
1. Valitse **PUNUM**-kenttä ja syötä ostotilauksen numero.
1. Vahvista kirjaus valitsemalla Vahvista-painike (✔) sivun alareunasta.
1. Syötä vastaanotettavan ostotilauksen rivinumero. Valitse **LINENUM**-kenttä ja syötä numero näppäimistön avulla *1*.
1. Vahvista kirjaus.
1. Syötä vastaanotettava määrä. Paina plusmerkki ( **+**) -painiketta kaksi kertaa, jos haluat suurentaa **Määrä**-kentän arvon arvoon *2*.
1. Rekisteröi merkintäsi valitsemalla sivun alareunasta (✔) -painike ja vahvista sitten kirjaus valitsemalla painike (✔) uudelleen.
1. Tarkastele tietoja **Ostotilaukset: hyllytys** -sivulla. Tällä sivulla näkyvät hyllytystä varten luodut työt (työ 1).

    Näkyviin tulee sijainti, johon vastaanotettu nimike hyllytetään ja juuri valmiiksi saamasi **Ostotilausrivien vastaanotto** -tehtävän rekisterikilpi, nimike, koko ja määrä.

1. Vahvista hyllytystyö.
1. Toista vaiheet 4–11 ostotilausriville 2. Määritä kuitenkin vaiheessa 8 määräksi *1*.

    Uusi hyllytystyö (työ 2) luodaan samalle sijainnille kuin työ 1.

1. Toista vaiheet 4–11 uudelleen ostotilausriville 2. Määritä vaiheessa 8 jäljellä olevaksi määräksi *1*.

    Uusi hyllytystyö (työ 3) luodaan samalle sijainnille kuin työ 1 ja työ 2. Tämä aiheutuu siitä, että sijaintidirektiivin strategiaksi on asetettu *Konsolidoi* ja **Sallitut tuotedimensioiden yhdistämiset** -pikavälilehden *Bulkki* **Sijaintiprofiilit** -asetus mahdollistaa eri **Koko**-variantin nimikkeiden varastoimisen tähän sijaintiin.

1. Toista vaiheet 4–11 ostotilausriville 3. Määritä vaiheessa 8 nimikenumeron *A0001* määräksi *1*.

    Uusi hyllytystyö (työ 4) luodaan eri sijainnille kuin ostotilausriveille 1 ja 2 käytettävä sijainti. Näin käy, koska sijaintiprofiilissa ei sallita tuotteiden yhdistämistä, mutta saman päätuotteen eri dimensiot on sallittu.

1. Valitse sivun yläreunassa oleva valikkopainike (jota kutsutaan joskus nimellä hampurilainen tai Hamburger-painike) ja poistu **Ostotilausrivin vastaanotto** -tilasta valitsemalla **Peruuta**.

> [!TIP]
> Voit toistaa tämän skenaarion, mutta tällä kertaa määritä **Koko**-kentän arvoksi  - *Ei* **Salli tuotedimensioiden yhdistäminen**-pikavälilehden kohdassa *BULKKI* **Sijaintiprofiilit**, jolloin mitään tuotedimensioita ei voi varastoida samaan sijaintiin. Tällöin kun vastaanotat ostotilauksen, jokainen tuotevariantti sijoitetaan uuteen sijaintiin.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]