---
title: Lähtevien lajittelu
description: Tässä artikkelissa on tietoja lähtevien lajittelusta. Tämä toiminto helpottaa pienien konttien käsittelyä ja auttaa varastotyöntekijöitä parantamaan kuorma-auton kuormalavakapasiteetin suunnittelua ja järjestämistä.
author: Mirzaab
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSPack, WHSOutboundSortTemplate, WHSOutboundSortPositionAssignments, WHSLocationType, WHSLoactionProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: ec7bc573329a0f8a37b2fd17dcb998ec161b04e8
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336332"
---
# <a name="outbound-sorting"></a>Lähtevä lajittelu

[!include [banner](../includes/banner.md)]

Tämä toiminto helpottaa pienien konttien käsittelyä ja auttaa varastotyöntekijöitä parantamaan kuorma-auton kuormalavakapasiteetin suunnittelua ja järjestämistä. Lähtevää lajittelua käytettäessä pakatut kontit voidaan lajitella oikealle kuormalavalle pakkausasemalta. Myös pakkaushierarkia voidaan luoda.

Tämän toiminnon avulla pakatuista konteista voidaan luoda kuormalavoja pakkaustoiminnolla. Konttia ei lähetetä lopulliseen toimitussijaintiin, sillä se on alkuperäisessä pakkaustyönkulussa. Työntekijät voivat sen sijaan sulkea kontin ja siirtää sen lajittelutyypin sijaintiin. He voivat sitten lajitella kontit paikkoihin, joissa kussakin on rekisterikilpi (RK). Konttien lajittelemisen jälkeen voidaan luoda työ, jolla koko rekisterikilpi lähetetään lopulliselle lähetyslaiturille tai väliaikaisiin sijainteihin sijaintidirektiivien tai omien tarpeiden mukaan. Lisäksi lajittelupaikan sulkeminen siirtää varaston heti lopulliselle lähetyslaiturille tilaukseen kerättäväksi.

## <a name="turn-on-the-outbound-sorting-feature"></a>Lähtevän lajittelutoiminnon ottaminen käyttöön

Ennen kuin käytät toimintoa, se on otettava käyttöön järjestelmässä. Järjestelmänvalvojat voivat käyttää [Toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) työtilaa tarkistaakseen toiminnon tilan sekä laittaa sen päälle, jos sitä vaaditaan. Tässä tapauksessa toiminto näkyy seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Toiminnon nimi:** *Lähtevä lajittelu*

## <a name="setup"></a>Määritys

Tässä skenaariossa on käytettävä **USMF**-vakioesittelytietoja ja varastoa *62*. Lisäksi on suoritettava seuraavissa alaosioissa käsitellyt määritykset.

### <a name="set-up-a-wave-template"></a>Aaltomallin asetuksien määrittäminen

Tämä määritys käsittelee automaattisesti aallon ja luoda työn, kun rivi vapautetaan varastoon.

1. Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aaltomallit**.
1. Valitse malliluettelossa **Varasto 62**.
1. Varmista **Yleiset**-pikavälilehdessä, että **Käsittele aalto, kun se vapautetaan varastoon** -vaihtoehtona on *Kyllä*.

### <a name="set-up-a-worker"></a>Työntekijän määrittäminen

Pakkausasemaa pidetään sijaintina. Pakkausasemaan kirjautuvat varastotyöntekijät näkevät ja voivat käsitellä vain kyseiseen pakkaussijaintiin suunniteltuja lähetyksiä ja kontteja. Microsoft Dynamics 365:n kirjautuvan käyttäjän on oltava määritetty työntekijäksi varastonhallinnassa. Jos käyttäjän nimi ei ole työn käyttäjäluettelossa, lisää se käyttämällä seuraavaa menettelyä.

> [!NOTE]
> Näissä ohjeissa oletetaan, että käyttäjä on jo järjestelmässä ja että hänet on liitetty omana työntekijänä tai työntekijänä **Human Resources** -moduulissa.

1. Valitse **Varastonhallinta \> Asetukset \> Työntekijä**.
1. Valitse **Uusi**.
1. Valitse **Työntekijä**-kentässä kohdekäyttäjä työntekijäluettelossa.
1. Valitse **Valitse**.
1. Valitse toimintoruudussa **Tallenna**.
1. Luo mobiililaitetili valitsemalla **Käyttäjät**-pikavälilehdessä **Uusi** ja määritä sille seuraavat arvot:

    - **Käyttäjätunnus:** anna yksilöivä tunnus.
    - **Käyttäjänimi:** anna tunnukselle nimi.
    - **Oletusvarasto:** *62*
    - **Valikon nimi:** *Pää*

1. Valitse toimintoruudussa **Tallenna**.
1. Voit luoda avautuvassa **Määritä salasana** -valintaikkunassa yksinkertaisen salasanan, jolla käyttäjä voi kirjautua mobiilisovellukseen. Määritä seuraavat arvot:

    - **Salasana:** anna yksinkertainen salasana.
    - **Vahvista salasana:** anna sama salasana uudelleen.

1. Valitse **Määritä salasana**.

    Toimintokeskuksessa on ilmoitus, joka ilmaisee, että luodulle käyttäjälle on määritetty salasana.

### <a name="create-a-location-type"></a>Sijaintityypin luonti

1. Valitse **Varastonhallinta \> Asetukset \> Varasto \> Sijaintityypit**.
1. Luo sijaintityyppi valitsemalla toimintoruudussa **Uusi** ja määritä sille seuraavat arvot:

    - **Sijaintityyppi:** *LAJITTELU*
    - **Kuvaus:** *Lajittelu*

1. Valitse toimintoruudussa **Tallenna**.

