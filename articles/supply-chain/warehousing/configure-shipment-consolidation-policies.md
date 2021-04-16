---
title: Lähetyksen konsolidointikäytäntöjen määrittäminen
description: Tässä ohjeaiheessa käsitellään lähetyksen oletusarvoisten ja mukautettujen konsolidointikäytäntöjen määrittämistä.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, TMSMode, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 03150ccdaeaf48754f04a4329cb1bc14ea2b6895
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840410"
---
# <a name="configure-shipment-consolidation-policies"></a>Lähetyksen konsolidointikäytäntöjen määrittäminen

[!include [banner](../includes/banner.md)]

Lähetyksen konsolidointikäytäntöjä käyttävän lähetyksen konsolidointiprosessin avulla voidaan tehdä automaattinen lähetyksen konsolidointi automaattisen ja manuaaliseen varastoon vapautuksen aikana. Ensimmäiset käytännöt on määritettävä, kun toiminto otetaan käyttöön. Jos käytäntöjä ei määritetä, jokainen myyntirivi luo erillisen lähetyksen, jossa on yksi kuormarivi.

Tämän ohjeaiheen skenaarioiden avulla näytetään, miten määritetään oletusarvoiset ja mukautetut lähetyksen konsolidointikäytännöt.

## <a name="turn-on-the-shipment-consolidation-policies-feature"></a>Lähetyksen konsolidointikäytäntötoiminnon ottaminen käyttöön

