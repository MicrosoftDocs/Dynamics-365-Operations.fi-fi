---
title: Live-synkronoinnin ongelmien vianmääritys
description: Tässä ohjeaiheessa on vianmääritystietoja, joiden avulla voit korjata ongelmia suoralla synkronoinnilla.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: b40b71eb45ae5a95a732c9554356afcddecb750e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566810"
---
# <a name="troubleshoot-live-synchronization-issues"></a><span data-ttu-id="e36ec-103">Live-synkronoinnin ongelmien vianmääritys</span><span class="sxs-lookup"><span data-stu-id="e36ec-103">Troubleshoot live synchronization issues</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="e36ec-104">Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Dataversen välillä.</span><span class="sxs-lookup"><span data-stu-id="e36ec-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="e36ec-105">Erityisesti se tarjoaa tietoja, joiden avulla voit korjata ongelmia suoralla synkronoinnilla.</span><span class="sxs-lookup"><span data-stu-id="e36ec-105">Specifically, it provides information that can help you fix issues with live synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e36ec-106">Jotkin tämän ohjeaiheen osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoftin Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia.</span><span class="sxs-lookup"><span data-stu-id="e36ec-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="e36ec-107">Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.</span><span class="sxs-lookup"><span data-stu-id="e36ec-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-row-in-a-finance-and-operations-app"></a><span data-ttu-id="e36ec-108">Suora synkronointi tuo näyttöön 403 Kielletty -virhesanoman, kun luot rivin Finance and Operations -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="e36ec-108">Live synchronization throws a 403 Forbidden error when you create a row in a Finance and Operations app</span></span>

<span data-ttu-id="e36ec-109">Näyttöön saattaa tulla seuraava virhesanoma, kun luot rivin Finance and Operations -sovelluksessa:</span><span class="sxs-lookup"><span data-stu-id="e36ec-109">You might receive the following error message when you create a row in a Finance and Operations app:</span></span>

<span data-ttu-id="e36ec-110">*\[{\\"virhe\\":{\\"koodi\\":\\"0x80072560\\",\\"viesti\\":\\"Käyttäjä ei ole organisaation jäsen.\\"}}\], Etäpalvelin palautti virheen: (403) Kielletty."}}".*</span><span class="sxs-lookup"><span data-stu-id="e36ec-110">*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"The user is not a member of the organization.\\"}}\], The remote server returned an error: (403) Forbidden."}}".*</span></span>

<span data-ttu-id="e36ec-111">Voit korjata ongelman noudattamalla [Järjestelmän vaatimukset ja edellytykset](requirements-and-prerequisites.md)-kohdan ohjeita.</span><span class="sxs-lookup"><span data-stu-id="e36ec-111">To fix the issue, follow the steps in [System requirements and prerequisites](requirements-and-prerequisites.md).</span></span> <span data-ttu-id="e36ec-112">Näiden vaiheiden suorittaminen Dataversessä edellyttää, että sovelluksessa luoduilla kaksoiskirjoituskäyttäjillä on järjestelmänvalvojan rooli.</span><span class="sxs-lookup"><span data-stu-id="e36ec-112">To complete those steps, the dual-write application users who are created in Dataverse must have the system admin role.</span></span> <span data-ttu-id="e36ec-113">Omistavan ryhmän oletusryhmällä on oltava myös järjestelmänvalvojan rooli.</span><span class="sxs-lookup"><span data-stu-id="e36ec-113">The default owning team must also have the system admin role.</span></span>

## <a name="live-synchronization-for-any-table-consistently-throws-a-similar-error-when-you-create-a-row-in-a-finance-and-operations-app"></a><span data-ttu-id="e36ec-114">Minkä tahansa taulukon suora synkronointi johtaa järjestelmällisesti samanlaisen virheeseen, kun luot rivin Finance and Operations -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="e36ec-114">Live synchronization for any table consistently throws a similar error when you create a row in a Finance and Operations app</span></span>