### <a name="set-up-warehouse-management-parameters"></a>Varastonhallinnan parametrien määrittäminen

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**.
1. Valitse **Yleiset**-välilehden **Sijaintityypit**-pikavälilehden **Lajittelun sijaintityyppi** -kentän arvoksi *LAJITTELU*.
1. Valitse toimintoruudussa **Tallenna**.

### <a name="set-up-a-location-profile"></a>Sijaintiprofiilin määrittäminen

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varasto \> Sijaintiprofiilit**.
1. Valitse toimintoruudussa **Uusi**.
1. Aseta otsikkorivillä seuraavat arvot:

    - **Sijaintiprofiilin tunnus:** *Lajittelu*
    - **Nimi:** *Lajittelu*

1. Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:

    - **Sijainnin muoto:** *ASRB* (käytävä-teline-hylly-lokero)
    - **Sijaintityyppi:** *LAJITTELU*
    - **Käytä rekisterikilven seurantaa:** *Kyllä*
    - **Salli yhdistetyt nimikkeet:** *Kyllä* (Kun arvoksi valitaan *Kyllä*, **Salli yhdistetyt varastoerät** -asetukseksi määritetään automaattisesti *Kyllä* eikä tätä asetusta voi muuttaa erikseen.)

1. Valitse **Tallenna**.

### <a name="set-up-a-location"></a>Sijainnin määrittäminen

1. Valitse **Varastonhallinta \> Asetukset \> Varasto \> Sijainnit**.
1. Poista ylätunnisteessa **Luo tarkistusnumeroita sijaintiin** -valintaruudun valinta.
1. Luo sijainti valitsemalla toimintoruudussa **Uusi** ja määritä sille seuraavat arvot:

    - **Varasto**: *62*
    - **Sijainti:** *SORT*
    - **Sijaintiprofiilin tunnus:** *LAJITTELU*

1. Valitse **Tallenna**.

### <a name="set-up-an-outbound-sorting-template"></a>Lähtevän lajittelumallin määrittäminen

Lähtevä lajittelumalli määrittää, luodaanko työ lajittelusijainnin ulkopuolella ja tehdäänkö lajittelu manuaalisesti vai automaattisesti.

Tässä skenaariossa luodaan lähtevä lajittelumalli luomaan kuormalavat pakkausaseman jälkeen.

1. Valitse **Varastonhallinta \> Asetukset \> Pakkaus \> Lähtevät lajittelumallit**.
1. Valitse toimintoruudussa **Uusi**.
1. Määritä uuden mallin ylätunnisteessa seuraavat arvot:

    - **Lähtevän lajittelumallin tunnus:** *AutoWork*
    - **Kuvaus:** *Automaattisen työn luonti*
    - **Lähtevän lajittelumallin tyyppi:** *Kontti*
    - **Varasto**: *62*
    - **Sijainti:** *SORT*

1. Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:

    - **Lajittelun tarkistus:** *Sijainnin tarkistus*.
    - **Luo työ paikkaan suljettaessa:** *Kyllä*

        Jos tämän vaihtoehdon arvona on *Kyllä*, kun paikka luodaan, työ luodaan siirtämään varasto lopulliseen lähetyssijaintiin. Jos vaihtoehdon arvona on *Ei*, varasto kerätään tilaukseen heti, kun paikka suljetaan.

    - **Paikan määritys:** *Automaattinen*

        Jos kentässä on valittu *Manuaalinen*, käyttäjän on aina ilmaistava, mihin paikkaan varasto lajitellaan. Jos kentässä on valittu *Automaattinen*, järjestelmä ohjaa mahdollisuuksien mukaan varaston automaattisesti sijaintiin lajittelumallin taukojen perusteella.

1. Valitse **Tallenna**, jolloin **Muokkaa kyselyä** -painike tulee näkyviin toimintoruudussa.
1. Valitse toimintoruudussa **Muokkaa kyselyä**.
1. Lisää kyselyeditorin **Lajittelu**-välilehdessä rivi, jolla on seuraavat arvot:

    - **Taulukko:** *Lähetykset*
    - **Johdettu taulu:** *Lähetykset*
    - **Kenttä:** *Rahdinkuljetuspalvelu*

        Kun olet valinnut tämän arvon, näyttöön saattaa tulla seuraava sanoma: "Rahdinkuljetuspalvelukenttä ei ole indeksikenttä. Haluatko lisätä lajittelun tähän? " Valitse **Kyllä**.

    - **Hakusuunta:** *Laskeva*

1. Valitse **OK**.
1. Näyttö voi tulla seuraava sanoma: Ryhmittely nollataan. Haluatko jatkaa?" Valitse **Kyllä**.

    **Lähtevän lajittelun mallivaihdot** -painike tulee näkyviin toimintoruudussa.

1. Valitse toimintoruudussa **Lähtevän lajittelun mallivaihdot**.
1. Määritä **Lähtevien lajitteluehdot** -valintaikkunassa seuraavat arvot:

    - **Viitetaulukon nimi:** *Lähetykset*
    - **Viitekentän nimi:** *Rahdinkuljetuspalvelu*
    - **Ryhmittele kentän mukaan:** Ryhmittele lähetykset rahdinkuljettajapalvelun mukaan valitsemalla tämä valintaruutu.

1. Valitse **OK** tallentaaksesi asetukset ja sulje valintaikkuna.

### <a name="set-up-container-packing-policies"></a>Kontin pakkauskäytäntöjen määrittäminen

1. Valitse **Varastonhallinta \> Asetukset \> Kontit \> Kontin pakkauskäytännöt**.
1. Valitse toimintoruudussa **Uusi**.
1. Määritä uuden käytännön ylätunnisteessa seuraavat arvot:

    - **Kontin pakkauskäytäntö:** *Lajittelu*
    - **Kuvaus:** *Lajittelu*

1. Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:

    - **Varasto**: *62*
    - **Lajittelun oletussijainti:** *LAJITTELU*
    - **Painoyksikkö:** *kg*
    - **Kontin sulkemiskäytäntö:** *Automaattinen vapautus*
    - **Kontin vapautuskäytäntö:** *Säilön määrittäminen lähtevään lajittelusijaintiin*

1. Valitse **Tallenna**.

### <a name="set-up-packing-profiles"></a>Määritä pakkausprofiilit

Luo uusi lajittelutoiminnon kanssa yhdessä käytettävä pakkausprofiili.

1. Valitse **Varastonhallinta \> Asetukset \> Pakkaus \> Pakkausprofiilit**.
1. Luo rivi valitsemalla toimintoruudussa **Uusi** ja määritä sille seuraavat arvot:

    - **Pakkausprofiilin tunnus:** *Lajitteli*
    - **Kuvaus:** *Lajittelu*
    - **Kontin pakkauskäytäntö:** *Lajittelu*
    - **Konttitunnuksen tila:** *Automaattinen*
    - **Kontin tyyppi:** *Laatikko-suuri*
    - **Luo kontti automaattisesti, kun kontti suljetaan:** Tyhjennetty (= *Ei*)

1. Valitse **Tallenna**.

### <a name="set-up-work-classes"></a>Työluokkien määrittäminen

Määritä yhdessä lajittelun kanssa käytettävä työluokka.

1. Valitse **Varastonhallinta \> Asetukset \> Työ \> Työluokka**.
1. Luo lajittelu työluokka valitsemalla toimintoruudussa **Uusi** ja määritä sille seuraavat arvot:

    - **Työluokan tunnus:** *Lajittelu*
    - **Kuvaus:** *Lajittelu*
    - **Työtilauksen tyyppi:** *Lajiteltu varastokeräily*

1. Valitse **Tallenna**.

### <a name="set-up-mobile-device-menu-items"></a>Mobiililaitteen valikkovaihtoehtojen määrittäminen

#### <a name="set-up-a-new-pallet-menu-item"></a>Uuden kuormalavan valikkovaihtoehdon määrittäminen

Luo mobiililaitteen valikkovaihtoehto lajittelun aikana tapahtuvalla kuormalavojen luonnille.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Valitse toimintoruudussa **Uusi**.
1. Aseta otsikkorivillä seuraavat arvot:

    - **Valikkovaihtoehdon nimi:** *Kuormalavan luonti*
    - **Otsikko:** *Kuormalavan luonti*
    - **Tila:** *Epäsuora*
    - **Käytä aiemmin luotua työtä:** *Ei*

1. Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:

    - **Tehtäväkoodi:** *Lähtevä lajittelu*

        Kun tämän kentän asetuksena on *Lähtevä lajittelu*, **Lähtevän lajittelumallin tunnus** -kenttä on näkyvissä.

    - **Käytä prosessiopasta:** *Kyllä*

        Kun **Tehtäväkoodi**-kentän asetuksena *Lähtevä lajittelu*, tämän asetuksen määrityksenä on automaattisesti *Kyllä*.

    - **Lähtevän lajittelumallin tunnus:** *AutoWork*

1. Valitse **Tallenna**.

#### <a name="set-up-a-new-loading-menu-item"></a>Uuden kuormaamisen valikkovaihtoehdon määrittäminen

Luo seuraavaksi valikkovaihtoehto, jolla käyttäjät voivat siirtää lajitellut varastonimikkeet lähetyssijaintiin.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.
1. Valitse toimintoruudussa **Uusi**.
1. Aseta otsikkorivillä seuraavat arvot:

    - **Valikkovaihtoehdon nimi:** *Kuormaus lajittelusta*
    - **Otsikko:** *Kuormaus lajittelusta*
    - **Tila:** *Työ*
    - **Käytä aiemmin luotua työtä:** *Kyllä*

1. Määritä **Yleinen**-pikavälilehden **Ohjaus**-kentän arvoksi *Käyttäjäohjattu*.
1. Valitse **Työluokat**-pikavälilehdessä **Uusi** ja määritä sitten seuraavat arvot:

    - **Työluokan tunnus:** *LAJITTELU*
    - **Työtilauksen tyyppi:** *Lajiteltu varastokeräily*

1. Valitse **Tallenna**.

### <a name="set-up-the-mobile-device-menu"></a>Mobiililaitteen valikon määrittäminen

Uudet valikkovaihtoehdot on nyt lisättävä mobiililaitteen valikkoon.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikko**.
1. Valitse **Lähtevä**-valikko.
1. Valitse toimintoruudussa **Muokkaa**.
1. Etsi ja valitse **Kuormalavan luonti** **Käytettävissä olevat valikot ja valikkovaihtoehdot** -sarakkeessa.
1. Siirrä **Kuormalavan luonti** oikealla nuolipainikkeella **Valikon rakenne** -sarakkeeseen.
1. Siirrä **Kuormalavan luonti** -valikkovaihtoehto ylä- ja alanuolipainikkeilla sopivaan paikkaan mobiililaitteen valikossa.
1. Valitse **Tallenna**.
1. Lisää **Kuormaus lajittelusta** -valikkovaihtoehto **Lähtevät**-valikkoon vastaavasti.

### <a name="set-up-location-directives"></a>Määritä sijaintidirektiivit

*Sijaintidirektiivit* ovat sääntöjä, jotka auttavat tunnistamaan keräily- ja poispanosijainnit varaston siirrossa. Nyt on luotava sääntö, jolla lajittelutyötä hallitaan.

