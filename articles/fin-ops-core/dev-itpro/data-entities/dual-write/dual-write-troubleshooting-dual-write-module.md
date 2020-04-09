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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172757"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="22c16-103">Finance and Operations -sovellusten kaksoiskirjoitusmoduulin ongelmien vianmääritys</span><span class="sxs-lookup"><span data-stu-id="22c16-103">Troubleshoot issues with the Dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="22c16-104">Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Common Data Servicen välillä.</span><span class="sxs-lookup"><span data-stu-id="22c16-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="22c16-105">Erityisesti se tarjoaa vianmääritystietoja, joiden avulla voit korjata Finance and Operations -sovellusten **kaksoiskirjoitusmoduulin** ongelmia.</span><span class="sxs-lookup"><span data-stu-id="22c16-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="22c16-106">Jotkin tämän ohjeaiheen osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoftin Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia.</span><span class="sxs-lookup"><span data-stu-id="22c16-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="22c16-107">Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.</span><span class="sxs-lookup"><span data-stu-id="22c16-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="22c16-108">Kaksoiskirjoitusmoduulia ei voi ladata Finance and Operations -sovellukseen</span><span class="sxs-lookup"><span data-stu-id="22c16-108">You can't load the Dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="22c16-109">Jos **Kaksoiskirjoitus**-sivua ei voi avata valitsemalla **Tietojen hallinta** -työtilassa **Kaksoiskirjoitus**-ruutu, tietojen integrointipalvelu ei todennäköisesti ole toiminnassa.</span><span class="sxs-lookup"><span data-stu-id="22c16-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="22c16-110">Luo tukipyyntö, joka pyytää tietojen integrointipalvelun uudelleenkäynnistystä.</span><span class="sxs-lookup"><span data-stu-id="22c16-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a><span data-ttu-id="22c16-111">Virhe yritettäessä luoda uutta entiteetin yhdistämismääritystä</span><span class="sxs-lookup"><span data-stu-id="22c16-111">Error when you try to create a new entity mapping</span></span>

<span data-ttu-id="22c16-112">**Ongelman korjauksen edellyttämät tunnistetiedot:** Azure AD -vuokralaisten hallinta</span><span class="sxs-lookup"><span data-stu-id="22c16-112">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="22c16-113">Näyttöön saattaa tulla seuraava virhesanoma, kun yrität määrittää uuden entiteetin kaksoiskirjoittamista varten:</span><span class="sxs-lookup"><span data-stu-id="22c16-113">You might receive the following error message when you try to configure a new entity for dual-write:</span></span>

<span data-ttu-id="22c16-114">*Vastauksen tilakoodi ei tarkoita onnistumista: 401 (Luvaton)*</span><span class="sxs-lookup"><span data-stu-id="22c16-114">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>

<span data-ttu-id="22c16-115">Tämä virhe ilmenee, koska vain Azure AD -vuokralaisen järjestelmänvalvoja voi lisätä uuden entiteetin yhdistämismäärityksen.</span><span class="sxs-lookup"><span data-stu-id="22c16-115">This error occurs because only an Azure AD tenant admin can add a new entity mapping.</span></span>

<span data-ttu-id="22c16-116">Voit korjata ongelman kirjautumalla Finance and Operations -sovellukseen Azure AD -ylläpitäjänä.</span><span class="sxs-lookup"><span data-stu-id="22c16-116">To fix the issue, sign in to the Finance and Operations app as an Azure AD admin tenant.</span></span> <span data-ttu-id="22c16-117">Sinun on myös mentävä web.PowerApps. comiin ja vahvistaa yhteys uudelleen.</span><span class="sxs-lookup"><span data-stu-id="22c16-117">You must also go to web.PowerApps.com and revalidate your connection.</span></span>

## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="22c16-118">Virhe avattaessa kaksoiskirjoituskäyttöliittymää</span><span class="sxs-lookup"><span data-stu-id="22c16-118">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="22c16-119">Näyttöön saattaa tulla seuraavan kaltainen virhesanoma, kun yrität käyttää **Tietojen hallinta** -työtilan kaksoiskirjoittamista:</span><span class="sxs-lookup"><span data-stu-id="22c16-119">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="22c16-120">*login.microsoftonline.com kieltäytyi muodostamasta yhteyttä.*</span><span class="sxs-lookup"><span data-stu-id="22c16-120">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="22c16-121">Jos haluat korjata ongelman, kirjaudu sisään käyttämällä InPrivate-ikkunaa Microsoft Edgessä, tuntemattoman käyttäjän ikkunaa Chromiumissa tai tuntemattoman käyttäjän ikkunaa Google Chromessa.</span><span class="sxs-lookup"><span data-stu-id="22c16-121">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="22c16-122">Sinun on myös avattava kolmannen osapuolen evästeet tai poistettava niiden valinta.</span><span class="sxs-lookup"><span data-stu-id="22c16-122">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a><span data-ttu-id="22c16-123">Virhe yhdistettäessä ympäristöä kaksoiskirjoittamista tai uuden entiteetin yhdistämismääritystä varten</span><span class="sxs-lookup"><span data-stu-id="22c16-123">Error when you link the environment for dual-write or add a new entity mapping</span></span>

<span data-ttu-id="22c16-124">**Ongelman korjauksen edellyttämät tunnistetiedot:** Azure AD -vuokralaisten hallinta</span><span class="sxs-lookup"><span data-stu-id="22c16-124">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="22c16-125">Saatat kohdata seuraavan virheen linkittäessäsi tai luodessasi karttoja:</span><span class="sxs-lookup"><span data-stu-id="22c16-125">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="22c16-126">*Vastauksen tilakoodi ei ilmaise onnistumista: 403 (tokenexchange).<br> Istunnon tunnus: \<istuntosi tunnus\><br> Päätehtävän tunnus: \<päätehtäväsi tunnus\>*</span><span class="sxs-lookup"><span data-stu-id="22c16-126">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="22c16-127">Tämä virhe voi ilmetä, jos sinulla ei ole riittäviä oikeuksia yhdistää kaksoiskirjoitukseen tai luoda karttoja.</span><span class="sxs-lookup"><span data-stu-id="22c16-127">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="22c16-128">Sinun on käytettävä Azure AD -vuokralaisen järjestelmänvalvojan tiliä, jotta voit linkittää ympäristöjä ja lisätä uusia kohteiden yhdistämismäärityksiä.</span><span class="sxs-lookup"><span data-stu-id="22c16-128">You must use an Azure AD tenant admin account to link environments and add new entity mappings.</span></span> <span data-ttu-id="22c16-129">Asennuksen jälkeen voit kuitenkin käyttää muuta kuin järjestelmänvalvojan tiliä tilan tarkkailemiseen ja yhdistämismääritysten muokkaamiseen.</span><span class="sxs-lookup"><span data-stu-id="22c16-129">However, after setup, you can use a non-admin account to monitor status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-entity-mapping"></a><span data-ttu-id="22c16-130">Virhe yritettäessä pysäyttää entiteetin yhdistämismääritystä</span><span class="sxs-lookup"><span data-stu-id="22c16-130">Error when you stop the entity mapping</span></span>

<span data-ttu-id="22c16-131">Näyttöön saattaa tulla seuraava virhesanoma, kun yrität pysäyttää entiteetin yhdistämismääritystä:</span><span class="sxs-lookup"><span data-stu-id="22c16-131">You might receive the following error message when you try to stop the entity mappings:</span></span>

<span data-ttu-id="22c16-132">*\[Kielletty\], \[{"status": 403, "lähde":"","sanoma":"Virhe tunnuksen vaihdossa: Käyttäjällä ei ole oikeutta käyttää yhteyttä dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], Etäpalvelin palautti virheen: (403) kielletty.*</span><span class="sxs-lookup"><span data-stu-id="22c16-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="22c16-133">Tämä virhe ilmenee, kun linkitetty Common Data Service -ympäristö ei ole käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="22c16-133">This error occurs when the linked Common Data Service environment isn't available.</span></span>

<span data-ttu-id="22c16-134">Voit korjata ongelman luomalla pyynnön tietojen integrointitiimille.</span><span class="sxs-lookup"><span data-stu-id="22c16-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="22c16-135">Liitä verkon jäljitys, jotta tietojen integrointiryhmä voi merkitä karttojen tilaksi **Ei käynnissä** taustalla.</span><span class="sxs-lookup"><span data-stu-id="22c16-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>
