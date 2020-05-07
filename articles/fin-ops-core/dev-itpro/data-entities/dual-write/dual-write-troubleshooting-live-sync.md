---
title: Live-synkronoinnin ongelmien vianmääritys
description: Tässä ohjeaiheessa on vianmääritystietoja, joiden avulla voit korjata ongelmia suoralla synkronoinnilla.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: d45b19c1e88e6a27bde4335d4a356f2173bdfcd3
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275414"
---
# <a name="troubleshoot-live-synchronization-issues"></a>Live-synkronoinnin ongelmien vianmääritys

[!include [banner](../../includes/banner.md)]



Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Common Data Servicen välillä. Erityisesti se tarjoaa tietoja, joiden avulla voit korjata ongelmia suoralla synkronoinnilla.

> [!IMPORTANT]
> Jotkin tämän ohjeaiheen osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoftin Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia. Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-record-in-a-finance-and-operations-app"></a>Suora synkronointi tuo näyttöön 403 Kielletty -virhesanoman, kun luot tietueen Finance and Operations -sovelluksessa

Näyttöön saattaa tulla seuraava virhesanoma, kun luot tietueen Finance and Operations -sovelluksessa:

*\[{\\"virhe\\":{\\"koodi\\":\\"0x80072560\\",\\"viesti\\":\\"Käyttäjä ei ole organisaation jäsen.\\"}}\], Etäpalvelin palautti virheen: (403) Kielletty."}}".*

Voit korjata ongelman noudattamalla [Järjestelmän vaatimukset ja edellytykset](requirements-and-prerequisites.md)-kohdan ohjeita. Näiden vaiheiden suorittaminen Common Data Servicessä edellyttää, että sovelluksessa luoduilla kaksoiskirjoituskäyttäjillä on järjestelmänvalvojan rooli. Omistavan ryhmän oletusryhmällä on oltava myös järjestelmänvalvojan rooli.

## <a name="live-synchronization-for-any-entity-consistently-throws-a-similar-error-when-you-create-a-record-in-a-finance-and-operations-app"></a>Minkä tahansa yksikön suora synkronointi johtaa järjestelmällisesti samanlaisen virheeseen, kun luot tietueen Finance and Operations -sovelluksessa.

**Ongelman korjaamiseen tarvittava rooli:** Järjestelmänvalvoja

Näyttöön saattaa tulla seuraavan kaltainen virhesanoma aina, kun yrität tallentaa Finance and Operations -sovelluksen yksikön tietoja:

*Muutoksia ei voi tallentaa tietokantaan. Työyksikkö ei voi sitoutua tapahtumaan. Tietoja ei voi kirjoittaa yksikön mittayksikköön. Kirjoitukset UnitOfMeasureEntity-kohtaan epäonnistuivat ja näkyviin tuli virhesanoma Ei voi synkronoida mittayksikön kanssa.*

Voit korjata ongelman varmistamalla, että sekä Finance and Operations -sovelluksessa että Common Data Servicessä on tarvittavat viitetiedot. Jos esimerkiksi asiakas, joka olet Finance and Operations -sovelluksessa, kuuluu tiettyyn asiakasryhmään, varmista, että asiakasryhmä on olemassa Common Data Servicessä.

Jos molemmilla puolilla on tietoja ja olet vahvistanut, että ongelma ei liity tietoihin, toimi seuraavasti.

1. Pysäytä liittyvä yksikkö.
2. Kirjaudu sisään Finance and Operations -sovellukseen ja varmista, että epäonnistuneen yksikön tietueita on olemassa DualWriteProjectConfiguration- ja DualWriteProjectFieldConfiguration-taulukoissa. Kysely näyttää esimerkiksi siltä, että **Asiakkaat**-yksikkö epäonnistuu.

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. Jos epäonnistuneen yksikön tietueissa on tietoja myös sen jälkeen, kun olet estänyt kohteen yhdistämismäärityksen, poista epäonnistuvaan yksikköön liittyvät tiedot. Kirjoita **projectname**-sarakkeesta kommentti DualWriteProjectConfiguration-taulussa ja nouda tietue DualWriteProjectFieldConfiguration-taulusta käyttämällä projektin nimeä tietueen poistamiseen.
4. Aloita entiteetin yhdistämismääritys. Tarkista, synkronoitiinko tiedot ilman ongelmia.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>Luku- tai kirjoitusoikeusvirheiden käsitteleminen Finance and Operations -sovelluksen tietojen luonnin yhteydessä

