---
title: Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto
description: Tässä ohjeaiheessa kerrotaan, miten uusi sähköisen kaupankäynnin Dynamics 365 Commerce -sivusto otetaan käyttöön Microsoft Dynamics Lifecycle Services (LCS) -palvelun avulla.
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b228babfd32a4191eeed2a6d924a8b99f1a5311
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936703"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="676ac-103">Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="676ac-103">Deploy a new e-commerce tenant</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="676ac-104">Tässä ohjeaiheessa kerrotaan, miten uusi sähköisen kaupankäynnin Dynamics 365 Commerce -sivusto otetaan käyttöön Microsoft Dynamics Lifecycle Services (LCS) -palvelun avulla.</span><span class="sxs-lookup"><span data-stu-id="676ac-104">This topic describes how to deploy a new Dynamics 365 Commerce e-commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="676ac-105">Microsoft Dynamics Lifecycle Services (LCS) on pilvipohjainen yhteinen työtila, jossa kumppanit ja asiakkaat voivat hallita projekteja ja ympäristöjä, katsella uusimpia tietoja Microsoft Dynamics -tuotteista ja -toiminnoista sekä luoda, seurata ja selata tukitapauksia.</span><span class="sxs-lookup"><span data-stu-id="676ac-105">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="676ac-106">Sähköisen kaupankäynnin hallintatoiminnot integroidaan LCS:n kanssa.</span><span class="sxs-lookup"><span data-stu-id="676ac-106">E-commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="676ac-107">Lisätietoja LCS:stä on kohdassa [Lifecycle Services -käyttöopas](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="676ac-107">To learn more about LCS, see the [Lifecycle Services User Guide](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="676ac-108">Aloittaminen</span><span class="sxs-lookup"><span data-stu-id="676ac-108">Get started</span></span>

