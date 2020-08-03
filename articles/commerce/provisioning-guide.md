---
title: Dynamics 365 Commerce -arviointiympäristön valmisteleminen
description: Tässä ohjeaiheessa kerrotaan, kuinka voit valmistella Microsoft Dynamics 365 Commercen arviointiympäristön.
author: psimolin
manager: annbe
ms.date: 07/16/2020
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
ms.openlocfilehash: e5ce2002c66a1c36d5647d3c76684b394fc1ff79
ms.sourcegitcommit: 5175e3fae432016246244cf70fe05465f43de88c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/17/2020
ms.locfileid: "3599847"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="bab98-103">Dynamics 365 Commerce -arviointiympäristön valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="bab98-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bab98-104">Tässä ohjeaiheessa kerrotaan, kuinka voit valmistella Microsoft Dynamics 365 Commercen arviointiympäristön.</span><span class="sxs-lookup"><span data-stu-id="bab98-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="bab98-105">Ennen kuin aloitat, suosittelemme, että tarkistat tämän aiheen nopeasti, jotta saat käsityksen prosessin vaatimista aiheista.</span><span class="sxs-lookup"><span data-stu-id="bab98-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="bab98-106">Commercen arviointiympäristöt eivät ole yleisesti saatavana, ja ne myönnetään kumppaneille ja asiakkaille pyyntökohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="bab98-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="bab98-107">Pyydä lisätietoja Microsoft-kumppanilta.</span><span class="sxs-lookup"><span data-stu-id="bab98-107">For more information, reach out to your Microsoft partner contact.</span></span>

## <a name="overview"></a><span data-ttu-id="bab98-108">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="bab98-108">Overview</span></span>

<span data-ttu-id="bab98-109">Commercen arviointiympäristön onnistunut valmistelu edellyttää sellaisen projektin luontia, jossa on tietty tuotteen nimi ja tyyppi.</span><span class="sxs-lookup"><span data-stu-id="bab98-109">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="bab98-110">Ympäristöllä ja Commerce Scale Unit (CSU) -ratkaisulla on myös joitakin tiettyjä parametreja, joita on käytettävä, jos oletat valmistelevasi sähköisen kaupankäynnin myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="bab98-110">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="bab98-111">Tämän ohjeaiheen ohjeissa kuvataan kaikki vaiheet, joita tarvitaan valmisteluun, ja parametrit, joita on käytettävä.</span><span class="sxs-lookup"><span data-stu-id="bab98-111">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="bab98-112">Kun olet onnistuneesti valmistellut Commercen arviointiympäristön, sinun on suoritettava muutama valmistelun jälkeinen vaihe sen käyttöönottamista varten.</span><span class="sxs-lookup"><span data-stu-id="bab98-112">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="bab98-113">Jotkin vaiheet ovat valinnaisia. Tämä riippuu siitä, mitä järjestelmän alueita haluat arvioida.</span><span class="sxs-lookup"><span data-stu-id="bab98-113">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="bab98-114">Voit aina suorittaa valinnaiset vaiheet myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="bab98-114">You can always complete the optional steps later.</span></span>

