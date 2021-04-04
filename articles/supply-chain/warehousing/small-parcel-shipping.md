---
title: Pienten pakettien lähettäminen
description: Tässä aiheessa on tietoja pienten pakettien lähetystoiminnosta. Tämän toiminnon avulla Microsoft Dynamics 365 Supply Chain Management voi lähettää tietoja pakatusta kontista rahdinkuljettajalle sekä saada kyseiseltä rahdinkuljettajalta osoitetarran, lähetyshinnan ja seurantanumeron.
author: Mirzaab
manager: tfehr
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 37f07139853c30da25c067a3d736b4b9bf4eb361
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501171"
---
# <a name="small-parcel-shipping"></a>Pienten pakettien lähettäminen

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Pienten pakettien lähetystoiminnon avulla Microsoft Dynamics 365 Supply Chain Management voi olla suoraan yhteydessä rahdinkuljettajaan muodostamalla viestintäkehyksen rahdinkuljettajan ohjelmointirajapintojen kautta. Tämä toiminto on kätevä, kun yksittäisiä myyntitilauksia lähetetään kaupallisten rahdinkuljettajien kanssa sen sijaan, että käytettäisiin konttitoimitusta tai kuorma-auton osakuormatoimitusta (LTL).

Pienten pakettien lähetystoiminto on yhteydessä rahdinkuljettajaan käyttämällä *hinnan laskentamoduulia*. Organisaation on kehitettävä tämä hinnanlaskentamoduuli yhdessä rahdinkuljettajan tai rahdinkuljettajakeskuspalvelun kanssa. Hinnan laskentamoduulin avulla Supply Chain Management voi lähettää tietoja pakatusta kontista rahdinkuljettajalle sekä saada kyseiseltä rahdinkuljettajalta osoitetarran, lähetyshinnan ja seurantanumeron.

Palautettu lähetyshinta lisätään lähetykseen liittyvään myyntitilaukseen muuna kuluna. Palautettu osoitetarra voidaan sitten tulostaa automaattisesti käyttämällä ZPL (Zebra-ohjelmointikieli) -tulostimella ja kiinnittää toimitukseen. Rahdinkuljettaja skannaa sitten tämän osoitetarran, kun se noutaa paketit varastosta.

## <a name="prepare-your-system-to-support-sps"></a>Järjestelmän valmisteleminen tukemaan pienten pakettien lähetystoimintoa

Ennen pienten pakettien lähetystoiminnon käytön aloittamista se on otettava käyttöön ominaisuuksien hallinnassa, hinnan laskentamoduuli on lisättävä sekä **Kuljetuksenhallinta**- ja **Varastonhallinta**-moduulit on määritettävä tukemaan toimintoja.

### <a name="turn-on-the-sps-feature"></a>Pienten pakettien lähetystoiminnon ottaminen käyttöön

