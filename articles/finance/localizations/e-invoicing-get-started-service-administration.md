---
title: Sähköisen laskutuksen lisäosan palvelun hallinnan aloittaminen
description: Tässä aiheessa selitetään, miten sähköisen laskutuksen lisäosan käyttö voidaan aloittaa.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 05b00380cec7511adad2467d3f252799a4aaee5c
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592523"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="f46e9-103">Sähköisen laskutuksen lisäosan palvelun hallinnan aloittaminen</span><span class="sxs-lookup"><span data-stu-id="f46e9-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="f46e9-104">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="f46e9-104">Prerequisites</span></span>

<span data-ttu-id="f46e9-105">Ennen kuin voit suorittaa tämän ohjeaiheen vaiheita, seuraavien edellytysten on toteuduttava:</span><span class="sxs-lookup"><span data-stu-id="f46e9-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="f46e9-106">Sinulla on oltava Microsoft Dynamics Lifecycle Services (LCS) -tili.</span><span class="sxs-lookup"><span data-stu-id="f46e9-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="f46e9-107">Käytössäsi on oltava LCS-projekti, joka sisältää Microsoft Dynamics 365 Financen ja Dynamics 365 Supply Chain Managementin version 10.0.17 tai sitä myöhemmän version.</span><span class="sxs-lookup"><span data-stu-id="f46e9-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="f46e9-108">Lisäksi nämä sovellukset on otettava käyttöön jossakin seuraavista Azure-alueista:</span><span class="sxs-lookup"><span data-stu-id="f46e9-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="f46e9-109">Itä-Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="f46e9-109">East US</span></span>
    - <span data-ttu-id="f46e9-110">Länsi-Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="f46e9-110">West US</span></span>
    - <span data-ttu-id="f46e9-111">Pohjois-EU</span><span class="sxs-lookup"><span data-stu-id="f46e9-111">North EU</span></span>
    - <span data-ttu-id="f46e9-112">Länsi-EU</span><span class="sxs-lookup"><span data-stu-id="f46e9-112">West EU</span></span>

