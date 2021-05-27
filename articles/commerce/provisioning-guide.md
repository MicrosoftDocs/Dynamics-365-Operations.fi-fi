---
title: Dynamics 365 Commerce -arviointiympäristön valmisteleminen
description: Tässä ohjeaiheessa kerrotaan, kuinka voit valmistella Microsoft Dynamics 365 Commercen arviointiympäristön.
author: psimolin
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6b675d4af6fb9a080f3f3a13e64b2c5b6ad4b783
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022419"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="b42d6-103">Dynamics 365 Commerce -arviointiympäristön valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="b42d6-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b42d6-104">Tässä ohjeaiheessa kerrotaan, kuinka voit valmistella Microsoft Dynamics 365 Commercen arviointiympäristön.</span><span class="sxs-lookup"><span data-stu-id="b42d6-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="b42d6-105">Ennen kuin aloitat, suosittelemme, että tarkistat tämän aiheen nopeasti, jotta saat käsityksen prosessin vaatimista aiheista.</span><span class="sxs-lookup"><span data-stu-id="b42d6-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="b42d6-106">Commercen arviointiympäristöt eivät ole yleisesti saatavana, ja ne myönnetään kumppaneille ja asiakkaille pyyntökohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="b42d6-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="b42d6-107">Pyydä lisätietoja Microsoft-kumppanilta.</span><span class="sxs-lookup"><span data-stu-id="b42d6-107">For more information, reach out to your Microsoft partner contact.</span></span>

