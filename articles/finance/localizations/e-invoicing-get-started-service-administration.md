---
title: Sähköisen laskutuksen palvelun hallinnan aloittaminen
description: Tässä aiheessa selitetään, miten sähköisen laskutuksen käyttö voidaan aloittaa.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ec431cb4a3620459d905f64a80fd820a2113290f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840145"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a><span data-ttu-id="8cd01-103">Sähköisen laskutuksen palvelun hallinnan aloittaminen</span><span class="sxs-lookup"><span data-stu-id="8cd01-103">Get started with Electronic invoicing service administration</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="8cd01-104">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="8cd01-104">Prerequisites</span></span>

<span data-ttu-id="8cd01-105">Ennen kuin voit suorittaa tämän ohjeaiheen vaiheita, seuraavien edellytysten on toteuduttava:</span><span class="sxs-lookup"><span data-stu-id="8cd01-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="8cd01-106">Sinulla on oltava Microsoft Dynamics Lifecycle Services (LCS) -tili.</span><span class="sxs-lookup"><span data-stu-id="8cd01-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="8cd01-107">Käytössäsi on oltava LCS-projekti, joka sisältää Microsoft Dynamics 365 Financen ja Dynamics 365 Supply Chain Managementin version 10.0.17 tai sitä myöhemmän version.</span><span class="sxs-lookup"><span data-stu-id="8cd01-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="8cd01-108">Lisäksi nämä sovellukset on otettava käyttöön jossakin seuraavista Azure-alueista:</span><span class="sxs-lookup"><span data-stu-id="8cd01-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="8cd01-109">Itä-Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="8cd01-109">East US</span></span>
    - <span data-ttu-id="8cd01-110">Länsi-Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="8cd01-110">West US</span></span>
    - <span data-ttu-id="8cd01-111">Pohjois-EU</span><span class="sxs-lookup"><span data-stu-id="8cd01-111">North EU</span></span>
    - <span data-ttu-id="8cd01-112">Länsi-EU</span><span class="sxs-lookup"><span data-stu-id="8cd01-112">West EU</span></span>

