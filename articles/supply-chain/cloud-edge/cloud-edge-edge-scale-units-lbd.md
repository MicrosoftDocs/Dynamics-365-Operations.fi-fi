---
title: Ota reunan asteikon yksiköt käyttöön mukautetussa laitteistossa LBD:n avulla
description: Tässä ohjeaiheessa kerrotaan, paikallisia reunapalvelujen scale uniteja valmistellaan käyttämällä mukautettua laitteistoa ja käyttöönottoa, joka perustuu paikallisiin liiketoimintatietoihin.
author: cabeln
ms.date: 11/29/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 2407d4e3c6adaf5df2e8f5440ee8336f86012caf
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920670"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd"></a>Ota reunan asteikon yksiköt käyttöön mukautetussa laitteistossa LBD:n avulla

[!include [banner](../includes/banner.md)]

Reunan asteen yksiköillä on tärkeä rooli toimitusketjun hallinnan hajautetussa hybriditopologiassa. Hybriditopologiassa voit jakaa työkuormia Supply Chain Management -pilvikeskuksen ja ylimääräisten scale unitien välillä pilvessä tai reunalla.

Reunapalvelujen scale unitit voidaan ottaa käyttöön luomalla paikallisen yritystiedon (LBD) [paikallinen ympäristö](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) ja määrittämällä se sitten toimimaan scale unitina toimitusketjun hallinnan hajautetussa hybriditopologiassa. Tämä saavutetaan yhdistämällä paikallinen LBD-ympäristö pilvessä toimivaan Supply Chain Management -ympäristöön, joka on määritetty toimimaan keskuksena.  

Tässä aiheessa kuvataan, miten paikallinen LBD-ympäristö määritetään reunapalvelujen scale unitiksi ja yhdistetään sitten keskukseen.

## <a name="deployment-overview"></a>Käyttöönoton yleiskatsaus

Tässä on käyttöönottovaiheiden yleiskatsaus.

1. **Ota LBD-paikka käyttöön Microsoft Dynamics Lifecycle Servicesin (LCS) LBD-projektissa.**