Ennen kuin pienten pakettien lähetystoimintotoa voidaan käyttää, se on otettava käyttöön järjestelmässä. Järjestelmänvalvojat voivat tarkistaa [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilassa toiminnon tilan ja ottaa sen tarvittaessa käyttöön. Tässä tapauksessa toiminto näkyy seuraavalla tavalla:

- **Moduuli:** *Kuljetustenhallinta*
- **Toiminnon nimi:** *Pienten pakettien lähetys*

### <a name="deploy-and-set-up-rate-engines"></a>Hinnan laskentamoduulinen ottaminen käyttöön ja määrittäminen

Supply Chain Management ei sisällä yhtään hinnan laskentamoduulia. Tarvittavat hinnan laskentamoduulin on hankittava tai luotava, minkä jälkeen ne on lisättävä järjestelmään. Microsoftilla on kuitenkin hinnan laskennan esittelymoduuli, jota voi käyttää testaukseen.

#### <a name="download-and-deploy-the-demo-rate-engine"></a>Hinnan laskennan esittelymoduulin lataaminen ja ottaminen käyttöön

Hinnan laskennan esittelymoduuli haetaan seuraavasti:

1. Lataa GitHubissa [hinnan laskennan DLL (dynamic-link library) -kirjasto](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).
1. Tallenna DLL-kirjasto Supply Chain Management -palvelimessa kansioon **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin**.

#### <a name="create-and-deploy-functional-rate-engines"></a>Toiminnallisten hinnan laskentamoduulien luominen ja ottaminen käyttöön

Lisätietoja toiminnallisten tuotanto- tai testiympäristössä käytettävien hinnan laskentamoduulien luomisesta ja ottamisesta käyttöön on seuraavissa aiheissa:

- [Uuden kuljetuksenhallintamoduulin luominen](../transportation/create-new-transportation-management-engine.md)
- [Kuljetustenhallintamoduulien määrittäminen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

Lisätietoja pienten pakettien lähetyksen hinnan laskentamoduulin luomisesta on seuraavassa blogikirjoituksessa: [Pienten pakettien lähettäminen: pienten pakettien lähetystoiminnon hyödyntäminen Microsoft Dynamics 365:ssä](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a>Hinnan laskentamoduulin määrittäminen Supply Chain Managementissa

Kun pienten pakettien hinnan laskentamoduuli on luotu ja otettu käyttöön, se määritetään seuraavasti:

1. Valitse **Kuljetustenhallinta \> Asetukset \> Moduulit \> Hinnan laskenta**.
1. Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**.
1. Määritä uudella rivillä seuraavat kentät:

    - **Hinnoittelumoduuli** – Anna hinnan laskentamoduulille yksilöivä nimi. Jos käytössä on hinnan laskennan esittelymoduuli, anna nimeksi *Hinnan laskennan esittelymoduuli*.
    - **Nimi** – Anna lyhyt hinnan laskentamoduulin kuvaus. Jos käytössä on hinnan laskennan esittelymoduuli, anna nimeksi *Hinnan laskennan esittelymoduuli*.
    - **Luokituksen metatietojen tunnus** – Valitse hinnan laskentaperuste. Hinta voidaan laskea esimerkiksi etäisyyden perusteella. Jos käytössä on hinnan laskennan esittelymoduuli, tämän kentän voi jättää tyhjäksi.
    - **Laskennan kokoonpano** – Anna käyttöönotetun DLL-paketin tiedostonimi. Jos käytössä on hinnan laskennan esittelymoduuli, anna nimeksi *TMSSmallParcelShippingEngine.dll*.
    - **Moduulin luokka** – Anna hinnan laskentamoduulille muodostetun luokan nimi. Jos käytössä on hinnan laskennan esittelymoduuli, anna nimeksi *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.

## <a name="example-scenario"></a>Esimerkkiskenaario

Tässä esimerkkiskenaariossa näytetään, miten pienten pakettien lähetystoiminto määritetään ja miten sitä käytetään sen jälkeen, kun järjestelmä on valmisteltu aiemmin tässä aiheessa kuvatulla tavalla. Tässä skenaariossa käytetään edellä mainittua hinnan laskennan esittelymoduulia.

### <a name="make-demo-data-available"></a>Demotietojen ottaminen käyttöön

Tämän skenaarion käyttäminen tässä määritettyjen esittelytietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon vakiomuotoiset [esittelytiedot](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) on asennettu. Sinun on myös valittava **USMF**-yritys ennen kuin aloitat.

### <a name="set-up-the-scenario"></a>Määritä skenaario

Tässä esimerkkiskenaariossa tarvitaan esittelyrahdinkuljettaja, rahdinkuljettajaryhmä, pakkauskäytäntö ja pakkausprofiili. Seuraavissa alakohdissa käsitellään skenaariossa tarvittavien tietueiden valmistelua. Tuotantoskenaarion määritysprosessi muistuttaa yleensä tässä kuvattua prosessia. Määritettävät arvot ovat kuitenkin erilaisia.

#### <a name="set-up-carriers"></a>Rahdinkuljettajien määrittäminen

Rahdinkuljettaja määritetään seuraavasti:

1. Valitse **Kuljetustenhallinta \> Asetukset \> Rahdinkuljettajat \> Lähetyksen rahdinkuljettajat**.
1. Lisää rahdinkuljettaja valitsemalla toimintoruudussa **Uusi**.
1. Määritä otsikossa seuraavat arvot:

    - **Rahdinkuljettaja:** *Esittelyn rahdinkuljettaja*
    - **Nimi:** *Esittelyn rahdinkuljettaja*
    - **Tila:** *Maa*

1. Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:

    - **Aktivoi lähetyksen rahdinkuljettaja:** *Kyllä*
    - **Aktivoi rahdinkuljettajan luokitus:** *Kyllä*

1. Lisää palvelu ruudukkoon valitsemalla **Palvelut**-pikavälilehdessä **Uusi**.
1. Määritä uuden palvelun seuraavat arvot:

    - **Rahdinkuljetuspalvelu:** *Esittelyn rahdinkuljetuspalvelu*
    - **Nimi:** *Esittelyn rahdinkuljetuspalvelu*
    - **Kuljetusmenetelmä:** *Maa*

    Anna tarvittaessa kaikkiin muihin kenttiin jokin arvo. (Kun uusi rahdinkuljettajatietue tallennetaan, uusi toimitustapa luodaan ja **Toimitustapa**-kenttä määritetään automaattisesti.)

1. Lisää hinnoitteluprofiili ruudukkoon **Hinnoitteluprofiilit**-pikavälilehdessä **Uusi**.
1. Määritä uuden profiilin seuraavat arvot:

    - **Hinnoitteluprofiili:** *Esittelyn rahdinkuljetuspalvelu*
    - **Nimi:** *Esittelyn rahdinkuljetuspalvelu*
    - **Hinnan laskenta:** *Hinnan laskennan esittelymoduuli*

    Anna tarvittaessa kaikkiin muihin kenttiin jokin arvo.

1. Valitse toimintoruudussa **Tallenna**.

Lisätietoja rahdinkuljettajien määrittämisestä on kohdassa [Rahdinkuljettajien määrittäminen](../transportation/tasks/set-up-shipping-carriers.md).

#### <a name="set-up-carrier-service-accounts"></a>Rahdinkuljetuspalvelutilien määrittäminen

Rahdinkuljetuspalvelutili määritetään seuraavasti:

1. Valitse **Kuljetustenhallinta \> Asetukset \> Hinnoittelu \> Rahdinkuljetuspalvelutili**.
1. Lisää rahdinkuljetuspalvelutili valitsemalla toimintoruudussa **Uusi**.
1. Määritä uuden tilin seuraavat arvot:

    - **Rahdinkuljettaja:** *Esittelyn rahdinkuljettaja*
    - **Rahdinkuljetuspalvelu:** *Esittelyn rahdinkuljetuspalvelu*
    - **Rahdinkuljettajan asiakastilin numero:** Rahdinkuljettajan asiakastilin numero, jolla yhteys rahdinkuljettajaan vahvistetaan ja todennetaan. Rahdinkuljettaja ilmoittaa tämän arvon. Jos käytössä on esittelypalvelu, arvo voi olla mikä tahansa.
    - **Toimipaikka:** *6*
    - **Varasto**: *62*

    > [!NOTE]
    > **Rahdinkuljettajan asiakastilin numero** -arvo on usein ainoa arvo, joka tarvitaan yhteyden todentamiseen. Jos rahdinkuljettaja kuitenkin edellyttää lisätodennusparametreja, organisaation on mukautettava tätä sivua lisäämällä tarvittavat lisäkenttiä.

#### <a name="set-up-a-container-packing-policy"></a>Kontin pakkauskäytännön määrittäminen

Kontin pakkauskäytäntö määritetään seuraavasti:

1. Jos ZPL-tulostinmääritystä ei ole vielä tehty, määritä se asiakirjan reititysagenttisovelluksella. Lisätietoja on kohdassa [Asiakirjojen tulostamisen yleiskatsaus](../../fin-ops-core/dev-itpro/analytics/print-documents.md) ja siihen liittyvissä aiheissa.
1. Valitse **Varastonhallinta \> Asetukset \> Kontit \> Kontin pakkauskäytännöt**.
1. Lisää kontin pakkauskäytäntö valitsemalla toimintoruudussa **Uusi**.
1. Määritä uuden käytännön otsikossa seuraavat arvot:

    - **Kontin pakkauskäytäntö:** *Esittelyn pakkauskäytäntö*
    - **Kuvaus:** käytännön kuvaus

1. Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:

    - **Varasto**: *62*
    - **Lopullisen lähetyksen oletussijainti:** *Lastauspaikan ovi*
    - **Painoyksikkö:** *KG*
    - **Kontin sulkemiskäytäntö:** *Automaattinen vapautus*
    - **Kontin vapautuskäytäntö:** *Tee saatavaksi lopullisessa lähetyssijainnissa*

1. Määritä seuraavat arvot **Kontin lastiluettelo** -pikavälilehdessä:

    - **Automaattinen lastiluettelo konttia suljettaessa:** *Kyllä*
    - **Kontin lastiluettelon vaatimukset:** *Kuljetustenhallinta*
    - **Tulosta kontin sisältö:** *Ei*

1. Määritä seuraavat arvot **Rahdinkuljettajan etiketin tulostus** -pikavälilehdessä:

    - **Tulosta kontin osoitetarra:** *Aina*
    - **Tulostimen nimi:** osoitetarrat tulostavan ZPL-tulostimen nimi.

#### <a name="set-up-a-packing-profile"></a>Pakkausprofiilin määrittäminen

Määritä pakkausprofiili seuraavasti:

1. Valitse **Varastonhallinta \> Asetukset \> Pakkaus \> Pakkausprofiilit**.
1. Lisää pakkausprofiili ruudukkoon valitsemalla toimintoruudussa **Uusi**.
1. Määritä uuden profiilin seuraavat arvot:

    - **Pakkausprofiilin tunnus:** *Esittely pakkausprofiili*
    - **Kuvaus:** profiilin kuvaus
    - **Kontin pakkauskäytäntö:** *Esittelyn pakkauskäytäntö*
    - **Konttitunnuksen tila:** *Automaattinen*
    - **Kontin tyyppi:** *Pieni pakkaus*

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a>Asiakkaan määrittäminen käyttämään pienten pakettien lähetyksen rahdinkuljettajaa

Määritä asiakas käyttämään luotua rahdinkuljettajaa seuraavasti:

1. Valitse **Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**.
1. Etsi ja valitse ruudukossa asiakas *US-027*.
1. Valitse toimintoruudun **Yleiset**-välilehden **Asetukset**-ryhmässä **Rahdinkuljettajan asiakastilit**.
1. Lisää tili ruudukkoon valitsemalla **Rahdinkuljettajan asiakastilit** -sivun toimintoruudussa **Uusi**.
1. Määritä uuden tilin seuraavat arvot:

    - **Rahdinkuljettaja:** *Esittelyn rahdinkuljettaja*
    - **Rahdinkuljettajan asiakastilin numero:** *12345* (Arvolla ei ole sinänsä merkitystä tässä skenaariossa, mutta siihen viitataan seuraavassa osassa.)

### <a name="go-through-the-example-scenario"></a>Esimerkkiskenaarion suorittaminen

Kun kaikki näytetiedot on määritetty edellisessä osassa kuvatulla tavalla, esimerkkiskenaario voidaan suorittaa.

#### <a name="create-a-sales-order-and-process-the-work"></a>Myyntitilauksen luominen ja työn käsitteleminen

Luo myyntitilaus seuraavasti:

1. Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.
1. Luo uusi myyntitilaus valitsemalla **Uusi**.
1. Määritä **Luo myyntitilaus** -valintaikkunan **Asiakastili**-kentän arvoksi *US-027*.
1. Valitse **OK** luodaksesi ostotilauksen ja sulje valintaikkuna.
1. Uusi myyntitilaus avataan. Määritä **Myyntitilauksen otsikko** -pikavälilehden **Rahdinkuljettajan asiakastilin numero** -kentän arvoksi asiakkaalle aiemmin valittu arvo (*12345*).
1. Lisää **Myyntitilausrivit**-osassa myyntirivi ja määritä sille seuraavat arvot:

    - **Nimiketunnus:** *A0002*
    - **Määrä** *1*
    - **Toimipaikka:** *6*
    - **Varasto**: *62*

1. Vaihda **Otsikko**-näkymään.
1. Määritä **Toimitus**-pikavälilehdessä seuraavat arvot:

    - **Rahdinkuljettaja:** *Esittelyn rahdinkuljettaja*
    - **Rahdinkuljetuspalvelu:** *Esittelyn rahdinkuljetuspalvelu*

1. Siirry takaisin **Rivit**-näkymään. Jos myyntirivin toimitustapa pyydetään päivittämään, valitse **Kyllä**.
1. Valitse **Myyntitilausrivit**-osassa aiemmin määritetty myyntirivi ja valitse sitten **Varasto \> Varaus**.
1. Valitse **Varaus**-sivulla **Varaa erä**, jos haluat varata koko valitun rivin määrän varastosta.
1. Palaa myyntitilaukseen sulkemalla **Varaus**-sivun.
1. Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.

    Työ luodaan siirtämään nimikkeet keräilysijainnista pakkausasemalle.

1. Valitse **Myyntitilausrivi**-osassa **Varasto \> Lähetyksen tiedot**.
1. Kirjoita **Lähetyksen tiedot** -sivulla oleva lähetyksen tunnus muistiin. Tunnusta tarvitaan, kun lähetys pakataan pakkausasemalla.
1. Palaa myyntitilaukseen sulkemalla **Lähetyksen tiedot**-sivu.
1. Kirjoita myyntitilauksen numero muistiin ja valitse **Varastonhallinta \> Työ \> Kaikki työt**.
1. Etsi ja valitse myyntitilauksen numerolla tilaukselle luotu työ.
1. Valitse toimintoruudun **Työ**-välilehdessä **Valmistunut työ**.
1. Valitse käyttäjätunnus **Valmistunut työ** -sivun **Käyttäjätunnus**-kentässä. Valitse sitten toimintoruudussa **Tarkista työ**.
1. Jos työ läpäisee tarkistuksen, valitse toimintoruudussa **Valmistunut työ**.

    Työ merkitään valmiiksi, mikä simuloi nimikkeiden siirtymistä pakkausasemalle.

#### <a name="pack-the-shipment"></a>Lähetyksen pakkaaminen

Pakkaa lähetys seuraavasti:

1. Valitse **Varastonhallinta \> Asetukset \> Työntekijä** ja varmista, että käyttäjätili on liitetty varastonhallinnan työntekijätiliin.
1. Valitse **Varastoinhallinta \> Keräily ja konttiinpakkaus \> Pakkaus**.
1. Määritä seuraavat arvot **Valitse pakkausasema** -valintaikkunassa:

    - **Toimipaikka:** *6*
    - **Varasto**: *62*
    - **Sijainti:** *Pakkaus*
    - **Pakkausprofiilin tunnus:** *Esittely pakkausprofiili*

1. Valitse **OK**.
1. **Pakkaus**-sivu avautuu. Tuotantoskenaariossa työntekijä voi skannata rekisterikilven tai lähetyksen tunnuksen. Avaa kuitenkin tässä skenaariossa **Kaikki lähetykset** -sivu ja etsi juuri luodun lähetyksen lähetyksen numero. Anna sitten tämä arvo **Pakkaus**-sivun **Rekisterikilpi tai lähetys** -kenttään. Vaihtoehtoisesti voit antaa aiemmin muistiin kirjoitetun lähetyksen tunnuksen.
1. Valitse toimintoruudussa **Uusi kontti**.
1. Avautuvassa valintaikkunassa on tietoja uudesta kontista. Älä muuta oletusarvoja ja valitse **OK**.
1. Valitse **Pakkaus**-sivun **Nimikkeen pakkaus** -pikavälilehden **Tunniste**-kentässä *A0002*. Voit nyt pakata kyseisen nimikkeen. Nimike lisätään konttiin.
1. Valitse toimintoruudussa **Lähetettävät kontit**.

    Avautuvalla **Lähetettävät kontit** -sivulla on juuri luodun kontin rivi. Kyseisen rivin **Kontin lastiluettelon tunnus** -kenttä on kuitenkin toistaiseksi tyhjä, koska osoitetarraa ja seurantanumeroa ei ole vielä saata rahdinkuljettajalta.

1. Valitse toimintoruudussa **Sulje kontti**.
1. Määritä **Sulje kontti** -valintaikkunan **Bruttopaino**-kentän arvoksi *1 kg* ja valitse sitten **OK**.

    Osoitetarra on tulostettava seuraavaksi aiemmin valitulla ZPL-tulostimella. Tarran pitäisi on seuraavan esimerkin kaltainen:

    ![Osoitetarraesimerkki](media/sps-label-example.png "Osoitetarraesimerkki")

1. Huomaa, että rahdinkuljettajalta saadut **Kontin lastiluettelon tunnus**- ja **Kokonaisrahti**-arvot on lisätty sellaisenaan.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]