<span data-ttu-id="b42d6-108">Commercen arviointiympäristön onnistunut valmistelu edellyttää sellaisen projektin luontia, jossa on tietty tuotteen nimi ja tyyppi.</span><span class="sxs-lookup"><span data-stu-id="b42d6-108">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="b42d6-109">Ympäristöllä ja Commerce Scale Unit (CSU) -ratkaisulla on myös joitakin tiettyjä parametreja, joita on käytettävä, jos oletat valmistelevasi sähköisen kaupankäynnin myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="b42d6-109">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="b42d6-110">Tämän ohjeaiheen ohjeissa kuvataan kaikki vaiheet, joita tarvitaan valmisteluun, ja parametrit, joita on käytettävä.</span><span class="sxs-lookup"><span data-stu-id="b42d6-110">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="b42d6-111">Kun olet onnistuneesti valmistellut Commercen arviointiympäristön, sinun on suoritettava muutama valmistelun jälkeinen vaihe sen käyttöönottamista varten.</span><span class="sxs-lookup"><span data-stu-id="b42d6-111">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="b42d6-112">Jotkin vaiheet ovat valinnaisia. Tämä riippuu siitä, mitä järjestelmän alueita haluat arvioida.</span><span class="sxs-lookup"><span data-stu-id="b42d6-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="b42d6-113">Voit aina suorittaa valinnaiset vaiheet myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="b42d6-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="b42d6-114">Lisätietoja Commercen arviointiympäristön määrittämistä valmistelun jälkeen on kohdassa [Commercen arviointiympäristön määrittäminen](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="b42d6-114">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="b42d6-115">Lisätietoja Commercen arviointiympäristön valinnaisten ominaisuuksien määrittämisestä on kohdassa [Commercen arviointiympäristön valinnaisten ominaisuuksien määrittäminen](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="b42d6-115">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b42d6-116">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="b42d6-116">Prerequisites</span></span>

<span data-ttu-id="b42d6-117">Seuraavien edellytysten on oltava käytössä, ennen kuin voit määrittää Commercen arviointiympäristön:</span><span class="sxs-lookup"><span data-stu-id="b42d6-117">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="b42d6-118">Sinut on otettu mukaan arviointiohjelmaan ja sinulle on annettu kapsiteettia arviointiympäristöä varten.</span><span class="sxs-lookup"><span data-stu-id="b42d6-118">You have been onboarded into the evaluation program and granted capacity for an evaluation environment.</span></span>
- <span data-ttu-id="b42d6-119">Sinulla on Microsoft Dynamics Lifecycle Services -portaalin (LCS) käyttöoikeus</span><span class="sxs-lookup"><span data-stu-id="b42d6-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="b42d6-120">Olet aiemmin luotu Microsoft Dynamics 365 -kumppani tai -asiakas ja pystyt luomaan Dynamics 365 Commerce -projektin.</span><span class="sxs-lookup"><span data-stu-id="b42d6-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="b42d6-121">Sinulla on Microsoft Azure -tilauksen järjestelmänvalvojan käyttöoikeus tai olet yhteydessä tilauksen järjestelmänvalvojaan, joka voi avustaa tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="b42d6-121">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="b42d6-122">Sinulla on käytettävissä Azure Active Directory (Azure AD) -vuokralaisen tunnus.</span><span class="sxs-lookup"><span data-stu-id="b42d6-122">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="b42d6-123">Olet luonut Azure AD -käyttöoikeusryhmän, jota voidaan käyttää sähköisen kaupankäynnin järjestelmänvalvojien ryhmänä, ja sinulla on ryhmän tunnus.</span><span class="sxs-lookup"><span data-stu-id="b42d6-123">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="b42d6-124">Olet luonut Azure AD -käyttöoikeusryhmän, jota voidaan käyttää arviot ja arvostelut -moderaattorien ryhmänä, ja sinulla on ryhmän tunnus.</span><span class="sxs-lookup"><span data-stu-id="b42d6-124">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="b42d6-125">(Tämä suojausryhmä voi olla sama kuin verkkokauppajärjestelmän järjestelmänvalvojaryhmä.)</span><span class="sxs-lookup"><span data-stu-id="b42d6-125">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="b42d6-126">Huomaa, että tämä luettelo ei ole täydellinen.</span><span class="sxs-lookup"><span data-stu-id="b42d6-126">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="b42d6-127">Jos ongelmia esiintyy, ota yhteys Microsoft-kumppaniin.</span><span class="sxs-lookup"><span data-stu-id="b42d6-127">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="b42d6-128">Commercen arviointiympäristön valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="b42d6-128">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="b42d6-129">Näissä ohjeissa käsitellään Commercen arviointiympäristö valmistelua.</span><span class="sxs-lookup"><span data-stu-id="b42d6-129">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="b42d6-130">Kun olet suorittanut ne onnistuneesti, Commercen arviointiympäristö on valmis määritettäväksi.</span><span class="sxs-lookup"><span data-stu-id="b42d6-130">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="b42d6-131">Kaikki tässä kuvatut toiminnot tapahtuvat LCS-portaalissa.</span><span class="sxs-lookup"><span data-stu-id="b42d6-131">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="b42d6-132">Luo uusi projekti</span><span class="sxs-lookup"><span data-stu-id="b42d6-132">Create a new project</span></span>

<span data-ttu-id="b42d6-133">Noudata seuraavia vaiheita luodaksesi uuden projektin LCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="b42d6-133">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="b42d6-134">Luo projekti valitsemalla LCS-aloitussivulla plusmerkki (**+**).</span><span class="sxs-lookup"><span data-stu-id="b42d6-134">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="b42d6-135">Noudata oikeanpuoleisessa ruudussa jotakin näistä vaiheista:</span><span class="sxs-lookup"><span data-stu-id="b42d6-135">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="b42d6-136">Jos olet kumppani, valitse **Siirrä, luo ratkaisuja ja opi**.</span><span class="sxs-lookup"><span data-stu-id="b42d6-136">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="b42d6-137">Jos olet asiakas, valitse **Mahdolliset myyntiä edeltävät toimet**.</span><span class="sxs-lookup"><span data-stu-id="b42d6-137">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="b42d6-138">Syötä mallin nimi, kuvaus ja toimiala.</span><span class="sxs-lookup"><span data-stu-id="b42d6-138">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="b42d6-139">Valitse **Tuotenimi** -kentässä **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="b42d6-139">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="b42d6-140">Valitse **Tuoteversio**-kentässä **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="b42d6-140">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="b42d6-141">Valitse **Metodologia**-kentässä **Dynamics Retail -implementointimetodologia**.</span><span class="sxs-lookup"><span data-stu-id="b42d6-141">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="b42d6-142">Valinnainen: Voit tuoda rooleja ja käyttäjiä aiemmin luodusta projektista.</span><span class="sxs-lookup"><span data-stu-id="b42d6-142">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="b42d6-143">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="b42d6-143">Select **Create**.</span></span> <span data-ttu-id="b42d6-144">Projektinäkymä avautuu.</span><span class="sxs-lookup"><span data-stu-id="b42d6-144">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="b42d6-145">Azure-yhdistimen lisääminen</span><span class="sxs-lookup"><span data-stu-id="b42d6-145">Add the Azure Connector</span></span>

<span data-ttu-id="b42d6-146">Lisää Azure Connector LCS-projektiin kohdassa [Azure Resource Manager (ARM) -perehdytyksen suorittaminen](../fin-ops-core/dev-itpro/deployment/arm-onboarding.md) olevien ohjeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="b42d6-146">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](../fin-ops-core/dev-itpro/deployment/arm-onboarding.md).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="b42d6-147">Käyttöönottoympäristö</span><span class="sxs-lookup"><span data-stu-id="b42d6-147">Deploy the environment</span></span>

<span data-ttu-id="b42d6-148">Määritä ympäristö näiden ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="b42d6-148">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="b42d6-149">Vaiheita 6, 7 ja/tai 8 ei ehkä tarvitse suorittaa, koska sivut, joilla on yksi vaihtoehto, ohitetaan.</span><span class="sxs-lookup"><span data-stu-id="b42d6-149">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="b42d6-150">Kun olet **Ympäristön parametrit** -näkymässä, varmista, että teksti **Dynamics 365 Commerce - esittely (10.0.* x* ja Platform-päivitys *xx*)\*\* näkyy suoraan **Ympäristön nimi** -kentän yläpuolella.</span><span class="sxs-lookup"><span data-stu-id="b42d6-150">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="b42d6-151">Katso tiedot vaiheen 8 jälkeen näkyvästä kuvasta.</span><span class="sxs-lookup"><span data-stu-id="b42d6-151">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="b42d6-152">Valitse päävalikosta **Pilvipalveluympäristöt**.</span><span class="sxs-lookup"><span data-stu-id="b42d6-152">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="b42d6-153">Valitse **+ Lisää** lisätäksesi ympäristön.</span><span class="sxs-lookup"><span data-stu-id="b42d6-153">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="b42d6-154">Valitse **Sovelluksen versio** -kentässä uusin versio.</span><span class="sxs-lookup"><span data-stu-id="b42d6-154">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="b42d6-155">Jos sinulla on erityinen tarve valita jokin muu sovellusversio kuin uusin versio, älä valitse vanhempaa versiota kuin **10.0.14.**</span><span class="sxs-lookup"><span data-stu-id="b42d6-155">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.14**.</span></span>
1. <span data-ttu-id="b42d6-156">Käytä **Käyttöympäristön versio** -kentässä käyttöympäristö versiota, joka valitaan automaattisesti valitsemaasi sovellusversioon.</span><span class="sxs-lookup"><span data-stu-id="b42d6-156">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Sovelluksen ja ympäristön versioiden valitseminen](./media/project1.png)