Näyttöön saattaa tulla "virheellinen pyyntö" -virhesanoma, joka muistuttaa seuraavaa esimerkkiä, kun luot tietoja Finance and Operations -sovelluksessa.

![Esimerkki virheellisen pyynnön virhesanomasta](media/error_record_id_source.png)

Ongelman korjaaminen edellyttää, että määrität oikean käyttöoikeusroolin yhdistetyn Dynamics 365 Sales- tai Dynamics 365 Customer Service -liiketoimintayksikön ryhmälle, jotta puuttuva oikeus voidaan ottaa käyttöön.

1. Etsi Finance and Operations -sovelluksessa liiketoimintayksikkö, joka on yhdistetty tietojen integroinnin yhteysjoukkoon.

    ![Organisaation yhdistämismääritys](media/mapped_business_unit.png)

2. Kirjaudu sisään ympäristöön Dynamics 365 -ohjelman mallipohjaisen sovelluksen avulla, siirry kohtaan **Asetus \> Suojaus** ja etsi yhdistetyn liiketoimintayksikön ryhmä.

    ![Yhdistetyn liiketoimintayksikön ryhmä](media/setting_security_page.png)

3. Avaa ryhmän sivu muokkausta varten ja valitse sitten **Ryhmän roolit** avataksesi **Hallitse ryhmän rooleja** -valintaikkunan.

    ![Roolien hallinta -painike](media/manage_team_roles.png)

4. Määritä rooli, jolla liittyvien yksiköiden luku- ja kirjoitusoikeudet ovat, ja valitse sitten **OK**.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-common-data-service-environment"></a>Synkronointiongelmien korjaaminen äskettäin muuttuneessa Common Data Service -ympäristössä

**Ongelman korjaamiseen tarvittava rooli:** Järjestelmänvalvoja

Näyttöön saattaa tulla seuraava virhesanoma, kun luot tietoa Finance and Operations -sovelluksessa:

*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Hyötykuormaa ei voida luoda yksikölle CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Hyötykuorman luonti epäonnistui, väärä URI: URI on tyhjä."}\],"isErrorCountUpdated":true}*

Tässä on virhe, joka näyttää Dynamics 365:n mallipohjaisen sovelluksen.

*Odottamaton virhe ISV-koodista. (ErrorType = ClientError) Odottamaton poikkeus laajennuksesta (Suorita): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: yksikön tilin käsittely epäonnistui - (yhteysyritys epäonnistui, koska yhdistetty osapuoli ei vastannut oikein tietyn ajanjakson jälkeen tai muodostettu yhteys epäonnistui, koska liitetty isäntä ei vastannut*

Tämä virhe ilmenee, kun Common Data Service -ympäristö palautetaan virheellisesti samaan aikaan, kun yrität luoda tietoja Finance and Operations -sovelluksessa.

Korjaa ongelma seuraavien ohjeiden mukaisesti.

1. Kirjaudu Finance and Operations -virtuaalikoneeseen (VM), avaa SQL Server Management Studio (SSMS) ja etsi tietoja DUALWRITEPROJECTCONFIGURATIONENTITY-taulusta, jossa **internalentityname** on sama kuin **Asiakkaat V3** ja **externalentityname** on sama kuin **tilit**. Tältä on kysely näyttää.

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. Suorita seuraava kysely käyttämällä edellisen kyselyn tuloksissa olevaa projektin nimeä.

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. Varmista, että **externalenvironmentURL**-sarakkeessa on oikea Common Data Service- tai sovelluksen URL-osoite. Poista kaikki tietueiden kaksoiskappaleet, jotka viittaavat väärään Common Data Service -URL-osoitteeseen. Poista vastaavat tiedot DUALWRITEPROJECTFIELDCONFIGURATION- ja DUALWRITEPROJECTCONFIGURATION-tauluista.
4. Pysäytä yksikön yhdistämismääritys ja käynnistä se sitten uudelleen
