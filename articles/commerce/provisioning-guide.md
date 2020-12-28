---
title: Dynamics 365 Commerce -arviointiympäristön valmisteleminen
description: Tässä ohjeaiheessa kerrotaan, kuinka voit valmistella Microsoft Dynamics 365 Commercen arviointiympäristön.
author: psimolin
manager: annbe
ms.date: 11/05/2020
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
ms.openlocfilehash: b54216a565c264dfcfe821581fee9df7b5e22323
ms.sourcegitcommit: 715508547f9a71a89a138190e8540686556c753d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/05/2020
ms.locfileid: "4412126"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="6253c-103">Dynamics 365 Commerce -arviointiympäristön valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="6253c-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6253c-104">Tässä ohjeaiheessa kerrotaan, kuinka voit valmistella Microsoft Dynamics 365 Commercen arviointiympäristön.</span><span class="sxs-lookup"><span data-stu-id="6253c-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="6253c-105">Ennen kuin aloitat, suosittelemme, että tarkistat tämän aiheen nopeasti, jotta saat käsityksen prosessin vaatimista aiheista.</span><span class="sxs-lookup"><span data-stu-id="6253c-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="6253c-106">Commercen arviointiympäristöt eivät ole yleisesti saatavana, ja ne myönnetään kumppaneille ja asiakkaille pyyntökohtaisesti.</span><span class="sxs-lookup"><span data-stu-id="6253c-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="6253c-107">Pyydä lisätietoja Microsoft-kumppanilta.</span><span class="sxs-lookup"><span data-stu-id="6253c-107">For more information, reach out to your Microsoft partner contact.</span></span>

## <a name="overview"></a><span data-ttu-id="6253c-108">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="6253c-108">Overview</span></span>

<span data-ttu-id="6253c-109">Commercen arviointiympäristön onnistunut valmistelu edellyttää sellaisen projektin luontia, jossa on tietty tuotteen nimi ja tyyppi.</span><span class="sxs-lookup"><span data-stu-id="6253c-109">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="6253c-110">Ympäristöllä ja Commerce Scale Unit (CSU) -ratkaisulla on myös joitakin tiettyjä parametreja, joita on käytettävä, jos oletat valmistelevasi sähköisen kaupankäynnin myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="6253c-110">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="6253c-111">Tämän ohjeaiheen ohjeissa kuvataan kaikki vaiheet, joita tarvitaan valmisteluun, ja parametrit, joita on käytettävä.</span><span class="sxs-lookup"><span data-stu-id="6253c-111">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="6253c-112">Kun olet onnistuneesti valmistellut Commercen arviointiympäristön, sinun on suoritettava muutama valmistelun jälkeinen vaihe sen käyttöönottamista varten.</span><span class="sxs-lookup"><span data-stu-id="6253c-112">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="6253c-113">Jotkin vaiheet ovat valinnaisia. Tämä riippuu siitä, mitä järjestelmän alueita haluat arvioida.</span><span class="sxs-lookup"><span data-stu-id="6253c-113">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="6253c-114">Voit aina suorittaa valinnaiset vaiheet myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="6253c-114">You can always complete the optional steps later.</span></span>