1. <span data-ttu-id="b42d6-158">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="b42d6-158">Select **Next**.</span></span>
1. <span data-ttu-id="b42d6-159">Valitse **Esittely** ympäristötopologiaksi.</span><span class="sxs-lookup"><span data-stu-id="b42d6-159">Select **Demo** as the environment topology.</span></span>

    ![Ympäristötopologia 1 valitseminen](./media/project2.png)

1. <span data-ttu-id="b42d6-161">Anna ympäristön nimi **Ympäristön käyttöönotto** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="b42d6-161">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="b42d6-162">Älä muuta Lisäasetukset-kohtaa.</span><span class="sxs-lookup"><span data-stu-id="b42d6-162">Leave the advanced settings as they are.</span></span>

    ![Ympäristön käyttöönotto -sivu](./media/project4.png)

1. <span data-ttu-id="b42d6-164">Säädä VM:n kokoa tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="b42d6-164">Adjust the VM size as required.</span></span> <span data-ttu-id="b42d6-165">(Suosittelemme VM:n varastointiyksikköä \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="b42d6-165">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="b42d6-166">Tarkista hinnoittelu- ja lisensointiehdot ja valitse sitten valintaruutu, jos hyväksyt ne.</span><span class="sxs-lookup"><span data-stu-id="b42d6-166">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="b42d6-167">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="b42d6-167">Select **Next**.</span></span>
1. <span data-ttu-id="b42d6-168">Kun tietojen oikeellisuus on vahvistettu käyttöönoton vahvistussivulla, valitse **Ota käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="b42d6-168">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="b42d6-169">Sinut siirretään **Pilvipalveluympäristöt**-näkymään ja ympäristösi pitäisi näkyä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="b42d6-169">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="b42d6-170">Pyydetty ympäristö näkyy jonossa. Tämän jälkeen se otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="b42d6-170">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="b42d6-171">Ympäristön työnkulut kestävät jonkin aikaa.</span><span class="sxs-lookup"><span data-stu-id="b42d6-171">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="b42d6-172">Tarkista tilanne, kun aikaa on kulunut noin kuudesta yhdeksään tuntiin.</span><span class="sxs-lookup"><span data-stu-id="b42d6-172">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="b42d6-173">Varmista ennen jatkamista, että ympäristösi tila on **Otettu käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="b42d6-173">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="b42d6-174">Alusta Commerce Scale Unit (pilvi)</span><span class="sxs-lookup"><span data-stu-id="b42d6-174">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="b42d6-175">Alusta CSU seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="b42d6-175">To initialize the CSU, follow these steps.</span></span>

1. <span data-ttu-id="b42d6-176">Valitse **Pilvipalveluympäristöt**-näkymässä luettelosta ympäristösi.</span><span class="sxs-lookup"><span data-stu-id="b42d6-176">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="b42d6-177">Valitse oikealla olevasta ympäristön näkymästä **Täydet tiedot**.</span><span class="sxs-lookup"><span data-stu-id="b42d6-177">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="b42d6-178">Näkyviin tulee ympäristön tietojen näkymä.</span><span class="sxs-lookup"><span data-stu-id="b42d6-178">The environment details view appears.</span></span>
1. <span data-ttu-id="b42d6-179">Valitse **Ympäristön ominaisuudet** -kohdassa **Hallitse**.</span><span class="sxs-lookup"><span data-stu-id="b42d6-179">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="b42d6-180">Valitse **Commerce**-välilehdestä **Alusta**.</span><span class="sxs-lookup"><span data-stu-id="b42d6-180">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="b42d6-181">Näkyviin tulee CSU-alustusparametrien näkymä.</span><span class="sxs-lookup"><span data-stu-id="b42d6-181">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="b42d6-182">Valitse **Alue**-kentässä alue, joka on sama alue tai lähellä sitä aluetta, jossa ympäristö otettiin käyttöön.</span><span class="sxs-lookup"><span data-stu-id="b42d6-182">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="b42d6-183">Älä tee muutoksia **Versio**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b42d6-183">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="b42d6-184">Valitse **Alusta**.</span><span class="sxs-lookup"><span data-stu-id="b42d6-184">Select **Initialize**.</span></span>
1. <span data-ttu-id="b42d6-185">Kun tietojen oikeellisuus on vahvistettu käyttöönoton vahvistussivulla, valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="b42d6-185">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="b42d6-186">**Commercen hallinta** -näkymä tulee uudelleen näkyviin, kun **Commerce**-välilehti on valittuna.</span><span class="sxs-lookup"><span data-stu-id="b42d6-186">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="b42d6-187">CSU on asetettu jonoon valmistelua varten.</span><span class="sxs-lookup"><span data-stu-id="b42d6-187">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="b42d6-188">Varmista ennen jatkamista, että CSU:si tila on **Onnistunut**.</span><span class="sxs-lookup"><span data-stu-id="b42d6-188">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="b42d6-189">Alustus kestää noin kahdesta viiteen tuntia.</span><span class="sxs-lookup"><span data-stu-id="b42d6-189">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="b42d6-190">Jos **Hallinta**-linkki ei ole ympäristön tietonäkymässä, ota yhteys Microsoftin yhteyshenkilöön.</span><span class="sxs-lookup"><span data-stu-id="b42d6-190">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

<span data-ttu-id="b42d6-191">Seuraava virhesanoma saattaa tulla näyttöön käyttöönottoprosessin aikana:</span><span class="sxs-lookup"><span data-stu-id="b42d6-191">During the deployment process, you might receive the following error message:</span></span>

> <span data-ttu-id="b42d6-192">Arviointiympäristöjen (esittely/testi) on rekisteröitävä Scale Unit Connector -sovellus \<application ID\> headquarters-sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="b42d6-192">Evaluation (demo/test) environments need to register the scale unit connector application \<application ID\> in headquarters.</span></span>

<span data-ttu-id="b42d6-193">Jos CSU-alustus epäonnistuu ja näyttöön tulee tämä virhesanoma, merkitse muistiin sovelluksen tunnus, joka on yleinen yksilöivä tunnus (GUID) ja rekisteröi CSU-käyttöönottosovellus Commerce headquarters -sovelluksessa noudattamalla seuraavan osan ohjeita.</span><span class="sxs-lookup"><span data-stu-id="b42d6-193">If the CSU initialization fails and you receive this error message, make a note of the application ID, which is a globally unique identifier (GUID), and then follow the steps in the next section to register the CSU deployment application in Commerce headquarters.</span></span>

### <a name="register-the-csu-deployment-application-in-commerce-headquarters-if-required"></a><span data-ttu-id="b42d6-194">Rekisteröi CSU-käyttöönottosovellus Commerce headquarters -sovelluksessa (jos pakollinen).</span><span class="sxs-lookup"><span data-stu-id="b42d6-194">Register the CSU deployment application in Commerce headquarters (if required)</span></span>

<span data-ttu-id="b42d6-195">Rekisteröi CSU-käyttöönottosovellus Commerce headquarters -sovelluksessa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="b42d6-195">To register the CSU deployment application in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="b42d6-196">Siirry Commerce headquarters -sovelluksessa kohtaan **Järjestelmän hallinta \> Asetukset \> Azure Active Directory -sovellukset**.</span><span class="sxs-lookup"><span data-stu-id="b42d6-196">In Commerce headquarters, go to **System administration \> Setup \> Azure Active Directory applications**.</span></span>
1. <span data-ttu-id="b42d6-197">Kirjoita vastaanottamasi CSU-alustuksen virhesanoman sovellustunnus **Asiakastunnus**-sarakkeeseen.</span><span class="sxs-lookup"><span data-stu-id="b42d6-197">In the **Client Id** column, enter the application ID from the CSU initialization error message that you received.</span></span>
1. <span data-ttu-id="b42d6-198">Kirjoita **Nimi**-sarakkeeseen mikä tahansa kuvaava teksti (esimerkiksi **CSU Eval**).</span><span class="sxs-lookup"><span data-stu-id="b42d6-198">In the **Name** column, enter any descriptive text (for example, **CSU Eval**).</span></span>
1. <span data-ttu-id="b42d6-199">Kirjoita **Käyttäjätunnus**-sarakkeeseen **RetailServiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="b42d6-199">In the **User ID** column, enter **RetailServiceAccount**.</span></span>
1. <span data-ttu-id="b42d6-200">Yritä CSU-alustusta ja käyttöönottoa uudelleen LCS:stä.</span><span class="sxs-lookup"><span data-stu-id="b42d6-200">Retry the CSU initialization and deployment from LCS.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="b42d6-201">Sähköisen kaupankäynnin alustaminen</span><span class="sxs-lookup"><span data-stu-id="b42d6-201">Initialize e-Commerce</span></span>

<span data-ttu-id="b42d6-202">Alusta sähköinen kaupankäynti seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="b42d6-202">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="b42d6-203">Tarkista arviointiversion suostumus **Sähköinen kaupankäynti**-välilehdessä ja valitse sitten **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="b42d6-203">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="b42d6-204">Anna **Sähköisen kaupankäynnin ympäristön nimi** -kenttään nimi.</span><span class="sxs-lookup"><span data-stu-id="b42d6-204">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="b42d6-205">Ota huomioon, että tämä nimi näkyy joissakin sähköisen kaupankäynnin esiintymään vievissä URL-osoitteissa.</span><span class="sxs-lookup"><span data-stu-id="b42d6-205">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="b42d6-206">Valitse **Commerce Scale Unitin nimi** -kentässä CSU-luettelosta.</span><span class="sxs-lookup"><span data-stu-id="b42d6-206">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="b42d6-207">(Luettelossa pitäisi olla vain yksi vaihtoehto.)</span><span class="sxs-lookup"><span data-stu-id="b42d6-207">(The list should have only one option.)</span></span>

    <span data-ttu-id="b42d6-208">**Sähköisen kaupankäynnin maantieteellinen alue** -kenttä täytetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="b42d6-208">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="b42d6-209">Jatka valitsemalla **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="b42d6-209">Select **Next** to continue.</span></span>
1. <span data-ttu-id="b42d6-210">Kirjoita **Tuetut isäntänimet** -kenttään mikä tahansa kelvollinen toimialue, kuten `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="b42d6-210">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="b42d6-211">Anna **Järjestelmänvalvojan AAD-käyttöoikeusryhmä** -kentässä käytettävän käyttöoikeusryhmän nimen kaksi ensimmäistä kirjainta ja näytä sitten hakutulokset valitsemalla suurennuslasikuvake.</span><span class="sxs-lookup"><span data-stu-id="b42d6-211">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="b42d6-212">Valitse luettelossa oikea käyttöoikeusryhmä.</span><span class="sxs-lookup"><span data-stu-id="b42d6-212">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="b42d6-213">Anna **Luokitusten ja arvostelujen valvojan AAD-käyttöoikeusryhmä** -kentässä käytettävän käyttöoikeusryhmän nimen kaksi ensimmäistä kirjainta ja näytä sitten hakutulokset valitsemalla suurennuslasikuvake.</span><span class="sxs-lookup"><span data-stu-id="b42d6-213">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="b42d6-214">Valitse luettelossa oikea käyttöoikeusryhmä.</span><span class="sxs-lookup"><span data-stu-id="b42d6-214">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="b42d6-215">Jätä **Ota luokitukset ja arvostelupalvelu käyttöön** -asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="b42d6-215">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="b42d6-216">Valitse **Alusta**.</span><span class="sxs-lookup"><span data-stu-id="b42d6-216">Select **Initialize**.</span></span> <span data-ttu-id="b42d6-217">**Commercen hallinta** -näkymä tulee uudelleen näkyviin, kun **e-Commerce**-välilehti on valittuna.</span><span class="sxs-lookup"><span data-stu-id="b42d6-217">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="b42d6-218">Sähköisen kaupankäynnin alustaminen on aloitettu.</span><span class="sxs-lookup"><span data-stu-id="b42d6-218">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="b42d6-219">Ennen kuin jatkat, odota, kunnes sähköisen kaupankäynnin alustamisen tila on **Alustaminen onnistui**.</span><span class="sxs-lookup"><span data-stu-id="b42d6-219">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="b42d6-220">Merkitse oikeassa alakulmassa olevassa **Linkit**-kohdassa seuraavien linkkien URL-osoitteet:</span><span class="sxs-lookup"><span data-stu-id="b42d6-220">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="b42d6-221">**Sähköisen kaupankäynnin sivusto** – linkki verkkokaupan sivustosi juureen.</span><span class="sxs-lookup"><span data-stu-id="b42d6-221">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="b42d6-222">**Commerce-sivuston luontiohjelma** – linkki sivuston hallintatyökaluun.</span><span class="sxs-lookup"><span data-stu-id="b42d6-222">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b42d6-223">Seuraavat vaiheet</span><span class="sxs-lookup"><span data-stu-id="b42d6-223">Next steps</span></span>

<span data-ttu-id="b42d6-224">Tietoja Commercen arviointiympäristön valmistelu- ja määritysprosessin jatkamisesta on kohdassa [Commercen arviointiympäristön määrittäminen](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="b42d6-224">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b42d6-225">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b42d6-225">Additional resources</span></span>

[<span data-ttu-id="b42d6-226">Dynamics 365 Commerce -arviointiympäristön yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="b42d6-226">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="b42d6-227">Dynamics 365 Commerce -arviointiympäristön määritykset</span><span class="sxs-lookup"><span data-stu-id="b42d6-227">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="b42d6-228">BOPIS:n määritykset Dynamics 365 Commerce -arviointiympäristössä</span><span class="sxs-lookup"><span data-stu-id="b42d6-228">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="b42d6-229">Dynamics 365 Commerce -arviointiympäristön valinnaisten ominaisuuksien määritykset</span><span class="sxs-lookup"><span data-stu-id="b42d6-229">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="b42d6-230">Dynamics 365 Commerce -arviointiympäristön usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="b42d6-230">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="b42d6-231">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="b42d6-231">Microsoft Lifecycle Services (LCS)</span></span>](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="b42d6-232">Commerce Scale Unit (pilvi)</span><span class="sxs-lookup"><span data-stu-id="b42d6-232">Commerce Scale Unit (cloud)</span></span>](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="b42d6-233">Microsoft Azure -portaali</span><span class="sxs-lookup"><span data-stu-id="b42d6-233">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="b42d6-234">Dynamics 365 Commerce -sivusto</span><span class="sxs-lookup"><span data-stu-id="b42d6-234">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]