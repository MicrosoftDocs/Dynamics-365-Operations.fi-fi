---
title: Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto
description: Tässä ohjeaiheessa kerrotaan, miten uusi sähköisen kaupankäynnin vuokraaja otetaan käyttöön Microsoft Dynamics Lifecycle Services (LCS) -palvelun avulla.
author: psimolin
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: c2632632b9b21dd3a88e9a4df0e65cfd28e579d2
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697448"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="9b599-103">Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="9b599-103">Deploy a new e-Commerce tenant</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="9b599-104">Tässä ohjeaiheessa kerrotaan, miten uusi sähköisen kaupankäynnin sivusto otetaan käyttöön Microsoft Dynamics Lifecycle Services (LCS) -palvelun avulla.</span><span class="sxs-lookup"><span data-stu-id="9b599-104">This topic describes how to deploy a new e-Commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="9b599-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="9b599-105">Overview</span></span>
    
<span data-ttu-id="9b599-106">Microsoft Dynamics Lifecycle Services (LCS) on pilvipohjainen yhteinen työtila, jossa kumppanit ja asiakkaat voivat hallita projekteja ja ympäristöjä, katsella uusimpia tietoja Microsoft Dynamics -tuotteista ja -toiminnoista sekä luoda, seurata ja selata tukitapauksia.</span><span class="sxs-lookup"><span data-stu-id="9b599-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="9b599-107">Sähköisen kaupankäynnin hallintatoiminnot integroidaan LCS:n kanssa.</span><span class="sxs-lookup"><span data-stu-id="9b599-107">E-Commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="9b599-108">Lisätietoja LCS:stä on kohdassa [Lifecycle Services -käyttöopas](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="9b599-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="9b599-109">Aloittaminen</span><span class="sxs-lookup"><span data-stu-id="9b599-109">Get started</span></span>