#### <a name="set-up-a-single-sku-directive"></a>Yhden varastointiyksikön direktiivin määrittäminen

1. Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.
1. Muuta vasemmassa ruudussa **Työtilauksen tyyppi** -kentän arvoksi *Lajiteltu varastokeräily*.
1. Valitse toimintoruudussa **Uusi**.
1. Aseta otsikkorivillä seuraavat arvot:

    - **Järjestys:** *1*
    - **Nimi:** *Baydoor*

1. Määritä **Sijaintidirektiivit**-pikavälilehdessä seuraavat arvot:

    - **Työtyyppi:** *Aseta*
    - **Toimipaikka:** *6*
    - **Varasto**: *62*
    - **Useita varastointiyksiköitä:** *Ei*

1. Valitsemalla **Tallenna** voit ottaa **Rivit**-pikavälilehden työkalurivin käyttöön.
1. Valitse **Rivit**-pikavälilehdessä **Uusi** ja määritä sitten seuraavat arvot uudella rivillä. Hyväksy kaikkien muiden kenttien oletusarvot.

    - **Järjestys:** *1*
    - **Alku:** *0*
    - **Loppu:** *1 000 000*

1. Valitsemalla **Tallenna** voit ottaa **Sijaintidirektiivitoiminnot**-pikavälilehden työkalurivin käyttöön.
1. Valitse **Sijaintidirektiivitoiminnot**-pikavälilehdessä **Uusi** ja määritä sitten seuraavat arvot uudella rivillä. Hyväksy kaikkien muiden kenttien oletusarvot.

    - **Järjestys:** *1*
    - **Nimi:** *Baydoor*

1. Valitse **Tallenna**.
1. Valitse **Sijaintidirektiivitoiminnot**-pikavälilehdessä **Muokkaa kyselyä**.
1. Etsi kyselyeditoriin **Alue**-välilehdessä rivi, jonka **Kenttä**-kentän asetuksena on *Sijainti*. Määritä tämän rivin **Ehdot**-kentän arvoksi *Lastauspaikan ovi*.
1. Tallenna asetukset valitsemalla **OK** ja sulje kyselyeditori.

#### <a name="set-up-a-multiple-sku-directive"></a>Usean varastointiyksikön direktiivin määrittäminen

1. Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.
1. Muuta vasemmassa ruudussa **Työtilauksen tyyppi** -kentän arvoksi *Lajiteltu varastokeräily*.
1. Valitse toimintoruudussa **Uusi**.
1. Aseta otsikkorivillä seuraavat arvot:

    - **Järjestys:** *2*
    - **Nimi:** *Monta lastausovea*

1. Määritä **Sijaintidirektiivit**-pikavälilehdessä seuraavat arvot:

    - **Työtyyppi:** *Aseta*
    - **Toimipaikka:** *6*
    - **Varasto**: *62*
    - **Useita varastointiyksiköitä:** *Kyllä*

1. Valitsemalla **Tallenna** voit ottaa **Rivit**-pikavälilehden työkalurivin käyttöön.
1. Valitse **Rivit**-pikavälilehdessä **Uusi** ja määritä sitten seuraavat arvot uudella rivillä. Hyväksy kaikkien muiden kenttien oletusarvot.

    - **Järjestys:** *1*
    - **Alku:** *0*
    - **Loppu:** *1 000 000*

1. Valitsemalla **Tallenna** voit ottaa **Sijaintidirektiivitoiminnot**-pikavälilehden työkalurivin käyttöön.
1. Valitse **Sijaintidirektiivitoiminnot**-pikavälilehdessä **Uusi** ja määritä sitten seuraavat arvot uudella rivillä. Hyväksy kaikkien muiden kenttien oletusarvot.

    - **Järjestys:** *1*
    - **Nimi:** *Monta lastausovea*

1. Valitse **Tallenna**.
1. Valitse **Sijaintidirektiivitoiminnot**-pikavälilehdessä **Muokkaa kyselyä**.
1. Etsi kyselyeditoriin **Alue**-välilehdessä rivi, jonka **Kenttä**-kentän asetuksena on *Sijainti*. Määritä tämän rivin **Ehdot**-kentän arvoksi *Lastauspaikan ovi*.
1. Tallenna asetukset valitsemalla **OK** ja sulje kyselyeditori.

### <a name="set-up-work-templates"></a>Määritä työmallit

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työmallit**.
1. Muuta **Työtilauksen tyyppi** -kentän arvoksi *Lajiteltu varastokeräily*.
1. Valitse toimintoruudussa **Uusi** ja luo työmalli.
1. Määritä **Yleiskatsaus**-välilehdessä seuraavat arvot:

    - **Järjestys:** *1*
    - **Työmalli:** *Lajittelu*
    - **Työmallin kuvaus:** *Lajittelu*

1. Valitse **Tallenna**, jos haluat, että **Työmallin tiedot** -pikavälilehti on käytettävissä.
1. Lisää rivi valitsemalla **Työmallin tiedot** -pikavälilehdessä **Uusi** ja määritä sitten seuraavat arvot:

    - **Työtyyppi:** *Poiminta*
    - **Työluokan tunnus:** *LAJITTELU*

1. Lisää toinen rivi valitsemalla **Uusi** uudelleen ja määritä sitten seuraavat arvot:

    - **Työtyyppi:** *Aseta*
    - **Työluokan tunnus:** *LAJITTELU*

1. Valitse **Tallenna**.

## <a name="scenario"></a>Skenaario

Tämä skenaario simuloi tilannetta, jossa pakatut kontit on lajiteltava pakkausaseman jälkeen automaattisesti eri paikkoihin (kuormalavoille) rahdinkuljetuspalvelun mukaan. Kun kaikki kuorman nimikkeet on pakattu ja lajiteltu osoitteen mukaan, kuormalavat siirretään lastausovelle.

