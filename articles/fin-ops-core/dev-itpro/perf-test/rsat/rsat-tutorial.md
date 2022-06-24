---
title: Regression Suite Automation Tool -opetusohjelma
description: Tässä artikkelissa käsitellään Regression Suite Automation Tool (RSAT) -työkalun käyttämistä. Siinä käsitellään erilaisia toimintoja ja annetaan esimerkkejä edistyneestä komentosarjojen käytöstä.
author: FrankDahl
ms.date: 09/23/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 04c7d7081ece4e077881092534ed061fe2d0e999
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854596"
---
# <a name="regression-suite-automation-tool-tutorial"></a>Regression Suite Automation Tool -opas

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> Lataa ja tallenna tämä ohje selaimen työkaluilla PDF-tiedostona.

Tässä oppaassa käsitellään yksityiskohtaisesti Regression Suite Automation Tool (RSAT) -työkalun lisätoimintoja. Se sisältää myös demon määrityksen ja siinä käsitellään strategiaa ja keskeisiä opittavia asioita.

## <a name="notable-features-of-rsat-and-task-recorder"></a>RSAT:in ja tehtävien tallennustoiminnon merkittävimmät ominaisuudet

### <a name="validate-a-field-value"></a>Kentän arvon tarkistaminen

RSAT-toiminnon avulla voit sisällyttää odotettuihin arvoihin oikeellisuustarkistusvaiheet. Lisätietoja tästä ominaisuudesta on artikkelissa [Tarkista odotetut arvot](rsat-validate-expected.md).

Seuraava esimerkki osoittaa, miten tällä toiminnolla tarkistetaan, onko käytettävissä oleva varastosaldo suurempi kuin 0 (nolla).

1. Luo demotietojen **USMF**-yrityksessä tehtävätallenne, jossa on seuraavat vaiheet:

    1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
    2. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa **Nimiketunnus**-kenttää arvolla **1000**.
    3. Valitse **Käytettävissä oleva varasto**.
    4. Käytä pikasuodatinta tietueiden etsimiseen. Voit esimerkiksi suodattaa **Toimipaikka**-kenttää arvolla **1**.
    5. Merkitse valittu rivi luettelossa.
    6. Tarkista, että **Yhteensä käytettävissä** -kentän arvo on **411,0000000000000000**.

2. Tallenna tehtävätallenne **kehittäjän tallenteena** ja liitä se testitapaukseen Azure DevOpsissa.
3. Lisää testitapaus testisuunnitelmaan ja lataa testitapaus RSAT-työkaluun.
4. Avaa Excel-parametritiedosto ja siirry **TestCaseSteps**-välilehteen.
5. Jos haluat tarkistaa, että käytettävissä oleva varasto on aina yli **0**, muuta **Yhteensä käytettävissä olevan tarkistaminen** -vaiheessa tämä arvo arvosta **411** arvoksi **0**. Muuta **Operaattori**-kentän arvo, yhtäsuuruusmerkki (**=**), suurempi kuin -merkiksi (**\>**).
6. Tallenna ja sulje Excelin parametritiedosto.
7. Tallenna Excelin parametritiedostoon tehdyt muutokset Azure DevOpsiin valitsemalla **Lataa palvelimeen**.

Huomaa, että jos tietyn nimikkeen **Yhteensä käytettävissä** -kentän arvo varastossa on suurempi kuin 0 (nolla), testi hyväksytään todellisen käytettävissä olevan varastosaldon arvosta riippumatta.

### <a name="saved-variables-and-chaining-of-test-cases"></a>Testitapausten tallennetut muuttujat ja ketjutus

Yksi RSAT-työkalun keskeisistä ominaisuuksista on testitapausten ketjuttaminen, eli ominaisuus, jolla testi voi siirtää muuttujat toisiin testeihin. Lisätietoja on artikkelissa [Kopioi muuttujat ketjutestitapauksiin](rsat-chain-test-cases.md).

### <a name="derived-test-case"></a>Johdettu testitapaus

RSAT-toiminnon avulla voit käyttää samaa tehtävätallennetta useissa testitapauksissa, jolloin tehtävä voidaan suorittaa eri tietokonfiguraatioiden avulla. Lisätietoja on artikkelissa [Johdetut testitapaukset](rsat-derived-test-cases.md).

### <a name="validate-notifications-and-messages"></a>Ilmoitusten ja sanomien vahvistaminen

