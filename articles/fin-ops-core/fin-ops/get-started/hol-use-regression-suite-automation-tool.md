---
title: Regression Suite Automation Tool -oppaan käyttäminen
description: Tässä ohjeaiheessa käsitellään Regression Suite Automation Tool (RSAT) -työkalun käyttämistä. Siinä käsitellään erilaisia toimintoja ja annetaan esimerkkejä edistyneestä komentosarjojen käytöstä.
author: kfend
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 6cdaa89fb6d50ebaaaefe7f92d7224a1567d17d1
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070817"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a>Regression Suite Automation Tool -oppaan käyttäminen

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Lataa ja tallenna tämä ohje selaimen työkaluilla PDF-tiedostona. 

Tässä oppaassa käsitellään yksityiskohtaisesti Regression Suite Automation Tool (RSAT) -työkalun lisätoimintoja. Se sisältää myös demon määrityksen ja siinä käsitellään strategiaa ja keskeisiä opittavia asioita.

## <a name="features-of-rsattask-recorder"></a>RSAT-työkalun ja tehtävän tallennustoiminnon toiminnot

### <a name="validate-a-field-value"></a>Kentän arvon tarkistaminen

Lisätietoja tästä toiminnosta on kohdassa [Uuden tarkistustoiminnon sisältävän tehtävätallenteen luominen](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).

### <a name="saved-variable"></a>Tallennettu muuttuja

Lisätietoja tästä toiminnosta on kohdassa [Tallennetun muuttujan luominen muokkaamalla aiemmin luotua tehtävätallennetta](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).

### <a name="derived-test-case"></a>Johdettu testitapaus

1. Avaa Regression Suite Automation Tool (RSAT) ja valitse molemmat kohdassa [Regression Suite Automation Tool -opetusohjelman määrittäminen ja asentaminen](./hol-set-up-regression-suite-automation-tool.md) luodut testitapaukset.
2. Valitse **Uusi \> Luo johdettu testitapaus**.

    ![Luo johdettu testitapaus -komento Uusi-valikossa](./media/use_rsa_tool_01.png)