### <a name="create-sales-orders-and-picking-work"></a>Myyntitilausten ja keräystyön luominen

#### <a name="create-sales-order-1"></a>Luo myyntitilaus 1

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Valitse toimintoruudussa **Uusi**.
1. Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:

    - **Asiakastili:** *US-005*
    - **Varasto**: *62*

1. Sulje valintaikkuna valitsemalla **OK**.

    Uusi myyntitilaus avataan.

1. Vaihda **Otsikko**-näkymään.
1. Määritä **Toimitus**-pikavälilehden **Kuljetus**-osassa seuraavat arvot:

    - **Rahdinkuljettaja:** *Lentorahti*
    - **Rahdinkuljetuspalvelu:** *Ilma*

1. Siirry **Rivit**-näkymään.
1. Jos uutta tyhjää riviä ei lisätä automaattisesti ruudukkoon, lisää se valitsemalla **Myyntitilausrivit**-pikavälilehdessä **Lisää rivi**.
1. Määritä seuraavat arvot uudella tilausrivillä:

    - **Nimiketunnus:** *A0001*
    - **Määrä** *2*

1. Kun uusi rivi on edelleen valittuna **Myyntitilausrivit**-pikavälilehdessä, valitse ruudukon yläpuolella olevassa **Varasto**-valikossa **Varaus**.
1. Valitse **Varaus**-sivulla **Varaa erä**, jos haluat varata valitun rivin koko määrän varastossa.
1. Palaa myyntitilaukseen sulkemalla **Varaus**-sivun.
1. Valitse toimintoruudussa **Varasto**-välilehden **Toiminnot**-ryhmässä **Vapauta varastoon**.
1. Näyttöön tulee tietosanoma, jossa näkyy tämän tilauksen lähetys ja aalto. Kirjoita muistiin aallon ja lähetyksen tunnusnumerot.

#### <a name="sales-order-2"></a>Myyntitilaus 2

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Valitse toimintoruudussa **Uusi**.
1. Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:

    - **Asiakastili:** *US-006*
    - **Varasto**: *62*

1. Sulje valintaikkuna valitsemalla **OK**.
1. Uusi myyntitilaus avataan. **Myyntitilausrivit**-pikavälilehden ruudukossa pitäisi olla uusi tyhjä rivi. Määritä seuraavat arvot kyseisellä tilausrivillä:

    - **Nimike:** *A0001*
    - **Määrä** *1*

1. Määritä **Rivitiedot**-pikavälilehden **Toimitus**-välilehden **Toimitustapa**-kentän arvoksi *Flowe-STD*.
1. Valitse **Myyntitilausrivit**-pikavälilehdessä **Lisää rivi** ja määritä sitten seuraavat arvot toisella tilausrivillä:

    - **Nimike:** *A0002*
    - **Määrä** *1*

1. Vaihda **Rivitiedot**-pikavälilehden **Toimitus**-välilehden **Toimitustapa**-kentän arvoksi *Air C-Air*.
1. Valitse ensimmäinen tilausrivi **Myyntitilausrivit**-pikavälilehdessä. Valitse sitten ruudukon yläpuolella olevassa **Varasto**-valikossa **Varaus**.
1. Valitse **Varaus**-sivulla **Varaa erä**, jos haluat varata valitun rivin koko määrän varastossa.
1. Palaa myyntitilaukseen sulkemalla **Varaus**-sivun.
1. Valitse toinen tilausrivi **Myyntitilausrivit**-pikavälilehdessä. Valitse sitten ruudukon yläpuolella olevassa **Varasto**-valikossa **Varaus**.
1. Valitse **Varaus**-sivulla **Varaa erä**, jos haluat varata valitun rivin koko määrän varastossa.
1. Palaa myyntitilaukseen sulkemalla **Varaus**-sivun.
1. Valitse toimintoruudussa **Varasto**-välilehden **Toiminnot**-ryhmässä **Vapauta varastoon**.
1. Näyttöön tulee tietosanoma, jossa näkyy tämän tilauksen lähetys ja aalto. Näet, että kaksi aallon tunnuslukua ja kaksi lähetyksen tunnuslukua on luotu; yksi kummallekin myyntitilausrivien toimitustavalle.

#### <a name="get-the-work-ids-from-the-work-details"></a>Työtunnusten hakeminen työn tiedoista

1. Valitse **Varastonhallinta \> Työ \> Työn tiedot**.
1. -Sivulla näkyvät työtunnukset, jotka on luotu myynti tilauksista. Etsi kummankin aallon ja lähetyksen työtunnus käyttämällä luotujen myyntitilausten aallon ja lähetyksen tunnuksia. Kirjoita nämä työtunnukset muistiin, sillä niitä tarvitaan seuraavissa vaiheissa. Näet, että toiselle myyntitilaukselle luotiin kaksi työtunnusta. Erilliset työtunnukset luodaan, jos eri sijainneista kerätään eri nimikkeitä.

### <a name="pick-items-for-the-sales-orders"></a>Nimikkeiden keräily myyntitilauksia varten

Tee luotu työ loppuun siirtämällä nimikkeet pakkausasemalle mobiililaitteen avulla.

