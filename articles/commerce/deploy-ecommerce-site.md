---
title: Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto
description: Tässä ohjeaiheessa kerrotaan, miten uusi sähköisen kaupankäynnin Dynamics 365 Commerce -sivusto otetaan käyttöön Microsoft Dynamics Lifecycle Services (LCS) -palvelun avulla.
author: psimolin
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 157dc8225e5bbf9338a1b5a79a2880e8a8c4bf10
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517279"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="7ba96-103">Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="7ba96-103">Deploy a new e-commerce tenant</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7ba96-104">Tässä ohjeaiheessa kerrotaan, miten uusi sähköisen kaupankäynnin Dynamics 365 Commerce -sivusto otetaan käyttöön Microsoft Dynamics Lifecycle Services (LCS) -palvelun avulla.</span><span class="sxs-lookup"><span data-stu-id="7ba96-104">This topic describes how to deploy a new Dynamics 365 Commerce e-commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="7ba96-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="7ba96-105">Overview</span></span>

<span data-ttu-id="7ba96-106">Microsoft Dynamics Lifecycle Services (LCS) on pilvipohjainen yhteinen työtila, jossa kumppanit ja asiakkaat voivat hallita projekteja ja ympäristöjä, katsella uusimpia tietoja Microsoft Dynamics -tuotteista ja -toiminnoista sekä luoda, seurata ja selata tukitapauksia.</span><span class="sxs-lookup"><span data-stu-id="7ba96-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="7ba96-107">Sähköisen kaupankäynnin hallintatoiminnot integroidaan LCS:n kanssa.</span><span class="sxs-lookup"><span data-stu-id="7ba96-107">E-commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="7ba96-108">Lisätietoja LCS:stä on kohdassa [Lifecycle Services -käyttöopas](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="7ba96-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="7ba96-109">Aloittaminen</span><span class="sxs-lookup"><span data-stu-id="7ba96-109">Get started</span></span>

