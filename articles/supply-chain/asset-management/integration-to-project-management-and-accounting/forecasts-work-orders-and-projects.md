---
title: Ennusteet, työtilaukset ja projektit
description: Tässä ohjeaiheessa selitetään ennusteiden ja työtilausten integrointi resurssien hallinnan Projektinhallinta ja kirjanpito -moduulin kanssa.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e986d139ac9d0a7729bb9787f05332bcc09f59b
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886813"
---
# <a name="forecasts-work-orders-and-projects"></a><span data-ttu-id="2d1b4-103">Ennusteet, työtilaukset ja projektit</span><span class="sxs-lookup"><span data-stu-id="2d1b4-103">Forecasts, work orders, and projects</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="2d1b4-104">Resurssien hallinnassa integrointi **Projektinhallinta ja kirjanpito** -moduuliin tehdään, jotta voidaan optimoida kustannusten hallinta, jonka avulla käyttäjät voivat seurata kustannuksia huoltotyön tyyppien ennusteissa ja työtilaustöissä.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-104">In Asset Management, integration to the **Project management and accounting** module is done to optimize cost control, allowing users to track costs on maintenance job type forecasts and work order jobs.</span></span>

<span data-ttu-id="2d1b4-105">Kunnossapitotöiden tyyppien ennusteiden seuraamista varten on tehtävä kaksi asetusta:</span><span class="sxs-lookup"><span data-stu-id="2d1b4-105">To track maintenance job type forecasts, two settings must be made:</span></span>

1. <span data-ttu-id="2d1b4-106">Valitse projekti kohdassa **Resurssien hallinta** > **Asetukset** > **Resurssienhallinnan parametrit** > **Resurssit** -linkki > **Projekti** -pikavälilehti > **Ylläpitoennusteen projekti** -kenttä.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-106">Select a project in **Asset management** > **Setup** > **Asset management parameters** > **Assets** link > **Project** FastTab > **Maintenance forecast project** field.</span></span>

2. <span data-ttu-id="2d1b4-107">Kun **Ylläpitotyön tyyppien oletus** -kohdassa luot ylläpitotyötyypin oletusrivin, riville luodaan automaattisestitehtävänumero (**Resirssien hallinta** > **Asetukset** > **työt** > **Ylläpitotyön tyyppien oletukset**).</span><span class="sxs-lookup"><span data-stu-id="2d1b4-107">In **Maintenance job type defaults**, when you create a mainteance job type default line, an activity number is automatically created for the line (**Asset management** > **Setup** > **Jobs** > **Maintenance job type defaults**).</span></span>

<span data-ttu-id="2d1b4-108">Kunnossapitotöiden tyypin ennusteissa on kaksi tarkoitusta: voit jäljittää ylläpitotyön tyyppien ennusteiden kustannukset **Projektinhallinta ja kirjanpito** -moduulissa.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-108">Maintenance job type forecasts serve two purposes: You are able to track costs on maintenance job type forecasts in the **Project management and accounting** module.</span></span> <span data-ttu-id="2d1b4-109">Lisäksi ennusteet siirretään automaattisesti työtilauksen työn projektiin, kun valitset kunnossapitotyön tyypin työtilaustyölle.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-109">Furthermore, forecasts are automatically transferred to a work order job project when you select a maintenance job type on a work order job.</span></span>

<span data-ttu-id="2d1b4-110">Jotta työtilausten töiden kustannukset voidaan jäljittää, on ensin määritettävä työtilausprojektit.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-110">To track costs on work order jobs, you must first set up work order projects.</span></span> <span data-ttu-id="2d1b4-111">Toimenpiteen kuvaus on kohdassa [Työtilauksen projektin määritys](../setup-for-work-orders/work-order-project-setup.md).</span><span class="sxs-lookup"><span data-stu-id="2d1b4-111">Refer to the [Work order project setup](../setup-for-work-orders/work-order-project-setup.md) section for a description of the procedure.</span></span>

## <a name="work-order-job-projects"></a><span data-ttu-id="2d1b4-112">Työtilauksen työn projektit</span><span class="sxs-lookup"><span data-stu-id="2d1b4-112">Work order job projects</span></span>