<span data-ttu-id="e36ec-115">**Ongelman korjaamiseen tarvittava rooli:** Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="e36ec-115">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="e36ec-116">Näyttöön saattaa tulla seuraavan kaltainen virhesanoma aina, kun yrität tallentaa Finance and Operations -sovelluksen taulukon tietoja:</span><span class="sxs-lookup"><span data-stu-id="e36ec-116">You might receive an error message like the following every time that you try to save table data in a Finance and Operations app:</span></span>

<span data-ttu-id="e36ec-117">*Muutoksia ei voi tallentaa tietokantaan. Työyksikkö ei voi sitoutua tapahtumaan. Tietoja ei voi kirjoittaa yksikön mittayksikköön. Kirjoitukset UnitOfMeasureEntity-kohtaan epäonnistuivat ja näkyviin tuli virhesanoma Ei voi synkronoida mittayksikön kanssa.*</span><span class="sxs-lookup"><span data-stu-id="e36ec-117">*Cannot save the changes to the database. Unit of Work can not commit transaction. Unable to write data to entity uoms. Writes to UnitOfMeasureEntity failed with error message Unable to sync with entity uoms.*</span></span>

<span data-ttu-id="e36ec-118">Voit korjata ongelman varmistamalla, että sekä Finance and Operations -sovelluksessa että Dataversessä on tarvittavat viitetiedot.</span><span class="sxs-lookup"><span data-stu-id="e36ec-118">To fix the issue, you must make sure that the prerequisite reference data exists in both the Finance and Operations app and Dataverse.</span></span> <span data-ttu-id="e36ec-119">Jos esimerkiksi asiakas, joka olet Finance and Operations -sovelluksessa, kuuluu tiettyyn asiakasryhmään, varmista, että asiakasryhmä on olemassa Dataversessä.</span><span class="sxs-lookup"><span data-stu-id="e36ec-119">For example, if the customer that you're in the Finance and Operations app belongs to a specific customer group, make sure that the customer group exists in Dataverse.</span></span>

<span data-ttu-id="e36ec-120">Jos molemmilla puolilla on tietoja ja olet vahvistanut, että ongelma ei liity tietoihin, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="e36ec-120">If data exists on both sides, and you've confirmed that the issue isn't data-related, follow these steps.</span></span>

1. <span data-ttu-id="e36ec-121">Pysäytä liittyvä taulukko.</span><span class="sxs-lookup"><span data-stu-id="e36ec-121">Stop the related table.</span></span>
2. <span data-ttu-id="e36ec-122">Kirjaudu sisään Finance and Operations -sovellukseen ja varmista, että epäonnistuneen taulukon rivejä on olemassa DualWriteProjectConfiguration- ja DualWriteProjectFieldConfiguration-taulukoissa.</span><span class="sxs-lookup"><span data-stu-id="e36ec-122">Sign in to the Finance and Operations app, and make sure that rows for the failing table exist in the DualWriteProjectConfiguration and DualWriteProjectFieldConfiguration tables.</span></span> <span data-ttu-id="e36ec-123">Kysely näyttää esimerkiksi siltä, että **Asiakkaat**-taulukko epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="e36ec-123">For example, here is what the query looks like if the **Customers** table is failing.</span></span>

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. <span data-ttu-id="e36ec-124">Jos epäonnistuneelle taulukolle on rivejä myös sen jälkeen, kun olet estänyt taulun yhdistämismäärityksen, poista epäonnistuvaan taulukkoon liittyvät rivit.</span><span class="sxs-lookup"><span data-stu-id="e36ec-124">If there are rows for the failing table even after you stop the table mapping, delete the rows that are related to the failing table.</span></span> <span data-ttu-id="e36ec-125">Tee **projectname**-sarakkeesta muistiinpano DualWriteProjectConfiguration-taulussa ja nouda rivi DualWriteProjectFieldConfiguration-taulusta käyttämällä projektin nimeä rivin poistamiseen.</span><span class="sxs-lookup"><span data-stu-id="e36ec-125">Make a note of the **projectname** column in the DualWriteProjectConfiguration table, and fetch the row in the DualWriteProjectFieldConfiguration table by using the project name to delete the row.</span></span>
4. <span data-ttu-id="e36ec-126">Aloita taulun yhdistäminen.</span><span class="sxs-lookup"><span data-stu-id="e36ec-126">Start the table mapping.</span></span> <span data-ttu-id="e36ec-127">Tarkista, synkronoitiinko tiedot ilman ongelmia.</span><span class="sxs-lookup"><span data-stu-id="e36ec-127">Validate whether the data is synced without any issues.</span></span>

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a><span data-ttu-id="e36ec-128">Luku- tai kirjoitusoikeusvirheiden käsitteleminen Finance and Operations -sovelluksen tietojen luonnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="e36ec-128">Handle read or write privilege errors when you create data in a Finance and Operations app</span></span>