<span data-ttu-id="bab98-115">Lisätietoja Commercen arviointiympäristön määrittämistä valmistelun jälkeen on kohdassa [Commercen arviointiympäristön määrittäminen](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="bab98-115">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="bab98-116">Lisätietoja Commercen arviointiympäristön valinnaisten ominaisuuksien määrittämisestä on kohdassa [Commercen arviointiympäristön valinnaisten ominaisuuksien määrittäminen](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="bab98-116">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bab98-117">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="bab98-117">Prerequisites</span></span>

<span data-ttu-id="bab98-118">Seuraavien edellytysten on oltava käytössä, ennen kuin voit määrittää Commercen arviointiympäristön:</span><span class="sxs-lookup"><span data-stu-id="bab98-118">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="bab98-119">Sinulla on Microsoft Dynamics Lifecycle Services -portaalin (LCS) käyttöoikeus</span><span class="sxs-lookup"><span data-stu-id="bab98-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="bab98-120">Olet aiemmin luotu Microsoft Dynamics 365 -kumppani tai -asiakas ja pystyt luomaan Dynamics 365 Commerce -projektin.</span><span class="sxs-lookup"><span data-stu-id="bab98-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="bab98-121">Sinulla on Microsoft Azure -tilauksen järjestelmänvalvojan käyttöoikeus tai olet yhteydessä tilauksen järjestelmänvalvojaan, joka voi avustaa tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="bab98-121">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="bab98-122">Sinulla on käytettävissä Azure Active Directory (Azure AD) -vuokralaisen tunnus.</span><span class="sxs-lookup"><span data-stu-id="bab98-122">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="bab98-123">Olet luonut Azure AD -käyttöoikeusryhmän, jota voidaan käyttää sähköisen kaupankäynnin järjestelmänvalvojien ryhmänä, ja sinulla on ryhmän tunnus.</span><span class="sxs-lookup"><span data-stu-id="bab98-123">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="bab98-124">Olet luonut Azure AD -käyttöoikeusryhmän, jota voidaan käyttää arviot ja arvostelut -moderaattorien ryhmänä, ja sinulla on ryhmän tunnus.</span><span class="sxs-lookup"><span data-stu-id="bab98-124">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="bab98-125">(Tämä suojausryhmä voi olla sama kuin verkkokauppajärjestelmän järjestelmänvalvojaryhmä.)</span><span class="sxs-lookup"><span data-stu-id="bab98-125">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="bab98-126">Huomaa, että tämä luettelo ei ole täydellinen.</span><span class="sxs-lookup"><span data-stu-id="bab98-126">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="bab98-127">Jos ongelmia esiintyy, ota yhteys Microsoft-kumppaniin.</span><span class="sxs-lookup"><span data-stu-id="bab98-127">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="bab98-128">Commercen arviointiympäristön valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="bab98-128">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="bab98-129">Näissä ohjeissa käsitellään Commercen arviointiympäristö valmistelua.</span><span class="sxs-lookup"><span data-stu-id="bab98-129">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="bab98-130">Kun olet suorittanut ne onnistuneesti, Commercen arviointiympäristö on valmis määritettäväksi.</span><span class="sxs-lookup"><span data-stu-id="bab98-130">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="bab98-131">Kaikki tässä kuvatut toiminnot tapahtuvat LCS-portaalissa.</span><span class="sxs-lookup"><span data-stu-id="bab98-131">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="bab98-132">Luo uusi projekti</span><span class="sxs-lookup"><span data-stu-id="bab98-132">Create a new project</span></span>

<span data-ttu-id="bab98-133">Noudata seuraavia vaiheita luodaksesi uuden projektin LCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="bab98-133">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="bab98-134">Luo projekti valitsemalla LCS-aloitussivulla plusmerkki (**+**).</span><span class="sxs-lookup"><span data-stu-id="bab98-134">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="bab98-135">Noudata oikeanpuoleisessa ruudussa jotakin näistä vaiheista:</span><span class="sxs-lookup"><span data-stu-id="bab98-135">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="bab98-136">Jos olet kumppani, valitse **Siirrä, luo ratkaisuja ja opi**.</span><span class="sxs-lookup"><span data-stu-id="bab98-136">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="bab98-137">Jos olet asiakas, valitse **Mahdolliset myyntiä edeltävät toimet**.</span><span class="sxs-lookup"><span data-stu-id="bab98-137">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="bab98-138">Syötä mallin nimi, kuvaus ja toimiala.</span><span class="sxs-lookup"><span data-stu-id="bab98-138">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="bab98-139">Valitse **Tuotenimi** -kentässä **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="bab98-139">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="bab98-140">Valitse **Tuoteversio**-kentässä **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="bab98-140">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="bab98-141">Valitse **Metodologia**-kentässä **Dynamics Retail -implementointimetodologia**.</span><span class="sxs-lookup"><span data-stu-id="bab98-141">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="bab98-142">Valinnainen: Voit tuoda rooleja ja käyttäjiä aiemmin luodusta projektista.</span><span class="sxs-lookup"><span data-stu-id="bab98-142">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="bab98-143">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="bab98-143">Select **Create**.</span></span> <span data-ttu-id="bab98-144">Projektinäkymä avautuu.</span><span class="sxs-lookup"><span data-stu-id="bab98-144">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="bab98-145">Azure-yhdistimen lisääminen</span><span class="sxs-lookup"><span data-stu-id="bab98-145">Add the Azure Connector</span></span>

<span data-ttu-id="bab98-146">Lisää Azure Connector LCS-projektiin kohdassa [Azure Resource Manager (ARM) -perehdytyksen suorittaminen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding) olevien ohjeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="bab98-146">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="bab98-147">Käyttöönottoympäristö</span><span class="sxs-lookup"><span data-stu-id="bab98-147">Deploy the environment</span></span>

<span data-ttu-id="bab98-148">Määritä ympäristö näiden ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="bab98-148">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="bab98-149">Vaiheita 6, 7 ja/tai 8 ei ehkä tarvitse suorittaa, koska sivut, joilla on yksi vaihtoehto, ohitetaan.</span><span class="sxs-lookup"><span data-stu-id="bab98-149">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="bab98-150">Kun olet **Ympäristön parametrit** -näkymässä, varmista, että teksti **Dynamics 365 Commerce - esittely (10.0.* x* ja Platform-päivitys *xx*)\*\* näkyy suoraan **Ympäristön nimi** -kentän yläpuolella.</span><span class="sxs-lookup"><span data-stu-id="bab98-150">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="bab98-151">Katso tiedot vaiheen 8 jälkeen näkyvästä kuvasta.</span><span class="sxs-lookup"><span data-stu-id="bab98-151">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="bab98-152">Valitse päävalikosta **Pilvipalveluympäristöt**.</span><span class="sxs-lookup"><span data-stu-id="bab98-152">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="bab98-153">Valitse **+ Lisää** lisätäksesi ympäristön.</span><span class="sxs-lookup"><span data-stu-id="bab98-153">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="bab98-154">Valitse **Sovelluksen versio** -kentässä uusin versio.</span><span class="sxs-lookup"><span data-stu-id="bab98-154">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="bab98-155">Jos sinulla on erityinen tarve valita jokin muu sovellusversio kuin uusin versio, älä valitse vanhempaa versiota kuin **10.0.8.**</span><span class="sxs-lookup"><span data-stu-id="bab98-155">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.8**.</span></span>
1. <span data-ttu-id="bab98-156">Käytä **Käyttöympäristön versio** -kentässä käyttöympäristö versiota, joka valitaan automaattisesti valitsemaasi sovellusversioon.</span><span class="sxs-lookup"><span data-stu-id="bab98-156">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Sovelluksen ja ympäristön versioiden valitseminen](./media/project1.png)

1. <span data-ttu-id="bab98-158">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="bab98-158">Select **Next**.</span></span>
1. <span data-ttu-id="bab98-159">Valitse **Esittely** ympäristötopologiaksi.</span><span class="sxs-lookup"><span data-stu-id="bab98-159">Select **Demo** as the environment topology.</span></span>

    ![Ympäristötopologia 1 valitseminen](./media/project2.png)

1. <span data-ttu-id="bab98-161">Anna ympäristön nimi **Ympäristön käyttöönotto** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="bab98-161">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="bab98-162">Älä muuta Lisäasetukset-kohtaa.</span><span class="sxs-lookup"><span data-stu-id="bab98-162">Leave the advanced settings as they are.</span></span>

    ![Ympäristön käyttöönotto -sivu](./media/project4.png)

1. <span data-ttu-id="bab98-164">Säädä VM:n kokoa tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="bab98-164">Adjust the VM size as required.</span></span> <span data-ttu-id="bab98-165">(Suosittelemme VM:n varastointiyksikköä \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="bab98-165">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="bab98-166">Tarkista hinnoittelu- ja lisensointiehdot ja valitse sitten valintaruutu, jos hyväksyt ne.</span><span class="sxs-lookup"><span data-stu-id="bab98-166">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="bab98-167">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="bab98-167">Select **Next**.</span></span>
1. <span data-ttu-id="bab98-168">Kun tietojen oikeellisuus on vahvistettu käyttöönoton vahvistussivulla, valitse **Ota käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="bab98-168">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="bab98-169">Sinut siirretään **Pilvipalveluympäristöt**-näkymään ja ympäristösi pitäisi näkyä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="bab98-169">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="bab98-170">Pyydetty ympäristö näkyy jonossa. Tämän jälkeen se otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="bab98-170">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="bab98-171">Ympäristön työnkulut kestävät jonkin aikaa.</span><span class="sxs-lookup"><span data-stu-id="bab98-171">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="bab98-172">Tarkista tilanne, kun aikaa on kulunut noin kuudesta yhdeksään tuntiin.</span><span class="sxs-lookup"><span data-stu-id="bab98-172">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="bab98-173">Varmista ennen jatkamista, että ympäristösi tila on **Otettu käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="bab98-173">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="bab98-174">Alusta Commerce Scale Unit (pilvi)</span><span class="sxs-lookup"><span data-stu-id="bab98-174">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="bab98-175">Alusta CSU-osoite seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="bab98-175">To initialize CSU, follow these steps.</span></span>

1. <span data-ttu-id="bab98-176">Valitse **Pilvipalveluympäristöt**-näkymässä luettelosta ympäristösi.</span><span class="sxs-lookup"><span data-stu-id="bab98-176">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="bab98-177">Valitse oikealla olevasta ympäristön näkymästä **Täydet tiedot**.</span><span class="sxs-lookup"><span data-stu-id="bab98-177">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="bab98-178">Näkyviin tulee ympäristön tietojen näkymä.</span><span class="sxs-lookup"><span data-stu-id="bab98-178">The environment details view appears.</span></span>
1. <span data-ttu-id="bab98-179">Valitse **Ympäristön ominaisuudet** -kohdassa **Hallitse**.</span><span class="sxs-lookup"><span data-stu-id="bab98-179">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="bab98-180">Valitse **Commerce**-välilehdestä **Alusta**.</span><span class="sxs-lookup"><span data-stu-id="bab98-180">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="bab98-181">Näkyviin tulee CSU-alustusparametrien näkymä.</span><span class="sxs-lookup"><span data-stu-id="bab98-181">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="bab98-182">Valitse **Alue**-kentässä alue, joka on sama alue tai lähellä sitä aluetta, jossa ympäristö otettiin käyttöön.</span><span class="sxs-lookup"><span data-stu-id="bab98-182">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="bab98-183">Älä tee muutoksia **Versio**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="bab98-183">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="bab98-184">Valitse **Alusta**.</span><span class="sxs-lookup"><span data-stu-id="bab98-184">Select **Initialize**.</span></span>
1. <span data-ttu-id="bab98-185">Kun tietojen oikeellisuus on vahvistettu käyttöönoton vahvistussivulla, valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="bab98-185">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="bab98-186">**Commercen hallinta** -näkymä tulee uudelleen näkyviin, kun **Commerce**-välilehti on valittuna.</span><span class="sxs-lookup"><span data-stu-id="bab98-186">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="bab98-187">CSU on asetettu jonoon valmistelua varten.</span><span class="sxs-lookup"><span data-stu-id="bab98-187">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="bab98-188">Varmista ennen jatkamista, että CSU:si tila on **Onnistunut**.</span><span class="sxs-lookup"><span data-stu-id="bab98-188">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="bab98-189">Alustus kestää noin kahdesta viiteen tuntia.</span><span class="sxs-lookup"><span data-stu-id="bab98-189">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="bab98-190">Jos **Hallinta**-linkki ei ole ympäristön tietonäkymässä, ota yhteys Microsoftin yhteyshenkilöön.</span><span class="sxs-lookup"><span data-stu-id="bab98-190">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="bab98-191">Sähköisen kaupankäynnin alustaminen</span><span class="sxs-lookup"><span data-stu-id="bab98-191">Initialize e-Commerce</span></span>

<span data-ttu-id="bab98-192">Alusta sähköinen kaupankäynti seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="bab98-192">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="bab98-193">Tarkista arviointiversion suostumus **Sähköinen kaupankäynti**-välilehdessä ja valitse sitten **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="bab98-193">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="bab98-194">Anna **Sähköisen kaupankäynnin ympäristön nimi** -kenttään nimi.</span><span class="sxs-lookup"><span data-stu-id="bab98-194">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="bab98-195">Ota huomioon, että tämä nimi näkyy joissakin sähköisen kaupankäynnin esiintymään vievissä URL-osoitteissa.</span><span class="sxs-lookup"><span data-stu-id="bab98-195">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="bab98-196">Valitse **Commerce Scale Unitin nimi** -kentässä CSU-luettelosta.</span><span class="sxs-lookup"><span data-stu-id="bab98-196">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="bab98-197">(Luettelossa pitäisi olla vain yksi vaihtoehto.)</span><span class="sxs-lookup"><span data-stu-id="bab98-197">(The list should have only one option.)</span></span>

    <span data-ttu-id="bab98-198">**Sähköisen kaupankäynnin maantieteellinen alue** -kenttä täytetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="bab98-198">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="bab98-199">Jatka valitsemalla **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="bab98-199">Select **Next** to continue.</span></span>
1. <span data-ttu-id="bab98-200">Kirjoita **Tuetut isäntänimet** -kenttään mikä tahansa kelvollinen toimialue, kuten `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="bab98-200">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="bab98-201">Anna **Järjestelmänvalvojan AAD-käyttöoikeusryhmä** -kentässä käytettävän käyttöoikeusryhmän nimen kaksi ensimmäistä kirjainta ja näytä sitten hakutulokset valitsemalla suurennuslasikuvake.</span><span class="sxs-lookup"><span data-stu-id="bab98-201">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="bab98-202">Valitse luettelossa oikea käyttöoikeusryhmä.</span><span class="sxs-lookup"><span data-stu-id="bab98-202">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="bab98-203">Anna **Luokitusten ja arvostelujen valvojan AAD-käyttöoikeusryhmä** -kentässä käytettävän käyttöoikeusryhmän nimen kaksi ensimmäistä kirjainta ja näytä sitten hakutulokset valitsemalla suurennuslasikuvake.</span><span class="sxs-lookup"><span data-stu-id="bab98-203">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="bab98-204">Valitse luettelossa oikea käyttöoikeusryhmä.</span><span class="sxs-lookup"><span data-stu-id="bab98-204">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="bab98-205">Jätä **Ota luokitukset ja arvostelupalvelu käyttöön** -asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="bab98-205">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="bab98-206">Valitse **Alusta**.</span><span class="sxs-lookup"><span data-stu-id="bab98-206">Select **Initialize**.</span></span> <span data-ttu-id="bab98-207">**Commercen hallinta** -näkymä tulee uudelleen näkyviin, kun **e-Commerce**-välilehti on valittuna.</span><span class="sxs-lookup"><span data-stu-id="bab98-207">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="bab98-208">Sähköisen kaupankäynnin alustaminen on aloitettu.</span><span class="sxs-lookup"><span data-stu-id="bab98-208">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="bab98-209">Ennen kuin jatkat, odota, kunnes sähköisen kaupankäynnin alustamisen tila on **Alustaminen onnistui**.</span><span class="sxs-lookup"><span data-stu-id="bab98-209">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="bab98-210">Merkitse oikeassa alakulmassa olevassa **Linkit**-kohdassa seuraavien linkkien URL-osoitteet:</span><span class="sxs-lookup"><span data-stu-id="bab98-210">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="bab98-211">**Sähköisen kaupankäynnin sivusto** – linkki verkkokaupan sivustosi juureen.</span><span class="sxs-lookup"><span data-stu-id="bab98-211">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="bab98-212">**Commerce-sivuston luontiohjelma** – linkki sivuston hallintatyökaluun.</span><span class="sxs-lookup"><span data-stu-id="bab98-212">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="bab98-213">Seuraavat vaiheet</span><span class="sxs-lookup"><span data-stu-id="bab98-213">Next steps</span></span>

<span data-ttu-id="bab98-214">Tietoja Commercen arviointiympäristön valmistelu- ja määritysprosessin jatkamisesta on kohdassa [Commercen arviointiympäristön määrittäminen](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="bab98-214">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bab98-215">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="bab98-215">Additional resources</span></span>

[<span data-ttu-id="bab98-216">Dynamics 365 Commerce -arviointiympäristön yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="bab98-216">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="bab98-217">Dynamics 365 Commerce -arviointiympäristön määritykset</span><span class="sxs-lookup"><span data-stu-id="bab98-217">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="bab98-218">BOPIS:n määritykset Dynamics 365 Commerce -arviointiympäristössä</span><span class="sxs-lookup"><span data-stu-id="bab98-218">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="bab98-219">Dynamics 365 Commerce -arviointiympäristön valinnaisten ominaisuuksien määritykset</span><span class="sxs-lookup"><span data-stu-id="bab98-219">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="bab98-220">Dynamics 365 Commerce -arviointiympäristön usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="bab98-220">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="bab98-221">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="bab98-221">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="bab98-222">Commerce Scale Unit (pilvi)</span><span class="sxs-lookup"><span data-stu-id="bab98-222">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="bab98-223">Microsoft Azure -portaali</span><span class="sxs-lookup"><span data-stu-id="bab98-223">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="bab98-224">Dynamics 365 Commerce -sivusto</span><span class="sxs-lookup"><span data-stu-id="bab98-224">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