<span data-ttu-id="2d1b4-113">Kun työtilaukseen luodaan työtilaustyö, työtilausprojekti määräytyy pääprojektin asetusten mukaan:**Resurssien hallinta** > **Asetukset** > **Työtilaukset** > **Projektiasetukset.**</span><span class="sxs-lookup"><span data-stu-id="2d1b4-113">When you create a work order job on a work order, the work order project is determined by the setup of the parent project for work orders in **Asset management** > **Setup** > **Work orders** > **Project setup**.</span></span>

<span data-ttu-id="2d1b4-114">Työtilauksen työprojektit luodaan seuraavien työtilaustietojen yhdistelmän avulla:</span><span class="sxs-lookup"><span data-stu-id="2d1b4-114">Work order job projects are created by using a combination of the following work order information:</span></span>

- <span data-ttu-id="2d1b4-115">Työtilauksessa valittu työtilaustyyppi</span><span class="sxs-lookup"><span data-stu-id="2d1b4-115">The Work order type selected on the work order</span></span> 
- <span data-ttu-id="2d1b4-116">Työtilaustyön käyttöomaisuuteen liittyvä toiminnallinen sijainti</span><span class="sxs-lookup"><span data-stu-id="2d1b4-116">The functional location related to the asset on the work order job</span></span>
- <span data-ttu-id="2d1b4-117">Työtilaustyön käyttöomaisuuteen liittyvä resurssityyppi</span><span class="sxs-lookup"><span data-stu-id="2d1b4-117">The Asset type related to the asset on the work order job</span></span>  
- <span data-ttu-id="2d1b4-118">Työtilaukseen määritetty odotettu alkamis- ja loppumisaika</span><span class="sxs-lookup"><span data-stu-id="2d1b4-118">The Expected start and end time set on the work order</span></span>  

<span data-ttu-id="2d1b4-119">On mahdollista, että kaikkia edellä mainittuja tietoja ei löydy työtilauksesta.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-119">It is possible that not all of the information mentioned above is found on a work order.</span></span> <span data-ttu-id="2d1b4-120">Näin ollen työtilauksen pääprojektin haku tehdään käyttämällä käytettävissä olevaa tietoyhdistelmää ja valitsemalla projektitunnus, joka vastaa työtilauksen tietoja.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-120">Therefore, the search for a work order parent project is done by using the available combination of data and selecting the project ID that corresponds with work order data.</span></span>

<span data-ttu-id="2d1b4-121">Esimerkki: Alla olevassa kuvassa käyttöomaisuuden tyypin "Truck Engine" määritys tarkoittaa, että jokainen kyseiselle käyttöomaisuustyypille luotu työtilaustyö on projektitunnuksen "000186" aliprojekti.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-121">Example: In the figure below, the setup of asset type "Truck Engine" means that every work order job created with that asset type will be a sub project of Project ID "000186".</span></span>

![Kuva 1](media/01-integration-to-pma.png)

<span data-ttu-id="2d1b4-123">Työtilaustyön projektitunnuksen ja siihen liittyvän tehtävän numeron (**Resurssien hallinta** > **Yhteiset** > **Työtilaukset** > **Kaikki työtilaukset** > valitse työtilaus luettelosta > **rivin tiedot** -pikavälilehti > **Projektitunnus** -kenttä **Tehtävän numero** -kenttä) tarkoitus on seurata työtilaustyöhön liittyviä kustannuksia ja työtilaustyölle valittua käyttöomaisuutta **Projektinhallinta ja kirjanpito** -moduulissa.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-123">The purpose of the project ID on the work order job, and the related activity number (**Asset management** > **Common** > **Work orders** > **All Work orders** > select work order in list > **Line details** FastTab > **Project ID** field and **Activity number** field), is to track costs related to the work order job, and the asset selected on the work order job, in the **Project management and accounting** module.</span></span> 

<span data-ttu-id="2d1b4-124">Alla olevassa kuvassa näkyy graafinen yleiskatsaus työtilausprojekteista ja niihin liittyvistä projektitehtävistä.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-124">In the figure below, you see a graphic overview of work order projects and related project activities.</span></span>

![Kuva 2](media/02-integration-to-pma.png)