<span data-ttu-id="7ba96-110">Ennen kuin voit alustaa sähköisen kaupankäynnin, sinun on alustettava projekti, ympäristö ja Retail Cloud Scale Unit (RCSU).</span><span class="sxs-lookup"><span data-stu-id="7ba96-110">Before you can initialize e-commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="7ba96-111">Jos haluat tehdä alustuksen LCS:ssä, tarvitset joko projektin omistajan tai ympäristön valvojan roolin oikeudet.</span><span class="sxs-lookup"><span data-stu-id="7ba96-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="7ba96-112">Tuotanto- ja eristysympäristön topologioita tuetaan.</span><span class="sxs-lookup"><span data-stu-id="7ba96-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="7ba96-113">Lisätietoja ympäristöistä on kohdassa [Ympäristön suunnittelu](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="7ba96-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="7ba96-114">Lisätietoja RCSU:sta on kohdassa [Retail Cloud Scale Unitin alustaminen](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="7ba96-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="7ba96-115">Sähköisen kaupankäynnin alustaminen</span><span class="sxs-lookup"><span data-stu-id="7ba96-115">Initialize e-commerce</span></span>

<span data-ttu-id="7ba96-116">Tämän menetelmän avulla voit alustaa sähköisen kaupankäynnin ominaisuuden aiemmin luodussa ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="7ba96-116">Use this procedure to initialize the e-commerce feature in an existing environment.</span></span>

<span data-ttu-id="7ba96-117">Varmista ennen aloittamista, että sinulla on seuraavat pakolliset tiedot:</span><span class="sxs-lookup"><span data-stu-id="7ba96-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="7ba96-118">Käytettävä RCSU.</span><span class="sxs-lookup"><span data-stu-id="7ba96-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="7ba96-119">Microsoft Azure Active Directory -käyttöoikeusryhmä, jota sähköisen kaupankäynnin järjestelmänvalvojat käyttävät group that will be used for e-Commerce system admins.</span><span class="sxs-lookup"><span data-stu-id="7ba96-119">The Microsoft Azure Active Directory security group that will be used for e-commerce system admins.</span></span>
- <span data-ttu-id="7ba96-120">Microsoft Azure Active Directory -käyttöoikeusryhmä, jota luokitusten ja arvostelujen valvojat käyttävät.</span><span class="sxs-lookup"><span data-stu-id="7ba96-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="7ba96-121">Toimialueet, jotka liitetään ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="7ba96-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="7ba96-122">Lisäksi voit kerätä seuraavat valinnaiset tiedot:</span><span class="sxs-lookup"><span data-stu-id="7ba96-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="7ba96-123">Azure AD:n kuluttajakaupan tiedot:</span><span class="sxs-lookup"><span data-stu-id="7ba96-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="7ba96-124">Vuokraajan nimi.</span><span class="sxs-lookup"><span data-stu-id="7ba96-124">Tenant Name.</span></span>
    - <span data-ttu-id="7ba96-125">Asiakastunnus.</span><span class="sxs-lookup"><span data-stu-id="7ba96-125">Client ID.</span></span>
    - <span data-ttu-id="7ba96-126">Sisäänkirjauksen mukautettu toimialue.</span><span class="sxs-lookup"><span data-stu-id="7ba96-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="7ba96-127">Vastauksen URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="7ba96-127">Reply URL.</span></span>
    - <span data-ttu-id="7ba96-128">SignUp SignIn -käytännön tunnus.</span><span class="sxs-lookup"><span data-stu-id="7ba96-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="7ba96-129">Salasanan nollauskäytännön tunnus.</span><span class="sxs-lookup"><span data-stu-id="7ba96-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="7ba96-130">Profiilin muokkauskäytännön tunnus.</span><span class="sxs-lookup"><span data-stu-id="7ba96-130">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="7ba96-131">Nämä tiedot voidaan lisätä myöhemmin palvelupyynnön avulla.</span><span class="sxs-lookup"><span data-stu-id="7ba96-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="7ba96-132">Kun olet kerännyt tarvittavat tiedot, alusta sähköinen kaupankäynti seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="7ba96-132">After you've collected the required information, follow these steps to initialize e-commerce.</span></span>

1. <span data-ttu-id="7ba96-133">Kirjaudu sisään [LCS:ään](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="7ba96-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="7ba96-134">Avaa projekti, joka sisältää sen ympäristön, jossa haluat alustaa sähköisen kaupankäynnin.</span><span class="sxs-lookup"><span data-stu-id="7ba96-134">Open the project that contains the environment where you want to initialize e-commerce.</span></span>
1. <span data-ttu-id="7ba96-135">Valitse **Ympäristöt**-osassa ympäristö.</span><span class="sxs-lookup"><span data-stu-id="7ba96-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="7ba96-136">Valitse **Ympäristön ominaisuudet** -kohdassa **Retailin hallinta** -linkki.</span><span class="sxs-lookup"><span data-stu-id="7ba96-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="7ba96-137">Valitse **Sähköinen kaupankäynti** -välilehdessä **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="7ba96-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="7ba96-138">Näyttöön tulee valintaikkuna, johon on kirjoitettava valmistelun edellyttämät tiedot.</span><span class="sxs-lookup"><span data-stu-id="7ba96-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="7ba96-139">Täytä tarvittavat tiedot ja siirry seuraavalle sivulle.</span><span class="sxs-lookup"><span data-stu-id="7ba96-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="7ba96-140">Täytä tarvittavat tiedot seuraavalla sivulla ja lähetä lomake.</span><span class="sxs-lookup"><span data-stu-id="7ba96-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="7ba96-141">Palaat **Sähköinen kaupankäynti** -välilehteen, jossa näet, että alustus on alkanut.</span><span class="sxs-lookup"><span data-stu-id="7ba96-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="7ba96-142">Jos haluat tarkastella alustuksen tilaa, valitse **Päivitä** tai palaa **Sähköinen kaupankäynti** -välilehteen myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="7ba96-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="7ba96-143">Kun sähköinen kaupankäynti alustetaan LCS:stä, järjestelmä valmistelee useita osia, jotka ovat pakollisia sähköisessä kaupankäynnissä, ja liittää ne ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="7ba96-143">When e-commerce is initialized from LCS, the system provisions several components that are required for e-commerce and associates them with the environment.</span></span> <span data-ttu-id="7ba96-144">Kun valmistelu on tehty, **Sähköinen kaupankäynti** -välilehti **Retail-hallinta**-sivulla päivitetään vastaamaan valmistelua.</span><span class="sxs-lookup"><span data-stu-id="7ba96-144">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="7ba96-145">Sivulla näkyvät viimeisimmät mukautuksen käyttöönotot ja muiden käynnissä olevien käyttöönottojen tila.</span><span class="sxs-lookup"><span data-stu-id="7ba96-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="7ba96-146">Se sisältää myös linkit sähköisen kaupankäynnin sivustoon ja sähköisen kaupankäynnin sivustomuodostinsivulle, jolla sivut luodaan.</span><span class="sxs-lookup"><span data-stu-id="7ba96-146">It also includes links to the e-commerce site and the Commerce site builder where sites are authored.</span></span>

## <a name="access-commerce-site-builder"></a><span data-ttu-id="7ba96-147">Commerce-sivuston muodostimen käyttö</span><span class="sxs-lookup"><span data-stu-id="7ba96-147">Access Commerce site builder</span></span>

<span data-ttu-id="7ba96-148">Kun haluat käyttää Commerce-sivuston muodostinta, siirry **Sähköinen kaupankäynti**-välilehteen LCS:n **Vähittäismyynnin hallinta** -sivu ja valitse **Sähköisen kaupankäynnin hallintatyökalu** -linkki.</span><span class="sxs-lookup"><span data-stu-id="7ba96-148">To access Commerce site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="7ba96-149">Sivustonmuodostimen aloitussivulla näkyy vuokraajatason näkymä.</span><span class="sxs-lookup"><span data-stu-id="7ba96-149">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="7ba96-150">Tällä sivulla voit:</span><span class="sxs-lookup"><span data-stu-id="7ba96-150">From this page, you can:</span></span>

- <span data-ttu-id="7ba96-151">Muokata vuokraajatason asetuksia.</span><span class="sxs-lookup"><span data-stu-id="7ba96-151">Modify tenant-level settings.</span></span>
- <span data-ttu-id="7ba96-152">Siirry mille tahansa luomallesi sivustolle katseluoikeuksilla.</span><span class="sxs-lookup"><span data-stu-id="7ba96-152">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="7ba96-153">Käytä tarkistustoimintoja, kuten arviointia ja raportointia.</span><span class="sxs-lookup"><span data-stu-id="7ba96-153">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="7ba96-154">Luo uusi sivusto.</span><span class="sxs-lookup"><span data-stu-id="7ba96-154">Create a new site.</span></span> <span data-ttu-id="7ba96-155">Lisätietoja uuden sivuston luomisesta ja käyttöönotosta on kohdassa [Luo sähköisen kaupankäynnin sivusto](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="7ba96-155">For more information about how to create a new site, see [Create an e-commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="7ba96-156">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="7ba96-156">Additional resources</span></span>

[<span data-ttu-id="7ba96-157">Toimialueen nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7ba96-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="7ba96-158">Sähköisen kaupankäynnin sivuston luominen</span><span class="sxs-lookup"><span data-stu-id="7ba96-158">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="7ba96-159">Dynamics 365 Commerce -sivuston liittäminen online-kanavaan</span><span class="sxs-lookup"><span data-stu-id="7ba96-159">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="7ba96-160">Robots.txt-tiedostojen hallinta</span><span class="sxs-lookup"><span data-stu-id="7ba96-160">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="7ba96-161">URL-uudelleenohjausten joukkolataus palveluun</span><span class="sxs-lookup"><span data-stu-id="7ba96-161">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="7ba96-162">B2C-vuokraajan määrittäminen Commercessa</span><span class="sxs-lookup"><span data-stu-id="7ba96-162">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="7ba96-163">Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten</span><span class="sxs-lookup"><span data-stu-id="7ba96-163">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="7ba96-164">Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä</span><span class="sxs-lookup"><span data-stu-id="7ba96-164">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="7ba96-165">Sisältöverkon (CDN) tuen lisääminen</span><span class="sxs-lookup"><span data-stu-id="7ba96-165">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="7ba96-166">Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="7ba96-166">Enable location-based store detection</span></span>](enable-store-detection.md)