<span data-ttu-id="9b599-110">Ennen kuin voit alustaa sähköisen kaupankäynnin, sinun on alustettava projekti, ympäristö ja Retail Cloud Scale Unit (RCSU).</span><span class="sxs-lookup"><span data-stu-id="9b599-110">Before you can initialize e-Commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="9b599-111">Jos haluat tehdä alustuksen LCS:ssä, tarvitset joko projektin omistajan tai ympäristön valvojan roolin oikeudet.</span><span class="sxs-lookup"><span data-stu-id="9b599-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="9b599-112">Tuotanto- ja eristysympäristön topologioita tuetaan.</span><span class="sxs-lookup"><span data-stu-id="9b599-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="9b599-113">Lisätietoja ympäristöistä on kohdassa [Ympäristön suunnittelu](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="9b599-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="9b599-114">Lisätietoja RCSU:sta on kohdassa [Retail Cloud Scale Unitin alustaminen](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="9b599-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="9b599-115">Sähköisen kaupankäynnin alustaminen</span><span class="sxs-lookup"><span data-stu-id="9b599-115">Initialize e-Commerce</span></span>

<span data-ttu-id="9b599-116">Tämän menetelmän avulla voit alustaa sähköisen kaupankäynnin ominaisuuden aiemmin luodussa ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="9b599-116">Use this procedure to initialize the e-Commerce feature in an existing environment.</span></span>

<span data-ttu-id="9b599-117">Varmista ennen aloittamista, että sinulla on seuraavat pakolliset tiedot:</span><span class="sxs-lookup"><span data-stu-id="9b599-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="9b599-118">Käytettävä RCSU.</span><span class="sxs-lookup"><span data-stu-id="9b599-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="9b599-119">Microsoft Azure Active Directory -käyttöoikeusryhmä, jota sähköisen kaupankäynnin järjestelmänvalvojat käyttävät group that will be used for e-Commerce system admins.</span><span class="sxs-lookup"><span data-stu-id="9b599-119">The Microsoft Azure Active Directory security group that will be used for e-Commerce system admins.</span></span>
- <span data-ttu-id="9b599-120">Microsoft Azure Active Directory -käyttöoikeusryhmä, jota luokitusten ja arvostelujen valvojat käyttävät.</span><span class="sxs-lookup"><span data-stu-id="9b599-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="9b599-121">Toimialueet, jotka liitetään ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="9b599-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="9b599-122">Lisäksi voit kerätä seuraavat valinnaiset tiedot:</span><span class="sxs-lookup"><span data-stu-id="9b599-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="9b599-123">Azure AD:n kuluttajakaupan tiedot:</span><span class="sxs-lookup"><span data-stu-id="9b599-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="9b599-124">Vuokraajan nimi.</span><span class="sxs-lookup"><span data-stu-id="9b599-124">Tenant Name.</span></span>
    - <span data-ttu-id="9b599-125">Asiakastunnus.</span><span class="sxs-lookup"><span data-stu-id="9b599-125">Client ID.</span></span>
    - <span data-ttu-id="9b599-126">Sisäänkirjauksen mukautettu toimialue.</span><span class="sxs-lookup"><span data-stu-id="9b599-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="9b599-127">Vastauksen URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="9b599-127">Reply URL.</span></span>
    - <span data-ttu-id="9b599-128">SignUp SignIn -käytännön tunnus.</span><span class="sxs-lookup"><span data-stu-id="9b599-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="9b599-129">Salasanan nollauskäytännön tunnus.</span><span class="sxs-lookup"><span data-stu-id="9b599-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="9b599-130">Profiilin muokkauskäytännön tunnus.</span><span class="sxs-lookup"><span data-stu-id="9b599-130">Edit Profile Policy ID.</span></span>

[!NOTE]
<span data-ttu-id="9b599-131">Nämä tiedot voidaan lisätä myöhemmin palvelupyynnön avulla.</span><span class="sxs-lookup"><span data-stu-id="9b599-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="9b599-132">Kun olet kerännyt tarvittavat tiedot, alusta sähköinen kaupankäynti seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="9b599-132">After you've collected the required information, follow these steps to initialize e-Commerce.</span></span>

1. <span data-ttu-id="9b599-133">Kirjaudu sisään [LCS:ään](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="9b599-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="9b599-134">Avaa projekti, joka sisältää sen ympäristön, jossa haluat alustaa sähköisen kaupankäynnin.</span><span class="sxs-lookup"><span data-stu-id="9b599-134">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="9b599-135">Valitse **Ympäristöt**-osassa ympäristö.</span><span class="sxs-lookup"><span data-stu-id="9b599-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="9b599-136">Valitse **Ympäristön ominaisuudet** -kohdassa **Retailin hallinta** -linkki.</span><span class="sxs-lookup"><span data-stu-id="9b599-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="9b599-137">Valitse **Sähköinen kaupankäynti** -välilehdessä **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="9b599-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="9b599-138">Näyttöön tulee valintaikkuna, johon on kirjoitettava valmistelun edellyttämät tiedot.</span><span class="sxs-lookup"><span data-stu-id="9b599-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="9b599-139">Täytä tarvittavat tiedot ja siirry seuraavalle sivulle.</span><span class="sxs-lookup"><span data-stu-id="9b599-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="9b599-140">Täytä tarvittavat tiedot seuraavalla sivulla ja lähetä lomake.</span><span class="sxs-lookup"><span data-stu-id="9b599-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="9b599-141">Palaat **Sähköinen kaupankäynti** -välilehteen, jossa näet, että alustus on alkanut.</span><span class="sxs-lookup"><span data-stu-id="9b599-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="9b599-142">Jos haluat tarkastella alustuksen tilaa, valitse **Päivitä** tai palaa **Sähköinen kaupankäynti** -välilehteen myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="9b599-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="9b599-143">Kun sähköinen kaupankäynti alustetaan LCS:stä, järjestelmä valmistelee useita osia, jotka ovat pakollisia sähköisessä kaupankäynnissä, ja liittää ne ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="9b599-143">When e-Commerce is initialized from LCS, the system provisions several components that are required for e-Commerce and associates them with the environment.</span></span> <span data-ttu-id="9b599-144">Kun valmistelu on tehty, **Sähköinen kaupankäynti** -välilehti **Retail-hallinta**-sivulla päivitetään vastaamaan valmistelua.</span><span class="sxs-lookup"><span data-stu-id="9b599-144">After provisioning is completed, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="9b599-145">Sivulla näkyvät viimeisimmät mukautuksen käyttöönotot ja muiden käynnissä olevien käyttöönottojen tila.</span><span class="sxs-lookup"><span data-stu-id="9b599-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="9b599-146">Se sisältää myös linkit sähköisen kaupankäynnin sivustoon ja sähköisen kaupankäynnin sivuston hallintatyökalun (muokkaustyökalu).</span><span class="sxs-lookup"><span data-stu-id="9b599-146">It also includes links to the e-Commerce site and the e-Commerce site management tool (the authoring tool).</span></span>

## <a name="access-the-authoring-environment"></a><span data-ttu-id="9b599-147">Muokkausympäristön käyttäminen</span><span class="sxs-lookup"><span data-stu-id="9b599-147">Access the authoring environment</span></span>

<span data-ttu-id="9b599-148">Jos haluat käyttää muokkausympäristöä, siirry **Sähköinen kaupankäynti** -välilehteen **Retail-hallinta**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="9b599-148">To access the authoring environment, go to the **e-Commerce** tab on the **Retail management** page.</span></span> <span data-ttu-id="9b599-149">Sieltä löydät linkit sähköisen kaupankäynnin sivustoon ja sivuston hallintatyökaluun.</span><span class="sxs-lookup"><span data-stu-id="9b599-149">There, you will find links to your e-Commerce site and the site management tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9b599-150">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="9b599-150">Additional resources</span></span>

[<span data-ttu-id="9b599-151">Verkkokaupan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="9b599-151">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="9b599-152">Sähköisen kaupankäynnin sivuston luominen</span><span class="sxs-lookup"><span data-stu-id="9b599-152">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="9b599-153">Liitä verkkosivusto kanavaan</span><span class="sxs-lookup"><span data-stu-id="9b599-153">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="9b599-154">Toimialueen nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="9b599-154">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="9b599-155">Sisältöverkon (CDN) tuen lisääminen</span><span class="sxs-lookup"><span data-stu-id="9b599-155">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="9b599-156">Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="9b599-156">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="9b599-157">Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten</span><span class="sxs-lookup"><span data-stu-id="9b599-157">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)
