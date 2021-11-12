---
title: Ota reunapalvelujen scale unitit käyttöön mukautetussa laitteistossa LBD:n avulla (esikatselu)
description: Tässä ohjeaiheessa kerrotaan, paikallisia reunapalvelujen scale uniteja valmistellaan käyttämällä mukautettua laitteistoa ja käyttöönottoa, joka perustuu paikallisiin liiketoimintatietoihin.
author: cabeln
ms.date: 04/22/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0ebbdaab9d6f040497d3158db2712e102b6e9aa8
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678978"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd-preview"></a>Ota reunapalvelujen scale unitit käyttöön mukautetussa laitteistossa LBD:n avulla (esikatselu)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)] <!--KFM: Until 11/1/2021 -->

Reunan asteen yksiköillä on tärkeä rooli toimitusketjun hallinnan hajautetussa hybriditopologiassa. Hybriditopologiassa voit jakaa työkuormia Supply Chain Management -pilvikeskuksen ja ylimääräisten scale unitien välillä pilvessä tai reunalla.

Reunapalvelujen scale unitit voidaan ottaa käyttöön luomalla paikallisen yritystiedon (LBD) [paikallinen ympäristö](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) ja määrittämällä se sitten toimimaan scale unitina toimitusketjun hallinnan hajautetussa hybriditopologiassa. Tämä saavutetaan yhdistämällä paikallinen LBD-ympäristö pilvessä toimivaan Supply Chain Management -ympäristöön, joka on määritetty toimimaan keskuksena.  