- <span data-ttu-id="f46e9-113">Dynamics 365 Regulatory Configuration Services (RCS) -tilin on oltava käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="f46e9-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="f46e9-114">RCS-tilin globalisointiominaisuus on otettava käyttöön toiminnonhallinnan kautta.</span><span class="sxs-lookup"><span data-stu-id="f46e9-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="f46e9-115">Lisätietoja: [Regulatory Configuration Services (RCS) – globalisointitoiminnot](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="f46e9-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="f46e9-116">On luotava avainsäilö ja tallennustili Azuressa.</span><span class="sxs-lookup"><span data-stu-id="f46e9-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="f46e9-117">Lisätietoja: [Azure-tallennustilin ja -avainsäilön luominen](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="f46e9-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="f46e9-118">Microservices-lisäosan asentaminen Lifecycle Servicesissa</span><span class="sxs-lookup"><span data-stu-id="f46e9-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="f46e9-119">Kirjaudu LCS-tilille.</span><span class="sxs-lookup"><span data-stu-id="f46e9-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="f46e9-120">Valitse **Esiversiotoiminnon hallinta** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="f46e9-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="f46e9-121">Valitse **Julkisen esiversion ominaisuudet** -osasta **Sähköisen laskutuksen palvelu**.</span><span class="sxs-lookup"><span data-stu-id="f46e9-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="f46e9-122">Varmista, että **Esiversiotoiminto käytössä** -asetukseksi on valittu **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="f46e9-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="f46e9-123">Valitse LCS-käyttöönottoprojekti LCS-koontinäytössä.</span><span class="sxs-lookup"><span data-stu-id="f46e9-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="f46e9-124">LCS-projektin on oltava käynnissä.</span><span class="sxs-lookup"><span data-stu-id="f46e9-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="f46e9-125">Valitse **Ympäristöapuohjelmat**-välilehdessä **Asenna uusi apuohjelma**.</span><span class="sxs-lookup"><span data-stu-id="f46e9-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="f46e9-126">Valitse **e-laskutuspalvelut** ja kirjoita **AAD-sovellustunnus** -kenttään **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span><span class="sxs-lookup"><span data-stu-id="f46e9-126">Select **e-invoicing Services** and in the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="f46e9-127">Tämä on kiinteä arvo.</span><span class="sxs-lookup"><span data-stu-id="f46e9-127">This is a fixed value.</span></span>
10. <span data-ttu-id="f46e9-128">Syötä **AAD-vuokraajatunnus**-kenttään Azure-tilaustilisi vuokraajan tunnus.</span><span class="sxs-lookup"><span data-stu-id="f46e9-128">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="f46e9-129">Lue ehdot ja valitse valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="f46e9-129">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="f46e9-130">Valitse **Asenna**.</span><span class="sxs-lookup"><span data-stu-id="f46e9-130">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="f46e9-131">Määritä RCS-integroinnin parametrit sähköisen laskutuksen lisäosan avulla.</span><span class="sxs-lookup"><span data-stu-id="f46e9-131">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="f46e9-132">Kirjaudu RCS-tilille.</span><span class="sxs-lookup"><span data-stu-id="f46e9-132">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="f46e9-133">Valitse **Sähköisen raportointi** -työtilan **Liittyvät linkit** -osassa **Sähköisen raportoinnin parametrit**.</span><span class="sxs-lookup"><span data-stu-id="f46e9-133">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="f46e9-134">Kirjoita **Sähköisen laskutuksen palvelu** -välilehdessä **Palvelun päätepisteen URI** -kenttään asianmukainen Azure-alueen palvelun päätepiste, joka näkyy seuraavassa taulukossa.</span><span class="sxs-lookup"><span data-stu-id="f46e9-134">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="f46e9-135">Konesalin Azure-alue</span><span class="sxs-lookup"><span data-stu-id="f46e9-135">Datacenter Azure geography</span></span> | <span data-ttu-id="f46e9-136">Palvelun päätepisteen URI-osoite</span><span class="sxs-lookup"><span data-stu-id="f46e9-136">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="f46e9-137">Itä-Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="f46e9-137">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="f46e9-138">Länsi-Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="f46e9-138">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="f46e9-139">Pohjois-EU</span><span class="sxs-lookup"><span data-stu-id="f46e9-139">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="f46e9-140">Länsi-EU</span><span class="sxs-lookup"><span data-stu-id="f46e9-140">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="f46e9-141">Varmista, että **Sovellustunnus**-kentän arvo on **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="f46e9-141">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="f46e9-142">Tämä arvo on kiinteä arvo.</span><span class="sxs-lookup"><span data-stu-id="f46e9-142">This value is a fixed value.</span></span>
5. <span data-ttu-id="f46e9-143">Syötä **LCS-ympäristötunnus**-kenttään LCS-tilaustilisi tunnus.</span><span class="sxs-lookup"><span data-stu-id="f46e9-143">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="f46e9-144">Valitse **Tallenna** ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="f46e9-144">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="f46e9-145">Luo avainsäilön salainen koodi</span><span class="sxs-lookup"><span data-stu-id="f46e9-145">Create Key Vault secret</span></span>

1. <span data-ttu-id="f46e9-146">Kirjaudu RCS-tilille.</span><span class="sxs-lookup"><span data-stu-id="f46e9-146">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="f46e9-147">Valitse **Globalisaatio-ominaisuudet**-työtilan **Ympäristö**-osassa **Sähköisen laskutuksen lisäosa** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="f46e9-147">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>
3. <span data-ttu-id="f46e9-148">Valitse **Ympäristöasetukset**-sivun toimintoruudusta **Palveluympäristö** ja valitse sitten **Key Vault -parametrit**.</span><span class="sxs-lookup"><span data-stu-id="f46e9-148">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="f46e9-149">Valitse **Uusi**, jos haluat luoda avainsäilön salaisen koodin.</span><span class="sxs-lookup"><span data-stu-id="f46e9-149">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="f46e9-150">Syötä **Nimi**-kenttään avainsäilön salaisen koodin nimi.</span><span class="sxs-lookup"><span data-stu-id="f46e9-150">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="f46e9-151">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="f46e9-151">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="f46e9-152">Liitä **Key Vault – URI** -kenttään Azure Key Vaultin salainen koodi.</span><span class="sxs-lookup"><span data-stu-id="f46e9-152">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="f46e9-153">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f46e9-153">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="f46e9-154">Luo tallennustilin salainen koodi</span><span class="sxs-lookup"><span data-stu-id="f46e9-154">Create Storage account secret</span></span>

1. <span data-ttu-id="f46e9-155">Siirry kohtaan **Järjestelmänhallinta** > **Asetukset** > **Avainsäilön parametit** ja valitse avainsäilön salainen koodi.</span><span class="sxs-lookup"><span data-stu-id="f46e9-155">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="f46e9-156">Valitse **Varmenteet**-osasta **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="f46e9-156">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="f46e9-157">Kirjoita **Nimi**-kenttään tallennustilin salaisen koodin nimi ja **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="f46e9-157">In the **Name** field, enter the name of the storage account secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="f46e9-158">Valitse **Tyyppi**-kentästä **Varmenne**.</span><span class="sxs-lookup"><span data-stu-id="f46e9-158">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="f46e9-159">Valitse **Tallenna** ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="f46e9-159">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="f46e9-160">Digitaalisen varmenteen salaisen koodin luonti</span><span class="sxs-lookup"><span data-stu-id="f46e9-160">Create a digital certificate secret</span></span>

1. <span data-ttu-id="f46e9-161">Siirry kohtaan **Järjestelmänhallinta** > **Asetukset** > **Avainsäilön parametit** ja valitse avainsäilön salainen koodi.</span><span class="sxs-lookup"><span data-stu-id="f46e9-161">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="f46e9-162">Valitse **Varmenteet**-osasta **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="f46e9-162">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="f46e9-163">Kirjoita **Nimi**-kenttään digitaalisen varmenteen salaisen koodin nimi ja **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="f46e9-163">In the **Name** field, enter the name of the digital certificate secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="f46e9-164">Valitse **Tyyppi**-kentästä **Varmenne**.</span><span class="sxs-lookup"><span data-stu-id="f46e9-164">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="f46e9-165">Valitse **Tallenna** ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="f46e9-165">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="f46e9-166">Sähköisen laskutuksen lisäosaympäristön luonti</span><span class="sxs-lookup"><span data-stu-id="f46e9-166">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="f46e9-167">Kirjaudu RCS-tilille.</span><span class="sxs-lookup"><span data-stu-id="f46e9-167">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="f46e9-168">Valitse **Globalisaatio-ominaisuudet**-työtilan **Ympäristö**-osassa **Sähköisen laskutuksen lisäosa** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="f46e9-168">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="f46e9-169">Palveluympäristön luominen</span><span class="sxs-lookup"><span data-stu-id="f46e9-169">Create a service environment</span></span>

1. <span data-ttu-id="f46e9-170">Valitse **Ympäristöasetukset**-sivun toimintoruudusta **Palveluympäristö**.</span><span class="sxs-lookup"><span data-stu-id="f46e9-170">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="f46e9-171">Luo uusi palveluympäristö valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f46e9-171">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="f46e9-172">Syötä **Nimi**-kenttään sähköisen laskutuksen ympäristön nimi.</span><span class="sxs-lookup"><span data-stu-id="f46e9-172">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="f46e9-173">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="f46e9-173">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="f46e9-174">Valitse **Tallennutilin SAS-tunnuksen salasana** -kentässä sen tallennustilin varmenteen nimi, jota on käytettävä tallennustiliin todentautumisessa.</span><span class="sxs-lookup"><span data-stu-id="f46e9-174">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="f46e9-175">Valitse **Käyttäjät**-osassa **Lisää**, kun haluat lisätä käyttäjän, joka voi lähettää sähköisiä laskuja ympäristön kautta sekä muodostaa yhteyden tallennustiliin.</span><span class="sxs-lookup"><span data-stu-id="f46e9-175">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="f46e9-176">Kirjoita **Käyttäjätunnus**-kenttään käyttäjän alias.</span><span class="sxs-lookup"><span data-stu-id="f46e9-176">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="f46e9-177">Kirjoita **Sähköpostiosoite**-kenttään käyttäjän sähköpostiosoite.</span><span class="sxs-lookup"><span data-stu-id="f46e9-177">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="f46e9-178">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f46e9-178">Select **Save**.</span></span>
8. <span data-ttu-id="f46e9-179">Jos maa-/aluekohtaiset laskut edellyttävät tiettyjen varmenteiden soveltamista digitaaliseen allekirjoitukseen, valitse toimintoruudusta **Key Vaultin parametrit** sitten **Varmenneketju** ja suorita seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="f46e9-179">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="f46e9-180">Valitse **Uusi**, jos haluat luoda varmenneketjun.</span><span class="sxs-lookup"><span data-stu-id="f46e9-180">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="f46e9-181">Syötä **Nimi**-kenttään varmenneketjun nimi.</span><span class="sxs-lookup"><span data-stu-id="f46e9-181">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="f46e9-182">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="f46e9-182">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="f46e9-183">Lisää ketjuun varmenne valitsemalla **Varmenteet**-osasta **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="f46e9-183">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="f46e9-184">Voit muuttaa todistuksen sijaintia ketjussa **Ylös**- tai **Alas**-painikkeella.</span><span class="sxs-lookup"><span data-stu-id="f46e9-184">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="f46e9-185">Valitse **Tallenna** ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="f46e9-185">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="f46e9-186">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f46e9-186">Close the page.</span></span>
9. <span data-ttu-id="f46e9-187">Julkaise ympäristö pilveen valitsemalla **Palveluympäristö**-sivun toimintoruudussa **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="f46e9-187">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="f46e9-188">**Tila**-kentän arvoksi tulee **Julkaisu**.</span><span class="sxs-lookup"><span data-stu-id="f46e9-188">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="f46e9-189">Luo yhdistetty sovellus</span><span class="sxs-lookup"><span data-stu-id="f46e9-189">Create a connected application</span></span>

1. <span data-ttu-id="f46e9-190">Valitse **Ympäristöasetukset**-sivun toimintoruudusta **Yhdistetyt sovellukset**.</span><span class="sxs-lookup"><span data-stu-id="f46e9-190">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="f46e9-191">Luo yhdistetty sovellus valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f46e9-191">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="f46e9-192">Syötä **Nimi**-kenttään yhdistettävän sovelluksen nimi.</span><span class="sxs-lookup"><span data-stu-id="f46e9-192">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="f46e9-193">Kirjoita **Sovellus**-kenttään sen Finance- tai Supply Chain Managements -ympäristön URL-osoite, johon haluat yhdistää.</span><span class="sxs-lookup"><span data-stu-id="f46e9-193">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="f46e9-194">Kirjoita **Vuokraaja**-kenttään Finance- tai Supply Chain Managements -ympäristön vuokraaja.</span><span class="sxs-lookup"><span data-stu-id="f46e9-194">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="f46e9-195">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f46e9-195">Select **Save**.</span></span>
6. <span data-ttu-id="f46e9-196">Testaa yhteys ympäristöön valitsemalla toimintoruudussa **Tarkista yhteys**.</span><span class="sxs-lookup"><span data-stu-id="f46e9-196">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="f46e9-197">Sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="f46e9-197">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="f46e9-198">Liitettyjen sovellusten linkittäminen ympäristöihin</span><span class="sxs-lookup"><span data-stu-id="f46e9-198">Link connected applications to environments</span></span>

1. <span data-ttu-id="f46e9-199">Valitse **Ympäristöasetukset**-sivulla **Uusi**, jos haluat määrittää liitetyn sovelluksen ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="f46e9-199">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="f46e9-200">Valitse **Yhdistetty sovellus** -kentässä yhdistetty sovellus.</span><span class="sxs-lookup"><span data-stu-id="f46e9-200">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="f46e9-201">Valitse **Palveluympäristö**-kentässä palveluympäristö.</span><span class="sxs-lookup"><span data-stu-id="f46e9-201">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="f46e9-202">Valitse **Tallenna** ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="f46e9-202">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="f46e9-203">Sähköisen laskutuksen lisäosan integroinnin määrittäminen Financessa tai Supply Chain Managementissa</span><span class="sxs-lookup"><span data-stu-id="f46e9-203">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="f46e9-204">Sähköisen laskutuksen lisäosan integrointitoiminnon käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="f46e9-204">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="f46e9-205">Kirjaudu Finance- tai Supply Chain Management -esiintymään.</span><span class="sxs-lookup"><span data-stu-id="f46e9-205">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="f46e9-206">Etsi **Sähköisen laskutuksen lisäosan integrointi** -toimintoa **Toiminnonhallinta**-työtilassa.</span><span class="sxs-lookup"><span data-stu-id="f46e9-206">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="f46e9-207">Jos tämä toiminto ei näy sivulla, valitse **Tarkista päivitykset**.</span><span class="sxs-lookup"><span data-stu-id="f46e9-207">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="f46e9-208">Valitse toiminto ja valitse sitten **Ota käyttöön nyt**.</span><span class="sxs-lookup"><span data-stu-id="f46e9-208">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="f46e9-209">Palvelun päätepisteen URL-osoitteen määritys</span><span class="sxs-lookup"><span data-stu-id="f46e9-209">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="f46e9-210">Siirry kohtaan **Organisaation hallinta \> Määritys \> Sähköisten asiakirjojen parametrit**.</span><span class="sxs-lookup"><span data-stu-id="f46e9-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="f46e9-211">Kirjoita **Lähetyspalvelu** -välilehdessä **Palvelun päätepisteen URL** -kenttään asianmukainen Azure-alueen palvelun päätepiste, joka näkyy seuraavassa taulukossa.</span><span class="sxs-lookup"><span data-stu-id="f46e9-211">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="f46e9-212">Konesalin Azure-alue</span><span class="sxs-lookup"><span data-stu-id="f46e9-212">Datacenter Azure geography</span></span> | <span data-ttu-id="f46e9-213">Palvelun päätepisteen URL-osoite</span><span class="sxs-lookup"><span data-stu-id="f46e9-213">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="f46e9-214">Itä-Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="f46e9-214">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="f46e9-215">Länsi-Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="f46e9-215">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="f46e9-216">Pohjois-EU</span><span class="sxs-lookup"><span data-stu-id="f46e9-216">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="f46e9-217">Länsi-EU</span><span class="sxs-lookup"><span data-stu-id="f46e9-217">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="f46e9-218">Syötä **Ympäristö**-kenttään sähköisen laskutuksen lisäosan ympäristön nimi.</span><span class="sxs-lookup"><span data-stu-id="f46e9-218">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="f46e9-219">Valitse **Tallenna** ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="f46e9-219">Select **Save**, and then close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