1. Kirjaudu mobiililaitteella varastoon *62* käyttämällä käyttäjätunnusta, jonka loit tätä skenaariota varten, (tai aiemmin luodun esittelytietojen käyttäjän käyttäjätunnusta).
1. Valitse päävalikossa **Lähtevä**.
1. Valitse **Lähtevä**-valikossa **Myynnin keräily**.
1. Anna **Tunnus**-kenttään myyntitilaukselle 1 luotu työtunnus.
1. Valitse **OK**.
1. Anna **Myyntitilaukset – keräily** -sivulla myyntitilaukselle 1 luotu kohderekisterikilpi. Huomaa, että keräilysijainti (*joukko-001*), nimike (*A0001*) ja määrä (*2 kpl*) ovat näkyvissä.
1. Valitse **OK**.
1. Tarkista **Myyntitilaukset – poispano** -sivulla olevat tiedot. **Sijainti**-kentän pitäisi ilmaista, että kerätyt nimikkeet ovat menossa *Pakkaus*-sijaintiin.
1. Valitse **OK**.

    **Skannaa työn tunnus tai rekisterikilven tunnus** -sivulla on Työ valmis -sanoma, joka ilmaisee, myyntitilauksen 1 työtunnus on valmistunut.

    Seuraavaksi kerätään myyntitilaus 2.

1. Anna **Tunnus**-kenttään työtunnus, joka luotiin myyntitilaukselle 2 ja jossa rivillä 1 on nimike *A0001*.
1. Valitse **OK**.
1. Anna **Myyntilaukset – keräily** -sivulla kohderekisterikilpi. Huomaa, että keräilysijainti (*joukko-001*), nimike (*A0001*) ja määrä (*1 kpl*) ovat näkyvissä.
1. Valitse **OK**.
1. Tarkista **Myyntitilaukset – poispano** -sivulla olevat tiedot. **Sijainti**-kentän pitäisi ilmaista, että kerätyt nimikkeet ovat menossa *Pakkaus*-sijaintiin.
1. Valitse **OK**.

    **Skannaa työn tunnus tai rekisterikilven tunnus** -sivulla on Työ valmis -sanoma. Sanoma ilmaisee, että myyntilauksen 2 rivin 1 työtunnus on valmis.

1. Anna **Tunnus**-kenttään työtunnus, joka luotiin myyntitilaukselle 2 ja jossa rivillä 2 on nimike *A0002*.
1. Valitse **OK**.
1. Anna **Myyntilaukset – keräily** -sivulla kohderekisterikilpi. Huomaa, että keräilysijainti (*joukko-002*), nimike (*A0001*) ja määrä (*1 kpl*) ovat näkyvissä.
1. Valitse **OK**.
1. Tarkista **Myyntitilaukset – poispano** -sivulla olevat tiedot. **Sijainti**-kentän pitäisi ilmaista, että kerätyt nimikkeet ovat menossa *Pakkaus*-sijaintiin.
1. Valitse **OK**.

    **Skannaa työn tunnus tai rekisterikilven tunnus** -sivulla on Työ valmis -sanoma. Sanoma ilmaisee, että myyntilauksen 2 rivin 2 työtunnus on valmis.

### <a name="pack-sales-orders-into-containers"></a>Myyntitilausten pakkaaminen kontteihin

#### <a name="pack-sales-order-1-into-containers"></a>Myyntitilauksen 1 pakkaaminen kontteihin

1. Valitse **Varastoinhallinta \> Pakkaus ja konttiinpakkaus \> Pakkaus**.

    **Valitse pakkausasema** -valintaikkuna avautuu. **Työntekijä**-kentässä pitäisi oletusarvoisesti olla aiemmin määritetyn työntekijän nimi.

1. Määritä seuraavat arvot tiettyyn pakkaussijaintiin suunniteltujen lähetysten ja konttien tarkastelua ja käsittelyä varten:

    - **Toimipaikka:** *6*
    - **Varasto**: *62*
    - **Sijainti:** *Pakkaus*
    - **Pakkausprofiilin tunnus:** *Lajitteli*

1. Sulje valintaikkuna valitsemalla **OK**.
1. Anna **Pakkaus**-sivun **Rekisterikilpi tai lähetys**-kenttään myyntitilauksen 1 kohderekisterikilpi. Siirry sitten kentästä pois painamalla **Sarkain**- tai **Enter**-näppäintä.
1. Valitse toimintoruudussa **Uusi kontti**.
1. Hyväksy kaikki oletusasetukset ja valitse **OK**. Kirjoita kontin tunnus muistiin.
1. Määritä **Nimikkeen pakkaus** -pikavälilehdessä seuraavat arvot:

    - **Määrä** *1*
    - **Tunniste:** nimike *A0001*

1. Valitse toimintoruudussa **Sulje kontti**.
1. Valitse **Sulje kontti** -valintaikkunassa **Hae järjestelmän paino**, jolloin järjestelmä päivittää **Bruttopaino**-kentän.
1. Valitse **OK**. Kontti siirretään *LAJITTELU*-sijaintiin ja on valmis lajiteltavaksi.
1. Lisää toinen myyntilauksen 1 rekisterikilven nimike uuteen konttiin luomalla toinen kontti.
1. Valitse toimintoruudussa **Uusi kontti**.
1. Hyväksy kaikki oletusasetukset ja valitse **OK**. Kirjoita kontin tunnus muistiin.
1. Määritä **Nimikkeen pakkaus** -pikavälilehdessä seuraavat arvot:

    - **Määrä** *1*
    - **Tunniste:** nimike *A0001*

1. Valitse toimintoruudussa **Sulje kontti**.
1. Valitse **Sulje kontti** -valintaikkunassa **Hae järjestelmän paino**, jolloin järjestelmä päivittää **Bruttopaino**-kentän.
1. Valitse **OK**. Kontti siirretään *LAJITTELU*-sijaintiin ja on valmis lajiteltavaksi.

#### <a name="pack-sales-order-2-into-containers"></a>Myyntitilauksen 2 pakkaaminen kontteihin