1. **Määritä ja ota käyttöön LBD-ympäristö *tyhjällä* tietokannalla.**

    Käytä LCS:ää LBD-ympäristön käyttöönottoon viimeisimmällä topologialla ja tyhjällä tietokannalla. Lisätietoja on myöhemmin tämän aiheen kohdassa [LBD-ympäristön määritys ja käyttöönotto tyhjällä tietokannalla](#set-up-deploy). Keskus- ja scale unit -ympäristössä on käytettävä vähintään Supply Chain Managementin versiota 10.0.21.

1. **Lataa kohdepaketit LCS:n LBD-projektiresursseihin**

    Valmistele sovellus-, ympäristö- ja mukautuspaketit, joita käytät keskuksessa ja reunapalvelujen scale unitissa. Lisätietoja on myöhemmin tämän aiheen osassa [Kohdepakettien lataaminen LBD-projektiresursseihin LCS:ssä](#upload-packages).

1. **Anna kohdepaketit LBD-ympäristön käyttöön.**

    Tällä vaiheella varmistetaan, että sama koontiversio ja samat mukautukset otetaan käyttöön keskuksessa ja sijainnissa. Lisätietoja on myöhemmin tämän aiheen osassa [Anna kohdepaketit LBD-ympäristön käyttöön](#service-target-packages).

1. **Suorita scale unitin määritys ja työkuorman kohdistus.**

    Lisätietoja on myöhemmin tämän aiheen osassa [Kohdista LBD:n reunapalvelujen scale unit keskukseen](#assign-edge-to-hub).

Loput tämän ohjeaiheen osat sisältävät tarkempia tietoja näiden vaiheiden suorittamisesta.

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>Määritä ja ota käyttöön LBD-ympäristö tyhjällä tietokannalla

Tämä vaihe luo toimivan LBD-ympäristön. Ympäristöllä ei kuitenkaan välttämättä ole samoja sovellusten ja ympäristöjen versioita kuin keskusympäristöllä. Lisäksi siitä puuttuvat vielä mukautukset, eikä sitä ole vielä määritetty toimimaan scale unitina.

1. Noudata kohdan [Paikallisten ympäristöjen määrittäminen ja käyttöönotto (Platform update 41 ja uudemmat)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md) ohjeita. Keskus- ja scale unit -ympäristössä on käytettävä vähintään Supply Chain Managementin versiota 10.0.21. Lisäksi infrastruktuurikomentosarjoissa on oltava käytössä vähintään versio 2.12.0. 

    > [!IMPORTANT]
    > Lue tämän osan loppuosa, **ennen** kuin suoritat kyseisen aiheen vaiheet.

1. Suorita seuraava komentosarja, ennen kuin kuvaat määrityksesi tiedostossa infrastructure\\ConfigTemplate.xml:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Tämä komentosarja poistaa kaikki määritykset, joita ei tarvita reunapalvelujen scale unitien käyttöönotossa.

1. Määritä tyhjiä tietoja sisältävä tietokanta kohdassa [Tietokantojen määritys](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) kuvatulla tavalla. Käytä tässä vaiheessa tyhjää data.bak-tiedostoa.
1. Kun [Tietokantojen määrittäminen](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) -vaihe on suoritettu, Scale Unit Alm Orchestrator -tietokanta on määritettävä suorittamalla seuraava komentosarja.

    > [!NOTE]
    > Financial Reporting -tietokantaa ei määritetä [Tietokantojen määrittäminen](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) -vaiheessa.

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName EdgeScaleUnit
    ```

    Initialize-Database.ps1-komentosarja suorittaa seuraavat toiminnot:

    1. Luo tyhjä **ScaleUnitAlmDb**-niminen tietokanta.
    2. Yhdistä käyttäjät tietokantarooleihin seuraavan taulukon mukaisesti.

        | Käyttäjä            | Tyyppi | Tietokantarooli |
        |-----------------|------|---------------|
        | svc-LocalAgent$ | gMSA | db\_owner     |

1. Jatka kohdan [Paikallisten ympäristöjen määrittäminen ja käyttöönotto (Platform update 41 ja uudemmat)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md) ohjeiden noudattamista.
1. Kun [AD FS -määritys](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) -vaihe on suoritettu, toimi seuraavasti:

    1. Luo uusi Active Directory Federation Services (AD FS) -sovellus, jonka avulla Alm Orchestration -palvelu voi olla yhteydessä AOS (Application Object Server) -palvelimeen.

        ```powershell
        # Host URL is your DNS record\host name for accessing the AOS
        .\Create-ADFSServerApplicationForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -HostUrl 'https://ax.d365ffo.onprem.contoso.com'
        ```

    1. Luo uusi Azure Active Directory (Azure AD) -sovellus, jonka avulla Alm Orchestration -palvelu voi olla yhteydessä Scale Unit -hallintapalveluun.

        ```powershell
        # Example .\Create-SumAADApplication.ps1 -ConfigurationFilePath ..\ConfigTemplate.xml -TenantId '6240a19e-86f1-41af-91ab-dbe29dbcfb95' -ApplicationDisplayName 'EdgeAgent-SUMCommunication-EN01'
        .\Create-SumAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                       -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                       -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
        ```

1. Jatka kohdan [Paikallisten ympäristöjen määrittäminen ja käyttöönotto (Platform update 41 ja uudemmat)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md) ohjeiden noudattamista. Kun paikallisen edustajan määritys on annettava, varmista, että reunan Scale Unit -ominaisuudet on otettu käyttöön ja että kaikki tarvittavat parametrit on annettu.

    ![Reunan Scale unit -ominaisuuksien ottaminen käyttöön](media/EnableEdgeScaleUnitFeatures.png "Reunan Scale unit -ominaisuuksien ottaminen käyttöön")

1. Määritä käyttöönottoa edeltävä komentosarja ennen ympäristön käyttöönottoa LCS:stä. Lisätietoja: [Paikallisen edustajan ennen käyttöönottoa ja sen jälkeen suoritettavat komentosarjat](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md).

    1. Kopioi Configure-CloudAndEdge.ps1-komentosarja **infrastruktuurikomentosarjojen** **ScaleUnit**-kansiosta **Komentosarjat**-kansioon siinä edustajatiedostojen jaetussa tallennustilassa, joka on määritetty ympäristössä. Tyypillinen polku on \\\\lbdiscsi01\\edustaja\\Komentosarjat.
    2. Luo komentosarja **PreDeployment.ps1**, joka käynnistää komentosarjat käyttäen tarvittavia parametreja. Käyttöönottoa edeltävä komentosarja on sijoitettava edustajatiedostojen jaetun tallennustilan **Komentosarjat**-kansioon. Muuten sitä ei voi suorttaa. Tyypillinen polku on \\\\lbdiscsi01\\edustaja\\Komentosarjat\\PreDeployment.ps1.

        PreDeployment.ps1-komentosarjan sisältö muistuttaa seuraavaa esimerkkiä.

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        . $PSScriptRoot\Configure-CloudAndEdge.ps1 -AgentShare $agentShare -InstanceId '@A'
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
1. Kun ympäristö on otettu käyttöön, toimi seuraavasti:

    1. Suorita seuraava SQL-komennot yritystietokannassa (AXDB).

        ```sql
        ALTER TABLE dbo.NUMBERSEQUENCETABLE ENABLE CHANGE_TRACKING WITH (TRACK_COLUMNS_UPDATED = ON)
        delete from NumberSequenceTable
        delete from NumberSequenceReference
        delete from NumberSequenceScope
        delete from FeatureManagementMetadata
        delete from FeatureManagementState
        delete from SysFeatureStateV0
        ```

    1. Lisää samanaikaisten eräistuntojen enimmäismääräksi arvo, joka on suurempi kuin 4.

        ```sql
        Update batchserverconfig set maxbatchsessions = '<Replace with number of concurrent batch tasks you want>'
        ```

    1. Tarkista, että muutoksen seuranta on otettu käyttöön yritystietokannassa (AXDB).

        1. Avaa SQL Server Management Studio (SSMS).
        1. Pidä yritystietokantaa (AXDB) valittuna (tai napsauta sitä hiiren kakkospainikkeella) ja valitse sitten **Ominaisuudet**.
        1. Valitse avautuvassa ikkunassa **Muutosten seuranta** ja määritä sitten seuraavat arvot:

            - **Muutosten seuranta:** *Tosi*
            - **Säilytysaika:** *7*
            - **Säilytyksen yksiköt:** *Päivää*
            - **Automaattinen puhdistus:** *Tosi*

    1. Lisää aiemmin luotu AD FS -sovelluksen tunnus (käyttämällä Create-ADFSServerApplicationForEdgeScaleUnits.ps1-komentosarjaa) Azure AD -sovellustaulukkoon scale unitissa. Tämä vaihe voidaan suorittaa manuaalisesti käyttöliittymässä. Vaihtoehtoisesti se voidaan suorittaa tietokannan kautta seuraavan komentosarjan avulla.

        ```sql
        DECLARE @ALMOrchestratorId NVARCHAR(76) = '<Replace with the ADFS Application ID created in a previous step>';

        IF NOT EXISTS (SELECT TOP 1 1 FROM SysAADClientTable WHERE AADClientId = @ALMOrchestratorId)
        BEGIN
            INSERT INTO SysAADClientTable (AADClientId, UserId, Name, ModifiedBy, CreatedBy)
            VALUES (@ALMOrchestratorId, 'ScaleUnitManagement', 'Scale Unit Management', 'Admin', 'Admin');
        END
        ```

## <a name="set-up-an-azure-key-vault-and-an-azure-ad-application-to-enable-communication-between-scale-units"></a><a name="set-up-keyvault"></a>Azure Key Vaultin ja Azure AD -sovelluksen määrittäminen ottamaan käyttöön scale unitien välinen viestintä

1. Kun ympäristö on otettu käyttöön, Azure AD -lisäsovellus luodaan ottamaan käyttöön luotettava viestintä sovelluksen ja scale unitin välillä.

    ```powershell
    .\Create-SpokeToHubAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                          -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                          -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
    ```

1. Kun sovellus on luotu, asiakasohjelman salasana on luotava ja tallennettava Azure Key Vaultiin. Lisäksi on myönnettävä luodun Azure AD -sovelluksen käyttöoikeus, jotta se voi noutaa avainsäilöön tallennetut salasanat. Seuraava komentosarja suorittaa kätevästi kaikki tarvittavat toiminnot automaattisesti.

    ```powershell
    .\Create-SpokeToHubAADAppSecrets.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                         -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                         -SubscriptionName '<Any subscription within your tenant>' `
                                         -ResourceGroupName '<Any resource group within your subscription>' `
                                         -KeyVaultName '<Any key vault within your resource group>' `
                                         -Location '<Any Azure location where Azure Key Vault is available>' `
                                         -LCSEnvironmentId '<The LCS environment ID of your deployed scale unit>' `
    ```

    > [!NOTE]
    > Jos määritettyä **KeyVaultName**-arvoa ei ole yhdessäkään avainsäilössä, komentosarja luo sellaisen automaattisesti.

1. Lisää juuri luotu Azure AD -sovelluksen tunnus (Create-SpokeToHubAADApplication.ps1-komentosarjaa käytettäessä) Azure AD -sovellustaulukkoon keskuksessa. Tämä vaihe voidaan suorittaa manuaalisesti käyttöliittymässä.

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>Lataa kohdepaketit LCS:n LBD-projektiresursseihin

Tässä vaiheessa valmistellaan sovellusversio, ympäristöversio ja mukautukset, jotka siirretään LBD:n scale unit -ympäristöön.

1. Lataa sama yhdistetty sovellus-/ympäristöpaketti, jota käytettiin keskusympäristöön LCS:n paikallisen projektin resurssikirjastossa.
1. Nouda kopio mukautetusta käyttöönotettavasta paketista, jota käytettiin keskusympäristöön, ja lataa se LCS:n paikallisen projektin resurssikirjastoon.

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>Anna kohdepaketit LBD-ympäristön käyttöön.

Tässä vaiheessa täsmäytetään LBD:n scale unit -ympäristön sovellusversio, ympäristöversio ja mukautukset keskuksen kanssa.

1. Anna LBD-ympäristön käyttöön yhdistetty sovellus-/ympäristöpaketti, jonka latasit edellisessä vaiheessa.
1. Anna LBD-ympäristön käyttöön mukautettu käyttöönotettava paketti, jonka latasit edellisessä vaiheessa.

    ![Päivitysten käyttäminen LCS:ssä](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "Päivitysten käyttäminen LCS:ssä")

    ![Mukautuspaketin valitseminen.](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "Mukautuspaketin valitseminen")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>Kohdista LBD:n reunapalvelujen scale unit keskukseen

Reunan scale unitit määritetään ja niitä hallitaan Scale Unit -hallintaportaalissa. Lisätietoja on kohdassa [Scale unitien ja kuormitusten hallinta Scale Unit -hallintaportaalissa](./cloud-edge-landing-page.md#scale-unit-manager-portal).

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