> [!IMPORTANT]
> Ohjeaiheen [ensimmäisessä skenaariossa](#scenario-1) määritetään ensin varasto siten, että se käyttää aiemman lähetyksen konsolidointitoimintoa. Tämän jälkeen otetaan käyttöön lähetyksen konsolidointikäytännöt. Tällä tavoin näytetään, miten päivitysskenaario toimii. Jos ensimmäisessä skenaariossa on tarkoitus käyttää demotietoympäristöä, älä ota toimintoa käyttöön ennen skenaarioon toteuttamista.

*Lähetyksen konsolidointikäytännöt* -toiminto on otettava järjestelmässä käyttöön, ennen kuin sitä voi käyttää. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Toiminnon nimi:** *Lähetyksen konsolidointi*

## <a name="make-demo-data-available"></a>Demotietojen ottaminen käyttöön

Ohjeaiheen kaikissa skenaarioissa viitataan arvoihin ja tietueisiin, jotka sisältyvät Microsoft Dynamics 365 Supply Chain Managementin vakiodemotietoihin. Jos haluat käyttää harjoituksissa näitä annettuja arvoja, varmista, että demotiedot on asennettu työskentely-ympäristöön ja että yritykseksi on valittu **USMF** ennen aloittamista.

## <a name="scenario-1-configure-default-shipment-consolidation-policies"></a><a name="scenario-1"></a>Skenaario 1: Lähetyksen oletusarvoisten konsolidointikäytäntöjen määrittäminen

Sen jälkeen kun *Lähetyksen konsolidointikäytännöt* -toiminto on otettu käyttöön, vähimmäismäärä oletuskäytäntöjä on määritettävä kahdessa tilanteessa:

- päivitettävässä ympäristössä on jo tietoja
- määritettävänä on täysin uusi ympäristö.

### <a name="upgrade-an-environment-where-warehouses-are-already-configured-for-cross-order-consolidation"></a>Ympäristön päivittäminen, kun tilausten välinen konsolidointi on jo määritetty varastoissa

Kun tämä menettely aloitetaan, *Lähetyksen konsolidointikäytännöt* -toiminnon on oltava pois käytöstä, sillä vain niin voidaan simuloida ympäristöä, jossa on jo käytössä perustason tilausten välinen konsolidointitoiminto. Toiminto otetaan sitten käyttöön ominaisuuden hallinnassa, jolloin saat tietää, miten lähetyksen konsolidointikäytännöt määritetään päivityksen jälkeen.

Oletusarvoiset lähetyksen konsolidointikäytännöt määritetään seuraavien ohjeiden avulla ympäristössä, joissa tilausten välinen konsolidointi on jo määritetty varastoissa.

1. Valitse **Varastonhallinta \> Asetukset \> Varasto \> Varastot**.
1. Etsi ja avaa luettelossa sopiva varastotietue (kuten varasto *24* **USMF**-demotiedoissa).
1. Valitse toimintoruudussa **Muokkaa**.
1. Valitse **Varasto**-pikavälilehdessä **Konsolidoi lähetys varastoon vapautettaessa** -asetukseksi *Kyllä*.
1. Toista vaiheet 2–4 kaikissa varastoissa, joissa on tehtävä konsolidointi.
1. Sulje sivu.
1. Ota *Lähetyksen konsolidointikäytännöt* -toiminto käyttöön [toiminnon hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). **Toiminnon hallinta** -työtilassa toiminnon nimi on *Lähetyksen konsolidointi*.
1. Valitse **Varastonhallinta \> Asetukset \> Vapauta varastoon \> Lähetyksen konsolidointikäytännöt**. Selain on ehkä päivitettävä, ennen kuin uusi **Lähetyksen konsolidointikäytännöt** -valikkovaihtoehto näkyy toiminnon käyttöönottamisen jälkeen.
1. Luo seuraavat käytännöt valitsemalla toimintoruudussa **Luo oletusasetukset**:

    - *Myyntitilaukset*-käytäntötyypin **Tilaustenvälinen**-käytäntö (mikäli vähintään yksi varasto on määritetty käyttämään aiempaa konsolidointitoimintoa)
    - *Myyntitilaukset*-käytäntötyypin **Oletus**-käytäntö
    - *Siirtovarasto-otto*-käytäntötyypin **Oletus**-käytäntö
    - *Siirtovarasto-otto*-käytäntötyypin **Tilaustenvälinen**-käytäntö (mikäli vähintään yksi varasto on määritetty käyttämään aiempaa konsolidointitoimintoa)

    > [!NOTE]
    > - Molemmissa **Tilaustenvälinen**-käytännöissä otetaan huomioon samat kenttäjoukot kuin aiemmassa logiikassa tilausnumerokenttää lukuun ottamatta. (Kyseisellä kentällä konsolidoidaan rivit lähetyksiksi esimerkiksi varaston, toimituksen kuljetustavan ja osoitteen perusteella.)
    > - Molemmissa **Oletus**-käytännöissä otetaan huomioon samat kenttäjoukot kuin aiemmassa logiikassa tilausnumerokenttää mukaan lukien. (Kyseisellä kentällä konsolidoidaan rivit lähetyksiksi esimerkiksi tilausnumero, varaston, toimituksen kuljetustavan ja osoitteen perusteella.)

1. Valitse *Myyntitilaukset*-käytäntötyypiksi **Tilaustenvälinen**-käytäntö ja valitse sitten toimintoruudussa **Muokkaa kyselyä**.
1. Kiinnitä huomiota kyselyeditorin valintaikkunassa on luettelo, jossa varastojen **Konsolidoi lähetys varastoon vapautettaessa** -asetukseksi on määritetty *Kyllä*. Tämän vuoksi ne sisältyvät kyselyyn.

### <a name="create-default-policies-for-a-new-environment"></a>Uuden ympäristön oletuskäytäntöjen luominen

Määritä lähetyksen oletusarvoiset konsolidointikäytännöt seuraavien ohjeiden mukaisesti:

1. Ota *Lähetyksen konsolidointikäytännöt* -toiminto käyttöön [toiminnon hallinnassa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), jos toimintoa ei ole vielä otettu käyttöön. **Toiminnon hallinta** -työtilassa toiminnon nimi on *Lähetyksen konsolidointi*.
1. Valitse **Varastonhallinta \> Asetukset \> Vapauta varastoon \> Lähetyksen konsolidointikäytännöt**.
1. Luo seuraavat käytännöt valitsemalla toimintoruudussa **Luo oletusasetukset**:

    - *Myyntitilaukset*-käytäntötyypin **Oletus**-käytäntö
    - *Siirtovarasto-otto*-käytäntötyypin **Oletus**-käytäntö

    > [!NOTE]
    > Molemmissa **Oletus**-käytännöissä otetaan huomioon samat kenttäjoukot kuin aiemmassa logiikassa tilausnumerokenttää mukaan lukien. (Kyseisellä kentällä konsolidoidaan rivit lähetyksiksi esimerkiksi tilausnumero, varaston, toimituksen kuljetustavan ja osoitteen perusteella.)

## <a name="scenario-2-configure-custom-shipment-consolidation-policies"></a>Skenaario 2: Lähetyksen mukautettujen konsolidointikäytäntöjen määrittäminen

Tässä skenaariossa näytetään, miten lähetyksen mukautetut konsolidointikäytännöt määritetään. Mukautetut käytännöt voivat tukea monimutkaisia liiketoimintavaatimuksia, joissa lähetyksen konsolidointi määräytyy useiden ehtojen perusteella. Kunkin tämän skenaarion esimerkkikäytäntö sisältää lyhyen liiketoimintatapauksen kuvauksen. Nämä esimerkkikäytännöt on määritettävä järjestyksessä, joka varmistaa kyselyjen alhaalta ylöspäin etenevän arvioinnin. (Toisin sanoen käytännöt, joissa on eniten ehtoja arvioidaan korkeimman prioriteetin käytäntönä.)

### <a name="turn-on-the-feature-and-prepare-master-data-for-this-scenario"></a>Toiminnon ottaminen käyttöön ja skenaarion päätietojen valmisteleminen

Ennen kuin tämän skenaarion harjoituksia tehdään, toiminto on otettava käyttöön ja suodatukseen tarvittavat päätiedot on valmisteltava jäljempänä annettavien ohjeiden mukaisesti. (Nämä edellytykset koskevat myös skenaarioluetteloa, joka on kohdassa [Esimerkkiskenaarioita lähetyksen konsolidointikäytäntöjen käyttämisestä](#example-scenarios).)

#### <a name="turn-on-the-feature-and-create-the-default-policies"></a>Toiminnon ottaminen käyttöön ja oletuskäytäntöjen luominen

Ota toiminto käyttöön toimintojen hallinnassa, jos sitä ei ole vielä otettu käyttöön, ja luo [skenaariossa 1](#scenario-1) kuvatut oletuskonsolidointikäytännöt.

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
1. Siirrä kenttä **Valitut kentät** -luetteloon valitsemalla **Lisää**-painike ![oikea nuoli](media/forward-button.png).
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
1. Siirrä kenttä **Valitut kentät** -luetteloon valitsemalla **Lisää**-painike ![oikea nuoli](media/forward-button.png).
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
1. Siirrä kenttä **Valitut kentät** -luetteloon valitsemalla **Lisää**-painike ![oikea nuoli](media/forward-button.png).
1. Valitse **Jäljellä olevat kentät** -luettelossa rivi, jossa **Kentän nimi** -kentän asetuksena *Toimitustapa*.
1. Siirrä kenttä **Valitut kentät** -luetteloon valitsemalla **Lisää**-painike ![oikea nuoli](media/forward-button.png).
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
1. Siirrä kenttä **Valitut kentät** -luetteloon valitsemalla **Lisää**-painike ![oikea nuoli](media/forward-button.png).
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

Yleensä tämä liiketoimintatapaus otetaan huomioon käyttämällä [skenaariossa 1](#scenario-1) luotoja oletuskäytäntöjä. Samanlaisia käytäntöjä voi kuitenkin luoda myös seuraavien ohjeiden mukaisesti:

1. Valitse **Varastonhallinta \> Asetukset \> Vapauta varastoon \> Lähetyksen konsolidointikäytännöt**.
1. Määritä **Käytännön tyyppi** -kentän asetukseksi *Myyntitilaukset*.
1. Luo uusi käytäntö, jossa on seuraavat asetukset valitsemalla toimintoruudussa **Uusi**:

    - **Käytännön nimi:** *Tilaustenvälinen*
    - **Käytännön kuvaus:** *tiettyjen varastojen tilausten välinen konsolidointi*

1. Jätä **Avoimien lähetysten konsolidointi** -asetukseksi *Ei*.
1. Valitse toimintoruudussa **Tallenna**.
1. Valitse **Konsolidointikentät**-pikavälilehden **Jäljellä olevat kentät** -kentässä rivi, jossa **Kentän nimi** -kentän asetuksena on *Toimitustapa*.
1. Siirrä kenttä **Valitut kentät** -luetteloon valitsemalla **Lisää**-painike ![oikea nuoli](media/forward-button.png).
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

Seuraavat skenaariot näyttävät, miten tämän ohjeaiheen mukaisesti luotuja lähetyksen konsolidointikäytäntöjä voidaan käyttää. Kukin skenaario käsittelee lähetyksen konsolidointiprosessia, joka käyttää lähetyksen konsolidointikäytäntöjä automaattisen tai manuaaliseen varastoon vapautuksen aikana:

- Skenaario 1: [Lähetysten konsolidointi, kun ne vapautetaan varastoon myyntitilausten automaattisella vapauttamisella](../warehousing/consolidate-shipments-automatic.md)
- Skenaario 2: [Lähetysten konsolidointi, kun lähetyksen konsolidointikäytäntö korvataan Vapauta varastoon -sivulla](../warehousing/consolidate-shipments-release-to-warehouse-override.md)
- Skenaario 3: [Lähetysten konsolidointi käyttämällä Vapauta varastoon -toimintoa kuormasuunnittelun työtilassa](../warehousing/consolidate-shipments-load-planning-workbench.md)
- Skenaario 4: [Lähetysten konsolidointi käyttämällä lähetyksen konsolidoinnin työtilaa](../warehousing/consolidate-shipments-manual-workbench.md)
- Skenaario 5: [Lähetysten konsolidointi manuaalisesti käyttämällä Konsolidoi lähetykset -sivua](../warehousing/consolidate-shipments-manual-form.md)


## <a name="additional-resources"></a>Lisäresurssit

- [Lähetyksen konsolidoinnin käytännöt](about-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]