- <span data-ttu-id="8cd01-113">Dynamics 365 Regulatory Configuration Services (RCS) -tilin on oltava käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="8cd01-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="8cd01-114">RCS-tilin globalisointiominaisuus on otettava käyttöön toiminnonhallinnan kautta.</span><span class="sxs-lookup"><span data-stu-id="8cd01-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="8cd01-115">Lisätietoja: [Regulatory Configuration Services (RCS) – globalisointitoiminnot](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="8cd01-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="8cd01-116">On luotava avainsäilö ja tallennustili Azuressa.</span><span class="sxs-lookup"><span data-stu-id="8cd01-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="8cd01-117">Lisätietoja: [Azure-tallennustilin ja -avainsäilön luominen](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="8cd01-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a><span data-ttu-id="8cd01-118">Microservices-lisäosan asentaminen Lifecycle Servicesissa</span><span class="sxs-lookup"><span data-stu-id="8cd01-118">Install the add-in for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="8cd01-119">Kirjaudu LCS-tilille.</span><span class="sxs-lookup"><span data-stu-id="8cd01-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="8cd01-120">Valitse **Esiversiotoiminnon hallinta** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="8cd01-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="8cd01-121">Valitse **Julkisen esiversion ominaisuudet** -osasta **Sähköisen laskutuksen palvelu**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="8cd01-122">Varmista, että **Esiversiotoiminto käytössä** -asetukseksi on valittu **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="8cd01-123">Valitse LCS-käyttöönottoprojekti LCS-koontinäytössä.</span><span class="sxs-lookup"><span data-stu-id="8cd01-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="8cd01-124">LCS-projektin on oltava käynnissä.</span><span class="sxs-lookup"><span data-stu-id="8cd01-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="8cd01-125">Valitse **Ympäristöapuohjelmat**-välilehdessä **Asenna uusi apuohjelma**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="8cd01-126">Valitse **sähköisen laskutuksen palvelut**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-126">Select **e-invoicing Services**.</span></span>
9. <span data-ttu-id="8cd01-127">Kirjoita **AAD-sovellustunnus**-kenttään **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-127">In the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="8cd01-128">Tämä on kiinteä arvo.</span><span class="sxs-lookup"><span data-stu-id="8cd01-128">This is a fixed value.</span></span>
10. <span data-ttu-id="8cd01-129">Syötä **AAD-vuokraajatunnus**-kenttään Azure-tilaustilisi vuokraajan tunnus.</span><span class="sxs-lookup"><span data-stu-id="8cd01-129">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="8cd01-130">Lue ehdot ja valitse valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="8cd01-130">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="8cd01-131">Valitse **Asenna**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-131">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a><span data-ttu-id="8cd01-132">Määritä RCS-integroinnin parametrit sähköisen laskutuksen avulla</span><span class="sxs-lookup"><span data-stu-id="8cd01-132">Set up the parameters for RCS integration with Electronic invoicing</span></span>

1. <span data-ttu-id="8cd01-133">Kirjaudu RCS-tilille.</span><span class="sxs-lookup"><span data-stu-id="8cd01-133">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="8cd01-134">Valitse **Sähköisen raportointi** -työtilan **Liittyvät linkit** -osassa **Sähköisen raportoinnin parametrit**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-134">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="8cd01-135">Kirjoita **Sähköisen laskutuksen palvelu** -välilehdessä **Palvelun päätepisteen URI** -kenttään asianmukainen Azure-alueen palvelun päätepiste, joka näkyy seuraavassa taulukossa.</span><span class="sxs-lookup"><span data-stu-id="8cd01-135">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="8cd01-136">Konesalin Azure-alue</span><span class="sxs-lookup"><span data-stu-id="8cd01-136">Datacenter Azure geography</span></span> | <span data-ttu-id="8cd01-137">Palvelun päätepisteen URI-osoite</span><span class="sxs-lookup"><span data-stu-id="8cd01-137">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="8cd01-138">Itä-Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="8cd01-138">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="8cd01-139">Länsi-Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="8cd01-139">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="8cd01-140">Pohjois-EU</span><span class="sxs-lookup"><span data-stu-id="8cd01-140">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="8cd01-141">Länsi-EU</span><span class="sxs-lookup"><span data-stu-id="8cd01-141">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="8cd01-142">Varmista, että **Sovellustunnus**-kentän arvo on **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-142">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="8cd01-143">Tämä arvo on kiinteä arvo.</span><span class="sxs-lookup"><span data-stu-id="8cd01-143">This value is a fixed value.</span></span>
5. <span data-ttu-id="8cd01-144">Syötä **LCS-ympäristötunnus**-kenttään LCS-ympäristösi tunnus.</span><span class="sxs-lookup"><span data-stu-id="8cd01-144">In the **LCS Environment Id** field, enter the ID of your LCS environment.</span></span>
6. <span data-ttu-id="8cd01-145">Valitse **Tallenna** ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="8cd01-145">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-references"></a><span data-ttu-id="8cd01-146">Avainsäilöviitteiden luominen</span><span class="sxs-lookup"><span data-stu-id="8cd01-146">Create Key Vault references</span></span>

1. <span data-ttu-id="8cd01-147">Kirjaudu RCS-tilille.</span><span class="sxs-lookup"><span data-stu-id="8cd01-147">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="8cd01-148">Valitse **Globalisaatio-ominaisuudet**-työtilan **Ympäristö**-osassa **Sähköinen laskutus** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="8cd01-148">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="8cd01-149">Valitse **Ympäristöasetukset**-sivun toimintoruudusta **Palveluympäristö** ja valitse sitten **Key Vault -parametrit**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-149">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="8cd01-150">Valitse **Uusi**, jos haluat luoda avainsäilön viitteen.</span><span class="sxs-lookup"><span data-stu-id="8cd01-150">Select **New** to create a key vault reference.</span></span>
5. <span data-ttu-id="8cd01-151">Syötä **Nimi**-kenttään avainsäilön viitteen nimi.</span><span class="sxs-lookup"><span data-stu-id="8cd01-151">In the **Name** field, enter the name of the key vault reference.</span></span> <span data-ttu-id="8cd01-152">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="8cd01-152">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="8cd01-153">Liitä **Key Vault – URI** -kenttään Azure Key Vaultin avainsäilön salainen koodi.</span><span class="sxs-lookup"><span data-stu-id="8cd01-153">In the **Key Vault URI** field, paste the key vault secret from Azure Key Vault.</span></span> <span data-ttu-id="8cd01-154">Lisätietoja: [Azure-tallennustilin ja -avainsäilön luominen](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="8cd01-154">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
7. <span data-ttu-id="8cd01-155">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-155">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="8cd01-156">Luo tallennustilin salainen koodi</span><span class="sxs-lookup"><span data-stu-id="8cd01-156">Create Storage account secret</span></span>

1. <span data-ttu-id="8cd01-157">Valitse **Ympäristöasetukset**-sivun toimintoruudusta **Palveluympäristö** > **Key Vault -parametrit**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-157">On the **Environment setups** page, on the Action Pane, select **Service environment** > **Key Vault parameters**.</span></span>
2. <span data-ttu-id="8cd01-158">Valitse **Varmenteet**-osasta **Key Vault -viite** ja sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-158">Select a **Key Vault reference** and in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="8cd01-159">Syötä **Nimi**-kenttään tallennustilin salaisen koodin nimi.</span><span class="sxs-lookup"><span data-stu-id="8cd01-159">In the **Name** field, enter the name of the storage account secret.</span></span> <span data-ttu-id="8cd01-160">Lisätietoja: [Azure-tallennustilin ja -avainsäilön luominen](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="8cd01-160">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="8cd01-161">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="8cd01-161">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="8cd01-162">Kirjoita **Tyyppi**-kenttään **Salainen koodi**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-162">In the **Type** field, select **Secret**.</span></span>
6. <span data-ttu-id="8cd01-163">Valitse **Tallenna** ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="8cd01-163">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="8cd01-164">Digitaalisen varmenteen salaisen koodin luonti</span><span class="sxs-lookup"><span data-stu-id="8cd01-164">Create a digital certificate secret</span></span>

1. <span data-ttu-id="8cd01-165">Valitse **Ympäristöasetukset**-sivun toimintoruudusta **Palveluympäristö** ja valitse sitten **Key Vault -parametrit**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-165">On the **Environment setups** page, on the action Pane, select **Service environment** and then select **Key Vault parameters**.</span></span>
2. <span data-ttu-id="8cd01-166">Valitse **Varmenteet**-osasta **Key Vault -viite** ja sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-166">Select a **Key Vault reference** and then in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="8cd01-167">Syötä **Nimi**-kenttään digitaalisen varmenteen salaisen koodin nimi.</span><span class="sxs-lookup"><span data-stu-id="8cd01-167">In the **Name** field, enter the name of the digital certificate secret.</span></span> <span data-ttu-id="8cd01-168">Lisätietoja: [Azure-tallennustilin ja -avainsäilön luominen](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="8cd01-168">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="8cd01-169">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="8cd01-169">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="8cd01-170">Valitse **Tyyppi**-kentästä **Varmenne**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-170">In the **Type** field, select **Certificate**.</span></span>
6. <span data-ttu-id="8cd01-171">Valitse **Tallenna** ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="8cd01-171">Select **Save**, and then close the page.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="8cd01-172">Palveluympäristön luominen</span><span class="sxs-lookup"><span data-stu-id="8cd01-172">Create a service environment</span></span>

1. <span data-ttu-id="8cd01-173">Kirjaudu RCS-tilille.</span><span class="sxs-lookup"><span data-stu-id="8cd01-173">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="8cd01-174">Valitse **Globalisaatio-ominaisuudet**-työtilan **Ympäristö**-osassa **Sähköinen laskutus** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="8cd01-174">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="8cd01-175">Valitse **Ympäristöasetukset**-sivun toimintoruudusta **Palveluympäristö**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-175">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
4. <span data-ttu-id="8cd01-176">Luo uusi palveluympäristö valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-176">Select **New** to create a new service environment.</span></span>
5. <span data-ttu-id="8cd01-177">Syötä **Nimi**-kenttään sähköisen laskutuksen ympäristön nimi.</span><span class="sxs-lookup"><span data-stu-id="8cd01-177">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="8cd01-178">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="8cd01-178">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="8cd01-179">Valitse **Tallennutilin SAS-tunnuksen salasana** -kentässä sen tallennustilin varmenteen nimi, jota on käytettävä tallennustiliin todentautumisessa.</span><span class="sxs-lookup"><span data-stu-id="8cd01-179">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
7. <span data-ttu-id="8cd01-180">Valitse **Käyttäjät**-osassa **Lisää**, kun haluat lisätä käyttäjän, joka voi lähettää sähköisiä laskuja ympäristön kautta sekä muodostaa yhteyden tallennustiliin.</span><span class="sxs-lookup"><span data-stu-id="8cd01-180">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
8. <span data-ttu-id="8cd01-181">Kirjoita **Käyttäjätunnus**-kenttään käyttäjän alias.</span><span class="sxs-lookup"><span data-stu-id="8cd01-181">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="8cd01-182">Kirjoita **Sähköpostiosoite**-kenttään käyttäjän sähköpostiosoite.</span><span class="sxs-lookup"><span data-stu-id="8cd01-182">In the **Email** field, enter the user's email address.</span></span>
9. <span data-ttu-id="8cd01-183">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-183">Select **Save**.</span></span>
10. <span data-ttu-id="8cd01-184">Jos maa-/aluekohtaiset laskut edellyttävät tiettyjen varmenteiden soveltamista digitaaliseen allekirjoitukseen, valitse toimintoruudusta **Key Vaultin parametrit** sitten **Varmenneketju** ja suorita seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="8cd01-184">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>
    1. <span data-ttu-id="8cd01-185">Valitse **Uusi**, jos haluat luoda varmenneketjun.</span><span class="sxs-lookup"><span data-stu-id="8cd01-185">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="8cd01-186">Syötä **Nimi**-kenttään varmenneketjun nimi.</span><span class="sxs-lookup"><span data-stu-id="8cd01-186">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="8cd01-187">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="8cd01-187">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="8cd01-188">Lisää ketjuun varmenne valitsemalla **Varmenteet**-osasta **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-188">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="8cd01-189">Voit muuttaa todistuksen sijaintia ketjussa **Ylös**- tai **Alas**-painikkeella.</span><span class="sxs-lookup"><span data-stu-id="8cd01-189">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="8cd01-190">Valitse **Tallenna** ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="8cd01-190">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="8cd01-191">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8cd01-191">Close the page.</span></span>
11. <span data-ttu-id="8cd01-192">Julkaise ympäristö pilveen valitsemalla **Palveluympäristö**-sivun toimintoruudussa **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-192">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="8cd01-193">**Tila**-kentän arvoksi tulee **Julkaisu**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-193">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="8cd01-194">Luo yhdistetty sovellus</span><span class="sxs-lookup"><span data-stu-id="8cd01-194">Create a connected application</span></span>

1. <span data-ttu-id="8cd01-195">Valitse **Ympäristöasetukset**-sivun toimintoruudusta **Yhdistetyt sovellukset**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-195">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="8cd01-196">Luo yhdistetty sovellus valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-196">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="8cd01-197">Syötä **Nimi**-kenttään yhdistettävän sovelluksen nimi.</span><span class="sxs-lookup"><span data-stu-id="8cd01-197">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="8cd01-198">Kirjoita **Sovellus**-kenttään sen Finance- tai Supply Chain Managements -ympäristön URL-osoite, johon haluat yhdistää.</span><span class="sxs-lookup"><span data-stu-id="8cd01-198">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="8cd01-199">Kirjoita **Vuokraaja**-kenttään Finance- tai Supply Chain Managements -ympäristön vuokraaja.</span><span class="sxs-lookup"><span data-stu-id="8cd01-199">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="8cd01-200">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-200">Select **Save**.</span></span>
6. <span data-ttu-id="8cd01-201">Testaa yhteys ympäristöön valitsemalla toimintoruudussa **Tarkista yhteys**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-201">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="8cd01-202">Sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="8cd01-202">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="8cd01-203">Liitettyjen sovellusten linkittäminen ympäristöihin</span><span class="sxs-lookup"><span data-stu-id="8cd01-203">Link connected applications to environments</span></span>

1. <span data-ttu-id="8cd01-204">Valitse **Ympäristöasetukset**-sivulla **Uusi**, jos haluat määrittää liitetyn sovelluksen ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="8cd01-204">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="8cd01-205">Valitse **Yhdistetty sovellus** -kentässä yhdistetty sovellus.</span><span class="sxs-lookup"><span data-stu-id="8cd01-205">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="8cd01-206">Valitse **Palveluympäristö**-kentässä palveluympäristö.</span><span class="sxs-lookup"><span data-stu-id="8cd01-206">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="8cd01-207">Valitse **Tallenna** ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="8cd01-207">Select **Save**, and then close the page.</span></span>

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="8cd01-208">Sähköisen laskutuksen integroinnin määrittäminen Financessa ja Supply Chain Managementissa</span><span class="sxs-lookup"><span data-stu-id="8cd01-208">Set up Electronic invoicing integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a><span data-ttu-id="8cd01-209">Sähköisen laskutuksen integrointitoiminnon käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="8cd01-209">Turn on the Electronic invoicing integration feature</span></span>

1. <span data-ttu-id="8cd01-210">Kirjaudu Finance- tai Supply Chain Management -esiintymään.</span><span class="sxs-lookup"><span data-stu-id="8cd01-210">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="8cd01-211">Etsi **Sähköisen laskutuksen integrointi** -toimintoa **Toiminnonhallinta**-työtilassa.</span><span class="sxs-lookup"><span data-stu-id="8cd01-211">In the **Feature management** workspace, search for the **Electronic invoicing integration** feature.</span></span> <span data-ttu-id="8cd01-212">Jos tämä toiminto ei näy sivulla, valitse **Tarkista päivitykset**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-212">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="8cd01-213">Valitse toiminto ja valitse sitten **Ota käyttöön nyt**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-213">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="8cd01-214">Palvelun päätepisteen URL-osoitteen määritys</span><span class="sxs-lookup"><span data-stu-id="8cd01-214">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="8cd01-215">Siirry kohtaan **Organisaation hallinta \> Määritys \> Sähköisten asiakirjojen parametrit**.</span><span class="sxs-lookup"><span data-stu-id="8cd01-215">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="8cd01-216">Kirjoita **Lähetyspalvelu** -välilehdessä **Palvelun päätepisteen URL** -kenttään asianmukainen Azure-alueen palvelun päätepiste, joka näkyy seuraavassa taulukossa.</span><span class="sxs-lookup"><span data-stu-id="8cd01-216">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="8cd01-217">Konesalin Azure-alue</span><span class="sxs-lookup"><span data-stu-id="8cd01-217">Datacenter Azure geography</span></span> | <span data-ttu-id="8cd01-218">Palvelun päätepisteen URL-osoite</span><span class="sxs-lookup"><span data-stu-id="8cd01-218">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="8cd01-219">Itä-Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="8cd01-219">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="8cd01-220">Länsi-Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="8cd01-220">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="8cd01-221">Pohjois-EU</span><span class="sxs-lookup"><span data-stu-id="8cd01-221">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="8cd01-222">Länsi-EU</span><span class="sxs-lookup"><span data-stu-id="8cd01-222">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="8cd01-223">Syötä **Ympäristö**-kenttään sähköisessä laskutuksessa julkaistun palveluympäristön nimi.</span><span class="sxs-lookup"><span data-stu-id="8cd01-223">In the **Environment** field, enter the name of the service environment published in Electronic invoicing.</span></span>
4. <span data-ttu-id="8cd01-224">Valitse **Tallenna** ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="8cd01-224">Select **Save**, and then close the page.</span></span>

### <a name="enable-flighting-keys"></a><span data-ttu-id="8cd01-225">Väliversioavainten ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="8cd01-225">Enable Flighting keys</span></span>

<span data-ttu-id="8cd01-226">Ota käyttöön väliversioavaimet Microsoft Dynamics 365 Financelle tai Microsoft Dynamics 365 Supply Chain Management -versiolle 10.0.17 tai vanhemmalle versiolle.</span><span class="sxs-lookup"><span data-stu-id="8cd01-226">Enable Flight keys for  Microsoft Dynamics 365 Finance or  Microsoft Dynamics 365 Supply Chain Management versions 10.0.17 or earlier.</span></span> 
1. <span data-ttu-id="8cd01-227">Suorita seuraava SQL-komento:</span><span class="sxs-lookup"><span data-stu-id="8cd01-227">Execute the following SQL command:</span></span>

    <span data-ttu-id="8cd01-228">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span><span class="sxs-lookup"><span data-stu-id="8cd01-228">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span></span>
    
    <span data-ttu-id="8cd01-229">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span><span class="sxs-lookup"><span data-stu-id="8cd01-229">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span></span>

2. <span data-ttu-id="8cd01-230">Suorita IISreset-komento kaikille AOS-kohteille.</span><span class="sxs-lookup"><span data-stu-id="8cd01-230">Perform an IISreset command for all AOS's.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