<span data-ttu-id="2d1b4-126">Kun työtilaukseen luodaan uusi työtilaustyö, työtilausprojekti luodaan automaattisesti työlle.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-126">When a new work order job is created on a work order, a work order project is automatically created for the job.</span></span> <span data-ttu-id="2d1b4-127">Työtilaus työhön liittyvän käyttöomaisuuserän taloushallinnon dimensiot siirretään automaattisesti työtilausprojektiin.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-127">The financial dimensions for the asset related to the work order job are automatically transferred to the work order project.</span></span> <span data-ttu-id="2d1b4-128">Työtilaustyölle luodulle projektitehtävälle on liitetty siihen liittyviä tietoja, jotka koskevat kunnossapitotöiden tyyppiä, kunnossapitotöiden tyypin varianttia ja kauppaa.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-128">The project activity created for a work order job has related information attached to it regarding maintenance job type, maintenance job type variant, and trade.</span></span> <span data-ttu-id="2d1b4-129">Näistä tiedoista on hyötyä esimerkiksi silloin, kun luot ostotilauksen työtilauksesta ( katso [Hankinta](../work-orders/procurement.md)) tai jos käytät **Projektinhallinta ja kirjanpito** -moduulia ajan rekisteröintiä varten.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-129">Those data are useful if, for example, you create a purchase order from a work order (see [Procurement](../work-orders/procurement.md)), or if you use the **Project management and accounting** module for time registration.</span></span>  

<span data-ttu-id="2d1b4-130">Jos käyttöomaisuus on asennettu toiminnallisessa sijainnissa ja kyseinen käyttöomaisuuserä on myöhemmin asennettu toiseen toimintosijaintiin, uuteen toimintosijaintiin liittyvät taloushallinnon dimensiot päivitetään automaattisesti käyttöomaisuuserälle.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-130">If the asset was installed on a functional location, and that asset is later installed on another functional location, the financial dimensions related to the new functional location is automatically updated on the asset.</span></span> <span data-ttu-id="2d1b4-131">Kun luot käyttöomaisuudelle työtilaustyön, työtilaustyön työtilausprojekti saa automaattisesti käyttöomaisuus erään liittyvät taloushallinnon dimensiot.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-131">Subsequently, when you create a work order job for the asset, the work order project for the work order job automatically gets the financial dimensions that are now related to the asset.</span></span> <span data-ttu-id="2d1b4-132">Tämä tarkoittaa, että kun käytät toiminnallisia sijainteja, kustannuksia voidaan aina seurata niissä toiminnallisissa sijainneissa, joissa käyttöomaisuuserä on asennettuna tiettynä aikana.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-132">This means that when you use functional locations, costs can always be tracked on the functional locations on which an asset was installed at any given time.</span></span> <span data-ttu-id="2d1b4-133">Taloushallinnon dimensioiden automaattinen päivitys varmistaa projektinhallinnan ja raportoinnin kustannusten täydellisen jäljitettävyyden.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-133">The automatic update of financial dimensions ensures complete traceability of costs for project controlling and reporting.</span></span>  


## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a><span data-ttu-id="2d1b4-134">Työtilausprojektit, työtilausten elinkaaritilat, projektin vaiheet ja projektityypit</span><span class="sxs-lookup"><span data-stu-id="2d1b4-134">Work order projects, work order lifecycle states, project stages, and project types</span></span>

<span data-ttu-id="2d1b4-135">Voit varmistaa työtilausten elinkaaritilojen ja niihin liittyvien projektivaiheiden oikean käytön harkitsemalla riippuvuuksia suhteessa **Projektinhallinta ja kirjanpito** -moduuliin:</span><span class="sxs-lookup"><span data-stu-id="2d1b4-135">To ensure correct use of work order lifecycle states and related project stages on work orders, consider the dependencies in relation to the **Project management and accounting** module:</span></span>