<span data-ttu-id="676ac-109">Ennen kuin voit alustaa sähköisen kaupankäynnin, sinun on alustettava projekti, ympäristö ja Retail Cloud Scale Unit (RCSU).</span><span class="sxs-lookup"><span data-stu-id="676ac-109">Before you can initialize e-commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="676ac-110">Jos haluat tehdä alustuksen LCS:ssä, tarvitset joko projektin omistajan tai ympäristön valvojan roolin oikeudet.</span><span class="sxs-lookup"><span data-stu-id="676ac-110">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="676ac-111">Tuotanto- ja eristysympäristön topologioita tuetaan.</span><span class="sxs-lookup"><span data-stu-id="676ac-111">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="676ac-112">Lisätietoja ympäristöistä on kohdassa [Ympäristön suunnittelu](/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="676ac-112">For more information about environments, see [Environment planning](/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="676ac-113">Lisätietoja RCSU:sta on kohdassa [Retail Cloud Scale Unitin alustaminen](/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="676ac-113">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="676ac-114">Sähköisen kaupankäynnin alustaminen</span><span class="sxs-lookup"><span data-stu-id="676ac-114">Initialize e-commerce</span></span>

<span data-ttu-id="676ac-115">Tämän menetelmän avulla voit alustaa sähköisen kaupankäynnin ominaisuuden aiemmin luodussa ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="676ac-115">Use this procedure to initialize the e-commerce feature in an existing environment.</span></span>

<span data-ttu-id="676ac-116">Varmista ennen aloittamista, että sinulla on seuraavat pakolliset tiedot:</span><span class="sxs-lookup"><span data-stu-id="676ac-116">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="676ac-117">Käytettävä RCSU.</span><span class="sxs-lookup"><span data-stu-id="676ac-117">The RCSU that will be used.</span></span>
- <span data-ttu-id="676ac-118">Microsoft Azure Active Directory -käyttöoikeusryhmä, jota sähköisen kaupankäynnin järjestelmänvalvojat käyttävät group that will be used for e-Commerce system admins.</span><span class="sxs-lookup"><span data-stu-id="676ac-118">The Microsoft Azure Active Directory security group that will be used for e-commerce system admins.</span></span>
- <span data-ttu-id="676ac-119">Microsoft Azure Active Directory -käyttöoikeusryhmä, jota luokitusten ja arvostelujen valvojat käyttävät.</span><span class="sxs-lookup"><span data-stu-id="676ac-119">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="676ac-120">Toimialueet, jotka liitetään ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="676ac-120">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="676ac-121">Lisäksi voit kerätä seuraavat valinnaiset tiedot:</span><span class="sxs-lookup"><span data-stu-id="676ac-121">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="676ac-122">Azure AD:n kuluttajakaupan tiedot:</span><span class="sxs-lookup"><span data-stu-id="676ac-122">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="676ac-123">Vuokraajan nimi.</span><span class="sxs-lookup"><span data-stu-id="676ac-123">Tenant Name.</span></span>
    - <span data-ttu-id="676ac-124">Asiakastunnus.</span><span class="sxs-lookup"><span data-stu-id="676ac-124">Client ID.</span></span>
    - <span data-ttu-id="676ac-125">Sisäänkirjauksen mukautettu toimialue.</span><span class="sxs-lookup"><span data-stu-id="676ac-125">Login Custom Domain.</span></span>
    - <span data-ttu-id="676ac-126">Vastauksen URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="676ac-126">Reply URL.</span></span>
    - <span data-ttu-id="676ac-127">SignUp SignIn -käytännön tunnus.</span><span class="sxs-lookup"><span data-stu-id="676ac-127">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="676ac-128">Salasanan nollauskäytännön tunnus.</span><span class="sxs-lookup"><span data-stu-id="676ac-128">Reset password Policy ID.</span></span>
    - <span data-ttu-id="676ac-129">Profiilin muokkauskäytännön tunnus.</span><span class="sxs-lookup"><span data-stu-id="676ac-129">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="676ac-130">Nämä tiedot voidaan lisätä myöhemmin palvelupyynnön avulla.</span><span class="sxs-lookup"><span data-stu-id="676ac-130">This information can be added later, through a service request.</span></span>

<span data-ttu-id="676ac-131">Kun olet kerännyt tarvittavat tiedot, alusta sähköinen kaupankäynti seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="676ac-131">After you've collected the required information, follow these steps to initialize e-commerce.</span></span>

1. <span data-ttu-id="676ac-132">Kirjaudu sisään [LCS:ään](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="676ac-132">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="676ac-133">Avaa projekti, joka sisältää sen ympäristön, jossa haluat alustaa sähköisen kaupankäynnin.</span><span class="sxs-lookup"><span data-stu-id="676ac-133">Open the project that contains the environment where you want to initialize e-commerce.</span></span>
1. <span data-ttu-id="676ac-134">Valitse **Ympäristöt**-osassa ympäristö.</span><span class="sxs-lookup"><span data-stu-id="676ac-134">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="676ac-135">Valitse **Ympäristön ominaisuudet** -kohdassa **Retailin hallinta** -linkki.</span><span class="sxs-lookup"><span data-stu-id="676ac-135">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="676ac-136">Valitse **Sähköinen kaupankäynti** -välilehdessä **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="676ac-136">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="676ac-137">Näyttöön tulee valintaikkuna, johon on kirjoitettava valmistelun edellyttämät tiedot.</span><span class="sxs-lookup"><span data-stu-id="676ac-137">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="676ac-138">Täytä tarvittavat tiedot ja siirry seuraavalle sivulle.</span><span class="sxs-lookup"><span data-stu-id="676ac-138">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="676ac-139">Täytä tarvittavat tiedot seuraavalla sivulla ja lähetä lomake.</span><span class="sxs-lookup"><span data-stu-id="676ac-139">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="676ac-140">Palaat **Sähköinen kaupankäynti** -välilehteen, jossa näet, että alustus on alkanut.</span><span class="sxs-lookup"><span data-stu-id="676ac-140">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="676ac-141">Jos haluat tarkastella alustuksen tilaa, valitse **Päivitä** tai palaa **Sähköinen kaupankäynti** -välilehteen myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="676ac-141">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="676ac-142">Kun sähköinen kaupankäynti alustetaan LCS:stä, järjestelmä valmistelee useita osia, jotka ovat pakollisia sähköisessä kaupankäynnissä, ja liittää ne ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="676ac-142">When e-commerce is initialized from LCS, the system provisions several components that are required for e-commerce and associates them with the environment.</span></span> <span data-ttu-id="676ac-143">Kun valmistelu on tehty, **Sähköinen kaupankäynti** -välilehti **Retail-hallinta**-sivulla päivitetään vastaamaan valmistelua.</span><span class="sxs-lookup"><span data-stu-id="676ac-143">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="676ac-144">Sivulla näkyvät viimeisimmät mukautuksen käyttöönotot ja muiden käynnissä olevien käyttöönottojen tila.</span><span class="sxs-lookup"><span data-stu-id="676ac-144">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="676ac-145">Se sisältää myös linkit sähköisen kaupankäynnin sivustoon ja sähköisen kaupankäynnin sivustomuodostinsivulle, jolla sivut luodaan.</span><span class="sxs-lookup"><span data-stu-id="676ac-145">It also includes links to the e-commerce site and the Commerce site builder where sites are authored.</span></span>

## <a name="access-commerce-site-builder"></a><span data-ttu-id="676ac-146">Commerce-sivuston muodostimen käyttö</span><span class="sxs-lookup"><span data-stu-id="676ac-146">Access Commerce site builder</span></span>

<span data-ttu-id="676ac-147">Kun haluat käyttää Commerce-sivuston muodostinta, siirry **Sähköinen kaupankäynti**-välilehteen LCS:n **Vähittäismyynnin hallinta** -sivu ja valitse **Sähköisen kaupankäynnin hallintatyökalu** -linkki.</span><span class="sxs-lookup"><span data-stu-id="676ac-147">To access Commerce site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="676ac-148">Sivustonmuodostimen aloitussivulla näkyy vuokraajatason näkymä.</span><span class="sxs-lookup"><span data-stu-id="676ac-148">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="676ac-149">Tällä sivulla voit:</span><span class="sxs-lookup"><span data-stu-id="676ac-149">From this page, you can:</span></span>

- <span data-ttu-id="676ac-150">Muokata vuokraajatason asetuksia.</span><span class="sxs-lookup"><span data-stu-id="676ac-150">Modify tenant-level settings.</span></span>
- <span data-ttu-id="676ac-151">Siirry mille tahansa luomallesi sivustolle katseluoikeuksilla.</span><span class="sxs-lookup"><span data-stu-id="676ac-151">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="676ac-152">Käytä tarkistustoimintoja, kuten arviointia ja raportointia.</span><span class="sxs-lookup"><span data-stu-id="676ac-152">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="676ac-153">Luo uusi sivusto.</span><span class="sxs-lookup"><span data-stu-id="676ac-153">Create a new site.</span></span> <span data-ttu-id="676ac-154">Lisätietoja uuden sivuston luomisesta ja käyttöönotosta on kohdassa [Luo sähköisen kaupankäynnin sivusto](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="676ac-154">For more information about how to create a new site, see [Create an e-commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="676ac-155">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="676ac-155">Additional resources</span></span>

[<span data-ttu-id="676ac-156">Toimialueen nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="676ac-156">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="676ac-157">Sähköisen kaupankäynnin sivuston luominen</span><span class="sxs-lookup"><span data-stu-id="676ac-157">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="676ac-158">Dynamics 365 Commerce -sivuston liittäminen online-kanavaan</span><span class="sxs-lookup"><span data-stu-id="676ac-158">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="676ac-159">Robots.txt-tiedostojen hallinta</span><span class="sxs-lookup"><span data-stu-id="676ac-159">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="676ac-160">URL-uudelleenohjausten joukkolataus palveluun</span><span class="sxs-lookup"><span data-stu-id="676ac-160">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="676ac-161">B2C-vuokraajan määrittäminen Commercessa</span><span class="sxs-lookup"><span data-stu-id="676ac-161">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="676ac-162">Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten</span><span class="sxs-lookup"><span data-stu-id="676ac-162">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="676ac-163">Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä</span><span class="sxs-lookup"><span data-stu-id="676ac-163">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="676ac-164">Sisältöverkon (CDN) tuen lisääminen</span><span class="sxs-lookup"><span data-stu-id="676ac-164">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="676ac-165">Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="676ac-165">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]