1. Anna **Pakkaus**-sivun **Rekisterikilpi tai lähetys**-kenttään myyntitilauksen 2 rivin 1 kohderekisterikilpi. Siirry sitten kentästä pois painamalla **Sarkain**- tai **Enter**-näppäintä.
1. Valitse toimintoruudussa **Uusi kontti**.
1. Hyväksy kaikki oletusasetukset ja valitse **OK**. Kirjoita kontin tunnus muistiin.
1. Määritä **Nimikkeen pakkaus** -pikavälilehdessä seuraavat arvot:

    - **Määrä** *1*
    - **Tunniste:** nimike *A0001*

1. Valitse toimintoruudussa **Sulje kontti**.
1. Valitse **Sulje kontti** -valintaikkunassa **Hae järjestelmän paino**, jolloin järjestelmä päivittää **Bruttopaino**-kentän.
1. Valitse **OK**. Kontti siirretään *LAJITTELU*-sijaintiin ja on valmis lajiteltavaksi.
1. **Rekisterikilpi tai lähetys** -kenttään myyntitilauksen 2 rivin 2 kohderekisterikilpi. Siirry sitten kentästä pois painamalla **Sarkain**- tai **Enter**-näppäintä.
1. Valitse toimintoruudussa **Uusi kontti**.
1. Hyväksy kaikki oletusasetukset ja valitse **OK**. Kirjoita kontin tunnus muistiin.
1. Määritä **Nimikkeen pakkaus** -pikavälilehdessä seuraavat arvot:

    - **Määrä** *1*
    - **Tunnistekenttä:** nimike *A0002*

1. Valitse toimintoruudussa **Sulje kontti**.
1. Valitse **Sulje kontti** -valintaikkunassa **Hae järjestelmän paino**, jolloin järjestelmä päivittää **Bruttopaino**-kentän.
1. Valitse **OK**. Kontti siirretään *LAJITTELU*-sijaintiin ja on valmis lajiteltavaksi.

Voit tarkastella kontin tietoja valitsemalla **Varastonhallinta \> Pakkaus ja konttiinpakkaus \> Kontit** ja hakemalla pakkauksen aikana luodut konttitunnukset.

### <a name="sort-the-containers"></a>Konttien lajittelu

> [!IMPORTANT]
> Kun teet lähtevän lajittelun käyttämällä **Kuormalavan luonti** -valikkovaihtoehtoa mobiilisovelluksessa, näkyviin tulee **Täysi**-painike. *Älä käytä **Täysi**-painiketta lajittelun tai paikan sulkemiseen.*
>
> **Täysi**-painike on oletusarvo eikä sitä voi poistaa käytöstä tai poistaa sivulta. Sitä ei käytetä *Lähtevä lajittelu* -toiminnossa.

#### <a name="sort-the-first-container"></a>Ensimmäisen kontin lajittelu

1. Kirjaudu mobiililaitteella varastoon *62* käyttämällä käyttäjätunnusta, jonka loit tätä skenaariota varten, (tai aiemmin luodun esittelytietojen käyttäjän käyttäjätunnusta).
1. Valitse päävalikossa **Lähtevä**.
1. Valitse **Lähtevä**-valikossa **Kuormalavan luonti**.
1. Anna **Rekisterikilpi/kontti**-kenttään myyntilaukseen 1 liitetyn ensimmäisen kontin tunnus.
1. Valitse **OK**.
1. Koska lajittelua ei tällä hetkellä ole, sellainen on määritettävä. Anna **Lajittelupaikan tunnus** -kenttään *SP01*.
1. Koska lajittelupaikkaan *SP01* ei ole tällä hetkellä liitetty rekisterikilpeä, se on määritettävä. Anna **RK**-kentässä *PLP01*.
1. Valitse **OK**.
1. Koska lajittelupaikan vahvistus on otettu käyttöön, lajittelupaikan tunnus on annettava uudelleen. Anna **Lajittelupaikan tunnus** -kenttään *SP01*.
1. Valitse **OK**.

    Näyttöön tulee Työ valmis -sanoma.

> [!TIP]
> Voit tarkastella lajittelupaikkaa ja siinä oleva rekisterikilpeä valitsemalla **Varastohallinta \> Pakkaus ja konttiinpakkaus \> Lähtevän lajittelupaikan määritykset**.
>
> **Lähtevän lajittelupaikan määritykset** -sivulla näkyy kaikki tällä hetkellä aktiivisena olevat lajittelupaikat. **Lajittelupaikan tapahtumat** -kentässä näkyy rekisterikilpi, joka on liitetty kuhunkin lajittelupaikkaan ja lajittelupaikassa oleviin kontteihin. Huomaa, että yksi lajittelupaikka on luotu jo aiemmin ja että **Sijainnin lajitteluehdot** -pikavälilehdessä on **Lähetys – rahdinkuljettaja – ilma** -kohdan ehdot.

#### <a name="sort-the-remaining-containers"></a>Jäljellä olevien konttien lajittelu

1. Kirjaudu mobiililaitteella varastoon *62* käyttämällä käyttäjätunnusta, jonka loit tätä skenaariota varten, (tai aiemmin luodun esittelytietojen käyttäjän käyttäjätunnusta).
1. Valitse päävalikossa **Lähtevä**.
1. Valitse **Lähtevä**-valikossa **Kuormalavan luonti**.
1. Anna **Rekisterikilpi/kontti**-kenttään myyntilaukseen 1 liitetyn toisen kontin tunnus.
1. Valitse **OK**. Koska lajittelumalli on määritetty tekemään lajittelu automaattisesti ja olemassa on ehdot täyttävä lajittelupaikka, ohjaus oikeaan lajittelupaikkaan tehdään automaattisesti.
1. Valitse **OK**.
1. Lajittelupaikan tunnuksen vahvistaminen osoittaa, että varasto on oikeassa paikassa. Anna **Lajittelupaikan tunnus** -kenttään *SP01*.
1. Valitse **OK**.

    Myyntitilauksen 1 toisen kontin työ on valmis. Seuraavaksi lajitellaan myyntitilauksen 2 jäljellä olevat kontit.

