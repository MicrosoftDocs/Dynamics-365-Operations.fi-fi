---
title: Dynamics 365 Commercen esiversioympäristön valmistelu
description: Tässä ohjeaiheessa kerrotaan, kuinka voit valmistella Microsoft Dynamics 365 Commercen esikatseluympäristön.
author: psimolin
manager: annbe
ms.date: 04/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d54db89372a0f9ef5b267d25e14067e3243a803c
ms.sourcegitcommit: 4254acb3cf8c6299fc2f3818ea6c499f058320d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/09/2020
ms.locfileid: "3254745"
---
# <a name="provision-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="b13f0-103">Dynamics 365 Commercen esiversioympäristön valmistelu</span><span class="sxs-lookup"><span data-stu-id="b13f0-103">Provision a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b13f0-104">Tässä ohjeaiheessa kerrotaan, kuinka voit valmistella Dynamics 365 Commercen esikatseluympäristön.</span><span class="sxs-lookup"><span data-stu-id="b13f0-104">This topic explains how to provision a Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="b13f0-105">Ennen kuin aloitat, suosittelemme, että tarkistat tämän aiheen nopeasti, jotta saat käsityksen prosessin vaatimista aiheista.</span><span class="sxs-lookup"><span data-stu-id="b13f0-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="b13f0-106">Jos sinulle ei ole vielä myönnetty Dynamics 365 Commerce Preview -sovelluksen käyttöoikeutta, voit pyytää esiversion käyttöoikeuden [Dynamics 365 Commerce -sivuston avulla](https://aka.ms/Dynamics365CommerceWebsite).</span><span class="sxs-lookup"><span data-stu-id="b13f0-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Dynamics 365 Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="b13f0-107">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="b13f0-107">Overview</span></span>