<span data-ttu-id="6253c-115">Lisätietoja Commercen arviointiympäristön määrittämistä valmistelun jälkeen on kohdassa [Commercen arviointiympäristön määrittäminen](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="6253c-115">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="6253c-116">Lisätietoja Commercen arviointiympäristön valinnaisten ominaisuuksien määrittämisestä on kohdassa [Commercen arviointiympäristön valinnaisten ominaisuuksien määrittäminen](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="6253c-116">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6253c-117">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="6253c-117">Prerequisites</span></span>

<span data-ttu-id="6253c-118">Seuraavien edellytysten on oltava käytössä, ennen kuin voit määrittää Commercen arviointiympäristön:</span><span class="sxs-lookup"><span data-stu-id="6253c-118">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="6253c-119">Sinut on otettu mukaan arviointiohjelmaan ja sinulle on annettu kapsiteettia arviointiympäristöä varten.</span><span class="sxs-lookup"><span data-stu-id="6253c-119">You have been onboarded into the evaluation program and granted capacity for an evaluation environment.</span></span>
- <span data-ttu-id="6253c-120">Sinulla on Microsoft Dynamics Lifecycle Services -portaalin (LCS) käyttöoikeus</span><span class="sxs-lookup"><span data-stu-id="6253c-120">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="6253c-121">Olet aiemmin luotu Microsoft Dynamics 365 -kumppani tai -asiakas ja pystyt luomaan Dynamics 365 Commerce -projektin.</span><span class="sxs-lookup"><span data-stu-id="6253c-121">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="6253c-122">Sinulla on Microsoft Azure -tilauksen järjestelmänvalvojan käyttöoikeus tai olet yhteydessä tilauksen järjestelmänvalvojaan, joka voi avustaa tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="6253c-122">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="6253c-123">Sinulla on käytettävissä Azure Active Directory (Azure AD) -vuokralaisen tunnus.</span><span class="sxs-lookup"><span data-stu-id="6253c-123">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="6253c-124">Olet luonut Azure AD -käyttöoikeusryhmän, jota voidaan käyttää sähköisen kaupankäynnin järjestelmänvalvojien ryhmänä, ja sinulla on ryhmän tunnus.</span><span class="sxs-lookup"><span data-stu-id="6253c-124">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="6253c-125">Olet luonut Azure AD -käyttöoikeusryhmän, jota voidaan käyttää arviot ja arvostelut -moderaattorien ryhmänä, ja sinulla on ryhmän tunnus.</span><span class="sxs-lookup"><span data-stu-id="6253c-125">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="6253c-126">(Tämä suojausryhmä voi olla sama kuin verkkokauppajärjestelmän järjestelmänvalvojaryhmä.)</span><span class="sxs-lookup"><span data-stu-id="6253c-126">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="6253c-127">Huomaa, että tämä luettelo ei ole täydellinen.</span><span class="sxs-lookup"><span data-stu-id="6253c-127">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="6253c-128">Jos ongelmia esiintyy, ota yhteys Microsoft-kumppaniin.</span><span class="sxs-lookup"><span data-stu-id="6253c-128">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="6253c-129">Commercen arviointiympäristön valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="6253c-129">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="6253c-130">Näissä ohjeissa käsitellään Commercen arviointiympäristö valmistelua.</span><span class="sxs-lookup"><span data-stu-id="6253c-130">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="6253c-131">Kun olet suorittanut ne onnistuneesti, Commercen arviointiympäristö on valmis määritettäväksi.</span><span class="sxs-lookup"><span data-stu-id="6253c-131">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="6253c-132">Kaikki tässä kuvatut toiminnot tapahtuvat LCS-portaalissa.</span><span class="sxs-lookup"><span data-stu-id="6253c-132">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="6253c-133">Luo uusi projekti</span><span class="sxs-lookup"><span data-stu-id="6253c-133">Create a new project</span></span>

<span data-ttu-id="6253c-134">Noudata seuraavia vaiheita luodaksesi uuden projektin LCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="6253c-134">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="6253c-135">Luo projekti valitsemalla LCS-aloitussivulla plusmerkki (**+**).</span><span class="sxs-lookup"><span data-stu-id="6253c-135">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="6253c-136">Noudata oikeanpuoleisessa ruudussa jotakin näistä vaiheista:</span><span class="sxs-lookup"><span data-stu-id="6253c-136">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="6253c-137">Jos olet kumppani, valitse **Siirrä, luo ratkaisuja ja opi**.</span><span class="sxs-lookup"><span data-stu-id="6253c-137">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="6253c-138">Jos olet asiakas, valitse **Mahdolliset myyntiä edeltävät toimet**.</span><span class="sxs-lookup"><span data-stu-id="6253c-138">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="6253c-139">Syötä mallin nimi, kuvaus ja toimiala.</span><span class="sxs-lookup"><span data-stu-id="6253c-139">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="6253c-140">Valitse **Tuotenimi** -kentässä **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="6253c-140">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="6253c-141">Valitse **Tuoteversio**-kentässä **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="6253c-141">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="6253c-142">Valitse **Metodologia**-kentässä **Dynamics Retail -implementointimetodologia**.</span><span class="sxs-lookup"><span data-stu-id="6253c-142">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="6253c-143">Valinnainen: Voit tuoda rooleja ja käyttäjiä aiemmin luodusta projektista.</span><span class="sxs-lookup"><span data-stu-id="6253c-143">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="6253c-144">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="6253c-144">Select **Create**.</span></span> <span data-ttu-id="6253c-145">Projektinäkymä avautuu.</span><span class="sxs-lookup"><span data-stu-id="6253c-145">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="6253c-146">Azure-yhdistimen lisääminen</span><span class="sxs-lookup"><span data-stu-id="6253c-146">Add the Azure Connector</span></span>

<span data-ttu-id="6253c-147">Lisää Azure Connector LCS-projektiin kohdassa [Azure Resource Manager (ARM) -perehdytyksen suorittaminen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding) olevien ohjeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="6253c-147">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="6253c-148">Käyttöönottoympäristö</span><span class="sxs-lookup"><span data-stu-id="6253c-148">Deploy the environment</span></span>

<span data-ttu-id="6253c-149">Määritä ympäristö näiden ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="6253c-149">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="6253c-150">Vaiheita 6, 7 ja/tai 8 ei ehkä tarvitse suorittaa, koska sivut, joilla on yksi vaihtoehto, ohitetaan.</span><span class="sxs-lookup"><span data-stu-id="6253c-150">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="6253c-151">Kun olet **Ympäristön parametrit** -näkymässä, varmista, että teksti **Dynamics 365 Commerce - esittely (10.0.* x* ja Platform-päivitys *xx*)\*\* näkyy suoraan **Ympäristön nimi** -kentän yläpuolella.</span><span class="sxs-lookup"><span data-stu-id="6253c-151">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="6253c-152">Katso tiedot vaiheen 8 jälkeen näkyvästä kuvasta.</span><span class="sxs-lookup"><span data-stu-id="6253c-152">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="6253c-153">Valitse päävalikosta **Pilvipalveluympäristöt**.</span><span class="sxs-lookup"><span data-stu-id="6253c-153">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="6253c-154">Valitse **+ Lisää** lisätäksesi ympäristön.</span><span class="sxs-lookup"><span data-stu-id="6253c-154">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="6253c-155">Valitse **Sovelluksen versio** -kentässä uusin versio.</span><span class="sxs-lookup"><span data-stu-id="6253c-155">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="6253c-156">Jos sinulla on erityinen tarve valita jokin muu sovellusversio kuin uusin versio, älä valitse vanhempaa versiota kuin **10.0.14.**</span><span class="sxs-lookup"><span data-stu-id="6253c-156">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.14**.</span></span>
1. <span data-ttu-id="6253c-157">Käytä **Käyttöympäristön versio** -kentässä käyttöympäristö versiota, joka valitaan automaattisesti valitsemaasi sovellusversioon.</span><span class="sxs-lookup"><span data-stu-id="6253c-157">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Sovelluksen ja ympäristön versioiden valitseminen](./media/project1.png)

1. <span data-ttu-id="6253c-159">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="6253c-159">Select **Next**.</span></span>
1. <span data-ttu-id="6253c-160">Valitse **Esittely** ympäristötopologiaksi.</span><span class="sxs-lookup"><span data-stu-id="6253c-160">Select **Demo** as the environment topology.</span></span>

    ![Ympäristötopologia 1 valitseminen](./media/project2.png)

1. <span data-ttu-id="6253c-162">Anna ympäristön nimi **Ympäristön käyttöönotto** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="6253c-162">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="6253c-163">Älä muuta Lisäasetukset-kohtaa.</span><span class="sxs-lookup"><span data-stu-id="6253c-163">Leave the advanced settings as they are.</span></span>

    ![Ympäristön käyttöönotto -sivu](./media/project4.png)

1. <span data-ttu-id="6253c-165">Säädä VM:n kokoa tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="6253c-165">Adjust the VM size as required.</span></span> <span data-ttu-id="6253c-166">(Suosittelemme VM:n varastointiyksikköä \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="6253c-166">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="6253c-167">Tarkista hinnoittelu- ja lisensointiehdot ja valitse sitten valintaruutu, jos hyväksyt ne.</span><span class="sxs-lookup"><span data-stu-id="6253c-167">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="6253c-168">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="6253c-168">Select **Next**.</span></span>
1. <span data-ttu-id="6253c-169">Kun tietojen oikeellisuus on vahvistettu käyttöönoton vahvistussivulla, valitse **Ota käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="6253c-169">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="6253c-170">Sinut siirretään **Pilvipalveluympäristöt**-näkymään ja ympäristösi pitäisi näkyä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="6253c-170">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="6253c-171">Pyydetty ympäristö näkyy jonossa. Tämän jälkeen se otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="6253c-171">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="6253c-172">Ympäristön työnkulut kestävät jonkin aikaa.</span><span class="sxs-lookup"><span data-stu-id="6253c-172">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="6253c-173">Tarkista tilanne, kun aikaa on kulunut noin kuudesta yhdeksään tuntiin.</span><span class="sxs-lookup"><span data-stu-id="6253c-173">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="6253c-174">Varmista ennen jatkamista, että ympäristösi tila on **Otettu käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="6253c-174">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="6253c-175">Alusta Commerce Scale Unit (pilvi)</span><span class="sxs-lookup"><span data-stu-id="6253c-175">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="6253c-176">Alusta CSU-osoite seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="6253c-176">To initialize CSU, follow these steps.</span></span>

1. <span data-ttu-id="6253c-177">Valitse **Pilvipalveluympäristöt**-näkymässä luettelosta ympäristösi.</span><span class="sxs-lookup"><span data-stu-id="6253c-177">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="6253c-178">Valitse oikealla olevasta ympäristön näkymästä **Täydet tiedot**.</span><span class="sxs-lookup"><span data-stu-id="6253c-178">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="6253c-179">Näkyviin tulee ympäristön tietojen näkymä.</span><span class="sxs-lookup"><span data-stu-id="6253c-179">The environment details view appears.</span></span>
1. <span data-ttu-id="6253c-180">Valitse **Ympäristön ominaisuudet** -kohdassa **Hallitse**.</span><span class="sxs-lookup"><span data-stu-id="6253c-180">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="6253c-181">Valitse **Commerce**-välilehdestä **Alusta**.</span><span class="sxs-lookup"><span data-stu-id="6253c-181">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="6253c-182">Näkyviin tulee CSU-alustusparametrien näkymä.</span><span class="sxs-lookup"><span data-stu-id="6253c-182">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="6253c-183">Valitse **Alue**-kentässä alue, joka on sama alue tai lähellä sitä aluetta, jossa ympäristö otettiin käyttöön.</span><span class="sxs-lookup"><span data-stu-id="6253c-183">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="6253c-184">Älä tee muutoksia **Versio**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6253c-184">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="6253c-185">Valitse **Alusta**.</span><span class="sxs-lookup"><span data-stu-id="6253c-185">Select **Initialize**.</span></span>
1. <span data-ttu-id="6253c-186">Kun tietojen oikeellisuus on vahvistettu käyttöönoton vahvistussivulla, valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="6253c-186">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="6253c-187">**Commercen hallinta** -näkymä tulee uudelleen näkyviin, kun **Commerce**-välilehti on valittuna.</span><span class="sxs-lookup"><span data-stu-id="6253c-187">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="6253c-188">CSU on asetettu jonoon valmistelua varten.</span><span class="sxs-lookup"><span data-stu-id="6253c-188">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="6253c-189">Varmista ennen jatkamista, että CSU:si tila on **Onnistunut**.</span><span class="sxs-lookup"><span data-stu-id="6253c-189">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="6253c-190">Alustus kestää noin kahdesta viiteen tuntia.</span><span class="sxs-lookup"><span data-stu-id="6253c-190">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="6253c-191">Jos **Hallinta**-linkki ei ole ympäristön tietonäkymässä, ota yhteys Microsoftin yhteyshenkilöön.</span><span class="sxs-lookup"><span data-stu-id="6253c-191">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="6253c-192">Sähköisen kaupankäynnin alustaminen</span><span class="sxs-lookup"><span data-stu-id="6253c-192">Initialize e-Commerce</span></span>

<span data-ttu-id="6253c-193">Alusta sähköinen kaupankäynti seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="6253c-193">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="6253c-194">Tarkista arviointiversion suostumus **Sähköinen kaupankäynti**-välilehdessä ja valitse sitten **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="6253c-194">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="6253c-195">Anna **Sähköisen kaupankäynnin ympäristön nimi** -kenttään nimi.</span><span class="sxs-lookup"><span data-stu-id="6253c-195">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="6253c-196">Ota huomioon, että tämä nimi näkyy joissakin sähköisen kaupankäynnin esiintymään vievissä URL-osoitteissa.</span><span class="sxs-lookup"><span data-stu-id="6253c-196">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="6253c-197">Valitse **Commerce Scale Unitin nimi** -kentässä CSU-luettelosta.</span><span class="sxs-lookup"><span data-stu-id="6253c-197">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="6253c-198">(Luettelossa pitäisi olla vain yksi vaihtoehto.)</span><span class="sxs-lookup"><span data-stu-id="6253c-198">(The list should have only one option.)</span></span>

    <span data-ttu-id="6253c-199">**Sähköisen kaupankäynnin maantieteellinen alue** -kenttä täytetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="6253c-199">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="6253c-200">Jatka valitsemalla **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="6253c-200">Select **Next** to continue.</span></span>
1. <span data-ttu-id="6253c-201">Kirjoita **Tuetut isäntänimet** -kenttään mikä tahansa kelvollinen toimialue, kuten `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="6253c-201">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="6253c-202">Anna **Järjestelmänvalvojan AAD-käyttöoikeusryhmä** -kentässä käytettävän käyttöoikeusryhmän nimen kaksi ensimmäistä kirjainta ja näytä sitten hakutulokset valitsemalla suurennuslasikuvake.</span><span class="sxs-lookup"><span data-stu-id="6253c-202">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="6253c-203">Valitse luettelossa oikea käyttöoikeusryhmä.</span><span class="sxs-lookup"><span data-stu-id="6253c-203">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="6253c-204">Anna **Luokitusten ja arvostelujen valvojan AAD-käyttöoikeusryhmä** -kentässä käytettävän käyttöoikeusryhmän nimen kaksi ensimmäistä kirjainta ja näytä sitten hakutulokset valitsemalla suurennuslasikuvake.</span><span class="sxs-lookup"><span data-stu-id="6253c-204">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="6253c-205">Valitse luettelossa oikea käyttöoikeusryhmä.</span><span class="sxs-lookup"><span data-stu-id="6253c-205">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="6253c-206">Jätä **Ota luokitukset ja arvostelupalvelu käyttöön** -asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="6253c-206">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="6253c-207">Valitse **Alusta**.</span><span class="sxs-lookup"><span data-stu-id="6253c-207">Select **Initialize**.</span></span> <span data-ttu-id="6253c-208">**Commercen hallinta** -näkymä tulee uudelleen näkyviin, kun **e-Commerce**-välilehti on valittuna.</span><span class="sxs-lookup"><span data-stu-id="6253c-208">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="6253c-209">Sähköisen kaupankäynnin alustaminen on aloitettu.</span><span class="sxs-lookup"><span data-stu-id="6253c-209">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="6253c-210">Ennen kuin jatkat, odota, kunnes sähköisen kaupankäynnin alustamisen tila on **Alustaminen onnistui**.</span><span class="sxs-lookup"><span data-stu-id="6253c-210">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="6253c-211">Merkitse oikeassa alakulmassa olevassa **Linkit**-kohdassa seuraavien linkkien URL-osoitteet:</span><span class="sxs-lookup"><span data-stu-id="6253c-211">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="6253c-212">**Sähköisen kaupankäynnin sivusto** – linkki verkkokaupan sivustosi juureen.</span><span class="sxs-lookup"><span data-stu-id="6253c-212">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="6253c-213">**Commerce-sivuston luontiohjelma** – linkki sivuston hallintatyökaluun.</span><span class="sxs-lookup"><span data-stu-id="6253c-213">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="6253c-214">Seuraavat vaiheet</span><span class="sxs-lookup"><span data-stu-id="6253c-214">Next steps</span></span>

<span data-ttu-id="6253c-215">Tietoja Commercen arviointiympäristön valmistelu- ja määritysprosessin jatkamisesta on kohdassa [Commercen arviointiympäristön määrittäminen](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="6253c-215">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6253c-216">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="6253c-216">Additional resources</span></span>

[<span data-ttu-id="6253c-217">Dynamics 365 Commerce -arviointiympäristön yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="6253c-217">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="6253c-218">Dynamics 365 Commerce -arviointiympäristön määritykset</span><span class="sxs-lookup"><span data-stu-id="6253c-218">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="6253c-219">BOPIS:n määritykset Dynamics 365 Commerce -arviointiympäristössä</span><span class="sxs-lookup"><span data-stu-id="6253c-219">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="6253c-220">Dynamics 365 Commerce -arviointiympäristön valinnaisten ominaisuuksien määritykset</span><span class="sxs-lookup"><span data-stu-id="6253c-220">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="6253c-221">Dynamics 365 Commerce -arviointiympäristön usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="6253c-221">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="6253c-222">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="6253c-222">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="6253c-223">Commerce Scale Unit (pilvi)</span><span class="sxs-lookup"><span data-stu-id="6253c-223">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="6253c-224">Microsoft Azure -portaali</span><span class="sxs-lookup"><span data-stu-id="6253c-224">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="6253c-225">Dynamics 365 Commerce -sivusto</span><span class="sxs-lookup"><span data-stu-id="6253c-225">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