<span data-ttu-id="e36ec-129">Näyttöön saattaa tulla "virheellinen pyyntö" -virhesanoma, joka muistuttaa seuraavaa esimerkkiä, kun luot tietoja Finance and Operations -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="e36ec-129">You might receive a "Bad Request" error message that resembles the following example when you create data in a Finance and Operations app.</span></span>

![Esimerkki virheellisen pyynnön virhesanomasta](media/error_record_id_source.png)

<span data-ttu-id="e36ec-131">Ongelman korjaaminen edellyttää, että määrität oikean käyttöoikeusroolin yhdistetyn Dynamics 365 Sales- tai Dynamics 365 Customer Service -liiketoimintayksikön ryhmälle, jotta puuttuva oikeus voidaan ottaa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="e36ec-131">To fix the issue, you must assign the correct security role to the team of the mapped Dynamics 365 Sales or Dynamics 365 Customer Service business unit to enable the missing privilege.</span></span>

1. <span data-ttu-id="e36ec-132">Etsi Finance and Operations -sovelluksessa liiketoimintayksikkö, joka on yhdistetty tietojen integroinnin yhteysjoukkoon.</span><span class="sxs-lookup"><span data-stu-id="e36ec-132">In the Finance and Operations app, find the business unit that is mapped in the Data Integration connection set.</span></span>

    ![Organisaation yhdistämismääritys](media/mapped_business_unit.png)

2. <span data-ttu-id="e36ec-134">Kirjaudu sisään ympäristöön Dynamics 365 -ohjelman mallipohjaisen sovelluksen avulla, siirry kohtaan **Asetus \> Suojaus** ja etsi yhdistetyn liiketoimintayksikön ryhmä.</span><span class="sxs-lookup"><span data-stu-id="e36ec-134">Sign in to the environment in the model-driven app in Dynamics 365, navigate to **Setting \> Security**, and find the team of the mapped business unit.</span></span>

    ![Yhdistetyn liiketoimintayksikön ryhmä](media/setting_security_page.png)

3. <span data-ttu-id="e36ec-136">Avaa ryhmän sivu muokkausta varten ja valitse sitten **Ryhmän roolit** avataksesi **Hallitse ryhmän rooleja** -valintaikkunan.</span><span class="sxs-lookup"><span data-stu-id="e36ec-136">Open the page for the team for editing, and then select **Manage roles** to open the **Manage Team Roles** dialog box.</span></span>

    ![Roolien hallinta -painike](media/manage_team_roles.png)

4. <span data-ttu-id="e36ec-138">Delegoi rooli, jolla on liittyvien taulujenn luku- ja kirjoitusoikeudet, ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="e36ec-138">Assign the role that has the read/write privilege for the relevant tables, and then select **OK**.</span></span>

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a><span data-ttu-id="e36ec-139">Synkronointiongelmien korjaaminen äskettäin muuttuneessa Dataverse -ympäristössä</span><span class="sxs-lookup"><span data-stu-id="e36ec-139">Fix synchronization issues in an environment that has a recently changed Dataverse environment</span></span>

<span data-ttu-id="e36ec-140">**Ongelman korjaamiseen tarvittava rooli:** Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="e36ec-140">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="e36ec-141">Näyttöön saattaa tulla seuraava virhesanoma, kun luot tietoa Finance and Operations -sovelluksessa:</span><span class="sxs-lookup"><span data-stu-id="e36ec-141">You might receive the following error message when you create data in a Finance and Operations app:</span></span>