<span data-ttu-id="b13f0-108">Jotta voit laatia Commerce Preview -ympäristön onnistuneesti, sinun on luotava projekti, jolla on tietty tuotteen nimi ja tyyppi.</span><span class="sxs-lookup"><span data-stu-id="b13f0-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="b13f0-109">Ympäristöllä ja commerce scale unit (CSU) -ratkaisulla on myös joitakin tiettyjä parametreja, joita on käytettävä, kun myöhemmin valmistelet sähköistä kaupankäyntiä.</span><span class="sxs-lookup"><span data-stu-id="b13f0-109">The environment and commerce scale unit (CSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="b13f0-110">Tämän ohjeaiheen ohjeissa kuvataan kaikki tarvittavat vaiheet käyttöönoton suorittamiseksi ja parametrit, joita sinun on käytettävä.</span><span class="sxs-lookup"><span data-stu-id="b13f0-110">The instructions in this topic describe all the steps required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="b13f0-111">Kun olet onnistuneesti valmistellut Commercen esikatseluympäristön, sinun on suoritettava muutama valmistelun jälkeinen vaihe sen valmistelemiseksi.</span><span class="sxs-lookup"><span data-stu-id="b13f0-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="b13f0-112">Jotkin vaiheet ovat valinnaisia. Tämä riippuu siitä, mitä järjestelmän alueita haluat arvioida.</span><span class="sxs-lookup"><span data-stu-id="b13f0-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="b13f0-113">Voit aina suorittaa valinnaiset vaiheet myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="b13f0-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="b13f0-114">Katso lisätietoja Commercen esikatseluympäristön määrittelystä kohdasta sen jälkeen, kun olet valmistellut sen [Commercen esikatseluympäristön määrittäminen](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="b13f0-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="b13f0-115">Jos haluat lisätietoja valinnaisten ominaisuuksien määrittämisestä Commercen esikatseluympäristöön, katso [Lisäominaisuuksien määrittäminen Commercen esikatseluympäristöä varten](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="b13f0-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="b13f0-116">Jos haluat lisätietoja valmistelun vaiheista tai jos kohtaat ongelmia, kerro se Microsoftille [Microsoft Dynamics 365 Commerce Preview Yammer -ryhmän](https://aka.ms/Dynamics365CommercePreviewYammer) kautta.</span><span class="sxs-lookup"><span data-stu-id="b13f0-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b13f0-117">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="b13f0-117">Prerequisites</span></span>

<span data-ttu-id="b13f0-118">Seuraavien edellytysten on oltava käytössä, ennen kuin voit määrittää Commerce Preview -ympäristön:</span><span class="sxs-lookup"><span data-stu-id="b13f0-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="b13f0-119">Sinulla on Microsoft Dynamics Lifecycle Services -portaalin (LCS) käyttöoikeus</span><span class="sxs-lookup"><span data-stu-id="b13f0-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="b13f0-120">Olet aiemmin luotu Microsoft Dynamics 365 -kumppani tai -asiakas ja pystyt luomaan Dynamics 365 Commerce -projektin.</span><span class="sxs-lookup"><span data-stu-id="b13f0-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="b13f0-121">Sinut on hyväksytty Dynamics 365 Commerce Preview -ohjelmaan.</span><span class="sxs-lookup"><span data-stu-id="b13f0-121">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="b13f0-122">Sinulla on projektin luomisessa vaaditut **Siirrä, luo ratkaisuja ja opi** -kohtien oikeudet.</span><span class="sxs-lookup"><span data-stu-id="b13f0-122">You have the required permissions to create a project for **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="b13f0-123">Olet **Ympäristövastaava**- tai **Projektin omistaja** -roolin jäsen projektissa, jolle valmistelet ympäristöä.</span><span class="sxs-lookup"><span data-stu-id="b13f0-123">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="b13f0-124">Sinulla on järjestelmänvalvojan oikeudet Microsoft Azure -tilausta varten, tai ota yhteyttä tilauksen järjestelmänvalvojaan, joka voi suorittaa puolestasi järjestelmänvalvojan oikeudet vaativat kaksi vaihetta.</span><span class="sxs-lookup"><span data-stu-id="b13f0-124">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="b13f0-125">Sinulla on käytettävissä Azure Active Directory (Azure AD) -vuokralaisen tunnus.</span><span class="sxs-lookup"><span data-stu-id="b13f0-125">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="b13f0-126">Olet luonut Azure AD -käyttöoikeusryhmän, jota voidaan käyttää sähköisen kaupankäynnin järjestelmänvalvojien ryhmänä, ja sinulla on ryhmän tunnus.</span><span class="sxs-lookup"><span data-stu-id="b13f0-126">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="b13f0-127">Olet luonut Azure AD -käyttöoikeusryhmän, jota voidaan käyttää arviot ja arvostelut -moderaattorien ryhmänä, ja sinulla on ryhmän tunnus.</span><span class="sxs-lookup"><span data-stu-id="b13f0-127">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="b13f0-128">(Tämä suojausryhmä voi olla sama kuin verkkokauppajärjestelmän järjestelmänvalvojaryhmä.)</span><span class="sxs-lookup"><span data-stu-id="b13f0-128">(This security group can be the same as the e-Commerce system admin group.)</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="b13f0-129">Commercen esikatseluympäristön valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="b13f0-129">Provision your Commerce preview environment</span></span>

<span data-ttu-id="b13f0-130">Näissä ohjeissa kerrotaan, miten Commerce Preview -ympäristö tarjotaan.</span><span class="sxs-lookup"><span data-stu-id="b13f0-130">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="b13f0-131">Kun olet suorittanut ne onnistuneesti, Commerce Preview -ympäristö on valmiina konfigurointia varten.</span><span class="sxs-lookup"><span data-stu-id="b13f0-131">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="b13f0-132">Kaikki tässä kuvatut toiminnot tapahtuvat LCS-portaalissa.</span><span class="sxs-lookup"><span data-stu-id="b13f0-132">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b13f0-133">Esikatselun käyttö on sidottu Commerce-esikatselusovelluksessa määrittämääsi LCS-tiliin ja organisaatioon.</span><span class="sxs-lookup"><span data-stu-id="b13f0-133">Preview access is tied to the LCS account and organization that you specified in your Commerce preview application.</span></span> <span data-ttu-id="b13f0-134">Sinun on käytettävä samaa tiliä Commerce Preview -ympäristön tarjoamiseen.</span><span class="sxs-lookup"><span data-stu-id="b13f0-134">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="b13f0-135">Jos sinun täytyy käyttää Commerce Preview -ympäristössä eri LCS-tiliä tai -vuokraajaa, sinun on annettava kyseiset tiedot Microsoftille.</span><span class="sxs-lookup"><span data-stu-id="b13f0-135">If you need to use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="b13f0-136">Yhteystiedot ovat jäljempänä tämän ohjeaiheen [ Commerce Preview -ympäristön tuki](#commerce-preview-environment-support) -osiossa.</span><span class="sxs-lookup"><span data-stu-id="b13f0-136">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="b13f0-137">Tarkista, että esiversio-ominaisuudet ovat käytettävissä ja että ne on otettu käyttöön LCS:ssä</span><span class="sxs-lookup"><span data-stu-id="b13f0-137">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="b13f0-138">Toimi seuraavasti tarkistaaksesi, että esiversio-ominaisuudet ovat käytettävissä ja että ne on otettu käyttöön LCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="b13f0-138">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="b13f0-139">Kirjaudu sisään [LCS-portaaliin](https://lcs.dynamics.com) käyttämällä samaa LCS-tiliä, jota käytit pyytämällä esikatselun käyttöoikeutta.</span><span class="sxs-lookup"><span data-stu-id="b13f0-139">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="b13f0-140">Vieritä LCS:n kotisivua oikeaan reunaan ja valitse **Esiversio-ominaisuuksien hallinta** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="b13f0-140">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![Esiversion hallinta -ruutu](./media/preview1.png)

1. <span data-ttu-id="b13f0-142">Vieritä **Yksityisen esiversion ominaisuudet** -kohtaan ja vahvista, että seuraavat ominaisuudet ovat käytettävissä ja että ne on otettu käyttöön:</span><span class="sxs-lookup"><span data-stu-id="b13f0-142">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="b13f0-143">Sähköisen kaupankäynnin arviointi</span><span class="sxs-lookup"><span data-stu-id="b13f0-143">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="b13f0-144">Commerce Preview -ohjelman ympäristöt</span><span class="sxs-lookup"><span data-stu-id="b13f0-144">Commerce Preview Program Environments</span></span>

    ![Yksityisen esiversion ominaisuudet](./media/preview2.png)

1. <span data-ttu-id="b13f0-146">Jos nämä ominaisuudet eivät näy luettelossa, ota yhteyttä Microsoftiin ja anna työsähköpostiosoitteesi, LCS-tilisi ja vuokralaisen tiedot.</span><span class="sxs-lookup"><span data-stu-id="b13f0-146">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="b13f0-147">Yhteystiedot löydät [ Commerce Preview -ympäristön tuki](#commerce-preview-environment-support) -osiosta.</span><span class="sxs-lookup"><span data-stu-id="b13f0-147">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="b13f0-148">Luo uusi projekti</span><span class="sxs-lookup"><span data-stu-id="b13f0-148">Create a new project</span></span>

<span data-ttu-id="b13f0-149">Noudata seuraavia vaiheita luodaksesi uuden projektin LCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="b13f0-149">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="b13f0-150">Luo projekti valitsemalla LCS-aloitussivulla plusmerkki (**+**).</span><span class="sxs-lookup"><span data-stu-id="b13f0-150">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="b13f0-151">Noudata oikeanpuoleisessa ruudussa jotakin näistä vaiheista:</span><span class="sxs-lookup"><span data-stu-id="b13f0-151">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="b13f0-152">Jos olet kumppani, valitse **Siirrä, luo ratkaisuja ja opi**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-152">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="b13f0-153">Jos olet asiakas, valitse **Mahdolliset myyntiä edeltävät toimet**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-153">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="b13f0-154">Syötä mallin nimi, kuvaus ja toimiala.</span><span class="sxs-lookup"><span data-stu-id="b13f0-154">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="b13f0-155">Valitse **Tuotenimi** -kentässä **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-155">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="b13f0-156">Valitse **Tuoteversio**-kentässä **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-156">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="b13f0-157">Valitse **Metodologia**-kentässä **Dynamics Retail -implementointimetodologia**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-157">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="b13f0-158">Valinnainen: Voit tuoda rooleja ja käyttäjiä aiemmin luodusta projektista.</span><span class="sxs-lookup"><span data-stu-id="b13f0-158">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="b13f0-159">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-159">Select **Create**.</span></span> <span data-ttu-id="b13f0-160">Projektinäkymä avautuu.</span><span class="sxs-lookup"><span data-stu-id="b13f0-160">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="b13f0-161">Azure-yhdistimen lisääminen</span><span class="sxs-lookup"><span data-stu-id="b13f0-161">Add the Azure Connector</span></span>

<span data-ttu-id="b13f0-162">Voit lisätä Azure-yhdistin LCS-projektiin noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="b13f0-162">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="b13f0-163">Noudata seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="b13f0-163">Follow one of these steps:</span></span>

    - <span data-ttu-id="b13f0-164">Jos olet kumppani, valitse **Projektin asetukset** -ruutu oikeassa reunassa.</span><span class="sxs-lookup"><span data-stu-id="b13f0-164">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="b13f0-165">Jos olet asiakas, valitse ylävalikosta **Projektin asetukset**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-165">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="b13f0-166">Valitse **Azure-yhdistimet**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-166">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="b13f0-167">Lisää Azure-yhdistin valitsemalla**Lisää**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-167">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="b13f0-168">Kirjoita nimi.</span><span class="sxs-lookup"><span data-stu-id="b13f0-168">Enter a name.</span></span>
1. <span data-ttu-id="b13f0-169">Anna Azure-tilauksen tunnus.</span><span class="sxs-lookup"><span data-stu-id="b13f0-169">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="b13f0-170">Ota **Määritä Azuren resurssienhallinta (ARM)** -valinta käyttöön.</span><span class="sxs-lookup"><span data-stu-id="b13f0-170">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="b13f0-171">Varmista, että **Azure-tilauksen AAD-vuokraajan toimialue (tai tunnus)** -arvo on määritetty oikein.</span><span class="sxs-lookup"><span data-stu-id="b13f0-171">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="b13f0-172">Ota tarvittaessa yhteys Azure-tilauksen järjestelmänvalvojaan.</span><span class="sxs-lookup"><span data-stu-id="b13f0-172">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="b13f0-173">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-173">Select **Next**.</span></span>
1. <span data-ttu-id="b13f0-174">Noudata sivulle tulevia ohjeita ja myönnä tilaukselle tarvittavien sovellusten käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="b13f0-174">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="b13f0-175">Ota tarvittaessa yhteys Azure-tilauksen järjestelmänvalvojaan.</span><span class="sxs-lookup"><span data-stu-id="b13f0-175">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="b13f0-176">Kirjaudu [Azure-portaalin osoitteessa](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="b13f0-176">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="b13f0-177">Varmista, että oikea hakemisto on valittuna, ja valitse sitten vasemmalla olevasta valikosta **Tilaukset**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-177">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="b13f0-178">Etsi oikea tilaus luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="b13f0-178">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="b13f0-179">Käytä hakutoimintoa tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="b13f0-179">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="b13f0-180">Valitse valikosta **Käytön valvonta (IAM)**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-180">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="b13f0-181">Valitse **Lisää** oikealla olevassa **Lisää roolin määritys** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="b13f0-181">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="b13f0-182">**Lisää roolin määritys** -ruutu avautuu.</span><span class="sxs-lookup"><span data-stu-id="b13f0-182">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="b13f0-183">Valitse **Rooli**-kentästä **Osallistuja**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-183">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="b13f0-184">Jätä **Määritä käyttöoikeus** -kenttään oletusarvo, **Azure AD -käyttäjä, ryhmä tai palvelun päätieto**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-184">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="b13f0-185">Syötä **Valitse**-kohtaan **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-185">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="b13f0-186">Valitse luettelosta **Dynamics-käyttöönoton palvelut Services \[käytössä wsfed\]**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-186">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="b13f0-187">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-187">Select **Save**.</span></span>

1. <span data-ttu-id="b13f0-188">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-188">Select **Next**.</span></span>
1. <span data-ttu-id="b13f0-189">Noudata sivulle tulevia ohjeita ja myönnä tilaukselle tarvittavien sovellusten käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="b13f0-189">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="b13f0-190">Ota tarvittaessa yhteys Azure-tilauksen järjestelmänvalvojaan.</span><span class="sxs-lookup"><span data-stu-id="b13f0-190">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="b13f0-191">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-191">Select **Next**.</span></span>
1. <span data-ttu-id="b13f0-192">Valitse **Azure-alue**-kohdassa **Itä-Yhdysvallat**, **Itä-Yhdysvallat 2**, **Länsi-Yhdysvallat** tai **Länsi-Yhdysvallat 2**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-192">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="b13f0-193">Valitse **Yhdistä**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-193">Select **Connect**.</span></span> <span data-ttu-id="b13f0-194">Azure-yhdistin näkyy luettelossa.</span><span class="sxs-lookup"><span data-stu-id="b13f0-194">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="b13f0-195">Tuo Commerce Preview -esittelyalustan laajennus</span><span class="sxs-lookup"><span data-stu-id="b13f0-195">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="b13f0-196">Voit tuoda Commerce Preview-demokannan laajennuksen projektiin noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="b13f0-196">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="b13f0-197">Avaa projektin kotisivu valitsemalla projektin nimi yläreunassa.</span><span class="sxs-lookup"><span data-stu-id="b13f0-197">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="b13f0-198">Noudata seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="b13f0-198">Follow one of these steps:</span></span>

    - <span data-ttu-id="b13f0-199">Jos olet kumppani, valitse **Omaisuuskirjasto** -ruutu oikeassa reunassa.</span><span class="sxs-lookup"><span data-stu-id="b13f0-199">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="b13f0-200">Jos olet asiakas, valitse ylävalikosta **Omaisuuskirjasto**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-200">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="b13f0-201">Valitse vasemmalla olevasta luettelosta **Käyttöönotettava ohjelmistopaketti**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-201">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="b13f0-202">Valitse **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-202">Select **Import**.</span></span>
1. <span data-ttu-id="b13f0-203">Valitse **Commerce Preview -esittelyn peruslaajennus** **Jaettu resurssikirjasto** -kohdan resurssiluettelosta.</span><span class="sxs-lookup"><span data-stu-id="b13f0-203">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="b13f0-204">Valitse **Kerää**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-204">Select **Pick**.</span></span> <span data-ttu-id="b13f0-205">Sinut siirretään resurssikirjastoon ja laajennuksen tulisi näkyä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="b13f0-205">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="b13f0-206">Seuraavassa kuvassa näkyvät toiminnot, jotka on tehtävä LCS-**resurssikirjasto**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="b13f0-206">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![Commerce Preview -esittelyalustan laajennuksen tuominen](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="b13f0-208">Käyttöönottoympäristö</span><span class="sxs-lookup"><span data-stu-id="b13f0-208">Deploy the environment</span></span>

<span data-ttu-id="b13f0-209">Määritä ympäristö näiden ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="b13f0-209">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="b13f0-210">Vaiheita 6, 7 ja/tai 8 ei ehkä tarvitse suorittaa, koska sivut, joilla on yksi vaihtoehto, ohitetaan.</span><span class="sxs-lookup"><span data-stu-id="b13f0-210">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="b13f0-211">Kun olet **Ympäristön parametrit** -näkymässä, varmista, että teksti **Dynamics 365 Commerce - esittely (10.0.* x* ja Platform-päivitys *xx*)\*\* näkyy suoraan **Ympäristön nimi** -kentän yläpuolella.</span><span class="sxs-lookup"><span data-stu-id="b13f0-211">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="b13f0-212">Katso tiedot vaiheen 8 jälkeen näkyvästä kuvasta.</span><span class="sxs-lookup"><span data-stu-id="b13f0-212">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="b13f0-213">Valitse päävalikosta **Pilvipalveluympäristöt**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-213">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="b13f0-214">Valitse **+ Lisää** lisätäksesi ympäristön.</span><span class="sxs-lookup"><span data-stu-id="b13f0-214">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="b13f0-215">Valitse **Sovelluksen versio** -kentässä uusin versio.</span><span class="sxs-lookup"><span data-stu-id="b13f0-215">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="b13f0-216">Jos sinulla on erityinen tarve valita jokin muu sovellusversio kuin uusin versio, älä valitse vanhempaa versiota kuin **10.0.8.**</span><span class="sxs-lookup"><span data-stu-id="b13f0-216">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.8**.</span></span>
1. <span data-ttu-id="b13f0-217">Käytä **Käyttöympäristön versio** -kentässä käyttöympäristö versiota, joka valitaan automaattisesti valitsemaasi sovellusversioon.</span><span class="sxs-lookup"><span data-stu-id="b13f0-217">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Sovelluksen ja ympäristön versioiden valitseminen](./media/project1.png)

1. <span data-ttu-id="b13f0-219">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-219">Select **Next**.</span></span>
1. <span data-ttu-id="b13f0-220">Valitse **Esittely** ympäristötopologiaksi.</span><span class="sxs-lookup"><span data-stu-id="b13f0-220">Select **Demo** as the environment topology.</span></span>

    ![Ympäristötopologia 1 valitseminen](./media/project2.png)

1. <span data-ttu-id="b13f0-222">Valitse **Dynamics 365 Commerce - Esittely** ympäristötopologiaksi.</span><span class="sxs-lookup"><span data-stu-id="b13f0-222">Select **Dynamics 365 Commerce - Demo** as the environment topology.</span></span> <span data-ttu-id="b13f0-223">Jos olet määrittänyt aiemmin yhden Azure-yhdistimen, sitä käytetään tässä ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="b13f0-223">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="b13f0-224">Jos olet määrittänyt useita Azure-yhdistimiä, voit valita käytettävän yhdistimen: **Itä-Yhdysvallat**, **Itä-Yhdysvallat 2**, **Länsi-Yhdysvallat**tai **Länsi-Yhdysvallat 2**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-224">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="b13f0-225">(Parhaan päästä päähän-suorituskyvyn saavuttamiseksi suosittelemme valitsemaan **Länsi-Yhdysvallat 2**.)</span><span class="sxs-lookup"><span data-stu-id="b13f0-225">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![Ympäristötopologia 2 valitseminen](./media/project3.png)

1. <span data-ttu-id="b13f0-227">Anna ympäristön nimi **Ympäristön käyttöönotto** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="b13f0-227">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="b13f0-228">Älä muuta Lisäasetukset-kohtaa.</span><span class="sxs-lookup"><span data-stu-id="b13f0-228">Leave the advanced settings as they are.</span></span>

    ![Ympäristön käyttöönotto -sivu](./media/project4.png)

1. <span data-ttu-id="b13f0-230">Säädä VM:n kokoa tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="b13f0-230">Adjust the VM size as required.</span></span> <span data-ttu-id="b13f0-231">(Suosittelemme VM:n varastointiyksikköä \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="b13f0-231">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="b13f0-232">Tarkista hinnoittelu- ja lisensointiehdot ja valitse sitten valintaruutu, jos hyväksyt ne.</span><span class="sxs-lookup"><span data-stu-id="b13f0-232">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="b13f0-233">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-233">Select **Next**.</span></span>
1. <span data-ttu-id="b13f0-234">Kun tietojen oikeellisuus on vahvistettu käyttöönoton vahvistussivulla, valitse **Ota käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-234">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="b13f0-235">Sinut siirretään **Pilvipalveluympäristöt**-näkymään ja ympäristösi pitäisi näkyä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="b13f0-235">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="b13f0-236">Pyydetty ympäristö näkyy jonossa. Tämän jälkeen se otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="b13f0-236">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="b13f0-237">Ympäristön työnkulut kestävät jonkin aikaa.</span><span class="sxs-lookup"><span data-stu-id="b13f0-237">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="b13f0-238">Tarkista tilanne, kun aikaa on kulunut noin kuudesta yhdeksään tuntiin.</span><span class="sxs-lookup"><span data-stu-id="b13f0-238">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="b13f0-239">Varmista ennen jatkamista, että ympäristösi tila on **Otettu käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-239">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-csu"></a><span data-ttu-id="b13f0-240">Alusta Commerce Scale unit (CSU)</span><span class="sxs-lookup"><span data-stu-id="b13f0-240">Initialize the commerce scale unit (CSU)</span></span>

<span data-ttu-id="b13f0-241">Alusta CSU-osoite seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="b13f0-241">To initialize CSU, follow these steps.</span></span>

1. <span data-ttu-id="b13f0-242">Valitse **Pilvipalveluympäristöt**-näkymässä luettelosta ympäristösi.</span><span class="sxs-lookup"><span data-stu-id="b13f0-242">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="b13f0-243">Valitse oikealla olevasta ympäristön näkymästä **Täydet tiedot**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-243">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="b13f0-244">Näkyviin tulee ympäristön tietojen näkymä.</span><span class="sxs-lookup"><span data-stu-id="b13f0-244">The environment details view appears.</span></span>
1. <span data-ttu-id="b13f0-245">Valitse **Ympäristön ominaisuudet** -kohdassa **Hallitse**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-245">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="b13f0-246">Valitse **Commerce**-välilehdestä **Alusta**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-246">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="b13f0-247">Näkyviin tulee CSU-alustusparametrien näkymä.</span><span class="sxs-lookup"><span data-stu-id="b13f0-247">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="b13f0-248">Valitse **Alue**-kohdassa **Itä-Yhdysvallat**, **Itä-Yhdysvallat 2**, **Länsi-Yhdysvallat** tai **Länsi-Yhdysvallat 2**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-248">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="b13f0-249">Valitse **Versio**-kentässä **Määritä versio** -luettelosta ja määritä sitten **9.18.20014.4** näyttöön tulevassa kentässä.</span><span class="sxs-lookup"><span data-stu-id="b13f0-249">In the **Version** field, select **Specify a version** in the list, and then specify **9.18.20014.4** in the field that appears.</span></span> <span data-ttu-id="b13f0-250">Muista määrittää tarkka versio, joka on ilmoitettu tässä.</span><span class="sxs-lookup"><span data-stu-id="b13f0-250">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="b13f0-251">Muussa tapauksessa sinun on päivitettävä RCSU oikeaan versioon myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="b13f0-251">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="b13f0-252">Ota käyttöön **Laajennuksen käyttäminen** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="b13f0-252">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="b13f0-253">Valitse laajennusluettelosta **Commerce Preview -esittelyn peruslaajennus**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-253">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="b13f0-254">Valitse **Alusta**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-254">Select **Initialize**.</span></span>
1. <span data-ttu-id="b13f0-255">Kun tietojen oikeellisuus on vahvistettu käyttöönoton vahvistussivulla, valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-255">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="b13f0-256">**Commercen hallinta** -näkymä tulee uudelleen näkyviin, kun **Commerce**-välilehti on valittuna.</span><span class="sxs-lookup"><span data-stu-id="b13f0-256">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="b13f0-257">CSU on asetettu jonoon valmistelua varten.</span><span class="sxs-lookup"><span data-stu-id="b13f0-257">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="b13f0-258">Varmista ennen jatkamista, että CSU:si tila on **Onnistunut**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-258">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="b13f0-259">Alustus kestää noin kahdesta viiteen tuntia.</span><span class="sxs-lookup"><span data-stu-id="b13f0-259">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="b13f0-260">Sähköisen kaupankäynnin alustaminen</span><span class="sxs-lookup"><span data-stu-id="b13f0-260">Initialize e-Commerce</span></span>

<span data-ttu-id="b13f0-261">Alusta sähköinen kaupankäynti seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="b13f0-261">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="b13f0-262">Tarkista esikatselun suostumus **sähköisen kaupankäynnin**-välilehdestä ja valitse sitten **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-262">On the **e-Commerce** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="b13f0-263">Kirjoita **Sähköisen kaupankäynnin vuokraajan nimi** -kenttään nimi.</span><span class="sxs-lookup"><span data-stu-id="b13f0-263">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="b13f0-264">Ota huomioon, että tämä nimi näkyy joissakin sähköisen kaupankäynnin esiintymään vievissä URL-osoitteissa.</span><span class="sxs-lookup"><span data-stu-id="b13f0-264">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="b13f0-265">Valitse **Commerce Scale -yksikön nimi** -kentässä CSU-luettelosta.</span><span class="sxs-lookup"><span data-stu-id="b13f0-265">In the **Commerce scale unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="b13f0-266">(Luettelossa pitäisi olla vain yksi vaihtoehto.)</span><span class="sxs-lookup"><span data-stu-id="b13f0-266">(The list should have only one option.)</span></span>

    <span data-ttu-id="b13f0-267">**Sähköisen kaupankäynnin paikkatieto** -kenttä määritetään automaattisesti, eikä arvoa voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="b13f0-267">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="b13f0-268">Jatka valitsemalla **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-268">Select **Next** to continue.</span></span>
1. <span data-ttu-id="b13f0-269">Kirjoita **Tuetut isäntänimet** -kenttään mikä tahansa kelvollinen toimialue, kuten `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="b13f0-269">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="b13f0-270">**AAD-suojausryhmän järjestelmänhallinta** -kenttään, kirjoita haluamasi käyttöoikeusryhmän nimen muutama ensimmäinen kirjain.</span><span class="sxs-lookup"><span data-stu-id="b13f0-270">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="b13f0-271">Tuo hakutulokset näkyviin valitsemalla suurennuslasikuvake.</span><span class="sxs-lookup"><span data-stu-id="b13f0-271">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="b13f0-272">Valitse luettelosta oikea suojausryhmä.</span><span class="sxs-lookup"><span data-stu-id="b13f0-272">Select the correct security group from the list.</span></span>
2.  <span data-ttu-id="b13f0-273">**AAD-turvallisuusryhmä luokituksille ja arvosteluvalvoja** -kenttään, kirjoita haluamasi käyttöoikeusryhmän nimen muutama ensimmäinen kirjain.</span><span class="sxs-lookup"><span data-stu-id="b13f0-273">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="b13f0-274">Tuo hakutulokset näkyviin valitsemalla suurennuslasikuvake.</span><span class="sxs-lookup"><span data-stu-id="b13f0-274">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="b13f0-275">Valitse luettelosta oikea suojausryhmä.</span><span class="sxs-lookup"><span data-stu-id="b13f0-275">Select the correct security group from the list.</span></span>
1. <span data-ttu-id="b13f0-276">Jätä **Ota luokitukset ja arvostelut -palvelu käyttöön** -asetus päälle.</span><span class="sxs-lookup"><span data-stu-id="b13f0-276">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="b13f0-277">Valitse **Alusta**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-277">Select **Initialize**.</span></span> <span data-ttu-id="b13f0-278">**Commercen hallinta** -näkymä tulee uudelleen näkyviin, kun **e-Commerce**-välilehti on valittuna.</span><span class="sxs-lookup"><span data-stu-id="b13f0-278">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="b13f0-279">Sähköisen kaupankäynnin alustaminen on aloitettu.</span><span class="sxs-lookup"><span data-stu-id="b13f0-279">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="b13f0-280">Ennen kuin jatkat, odota, kunnes sähköisen kaupankäynnin alustamisen tila on **Alustaminen onnistui**.</span><span class="sxs-lookup"><span data-stu-id="b13f0-280">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="b13f0-281">Merkitse oikeassa alakulmassa olevassa **Linkit**-kohdassa seuraavien linkkien URL-osoitteet:</span><span class="sxs-lookup"><span data-stu-id="b13f0-281">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="b13f0-282">**Sähköisen kaupankäynnin sivusto** – linkki verkkokaupan sivustosi juureen.</span><span class="sxs-lookup"><span data-stu-id="b13f0-282">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="b13f0-283">**Sähköisen kaupankäynnin hallintatyökalu** – linkki sivuston hallintatyökaluun.</span><span class="sxs-lookup"><span data-stu-id="b13f0-283">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="b13f0-284">Commercen esikatseluympäristön tuki</span><span class="sxs-lookup"><span data-stu-id="b13f0-284">Commerce preview environment support</span></span>

<span data-ttu-id="b13f0-285">Jos valmisteluvaiheiden suorittamisen aikana on ongelmia, saat apua [Microsoft Dynamics 365 Commerce Preview Yammer -ryhmästä](https://aka.ms/Dynamics365CommercePreviewYammer).</span><span class="sxs-lookup"><span data-stu-id="b13f0-285">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b13f0-286">Seuraavat vaiheet</span><span class="sxs-lookup"><span data-stu-id="b13f0-286">Next steps</span></span>

<span data-ttu-id="b13f0-287">Jatkaaksesi käyttöönotto- ja määritysprosessia Commercen esikatseluympäristön määrittelystä, katso [Commercen esikatseluympäristön määrittäminen](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="b13f0-287">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b13f0-288">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b13f0-288">Additional resources</span></span>

[<span data-ttu-id="b13f0-289">Dynamics 365 Commercen esikatseluympäristön yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="b13f0-289">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="b13f0-290">Dynamics 365 Commercen esikatseluympäristön määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b13f0-290">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="b13f0-291">Valinnaisten ominaisuuksien määrittäminen Dynamics 365 Commercen esikatseluympäristöä varten</span><span class="sxs-lookup"><span data-stu-id="b13f0-291">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="b13f0-292">Dynamics 365 Commerce -esikatseluympäristön usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="b13f0-292">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="b13f0-293">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="b13f0-293">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="b13f0-294">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="b13f0-294">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="b13f0-295">Microsoft Azure -portaali</span><span class="sxs-lookup"><span data-stu-id="b13f0-295">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="b13f0-296">Dynamics 365 Commerce -sivusto</span><span class="sxs-lookup"><span data-stu-id="b13f0-296">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

