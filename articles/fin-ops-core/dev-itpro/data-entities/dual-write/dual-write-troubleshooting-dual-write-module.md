---
title: Finance and Operations -sovellusten kaksoiskirjoitusmoduulin ongelmien vianmääritys
description: Tässä ohjeaiheessa on vianmääritys tietoja, joiden avulla voit korjata Finance and Operations -sovellusten kaksoiskirjoitusmoduulin ongelmia.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2241e7e6219f95115f55bc45a4d94550276e1e21
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683620"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="7e50f-103">Finance and Operations -sovellusten kaksoiskirjoitusmoduulin ongelmien vianmääritys</span><span class="sxs-lookup"><span data-stu-id="7e50f-103">Troubleshoot issues with the dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="7e50f-104">Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Dataversen välillä.</span><span class="sxs-lookup"><span data-stu-id="7e50f-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="7e50f-105">Erityisesti se tarjoaa vianmääritystietoja, joiden avulla voit korjata Finance and Operations -sovellusten **kaksoiskirjoitusmoduulin** ongelmia.</span><span class="sxs-lookup"><span data-stu-id="7e50f-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7e50f-106">Jotkin tämän ohjeaiheen osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoftin Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia.</span><span class="sxs-lookup"><span data-stu-id="7e50f-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="7e50f-107">Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.</span><span class="sxs-lookup"><span data-stu-id="7e50f-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="7e50f-108">Kaksoiskirjoitusmoduulia ei voi ladata Finance and Operations -sovellukseen</span><span class="sxs-lookup"><span data-stu-id="7e50f-108">You can't load the dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="7e50f-109">Jos **Kaksoiskirjoitus**-sivua ei voi avata valitsemalla **Tietojen hallinta** -työtilassa **Kaksoiskirjoitus**-ruutu, tietojen integrointipalvelu ei todennäköisesti ole toiminnassa.</span><span class="sxs-lookup"><span data-stu-id="7e50f-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="7e50f-110">Luo tukipyyntö, joka pyytää tietojen integrointipalvelun uudelleenkäynnistystä.</span><span class="sxs-lookup"><span data-stu-id="7e50f-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-table-map"></a><span data-ttu-id="7e50f-111">Virhe yritettäessä luoda uutta taulukon yhdistämismääritystä</span><span class="sxs-lookup"><span data-stu-id="7e50f-111">Error when you try to create a new table map</span></span>

<span data-ttu-id="7e50f-112">**Tarvittavat tunnistetiedot ongelman korjaamiseksi:** Sama käyttäjä, joka määrittää kaksoiskirjoituksen.</span><span class="sxs-lookup"><span data-stu-id="7e50f-112">**Required credentials to fix the issue:** The same user that setup dual-write.</span></span>

<span data-ttu-id="7e50f-113">Näyttöön saattaa tulla seuraava virhesanoma, kun yrität määrittää uuden entiteetin kaksoiskirjoittamista varten.</span><span class="sxs-lookup"><span data-stu-id="7e50f-113">You might receive the following error message when you try to configure a new entity for dual-write.</span></span> <span data-ttu-id="7e50f-114">Ainoa käyttäjä, joka voi luoda yhdistämismäärityksen, on käyttäjä, joka määrittää kaksoiskirjoituksen yhteyden.</span><span class="sxs-lookup"><span data-stu-id="7e50f-114">The only user that can create a map is the user who setup the dual-write connection.</span></span>

<span data-ttu-id="7e50f-115">*Vastauksen tilakoodi ei tarkoita onnistumista: 401 (Luvaton)*</span><span class="sxs-lookup"><span data-stu-id="7e50f-115">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>


## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="7e50f-116">Virhe avattaessa kaksoiskirjoituskäyttöliittymää</span><span class="sxs-lookup"><span data-stu-id="7e50f-116">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="7e50f-117">Näyttöön saattaa tulla seuraavan kaltainen virhesanoma, kun yrität käyttää **Tietojen hallinta** -työtilan kaksoiskirjoittamista:</span><span class="sxs-lookup"><span data-stu-id="7e50f-117">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="7e50f-118">*login.microsoftonline.com kieltäytyi muodostamasta yhteyttä.*</span><span class="sxs-lookup"><span data-stu-id="7e50f-118">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="7e50f-119">Jos haluat korjata ongelman, kirjaudu sisään käyttämällä InPrivate-ikkunaa Microsoft Edgessä, tuntemattoman käyttäjän ikkunaa Chromiumissa tai tuntemattoman käyttäjän ikkunaa Google Chromessa.</span><span class="sxs-lookup"><span data-stu-id="7e50f-119">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="7e50f-120">Sinun on myös avattava kolmannen osapuolen evästeet tai poistettava niiden valinta.</span><span class="sxs-lookup"><span data-stu-id="7e50f-120">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a><span data-ttu-id="7e50f-121">Virhe yhdistettäessä ympäristöä kaksoiskirjoittamista tai uuden taulun yhdistämismääritystä varten</span><span class="sxs-lookup"><span data-stu-id="7e50f-121">Error when you link the environment for dual-write or add a new table mapping</span></span>

<span data-ttu-id="7e50f-122">**Ongelman korjaava rooli:** Järjestelmän ylläpitäjä sekä Finance and Operations -sovelluksissa ja Dataversessä.</span><span class="sxs-lookup"><span data-stu-id="7e50f-122">**Required role to fix the issue:** System administrator in both Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="7e50f-123">Saatat kohdata seuraavan virheen linkittäessäsi tai luodessasi karttoja:</span><span class="sxs-lookup"><span data-stu-id="7e50f-123">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="7e50f-124">*Vastauksen tilakoodi ei ilmaise onnistumista: 403 (tokenexchange).<br> Istunnon tunnus: \<your session id\><br> Päätehtävän tunnus: \<your root activity id\>*</span><span class="sxs-lookup"><span data-stu-id="7e50f-124">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="7e50f-125">Tämä virhe voi ilmetä, jos sinulla ei ole riittäviä oikeuksia yhdistää kaksoiskirjoitukseen tai luoda karttoja.</span><span class="sxs-lookup"><span data-stu-id="7e50f-125">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="7e50f-126">Tämä virhe voi ilmetä myös, jos Dataverse -ympäristö nollautuu ilman kaksoiskirjoituksen linkityksen poistamista.</span><span class="sxs-lookup"><span data-stu-id="7e50f-126">This error can also occur if the Dataverse environment was reset without unlinking dual-write.</span></span> <span data-ttu-id="7e50f-127">Kuka tahansa käyttäjä, jolla on järjestelmänvalvojan rooli sekä Finance and Operations-sovelluksissa että Dataversessä voi linkittää ympäristöt.</span><span class="sxs-lookup"><span data-stu-id="7e50f-127">Any user with system administrator role in both Finance and Operations apps and Dataverse can link the environments.</span></span> <span data-ttu-id="7e50f-128">Vain kaksoiskirjoitusyhteyden asetusten luonut käyttäjä voi lisätä uusia taulujen yhdistämismäärityksiä.</span><span class="sxs-lookup"><span data-stu-id="7e50f-128">Only the user who setup the dual-write connection can add new table maps.</span></span> <span data-ttu-id="7e50f-129">Asennuksen jälkeen kuka tahansa järjestelmänvalvoja, jolla on järjestelmänvalvojan rooli, voi valvoa tilaa ja muokata yhdistämismäärityksiä.</span><span class="sxs-lookup"><span data-stu-id="7e50f-129">After setup, any user with system administrator role can monitor the status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-table-mapping"></a><span data-ttu-id="7e50f-130">Virhe yritettäessä pysäyttää taulun yhdistämismääritystä</span><span class="sxs-lookup"><span data-stu-id="7e50f-130">Error when you stop the table mapping</span></span>

<span data-ttu-id="7e50f-131">Näyttöön saattaa tulla seuraava virhesanoma, kun yrität pysäyttää taulujen yhdistämismääritystä:</span><span class="sxs-lookup"><span data-stu-id="7e50f-131">You might receive the following error message when you try to stop the table mappings:</span></span>