- <span data-ttu-id="2d1b4-136">**Projektinhallinta ja kirjanpito** -moduulissa projektin vaiheet määritetään **Projektinhallinnan ja kirjanpidon parametrit** asetuksissa määritetyille projektityypeille.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-136">In the **Project management and accounting** module, project stages are set up on project types in **Project management and accounting parameters**.</span></span>  
- <span data-ttu-id="2d1b4-137">Muista **Projektinhallinnan ja kirjanpidon parametrit** -asetuksissa valita haluamasi projektivaiheen valintaruudut kaikille projektityypeille, joita aiot käyttää.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-137">In **Project management and accounting parameters**, remember to select relevant project stage check boxes for all the project types you are going to use.</span></span> <span data-ttu-id="2d1b4-138">Alla olevassa kuvassa on viisi vaihetta **Luotu** - **Arvioitu** - **Ajoitettu** - **Käynnissä** - **Valmis** valittu projektityypeille "Aika ja materiaali" sekä "Sisäinen".</span><span class="sxs-lookup"><span data-stu-id="2d1b4-138">In the figure below, five stages **Created** - **Estimated** - **Scheduled** - **In process** - **Finished** have been selected for the project types "Time and material" and "Internal".</span></span> <span data-ttu-id="2d1b4-139">Nämä viisi vaihetta koskevat sekä sisäisiä ylläpitotöitä että palveluhuoltotöitä.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-139">Those five stages are relevant for both internal maintenance and service maintenance jobs.</span></span>  
- <span data-ttu-id="2d1b4-140">**Resurssien hallinnassa** projektityypit määritetään projektiryhmien mukaan, jotka määritetään **Työtilauksen projektiasetukset** -lomakkeessa > **Projektiryhmä**-linkin kautta.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-140">In **Asset Management**, project types are defined by the project groups you set up in the **Work order project setup** form > **Project group** link.</span></span>  
- <span data-ttu-id="2d1b4-141">**Työtilauksen projektiasetukset** -asetusten projektiryhmien asetuksia käytetään luotaessa työtilauksia.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-141">The project groups setup in **Work order project setup** are used when you create work orders.</span></span> <span data-ttu-id="2d1b4-142">Kun työtilaus luodaan, työtilausprojekti luodaan automaattisesti työtilaukselle.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-142">When a work order is created, a work order project is automatically created for the work order.</span></span>  
- <span data-ttu-id="2d1b4-143">Työtilauksen elinkaaritiloilla on oltava siihen liittyvä projektivaihe.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-143">Work order lifecycle states must each have a related project stage.</span></span>  
- <span data-ttu-id="2d1b4-144">Työtilauksen elinkaaren tilaan liittyvä projektin vaihe on määritettävä työtilausprojektissa määritetyn projektiryhmän aktiiviseksi vaiheeksi.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-144">The project stage related to a work order lifecycle state must be defined as an active stage for the project group defined in the work order project.</span></span> <span data-ttu-id="2d1b4-145">Työtilausprojekti luodaan automaattisesti työtilaukseen.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-145">The work order project is automatically created on a work order.</span></span>  
- <span data-ttu-id="2d1b4-146">Kun luot uuden työtilauksen, työtilausprojektin automaattinen kohdistus perustuu **Työtilauksen projektiasetukset** -kohdan asetuksiin (**Resurssien hallinta** > **Asetukset** > **Työtilaukset** > **Projektiasetukset**).</span><span class="sxs-lookup"><span data-stu-id="2d1b4-146">When you create a new work order, the automatic allocation of a work order project is based on the setup in **Work order project setup** (**Asset management** > **Setup** > **Work orders** > **Project setup**).</span></span>  

<span data-ttu-id="2d1b4-147">Alla olevissa kuvissa näkyvät työtilauksen projektiryhmien, liittyvien projektityyppien, projektin vaiheiden ja työtilausten elinkaaritilojen väliset kytkennät.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-147">Associations between work order project groups, related project types, project stages, and work order lifecycle states are shown in the figures below.</span></span>  

![Kuva 3](media/03-integration-to-pma.png)

![Kuva 4](media/04-integration-to-pma.png)

![Kuva 5](media/05-integration-to-pma.png)

<span data-ttu-id="2d1b4-151">Katso [Työtilausprojektin asetukset](../setup-for-work-orders/work-order-project-setup.md) -kohta työtilausprojektien määrittämistä varten sekä [Työtilauksen elinkaaren tilat](../setup-for-work-orders/work-order-lifecycle-states.md) koskien työtilausten elinkaaritilojen luomista.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-151">Refer to [Work order project setup](../setup-for-work-orders/work-order-project-setup.md) regarding how to set up work order projects, and to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) regarding how to create work order lifecycle states.</span></span>

<span data-ttu-id="2d1b4-152">Alla olevassa kuvassa esitetään graafinen yleiskatsaus eri projekteista, jotka luodaan **Resurssien hallinta**- moduulissa, jotta saadaan integrointi **Projektinhallinta ja kirjanpito** -moduuliin sekä työprosessit, joihin projektit liittyvät.</span><span class="sxs-lookup"><span data-stu-id="2d1b4-152">The figure below shows a graphic overview of the various projects that are created in the **Asset management** module to allow integration with the **Project management and accounting** module, as well as the work processes to which the projects are related.</span></span>

![Kuva 6](media/06-integration-to-pma.png)