1. Anna **Rekisterikilpi/kontti**-kentässä sen myyntitilauksen 2 kontin konttitunnus, jossa nimike *A0001* on. Koska rahdinkuljettaja ei ole sama, sinua pyydetään antamaan uusi lajittelupaikka ja määrittämään rekisterikilpi kyseiseen paikkaan. Käytä lajittelupaikkaa *SP02* ja rekisterikilpeä *PLP02*.
1. Valitse **OK**.
1. Vahvista lajittelupaikka antamalla *SP02* **Lajittelupaikan tunnus** -kentässä.
1. Valitse **OK**.

    Kontin työ on valmis.

1. Anna **Rekisterikilpi/kontti**-kentässä sen myyntitilauksen 2 jäljellä olevan kontin konttitunnus, jossa nimike *A0002* on. Koska rahdinkuljettaja on sama kuin myyntitilauksen 1 rahdinkuljettaja, järjestelmä näyttää aiemmin luodun ehdot täyttävän lajittelupaikan.
1. Valitse **OK**.
1. Vahvista lajittelupaikka antamalla *SP01* **Lajittelupaikan tunnus** -kentässä.
1. Valitse **OK**.

    Kontin työ on valmis.

### <a name="close-the-outbound-sorting-positions"></a>Lähtevien lajittelupaikkojen sulkeminen

Kun koko varasto on lajiteltu, työtä ei voi luoda, ennen kuin paikka on suljettu. Lajitellun varaston keräilytyö luodaan siirtämään varasto lastausovelle.

#### <a name="close-a-position-from-the-mobile-device"></a>Paikan sulkeminen mobiililaitteessa

1. Kirjaudu mobiililaitteella varastoon *62* käyttämällä käyttäjätunnusta, jonka loit tätä skenaariota varten, (tai aiemmin luodun esittelytietojen käyttäjän käyttäjätunnusta).
1. Valitse päävalikossa **Lähtevä**.
1. Valitse **Lähtevä**-valikossa **Kuormalavan luonti**.
1. Anna **Rekisterikilpi/kontti**-kentässä sen kontin tunnus, joka lajiteltiin lajittelupaikkaan *SP01*.
1. Valitse **OK**.
1. Näyttöön avautuvan sanoman mukaan kontti on jo lajiteltu paikkaan SP01. Suljetaanko sijainti? Valitse **Sulje**.

    Työ on valmis.

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a>Paikan sulkeminen lähtevän lajittelupaikan määrityksistä

1. Valitse **Varastohallinta \> Pakkaus ja konttiinpakkaus \> Lähtevän lajittelupaikan määritykset**.
1. Valitse vasemmasta sarakkeessa **SP02**. Tämä lähtevä lajittelupaikan rivi on suljettava rivi.
1. Valitse toimintoruudussa **Sulje sijainti**. Lajittelusijaintitietue suljetaan, eikä se enää ole näkyvissä.

    > [!TIP]
    > Voit näyttää kaikki suljetut sijaintitietueet valitsemalla **Näytä suljetut** -valintaruudun.

### <a name="sorted-inventory-picking"></a>Lajiteltu varaston keräily

Lajitellun varaston keräilytyö on suoritettava loppuun. Kun se on valmis, varasto kerätään myyntitilaukseen. Tässä vaiheessa käytetään kaikki muita varastoprosesseja.

1. Kirjaudu mobiililaitteella varastoon *62* käyttämällä käyttäjätunnusta, jonka loit tätä skenaariota varten, (tai aiemmin luodun esittelytietojen käyttäjän käyttäjätunnusta).
1. Valitse päävalikossa **Lähtevä**.
1. Valitse **Lähtevä**-valikossa **Kuormaus lajitellusta**.
1. Anna kohderekisterikilven tunnus ensimmäisestä lajittelusijainnista *SP01*. Määritä **Tunnus**-kentän arvoksi *PLP01*.
1. Valitse **OK**.
1. **Lajitellun varaston keräily: keräys** -sivulla näkyy tehtävä keräilytyö. Tee keräys *LAJITTELU*-sijainnista ja kohderekisterikilvestä *PLP01*, jossa on useita nimikkeitä ja jonka määrä on *3*.
1. Valitse **OK**.
1. **Lajitellun varaston keräily: poispano** -sivulla näkyy tehtävä poispanotyö. Tee poispano *Lastausovi*-sijaintiin ja kohderekisterikilpeen *PLP01*, jossa on useita nimikkeitä ja jonka määrä on *3*.
1. Valitse **OK**.

    Työ on valmis.

1. Anna kohderekisterikilven tunnus toisesta lajittelusijainnista *SP02*. Määritä **Tunnus**-kentän arvoksi *PLP02*.
1. Valitse **OK**.
1. **Lajitellun varaston keräily: keräys** -sivulla näkyy tehtävä keräilytyö. Tee keräys *LAJITTELU*-sijainnista ja kohderekisterikilvestä *PLP02*, jossa on useita nimikkeitä ja jonka määrä on *1*.
1. Valitse **OK**.
1. **Lajitellun varaston keräily: poispano** -sivulla näkyy tehtävä poispanotyö. Tee poispano *Lastausovi*-sijaintiin ja kohderekisterikilpeen *PLP02*, jossa on useita nimikkeitä ja jonka määrä on *1*.
1. Valitse **OK**.

    Työ on valmis.

Tästä eteenpäin käytetään kaikki muita varastoprosesseja.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]