<span data-ttu-id="7e50f-132">*\[Kielletty\], \[{"status": 403, "lähde":"","sanoma":"Virhe tunnuksen vaihdossa: Käyttäjällä ei ole oikeutta käyttää yhteyttä dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], Etäpalvelin palautti virheen: (403) kielletty.*</span><span class="sxs-lookup"><span data-stu-id="7e50f-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="7e50f-133">Tämä virhe ilmenee, kun linkitetty Dataverse -ympäristö ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="7e50f-133">This error occurs when the linked Dataverse environment isn't available.</span></span>

<span data-ttu-id="7e50f-134">Voit korjata ongelman luomalla pyynnön tietojen integrointitiimille.</span><span class="sxs-lookup"><span data-stu-id="7e50f-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="7e50f-135">Liitä verkon jäljitys, jotta tietojen integrointiryhmä voi merkitä karttojen tilaksi **Ei käynnissä** taustalla.</span><span class="sxs-lookup"><span data-stu-id="7e50f-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>

## <a name="error-while-trying-to-start-an-table-mapping"></a><span data-ttu-id="7e50f-136">Virhe yritettäessä käynnistää taulun yhdistämismääritystä</span><span class="sxs-lookup"><span data-stu-id="7e50f-136">Error while trying to start an table mapping</span></span>

<span data-ttu-id="7e50f-137">Näyttöön voi tulla seuraavankaltainen virhesanoma, kun yrität määrittää yhdistämismäärityksen tilaksi **Käytössä**:</span><span class="sxs-lookup"><span data-stu-id="7e50f-137">You might receive an error like the following when you try to set that state of a mapping to **Running**:</span></span>

<span data-ttu-id="7e50f-138">*Tietojen alkuperäistä synkronointia ei voi suorittaa loppuun. Virhe: kaksoiskirjoitusvirhe - laajennuksen rekisteröiminen epäonnistui: kaksoiskirjoitushaun metatietoja ei voi muodostaa. Virheen objektin viitettä ei ole määritetty objektin esiintymälle.*</span><span class="sxs-lookup"><span data-stu-id="7e50f-138">*Unable to complete initial data sync. Error: dual-write failure - plugin registration failed: Unable to build dual-write lookup metadata. Error object reference not set to an instance of an object.*</span></span>

<span data-ttu-id="7e50f-139">Tämän virheen korjaus määräytyy virheen syyn mukaan:</span><span class="sxs-lookup"><span data-stu-id="7e50f-139">The fix for this error depends on the cause of the error:</span></span>

+ <span data-ttu-id="7e50f-140">Jos yhdistämismääritykset ovat riippuvaisia määrityksistä, varmista, että otat käyttöön tämän taulun yhdistämismäärityksen sidonnaiset määritykset.</span><span class="sxs-lookup"><span data-stu-id="7e50f-140">If the mapping has dependent mappings, then make sure to enable the dependent mappings of this table mapping.</span></span>
+ <span data-ttu-id="7e50f-141">Yhdistämismäärityksestä saattaa puuttua lähde- tai kohdekentät.</span><span class="sxs-lookup"><span data-stu-id="7e50f-141">The mapping might be missing source or destination fields.</span></span> <span data-ttu-id="7e50f-142">Jos Finance and Operations -sovelluksen kenttä puuttuu, noudata [Puuttuvien yksikkökenttien ongelma yhdistämismäärityksissä](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps) -kohdan ohjeita.</span><span class="sxs-lookup"><span data-stu-id="7e50f-142">If a field in the Finance and Operations app is missing, then follow the steps in the section [Missing entity fields issue on maps](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps).</span></span> <span data-ttu-id="7e50f-143">Jos kenttä Dataversessä puuttuu, valitse yhdistämismäärityksessä **Päivitä taulut** -painike, jotta kentät täytetään automaattisesti takaisin yhdistämismääritykseen.</span><span class="sxs-lookup"><span data-stu-id="7e50f-143">If a field in Dataverse is missing, then click **Refresh tables** button on the mapping so that the fields are automatically populated back into the mapping.</span></span>