Tällä toiminnolla tarkistetaan, tapahtuiko toiminto. Kun esimerkiksi tuotantotilaus luodaan, arvioidaan ja aloitetaan, sovellus ilmoittaa Tuotanto - käynnistys -sanomalla, että tuotantotilaus on aloitettu.

![Tuotanto - käynnistys -ilmoitus.](./media/use_rsa_tool_05.png)

Voit tarkistaa tämän sanoman RSAT-työkalussa etsimällä kyseisen tallenteen antamalla sanoman tekstin Excelin parametritiedoston **Viestin tarkistus**-välilehdessä.

![Viestin tarkistus -välilehti.](./media/use_rsa_tool_06.png)

Kun testitapaus on suoritettu, Excelin parametritiedostoa verrataan näytettävään sanomaan. Jos sanomat eivät vastaa toisiaan, testitapaus epäonnistuu.

> [!NOTE]
> Voit antaa Excelin parametritiedoston **Viestitarkistus**-välilehdessä useita sanomia. Sanomat voivat myös olla virhe- tai varoitussanomia ilmoitussanomien sijaan.

### <a name="snapshot"></a>Tilannevedos

Tämä toiminto ottaa näyttökuvat tehtävätallenteen aikana suoritetuista vaiheista. Se on hyödyllinen tarkistus- tai virheenkorjaustarkoituksiin.