<span data-ttu-id="e36ec-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Hyötykuormaa ei voida luoda yksikölle CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Hyötykuorman luonti epäonnistui, väärä URI: URI on tyhjä."}\],"isErrorCountUpdated":true}*</span><span class="sxs-lookup"><span data-stu-id="e36ec-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Unable to generate payload for entity CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Payload creation failed with error Invalid URI: The URI is empty."}\],"isErrorCountUpdated":true}*</span></span>

<span data-ttu-id="e36ec-143">Tässä on virhe, joka näyttää Dynamics 365:n mallipohjaisen sovelluksen.</span><span class="sxs-lookup"><span data-stu-id="e36ec-143">Here is what the error looks like in the model-driven app in Dynamics 365:</span></span>

<span data-ttu-id="e36ec-144">*Odottamaton virhe ISV-koodista. (ErrorType = ClientError) Odottamaton poikkeus laajennuksesta (Suorita): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: yksikön tilin käsittely epäonnistui - (yhteysyritys epäonnistui, koska yhdistetty osapuoli ei vastannut oikein tietyn ajanjakson jälkeen tai muodostettu yhteys epäonnistui, koska liitetty isäntä ei vastannut*</span><span class="sxs-lookup"><span data-stu-id="e36ec-144">*An unexpected error occurred from ISV code. (ErrorType = ClientError) Unexpected exception from plug-in (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: failed to process entity account - (A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond*</span></span>

<span data-ttu-id="e36ec-145">Tämä virhe ilmenee, kun Dataverse -ympäristö palautetaan virheellisesti samaan aikaan, kun yrität luoda tietoja Finance and Operations -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="e36ec-145">This error occurs when the Dataverse environment is incorrectly reset at the same time that you try to create data in the Finance and Operations app.</span></span>

<span data-ttu-id="e36ec-146">Korjaa ongelma seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="e36ec-146">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="e36ec-147">Kirjaudu Finance and Operations -virtuaalikoneeseen (VM), avaa SQL Server Management Studio (SSMS) ja etsi rivejä DUALWRITEPROJECTCONFIGURATIONENTITY-taulusta, jossa **internalentityname** on sama kuin **Asiakkaat V3** ja **externalentityname** on sama kuin **tilit**.</span><span class="sxs-lookup"><span data-stu-id="e36ec-147">Sign in to the Finance and Operations virtual machine (VM), open SQL Server Management Studio (SSMS), and look for rows in the DUALWRITEPROJECTCONFIGURATIONENTITY table where **internalentityname** equals **Customers V3** and **externalentityname** equals **accounts**.</span></span> <span data-ttu-id="e36ec-148">Tältä on kysely näyttää.</span><span class="sxs-lookup"><span data-stu-id="e36ec-148">Here is what the query looks like.</span></span>

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. <span data-ttu-id="e36ec-149">Suorita seuraava kysely käyttämällä edellisen kyselyn tuloksissa olevaa projektin nimeä.</span><span class="sxs-lookup"><span data-stu-id="e36ec-149">Use the project name from the results of the previous query to run the following query.</span></span>

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. <span data-ttu-id="e36ec-150">Varmista, että **externalenvironmentURL**-sarakkeessa on oikea Dataverse- tai sovelluksen URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="e36ec-150">Make sure that the **externalenvironmentURL** column has the correct Dataverse or app URL.</span></span> <span data-ttu-id="e36ec-151">Poista kaikki rivien kaksoiskappaleet, jotka viittaavat väärään Dataverse -URL-osoitteeseen.</span><span class="sxs-lookup"><span data-stu-id="e36ec-151">Delete any duplicate rows that point to the wrong Dataverse URL.</span></span> <span data-ttu-id="e36ec-152">Poista vastaavat rivit DUALWRITEPROJECTFIELDCONFIGURATION- ja DUALWRITEPROJECTCONFIGURATION-tauluista.</span><span class="sxs-lookup"><span data-stu-id="e36ec-152">Delete the corresponding rows in the DUALWRITEPROJECTFIELDCONFIGURATION and DUALWRITEPROJECTCONFIGURATION tables.</span></span>
4. <span data-ttu-id="e36ec-153">Pysäytä taulun yhdistäminen ja käynnistä se sitten uudelleen</span><span class="sxs-lookup"><span data-stu-id="e36ec-153">Stop the table mapping, and then restart it</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]