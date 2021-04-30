---
title: Suunnittele uusi ER-ratkaisu mukautetun raportin tulostamiseen
description: Tässä ohjeaiheessa kerrotaan miten ER-ratkaisu mukautetun raportin tulostamiseen suunnitellaan.
author: NickSelin
ms.date: 08/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6a3e0e4a8389fdd6580f66004d86ef4b1980dd9f
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891790"
---
# <a name="design-a-new-er-solution-to-print-a-custom-report"></a>Suunnittele uusi ER-ratkaisu mukautetun raportin tulostamiseen

[!include[banner](../includes/banner.md)]

Seuraavissa vaiheissa selitetään, miten järjestelmänvalvoja-, sähköisen raportoinnin kehittäjä- tai sähköisen raportoinnin toiminnallinen konsultti -roolin käyttäjä voi määrittää ER-kehyksen parametrit, suunnitella uuden ER-ratkaisun vaaditut ER-kokoonpanot tietyn yritystoimialueen tietojen käyttöä varten ja luoda mukautetun raportin Microsoft Office -muodossa. Nämä vaiheet voidaan suorittaa **USMF**-yrityksessä.

- [Määritä ER-kehys](#ConfigureFramework)

    - [Konfiguroi ER-parametrit](#ConfigureParameters)
    - [Aktivoi ER-konfiguraation lähde](#ActivateProvider)

        - [Tarkista ER-konfiguraation lähteiden luettelo](#ReviewProvidersList)
        - [Lisää uusi ER-konfiguraation lähde](#AddProvider)
        - [Aktivoi ER-konfiguraation lähde](#ActivateAddedProvider)

- [Toimialuekohtaisen tietomallin suunnitteleminen](#DesignModel)

    - [Uuden tietomallimäärityksen tuominen](#ImportDataModel)
    - [Uuden tietomallin konfiguraation luominen](#DesignDataModel)

        - [Tietomallin nimeäminen](#NameDataModel)
        - [Tietomallikenttien lisääminen](#FieldsEntry)
        - [Tietomallin rakenteen täydentäminen](#CompleteDataModel)

- [Mallin määrityksen suunnitteleminen konfiguroidulle tietomallille](#DesignMapping)

    - [Uuden mallimäärityksen tuominen](#ImportModelMapping)
    - [Uuden mallin yhdistämismäärityksen luominen](#CreateModelMapping)

        - [Uuden mallimäärityskomponentin suunnitteleminen](#DesignMappingComponent)
        - [Tietolähteiden lisääminen sovellustaulujen käyttämiseen](#AddMmDataSource1)
        - [Tietolähteiden lisääminen sovellusluettelointien käyttämiseen](#AddMmDataSource2)
        - [Voit luoda raportin määritetyllä kielellä lisäämällä ER-otsikoita](#AddMmLabels)
        - [Lisää tietolähde muuntamaan lueteltujen arvojen vertailutulokset tekstiarvoihin](#AddMmDataSource3)
        - [Tietolähteen sitominen tietomallikenttiin](#AddMmBindings1)
        - [Mallin määrityksen rakenteen täydentäminen](#CompleteModelMapping)

- [Mukautetun raportin mallin suunnitteleminen](#DesignReportTemplate)
- [Muodon suunnittelu](#DesignFormat)

    - [Tuo suunniteltu muotokonfiguraatio](#FormatImport)
    - [Uuden muotokonfiguraation luominen](#FormatCreate)

        - [Tuo raporttimalli](#ImportReportTemplate)
        - [Muodon konfigurointi](#ConfigureFormat)
        - [Raportin otsikon tietojen sidonnan määrittäminen](#DefineFormatBindings)
        - [Mallin tietolähteen tarkistaminen](#ReviewModelDataSource)
        - [Muotoelementtien sidonta tietolähdekenttiin](#BindFormatElements)

    - [Suunnitellun muodon suorittaminen ER-muodosta](#RunFormatFromER)

- [Suunnitellun muodon säätäminen](#TuneFormat)

    - [Tiedostomuodon muokkaaminen luodun tiedoston nimen muuttamista varten](#ModifyToChangeName)
    - [Muodon muokkaaminen muuttamalla kysymysten järjestystä](#ModifyToOrder)
    - [Muokatun muodon suorittaminen ER-muodosta](#RunFormatFromER2)
    - [Suunnittele muoto loppuun](#CompleteFormat)

- [Sovelluksen artefaktien laatiminen suunniteltua raporttia varten](#DevelopCustomCode)

    - [Lähdekoodin muokkaaminen](#ModifySourceCode)

        - [Tietosopimusluokan lisääminen](#DataContractClass)
        - [UI Builder -luokan lisääminen](#UIBuilderClass)
        - [Tietopalveluluokan lisääminen](#DataProviderClass)
        - [Käyttöliittymätekstitiedoston lisääminen](#LabelsFile)
        - [Raporttipalveluluokan lisääminen](#ServiceClass)
        - [Raportin ohjainluokan lisääminen](#ControllerClass)
        - [Valikkovaihtoehdon lisääminen](#MenuItem)
        - [Valikkovaihtoehdon lisääminen valikkoon](#Menu)
        - [Visual Studio -projektin luominen](#BuildVSProject)

    - [Muodon suorittaminen sovelluksesta](#RunFormatFromApp)

- [Suunnitellun ER-ratkaisun säätäminen](#TuneSolution)

    - [Mallin yhdistämismäärityksen muokkaaminen](#ModifyModelMapping)

        - [Tietolähteiden lisääminen tietosopimusobjektien käyttämiseen](#AddDataSource1)
        - [Tietolähteen lisääminen ER-muotomääritystietueen käyttämiseen](#AddDataSource2)
        - [Tietolähteen lisääminen käynnissä olevan ER-muodon muotomääritystietueen käyttämiseen](#AddDataSource3)
        - [Kirjoita suoritettavan ER-muodon nimi tietomalliin](#AddBinding)
        - [Mallin määrityksen rakenteen täydentäminen](#CompleteModelMapping2)

    - [Muodon muokkaaminen](#ModifyFormat)

        - [Lisää uusi muotoelementti](#AddFormatElement)
        - [Sido lisätty muotoelementti](#BindAddedFormatElement)
        - [Suunnittele muoto loppuun](#CompleteFormat2)

    - [Muodon suorittaminen sovelluksesta](#RunFormatFromApp2)
    - [Muodon suorittaminen ER-muodosta](#RunFormatFromER3)
    - [Muotokohteen määrittäminen näytön esikatselua varten](#ConfigureDestination)
    - [Voit esikatsella sitä PDF-tiedostona suorittamalla sovelluksen muodon](#RunFormatFromApp3)

- [Lisäresurssit](#References)

Tässä esimerkissä luodaan uusi ER-ratkaisu [kyselylomake](../../../human-resources/hr-learning-questionnaires.md)-moduulia varten. Uuden ER-ratkaisun avulla voit suunnitella raportin käyttämällä Microsoft Excel -laskentataulukkoa mallina. Tämän jälkeen voit luoda **kyselylomake**-raportin Excel- tai PDF-muodossa sen lisäksi, että luot aiemmin luodun SQL Server Reporting Services (SSRS) -raportin. Voit myös muokata uutta raporttia myöhemmin pyydettäessä. Koodausta ei tarvita.

1. Voit suorittaa aiemmin luodun raportin siirtymällä kohtaan **kyselylomake** \> **suunnittelu** \> **kyselylomakkeiden raportti**.

    ![Valitaan Kyselylomake-valikkokohta Kysely-moduulista nykyisen SSRS-raportin suorittamiseksi](./media/er-quick-start1-application-menu-origin.png)

2. Määritä valintaehdot **kyselylomakkeiden raportti** -valintaikkunassa. Käytä suodatinta niin, että raportti sisältää vain **SBCCrsExam**-kyselyn.

    ![Kyselylomakkeiden raportti -valintaikkunan valintaehtojen määrittäminen](./media/er-quick-start1-ssrs-report-dialog.png)

Seuraavassa kuvassa näkyy SSRS-raportin luotu versio **SBCCrsExam**-kyselystä.

![Luotu SSRS-raportti](./media/er-quick-start1-ssrs-report.png)

## <a name="configure-the-er-framework"></a><a name="ConfigureFramework"></a>Määritä ER-kehys

Sähköisen raportoinnin toiminnallisen kehittäjän roolissa olevan käyttäjän on määritettävä sähköisen raportoinnin parametrien vähimmäisjoukko, ennen kuin voit alkaa käyttää ER-kehystä uuden ER-ratkaisusi suunnitteluun.

### <a name="configure-er-parameters"></a><a name="ConfigureParameters"></a>Konfiguroi ER-parametrit

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Sähköinen raportointi** -työtilasta **Sähköisen raportoinnin parametrit**.
3. Määritä **Sähköisen raportoinnin parametrit** -sivun **Yleinen**-välilehdessä **Ota käyttöön suunnittelutila** -asetukseksi **Kyllä**.
4. Määritä **Liitteet**-välilehdessä seuraavat parametrit:

    - Määritä **Konfiguraatiot**-kenttä **Tiedostoon** **USMF**-yritykselle.
    - Määritä **Työarkisto**-, **Väliaikainen**-, **Perusrivi**- ja **Muut**-kentissä **Tiedostoon**.

Lisätietoja ER-parametreista on kohdassa [Määritä ER-kehys](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a name="ActivateProvider"></a>Aktivoi ER-konfiguraation lähde

Jokainen ER-konfiguraatio merkitään ER-konfiguraation lähteen omistamaksi. Siksi sinun on aktivoitava ER-konfiguraation lähde **Sähköinen raportointi** -työtilassa, ennen kuin voit alkaa lisätä tai muokata mitä tahansa ER-konfiguraatioita.

> [!NOTE]
> Vain ER-konfiguraation omistaja voi muokata sitä. Siksi ennen kuin ER-konfiguraatiota voi muokata, asianmukainen ER-konfiguraation lähde on aktivoitava **Sähköinen raportointi** -työtilassa.

#### <a name="review-the-list-of-er-configuration-providers"></a><a name="ReviewProvidersList"></a>Tarkista ER-konfiguraation lähteiden luettelo

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Sähköisen raportointi** -työtilan **Liittyvät linkit** -osassa **Konfiguraation lähteet**.
3. **Konfiguraation lähteet** -sivulla jokaisen konfiguraation lähteen tietueella on yksilöllinen nimi ja URL-osoite. Tarkista tämän sivun sisältö. Jos **Litware, Inc.** (`https://www.litware.com`) -tietue on jo olemassa, ohita seuraava menettely, [Lisää uusi ER-konfiguraation lähde](#ActivateProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a name="AddProvider"></a>Lisää uusi ER-konfiguraation lähde

1. Valitse **Konfiguraation lähteet**-sivulla **Uusi**.
2. Kirjoita **Nimi**-kenttään **Litware, Inc.**
3. Kirjoita **Internetosoite**-kenttään `https://www.litware.com`.
4. Valitse **Tallenna**.

#### <a name="activate-an-er-configuration-provider"></a><a name="ActivateAddedProvider"></a>Aktivoi ER-konfiguraation lähde

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Sähköinen raportointi** -työtilassa **Litware, Inc**-määrityspalvelu.
3. Valitse **Määritä aktiivinen**.

Lisätietoja ER-konfiguraation lähteistä on kohdassa [Konfiguraation lähteiden luonti ja merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="design-a-domain-specific-data-model"></a><a name="DesignModel"></a>Toimialuekohtaisen tietomallin suunnitteleminen

Sinun on luotava uusi ER-konfiguraatio, joka sisältää [tietomalli](general-electronic-reporting.md#data-model-and-model-mapping-components)-komponentin **Kyselyn** liiketoimialueelle. Tätä tietomallia käytetään myöhemmin tietolähteenä suunniteltaessa ER-muotoa **kyselylomake**-raportin luomiseksi.

Kun [tuot uuden tietomallin määritys](#ImportDataModel) -osan vaiheet, voit tuoda vaaditun tietomallin mukana olevasta XML-tiedostosta. Voit myös suorittaa [uuden tietomallin määrityksen luomisen](#DesignDataModel) vaiheet ja suunnitella tämän tietomallin alusta alkaen.

### <a name="import-a-new-data-model-configuration"></a><a name="ImportDataModel"></a>Uuden tietomallimäärityksen tuominen

1. Lataa [kyselylomakkeet model.version.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) -tiedosto ja tallenna se paikalliseen tietokoneeseen.
2. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
3. Valitse **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**.
4. Valitse toimintoruudussa **Vaihda** \> **Lataa XML-tiedostosta**.
5. Valitse **Selaa** ja etsi ja valitse **kyselylomakkeiden model.version.1.xml** -tiedosto.
6. Tuo konfigurointi valitsemalla **OK**.

Jos haluat jatkaa, ohita seuraavat vaiheet, [Luo uusi tietomallin konfiguraatio](#DesignDataModel).

### <a name="create-a-new-data-model-configuration"></a><a name="DesignDataModel"></a>Uuden tietomallin konfiguraation luominen

1. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
2. Valitse **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**.
3. Valitse **Luo konfiguraatio**.
4. Kirjoita avattavan luettelon **Nimi**-kenttään **Kyselylomakemalli**.
5. Valitse **Luo konfigurointi** luodaksesi konfiguroinnin.

#### <a name="name-the-data-model"></a><a name="NameDataModel"></a>Tietomallin nimeäminen

1. Valitse **Konfiguraatiot**-sivun konfiguraatiopuun kohdasta **Kyselylomakemalli**.
2. Valitse **Suunnittelu**.
3. Kirjoita **tietomallin suunnittelu** -sivun **Yleinen**-pikavälilehden **Nimi**-kenttään <a name="DataModeName"></a>**kyselylomakkeet**.

#### <a name="add-new-data-model-fields"></a><a name="FieldsEntry"></a>Uusien tietomallikenttien lisääminen

1. Valitse **Tietomallisuunnittelu**-sivulla **Uusi**.
2. Tee seuraavat toimet avattavassa valintaikkunassa tietomallisolmun lisäämistä varten:

    1. Valitse uuden solmun tyypiksi **mallijuuri**.
    2. Kirjoita **Nimi**-kenttään <a name="RootDefinitionName"></a>**Juuri**.
    3. Valitse **Lisää** lisätäksesi uuden solmun.

    Tätä pääkuvausta käytetään **kyselylomake**-raportin tietojen toimittamisessa. Yksittäisellä tietomallilla voi olla useita kuvaajia. Kukin kuvaus voidaan määrittää yksittäiselle ER-muodolle, jotta raportin luomisessa tarvittavat tiedot tunnistetaan.

3. Valitse **Uusi** uudelleen ja tee sitten seuraavat toimet avattavassa valintaikkunassa tietomallisolmun lisäämistä varten:

    1. Valitse **Aktiivisen solmun alikohde** uuden solmun tyypiksi.
    2. Kirjoita **Nimi**-kenttään **CompanyName**.
    3. Valitse **Nimiketyyppi**-kentässä **Merkkijono**.
    4. Valitse **Lisää** lisätäksesi uuden kentän.

    Tämä kenttä on pakollinen, jotta nykyisen yrityksen nimi voidaan välittää ER-raportiksi, joka kuluttaa tämän tietomallin tietolähteenä.

4. Valitse **Uusi** uudelleen ja tee sitten seuraavat toimet avattavassa valintaikkunassa tietomallisolmun lisäämistä varten:

    1. Valitse **Aktiivisen solmun alikohde** uuden solmun tyypiksi.
    2. Kirjoita **Nimi**-kenttään **Kyselylomake**.
    3. Valitse **Nimiketyyppi**-kentässä **Tietueluettelo**.
    4. Valitse **Lisää** lisätäksesi uuden kentän.

    Tätä kenttää käytetään siirtämään kyselylomake ER-raporttiin, joka kuluttaa tämän tietomallin tietolähteenä.

5. Valitse **kyselylomake**-solmu.
6. Jatka muokattavien tietomallien pakollisten kenttien lisäämistä samalla tavalla, kunnes seuraava tietomallirakenne on valmis.

    | Kentän polku                                                    | Tietotyyppi   | Kentän nimi/palautettu arvo |
    |---------------------------------------------------------------|-------------|----------------------------------|
    | Juuri                                                          |             | Viitepistekyselylomakkeen tietojen pyytämisen yhteydessä. |
    | Juuri\\CompanyName                                             | Merkkijono      | Nykyisen yrityksen nimi. |
    | Juuri\\ExecutionContext                                        | Tallenna      | Muotoile suorituksen tiedot. |
    | Juuri\\ExecutionContext\\FormatName                            | Merkkijono      | Suoritettavan ER-muodon nimi. |
    | Juuri\\Kyselylomake                                           | Tietueluettelo | Kyselylomakkeiden luettelo |
    | Juuri\\kyselylomake\\aktiivinen                                   | Merkkijono      | Nykyisen kyselylomakkeen tila. |
    | Juuri\\Kyselylomake\\Koodi                                     | Merkkijono      | Nykyisen kyselylomakkeen koodi. |
    | Juuri\\Kyselylomake\\Kuvaus                              | Merkkijono      | Nykyisen kyselylomakkeen kuvaus. |
    | Juuri\\Kyselylomake\\QuestionnaireType                        | Merkkijono      | Nykyisen kyselylomakkeen tyyppi. |
    | Juuri\\Kyselylomake\\QuestionOrder                            | Merkkijono      | Nykyisen kyselylomakkeen numerojärjestys. |
    | Juuri\\Kyselylomake\\ResultsGroup                             | Tallenna      | Nykyisen kyselylomakkeen tulosparametrit. |
    | Juuri\\Kyselylomake\\ResultsGroup\\Koodi                       | Merkkijono      | Nykyisen tulosryhmän tunnuskoodi. |
    | Juuri\\Kyselylomake\\ResultsGroup\\Kuvaus                | Merkkijono      | Nykyisen tulosryhmän kuvaus. |
    | Juuri\\Kyselylomake\\ResultsGroup\\MaxNumberOfPoints          | Reaaliluku        | Ansaittujen pisteiden enimmäismäärä. |
    | Juuri\\Kyselylomake\\Kysymys                                 | Tietueluettelo | Nykyisen kyselylomakkeen kysymysluettelo. |
    | Juuri\\Kyselylomake\\Kysymys\\CollectionSequenceNumber       | Kokonaisluku     | Nykyisen vastauskokoelman järjestysnumero. |
    | Juuri\\Kyselylomake\\Kysymys\\Tunnus                             | Merkkijono      | Nykyisen kysymyksen tunnuskoodi. |
    | Juuri\\Kyselylomake\\Kysymys\\MustBeCompleted                | Merkkijono      | Lippu, joka ilmaisee, onko nykyiseen kysymykseen vastattava. |
    | Juuri\\Kyselylomake\\Kysymys\\PrimaryQuestion                | Merkkijono      | Lippu, joka ilmaisee, onko nykyinen kysymys ensisijainen. |
    | Juuri\\Kyselylomake\\Kysymys\\SequenceNumber                 | Kokonaisluku     | Nykyisen kysymyksen järjestysnumero. |
    | Juuri\\Kyselylomake\\Kysymys\\Teksti                           | Merkkijono      | Nykyisen kysymyksen teksti. |
    | Juuri\\Kyselylomake\\Kysymys\\Vastaus                         | Tietueluettelo | Nykyisen kysymyksen vastausluettelo. |
    | Juuri\\Kyselylomake\\Kysymys\\Vastaus\\CorrectAnswer          | Merkkijono      | Lippu, joka ilmaisee, onko nykyinen vastaus oikein. |
    | Juuri\\Kyselylomake\\Kysymys\\Vastaus\\Pisteet                 | Reaaliluku        | Pisteet, jotka ansaitaan nykyisen vastauksen valinnan yhteydessä. |
    | Juuri\\Kyselylomake\\Kysymys\\Vastaus\\SequenceNumber         | Kokonaisluku     | Nykyisen vastauksen järjestysnumero. |
    | Juuri\\Kyselylomake\\Kysymys\\Vastaus\\Teksti                   | Merkkijono      | Nykyisen vastauksen teksti. |

    Seuraavassa kuvassa näkyy **tietomallin suunnittelu** -sivulla valmiiksi muokattava tietomalli.

    ![Konfiguroitu tietomalli ER-tietomallin suunnittelussa](./media/er-quick-start1-model2.png)

7. Tallenna muutokset.
8. Sulje **Tietomallin suunnittelu** -sivu.

#### <a name="complete-the-design-of-the-data-model"></a><a name="CompleteDataModel"></a>Tietomallin rakenteen täydentäminen

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Konfiguraatiot**-sivun konfiguraatiopuun kohdasta **Kyselylomakemalli**.
3. Valitse **Versiot**-pikavälilehdessä konfiguraatioversio, jonka tila on **Luonnos**.
4. Valitse **Muutoksen tila** \> **Viimeistele**.

Tämän konfiguraation version 1 tila muutetaan **luonnoksesta** **valmiiksi**. Versiota 1 ei voi enää muuttaa. Tämä versio sisältää konfiguroidun tietomallin, ja sitä voidaan käyttää muiden ER-konfiguraatioiden pohjana. Tämän konfiguraation versio 2 luodaan, ja sen tila on **luonnos**. Voit muokata tätä versiota, jos haluat muuttaa **kyselylomakkeen** tietomallia.

![Konfiguraatiosivun muokattavan ER-konfiguraation versiot](./media/er-quick-start1-model-configuration.png)

Lisätietoja ER-kokoonpanojen versiotiedoista on kohdassa [sähköisen raportoinnin (ER) yleiskuvaus](general-electronic-reporting.md#component-versioning).

> [!NOTE]
> Määritetty tietomalli on **kyselylomakkeen** liiketoimialueen abstrakti esitystapa, eikä se sisällä suhteita Microsoft Dynamics 365 Financen artefakteihin.

## <a name="design-a-model-mapping-for-the-configured-data-model"></a><a name="DesignMapping"></a>Mallin määrityksen suunnitteleminen konfiguroidulle tietomallille

Sähköisen raportoinnin kehittäjän roolin käyttäjänä sinun on luotava uusi ER-konfiguraatio, joka sisältää **kyselylomakkeen** tietomallin [mallinyhdistämis](general-electronic-reporting.md#data-model-and-model-mapping-components)-komponentin . Koska tämä komponentti toteuttaa Financen konfiguroidun tietomallin, se on Finance-kohtainen. Mallikartoituskomponentti on konfiguroitava niin, että se määrittää sovellusobjektit, joita käytetään määritetyn tietomallin täyttämiseen sovellustiedoilla suorituksen aikana. Tämän tehtävän suorittaminen edellyttää, että olet tietoinen Financen **kyselylomakkeen** liiketoimialueen tietorakenteen toteutustiedoista.

Kun teet loppuun [tuot uuden mallin yhdistämismääritys](#ImportModelMapping) -osan vaiheet, voit tuoda vaaditun uuden mallin yhdistämismäärityksen mukana olevasta XML-tiedostosta. Voit myös suorittaa [uuden mallin yhdistämismäärityksen](#CreateModelMapping) vaiheet ja suunnitella tämän mallin yhdistämismäärityksen alusta alkaen.

### <a name="import-a-new-model-mapping-configuration"></a><a name="ImportModelMapping"></a>Uuden mallin yhdistämismäärityksen tuominen

1. Lataa [kyselylomakkeet mapping.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) -tiedosto ja tallenna se paikalliseen tietokoneeseen.
2. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
3. Valitse **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**.
4. Valitse toimintoruudussa **Vaihda** \> **Lataa XML-tiedostosta**.
5. Valitse **Selaa** ja etsi ja valitse **kyselylomakkeiden mapping.version.1.1.xml** -tiedosto.
6. Tuo konfigurointi valitsemalla **OK**.

Jos haluat jatkaa, ohita seuraavat vaiheet, [Luo uusi mallin yhdistämiskonfiguraatio](#CreateModelMapping).

### <a name="create-a-new-model-mapping-configuration"></a><a name="CreateModelMapping"></a>Uuden mallin yhdistämismäärityksen luominen

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Konfiguraatiot**-sivun konfiguraatiopuun kohdasta **Kyselylomakemalli**.
3. Valitse **Luo konfiguraatio**.
4. Toimi avattavassa valintaikkunassa seuraavasti:

    1. Syötä **Uusi**-kenttään **Tietomallikyselylomakkeisiin perustuvat mallin määritykset**.
    2. Kirjoita **Nimi**-kenttään **Kyselylomakkeen yhdistäminen**.
    3. **Valitse tietomallin määritys** -kentässä **Juuri**-määritys.
    4. Valitse **Luo konfigurointi** luodaksesi konfiguroinnin.

#### <a name="design-a-new-model-mapping-component"></a><a name="DesignMappingComponent"></a>Uuden mallimäärityskomponentin suunnitteleminen

1. Valitse **Konfiguraatiot**-sivun konfiguraatiopuun kohdasta **Kyselylomakkeen yhdistäminen**.
2. Avaa määritysluettelo valitsemalla **Suunnittelutoiminto**.
3. Valitse **kyselylomakkeiden yhdistämismääritys**, joka lisättiin automaattisesti **Juuri**-määritystä varten
4. Aloita valitun yhdistämismäärityksen määrittäminen valitsemalla **Suunnittelu**-toiminto.

**Juuri**-määritykselle lisätään automaattisesti uusi yhdistämismääritys. Tässä yhdistämisessä on **malliin**-suunta. Tämän vuoksi tätä määritystä voidaan käyttää tarvittavien tietojen tietomallin täyttämiseen.

#### <a name="add-data-sources-to-access-application-tables"></a><a name="AddMmDataSource1"></a>Tietolähteiden lisääminen sovellustaulujen käyttämiseen

Sinun on konfiguroitava tietolähteet, jotta voit käyttää kyselylomakkeen tietoja sisältäviä sovellustauluja.

1. Valitse **Mallin määrityksen suunnittelu** -sivun **Tietolähdetyypit**-ruudusta **Dynamics 365 for Operations\\Taulukkotiedot**.
2. Lisää uusi tietolähde, jonka avulla pääsee käyttämään KMCollection-taulua, jossa jokainen tietue vastaa yhtä kyselylomaketta:

    1. Valitse **Tietolähteet**-ruudussa **Lisää juuri**.
    2. Kirjoita valintaikkunan **Nimi**-kentässä **Kyselylomake**.
    3. Kirjoita **Taulu**-kenttään **KMCollection**.
    4. Määritä **Kysy kyselyä** -asetukseksi **Kyllä**. Tämän jälkeen voit määrittää tämän taulun [suodatus](../../fin-ops/get-started/advanced-filtering-query-options.md)-asetukset järjestelmän kyselyvalintaikkunassa suorituksen aikana.
    5. Lisää uusi tietolähde valitsemalla **OK**.

3. Valitse **Tietolähdetyypit**-ruudusta **Dynamics 365 for Operations\\Taulukkotiedot**.
4. Lisää uusi tietolähde, jonka avulla pääsee käyttämään KMQuestion-taulua, jossa jokainen tietue vastaa yhtä kysymystä lomakkeessa:

    1. Valitse **Tietolähteet**-ruudussa **Lisää juuri**.
    2. Kirjoita valintaikkunan **Nimi**-kenttään **Kysymys**.
    3. Kirjoita **Taulu**-kenttään **KMQuestion**.
    4. Lisää uusi tietolähde valitsemalla **OK**.

5. Valitse **Tietolähdetyypit**-ruudusta **Dynamics 365 for Operations\\Taulukkotiedot**.
6. Lisää uusi tietolähdeyritys, jonka avulla pääsee käyttämään KMAnswer-taulua, jossa jokainen tietue vastaa yhtä vastausta lomakkeessa:

    1. Valitse **Tietolähteet**-ruudussa **Lisää juuri**.
    2. Kirjoita **Nimi**-kenttään **Vastaus**.
    3. Kirjoita **Taulu**-kenttään **KMAnswer**.
    4. Lisää uusi tietolähde valitsemalla **OK**.

7. Valitse **Tietolähdetyypit**-ruudusta **Toiminnot\\Laskettu kenttä**.
8. Lisää uusi laskettu kenttä, jonka avulla voidaan käyttää KMQuestionResultGroup-taulun tietuetta pää-KMCollection-taulun jokaisesta tietueesta:

    1. Valitse **Tietolähteet**-ruudussa **Kyselylomake**.
    2. Valitse **Lisää**.
    3. Kirjoita valintaikkunan **Nimi**-kenttään **\$ResultGroup**.
    4. Valitse **Muokkaa kaavaa**.
    5. Syötä [ER-kaavaeditorin](general-electronic-reporting-formula-designer.md) **Kaava**-kenttään **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)**, jos haluat käyttää KMCollection- ja KMQuestionResultGroup-taulujen välistä yksi-moneen-[yhteyttä](er-formula-language.md#paths).
    6. Valitse **Tallenna** ja sulje kaavaeditori.
    7. Lisää uusi laskettu kenttä valitsemalla **OK**.

9. Valitse **Tietolähdetyypit**-ruudusta **Toiminnot\\Laskettu kenttä**.
10. Lisää uusi laskettu kenttä, jonka avulla voidaan käyttää KMQuestion-taulun kysymystietueita pää-KMCollectionQuestion-taulun jokaisesta tietueesta:

    1. Valitse **Tietolähteet**-ruudussa **Kyselylomake**.
    2. Laajenna **\<Suhteet**-solmu, joka sisältää yksi-moneen-suhteet KMCollection-tauluun.
    3. Valitse liittyvä **KMCollectionQuestion**-taulu ja valitse sitten **Lisää**.
    4. Kirjoita valintaikkunan **Nimi**-kenttään **\$Kysymys**.
    5. Valitse **Muokkaa kaavaa**.
    6. Kirjoita kaavaeditorissa **Kaava**-kenttään **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** ja palauta asianmukaiset kysymystiedot KMQuestion-taulusta.
    7. Valitse **Tallenna** ja sulje kaavaeditori.
    8. Lisää uusi laskettu kenttä valitsemalla **OK**.

11. Valitse **Tietolähdetyypit**-ruudusta **Toiminnot\\Laskettu kenttä**.
12. Lisää uusi laskettu kenttä, jonka avulla voidaan käyttää KMAnswer-taulun vastaustietueita pää-KMQuestion-taulun jokaisesta tietueesta:

    1. Valitse **Tietolähteet**-ruudussa **Kyselylomake.\<Relations.KMCollectionQuestion.\$Kysymys** ja valitse sitten **Lisää**.
    2. Kirjoita valintaikkunan **Nimi**-kenttään **\$Vastaus**.
    3. Valitse **Muokkaa kaavaa**.
    4. Kirjoita kaavaeditorissa **Kaava**-kenttään **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** ja palauta asianmukaiset vastaustiedot KMAnswer-taulusta.
    5. Valitse **Tallenna** ja sulje kaavaeditori.
    6. Lisää uusi laskettu kenttä valitsemalla **OK**.

13. Valitse **Tietolähdetyypit**-ruudusta **Dynamics 365 for Operations\\Taulukko**.
14. Lisää uusi tietolähde, jota käytetään CompanyInfo-taulun menetelmien käyttämiseen. Huomaa, että tämän taulun **find()**-menetelmä palauttaa tietueen, joka edustaa nykyisen Finance-instanssin yritystä, jota tämä yhdistäminen kutsuu kontekstissa.

    1. Valitse **Tietolähteet**-ruudussa **Lisää juuri**.
    2. Kirjoita valintaikkunan **Nimi**-kenttään **CompanyInfo**.
    3. Kirjoita **Taulu**-kenttään **CompanyInfo**.
    4. Lisää uusi tietolähde valitsemalla **OK**.

#### <a name="add-data-sources-to-access-application-enumerations"></a><a name="AddMmDataSource2"></a>Tietolähteiden lisääminen sovellusluettelointien käyttämiseen

Sinun on konfiguroitava tietolähteet, jotta voit käyttää sovellusten luettelointeja ja verrattava niiden arvoja **luettelointi**-tyypin kenttien arvoihin sovellustaulukoissa. Sinun on käytettävä vertailun tuloksia tietomallin asianmukaisten kenttien täyttämiseen.

1. Valitse **Mallin määrityksen suunnittelu** -sivun **Tietolähdetyypit**-ruudusta **Dynamics 365 for Operations\\Luettelointi**.
2. Lisää uusi tietolähde, jota käytetään **EnumAppNoYes**-luettelon arvojen käyttämiseen.

    1. Valitse **Tietolähteet**-ruudussa **Lisää juuri**.
    2. Kirjoita valintaikkunan **Nimi**-kenttään **EnumAppNoYes**.
    3. Kirjoita **luettelointi**-kenttään **NoYes**.
    4. Lisää uusi tietolähde valitsemalla **OK**.

3. Valitse **Tietolähdetyypit**-ruudusta **Dynamics 365 for Operations\\Luettelointi**.
4. Lisää uusi tietolähde, jota käytetään **KMCollectionQuestionMode**-luettelon arvojen käyttämiseen.

    1. Valitse **Tietolähteet**-ruudussa **Lisää juuri**.
    2. Kirjoita valintaikkunan **Nimi**-kentässä **EnumAppQuestionOrder**.
    3. Kirjoita **luettelointi**-kenttään **KMCollectionQuestionMode**.
    4. Lisää uusi tietolähde valitsemalla **OK**.

#### <a name="add-er-labels-to-generate-a-report-in-a-specified-language"></a><a name="AddMmLabels"></a>Voit luoda raportin määritetyllä kielellä lisäämällä ER-otsikoita

Voit lisätä ER-otsikoita ja määrittää jotkin tietolähteet palauttamaan arvoja, jotka määräytyvät mallin yhdistämiskutsun kontekstissa määritetyn kielen mukaan.

1. Valitse **Mallin määrityksen suunnittelu** -sivun **Tietolähteet**-ruudusta **Vastaus** ja valitse sitten **Muokkaa**.
2. Aktivoi **Otsikko**-kenttä.
3. Valitse **Käännä**.
4. Toimi **Tekstin kääntäminen** -valintaikkunassa seuraavasti:

    1. Kirjoita **Etiketin tunnus** -kenttään **PositiveAnswer**.
    2. Kirjoita **Teksti oletuskielellä** -kenttään **Kyllä**.
    3. Valitse **Käännä**.
    4. Kirjoita **Etiketin tunnus**-kenttään **NegativeAnswer**.
    5. Kirjoita **Teksti oletuskielellä** -kenttään **Ei**.
    6. Valitse **Käännä**.

5. Sulkee **tekstin kääntäjä** -valintaikkunan.
6. Valitse **Peruuta**.

![Muokattavien mallimääritysten ER-otsikoiden lisääminen](./media/er-quick-start1-adding-labels.png)

Olet kirjoittanut vain oletuskielelle määritetyt ER-etiketit. Lisätietoja siitä, miten ER-etiketit voidaan kääntää muille kielille, on ohjeaiheessa [Monikielisten raporttien suunnitteleminen](er-design-multilingual-reports.md).

#### <a name="add-a-data-source-to-transform-the-results-of-comparing-enumeration-values-to-a-text-value"></a><a name="AddMmDataSource3"></a>Lisää tietolähde muuntamaan lueteltujen arvojen vertailutulokset tekstiarvoihin

Koska luettelointiarvojen ja tekstiarvojen vertailun tulokset on muunnettava useita kertoja lähteiden erojen osalta, tämä logiikka kannattaa määrittää yhdeksi tietolähteeksi. Jotta voisit käyttää tätä tietolähdettä uudelleen, sinun on kuitenkin määritettävä se parametrisoiduksi tietolähteeksi. Katso lisätietoja kohdasta [Lasketun kentän muotoisten sähköisen raportoinnin tietolähteiden parametrisoitujen kutsujen tukeminen](er-calculated-field-type.md).

1. Valitse **Mallin määrityksen suunnittelu** -sivun **Tietolähdetyypit**-ruudusta **Yleiset\\Tyhjä säilö**.
2. Lisää uusi säilötietolähde:

    1. Valitse **Tietolähteet**-ruudussa **Lisää juuri**.
    2. Kirjoita valintaikkunan **Nimi**-kentässä **Avustaja**.
    3. Lisää uusi säilötietolähde valitsemalla **OK**.

3. Valitse **Tietolähdetyypit**-ruudusta **Toiminnot\\Laskettu kenttä**.
4. Uuden tietolähteen lisääminen:

    1. Valitse **Tietolähteet**-ruudussa **Avustaja**.
    2. Valitse **Lisää**.
    3. Kirjoita valintaikkunan **Nimi**-kenttään **NoYesEnumToString**.
    4. Valitse **Muokkaa kaavaa**.
    5. Valitse kaavaeditorissa **Parametrit**.
    6. Voit määrittää parametrit määritetylle lausekkeelle noudattamalla seuraavia ohjeita:

        1. Valitse **Uusi**.
        2. Kirjoita valintaikkunan **Nimi**-kenttään **Argumentti**.
        3. Valitse **Tyyppi**-kentässä **Totuusarvo**-tietotyyppi.
        4. Valitse **OK**.

    7. Kirjoita **Kaava**-kenttään **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")**, jos haluat, että oikean varoitusetiketin teksti palautetaan sen mukaan, mikä on suorituskontekstin kieli ja määritetyn parametrin arvo.
    8. Valitse **Tallenna** ja sulje kaavaeditori.
    9. Lisää uusi tietolähde valitsemalla **OK**.

![Konfiguroitu mallin määritys ER-tietomallin määrityksen suunnittelussa](./media/er-quick-start1-added-data-sources.png)

#### <a name="bind-data-sources-to-data-model-fields"></a><a name="AddMmBindings1"></a>Tietolähteen sitominen tietomallikenttiin

Sinun on sidottava määritetyt tietolähteet tietomallin kenttiin, jotta voit määrittää, miten tietomalli täytetään sovellustiedoilla suorituksen aikana.

1. Valitse **Mallin määrityksen suunnittelu** -sivun **Tietomalli**-ruudusta **CompanyName**.
2. Laajenna **Tietolähteet**-ruudussa **CompanyInfo** ja toimi seuraavasti:

    1. Laajenna **CompanyInfo.find()**-solmu, joka vastaa CompanyInfo-taulukon **find()**-menetelmää.
    2. Valitse **CompanyInfo.find().Name**.
    3. Valitse **sido**, jos haluat täyttää sen yrityksen nimen, jota konfiguroitu mallin määritys kutsuu suorituksen yhteydessä.

3. Valitse **Tietomalli**-ruudussa **Kyselylomake**.
4. Valitse **Tietolähteet**-ruudussa **Kyselylomake** ja valitse sitten **Sido** täyttääksesi kyselytietueet.
5. Laajenna **Tietomalli**-ruudussa **Kyselylomake** ja toimi seuraavasti:

    1. Valitse **Tietomalli**-ruudussa **Aktiivinen**.
    2. Valitse **Tietomalli**-ruudussa **Muokkaa**.
    3. Kirjoita **Kaava**-kenttään **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)**, jos haluat täyttää tekstin ja kielestä riippuvan tuloksen luettelointiarvojen vertailusta.

6. Jatka tietolähteiden sidontaa tietomallin kenttiin samalla tavalla, kunnes saavutat seuraavan tuloksen.

    | Kentän polku                                              | Tietotyyppi   | Toimenpide | Sitova lauseke |
    |---------------------------------------------------------|-------------|--------|--------------------|
    | CompanyName                                             | Merkkijono      | Sido   | CompanyInfo.'find()'.Name |
    | Kyselylomake                                           | Tietueluettelo | Sido   | Kyselylomake |
    | Kyselylomake\\Aktiivinen                                   | Merkkijono      | Muokkaa   | Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes) |
    | Kyselylomake\\Koodi                                     | Merkkijono      | Sido   | \@.kmCollectionId |
    | Kyselylomake\\Kuvaus                              | Merkkijono      | Sido   | \@.Kuvaus |
    | Kyselylomake\\QuestionnaireType                        | Merkkijono      | Sido   | \@.'&gt;Relations'.kmCollectionTypeId.Description |
    | Kyselylomake\\QuestionOrder                            | Merkkijono      | Muokkaa   | CASE (\@.questionMode,<br>EnumAppQuestionOrder.Conditional, "Conditional",<br>EnumAppQuestionOrder.Random, "Satunnainen (kyselylomakkeen prosenttiosuus)",<br>EnumAppQuestionOrder.RandomGroup, "Satunnainen (vastausryhmien prosenttiosuus)",<br>EnumAppQuestionOrder.Sequence, "Sequential",<br>"") |
    | Kyselylomake\\ResultsGroup                             | Tallenna      |        | |
    | Kyselylomake\\ResultsGroup\\Koodi                       | Merkkijono      | Sido   | \@.'\$ResultGroup'.kmQuestionResultGroupId |
    | Kyselylomake\\ResultsGroup\\Kuvaus                | Merkkijono      | Sido   | \@.'\$ResultGroup'.description |
    | Kyselylomake\\ResultsGroup\\MaxNumberOfPoints          | Reaaliluku        | Sido   | \@.'\$ResultGroup'.maxPoint |
    | Kyselylomake\\Kysymys                                 | Tietueluettelo | Sido   | \@.'&lt;Relations'.KMCollectionQuestion |
    | Kyselylomake\\Kysymys\\CollectionSequenceNumber       | Kokonaisluku     | Sido   | \@.answerCollectionSequenceNumber |
    | Kyselylomake\\Kysymys\\Tunnus                             | Merkkijono      | Sido   | \@.kmQuestionId |
    | Kyselylomake\\Kysymys\\MustBeCompleted                | Merkkijono      | Muokkaa   | Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes) |
    | Kyselylomake\\Kysymys\\PrimaryQuestion                | Merkkijono      | Sido   | \@.parentQuestionId |
    | Kyselylomake\\Kysymys\\SequenceNumber                 | Kokonaisluku     | Sido   | \@.SequenceNumber |
    | Kyselylomake\\Kysymys\\Teksti                           | Merkkijono      | Sido   | \@.'\$Question'.text |
    | Kyselylomake\\Kysymys\\Vastaus                         | Tietueluettelo | Sido   | \@.'\$Question'.'\$Answer' |
    | Kyselylomake\\Kysymys\\Vastaus\\CorrectAnswer          | Merkkijono      | Muokkaa   | Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes) |
    | Kyselylomake\\Kysymys\\Vastaus\\Pisteet                 | Reaaliluku        | Sido   | \@.point |
    | Kyselylomake\\Kysymys\\Vastaus\\SequenceNumber         | Kokonaisluku     | Sido   | \@.sequenceNumber |
    | Kyselylomake\\Kysymys\\Vastaus\\Teksti                   | Merkkijono      | Sido   | \@.text |

    Seuraavassa kuvassa näkyy **mallikartoituksen suunnittelu** -sivulla määritetyn mallikartoituksen lopullinen tila.

    ![Täysin konfiguroitu mallin määritys ER-tietomallin määrityksen suunnittelussa](./media/er-quick-start1-mapping2.png)

7. Tallenna muutokset.
8. Sulje **Mallimäärityksen sunnittelun** sivu.

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping"></a>Mallin määrityksen rakenteen täydentäminen

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Konfiguraatiot**-sivun konfiguraatiopuun kohdasta **Kyselylomakkeen yhdistäminen**.
3. Valitse **Versiot**-pikavälilehdessä konfiguraatioversio, jonka tila on **Luonnos**.
4. Valitse **Muutoksen tila** \> **Viimeistele**.

Tämän konfiguraation version 1.1 tila muutetaan **luonnoksesta** **valmiiksi**. Versiota 1.1 ei voi enää muuttaa. Tämä versio sisältää konfiguroidun mallin määrityksen, ja sitä voidaan käyttää muiden ER-konfiguraatioiden pohjana. Tämän konfiguraation versio 1.2 luodaan, ja sen tila on **luonnos**. Voit muokata tätä versiota, jos haluat muuttaa **kyselylomakkeen määrityksen** määritystä.

![Konfiguraatiosivun muokattavan ER-konfiguraation versiot](./media/er-quick-start1-mapping-configuration.png)

> [!NOTE]
> Määritetty mallimääritys on **kyselylomakkeen** liiketoimialuetta edustavan abstraktin tietomallin Finance-kohtainen toteutus.

## <a name="design-a-template-for-a-custom-report"></a><a name="DesignReportTemplate"></a>Mukautetun raportin mallin suunnitteleminen

ER-kehys käyttää ennalta määritettyjä malleja luodakseen tiedostoja Microsoft Office -muodoissa (Excel-työkirjoissa tai Word-asiakirjoissa). Kun tarvittava raportti luodaan, malliin täytetään tarvittavat tiedot määritetyn tietovuomäärityksen mukaan. Siksi sinun on ensin suunniteltava malli mukautettua raporttia varten. Tämä malli on suunniteltava Excel-työkirjana, jonka rakenne edustaa mukautetun raportin asettelua. Sinun on annettava jokaiselle Excel-kohteelle nimi, jonka aiot täyttää vaaditulla tiedoilla.

1. Lataa [kyselylomakkeiden raporttimalli.xslx](https://go.microsoft.com/fwlink/?linkid=851448) -tiedosto ja tallenna se paikalliseen tietokoneeseen.
2. Avaa tiedosto Excelissä ja tarkista työkirjan rakenne.

Kuten seuraavasta kuvasta näkyy, ladattu malli on suunniteltu tulostamaan kyselylomakkeita, joissa esitetään kyselyn kysymykset sekä asianmukaiset vastaukset.

![Excel-malli määritettyjen kyselylomakkeiden tulostamista varten](./media/er-quick-start1-template-layout.png)

Tähän malliin on lisätty Excel-nimiä kyselylomakkeen tietojen täyttämistä varten. Nimien hallinnan avulla voit tarkistaa Excelin nimet.

![Nimen hallinnan käyttäminen Excelin nimien tarkistamiseen annetussa Excel-mallissa](./media/er-quick-start1-template-names.png)

Raportin otsikot on lisätty englannin kielellä vakiotekstinä. Voit korvata raportin otsikot uusilla Excelin nimillä, jotka täyttävät otsikot ja kielikohtaiset tekstit, käyttämällä ER-muodon [otsikoita](#AddMmLabels), kuten teit kielikohtaisten lausekkeiden osalta määritetyssä mallin yhdistämismäärityksessä. Tässä tapauksessa ER-etiketit on lisättävä muokattavaan ER-muotoon.

Kuten seuraavasta kuvasta näkyy, mukautetun raportin otsikko on määritetty, jotta Excel voi tehdä sivutustyön.

![Mukautetun raportin ylätunniste annetussa Excel-mallissa](./media/er-quick-start1-template-header.png)

## <a name="design-a-format"></a><a name="DesignFormat"></a>Muodon suunnittelu

Sähköisen raportoinnin toiminnallinen konsultti -roolin käyttäjänä sinun on luotava uusi ER-konfiguraatio, joka sisältää [muoto](general-electronic-reporting.md#FormatComponentOutbound)-komponentin. Muotokomponentti on konfiguroitava siten, että se määrittää, miten raporttimalli täytetään vaadituilla tiedoilla suorituksen aikana.

Kun [tuot suunnitellun mallinmääritys](#FormatImport) -osan vaiheet, voit tuoda vaaditun muodon mukana olevasta XML-tiedostosta. Voit myös suorittaa [uuden muodon määrityksen luomisen](#FormatCreate) vaiheet ja suunnitella tämän muodon alusta alkaen.

### <a name="import-a-designed-format-configuration"></a><a name="FormatImport"></a>Tuo suunniteltu muotokonfiguraatio

1. Lataa [kyselylomakkeiden muoto.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) -tiedosto ja tallenna se paikalliseen tietokoneeseen.
2. Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.
3. Valitse **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**.
4. Valitse toimintoruudussa **Vaihda** \> **Lataa XML-tiedostosta**.
5. Valitse **Selaa** ja etsi ja valitse **kyselylomakkeiden format.version.1.1.xml** -tiedosto.
6. Tuo konfigurointi valitsemalla **OK**.

Jos haluat jatkaa, ohita seuraavat vaiheet, [Luo uusi muotokonfiguraatio](#FormatCreate).

### <a name="create-a-new-format-configuration"></a><a name="FormatCreate"></a>Uuden muotokonfiguraation luominen
 
1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Konfiguraatiot**-sivun konfiguraatiopuun kohdasta **Kyselylomakemalli**.
3. Valitse **Luo konfiguraatio**.
4. Toimi avattavassa valintaikkunassa seuraavasti:

    1. Syötä **Uusi**-kenttään **Tietomallikyselylomakkeisiin perustuva muoto**.
    2. Kirjoita **Nimi**-kenttään **Kyselylomakkeen raportti**.
    3. Valitse **Tietomallin määritelmä** -kentässä **1**.

        > [!NOTE]
        > - Jos valitset perustietomallin jonkin tietyn version, tietomallin vastaavan version rakenne näytetään **Malli**-tietolähteen rakenteena luodussa muodossa.
        > - Kenttä voidaan jättää tyhjäksi. Tässä tapauksessa tietomallin **Luonnos**-version rakenne esitetään **Malli**-tietolähteen rakenteena luotavan mallin muodossa. Tämän jälkeen voit muokata malliasi ja nähdä nämä muutokset heti muodossa. Tämä lähestymistapa voi parantaa ER-ratkaisun suunnittelun tehokkuutta, kun määrität tietomallin, mallin yhdistämisen ja muodon samanaikaisesti.
        > - Jos valitset perustietomallin tietyn version, voit siirtyä käyttämään **Luonnos**-versiota myöhemmin, kun aloitat muodon muokkaamisen.

    4. **Valitse tietomallin määritys** -kentässä **Juuri**-määritys.

5. Valitse **Luo konfigurointi** luodaksesi konfiguroinnin.

#### <a name="import-a-report-template"></a><a name="ImportReportTemplate"></a>Tuo raporttimalli

1. Valitse **Konfiguraatiot**-sivun konfiguraatiopuun kohdasta **Kyselylomakeraportti**.
2. Aloita mukautetun muodon määrittäminen valitsemalla **suunnittelutoiminto**.
3. Valitse **Muodon suunnittelija** -sivulla hallintapaneelista **Tuo** \> **Tuo Excelistä**.
4. Toimi valintaikkunassa seuraavasti:

    1. Valitse **Lisää malli**.
    2. Etsi ja valitse paikallisesti tallennettu **Kyselylomakkeen raporttimalli.xslx** -tiedosto ja valitse sitten **Avaa**.
    3. Tuo malli valitsemalla **OK**.

    ![Raporttimallin tuominen](./media/er-quick-start1-template-import.png)

**Excel\\Tiedosto**-muotoelementti lisätään automaattisesti muokattavaan muotoon juurielementtinä. Lisäksi **Excel\\Alue**-muotoelementti tai **Excel\\Solu**-muotoelementti lisätään automaattisesti jokaista tunnistettua Excel-mallin nimeä varten. **Excel\\Otsikko**-muoto, joka sisältää sisäkkäisen **Merkkijono**- elementin, lisätään automaattisesti tuodun mallin otsikkoasetusten mukaiseksi.

![Muotorakenne, joka sisältää automaattisesti lisätyt elementit ER-toiminnon suunnittelussa](./media/er-quick-start1-template-import2.png)

#### <a name="configure-a-format"></a><a name="ConfigureFormat"></a>Muodon konfigurointi

1. Valitse **Muotoilun suunnittelu** -sivun muotoilupuusta **Excel**-juurielementti.
2. Kirjoita sivun oikeassa reunassa olevan **Muoto**-välilehden **Nimi**-kenttään <a name="AddFormatRootElement"></a>**Raportti**.
3. Valitse **Kieliasetus**-kentästä **käyttäjäasetus**, jos haluat suorittaa raportin käyttäjän ensisijaisella kielellä.
4. Valitse **Kulttuuriasetus**-kentästä **käyttäjäasetus**, jos haluat suorittaa raportin käyttäjän ensisijaisessa kulttuurissa.

    Lisätietoja ER-prosessin kieli- ja kulttuurikonteksteista on ohjeaiheessa [Monikielisten raporttien suunnitteleminen](er-design-multilingual-reports.md).

    ![Suunnitellun raportin kieli- ja kulttuuriasetusten määrittäminen ER-toiminnon suunnittelussa](./media/er-quick-start1-template-format-structure1.png)

5. Laajenna pääsolmu muotopuussa ja valitse sitten **ResultsGroup**.
6. Valitse **Muoto**-välilehden **Replikointisuunta** -kentästä **Ei replikaatiota**, koska yksittäiselle kyselylomakkeelle ei odoteta olevan useita tulosryhmiä.

    ![Aluemuotoelementtien replikointisuunnan määrittäminen ER-toiminnon suunnittelussa](./media/er-quick-start1-template-format-structure2.png)

7. Valitse **Tallenna**.

#### <a name="define-the-data-binding-for-a-report-title"></a><a name="DefineFormatBindings"></a>Raportin otsikon tietojen sidonnan määrittäminen

Sinun on määritettävä tietosidontamuoto elementille, jota käytetään luodun raportin otsikon täyttämiseen.

1. Valitse **Muodon suunnittelija** -sivun oikealta puolelta **Määritys**-välilehdeltä **Raportti\\ReportTitle**-elementti.
2. Valitse **Muokkaa kaavaa**.
3. Valitse kaavaeditorissa **Käännä**.
4. Toimi **Tekstin kääntäminen** -valintaikkunassa seuraavasti:

    1. Kirjoita **Etiketin tunnus**-kenttään **ReportTitle**.
    2. Kirjoita **Teksti oletuskielellä** -kenttään **Kyselylomakeraportti**.
    3. Valitse ensin **Käännä** ja sitten **Tallenna**.
    4. Valitse **Käännä**, jos haluat sulkea **Tekstin kääntäminen** -valintaikkunan.

5. Sulje kaavaeditori.

    ![Sidonnan määrittäminen täyttämään luodun raportin otsikko](./media/er-quick-start1-add-report-title-label.png)

Tämän tekniikan avulla voit tehdä kaikki muut nykyisen mallin kielikohtaiset otsikot. Lisätietoja yhden ER-kokoonpanon lisättyjen otsikoiden kääntämisestä kaikille tuetuille kielille on ohjeaiheessa [monikielisten raporttien suunnitteleminen](er-design-multilingual-reports.md).

#### <a name="review-model-data-source"></a><a name="ReviewModelDataSource"></a>Mallin tietolähteen tarkistaminen

1. Valitse **Muotoile suunnittelua** -sivun **Yhdistämismääritys**-välilehdessä <a name="ModelDSName"></a>**mallin** tietolähde, joka edustaa tämän ER-muodon perustietomallia.
2. Valitse **Muokkaa**.
3. Tarkista **tietolähteen ominaisuudet** -valintaikkunan tiedot. Tämä tietolähde edustaa **kyselylomakemallin** ER-määrityksissä sijaitsevan **kyselylomakkeen** tietomallikomponentin versiota 1.

![ER-toimintojen suunnitteluohjelman mallitietolähteen tiedot](./media/er-quick-start1-model-data-source.png)

#### <a name="bind-format-elements-to-data-source-fields"></a><a name="BindFormatElements"></a>Muotoelementtien sidonta tietolähdekenttiin

Jos haluat määrittää, miten malli täytetään suorituksen aikana, sinun on sidottava kaikki sopivaan Excel-nimeen liittyvät muotoiluelementit yhteen tämän muodon tietolähteen yksittäiseen kenttään.

1. Valitse **Muotoilun suunnittelu** -sivun muotoilupuusta **Raportti\\CompanyName**-muotoelementti.
2. Valitse **Yhdistämismääritys**-välilehdestä **model.CompanyName**-tietolähdekenttä **merkkijono**-tyypistä.
3. Määritä yrityksen nimi malliin valitsemalla **sido**.
4. Valitse muotopuusta **Raportti\\kyselylomake**-elementti.
5. Valitse **Yhdistämismääritys**-välilehdestä **model.Questionnaire**-tietolähdekenttä **Tietueluettelo**-tyypistä.
6. Valitse **Sido**.
7. Valitsemalla **Näytä tiedot** saat näkyviin lisätietoja muotoiluelementeistä.

    **Kyselylomakkeen** alueen muotoelementti määritetään pystysuunnassa replikoitavaksi. Kun **tietueluettelo**-tyypin tietolähteeseen on sidottu Excel-mallin asianmukainen **kyselylomake**-alue, se toistetaan sidotun tietolähteen jokaisen tietueen osalta.
 
    ![Kyselylomakkeen aluemuodon elementin sitominen asianmukaisiin tietueluettelon tietolähteisiin ER-toiminnon suunnittelussa](./media/er-quick-start1-bindings1.png)

    Koska Excel-mallin **kyselylomakkeen** alue on määritetty rivien 5-14 välillä, nämä rivit toistetaan aina raportoitua kyselylomaketta käyttäen.

    ![Excel-mallin rivit, jotka toistetaan muodostettuun raporttiin tietueluettelon tietolähteiden jokaisesta tietueesta](./media/er-quick-start1-template-questionnaire-range.png)

8. Määritä muiden muotoelementtien samanlaiset sidonnat seuraavassa taulukossa kuvatulla tavalla.

    > [!NOTE]
    > Tässä taulukossa "tietolähteen polku" -sarakkeen tiedoilla oletetaan, että [suhteellinen polun](relative-path-data-bindings-er-models-format.md) ER-toiminto on käytössä.

    | Muotoile elementin polku                                      | Tietolähteen polku |
    |----------------------------------------------------------|------------------|
    | Excel\\ReportTitle                                       | **\@"GER\_LABEL:ReportTitle"** |
    | Excel\\CompanyName                                       | **model.CompanyName** |
    | Excel\\Kyselylomake                                     | **model.Questionnaire** |
    | Excel\\Kyselylomake\\Aktiivinen                             | **\@.Active**, where **\@** is **model.Questionnaire** |
    | Excel\\Kyselylomake\\Koodi                               | **\@.Code** |
    | Excel\\Kyselylomake\\Kuvaus                        | **\@.Description** |
    | Excel\\Kyselylomake\\QuestionnaireType                  | **\@.QuestionnaireType** |
    | Excel\\Kyselylomake\\QuestionOrder                      | **\@.QuestionOrder** |
    | Excel\\Kyselylomake\\ResultsGroup\\Koodi\_               | **\@.ResultsGroup.Code** |
    | Excel\\Kyselylomake\\ResultsGroup\\Kuvaus\_        | **\@.ResultsGroup.Description** |
    | Excel\\Kyselylomake\\ResultsGroup\\MaxNumberOfPoints    | **\@.ResultsGroup.MaxNumberOfPoint** |
    | Excel\\Kyselylomake\\Kysymys                           | **\@.Question** |
    | Excel\\Kyselylomake\\Kysymys\\CollectionSequenceNumber | **\@.CollectionSequenceNumber**, where **\@** is **model.Questionnaire.Question** |
    | Excel\\Kyselylomake\\Kysymys\\Tunnus                       | **\@.Id** |
    | Excel\\Kyselylomake\\Kysymys\\MustBeCompleted          | **\@.MustBeCompleted** |
    | Excel\\Kyselylomake\\Kysymys\\PrimaryQuestion          | **\@.PrimaryQuestion** |
    | Excel\\Kyselylomake\\Kysymys\\SequenceNumber           | **\@.SequenceNumber** |
    | Excel\\Kyselylomake\\Kysymys\\Teksti                     | **\@.Text** |
    | Excel\\Kyselylomake\\Kysymys\\Vastaus                   | **\@.Answer** |
    | Excel\\Kyselylomake\\Kysymys\\Vastaus\\CorrectAnswer    | **\@.CorrectAnswer**, where **\@** is **model.Questionnaire.Answer** |
    | Excel\\Kyselylomake\\Kysymys\\Vastaus\\Pisteet           | **\@.Points** |
    | Excel\\Kyselylomake\\Kysymys\\Vastaus\\Teksti             | **\@.Text** |

9. Kun olet valmis, valitse **Tallenna**.

Seuraavassa kuvassa näkyy **muodon suunnittelu** -sivulla määritetyn tietojen sidonnan lopullinen tila.

![Konfiguroitu tietojen sidonnan ER-toiminnon suunnittelussa](./media/er-quick-start1-bindings2.png)

> [!IMPORTANT]
> Koko kokoelma määritettyjä tietolähteitä ja sidoksia edustaa määritetyssä muodossa olevaa muotomäärityskomponenttia. Tätä muotomääritystä kutsutaan, kun raportin luonnin konfiguroitu muoto suoritetaan.

### <a name="run-a-designed-format-from-er"></a><a name="RunFormatFromER"></a>Suunnitellun muodon suorittaminen ER-muodosta

Voit nyt suorittaa suunnitellun muodon testausta varten **kokoonpanot**-sivulta.

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Konfiguraatiot**-sivun konfiguraatiopuu vasemmasta ruudusta, laajenna **Kysymyslomakemalli** ja valitse sitten **Kysymyslomakeraportti**.
3. Valitse muotoiluversion **suunnitteluohjelma**, jonka tila on **luonnos**.
4. Vallitse **Muodon suunnittelu** -sivulla **Suorita**.
5. Määritä **ER-parametrit**-valintaikkunan **sisällytettävät rekisterit** -pikavälilehdessä suodatusvaihtoehto niin, että vain **SBCCrsExam**-kysely on mukana.
6. Vahvista suodatusvaihtoehto valitsemalla **OK**.
7. Suorita raportti valitsemalla **OK**.
8. Tarkista aikaansaatu raportti.

[Oletusarvon](electronic-reporting-destinations.md#default-behavior) mukaan luotu raportti toimitetaan Excel-tiedostona, jonka voit ladata. Seuraavissa kuvissa näkyy kaksi sivua luotua raporttia Excel-muodossa.

![Esimerkki luodusta raportista Excel-muodossa, sivu 1](./media/er-quick-start1-report1a.png)

![Esimerkki luodusta raportista Excel-muodossa, sivu 2](./media/er-quick-start1-report1b.png)

## <a name="tune-a-designed-format"></a><a name="TuneFormat"></a>Suunnitellun muodon säätäminen

### <a name="modify-a-format-to-change-the-name-of-a-generated-document"></a><a name="ModifyToChangeName"></a>Tiedostomuodon muokkaaminen luodun tiedoston nimen muuttamista varten

Oletusarvon mukaan luotu tiedosto nimetään nykyisen käyttäjän aliaksen avulla. Muokkaamalla muotoa voit muuttaa tätä toimintoa siten, että luotu tiedosto nimetään mukautetun logiikan mukaan. Esimerkiksi luodun tiedoston nimi voi perustua nykyiseen istunnon päivämäärään ja kellonaikaan sekä raportin otsikkoon.

1. Valitse **Muodon suunnittelu** -sivulla **Raportti**-juurinimike.
2. Valitse **yhdistämismääritys**-välilehdestä **Muokkaa tiedostonimeä**.
3. Kirjoita **kaava**-kenttään **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.
4. Valitse **Tallenna** ja sulje kaavaeditori.
5. Valitse **Tallenna**.

### <a name="modify-a-format-to-change-the-order-of-questions"></a><a name="ModifyToOrder"></a>Muodon muokkaaminen muuttamalla kysymysten järjestystä

Kysymyksiä ei ole tilattu oikein luotavalla raportilla. Voit muuttaa järjestystä muokkaamalla muotoa.

1. Valitse **Muodon suunnittelu** -sivulla **Raportti**-juurinimike.
2. Laajenna **Määritys**-välilehden muotopuussa **Raportti\\kyselylomake\\kysymys**.

    ![Aluetyypin kysymysmuotoelementti ER-operaation suunnittelijassa](./media/er-quick-start1-bindings3.png)

3. Valitse **Yhdistämismääritys**-välilehdestä **model.Questionnaire**.
4. Valitse **Lisää** \> **Funktiot\\laskettu kenttä** ja kirjoita sitten **nimi**-kenttään **OrderedQuestions**.
5. Valitse **Muokkaa kaavaa**.
6. Kirjoita kaavaeditorin **kaava**-kenttään **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** voidaksesi tilata nykyisen kyselylomakkeen kysymysluettelon järjestysnumeron mukaan.
7. Valitse **Tallenna** ja sulje kaavaeditori.
8. Viimeistele uuden lasketun kentän syöttö valitsemalla **OK**.
9. Valitse **Yhdistämismääritys**-välilehdestä **model.Questionnaire.OrderedQuestions**.
10. Valitse muotopuussa **Excel\\Kysymyslomake\\Kysymys**.
11. Valitse **sido** ja vahvista sitten, että käytössä oleva **model.Questionnaire.Questions**-polku korvataan uudella **model.Questionnaire.OrderedQuestions**-polulla kaikissa sisäkkäisten elementtien sidonnoissa.
12. Valitse **Tallenna**.

![Kysymysmuotoelementin sitominen määritettyyn OrderedQuestions-tietolähteeseen ER-toiminnon suunnittelussa](./media/er-quick-start1-bindings4.png)

### <a name="run-a-modified-format-from-er"></a><a name="RunFormatFromER2"></a>Muokatun muodon suorittaminen ER-muodosta

Voit nyt suorittaa muokatun muodon testaustarkoituksessa ER-kehyksestä.

1. Vallitse **Muodon suunnittelu** -sivulla **Suorita**.
2. Määritä **ER-parametrit**-valintaikkunan **sisällytettävät rekisterit** -pikavälilehdessä suodatusvaihtoehto niin, että vain **SBCCrsExam**-kysely on mukana.
3. Vahvista suodatusvaihtoehto valitsemalla **OK**.
4. Suorita raportti valitsemalla **OK**.
5. Tarkista aikaansaatu raportti.

Seuraavassa kuvassa näkyy Excel-muodossa luotu raportti, jossa kysymykset on järjestetty oikein.

![Luotu raportti Excel-muodossa, jossa on oikein tilatut kysymykset](./media/er-quick-start1-report2.png)

### <a name="complete-the-format-design"></a><a name="CompleteFormat"></a>Suunnittele muoto loppuun

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Konfiguraatiot**-sivun konfiguraatiopuu vasemmasta ruudusta, laajenna **Kysymyslomakemalli** ja valitse sitten **Kysymyslomakeraportti**.
3. Valitse **Versiot**-pikavälilehdessä konfiguraatioversio, jonka tila on **Luonnos**.
4. Valitse **Muutoksen tila** \> **Viimeistele**.

Tämän konfiguraation version 1.1 tila muutetaan **luonnoksesta** **valmiiksi**. Versiota 1.1 ei voi enää muuttaa. Tämä versio sisältää määritetyn muodon, ja sitä voidaan käyttää mukautetun raportin tulostamiseen. Tämän konfiguraation versio 1.2 luodaan, ja sen tila on **luonnos**. Voit muokata tätä versiota, jos haluat muuttaa **kyselylomake**-raporttisi muotoa.

![Konfiguraatiosivun muokattavan ER-konfiguraation versiot](./media/er-quick-start1-format-configuration.png)

> [!NOTE]
> Konfiguroitu muoto on **kyselylomake**-raportin rakenne, eikä se sisällä mitään suhteita rahoitukseen määritettyihin esineisiin.

## <a name="develop-application-artefacts-to-call-the-designed-report"></a><a name="DevelopCustomCode"></a>Sovelluksen artefaktien laatiminen suunniteltua raporttia varten

Järjestelmänvalvojan roolin käyttäjänä sinun on kehitettävä uusi logiikka niin, että konfiguroitu ER-muoto voidaan kutsua sovelluksen käyttöliittymästä (UI) mukautetun raportin luomista varten. Tällä hetkellä ER ei tarjoa mitään ominaisuuksia tämäntyyppisen logiikan määrittämiseen. Siksi tarvitaan joitakin teknisiä töitä. 

Uuden logiikan luontia varten käyttöön on otettava jatkuvaa koontia tukeva topologia. Lisätietoja on kohdassa [Jatkuvaa koonnin ja testauksen automaatiota tukevien topologioiden käyttöönotto](../perf-test/continuous-build-test-automation.md). Tarvitset myös tämän topologian kehitysympäristön käyttöoikeuden. Lisätietoja saatavilla olevista ER-ohjelmointirajapinnoista on kohdassa [ER-kehys-API](er-apis-app73.md).

### <a name="modify-source-code"></a><a name="ModifySourceCode"></a>Lähdekoodin muokkaaminen

#### <a name="add-a-data-contract-class"></a><a name="DataContractClass"></a>Tietosopimusluokan lisääminen

Lisää uusi **QuestionnairesErReportContract**-luokka Microsoft Visual Studio -projektiin ja kirjoita koodi, joka määrittää konfiguroitavan ER-muodon suorittamiseen käytettävän tietosopimuksen.

```xpp
/// <summary>
///     This class is the data contract class for the <c>QuestionnairesErReportDP</c> class.
/// </summary>
/// <remarks>
///    This is the data contract class for the Questionnaires ER report.
/// </remarks>
[
    DataContractAttribute,
    SysOperationContractProcessingAttribute(classStr(QuestionnairesErReportUIBuilder))
    ]
    public class QuestionnairesErReportContract extends ERFormatMappingRunBaseContract implements SysOperationValidatable
{
    ERFormatMappingId formatMapping;

    /// <summary>
    ///    Validates the report parameters.
    /// </summary>
    /// <returns>
    ///    true if no errors; otherwise, false.
    /// </returns>
    public boolean validate()
    {
        boolean ret = true;
        if (!formatMapping)
        {
            ret = checkFailed(strFmt("@SYS26332", new SysDictType(extendedTypeNum(ERFormatMappingId)).label()));
        }
        return ret;
    }
    [
        DataMemberAttribute('FormatMapping'),
        SysOperationLabelAttribute(literalstr("@ElectronicReporting:FormatMapping")),
        SysOperationHelpTextAttribute(literalstr("@ElectronicReporting:FormatMapping"))
    ]
    public ERFormatMappingId parmFormatMapping(ERFormatMappingId _formatMapping = formatMapping)
    {
        formatMapping = _formatMapping;
        return formatMapping;
    }
}
```

#### <a name="add-a-ui-builder-class"></a><a name="UIBuilderClass"></a>UI Builder -luokan lisääminen

Lisää uusi **QuestionnairesErReportUIBuilder**-luokka Visual Studio -projektiisi ja kirjoita koodi, kun haluat luoda suorituksenaikaisen valintaikkunan, jota käytetään suoritettavan ER-muodon määritystunnuksen hakemiseen. Annettu koodi hakee vain ER-muotoja, jotka sisältävät **[kyselylomakkeen](#DataModeName)** **tietomalliin** viittaavan tietolähteen **[juuri](#RootDefinitionName)**-määritystä käyttäen.

> [!NOTE]
> Vaihtoehtoisesti voit suodattaa ER-integrointipisteiden avulla ER-muotoja. Lisätietoja on kohdassa [API, joka näyttää muodon yhdistämishaun](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).

```xpp
/// <summary>
/// The UIBuilder class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportUIBuilder extends SysOperationAutomaticUIBuilder
{
    public const str ERQuestionnairesModel = 'Questionnaires';
    public const str ERQuestionnairesDataContainer = 'Root';

    /// <summary>
    /// Action after build of the dialog UI.
    /// </summary>
    public void postBuild()
    {
        DialogField formatMapping;
        super();
        formatMapping = this.bindInfo().getDialogField(this.dataContractObject(),
            methodStr(QuestionnairesErReportContract, parmFormatMapping));
        formatMapping.registerOverrideMethod(
            methodStr(FormReferenceControl, lookupReference),
            methodStr(QuestionnairesErReportUIBuilder, formatMappingLookup),
            this);
    }

    /// <summary>
    /// Performs the lookup form for format mapping.
    /// </summary>
    /// <param name="_referenceGroupControl">
    /// The control to perform lookup form.
    /// </param>
    public void formatMappingLookup(FormReferenceControl _referenceGroupControl)
    {
        ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(
            _referenceGroupControl,
            ERQuestionnairesModel,
            ERQuestionnairesDataContainer).performFormLookup();
    }
}
```

#### <a name="add-a-data-provider-class"></a><a name="DataProviderClass"></a>Tietopalveluluokan lisääminen

Lisää uusi **QuestionnairesErReportDP**-luokka Microsoft Visual Studio -projektiin ja kirjoita koodi, joka näyttää konfiguroitavan ER-muodon suorittamiseen käytettävän tietopalvelun. Annettu koodi sisältää vain tämän tietopalvelun tietosopimuksen.

```xpp
/// <summary>
/// Data provider class for Questionnaires ER report.
/// </summary>
public class QuestionnairesErReportDP
{
    QuestionnairesErReportContract contract;
    public static QuestionnairesErReportDP construct()
    {
        QuestionnairesErReportDP  dataProvider;
        dataProvider = new QuestionnairesErReportDP();
        return dataProvider;
    }
}
```

#### <a name="add-a-labels-file"></a><a name="LabelsFile"></a>Käyttöliittymätekstitiedoston lisääminen

Lisää uusi **QuestionnairesErReportLabels\_en-US** -tarratiedosto Visual Studio -projektiisi ja määritä seuraavat uusien käyttöliittymäresurssien otsikot:

- Uuden valikkovaihtoehdon **\@QuestionnairesReport**-otsikko, joka sisältää seuraavan tekstin Yhdysvalloissa (en-US): **kyselylomakeraportti (palvelun tarjoaa ER)**
- **\@QuestionnairesReportBatchJobDescription**-etiketti, jos valittu ER-muoto ajoitetaan suoritettavaksi erätyönä

#### <a name="add-a-report-service-class"></a><a name="ServiceClass"></a>Raporttipalveluluokan lisääminen

Lisää uusi **QuestionnairesErReportService**-luokka Visual Studio -projektiisi ja kirjoita koodi, joka kutsuu ER-muotoa, määrittää sen muodon yhdistämistunnuksen avulla ja antaa parametriksi tietosopimuksen.

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
/// <summary>
/// The electronic reporting service class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportService extends SysOperationServiceBase
{
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'Questionnaires report';
    public const str ParametersDataSourceName = 'RunTimeParameters';

    /// <summary>
    /// Generates report by using Electronic reporting framework
    /// </summary>
    /// <param name = "_contract">The Questionnaires report contract</param>
    public void generateReportByGER(QuestionnairesErReportContract _contract)
    {
        ERFormatMappingId formatMappingId;
        QuestionnairesErReportDP  dataProvider;
        dataProvider = QuestionnairesErReportDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        if (formatMappingId)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, ParametersDataSourceName, _contract, true));

                // Call ER to generate the report.
                ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                if (formatMappingRun.parmShowPromptDialog(true))
                {
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());
                    formatMappingRun.run();
                }
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

Jos sinun on käytettävä sovellustietoja suorittavaa ER-muotoa, sinun on konfiguroitava **tietomalli**-tyypin tietolähdemuodon yhdistämismääritys. Tämä tietolähde viittaa tiettyyn tietyn tietomallin osaan käyttämällä yksittäistä päämääritystä. Kun ER-muoto suoritetaan, se kutsuu tätä tietolähdettä käyttämään sopivaa ER-mallimääritystä, joka on määritetty tietylle mallille ja päämääritykselle.

Kaikki tiedot, jotka voit valmistella lähdekoodissa ja tallentaa osana tietosopimusta, voidaan siirtää käytössä olevaan ER-muotoon käyttämällä tämän tyyppisiä ER-mallimäärityksiä. ER-mallin yhdistämismäärityksessä on määritettävä **objekti**-tyypin tietolähde, joka viittaa **[QuestionnairesErReportContract](#DataContractClass)**-luokkaan. Voit määrittää mallimäärityksen määrittämällä tietolähteen, joka kutsuu tätä mallimääritystä. Tässä koodissa on **ERModelDataSourceName**-vakion määrittämä tietolähde, jolla on **[malli](#ModelDSName)**-arvo. Määritä tietolähteen nimi, kun haluat määrittää, mitä tietolähdettä käytetään, kun tietojen sopimus paljastetaan mallimäärityksessä. Tässä koodissa on **ParametersDataSourceName**-vakion määrittämä nimi, jolla on <a name="DataContractDSName"></a>**RunTimeParameters**-arvo.

> [!NOTE]
> Uudessa ympäristössä ER-metatiedot on ehkä päivitettävä, jotta tämäntyyppinen luokka on käytettävissä ER-mallin yhdistämismäärityksen suunnittelussa. Lisätietoja on kohdassa [Sähköisen raportoinnin (ER) kehyksen määrittäminen](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).

#### <a name="add-a-report-controller-class"></a><a name="ControllerClass"></a>Raportin ohjainluokan lisääminen

Lisää uusi **QuestionnairesErReportController**-luokka Visual Studio -projektiisi ja kirjoita koodi, joka suorittaa ER-muodon joko synkronisessa tilassa tai eräajona, kuten haluat, valintaikkunassa, joka perustuu annetun **QuestionnairesErReportUIBuilder**-luokan logiikkaan.

```xpp
/// <summary>
/// The controller for Questionnaires ER report
/// </summary>
class QuestionnairesErReportController extends ERFormatMappingRunBaseController
{
    /// <summary>
    /// The main entrance of the controller
    /// </summary>
    /// <param name = "args">The arguments</param>
    public static void main(Args args)
    {
        QuestionnairesErReportController operation;
        operation = new QuestionnairesErReportController(
            classStr(QuestionnairesErReportService),
            methodStr(QuestionnairesErReportService, generateReportByGER),
            SysOperationExecutionMode::Synchronous);
        operation.startOperation();
    }

    /// <summary>
    /// Gets caption of the dialog.
    /// </summary>
    /// <returns>Caption of the dialog</returns>
    public ClassDescription defaultCaption()
    {
        ClassDescription batchDescription;
        batchDescription = "Questionnaires report (powered by ER)";
        return batchDescription;
    }
}
```

#### <a name="add-a-menu-item"></a><a name="MenuItem"></a>Valikkovaihtoehdon lisääminen

Lisää uusi **QuestionnairesErRepor**-valikkovaihtoehto Visual Studio -projektiisi. Tämä valikkoaihe viittaa **Objekti**-ominaisuuden **QuestionnairesErReportController**-luokkaan, ja sen avulla määritetään käyttäjän oikeudet valita ja suorittaa ER-muoto. **Otsikko**-ominaisuudessa tämä valikkoaihe viittaa aiemmin luomaasi **\@QuestionnairesReport**-tarraan, joten oikea teksti esitetään sovelluksen käyttöliittymässä.

#### <a name="add-a-menu-item-to-a-menu"></a><a name="Menu"></a>Valikkovaihtoehdon lisääminen valikkoon

Lisää nykyinen **KM**-valikko Visual Studio -projektiisi. Tähän valikkoon on lisättävä uusi **QuestionnairesErReport**-nimikkeen **Tuloste**-tyyppi. Tämän kohteen täytyy viitata edellisessä osassa kuvattuun **QuestionnairesErReport**-valikkokohteeseen.

#### <a name="build-a-visual-studio-project"></a><a name="BuildVSProject"></a> Visual Studio -projektin luominen

Luo projekti, jotta uusi valikkovaihtoehto on käyttäjien käytettävissä.

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp"></a>Muodon suorittaminen sovelluksesta

1. Siirry kohtaan **kyselylomake** \> **Suunnittelu** \> **Kyselylomakeraportti (palvelun tarjoaa ER)**.

    ![Valitaan Kyselylomakeraportti (palvelun tarjoaa ER) -valikkokohta Kysely-moduulista määritetyn ER-muodon suorittamiseksi](./media/er-quick-start1-application-menu-modified.png)

2. Valitse valintaikkunan **muodon määritys** -kentästä **kyselylomakkeiden raportti**.
3. Valitse **OK**.
4. Määritä **Sähköisen raportoinnin parametrit**-valintaikkunan **sisällytettävät rekisterit** -pikavälilehdessä suodatusvaihtoehto niin, että vain **SBCCrsExam**-kysely on mukana.
5. Vahvista suodatusvaihtoehto valitsemalla **OK**.
6. Suorita raportti valitsemalla **OK**.

    ![Sähköinen raportti -dialogi-ikkunan valintaehtojen määrittäminen](./media/er-quick-start1-report-run-dialog-page.png)

7. Tarkista aikaansaatu raportti.

## <a name="tune-a-designed-er-solution"></a><a name="TuneSolution"></a>Suunnitellun ER-ratkaisun säätäminen

Voit muokata konfiguroitavaa ER-ratkaisua siten, että se käyttää kehittämääsi tietopalveluluokkaa, jonka avulla voit käyttää käytössä olevan ER-muodon tietoja, ja siten, että se syöttää tämän ER-muodon nimen luotuun raporttiin.

### <a name="modify-a-model-mapping"></a><a name="ModifyModelMapping"></a>Mallin yhdistämismäärityksen muokkaaminen

#### <a name="add-data-sources-to-access-a-data-contract-object"></a><a name="AddDataSource1"></a>Tietolähteiden lisääminen tietosopimusobjektien käyttämiseen

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Konfiguraatiot**-sivun konfiguraatiopuu vasemmasta ruudusta, laajenna **Kysymyslomakemalli** ja valitse sitten **Kysymyslomakkeen määritys**.
3. Valitse **Suunnittelija**, jos haluat avata **Malli tietolähteen määritys** -sivulle.
4. Valitse **Suunnittelija**, jos haluat avata valitun yhdistämismäärityksen mallikartoituksen suunnittelussa.
5. Valitse **Mallin määrityksen suunnittelu** -sivun **Tietolähdetyypit**-ruudusta **Dynamics 365 for Operations\\Objekti**.
6. Valitse **Tietolähteet**-ruudussa **Lisää juuri**.
7. Kirjoita valintaikkunan **Nimi**-kenttään **[RunTimeParameters](#DataContractDSName)**, joka on määritetty **QuestionnairesErReportService**-luokan lähdekoodissa.
8. Kirjoita **luokka**-kenttään **[QuestionnairesErReportContract](#DataContractClass)**, joka on koodattu aiemmin.
9. Valitse **OK**.
10. Laajenna **RunTimeParameters**.

Lisätty tietolähde antaa tietoja suoritettavan ER-muodon yhdistämismäärityksen tietuetunnuksesta.

![Lisätty tietolähde ER-mallin määrityssuunnittelijaan](./media/er-quick-start1-mapping3.png)

#### <a name="add-a-data-source-to-access-er-format-mapping-records"></a><a name="AddDataSource2"></a>Tietolähteen lisääminen ER-muotomääritystietueen käyttämiseen

Jatka valitun mallimäärityksen muokkaamista lisäämällä tietolähde, joka käyttää ER-muotomääritystietueita.

1. Valitse **Mallin määrityksen suunnittelu** -sivun **Tietolähdetyypit**-ruudusta **Dynamics 365 for Operations\\Taulukkotiedot**.
2. Valitse **Tietolähteet**-ruudussa **Lisää juuri**.
3. Kirjoita valintaikkunan **Nimi**-kentässä **ER1**.
4. Kirjoita **Taulu**-kenttään **ERFormatMappingTable**.
5. Valitse **OK**.

#### <a name="add-a-data-source-to-access-a-format-mapping-record-of-a-running-er-format"></a><a name="AddDataSource3"></a>Tietolähteen lisääminen käynnissä olevan ER-muodon muotomääritystietueen käyttämiseen

Jatka valitun mallimäärityksen muokkaamista lisäämällä tietolähde, joka käyttää käynnissä olevan ER-muodon muotomääritystietueita.

1. Valitse **Mallin määrityksen suunnittelu** -sivun **Tietolähdetyypit**-ruudusta **Toiminnot\\Laskettu kenttä**.
2. Valitse **Tietolähteet**-ruudussa **Lisää juuri**.
3. Kirjoita valintaikkunan **Nimi**-kentässä **ER2**.
4. Valitse **Muokkaa kaavaa**.
5. Kirjoita kaavaeditorin **kaava**-kenttään **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.
6. Valitse **Tallenna** ja sulje kaavaeditori.
7. Valitse **OK**.

#### <a name="enter-the-name-of-the-running-er-format-in-the-data-model"></a><a name="AddBinding"></a>Kirjoita suoritettavan ER-muodon nimi tietomalliin

Jatka valitun mallimäärityksen muokkaamista niin, että käytössä olevan ER-muodon nimi kirjoitetaan tietomalliin.

1. Laajenna **Mallin määrityksen suunnittelu** -sivun **Tietomalli**-ruudusta **ExecutionContext** ja valitse sitten **ExecutionContext\\FormatName**.
2. Määritä tietojen sidonta valitun tietomallin kenttää varten valitsemalla **Tietomalli**-ruudussa **Muokkaa**.
3. Kirjoita kaavaeditorin **Kaava**-kenttään **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.
4. Valitse **Tallenna** ja sulje kaavaeditori.

Koska olet käyttänyt **FormatName**-kenttää, konfiguroitu mallikartoitus paljastaa nyt sellaisen ER-muodon nimen, joka kutsuu tätä mallimääritystä suorituksen aikana.

![Tietomallikentän sitominen ER-mallikartoituksen suunnittelutoimintoon lisätyn tietolähteen tapaan](./media/er-quick-start1-mapping4.png)

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping2"></a>Mallin määrityksen rakenteen täydentäminen

1. Valitse **Mallimäärityssuunnittelu**-sivulla **Tallenna**.
2. Sulje sivu.
3. Sulje mallimääritykset-sivu.
4. Varmista, että **kyselylomakkeen yhdistämis**-määritys on edelleen valittuna **konfiguraatiot**-sivun konfiguraatiopuussa. Valitse sitten **Versiot**-pikavälilehdessä konfiguraatioversio, jonka tila on **Luonnos**.
5. Valitse **Muutoksen tila** \> **Viimeistele**.

Tämän konfiguraation version 1.2 tila muutetaan **luonnoksesta** **valmiiksi**. Versiota 1.2 ei voi enää muuttaa. Tämä versio sisältää konfiguroidun mallin määrityksen, ja sitä voidaan käyttää muiden ER-konfiguraatioiden pohjana. Tämän konfiguraation versio 1.3 luodaan, ja sen tila on **luonnos**. Voit muokata tätä versiota, jos haluat muuttaa **kyselylomakkeen** mallimääritystä.

### <a name="modify-a-format"></a><a name="ModifyFormat"></a>Muodon muokkaaminen

Voit muokata konfiguroitavan ER-muotoa niin, että sen nimi näkyy sen raportin alatunnisteessa, joka luodaan, kun ER-muoto suoritetaan.

#### <a name="add-a-new-format-element"></a><a name="AddFormatElement"></a>Lisää uusi muotoelementti

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Konfiguraatiot**-sivun konfiguraatiopuu vasemmasta ruudusta, laajenna **Kysymyslomakemalli** ja valitse sitten **Kysymyslomakeraportti**.
3. Valitse **Suunnittelu**.
4. Valitse **Muodon suunnittelu** -sivulla **Raportti**-juurinimike.
5. Valitse **Lisää**, jos haluat lisätä uuden sisäkkäisen muodon elementin valitulle **raportin** juurikohteelle.
6. Valitse **Excel\\alatunniste**.
7. Kirjoita **Nimi**-kenttään **Alatunniste**.
8. Valitse **Raportti/Alatunniste** ja valitse sitten **Lisää**.
9. Valitse **Teksti\\Merkkijono**.

#### <a name="bind-the-added-format-element"></a><a name="BindAddedFormatElement"></a>Sido lisätty muotoelementti

1. Valitse **Muodon suunnittelija** -sivun **Määritys**-välilehden muotopuussa aktiivisessa **Alatunniste\\Merkkijono**-elementissä **Muokkaa kaavaa**.
2. Kirjoita kaavaeditorissa **kaava**-kenttään **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**.
3. Valitse **Tallenna** ja sulje kaavaeditori.
4. Valitse **Tallenna**.

Konfiguroitumuoto on muokattu siten, että sen nimi lisätään luodun raportin alatunnisteeseen käyttämällä **Alatunniste\\Merkkijono**-elementtiä.

![Alatunnisteen muotoiluelementin lisääminen määritettyyn muotoon ER-toiminnon suunnittelussa](./media/er-quick-start1-template-format-structure3.png)

#### <a name="complete-the-format-design"></a><a name="CompleteFormat2"></a>Suunnittele muoto loppuun

1. Sulje **Muodon suunnittelija** -sivu.
2. Varmista, että **kyselylomakkeen raportti**-määritys on edelleen valittuna **konfiguraatiot**-sivun konfiguraatiopuussa. Valitse sitten **Versiot**-pikavälilehdessä konfiguraatioversio, jonka tila on **Luonnos**.
3. Valitse **Muutoksen tila** \> **Viimeistele**.

Tämän konfiguraation version 1.2 tila muutetaan **luonnoksesta** **valmiiksi**. Versiota 1.2 ei voi enää muuttaa. Tämä versio sisältää konfiguroidun muodon, ja sitä voidaan käyttää muiden ER-konfiguraatioiden pohjana. Tämän konfiguraation versio 1.3 luodaan, ja sen tila on **luonnos**. Voit muokata tätä versiota, jos haluat muuttaa **kyselylomakkeen** raporttia.

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp2"></a>Muodon suorittaminen sovelluksesta

1. Siirry kohtaan **kyselylomake** \> **Suunnittelu** \> **Kyselylomakeraportti (palvelun tarjoaa ER)**.
2. Valitse valintaikkunan **muodon määritys** -kentästä **kyselylomakkeiden raportti**.
3. Valitse **OK**.
4. Määritä **ER-parametrit**-valintaikkunan **sisällytettävät rekisterit** -pikavälilehdessä suodatusvaihtoehto niin, että vain **SBCCrsExam**-kysely on mukana.
5. Vahvista suodatusvaihtoehto valitsemalla **OK**.
6. Suorita raportti valitsemalla **OK**.
7. Tarkista luotu raportti Excel-muodossa.

Huomaa, että luodun raportin alatunniste sisältää sen luonnissa käytetyn ER-muodon nimen.

![Luotu raportti Excel-muodossa](./media/er-quick-start1-report4.png)

### <a name="run-a-format-from-er"></a><a name="RunFormatFromER3"></a>Muodon suorittaminen ER-muodosta

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Konfiguraatiot**-sivun konfiguraatiopuu vasemmasta ruudusta, laajenna **Kysymyslomakemalli** ja valitse sitten **Kysymyslomakeraportti**.
3. Valitse toimintoruudussa **Suorita**.
4. Määritä **Sähköisen raportoinnin parametrit**-valintaikkunan **sisällytettävät rekisterit** -pikavälilehdessä suodatusvaihtoehto niin, että vain **SBCCrsExam**-kysely on mukana.
5. Vahvista suodatusvaihtoehto valitsemalla **OK**.
6. Suorita raportti valitsemalla **OK**.
7. Tarkista luotu raportti Excel-muodossa.

Huomaa, että luodun raportin alatunniste ei sisällä sen luonnissa käytetyn ER-muodon nimeä, koska tietosopimusobjekti ei siirtynyt käynnissä olevaan mallimääritykseen, kun ER-muodossa suoritettava ER-muoto kutsui sitä.

### <a name="configure-a-format-destination-for-on-screen-preview"></a><a name="ConfigureDestination"></a>Muotokohteen määrittäminen näytön esikatselua varten

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Sähköisen raportoinnin kohde**.
2. Lisää **Sähköisen raportoinnin kohde** -sivulla kohdetietue konfiguroidulle **kyselylomakeraportin** ER-muodolle.
3. Määritä **Tiedoston kohde** -pikavälilehdessä sen **raportti**-muotokomponentin **näyttö-** [kohde](er-destination-type-screen.md), joka on [lisätty](#AddFormatRootElement) määritetyn **kyselylomakeraportin** ER-muodon juurielementiksi.
4. Määritä **PDF-muuntoasetukset**-pikavälilehdessä kohde, joka muuntaa raportin [PDF-muotoon](electronic-reporting-destinations.md#OutputConversionToPDF), joka käyttää **vaakasuuntaista** sivun suuntaa.

![Mukautetun näyttökohteen määrittäminen ER-muodossa sähköisen raportoinnin kohdesivulla](./media/er-quick-start1-destination.png)

### <a name="run-a-format-from-the-application-to-preview-it-as-a-pdf-document"></a><a name="RunFormatFromApp3"></a>Voit esikatsella sitä PDF-tiedostona suorittamalla sovelluksen muodon

1. Siirry kohtaan **kyselylomake** \> **Suunnittelu** \> **Kyselylomakeraportti (palvelun tarjoaa ER)**.
2. Valitse valintaikkunan **muodon määritys** -kentästä **kyselylomakkeiden raportti**.
3. Valitse **OK**.
4. Määritä **Sähköisen raportoinnin parametrit**-valintaikkunan **sisällytettävät rekisterit** -pikavälilehdessä suodatusvaihtoehto niin, että vain **SBCCrsExam**-kysely on mukana.
5. Vahvista suodatusvaihtoehto valitsemalla **OK**.

    Huomaa, että **Kohteet**-pikavälilehden **tuloste**-kentän arvoksi on määritetty **Näyttö**. Jos haluat muuttaa konfiguroituja kohteita, valitse **Muuta**.

    ![ER-raportin suorituksenaikainen valintaikkuna, jossa voit muuttaa konfiguroidun kohteen](./media/er-quick-start1-run-settings.png)

6. Suorita raportti valitsemalla **OK**.
7. Tarkista luotu raportti PDF-muodossa.

    ![Luodun raportin esikatselu näytöllä PDF-muodossa](./media/er-quick-start1-preview-PDF.png)

## <a name="additional-resources"></a><a name="References"></a>Lisäresurssit

- [Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)
- [Sähköisen raportoinnin kaavakieli](er-formula-language.md)
- [Monikielisten raporttien suunnitteleminen](er-design-multilingual-reports.md)
- [Sähköisen raportoinnin kehyksen ohjelmointirajapinta](er-apis-app73.md)
- [CASE-funktio](er-functions-logical-case.md)
- [CONCATENATE-funktio](er-functions-text-concatenate.md)
- [DATETIMEFORMAT-funktio](er-functions-datetime-datetimeformat.md)
- [FILTER-funktio](er-functions-list-filter.md)
- [FIRSTORNULL-funktio](er-functions-list-firstornull.md)
- [FORMAT-funktio](er-functions-text-format.md)
- [IF-funktio](er-functions-logical-if.md)
- [ORDERBY-funktio](er-functions-list-orderby.md)
- [SESSIONNOW-funktio](er-functions-datetime-sessionnow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]