- Tätä ominaisuutta voi käyttää, kun RSAT on käytössä käyttöliittymässä, avaamalla **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config**-tiedosto RSAT-asennuskansiossa (esimerkiksi kansiossa **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ja muuttamalla seuraavan elementin arvo **epätosi** arvoksi **tosi**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

- Tätä ominaisuutta voi käyttää, kun RSAT on komentorivikäyttöliittymän käytössä (esimerkiksi Azure DevOps) käyttää sitä, avaamalla **Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe.config**-tiedosto RSAT-asennuskansiossa (esimerkiksi kansiossa **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ja muuttamalla seuraavan elementin arvo **epätosi** arvoksi **tosi**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

Kun testitapaukset suoritetaan, RSAT luo tilannevedoksia (näköistiedostoja) vaiheista ja tallentaa työskentelyhakemistossa olevien testitapausten toistokansioon. Toistokansioon luodaan erillinen **StepSnapshots**-alikansio. Tämä kansio sisältää suoritettavien testitapausten tilannevedokset.

## <a name="assignment"></a>Liitos

### <a name="scenario"></a>Skenaario

1. Tuote suunnittelija luo uuden julkaistun tuotteen.
2. Tuotantopäällikkö käynnistää tuotantotilauksen, joka nostaa varastotason kahteen kappaleeseen.
3. Valmistus alkaa ja päättää tuotantotilauksen sekä varmistaa, että käytettävissä oleva varastosaldo on kaksi kappaletta.
4. Myyntiryhmä vastaanottaa tilauksen, jossa on neljä kappaletta uutta tuotetta. Tämän vuoksi myyntiryhmä päivittää nettotarpeen dynaamisen suunnitelman kautta. Koska lisäkapasiteettia ei ole käytettävissä, tilausten oletuskäytännöksi on määritetty ostaminen valmistamisen sijaan. Tämän vuoksi luodaan suunnitellun ostotilauksen.
5. Ostaja lisää toimittajan, vahvistaa suunnitellun ostotilauksen ja vahvistaa lopuksi ostotilauksen.
6. Kun ostetut tavarat saapuvat myymälään, myymäläkäyttäjä hakee liittyvän ostotilauksen ja vastaanottaa tavarat. Koska tilaus on nyt valmis, tavarat voidaan kerätä ja pakata myyntitilauksen mukaisesti.
7. Talousosasta kirjaa osto- ja myyntilaskun.

Seuraavassa kuvassa on tämän skenaarion työnkulku.

![Demoskenaarion työnkulku.](./media/use_rsa_tool_14.png)

Seuraavassa kuvassa näkyy tämän skenaarion liiketoimintaprosessien hierarkia LCS-liiketoimintaprosessin mallintajassa.

![Demoskenaarion liiketoimintaprosessit.](./media/use_rsa_tool_15.png)

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
        downloadsuite
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitebyid
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        playbacksuitebyid
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a>?

Luettelee kaikki komennot tai näyttää tietyn komennon ohjeen sekä käytettävissä olevat parametrit.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a>?: Valinnaiset parametrit

`command`: Missä ``[command]`` on jokin edeltävän luettelon komennoista.

#### <a name="about"></a>tietoja

Näyttää asennetun RSAT-version.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls

Tyhjentää näytön.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a>lataa

Lataa liitteet (tallennus-, suoritus- ja parametritiedostot) määritetylle testitapaukselle Azure DevOpsista tuloshakemistoon. Voit käyttää ``list``-komentoa kaikkien käytettävissä olevien testitapausten kehotteeseen ja käyttää mitä tahansa ensimmäisen sarakkeen arvoa **test_case_id**-parametrina.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="download-optional-switches"></a>lataa: valinnaiset valitsimet

+ `/retry[=seconds]`: Jos tämä valitsin on määritetty ja muut RSAT-instanssit estävät palvelupyyntötestin, latausprosessi odottaa määritettyä sekuntien määrää ja yrittää vielä kerran. Oletusarvo valitsimelle \[sekuntia\] on 120 sekuntia. Jos tätä kytkentää ei ole, prosessi peruutetaan heti, jos testitapaukset on estetty.

##### <a name="download-required-parameters"></a>lataaminen: pakolliset parametrit

+ `test_case_id`: ilmaisee testitapauksen tunnuksen.

##### <a name="download-optional-parameters"></a>lataa: valinnaiset parametrit

+ `output_dir`: Ilmaisee tulostustyöhakemiston. Hakemisto on määritettävä. Jos parametria ei ole määritetty, käytetään asetusten työhakemistoa.

##### <a name="download-examples"></a>lataa: esimerkit

`download 123 c:\temp\rsat`

`download /retry=240 765`

#### <a name="downloadsuite"></a>downloadsuite

Lataa liitteet (tallennus-, suoritus- ja parametritiedostot) kaikille määritetyn testipaketin testitapauksille Azure DevOpsista tuloshakemistoon. Voit käyttää ``listtestsuitenames``-komentoa kaikkien käytettävissä olevien testipakettien kehotteeseen ja käyttää mitä tahansa ensimmäisen sarakkeen arvoa **test_suite_name**-parametrina.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``downloadsuite``**``[/retry[=<seconds>]] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="downloadsuite-optional-switches"></a>downloadsuite: valinnaiset valitsimet

+ `/retry[=seconds]`: Jos tämä valitsin on määritetty ja muut RSAT-instanssit estävät palvelupyyntötestin, latausprosessi odottaa määritettyä sekuntien määrää ja yrittää vielä kerran. Oletusarvo valitsimelle \[sekuntia\] on 120 sekuntia. Jos tätä kytkentää ei ole, prosessi peruutetaan heti, jos testitapaukset on estetty.
+ `/byid`: Tämä kytkentä ilmaisee, että haluamasi testisarja tunnistetaan testin nimen asemesta sen Azure DevOps-tunnuksella.

##### <a name="downloadsuite-required-parameters"></a>downloadsuite: pakolliset parametrit

+ `test_suite_name`: ilmaisee testiohjelmistopaketin nimen. Tämä parametri on pakollinen, jos /byid switch -arvoa **ei ole** määritetty. Tämä nimi on Azure DevOps-testipaketin nimi.
+ `test_suite_id`: ilmaisee testiohjelmistopaketin tunnusta. Tämä parametri on pakollinen, jos /byid switch -arvo **on** määritetty. Tämä tunnus on testipakettien Azure DevOps -tunnus.

##### <a name="downloadsuite-optional-parameters"></a>downloadsuite: valinnaiset parametrit

+ `output_dir`: Ilmaisee tulostustyöhakemiston. Hakemisto on määritettävä. Jos parametria ei ole määritetty, käytetään asetusten työhakemistoa.

##### <a name="downloadsuite-examples"></a>downloadsuite: esimerkit

`downloadsuite NameOfTheSuite c:\temp\rsat`

`downloadsuite /byid 123 c:\temp\rsat`

`downloadsuite /retry=240 /byid 765`

`downloadsuite /retry=240 /byid 765 c:\temp\rsat`

#### <a name="edit"></a>muokkaa

Voit avata parametritiedoston Excel-ohjelmassa ja muokata sitä.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a>muokkaa: pakolliset parametrit

+ `excel_file`: on sisällettävä täydellinen polku aiemmin luotuun Excel-tiedostoon.

##### <a name="edit-examples"></a>muokkaa: esimerkit

`edit c:\RSAT\123\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a>luo

Luo testisuorituksen ja parametritiedostot määritetylle testitapaukselle tulostushakemistossa. Voit käyttää ``list``-komentoa kaikkien käytettävissä olevien testitapausten hakemisessa. Käytä mitä tahansa ensimmäisen sarakkeen arvoa **test_case_id**-parametrina.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] [test_case_id] [output_dir]``

##### <a name="generate-optional-switches"></a>muodosta: valinnaiset valitsimet

+ `/retry[=seconds]`: Jos tämä valitsin on määritetty ja muut RSAT-instanssit estävät palvelupyyntötestin, muodostusprosessi odottaa määritettyä sekuntien määrää ja yrittää vielä kerran. Oletusarvo valitsimelle \[sekuntia\] on 120 sekuntia. Jos tätä kytkentää ei ole, prosessi peruutetaan heti, jos testitapaukset on estetty.
+ `/dllonly`: Luo vain testin suoritustiedostot. Älä luo uudelleen Excel-parametritiedostoa.
+ `/keepcustomexcel`: Päivitä aiemmin luotu parametritiedosto. Luo myös suoritustiedostot uudelleen.

##### <a name="generate-required-parameters"></a>luo: pakolliset parametrit

+ `test_case_id`: ilmaisee testitapauksen tunnuksen.

##### <a name="generate-optional-parameters"></a>luo: valinnaiset parametrit

+ `output_dir`: Ilmaisee tulostustyöhakemiston. Hakemisto on määritettävä. Jos parametria ei ole määritetty, käytetään asetusten työhakemistoa.

##### <a name="generate-examples"></a>luo: esimerkit

`generate 123 c:\temp\rsat`

`generate /retry=240 765 c:\rsat\last`

`generate /retry=240 /dllonly 765`

`generate /retry=240 /keepcustomexcel 765`

#### <a name="generatederived"></a>generatederived

Luo uuden johdetun testitapauksen (alitestitapauksen) toimitetusta testitapauksesta. Uusi testitapaus lisätään myös määritettyyn testisarjaan. Voit käyttää ``list``-komentoa kaikkien käytettävissä olevien testitapausten kehotteeseen ja käyttää mitä tahansa ensimmäisen sarakkeen arvoa **test_case_id**-parametrina.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[/retry[=<seconds>]] [parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-optional-switches"></a>generatederived: valinnaiset valitsimet

+ `/retry[=seconds]`: Jos tämä valitsin on määritetty ja muut RSAT-instanssit estävät palvelupyyntötestin, muodostusprosessi odottaa määritettyä sekuntien määrää ja yrittää vielä kerran. Oletusarvo valitsimelle \[sekuntia\] on 120 sekuntia. Jos tätä kytkentää ei ole, prosessi peruutetaan heti, jos testitapaukset on estetty.

##### <a name="generatederived-required-parameters"></a>generatederived: pakolliset parametrit

+ `parent_test_case_id`: ilmaisee päätestitapauksen tunnuksen.
+ `test_plan_id`: ilmaisee testisuunnitelman tunnuksen.
+ `test_suite_id`: ilmaisee testiohjelmistopaketin tunnusta.

##### <a name="generatederived-examples"></a>generatederived: esimerkit

`generatederived 123 8901 678`

`generatederived /retry 123 8901 678`

#### <a name="generatetestonly"></a>generatetestonly

Luo vain testisuoritustiedostot määritetylle testitapaukselle. Se ei luo Excel-parametritiedostoa. Tiedostot luodaan määritettyyn tulostehakemistoon. Voit käyttää ``list``-komentoa kaikkien käytettävissä olevien testitapausten kehotteeseen ja käyttää mitä tahansa ensimmäisen sarakkeen arvoa **test_case_id**-parametrina.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="generatetestonly-optional-switches"></a>generatetestonly: valinnaiset valitsimet

+ `/retry[=seconds]`: Jos tämä valitsin on määritetty ja muut RSAT-instanssit estävät palvelupyyntötestin, muodostusprosessi odottaa määritettyä sekuntien määrää ja yrittää vielä kerran. Oletusarvo valitsimelle \[sekuntia\] on 120 sekuntia. Jos tätä kytkentää ei ole, prosessi peruutetaan heti, jos testitapaukset on estetty.

##### <a name="generatetestonly-required-parameters"></a>generatetestonly: pakolliset parametrit

+ `test_case_id`: ilmaisee testitapauksen tunnuksen.

##### <a name="generatetestonly-optional-parameters"></a>generatetestonly: valinnaiset parametrit

+ `output_dir`: Ilmaisee tulostustyöhakemiston. Hakemisto on määritettävä. Jos parametria ei ole määritetty, käytetään asetusten työhakemistoa.

##### <a name="generatetestonly-examples"></a>generatetestonly: esimerkit

`generatetestonly 123 c:\temp\rsat`

`generatetestonly /retry=240 765`

#### <a name="generatetestsuite"></a>generatetestsuite

Luo testiautomaatiotiedostoja kaikille määritetyn testipaketin testitapauksille. Voit käyttää ``listtestsuitenames``-komentoa kaikkien käytettävissä olevien testipakettien kehotteeseen ja käyttää mitä tahansa ensimmäisen sarakkeen arvoa **test_suite_name**-parametrina.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="generatetestsuite-optional-switches"></a>generatetestsuite: valinnaiset valitsimet

+ `/retry[=seconds]`: Jos tämä valitsin on määritetty ja muut RSAT-instanssit estävät palvelupyyntötestin, muodostusprosessi odottaa määritettyä sekuntien määrää ja yrittää vielä kerran. Oletusarvo valitsimelle \[sekuntia\] on 120 sekuntia. Jos tätä kytkentää ei ole, prosessi peruutetaan heti, jos testitapaukset on estetty.
+ `/dllonly`: Luo vain testin suoritustiedostot. Älä luo uudelleen Excel-parametritiedostoa.
+ `/keepcustomexcel`: Päivitä aiemmin luotu parametritiedosto. Luo myös suoritustiedostot uudelleen.
+ `/byid`: Tämä kytkentä ilmaisee, että haluamasi testisarja tunnistetaan testin nimen asemesta sen Azure DevOps-tunnuksella.

##### <a name="generatetestsuite-required-parameters"></a>generatetestsuite: pakolliset parametrit

+ `test_suite_name`: ilmaisee testiohjelmistopaketin nimen. Tämä parametri on pakollinen, jos /byid switch -arvoa **ei ole** määritetty. Tämä nimi on Azure DevOps-testipaketin nimi.
+ `test_suite_id`: ilmaisee testiohjelmistopaketin tunnusta. Tämä parametri on pakollinen, jos /byid switch -arvo **on** määritetty. Tämä tunnus on testipakettien Azure DevOps -tunnus.

##### <a name="generatetestsuite-optional-parameters"></a>generatetestsuite: valinnaiset parametrit

+ `output_dir`: Ilmaisee tulostustyöhakemiston. Hakemisto on määritettävä. Jos parametria ei ole määritetty, käytetään asetusten työhakemistoa.

##### <a name="generatetestsuite-examples"></a>generatetestsuite: esimerkit

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite /retry Purchase c:\rsat\last`

`generatetestsuite /dllonly /byid 121`

`generatetestsuite /keepcustomexcel /byid 121`

#### <a name="help"></a>ohje

Sama kuin [?](#section) -komento.

#### <a name="list"></a>luettelo

Luettelee kaikki nykyisen testisuunnitelman käytettävissä olevat testitapaukset.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a>listtestplans

Luettelo kaikista käytettävissä olevista testisuunnitelmista.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a>listtestsuite

Luettelo määritetyn testiohjelmistopaketin testitapauksista. Voit käyttää ``listtestsuitenames``-komentoa kaikkien käytettävissä olevien testipakettien kehotteeseen ja käyttää mitä tahansa ensimmäisen sarakkeen arvoa luettelosta **tsuite_name**-parametrina.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[test_suite_name]``

##### <a name="listtestsuite-required-parameters"></a>listtestsuite: pakolliset parametrit

+ `test_suite_name`: Toivotun ohjelmistopaketin nimi.

##### <a name="listtestsuite-examples"></a>listtestsuite: esimerkit

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitebyid"></a>listtestsuitebyid

Luettelo määritetyn testiohjelmistopaketin testitapauksista.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitebyid``**``[test_suite_id]``

##### <a name="listtestsuitebyid-required-parameters"></a>listtestsuitebyid: pakolliset parametrit

+ `test_suite_id`: Toivotun ohjelmistopaketin tunnus.

##### <a name="listtestsuitebyid-examples"></a>listtestsuitebyid: esimerkit

`listtestsuitebyid 12345`

#### <a name="listtestsuitenames"></a>listtestsuitenames

Luettelee kaikki nykyisen testisuunnitelman käytettävissä olevat testipaketit.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a>toisto

Toistaa testitapauksen, joka liittyy määritettyyn Excel-parametritiedostoon. Tämä komento käyttää aiemmin luotuja paikallisia automaatiotiedostoja eikä lataa tiedostoja Azure DevOpsista. Tätä komentoa ei tueta POS:n kaupallisissa testitapauksissa.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file]``

##### <a name="playback-optional-switches"></a>playback: valinnaiset valitsimet

+ `/retry[=seconds]`: Jos tämä valitsin on määritetty ja muut RSAT-instanssit estävät palvelupyyntötestin, toistoprosessi odottaa määritettyä sekuntien määrää ja yrittää vielä kerran. Oletusarvo valitsimelle \[sekuntia\] on 120 sekuntia. Jos tätä kytkentää ei ole, prosessi peruutetaan heti, jos testitapaukset on estetty.
+ `/comments[="comment"]`: Anna mukautettu tietomerkkijono, joka sisällytetään Azure DevOps -testipakettisuoritusten yhteenveto- ja testitulossivujen **Huomautukset**-kenttään.

##### <a name="playback-required-parameters"></a>toisto: pakolliset parametrit

+ `excel_parameter_file`: Excel-parametritiedoston koko polku. Tiedoston on oltava olemassa.

##### <a name="playback-examples"></a>toisto: esimerkit

`playback c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playback /retry e:\temp\test.xlsx`

`playback /retry=300 e:\temp\test.xlsx`

`playback /comments="Payroll solution 10.0.0" e:\temp\test.xlsx`

#### <a name="playbackbyid"></a>playbackbyid

Toistaa useita testitapauksia samaan aikaan. Testitapaukset tunnistetaan niiden tunnuksen mukaan. Tämä komento lataa tiedostot Azure DevOpsista. Voit käyttää ``list``-komentoa kaikkien käytettävissä olevien testitapausten kehotteeseen ja käyttää mitä tahansa ensimmäisen sarakkeen arvoja **test_case_id**-parametrina.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[/retry[=<seconds>]] [/comments[="comment"]] [test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-optional-switches"></a>playbackbyid: valinnaiset valitsimet

+ `/retry[=seconds]`: Jos tämä valitsin on määritetty ja muut RSAT-instanssit estävät palvelupyyntötestin, toistoprosessi odottaa määritettyä sekuntien määrää ja yrittää vielä kerran. Oletusarvo valitsimelle \[sekuntia\] on 120 sekuntia. Jos tätä kytkentää ei ole, prosessi peruutetaan heti, jos testitapaukset on estetty.
+ `/comments[="comment"]`: Anna mukautettu tietomerkkijono, joka sisällytetään Azure DevOps -testipakettisuoritusten yhteenveto- ja testitulossivujen **Huomautukset**-kenttään.

##### <a name="playbackbyid-required-parameters"></a>playbackbyid: pakolliset parametrit

+ `test_case_id1`: Aiemmin luodun testitapauksen tunnus.
+ `test_case_id2`: Aiemmin luodun testitapauksen tunnus.
+ `test_case_idN`: Aiemmin luodun testitapauksen tunnus.

##### <a name="playbackbyid-examples"></a>playbackbyid: esimerkit

`playbackbyid 878`

`playbackbyid 2345 667 135`

`playbackbyid /comments="Payroll solution 10.0.0" 2345 667 135`

`playbackbyid /retry /comments="Payroll solution 10.0.0" 2345 667 135`

#### <a name="playbackmany"></a>playbackmany

Toistaa monia testitapauksia samaan aikaan. Testitapaukset yksilöidään Excel-parametritiedostojen avulla. Tämä komento käyttää aiemmin luotuja paikallisia automaatiotiedostoja eikä lataa tiedostoja Azure DevOpsista.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file1] [excel_parameter_file2] ... [excel_parameter_fileN]``

##### <a name="playbackmany-optional-switches"></a>playbackmany: valinnaiset valitsimet

+ `/retry[=seconds]`: Jos tämä valitsin on määritetty ja muut RSAT-instanssit estävät palvelupyyntötestin, toistoprosessi odottaa määritettyä sekuntien määrää ja yrittää vielä kerran. Oletusarvo valitsimelle \[sekuntia\] on 120 sekuntia. Jos tätä kytkentää ei ole, prosessi peruutetaan heti, jos testitapaukset on estetty.
+ `/comments[="comment"]`: Anna mukautettu tietomerkkijono, joka sisällytetään Azure DevOps -testipakettisuoritusten yhteenveto- ja testitulossivujen **Huomautukset**-kenttään.

##### <a name="playbackmany-required-parameters"></a>playbackmany: pakolliset parametrit

+ `excel_parameter_file1`: Excel-parametritiedoston koko polku. Tiedoston on oltava olemassa.
+ `excel_parameter_file2`: Excel-parametritiedoston koko polku. Tiedoston on oltava olemassa.
+ `excel_parameter_fileN`: Excel-parametritiedoston koko polku. Tiedoston on oltava olemassa.

##### <a name="playbackmany-examples"></a>playbackmany: esimerkit

`playbackmany c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playbackmany e:\temp\test.xlsx f:\RSAT\sample1.xlsx c:\RSAT\sample2.xlsx`

`playbackmany /retry=180 /comments="Payroll solution 10.0.0" e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a>playbacksuite

Toistaa kaikki testitapaukset yhdestä tai useammasta määritetystä testiohjelmistopaketista. Jos /local-valitsin on määritetty, paikallisia liitteitä käytetään toistoissa. Muussa tapauksessa liitteet ladataan Azure DevOpsista. Voit käyttää ``listtestsuitenames``-komentoa kaikkien käytettävissä olevien testipakettien kehotteeseen ja käyttää mitä tahansa ensimmäisen sarakkeen arvoa **tsuite_name**-parametrina.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] ([test_suite_name1] .. [test_suite_nameN] | [/byid] [test_suite_id1] .. [test_suite_idN])``

##### <a name="playbacksuite-optional-switches"></a>playbacksuite: valinnaiset valitsimet

+ `/updatedriver`: Jos tämä valitsin on määritetty, www-selaimen webtyökalu päivitetään tarvittaessa ennen www-selaimen suorittamista.
+ `/local`: Tämä kytkin osoittaa, että paikallisia liitteitä tulee käyttää toistoon sen sijaan, että tiedostot ladataan Azure DevOpsista.
+ `/retry[=seconds]`: Jos tämä valitsin on määritetty ja muut RSAT-instanssit estävät palvelupyyntötestin, toistoprosessi odottaa määritettyä sekuntien määrää ja yrittää vielä kerran. Oletusarvo valitsimelle \[sekuntia\] on 120 sekuntia. Jos tätä kytkentää ei ole, prosessi peruutetaan heti, jos testitapaukset on estetty.
+ `/comments[="comment"]`: Anna mukautettu tietomerkkijono, joka sisällytetään Azure DevOps -testipakettisuoritusten yhteenveto- ja testitulossivujen **Huomautukset**-kenttään.
+ `/byid`: Tämä kytkentä ilmaisee, että haluamasi testisarja tunnistetaan testin nimen asemesta sen Azure DevOps-tunnuksella.

##### <a name="playbacksuite-required-parameters"></a>playbacksuite: pakolliset parametrit

+ `test_suite_name1`: ilmaisee testiohjelmistopaketin nimen. Tämä parametri on pakollinen, jos /byid switch -arvoa **ei ole** määritetty. Tämä nimi on Azure DevOps-testipaketin nimi.
+ `test_suite_nameN`: ilmaisee testiohjelmistopaketin nimen. Tämä parametri on pakollinen, jos /byid switch -arvoa **ei ole** määritetty. Tämä nimi on Azure DevOps-testipaketin nimi.
+ `test_suite_id1`: ilmaisee testiohjelmistopaketin tunnusta. Tämä parametri on pakollinen, jos /byid switch -arvo **on** määritetty. Tämä tunnus on testipakettien Azure DevOps -tunnus.
+ `test_suite_idN`: ilmaisee testiohjelmistopaketin tunnusta. Tämä parametri on pakollinen, jos /byid switch -arvo **on** määritetty. Tämä tunnus on testipakettien Azure DevOps -tunnus.

##### <a name="playbacksuite-examples"></a>playbacksuite: esimerkit

`playbacksuite suiteName`

`playbacksuite suiteName suiteNameToo`

`playbacksuite /updatedriver /local /retry=180 /byid 151 156`

`playbacksuite /updatedriver /local /comments="Payroll solution 10.0.0" /byid 150`

#### <a name="playbacksuitebyid"></a>playbacksuitebyid

Suorittaa kaikki testitapaukset määritetyssä Azure DevOps -testiohjelmistopaketissa.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuitebyid``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] [test_suite_id]``

##### <a name="playbacksuitebyid-optional-switches"></a>playbacksuitebyid: valinnaiset valitsimet

+ `/retry[=seconds]`: Jos tämä valitsin on määritetty ja muut RSAT-instanssit estävät palvelupyyntötestin, toistoprosessi odottaa määritettyä sekuntien määrää ja yrittää vielä kerran. Oletusarvo valitsimelle \[sekuntia\] on 120 sekuntia. Jos tätä kytkentää ei ole, prosessi peruutetaan heti, jos testitapaukset on estetty.
+ `/comments[="comment"]`: Anna mukautettu tietomerkkijono, joka sisällytetään Azure DevOps -testipakettisuoritusten yhteenveto- ja testitulossivujen **Huomautukset**-kenttään.
+ `/byid`: Tämä kytkentä ilmaisee, että haluamasi testisarja tunnistetaan testin nimen asemesta sen Azure DevOps-tunnuksella.

##### <a name="playbacksuitebyid-required-parameters"></a>playbacksuitebyid: pakolliset parametrit

+ `test_suite_id`: Edustaa testipakettien tunnusta, joka on olemassa Azure DevOpsissa.

##### <a name="playbacksuitebyid-examples"></a>playbacksuitebyid: esimerkit

`playbacksuitebyid 2900`

`playbacksuitebyid /retry 2099`

`playbacksuitebyid /retry=200 2099`

`playbacksuitebyid /retry=200 /comments="some comment" 2099`

#### <a name="quit"></a>lopeta

Sulkee sovelluksen. Tästä komennosta on hyötyä vain silloin, kun sovellukset ovat käynnissä vuorovaikutteisessa tilassa.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

##### <a name="quit-examples"></a>quit: esimerkit

`quit`

#### <a name="upload"></a>lataa

Lataa palvelimeen liitetiedostot (tallennus-, suoritus- ja parametritiedostot), jotka kuuluvat määritettyyn testipaketteihin tai testitapauksiin Azure DevOpsiin.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``([test_suite_name] | [test_case_id1] .. [test_case_idN])``

##### <a name="upload-required-parameters"></a>upload: pakolliset parametrit

+ `test_suite_name`: Kaikki tiettyyn testiohjelmistopakettiin kuuluvat tiedostot ladataan.
+ `test_case_id1`: Edustaa ensimmäistä latausta varten ladattavaa testipaketin tapaustunnusta. Käytä tätä parametria vain, jos testipaketin nimeä ei ole annettu.
+ `test_case_idN`: Edustaa viimeistä latausta varten ladattavaa testipaketin tapaustunnusta. Käytä tätä parametria vain, jos testipaketin nimeä ei ole annettu.

##### <a name="upload-examples"></a>upload: esimerkit

`upload sample_suite`

`upload 2900`

`upload 123 456`

#### <a name="uploadrecording"></a>uploadrecording

Lataa vain yhteen tai useampaan määritettyyn testitapaukseen kuuluvan tallennustiedoston Azure DevOpsiin.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[test_case_id1] .. [test_case_idN]``

##### <a name="uploadrecording-required-parameters"></a>uploadrecording: pakolliset parametrit

+ `test_case_id1`: Edustaa ensimmäistä testitapauksen tunnusta tallennukselle, joka tulee ladata Azure DevOpsiin.
+ `test_case_idN`: Edustaa viimeistä testitapauksen tunnusta tallennukselle, joka tulee ladata Azure DevOpsiin.

##### <a name="uploadrecording-examples"></a>uploadrecording: esimerkit

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a>käyttö

Tässä välilehdessä näkyvät sovelluksen kolme käyttötapaa.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

Sovelluksen suorittaminen interaktiivisesti:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``

Sovelluksen suorittaminen komennon avulla:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp ``**``[command]``**

Sovelluksen suorittaminen asetustiedoston avulla:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``/settings [drive:\Path to\file.settings] [command]``**

### <a name="windows-powershell-examples"></a>Windows PowerShell -esimerkkejä

#### <a name="run-a-test-case-in-a-loop"></a>Testitapauksen suorittaminen silmukkana

Sinulla on uuden asiakkaan luova testikomentosarja. Tämä testisarja voidaan suorittaa komentosarjojen avulla silmukkana muodostamalla seuraavat tiedot satunnaisesti ennen kunkin iteraation suorittamista:

- Asiakastunnus
- Asiakkaan nimi
- Asiakkaan osoite

Asiakastunnuksen muoto on seuraavanlainen: *ATCUS\<number\>*, jossa \<number\> on arvo on luku **000000001** ja **999999999** väliltä.

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
$excelFilename = "full path to Excel parameter file"
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

```powershell
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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