Reunapalvelujen scale unitit ovat parhaillaan esikatselussa. Tämän vuoksi voit käyttää tällaista ympäristöä vain [esikatseluehtojen](https://aka.ms/scmcnepreviewterms) mukaisesti.

Tässä aiheessa kuvataan, miten paikallinen LBD-ympäristö määritetään reunapalvelujen scale unitiksi ja yhdistetään sitten keskukseen.

## <a name="deployment-overview"></a>Käyttöönoton yleiskatsaus

Tässä on käyttöönottovaiheiden yleiskatsaus.

1. **Ota LBD-paikka käyttöön Microsoft Dynamics Lifecycle Servicesin (LCS) LBD-projektissa.**

    Esikatselussa LBD:n reunapalvelujen scale unitit kohdistuvat olemassa oleviin LBD-asiakkaisiin. Lisäksi 60 päivän rajoitettu LBD-eristyspaikka tarjotaan vain tietyissä asiakastilanteissa.

1. **Määritä ja ota käyttöön LBD-ympäristö *tyhjällä* tietokannalla.**

    Käytä LCS:ää LBD-ympäristön käyttöönottoon viimeisimmällä topologialla ja tyhjällä tietokannalla. Lisätietoja on myöhemmin tämän aiheen kohdassa [LBD-ympäristön määritys ja käyttöönotto tyhjällä tietokannalla](#set-up-deploy). Sinun on käytettävä Supply Chain Managementin versiota 10.0.19, jossa on vähintään platform update 43 keskus- ja scale unit -ympäristöissä.

1. **Lataa kohdepaketit LCS:n LBD-projektiresursseihin**

    Valmistele sovellus-, ympäristö- ja mukautuspaketit, joita käytät keskuksessa ja reunapalvelujen scale unitissa. Lisätietoja on myöhemmin tämän aiheen osassa [Kohdepakettien lataaminen LBD-projektiresursseihin LCS:ssä](#upload-packages).

1. **Anna kohdepaketit LBD-ympäristön käyttöön.**

    Tällä vaiheella varmistetaan, että sama koontiversio ja samat mukautukset otetaan käyttöön keskuksessa ja sijainnissa. Lisätietoja on myöhemmin tämän aiheen osassa [Anna kohdepaketit LBD-ympäristön käyttöön](#service-target-packages).

1. **Suorita scale unitin määritys ja työkuorman kohdistus.**

    Lisätietoja on myöhemmin tämän aiheen osassa [Kohdista LBD:n reunapalvelujen scale unit keskukseen](#assign-edge-to-hub).

Loput tämän ohjeaiheen osat sisältävät tarkempia tietoja näiden vaiheiden suorittamisesta.

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>Määritä ja ota käyttöön LBD-ympäristö tyhjällä tietokannalla

Tämä vaihe luo toimivan LBD-ympäristön. Ympäristöllä ei kuitenkaan välttämättä ole samoja sovellusten ja ympäristöjen versioita kuin keskusympäristöllä. Lisäksi siitä puuttuvat vielä mukautukset, eikä sitä ole vielä määritetty toimimaan scale unitina.

1. Noudata kohdan [Paikallisten ympäristöjen määrittäminen ja käyttöönotto (Platform update 41 ja uudemmat)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md) ohjeita. Sinun on käytettävä Supply Chain Managementin versiota 10.0.19, jossa on vähintään ympäristöpäivitys 43 keskus- ja scale unit -ympäristöissä

    > [!IMPORTANT]
    > Lue tämän osan loppuosa, **ennen** kuin suoritat kyseisen aiheen vaiheet.

1. Suorita seuraava komentosarja, ennen kuin kuvaat määrityksesi tiedostossa infrastructure\\ConfigTemplate.xml:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Tämä komentosarja poistaa kaikki määritykset, joita ei tarvita reunapalvelujen scale unitien käyttöönotossa.

1. Määritä tyhjiä tietoja sisältävä tietokanta kohdassa [Tietokantojen määritys](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) kuvatulla tavalla. Käytä tässä vaiheessa tyhjää data.bak-tiedostoa.
1. Määritä käyttöönottoa edeltävä komentosarja. Lisätietoja: [Paikallisen edustajan ennen käyttöönottoa ja sen jälkeen suoritettavat komentosarjat](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md).

    1. Kopioi **ScaleUnit**-kansio kohdasta **Infrastruktuurikomentosarjat** **Komentosarjat**-kansioon edustajatiedostojen jaettuun tallennustilaan, joka on märitetty ympäristössä. Tyypillinen polku on \\\\lbdiscsi01\\edustaja\\Komentosarjat.
    2. Luo komentosarja **PreDeployment.ps1**, joka käynnistää komentosarjat käyttäen tarvittavia parametreja. Käyttöönottoa edeltävä komentosarja on sijoitettava edustajatiedostojen jaetun tallennustilan **Komentosarjat**-kansioon. Muuten sitä ei voi suorttaa. Tyypillinen polku on \\\\lbdiscsi01\\edustaja\\Komentosarjat\\PreDeployment.ps1.

        PreDeployment.ps1-komentosarjan sisältö muistuttaa seuraavaa esimerkkiä.

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        & $agentShare\Scripts\Configure-CloudandEdge.ps1 -AgentShare $agentShare -InstanceId '@A' -DatabaseServer 'lbdsqla01.contoso.com' -DatabaseName 'AXDB'
        ```

        > [!NOTE]
        > InstanceId-parametrissa saa olla vain kaksi merkkiä. Ensimmäinen merkki on @ ja toinen voi olla mikä tahansa englanninkielisten aakkosten iso kirjain.
        >
        > - Kelvolliset arvot:
        >   - @D
        >   - @X
        > - Kelvottomat arvot:
        >   - @a
        >   - @4
        >   - @#

1. Ota ympäristö käyttöön käyttäen uusinta käytettävissä olevaa perustopologiaa.

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>Lataa kohdepaketit LCS:n LBD-projektiresursseihin

Tässä vaiheessa valmistellaan sovellusversio, ympäristöversio ja mukautukset, jotka siirretään LBD:n scale unit -ympäristöön.

1. Lataa sama yhdistetty sovellus-/ympäristöpaketti, jota käytettiin keskusympäristöön LCS:n paikallisen projektin resurssikirjastossa.
1. Nouda kopio mukautetusta käyttöönotettavasta paketista, jota käytettiin keskusympäristöön, ja lataa se LCS:n paikallisen projektin resurssikirjastoon.

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>Anna kohdepaketit LBD-ympäristön käyttöön.

Tässä vaiheessa täsmäytetään LBD:n scale unit -ympäristön sovellusversio, ympäristöversio ja mukautukset keskuksen kanssa.

1. Anna LBD-ympäristön käyttöön yhdistetty sovellus-/ympäristöpaketti, jonka latasit edellisessä vaiheessa.
1. Anna LBD-ympäristön käyttöön mukautettu käyttöönotettava paketti, jonka latasit edellisessä vaiheessa.

    ![Toiminnon Ylläpidä > Ota päivitykset käyttöön LCS:ssä valitseminen.](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "Toiminnon Ylläpidä > Ota päivitykset käyttöön LCS:ssä valitseminen")

    ![Mukautuspaketin valitseminen.](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "Mukautuspaketin valitseminen")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>Kohdista LBD:n reunapalvelujen scale unit keskukseen

Kun reunapalvelujen scale unitit ovat edelleen esikatselussa, LBD:n reunapalvelujen scale unitin keskukseen kohdistamisessa on käytettävä GitHubissa käytettävissä olevia [scale unitien käyttöönotto- ja määritystyökaluja](https://github.com/microsoft/SCMScaleUnitDevTools). Tämän prosessin ansiosta LBD-määritys voi toimia reunapalvelujen scale unitina, ja se kohdistaa sen keskukseen. Prosessi muistuttaa yhden ruudun kehitysympäristön määrittämistä.

1. Lataa [SCMScaleUnitDevTools](https://github.com/microsoft/SCMScaleUnitDevTools/releases)-tiedoston viimeisin versio ja pura sen sisältö.
1. Luo kopio tiedostosta `UserConfig.sample.xml` ja anna sille nimeksi `UserConfig.xml`.
1. Luo Microsoft Azure Active Directory (Azure AD) -sovellus Azure AD -vuokraajassasi [Scale unitien ja työkuormien käyttöönotto-opas](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#aad-application-registrations) -oppaassa esitetyllä tavalla.
    1. Kun olet luonut sen, siirry keskuksen Azure AD -sovelluslomakkeeseen (SysAADClientTable).
    1. Luo uusi merkintä ja määritä luomasi sovelluksen tunnus **Asiakastunnus**-tunnukseksi. Määritä **Nimi**-kohdan arvoksi *ScaleUnits* ja **Käyttäjätunnus**-kohdan arvoksi *Järjestelmänvalvoja*.

1. Luo Active Directory -liittoutumispalvelut (AD FS) -sovellus oppaassa [Scale unitien ja työkuormien käyttöönotto-opas](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#adfs-application-registrations) esitetyllä tavalla.
    1. Kun olet luonut sen, siirry reunapalvelujen scale unitin Azure AD -sovelluslomakkeeseen (SysAADClientTable).
    1. Luo uusi merkintä ja määritä luomasi sovelluksen tunnus **Asiakastunnus**-tunnukseksi. Määritä kohdan **Käyttäjätunnus** arvoksi *Järjestelmänvalvoja*.

1. Muokkaa `UserConfig.xml`-tiedostoa.
    1. Syötä `InterAOSAADConfiguration`-osaan aiemmin luomasi Azure AD -sovelluksen tiedot.
        - Syötä `AppId`-elementtiin Azure-sovelluksen sovellustunnus.
        - Syötä `AppSecret`-elementtiin Azure-sovelluksen salainen koodi.
        - `Authority`-elementin on sisällettävä URL-osoite, joka määrittää vuokraajan suojausviranomaisen.

        ```xml
        <InterAOSAADConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopty56TGUedDTVhtER-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </InterAOSAADConfiguration>
        ```

    1. Muokkaa `ScaleUnitConfiguration`-osassa ensimmäisen `ScaleUnitInstance`-esiintymän `AuthConfiguration`-osaa.
        - Syötä `AppId`-elementtiin Azure-sovelluksen sovellustunnus.
        - Syötä `AppSecret`-elementtiin Azure-sovelluksen salainen koodi.
        - `Authority`-elementin on sisällettävä URL-osoite, joka määrittää vuokraajan suojausviranomaisen.

        ```xml
        <AuthConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopdz.6d3DTVOtf9Lo-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </AuthConfiguration>
        ```

    1. Määritä lisäksi tälle samalle `ScaleUnitInstance`-esiintymälle seuraavat arvot:
        - Määritä `Domain`-elementissä keskuksesi URL-osoite. Esimerkki: `https://cloudhub.sandbox.operations.dynamics.com/`
        - Varmista `EnvironmentType`-elementissä, että arvo `LCSHosted`on määritetty.

    1. Muokkaa `ScaleUnitConfiguration`-osassa toisen `ScaleUnitInstance`-esiintymän `AuthConfiguration`-osaa.
        - Syötä `AppId`-elementtiin AD FS -sovelluksen sovellustunnus.
        - Syötä `AppSecret`-elementtiin AD FS -sovelluksen salainen koodi.
        - `Authority`-elementin on sisällettävä AD FS -esiintymän URL-osoite.

        ```xml
        <AuthConfiguration>
            <AppId>26b16f25-21d8-4d36-987b-62df292895aa</AppId>
            <AppSecret>iZFfObgI6lLtY9kEbBjEFV98NqI5_YZ0e5SBcWER</AppSecret>
            <Authority>https://adfs.contoso.com/adfs</Authority>
        </AuthConfiguration>
        ```

    1. Määritä lisäksi tälle samalle `ScaleUnitInstance`-esiintymälle seuraavat arvot:
        - Määritä `Domain`-elementissä reunapalvelujen scale unitin URL-osoite. Esimerkki: https://ax.contoso.com/
        - Varmista `EnvironmentType`-elementissä, että arvo LDB on määritetty.
        - Syötä `ScaleUnitId`-elementtiin sama arvo, jonka määritit `InstanceId`-tunnukseksi, kun määritit käyttöönottoa edeltävän `Configure-CloudandEdge.ps1`-komentosarjan.

        > [!NOTE]
        > Jos et käytä oletustunnusta (@A), varmista, että päivität Työkuormat-osan jokaisen ConfiguredWorkload-työkuorman ScaleUnitId-tunnuksen.

1. Avaa PowerShell ja siirry `UserConfig.xml`-tiedoston sisältävään kansioon.

1. Suorita työkalu tällä komennolla.

    ```powershell
    .\CLI.exe
    ```

    > [!NOTE]
    > Työkalu on käynnistettävä uudelleen jokaisen toiminnon jälkeen.

1. Valitse työkalussa **2. Valmistele ympäristöt työkuorman asennusta varten**. Suorita sitten seuraavat vaiheet:
    1. Valitse **1. Valmistele keskus**.
    1. Valitse **2. Valmistele scale unit**.

    > [!NOTE]
    > Jos et suorita tätä komentoa puhtaasta asennuksesta ja se epäonnistuu, toimi seuraavasti:
    >
    > - Poista kaikki kansiot `aos-storage`-kansiosta (ei `GACAssemblies`-kansiota).
    > - Suorita seuraava SQL-komento yritystietokannassasi (AXDB):
    >
    > ```sql 
    > delete from storagefoler
    > ```

1. Suorita seuraava SQL-komennot yritystietokannassasi (AXDB):

    ```sql
    delete from FEATUREMANAGEMENTMETADATA
    delete from FEATUREMANAGEMENTSTATE
    delete from NUMBERSEQUENCESCOPE
    ```

1. Tarkista, että muutoksen seuranta on otettu käyttöön yritystietokannassa (AXDB)
    1. Käynnistä SQL Server Management Studio (SSMS).
    1. Napsauta yritystietokantaa (AXDB) hiiren kakkospainikkeella ja valitse ominaisuudet.
    1. Valitse avautuvassa ikkunassa **Muutosten seuranta** -vaihtoehto ja määritä seuraavat asetukset:

        - **Muutosten seuranta:** *Tosi*
        - **Säilytysaika:** *7*
        - **Säilytyksen yksiköt:** *Päivää*
        - **Automaattinen puhdistus:** *Tosi*

1. Valitse työkalussa **3. Asenna työkuormat**. Suorita sitten seuraavat vaiheet:
    1. Valitse **1. Asenna keskuksessa**.
    1. Valitse **2. Asenna scale unitissa**.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
