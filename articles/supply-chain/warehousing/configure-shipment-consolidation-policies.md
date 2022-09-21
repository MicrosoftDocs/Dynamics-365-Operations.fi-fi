---
title: Lähetyksen konsolidoinnin käytäntöjen määrittäminen
description: Tässä artikkelissa käsitellään lähetyksen oletusarvoisten ja mukautettujen konsolidointikäytäntöjen määrittämistä.
author: Mirzaab
ms.date: 09/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, TMSMode, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 0312d425d2ebc5311e894030423a916b90f1881a
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427979"
---
# <a name="configure-shipment-consolidation-policies"></a>Lähetyksen konsolidointikäytäntöjen määrittäminen

[!include [banner](../includes/banner.md)]

Lähetyksen konsolidointikäytäntöjä käyttävän lähetyksen konsolidointiprosessin avulla voidaan tehdä automaattinen lähetyksen konsolidointi automaattisen ja manuaaliseen varastoon vapautuksen aikana. Ensimmäiset käytännöt on määritettävä, kun toiminto otetaan käyttöön. Jos käytäntöjä ei määritetä, jokainen myyntirivi luo erillisen lähetyksen, jossa on yksi kuormarivi.

Tämän artikkelin skenaarioiden avulla näytetään, miten määritetään oletusarvoiset ja mukautetut lähetyksen konsolidointikäytännöt.

> [!WARNING]
> Jos päivität sen Microsoft Dynamics 365 Supply Chain Management -järjestelmän version, jossa olet käyttänyt vanhaa lähetyksen konsolidointitoimintoa, konsolidointi ei ehkä enää toimi odotetulla tavalla, jos et noudata tässä annettuja ohjeita.
>
> Kun Supply Chain Managementin asennuksissa *Lähetyksen konsolidoinnin käytännöt* -ominaisuus on poistettu käytöstä, voit ottaa lähetyksen konsolidoinnin käyttöön **Konsolidoi lähetys varastoon vapautettaessa** -asetuksen avulla yksittäisissä varastoissa. Tämä ominaisuus on pakollinen versiosta 10.0.29 alkaen. Kun ominaisuus on käytössä, **Konsolidoi lähetys varastoon vapautettaessa** -asetus piilotetaan ja toiminto korvataan tässä artikkelissa kuvatuilla *lähetyksen konsolidoinnin käytännöillä*. Jokainen käytäntö muodostaa konsolidointisäännöt ja sisältää kyselyn, jolla ohjataan käytännön käyttökohteita. Kun otat käyttöön ominaisuuden ensimmäisen kerran, lähetyksen konsolidointikäytäntöjä ei määritetä **Lähetyksen konsolidointikäytännöt** -sivulla. Kun käytäntöjä ei ole määritetty, järjestelmä käyttää vanhaa toimintatapaa. Tämän vuoksi jokainen olemassa oleva varasto jatkaa **Konsolidoi lähetys varastoon vapautettaessa** -asetuksen noudattamista, vaikka tämä asetus on nyt piilotettu. Kuitenkin vähintään yhden lähetyksen konsolidointikäytännön luomisen yhteydessä **Konsolidoi lähetys varastoon vapautettaessa** -asetus ei ole enää voimassa, ja konsolidointitoiminto on kokonaan käytäntöjen hallinnoima.
>
> Kun olet määrittänyt vähintään yhden lähetyksen konsolidointikäytännön, järjestelmä tarkistaa konsolidointikäytännöt aina, kun tilaus vapautetaan varastoon. Järjestelmä käsittelee käytännöt käyttämällä järjestystä, joka on määritetty kunkin käytännön **Käytäntöjärjestys**-arvon mukaan. Se käyttää ensimmäistä käytäntöä, jossa kysely vastaa uutta tilausta. Jos kyselyt eivät vastaa tilausta, jokainen tilausrivi luo erillisen lähetyksen, jossa on yksi kuormarivi. Tämän vuoksi varmuudeksi kannattaa luoda oletuskäytäntö, jota käytetään kaikissa varastoissa ja ryhmissä tilausnumeron mukaan. Anna tälle varmistuskäytännölle korkein mahdollinen **käytäntöjärjestyksen** arvo, jotta se käsitellään viimeisenä.
>
> Jos haluat luoda vanhan toimintatavan uudelleen, luo käytäntö, joka ei ryhmittele tilausnumeron mukaan ja jolla on kyselyehdot, jotka sisältävät soveltuvat varastot.