3. Näyttöön avautuva sanoma ilmoittaa, että jokaiselle nykyisessä testisarjassa valitulle testitapauksella luodaan johdettu testitapaus ja että jokaisella johdetulla testitapauksella on oma Excelin parametritiedoston kopio. Valitse **OK**.

    > [!NOTE]
    > Suoritettava testitapaus käyttää päätestitapauksen tehtävätallennetta ja omaa Excelin parametritiedoston kopioita. Tällä tavoin voit suorittaa saman testi eri parametreilla käyttämällä samaa tehtävätallennetta. Johdetun testitapauksen ei tarvitse kuulua samaan testisarjaan kuin sen päätestitapaus.

    ![Viestiruutu](./media/use_rsa_tool_02.png)

    Kaksi muuta johdettua testitapausta luodaan ja niille valitaan **Johdettu?** -valintaruutu.

    ![Luodut johdetut testitapaukset](./media/use_rsa_tool_03.png)

    Johdettu testitapaus luodaan automaattisesti Azure DevOpsissa. Se on **Luo uusi tuote** -testitapauksen alinimike ja siihen merkitään erityinen avainsana: **RSAT:DerivedTestSteps**. Lisäksi nämä testitapaukset lisätään automaattisesti testisuunnitelmaan Azure DevOpsissa.

    ![RSAT: DerivedTestSteps-avainsana](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > Jos luodut johdetut testitapaukset eivät jostain syytä ole oikeassa järjestyksessä, siirry Azure DevOps ja järjestä testisarjan testitapaukset uudelleen, jotta RSAT voi suorittaa ne oikeassa järjestyksessä.

4. Valitse ensin johdetut testitapaukset ja avaa sitten vastaavat Excelin parametritiedostot valitsemalla **Muokkaa**.
5. Muokkaa näitä Excelin parametritiedostoja samalla tavalla kuin muokkasit päätiedostoja. Toisen sanoen varmista, että tuotetunnus on määritetty automaattisesti luotavaksi. Varmista myös, että tallennettu muuttuja kopioidaan soveltuviin kenttiin.
6. Päivitä Excelin parametritiedoston **Yleiset**-välilehdessä **Yritys**-kentän arvoksi **USSI**. Tällä tavoin johdetut testitapaukset suoritetaan eri yrityksen perusteella kuin päätestitapaus. Jos haluat suorittaa testitapauksia tietyn käyttäjän (tai tiettyyn käyttäjään liitetyn roolin) osalta, voit päivittää **Testikäyttäjä**-kentän arvon.
7. Valitse **Suorita** ja tarkista, että tuote on luotu sekä USMF-yrityksessä että USSI-yrityksessä.

### <a name="validate-notifications"></a>Ilmoitusten tarkistaminen

Tällä toiminnolla tarkistetaan, tapahtuiko toiminto. Kun esimerkiksi tuotantotilaus luodaan, arvioidaan ja aloitetaan, sovellus ilmoittaa Tuotanto - käynnistys -sanomalla, että tuotantotilaus on aloitettu.

![Tuotanto - käynnistys -ilmoitus](./media/use_rsa_tool_05.png)

Voit tarkistaa tämän sanoman RSAT-työkalussa etsimällä kyseisen tallenteen antamalla sanoman tekstin Excelin parametritiedoston **Viestin tarkistus**-välilehdessä.

![Viestin tarkistus -välilehti](./media/use_rsa_tool_06.png)

Kun testitapaus on suoritettu, Excelin parametritiedostoa verrataan näytettävään sanomaan. Jos sanomat eivät vastaa toisiaan, testitapaus epäonnistuu.

> [!NOTE]
> Voit antaa Excelin parametritiedoston **Viestitarkistus**-välilehdessä useita sanomia. Sanomat voivat myös olla virhe- tai varoitussanomia ilmoitussanomien sijaan.

### <a name="validate-values-by-using-operators"></a>Arvojen tarkistaminen operaattorien avulla

RSAT-työkalun edellisissä versioissa arvot voitiin vahvistaa vain, jos tarkistusarvo ja odotettu arvo olivat samat. Uudella toiminnolla voi tarkistaa, että muuttuja ei ole yhtä suuri kuin tai on pienempi tai suurempi kuin määritetty arvo.

- Avaa tällä toiminnolla **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**-tiedosto RSAT-asennuskansiossa (esimerkiksi kansiossa **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ja muuta seuraavan elementin arvo **epätosi** arvoksi **tosi**.

    ```xml
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    Uusi **Operaattori**-kenttä tulee näkyviin Excelin parametritiedostossa.

    > [!NOTE]
    > Jos olet käyttänyt vanhaa RSAT-versiota, uudet Excelin parametritiedostot on luotava.

    ![Operaattorikenttä](./media/use_rsa_tool_07.png)

Seuraava esimerkki osoittaa, miten tällä toiminnolla tarkistetaan, onko varastosaldo suurempi kuin 0 (nolla).

1. Luo demotietojen **USMF**-yrityksessä tehtävätallenne, jossa on seuraavat vaiheet:

    1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
    2. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa **Nimiketunnus**-kenttää arvolla **1000**.
    3. Valitse **Käytettävissä oleva varasto**.
    4. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa **Toimipaikka**-kenttää arvolla **1**.
    5. Merkitse valittu rivi luettelossa.
    6. Tarkista, että **Yhteensä käytettävissä** -kentän arvo on **411,0000000000000000**.

2. Tallenna tehtävätallenne LCS:n BPM-kirjastoon ja synkronoi se Azure DevOpsiin.
3. Lisää testitapaus testisuunnitelmaan ja lataa testitapaus RSAT-työkaluun.
4. Avaa Excelin parametritiedosto. **Inventonhandimitem**-välilehdessä on **Tarkista InventOnhandItem** -osa, jossa on **Operaattori**-kenttä.

    ![Operaattorikenttä](./media/use_rsa_tool_08.png)

5. Jos haluat tarkistaa, että varastosaldo on aina yli 0, muuta **Arvo**-kentän arvo **411** arvoksi **0** ja **Operaattori**-kentän yhtä suuri kuin -merkki (**=**) suurempi kuin -merkiksi (**\>**).

    ![Arvo-ja Operaattori-kenttien muuttuneet arvot](./media/use_rsa_tool_09.png)

6. Tallenna ja sulje Excelin parametritiedosto.
7. Tallenna Excelin parametritiedostoon tehdyt muutokset Azure DevOpsiin valitsemalla **Lataa palvelimeen**.

Huomaa, että jos tietyn nimikkeen **Yhteensä käytettävissä** -kentän arvo varastossa on suurempi kuin 0 (nolla), testi hyväksytään todellisen varastosaldon arvosta riippumatta.

### <a name="generator-logs"></a>Generaattorin lokit

Tämä toiminto luo kansion, joka sisältää suoritettujen testitapausten lokit.

- Avaa tällä toiminnolla **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**-tiedosto RSAT-asennuskansiossa (esimerkiksi kansiossa **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ja muuta seuraavan elementin arvo **epätosi** arvoksi **tosi**.

    ```xml
    <add key="LogGeneration" value="false" />
    ```

Suoritettujen testitapausten lokitiedostot sijaitsevat kansiossa **C:\\Käyttäjät\\\<Käyttäjänimi\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.

![GeneratorLogs-kansio](./media/use_rsa_tool_10.png)

> [!NOTE]
> Jos testitapauksia oli luotu ennen .config-tiedoston arvon muuttamista, kyseisten testitapausten lokeja ei luoda, ennen kuin uudet testin suoritustiedostot luodaan.
> 
> ![Uusi-valikon Luo vain testin suoritustiedostot -komento](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a>Tilannevedos

Tämä toiminto ottaa näyttökuvat tehtävätallenteen aikana suoritetuista vaiheista.

- Avaa tällä toiminnolla **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**-tiedosto RSAT-asennuskansiossa (esimerkiksi kansiossa **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ja muuta seuraavan elementin arvo **epätosi** arvoksi **tosi**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

Jokaiselle suoritettavalle testitapaukselle luodaan erillinen kansio kohdassa **C:\\Käyttäjät\\\<Käyttäjänimi\>\\AppData\\Roaming\\regressionTool\\playback**.

![Testitapauksen tilannevedoskansio](./media/use_rsa_tool_12.png)

Kussakin näistä kansioista on tilannevedoksia testitapausten suorittamisen aikana suoritetuista vaiheista.

![Tilannevedostiedostot](./media/use_rsa_tool_13.png)

## <a name="assignment"></a>Määritys

### <a name="scenario"></a>Skenaario

1. Tuote suunnittelija luo uuden julkaistun tuotteen.
2. Tuotantopäällikkö käynnistää tuotantotilauksen, joka nostaa varastotason kahteen kappaleeseen.
3. Valmistus alkaa ja päättää tuotantotilauksen sekä varmistaa, että varastosaldo on kaksi kappaletta.
4. Myyntiryhmä vastaanottaa tilauksen, jossa on neljä kappaletta uutta tuotetta. Tämän vuoksi myyntiryhmä päivittää nettotarpeen dynaamisen suunnitelman kautta. Koska lisäkapasiteettia ei ole käytettävissä, tilausten oletuskäytännöksi on määritetty ostaminen valmistamisen sijaan. Tämän vuoksi luodaan suunnitellun ostotilauksen.
5. Ostaja lisää toimittajan, vahvistaa suunnitellun ostotilauksen ja vahvistaa lopuksi ostotilauksen.
6. Kun ostetut tavarat saapuvat myymälään, myymäläkäyttäjä hakee liittyvän ostotilauksen ja vastaanottaa tavarat. Koska tilaus on nyt valmis, tavarat voidaan kerätä ja pakata myyntitilauksen mukaisesti.
7. Talousosasta kirjaa osto- ja myyntilaskun.

Seuraavassa kuvassa on tämän skenaarion työnkulku.

![Demoskenaarion työnkulku](./media/use_rsa_tool_14.png)

Seuraavassa kuvassa on tämän skenaarion liiketoimintaprosessit RSAT-työkalussa.

![Demoskenaarion liiketoimintaprosessit](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a>Strategia – keskeinen opittava asia

### <a name="data"></a>Tiedot

- Varmista, että sinulla on tarvittavat tiedot (tuotanto-/ihannekonfiguraatiotietojen kopio ja siirretyt tiedot).
- Jos luot uusia tietoja tehtävän tallennustoiminnon kautta, luo sellaiset testinimet, jotka eivät ole ristiriidassa aiemmin luotujen nimien kanssa. (Käytä esimerkiksi etuliitettä, kuten **RSATxxx**).
- Suorita testit uudelleen muissa kuin tason 1 ympäristöissä käyttämällä Azuren ajankohtaan perustuvaa palautusta.
- Vaikka voit muodostaa ainutlaatuisia yhdistelmiä Excelin **SATUNNAINEN**- ja **NYT**-funktioita, sen työmäärä on huomattavan suuri. Esimerkki:

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a>Tehtävän tallennus

- Määritä skenaariot ennen tallentamisen aloittamista. Hyvin hallitussa projektissa on ennalta määritetyt testiskenaariot. Kun muodostat testitapausta, mieti, kuinka ennakoitavia kyseisten testiskenaarioiden tulos on.
- Jaa tallenteet, jos suorittajalla on eri rooli tai jos ennen seuraavaa vaihetta on odotettava tietty aika tai tiettyä ulkoista tapahtumaa.
- Vältä luettelossa olevien arvojen valitsemista. Käytä sen sijaan tekstimuotoja, kuten **FIFO**, **AudioRM** ja **SiteWH**. Jos valinta tehdään luettelossa, arvon sijainti luettelossa tallennetaan eikä itse arvoa. Jos kyseiseen luetteloon lisätään nimikkeitä, arvon sijainti voi muuttua. Tämän vuoksi tallenne käyttää eri parametria, mikä voi vaikuttaa skenaarion muihin osiin.
- Mieti tilannetta, jossa käyttäjiä on useita. Älä esimerkiksi oleta, että juuri luotu myyntitilaus valitaan aina automaattisesti. Etsi sen sijaan oikea tilaus aina suodattimella.
- Tallenna juuri luodun tuotteen nimi tehtävän tallennustoiminnon kopiointitoiminnolla, jolloin sitä voidaan käyttää ketjutetuissa testitapauksissa.
- Määritä tehtävän tallennustoiminnon tarkistustoiminnolla tarkistuspisteet tarkistamaan, että vaiheet on suoritettu oikein.

### <a name="rsat"></a>RSAT

- Jos suorittaa testin toisessa yrityksessä, voit vaihtaa yrityksen Excelin parametritiedoston **Yleiset**-välilehdessä. Varmista, että asetuksia ja tietoja voi käyttää juuri valitussa yrityksessä.
- Voit vaihtaa testikäyttäjän Excelin parametritiedoston **Yleiset**-välilehdessä. Määritä testitapauksen suorittavan käyttäjän sähköpostitunnus. Tällä tavoin testitapaus voidaan suorittaa turvallisesti käyttämällä määritetyn käyttäjän suojausoikeuksia.
- Jos haluat odottaa ennen testin aloittamista, voit määrittää tauon Excelin parametritiedoston **Yleiset**-välilehdessä. Tätä taukoa voidaan käyttää erätyössä (jos esimerkiksi työnkulku on suoritettava, ennen kuin seuraava vaihe voidaan suorittaa).

## <a name="advanced-scripting"></a>Edistyneet komentosarjat

### <a name="cli"></a>CLI

RSAT voidaan kutsua **Komentokehote**- tai **PowerShell**-ikkunasta.

> [!NOTE]
> Tarkista, että **TestRoot**-ympäristömuuttujan asetukseksi on määritetty RSAT-asennuspolku. (Avaa Microsoft Windowsissa **Ohjauspaneeli**, valitse sitten **Järjestelmä ja suojaus \> Järjestelmä \> Järjestelmän lisäasetukset** ja valitse lopuksi **Ympäristömuuttujat**.)

1. Avaa **Komentokehote**- tai **PowerShell**-ikkuna järjestelmänvalvojana.
2. Siirry RSAT-asennushakemistoon.

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. Luettele kaikki komennot.

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        ?
        about
        cls
        download
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a>? 
Näyttää kaikkien käytettävissä olevien komentojen ja niiden parametrien ohjeen.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="optional-parameters"></a>Valinnaiset parametrit

**``command``**


Jossa ``[command]`` on yksi alla määritetyistä komennoista.


#### <a name="about"></a>tietoja
Näyttää nykyisen version.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls
Tyhjentää näytön.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**


#### <a name="download"></a>lataa
Lataa määritetyn testitapauksen liitteet tulostushakemistoon. Voit käyttää ``list``-komentoa kaikkien käytettävissä olevien testitapausten hakemisessa. Käytä mitä tahansa ensimmäisen sarakkeen arvoa **test_case_id**-parametrina.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a>Pakolliset parametrit
**``test_case_id``** - edustaa testitapauksen tunnusta.  
**``output_dir``** - edustaa tulostushakemistoa. Hakemisto on määritettävä.

##### <a name="examples"></a>Esimerkkejä

``download 123 c:\temp\rsat``   
``download 765 c:\rsat\last``


#### <a name="edit"></a>muokkaa
Voit avata parametritiedoston Excel-ohjelmassa ja muokata sitä.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="required-parameters"></a>Pakolliset parametrit
**``excel_file``** - olemassa olevan Excel-tiedoston täydellinen polku on oltava.

##### <a name="examples"></a>Esimerkkejä
``edit c:\RSAT\TestCase_123_Base.xlsx``  
``edit e:\temp\TestCase_456_Base.xlsx``


#### <a name="generate"></a>luo
Luo testisuorituksen ja parametritiedostot määritetylle testitapaukselle tulostushakemistossa.
Voit käyttää ``list``-komentoa kaikkien käytettävissä olevien testitapausten hakemisessa. Käytä mitä tahansa ensimmäisen sarakkeen arvoa **test_case_id**-parametrina.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a>Pakolliset parametrit
**``test_case_id``** - edustaa testitapauksen tunnusta.  
**``output_dir``** - edustaa tulostushakemistoa. Hakemisto on määritettävä.

##### <a name="examples"></a>Esimerkkejä
``generate 123 c:\temp\rsat``  
``generate 765 c:\rsat\last``


#### <a name="generatederived"></a>generatederived
Luo uuden testitapauksen, joka johdetaan annetusta testitapauksesta. Voit käyttää ``list``-komentoa kaikkien käytettävissä olevien testitapausten hakemisessa. Käytä mitä tahansa ensimmäisen sarakkeen arvoa **test_case_id**-parametrina.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="required-parameters"></a>Pakolliset parametrit
**``parent_test_case_id``** - edustaa päätestitapauksen tunnusta.  
**``test_plan_id``** - edustaa testisuunnitelman tunnusta.  
**``test_suite_id``** - edustaa testiohjelmistopaketin tunnusta.

##### <a name="examples"></a>Esimerkkejä
``generatederived 123 8901 678``


#### <a name="generatetestonly"></a>generatetestonly
Luo vain testisuoritustiedoston määritetylle testitapaukselle tulostushakemistossa. Voit käyttää ``list``-komentoa kaikkien käytettävissä olevien testitapausten hakemisessa. Käytä mitä tahansa ensimmäisen sarakkeen arvoa **test_case_id**-parametrina.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a>Pakolliset parametrit
**``test_case_id``** - edustaa testitapauksen tunnusta.  
**``output_dir``** - edustaa tulostushakemistoa. Hakemisto on määritettävä.

##### <a name="examples"></a>Esimerkkejä
``generatetestonly 123 c:\temp\rsat``  
``generatetestonly 765 c:\rsat\last``


#### <a name="generatetestsuite"></a>generatetestsuite
Luo määritetyn ohjelmistopaketin kaikki testitapaukset tulostushakemistoon.
Voit käyttää ``listtestsuitenames``-komentoa kaikkien käytettävissä olevien testiohjelmistopakettien hakemisessa. Käytä mitä tahansa sarakkeen arvoa **test_suite_name**-parametrina.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="required-parameters"></a>Pakolliset parametrit
**``test_suite_name``** - edustaa testiohjelmistopaketin nimeä.  
**``output_dir``** - edustaa tulostushakemistoa. Hakemisto on määritettävä.

##### <a name="examples"></a>Esimerkkejä
``generatetestsuite Tests c:\temp\rsat``   
``generatetestsuite Purchase c:\rsat\last``


#### <a name="help"></a>ohje
Sama kuin [?](####?) komento


#### <a name="list"></a>luettelo
Luettelo kaikista käytettävissä olevista testitapauksista.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**


#### <a name="listtestplans"></a>listtestplans
Luettelo kaikista käytettävissä olevista testisuunnitelmista.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**


#### <a name="listtestsuite"></a>listtestsuite
Luettelo määritetyn testiohjelmistopaketin testitapauksista. Voit käyttää ``listtestsuitenames``-komentoa kaikkien käytettävissä olevien testiohjelmistopakettien hakemisessa. Käytä mitä tahansa ensimmäisen sarakkeen arvoa **suite_name**-parametrina.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="required-parameters"></a>Pakolliset parametrit
**``suite_name``** - halutun ohjelmistopaketin nimi.

##### <a name="examples"></a>Esimerkkejä
``listtestsuite "sample suite name"``  
``listtestsuite NameOfTheSuite``


#### <a name="listtestsuitenames"></a>listtestsuitenames
Luettelo kaikista käytettävissä olevista testiohjelmistopaketeista.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**


#### <a name="playback"></a>toisto
Toistaa testitapauksen Excel-tiedoston avulla.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="required-parameters"></a>Pakolliset parametrit
**``excel_file``** - Excel-tiedoston täydellinen polku. Tiedoston on oltava olemassa. 

##### <a name="examples"></a>Esimerkkejä
``
playback c:\RSAT\TestCaseParameters\sample1.xlsx
playback e:\temp\test.xlsx
``


#### <a name="playbackbyid"></a>playbackbyid
Toistaa useita testitapauksia kerralla.
Voit käyttää ``list``-komentoa kaikkien käytettävissä olevien testitapausten hakemisessa. Käytä mitä tahansa ensimmäisen sarakkeen arvoa **test_case_id**-parametrina.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="required-parameters"></a>Pakolliset parametrit
**``test_case_id1``** - olemassa olevan testitapauksen tunnus.  
**``test_case_id2``** - olemassa olevan testitapauksen tunnus.  
**``test_case_idN``** - olemassa olevan testitapauksen tunnus.  

##### <a name="examples"></a>Esimerkkejä
``playbackbyid 878``  
``playbackbyid 2345 667 135``


#### <a name="playbackmany"></a>playbackmany
Toistaa useita testitapauksia kerralla Excel-tiedostojen avulla.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="required-parameters"></a>Pakolliset parametrit
**``excel_file1``** - Excel-tiedoston täydellinen polku. Tiedoston on oltava olemassa.  
**``excel_file2``** - Excel-tiedoston täydellinen polku. Tiedoston on oltava olemassa.  
**``excel_fileN``** - Excel-tiedoston täydellinen polku. Tiedoston on oltava olemassa.  

##### <a name="examples"></a>Esimerkkejä
``playbackmany c:\RSAT\TestCaseParameters\param1.xlsx``  
``playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx``


#### <a name="playbacksuite"></a>playbacksuite
Toistaa kaikki testitapaukset määritetystä testiohjelmistopaketista. Voit käyttää ``listtestsuitenames``-komentoa kaikkien käytettävissä olevien testiohjelmistopakettien hakemisessa. Käytä mitä tahansa ensimmäisen sarakkeen arvoa **suite_name**-parametrina.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="required-parameters"></a>Pakolliset parametrit
**``suite_name``** - halutun ohjelmistopaketin nimi.

##### <a name="examples"></a>Esimerkkejä
``playbacksuite suiteName``  
``playbacksuite sample_suite``


#### <a name="quit"></a>lopeta
Sulkee sovelluksen.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**


#### <a name="upload"></a>lataa
Lataa kaikki määritettyyn testiohjelmistopakettiin tai määritettyihin testitapauksiin kuuluvat tiedostot.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="required-parameters"></a>Pakolliset parametrit
**``suite_name``** - kaikki tiettyyn testiohjelmistopakettiin kuuluvat tiedostot ladataan.
**``testcase_id``** - kaikki tiettyihin testitapauksiin kuuluvat tiedostot ladataan.

##### <a name="examples"></a>Esimerkkejä
``upload sample_suite``  
``upload 123``  
``upload 123 456``


#### <a name="uploadrecording"></a>uploadrecording
Lataa vain määritettyihin testitapauksiin kuuluvan tallennustiedoston.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="required-parameters"></a>Pakolliset parametrit
**``testcase_id``** - määritettyihin testitapauksiin kuuluva tallennustiedosto ladataan.

##### <a name="examples"></a>Esimerkkejä
``uploadrecording 123``  
``uploadrecording 123 456``


#### <a name="usage"></a>käyttö
Näyttää kaksi tapaa, joilla tätä sovellusta voi kutsua: toisessa käytetään oletusasetustiedostoa ja toinen määrittää asetustiedoston.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**


### <a name="windows-powershell-examples"></a>Windows PowerShell -esimerkkejä

#### <a name="run-a-test-case-in-a-loop"></a>Testitapauksen suorittaminen silmukkana

Sinulla on uuden asiakkaan luova testikomentosarja. Tämä testisarja voidaan suorittaa komentosarjojen avulla silmukkana muodostamalla seuraavat tiedot satunnaisesti ennen kunkin iteraation suorittamista:

- Asiakastunnus
- Asiakkaan nimi
- Asiakkaan osoitetiedot

Asiakastunnuksen muoto on seuraavanlainen: *ATCUS\<numero\>*, jossa \<numeron\> arvo on **000000001**–**999999999**.

Seuraavassa esimerkissä käytetään yhtä **aloitus**-parametria määrittämään ensimmäinen käytettävä numero. Is käyttää seuraavaa parametria **nr** määrittämään luotavien asiakkaiden määrän. Excelin parametritiedoston parametrit muutetaan kussakin iteraatiossa käyttämällä UpdateCustomer-funktiota. RSAT-komentorivi kutsutaan sitten RunTestCase-funktiolla.

Avaa integroitu Microsoft Windows PowerShell -komentosarjaympäristö (ISE) järjestelmänvalvojan tilassa ja liitä seuraava koodi **Untitled1.ps1**-nimiseen ikkunaan.

```powershell
param ( [int]$start = 1, [int]$nr = 1 )
function UpdateCustomer
{
    param ([string]$paramFilename, [string]$sheetName, [string]$CustId)
    $xl = New-Object -COM "Excel.Application"
    $xl.Visible = $false
    $wb = $xl.Workbooks.Open($paramFilename)
    $ws = $wb.Sheets.Item($sheetName)
    $ws.Cells.Item(3, 2).Value = "ATCUS" + $CustId
    $ws.Cells.Item(4, 2).Value = "Automated Test Customer " + $CustId
    $ws.Cells.Item(8, 2).Value = "Automated Test Street " + $CustId
    $wb.Save()
    $wb.Close()
    $xl.Quit()
    [System.Runtime.Interopservices.Marshal]::ReleaseComObject($xl)
}
function RunTestCase
{
    param ( [string]$filename )
    $cmd = "cd c:\Program Files (x86)\Regression Suite Automation Tool\ &&  "
    $cmd = $cmd + "Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playback "
    $cmd = $cmd + $filename
    cmd /c $cmd
}
$excelFilename = "full path to excel file parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a>Microsoft Dynamics 365:n tiedoista riippuvaisen komentosarjan suorittaminen

Seuraavassa esimerkissä ostotilauksen tila etsitään Open Data Protocol (OData) -kutsun avulla. Jos tila ei ole **invoiced**, voit esimerkiksi kutsua laskun kirjaavan RSAT-testitapauksen.

```xpp
function Odata_Get
{
    Param ( [string] $environment, [string] $cmd )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    $tenant = "your tenant"
    $creds = @{
        grant_type = "client_credentials"
        client_id = "your client application Id"
        client_secret = "your client secret"
        resource = $environment
    }
    $headers = $null
    $bearer = Invoke-RestMethod https://login.microsoftonline.com/$tenant/oauth2/token -Method Post -Body $creds -Headers $headers;
    $headers = @{
        Authorization = "Bearer " + $bearer.access_token
    }
    $Odata_cmd = $environment + '/data/' + $cmd
    return (Invoke-RestMethod -Uri $Odata_cmd -Method Get -Headers $headers -ContentType application/json )
}
function PurchaseOrderStatus
{
    Param ( [string] $environment, [string] $purchaseOrderNumber )
    $cmd = 'PurchaseOrderHeaders?$filter=PurchaseOrderNumber eq '
    $cmd = $cmd + "'" + $purchaseOrderNumber + "'"
    $response = Odata_Get -environment $environment -cmd $cmd
    return $response.value.PurchaseOrderStatus
}
$environment = "https://your environment"
$orderStatus = PurchaseOrderStatus -environment $environment -purchaseOrderNumber '000003'
if ($orderStatus -eq $null) {   write-host 'doesn''t exist'}
elseif ($orderStatus -ne 'invoiced') { RunTestCase "PostInvoice" }
```