## <a name="turn-on-the-shipment-consolidation-policies-feature"></a>Lähetyksen konsolidointikäytäntötoiminnon ottaminen käyttöön

Jos haluat käyttää *Lähetyksen konsolidointikäytännöt* -toimintoa, se on otettava järjestelmässä käyttöön. Supply Chain Managementin versiosta 10.0.29 alkaen tämä toiminto on pakollinen, eikä sitä voi poistaa käytöstä. Jos käytät vanhempaa versiota kuin 10.0.29, järjestelmänvalvojat voivat ottaa tämän toiminnon käyttöön tai pois käytöstä hakemalla *Lähetyksen konsolidoinnin käytännöt* -toimintoa [Toimintojen hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilassa.

## <a name="set-up-your-initial-consolidation-policies"></a><a name="initial-policies"></a>Määritä alkuperäiset konsolidointikäytännöt

Jos käytät uutta järjestelmää tai järjestelmää, jossa juuri otit käyttöön *Lähetyksen konsolidointikäytännöt* -ominaisuuden ensimmäisen kerran, määritä ensimmäiset lähetyksen konsolidointikäytännöt alla olevien vaiheiden avulla.

1. Valitse **Varastonhallinta \> Asetukset \> Vapauta varastoon \> Lähetyksen konsolidointikäytännöt**.
1. Luo seuraavat käytännöt valitsemalla toimintoruudussa **Luo oletusasetukset**:

    - Käytäntö, jonka nimi on *Myyntitilaukset*-käytäntötyypin *Oletusarvo*.
    - Käytäntö, jonka nimi on *Siirtovarasto-otto*-käytäntötyypin *Oletusarvo*.
    - Käytäntö, jonka nimi on *Siirtovarasto-otto*-käytäntötyypin *Tilaustenvälinen*. (Tämä käytäntö luodaan vain, jos sinulla on vähintään yksi varasto, jossa vanha **Konsolidoi lähetys varastoon vapautettaessa** -asetus on otettu käyttöön.)
    - Käytäntö, jonka nimi on *Myyntitilaukset*-käytäntötyypin *Tilaustenvälinen*. (Tämä käytäntö luodaan vain, jos sinulla on vähintään yksi varasto, jossa vanha **Konsolidoi lähetys varastoon vapautettaessa** -asetus on otettu käyttöön.)

    > [!NOTE]
    > - Molemmissa *Tilaustenvälinen*-käytännöissä otetaan huomioon samat kenttäjoukot kuin aiemmassa logiikassa. Tilauksen numerokenttä otetaan kuitenkin myös huomioon. (Kyseisellä kentällä konsolidoidaan rivit lähetyksiksi esimerkiksi varaston, toimituksen kuljetustavan ja osoitteen perusteella.)
    > - Molemmissa *Oletusarvo*-käytännöissä otetaan huomioon samat kenttäjoukot kuin aiemmassa logiikassa. Tilauksen numerokenttä otetaan kuitenkin myös huomioon. (Kyseisellä kentällä konsolidoidaan rivit lähetyksiksi esimerkiksi tilausnumero, varaston, toimituksen kuljetustavan ja osoitteen perusteella.)

1. Jos järjestelmä loi *Myyntitilaukset*-käytäntötyypiksi *Tilaustenvälinen*-käytännön, valitse se ja valitse sitten toimintoruudussa **Muokkaa kyselyä**. Kyselyeditorissa näkyvissä on, missä varastossa **Konsolidoi lähetys varastoon vapautettaessa** -asetus oli aikaisemmin käytössä. Siksi tämä käytäntö sisältää näiden varastojen aiemmat asetukset.
1. Mukauta uusia oletuskäytäntöjä tarpeen mukaan lisäämällä tai poistamalla kenttiä ja/tai muokkaamalla kyselyitä. Voit myös lisätä tarvittavan määrän uusia käytäntöjä. Esimerkkejä käytäntöjen mukauttamisesta ja määrittämisestä on myöhemmin tämän artikkelin esimerkkiskenaariossa.

## <a name="scenario-configure-custom-shipment-consolidation-policies"></a>Skenaario: Lähetyksen mukautettujen konsolidointikäytäntöjen määrittäminen

Tässä skenaariossa on esimerkki siitä, miten mukautetun lähetyksen konsolidointikäytännöt määritetään ja miten ne testataan esittelytietojen avulla. Mukautetut käytännöt voivat tukea monimutkaisia liiketoimintavaatimuksia, joissa lähetyksen konsolidointi määräytyy useiden ehtojen perusteella. Kunkin tämän skenaarion esimerkkikäytäntö sisältää lyhyen liiketoimintatapauksen kuvauksen. Nämä esimerkkikäytännöt on määritettävä järjestyksessä, joka varmistaa kyselyjen alhaalta ylöspäin etenevän arvioinnin. (Toisin sanoen käytännöt, joissa on eniten ehtoja arvioidaan korkeimman prioriteetin käytäntönä.)

### <a name="make-demo-data-available"></a>Demotietojen ottaminen käyttöön

Tässä skenaariossa viitataan arvoihin ja tietueisiin, jotka sisältyvät Supply Chain Management -sovelluksen [vakiodemotietoihin](../../fin-ops-core/fin-ops/get-started/demo-data.md). Jos haluat käyttää harjoituksissa näitä annettuja arvoja, varmista, että demotiedot on asennettu työskentely-ympäristöön ja että yritykseksi on valittu *USMF* ennen aloittamista.

### <a name="prepare-master-data-for-this-scenario"></a>Päätietojen valmisteleminen tälle skenaariolle

Ennen kuin tämän skenaarion harjoituksia tehdään, suodatukseen tarvittavat päätiedot on valmisteltava jäljempänä annettavien ohjeiden mukaisesti. (Nämä edellytykset koskevat myös skenaarioluetteloa, joka on [Esimerkkiskenaarioita lähetyksen konsolidointikäytäntöjen käyttämisestä](#example-scenarios) -osassa.)

#### <a name="create-two-new-product-filter-codes"></a>Kahden uuden tuotteen suodatinkoodin luominen

1. Valitse **Varastonhallinta \> Asetukset \> Tuotesuodattimet \> Tuotesuodattimet** ja lisää kaksi tuotesuodatinta:

    - Tuotesuodatin 1:

        - **Suodatinkoodi:** *Tulenarka*
        - **Suodattimen otsikko:** *Koodi 4*

    - Tuotesuodatin 2:

        - **Suodatinkoodi:** *Räjähdysherkkä*
        - **Suodattimen otsikko:** *Koodi 4*

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Avaa tuote, jonka nimiketunnus on *M9200*. (Valitussa tuotteessa on oltava käytössä edistykselliset varastonhallintaprosessit \[WMS\] ja WMS-prosessit on otettu valmiiksi käyttöön tässä tuotteessa **USMF**-demotiedoissa.)
1. Valitse **Varasto**-pikavälilehdessä **Koodi 4** -kentän asetukseksi *Tulenarka*.
1. Sulje sivu.
1. Avaa tuote, jonka nimiketunnus on *M9201*. (Myös tämän tuotteen WMS-prosessit on otettu valmiiksi käyttöön **USMF**-demotiedoissa.)
1. Valitse **Varasto**-pikavälilehdessä **Koodi 4** -kentän asetukseksi *Räjähdysherkkä*.
1. Sulje sivu.

#### <a name="create-a-new-transportation-mode-of-delivery"></a>Toimituksen uuden kuljetustavan luonti

1. Valitse **Kuljetustenhallinta \> Asetukset \> Rahdinkuljettajat \> Tila**.
1. Luo konsolidointikyselyissä käytettävä kuljetustapa ja anna sen nimeksi *Airways*.
1. Valitse **Kuljetustenhallinta \> Asetukset \> Rahdinkuljettajat \> Lähetyksen rahdinkuljettajat**.
1. Luo rahdinkuljettaja, jossa on seuraavat asetukset:

    - **Rahdinkuljettaja:** *Lento*
    - **Nimi:** *Lento*
    - **Tila:** *Lento*

1. Lisää uuden rahdinkuljettaja **Palvelut**-pikavälilehteen rivi, jossa on seuraavat asetukset:

    - **Rahdinkuljetuspalvelu:** *Ilma*
    - **Kuljetusmenetelmä:** *Ilma*

1. Valitse toimintoruudussa **Tallenna**.

    > [!NOTE]
    > Kun tallennat uuden rahdinkuljettajan, **Palvelut**-ruudukon uuden rivin **Toimitustapa**-kentän asetuksena on automaattisesti *Lento-Ilma*. Kun myyntitilauksen *Lento-Ilma*-toimitustapaa käytetään, *Lento*-kuljetustapaa käytetään liittyvissä lähetyksissä.

#### <a name="create-an-order-pool"></a>Tilauspoolin luominen

1. Valitse **Myynti ja markkinointi \> Asetukset \> Myyntitilaukset \> Tilauspoolit**.
1. Luo konsolidointikyselyssä käytettävä tilauspooli. Tilauspoolissa on oltava seuraavat asetukset:

    - **Pooli:** anna kokonaisluku, jota ei vielä käytetä muissa pooleissa.
    - **Nimi:** *ShipCons*

1. Valitse **Myynti ja markkinointi \> Asiakkaat \> Kaikki asiakkaat**.
1. Avaa asiakas, jonka asiakasnumero on *US-003*.
1. Valitse **Oletusmyyntitilaukset**-pikavälilehden **Myyntitilauspooli**-kentän asetukseksi juuri luotu tilauspooli.
1. Sulje sivu ja toista sitten vaiheet 4 ja 5 asiakkaalle, jonka asiakasnumero on *US-004*.

### <a name="create-example-policy-1"></a>Esimerkkikäytännön 1 luominen

Tässä esimerkissä luodaan *Asiakas+tila*-käytäntö, jota käytetään seuraavassa liiketoimintatapauksessa:

- Käytäntö tekee tietyn asiakastilin (*US-001*) ja tietyn toimitustavan (*Lento-Ilma*) kyselyn.
- Avoimien lähetysten konsolidointi on poistettu käytöstä.
- Konsolidointi tehdään tilauksentunnuksittain. (Toisin sanoen esimerkiksi tilaus- ja varastokohtaiset lähetykset ovat erillisiä.)

Luo tälle liiketoimintatapaukselle lähetyksen konsolidointikäytäntö seuraavasti:

1. Valitse **Varastonhallinta \> Asetukset \> Vapauta varastoon \> Lähetyksen konsolidointikäytännöt**.
1. Määritä **Käytännön tyyppi** -kentän asetukseksi *Myyntitilaukset*.
1. Luo uusi käytäntö, jossa on seuraavat asetukset valitsemalla toimintoruudussa **Uusi**:

    - **Käytännön nimi:** *CustomerMode*
    - **Käytännön kuvaus:** *Asiakastili ja toimitustapa*

1. Jätä **Avoimien lähetysten konsolidointi** -asetukseksi *Ei*.
1. Valitse toimintoruudussa **Tallenna**.
1. Valitse **Konsolidointikentät**-pikavälilehden **Jäljellä olevat kentät** -luettelossa rivi, jossa **Kentän nimi** -kentän asetuksena *Toimitustapa*.
1. Valitse **Lisää**-painike ![Oikea nuoli.](media/forward-button.png) siirtääksesi kentän **Valitut kentät** -luetteloon.
1. Valitse toimintoruudussa **Muokkaa kyselyä**.
1. Etsi kyselyeditorin valintaikkunan ruudukon **Alue**-välilehdessä rivi, jossa **Kenttä**-kentän asetuksena on *Asiakastili*, ja määritä kyseisen rivin **Ehdot**-kentän aseetukseksi *US-001*.
1. Lisää seuraavat asetukset sisältävä rivi ruudukkoon valitsemalla **Lisää**:

    - **Taulu:** *Tilausrivit*
    - **Johdettu taulu:** *Tilausrivit*
    - **Kenttä:** *Toimitustapa*
    - **Ehdot:** *Lento-Ilma*

1. Sulje valintaikkuna valitsemalla **OK**.

> [!NOTE]
> Tässä liiketoimintatapauksessa asiakkaan *US-001* *Lento-Ilma*-toimitustapaa käyttäviä tilausrivejä ei konsolidoida tilausten välillä. Tämä käytäntö on tarkoitettu käytettäväksi ensimmäisenä tapauksissa, joissa kyseisen asiakkaan kaikkien muiden toimitustapojen lähetykset konsolidoidaan.

### <a name="create-example-policy-2"></a>Esimerkkikäytännön 2 luominen

Tässä esimerkissä luodaan *Vaaralliset tuotteet* -käytäntö, jota käytetään seuraavassa liiketoimintatapauksessa:

- Käytäntö tekee tietyn suodatinkoodin (*vaarallinen*) ja tietyn toimitustavan (*Lento-Ilma*) kyselyn.
- Avoimien lähetysten konsolidointi on otettu käyttöön.
- Konsolidointi tehdään tilausten välillä. (Toisin sanoen esimerkiksi asiakas- ja varastokohtaiset lähetykset ovat erillisiä mutta vain kyselyssä määritetyssä nimikeryhmässä.)

Luo tälle liiketoimintatapaukselle lähetyksen konsolidointikäytäntö seuraavasti:

1. Valitse **Varastonhallinta \> Asetukset \> Vapauta varastoon \> Lähetyksen konsolidointikäytännöt**.
1. Määritä **Käytännön tyyppi** -kentän asetukseksi *Myyntitilaukset*.
1. Luo uusi käytäntö, jossa on seuraavat asetukset valitsemalla toimintoruudussa **Uusi**:

    - **Käytännön nimi:** *Nimiketyyppi*
    - **Käytännön kuvaus:** *Saman nimiketyypin konsolidointi tilausten välillä*

1. Määritä **Avoimien lähetysten konsolidointi** -asetukseksi *Kyllä*.
1. Valitse toimintoruudussa **Tallenna**.
1. Valitse **Konsolidointikentät**-pikavälilehden **Jäljellä olevat kentät** -luettelossa rivi, jossa **Kentän nimi** -kentän asetuksena *Toimitustapa*.
1. Valitse **Lisää**-painike ![Oikea nuoli.](media/forward-button.png) siirtääksesi kentän **Valitut kentät** -luetteloon.
1. Valitse toimintoruudussa **Muokkaa kyselyä**.
1. Laajenna ja valitse kyselyeditorin valintaruudun **Liitokset**-välilehdessä **Taulut \> Kuorman tiedot**.
1. Valitse **Lisää taulun liitos**.
1. Etsi ja valitse avautuvassa suhderuudukossa rivi, jossa **Suhde**-kentän asetuksena on *Varastonimikkeen tunnus (nimiketunnus)*, ja valitse sitten **Valitse**. 
1. Lisää seuraavat asetukset sisältävä rivi ruudukkoon valitsemalla **Alue**-välilehdessä **Lisää**:

    - **Taulu:** *Varastonimikkeen tunnus*
    - **Johdettu taulu:** *Varastonimikkeen tunnus*
    - **Kenttä:** *Koodi 4*
    - **Ehdot:** *Tulenarka*

1. Sulje valintaikkuna valitsemalla **OK**.

> [!NOTE]
> Tässä liiketoimintatapauksessa kaikki tilausrivit, jossa nimikkeillä on tietty suodatinkoodi (eli suodatinkoodi, jossa **Koodi 4** -kentän asetuksena on *Tulenarka*) konsolidoidaan muiden saman tyyppisten nimikkeiden kanssa tilausten välillä. Jos samalla tilillä, varastolla ja nimikeryhmällä on avoin lähetys, uudet rivit lisätään siihen.

### <a name="create-example-policy-3"></a>Esimerkkikäytännön 3 luominen

Tässä esimerkissä luodaan *Asiakkaan vaatimukset* -käytäntö, jota käytetään seuraavassa liiketoimintatapauksessa:

- Käytäntö tekemä kysely kohdistuu tiettyyn asiakastiliin.
- Avoimien lähetysten konsolidointi on otettu käyttöön.
- Konsolidointi tehdään tilausten välillä, mutta se perustuu asiakkaan tilauksiin. (Toisin sanoen useita tilauksia ryhmitetään lähetetyiksi saman asiakkaan tilausnumeron ja varaston perusteella.)

Luo tälle liiketoimintatapaukselle lähetyksen konsolidointikäytäntö seuraavasti:

1. Valitse **Varastonhallinta \> Asetukset \> Vapauta varastoon \> Lähetyksen konsolidointikäytännöt**.
1. Määritä **Käytännön tyyppi** -kentän asetukseksi *Myyntitilaukset*.
1. Luo uusi käytäntö, jossa on seuraavat asetukset valitsemalla toimintoruudussa **Uusi**:

    - **Käytännön nimi:** *CustomerOrderNo*
    - **Käytännön kuvaus:** *asiakkaan ostotilauksen rivien konsolidointi*

1. Määritä **Avoimien lähetysten konsolidointi** -asetukseksi *Kyllä*.
1. Valitse toimintoruudussa **Tallenna**.
1. Valitse **Konsolidointikentät**-pikavälilehden **Jäljellä olevat kentät** -luettelossa rivi, jossa **Kentän nimi** -kentän asetuksena on *Asiakkaan tilaus*.
1. Valitse **Lisää**-painike ![Oikea nuoli.](media/forward-button.png) siirtääksesi kentän **Valitut kentät** -luetteloon.
1. Valitse **Jäljellä olevat kentät** -luettelossa rivi, jossa **Kentän nimi** -kentän asetuksena *Toimitustapa*.
1. Valitse **Lisää**-painike ![Oikea nuoli.](media/forward-button.png) siirtääksesi kentän **Valitut kentät** -luetteloon.
1. Valitse toimintoruudussa **Muokkaa kyselyä**.
1. Etsi kyselyeditorin valintaikkunan **Alue**-välilehdessä rivi, jossa **Kenttä**-kentän asetuksena on *Asiakastili*, ja määritä kyseisen rivin **Ehdot**-kentän asetukseksi *US-001*.
1. Sulje valintaikkuna valitsemalla **OK**.

> [!NOTE]
> Tässä liiketoimintatapauksessa kaikki tilausrivit, joissa myyntitilauksissa on sama asiakkaan varasto-ottoehdotus, konsolidoidaan yhdeksi lähetykseksi myyntitilauksen numerosta riippumatta. (Asiakkaan tilausnumeroa käytetään asiakkaan ostotilauksen \[PO\]-numerona.) Jos samalla tilillä, samassa varastossa ja samassa asiakkaan tilauksessa on avoin lähetys, uudet rivit liitetään siihen. Tätä käytäntöä käytetään, jos asiakas lähettää ylimääräiset tilausrivit, joilla on sama PO-numero, useita kertoja päivän aikana ja haluaa, että kaikki rivit ryhmitetään yhdeksi lähetykseksi. (Toisin sanoen käytössä on yksi rahtikirja ja yksi pakkausluettelo.)

### <a name="create-example-policy-4"></a>Esimerkkikäytännön 4 luominen

Tässä esimerkissä luodaan *Asiakkaat sallivat konsolidoinnin* -käytäntö, jota käytetään seuraavassa liiketoimintatapauksessa:

- Käytäntö tekee kyselyn tietyssä tilauspoolissa lähetysten konsolidoinnin sallivien asiakkaiden tunnistamiseksi.
- Avoimien lähetysten konsolidointi on poistettu käytöstä.
- Konsolidointi tehdään asetusten välillä käyttämällä Tilaustenvälinen-oletuskäytännön valitsemia kenttiä (jolla toisinnetaan aiempi **Konsolidoi lähetys luovutettaessa varastoon**-valintaruutu).

- Voit ohittaa myyntitilauksen säännön valitsemalla toisen tilauspoolin.

Luo tälle liiketoimintatapaukselle lähetyksen konsolidointikäytäntö seuraavasti:

1. Valitse **Varastonhallinta \> Asetukset \> Vapauta varastoon \> Lähetyksen konsolidointikäytännöt**.
1. Määritä **Käytännön tyyppi** -kentän asetukseksi *Myyntitilaukset*.
1. Luo uusi käytäntö, jossa on seuraavat asetukset valitsemalla toimintoruudussa **Uusi**:

    - **Käytännön nimi:** *Tilauspooli*
    - **Käytännön kuvaus:** *Tilauspooliin perustuva tilausten välinen konsolidointi*

1. Jätä **Avoimien lähetysten konsolidointi** -asetukseksi *Ei*.
1. Valitse toimintoruudussa **Tallenna**.
1. Valitse **Konsolidointikentät**-pikavälilehden **Jäljellä olevat kentät** -luettelossa rivi, jossa **Kentän nimi** -kentän asetuksena *Toimitustapa*.
1. Valitse **Lisää**-painike ![Oikea nuoli.](media/forward-button.png) siirtääksesi kentän **Valitut kentät** -luetteloon.
1. Valitse toimintoruudussa **Muokkaa kyselyä**.
1. Lisää kyselyeditoriin valintaikkunassa seuraavat asetukset sisältävä rivi ruudukkoon valitsemalla **Alue**-välilehdessä **Lisää**:

    - **Taulu:** *Myyntitilaukset*
    - **Johdettu taulu:** *Myyntitilaukset*
    - **Kenttä:** *Pooli*
    - **Ehdot:** *ShipCons*

1. Sulje valintaikkuna valitsemalla **OK**.

> [!NOTE]
> Tässä liiketoimintatapauksessa kaikki tilausrivit, joilla myyntitilaukset kuuluvat samaan tilauspooliin, konsolidoidaan yhdeksi saman tilin, varaston ja kuljetuksen toimitustavan myyntitilausten väliseksi lähetykseksi. Asiakasryhmän erottamiseen voi käyttää tilauspoolin sijaan mitä tahansa muuta kenttää, ja myyntiotsikon otsikkoa voi käyttää oletusarvoisesti. Tätä menetelmää voi käyttää, jos konsolidointi perustuu asiakkaaseen eikä varastoon. (Aiemmassa konsolidointilogiikassa konsolidointitarve perustui varastoon.)

### <a name="create-example-policy-5"></a>Esimerkkikäytännön 5 luominen

Tässä esimerkissä luodaan *Varastot sallivat konsolidoinnin* -käytäntö, jota käytetään seuraavassa liiketoimintatapauksessa:

- Käytäntö tekee kyselyn tietyssä tilauspoolissa lähetyksiä konsolidoivien varastojen tunnistamiseksi.
- Avoimien lähetysten konsolidointi on poistettu käytöstä.
- Konsolidointi tehdään asetusten välillä käyttämällä Tilaustenvälinen-oletuskäytännön valitsemia kenttiä (jolla toisinnetaan aiempi **Konsolidoi lähetys luovutettaessa varastoon**-valintaruutu).

Yleensä tämä liiketoimintatapauksessa käytetään kohdassa [Määritä alkuperäiset konsolidointikäytännöt](#initial-policies) luotujen oletuskäytäntöjen avulla. Samanlaisia käytäntöjä voi kuitenkin luoda myös seuraavien ohjeiden mukaisesti:

1. Valitse **Varastonhallinta \> Asetukset \> Vapauta varastoon \> Lähetyksen konsolidointikäytännöt**.
1. Määritä **Käytännön tyyppi** -kentän asetukseksi *Myyntitilaukset*.
1. Luo uusi käytäntö, jossa on seuraavat asetukset valitsemalla toimintoruudussa **Uusi**:

    - **Käytännön nimi:** *Tilaustenvälinen*
    - **Käytännön kuvaus:** *tiettyjen varastojen tilausten välinen konsolidointi*

1. Jätä **Avoimien lähetysten konsolidointi** -asetukseksi *Ei*.
1. Valitse toimintoruudussa **Tallenna**.
1. Valitse **Konsolidointikentät**-pikavälilehden **Jäljellä olevat kentät** -kentässä rivi, jossa **Kentän nimi** -kentän asetuksena on *Toimitustapa*.
1. Valitse **Lisää**-painike ![Oikea nuoli.](media/forward-button.png) siirtääksesi kentän **Valitut kentät** -luetteloon.
1. Valitse toimintoruudussa **Muokkaa kyselyä**.
1. Etsi kyselyeditorin valintaikkunan **Alue**-välilehdessä rivi, jossa **Kenttä**-kentän asetuksena on *Varasto*, ja määritä kyseisen rivin **Ehdot**-kentän asetukseksi *61, 63*.
1. Sulje valintaikkuna valitsemalla **OK**.

### <a name="set-the-order"></a>Järjestyksen määrittäminen

Nyt kun kaikki käytännöt on luotu, niiden käyttöjärjestys on määritettävä. Käytäntöjä voidaan arvioida seuraavasti alhaalta ylöspäin niin, että käytäntöjen, joissa on eniten ehtoja, prioriteetti on korkein:

1. Valitse **Varastonhallinta \> Asetukset \> Vapauta varastoon \> Lähetyksen konsolidointikäytännöt**.
1. Määritä **Käytännön tyyppi** -kentän asetukseksi *Myyntitilaukset*.
1. Valitse kukin vasemmassa sarakkeessa oleva käytäntö ja järjestä käytännöt sitten seuraavaan järjestykseen toimintoruudun **Siirrä ylös**- ja **Siirrä alas** -painikkeita.

    1. CustomerMode
    1. Nimiketyyppi
    1. CustomerOrderNo
    1. Tilauspooli
    1. Tilaustenvälinen
    1. Oletusarvo

## <a name="example-scenarios-of-how-to-use-shipment-consolidation-policies"></a><a name="example-scenarios"></a> Esimerkkiskenaarioita lähetyksen konsolidointikäytäntöjen käyttämisestä

Seuraavat skenaariot näyttävät, miten tämän artikkelin mukaisesti luotuja lähetyksen konsolidointikäytäntöjä voidaan käyttää. Kukin skenaario käsittelee lähetyksen konsolidointiprosessia, joka käyttää lähetyksen konsolidointikäytäntöjä automaattisen tai manuaaliseen varastoon vapautuksen aikana:

- Skenaario 1: [Lähetysten konsolidointi, kun ne vapautetaan varastoon myyntitilausten automaattisella vapauttamisella](../warehousing/consolidate-shipments-automatic.md)
- Skenaario 2: [Lähetysten konsolidointi, kun lähetyksen konsolidointikäytäntö korvataan Vapauta varastoon -sivulla](../warehousing/consolidate-shipments-release-to-warehouse-override.md)
- Skenaario 3: [Lähetysten konsolidointi käyttämällä Vapauta varastoon -toimintoa kuormasuunnittelun työtilassa](../warehousing/consolidate-shipments-load-planning-workbench.md)
- Skenaario 4: [Lähetysten konsolidointi käyttämällä lähetyksen konsolidoinnin työtilaa](../warehousing/consolidate-shipments-manual-workbench.md)
- Skenaario 5: [Lähetysten konsolidointi manuaalisesti käyttämällä Konsolidoi lähetykset -sivua](../warehousing/consolidate-shipments-manual-form.md)


## <a name="additional-resources"></a>Lisäresurssit

- [Lähetyksen konsolidointikäytäntöjen yleiskatsaus](about-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
