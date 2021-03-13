---
title: Sähköisen laskutuksen lisäosan palvelun hallinnan aloittaminen
description: Tässä aiheessa selitetään, miten sähköisen laskutuksen lisäosan käyttö voidaan aloittaa.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
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
ms.openlocfilehash: 111ec65aa826795125d4a9ce835f72e1a0f41b7b
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104373"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="37c52-103">Sähköisen laskutuksen lisäosan palvelun hallinnan aloittaminen</span><span class="sxs-lookup"><span data-stu-id="37c52-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="37c52-104">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="37c52-104">Prerequisites</span></span>

<span data-ttu-id="37c52-105">Ennen kuin voit suorittaa tämän ohjeaiheen vaiheita, seuraavien edellytysten on toteuduttava:</span><span class="sxs-lookup"><span data-stu-id="37c52-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="37c52-106">Sinulla on oltava Microsoft Dynamics Lifecycle Services (LCS) -tili.</span><span class="sxs-lookup"><span data-stu-id="37c52-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="37c52-107">Käytössäsi on oltava LCS-projekti, joka sisältää Microsoft Dynamics 365 Financen ja Dynamics 365 Supply Chain Managementin version 10.0.13 tai sitä myöhemmän version.</span><span class="sxs-lookup"><span data-stu-id="37c52-107">You must have an LCS project that includes version 10.0.13 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="37c52-108">Lisäksi nämä sovellukset on otettava käyttöön jossakin seuraavista Azure-alueista:</span><span class="sxs-lookup"><span data-stu-id="37c52-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="37c52-109">Itä-Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="37c52-109">East US</span></span>
    - <span data-ttu-id="37c52-110">Länsi-Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="37c52-110">West US</span></span>
    - <span data-ttu-id="37c52-111">Pohjois-EU</span><span class="sxs-lookup"><span data-stu-id="37c52-111">North EU</span></span>
    - <span data-ttu-id="37c52-112">Länsi-EU</span><span class="sxs-lookup"><span data-stu-id="37c52-112">West EU</span></span>

- <span data-ttu-id="37c52-113">Dynamics 365 Regulatory Configuration Services (RCS) -tilin on oltava käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="37c52-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="37c52-114">RCS-tilin globalisointiominaisuus on otettava käyttöön toiminnonhallinnan kautta.</span><span class="sxs-lookup"><span data-stu-id="37c52-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="37c52-115">Lisätietoja: [Regulatory Configuration Services (RCS) – globalisointitoiminnot](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="37c52-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="37c52-116">On luotava avainsäilö ja tallennustili Azuressa.</span><span class="sxs-lookup"><span data-stu-id="37c52-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="37c52-117">Lisätietoja: [Azure-tallennustilin ja -avainsäilön luominen](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="37c52-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="37c52-118">Microservices-lisäosan asentaminen Lifecycle Servicesissa</span><span class="sxs-lookup"><span data-stu-id="37c52-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="37c52-119">Kirjaudu LCS-tilille.</span><span class="sxs-lookup"><span data-stu-id="37c52-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="37c52-120">Valitse **Esiversiotoiminnon hallinta** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="37c52-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="37c52-121">Valitse **Julkisen esiversion ominaisuudet** -osasta **Sähköisen laskutuksen palvelu**.</span><span class="sxs-lookup"><span data-stu-id="37c52-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="37c52-122">Varmista, että **Esiversiotoiminto käytössä** -asetukseksi on valittu **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="37c52-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>

## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="37c52-123">Määritä RCS-integroinnin parametrit sähköisen laskutuksen lisäosan avulla.</span><span class="sxs-lookup"><span data-stu-id="37c52-123">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="37c52-124">Kirjaudu RCS-tilille.</span><span class="sxs-lookup"><span data-stu-id="37c52-124">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="37c52-125">Valitse **Sähköisen raportointi** -työtilan **Liittyvät linkit** -osassa **Sähköisen raportoinnin parametrit**.</span><span class="sxs-lookup"><span data-stu-id="37c52-125">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="37c52-126">Kirjoita **Sähköisen laskutuksen palvelu** -välilehdessä **Palvelun päätepisteen URI** -kenttään asianmukainen Azure-alueen palvelun päätepiste, joka näkyy seuraavassa taulukossa.</span><span class="sxs-lookup"><span data-stu-id="37c52-126">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="37c52-127">Konesalin Azure-alue</span><span class="sxs-lookup"><span data-stu-id="37c52-127">Datacenter Azure geography</span></span> | <span data-ttu-id="37c52-128">Palvelun päätepisteen URI-osoite</span><span class="sxs-lookup"><span data-stu-id="37c52-128">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="37c52-129">Itä-Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="37c52-129">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="37c52-130">Länsi-Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="37c52-130">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="37c52-131">Pohjois-EU</span><span class="sxs-lookup"><span data-stu-id="37c52-131">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="37c52-132">Länsi-EU</span><span class="sxs-lookup"><span data-stu-id="37c52-132">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="37c52-133">Varmista, että **Sovellustunnus**-kentän arvo on **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="37c52-133">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="37c52-134">Tämä arvo on kiinteä arvo.</span><span class="sxs-lookup"><span data-stu-id="37c52-134">This value is a fixed value.</span></span>
5. <span data-ttu-id="37c52-135">Syötä **LCS-ympäristötunnus**-kenttään LCS-tilaustilisi tunnus.</span><span class="sxs-lookup"><span data-stu-id="37c52-135">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="37c52-136">Valitse **Tallenna** ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="37c52-136">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="37c52-137">Luo avainsäilön salainen koodi</span><span class="sxs-lookup"><span data-stu-id="37c52-137">Create Key Vault secret</span></span>

1. <span data-ttu-id="37c52-138">Kirjaudu RCS-tilille.</span><span class="sxs-lookup"><span data-stu-id="37c52-138">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="37c52-139">Valitse **Globalisointitoiminnot**-työtila ja **Ympäristö**-kohdan **Sähköinen laskutus** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="37c52-139">In the **Globalization feature** workspace, in the **Environment** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="37c52-140">Valitse **Ympäristöasetukset**-sivun toimintoruudusta **Palveluympäristö** ja valitse sitten **Key Vault -parametrit**.</span><span class="sxs-lookup"><span data-stu-id="37c52-140">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="37c52-141">Valitse **Uusi**, jos haluat luoda avainsäilön salaisen koodin.</span><span class="sxs-lookup"><span data-stu-id="37c52-141">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="37c52-142">Syötä **Nimi**-kenttään avainsäilön salaisen koodin nimi.</span><span class="sxs-lookup"><span data-stu-id="37c52-142">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="37c52-143">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="37c52-143">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="37c52-144">Liitä **Key Vault – URI** -kenttään Azure Key Vaultin salainen koodi.</span><span class="sxs-lookup"><span data-stu-id="37c52-144">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="37c52-145">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="37c52-145">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="37c52-146">Luo tallennustilin salainen koodi</span><span class="sxs-lookup"><span data-stu-id="37c52-146">Create Storage account secret</span></span>

1. <span data-ttu-id="37c52-147">Valitse **Varmenteet**-osasta **Key Vault -parametrit** -sivulla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="37c52-147">On **Key vault parameters** page, in the **Certificates** section, select **Add**.</span></span>
2. <span data-ttu-id="37c52-148">Syötä **Nimi**-kenttään tallennustilin salaisen koodin nimi.</span><span class="sxs-lookup"><span data-stu-id="37c52-148">In the **Name** field, enter the same of the storage account secret.</span></span> <span data-ttu-id="37c52-149">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="37c52-149">In the **Description** field, enter a description.</span></span>
3. <span data-ttu-id="37c52-150">Valitse **Tyyppi**-kentästä **Varmenne**.</span><span class="sxs-lookup"><span data-stu-id="37c52-150">In the **Type** field, select **Certificate**.</span></span>
4. <span data-ttu-id="37c52-151">Valitse **Tallenna** ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="37c52-151">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="37c52-152">Sähköisen laskutuksen lisäosaympäristön luonti</span><span class="sxs-lookup"><span data-stu-id="37c52-152">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="37c52-153">Kirjaudu RCS-tilille.</span><span class="sxs-lookup"><span data-stu-id="37c52-153">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="37c52-154">Valitse **Globalisointitoiminnot**-työtila ja **Ympäristö**-kohdan **Sähköinen laskutus** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="37c52-154">In the **Globalization feature** workspace, in the **Environment** section, select the **e-Invoicing** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="37c52-155">Palveluympäristön luominen</span><span class="sxs-lookup"><span data-stu-id="37c52-155">Create a service environment</span></span>

1. <span data-ttu-id="37c52-156">Valitse **Ympäristöasetukset**-sivun toimintoruudusta **Palveluympäristö**.</span><span class="sxs-lookup"><span data-stu-id="37c52-156">On the **Environment setups** page, on the action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="37c52-157">Luo uusi palveluympäristö valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="37c52-157">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="37c52-158">Syötä **Nimi**-kenttään sähköisen laskutuksen ympäristön nimi.</span><span class="sxs-lookup"><span data-stu-id="37c52-158">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="37c52-159">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="37c52-159">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="37c52-160">Valitse **Tallennutilin SAS-tunnuksen salasana** -kentässä sen varmenteen nimi, jota on käytettävä tallennustiliin todentautumisessa.</span><span class="sxs-lookup"><span data-stu-id="37c52-160">In the **Storage SAS token secret** field, select the name of the certificate that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="37c52-161">Valitse **Käyttäjät**-osassa **Lisää**, kun haluat lisätä käyttäjän, joka voi lähettää sähköisiä laskuja ympäristön kautta sekä muodostaa yhteyden tallennustiliin.</span><span class="sxs-lookup"><span data-stu-id="37c52-161">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="37c52-162">Kirjoita **Käyttäjätunnus**-kenttään käyttäjän alias.</span><span class="sxs-lookup"><span data-stu-id="37c52-162">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="37c52-163">Kirjoita **Sähköpostiosoite**-kenttään käyttäjän sähköpostiosoite.</span><span class="sxs-lookup"><span data-stu-id="37c52-163">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="37c52-164">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="37c52-164">Select **Save**.</span></span>
8. <span data-ttu-id="37c52-165">Jos maa-/aluekohtaiset laskut edellyttävät tiettyjen varmenteiden soveltamista digitaaliseen allekirjoitukseen, valitse toimintoruudusta **Key Vaultin parametrit** sitten **Varmenneketju** ja suorita seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="37c52-165">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="37c52-166">Valitse **Uusi**, jos haluat luoda varmenneketjun.</span><span class="sxs-lookup"><span data-stu-id="37c52-166">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="37c52-167">Syötä **Nimi**-kenttään varmenneketjun nimi.</span><span class="sxs-lookup"><span data-stu-id="37c52-167">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="37c52-168">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="37c52-168">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="37c52-169">Lisää ketjuun varmenne valitsemalla **Varmenteet**-osasta **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="37c52-169">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="37c52-170">Voit muuttaa todistuksen sijaintia ketjussa **Ylös**- tai **Alas**-painikkeella.</span><span class="sxs-lookup"><span data-stu-id="37c52-170">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="37c52-171">Valitse **Tallenna** ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="37c52-171">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="37c52-172">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="37c52-172">Close the page.</span></span>
9. <span data-ttu-id="37c52-173">Julkaise ympäristö pilveen valitsemalla **Palveluympäristö**-sivun toimintoruudussa **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="37c52-173">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="37c52-174">**Tila**-kentän arvoksi tulee **Julkaisu**.</span><span class="sxs-lookup"><span data-stu-id="37c52-174">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="37c52-175">Luo yhdistetty sovellus</span><span class="sxs-lookup"><span data-stu-id="37c52-175">Create a connected application</span></span>

1. <span data-ttu-id="37c52-176">Valitse **Ympäristöasetukset**-sivun toimintoruudusta **Yhdistetyt sovellukset**.</span><span class="sxs-lookup"><span data-stu-id="37c52-176">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="37c52-177">Luo yhdistetty sovellus valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="37c52-177">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="37c52-178">Syötä **Nimi**-kenttään yhdistettävän sovelluksen nimi.</span><span class="sxs-lookup"><span data-stu-id="37c52-178">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="37c52-179">Kirjoita **Sovellus**-kenttään sen Finance- tai Supply Chain Managements -ympäristön URL-osoite, johon haluat yhdistää.</span><span class="sxs-lookup"><span data-stu-id="37c52-179">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="37c52-180">Kirjoita **Vuokraaja**-kenttään Finance- tai Supply Chain Managements -ympäristön vuokraaja.</span><span class="sxs-lookup"><span data-stu-id="37c52-180">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="37c52-181">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="37c52-181">Select **Save**.</span></span>
6. <span data-ttu-id="37c52-182">Testaa yhteys ympäristöön valitsemalla toimintoruudussa **Tarkista yhteys**.</span><span class="sxs-lookup"><span data-stu-id="37c52-182">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="37c52-183">Sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="37c52-183">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="37c52-184">Liitettyjen sovellusten linkittäminen ympäristöihin</span><span class="sxs-lookup"><span data-stu-id="37c52-184">Link connected applications to environments</span></span>

1. <span data-ttu-id="37c52-185">Valitse **Ympäristöasetukset**-sivulla **Uusi**, jos haluat määrittää liitetyn sovelluksen ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="37c52-185">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="37c52-186">Valitse **Yhdistetty sovellus** -kentässä yhdistetty sovellus.</span><span class="sxs-lookup"><span data-stu-id="37c52-186">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="37c52-187">Valitse **Palveluympäristö**-kentässä palveluympäristö.</span><span class="sxs-lookup"><span data-stu-id="37c52-187">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="37c52-188">Valitse **Tallenna** ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="37c52-188">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="37c52-189">Sähköisen laskutuksen lisäosan integroinnin määrittäminen Financessa tai Supply Chain Managementissa</span><span class="sxs-lookup"><span data-stu-id="37c52-189">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="37c52-190">Sähköisen laskutuksen lisäosan integrointitoiminnon käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="37c52-190">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="37c52-191">Kirjaudu Finance- tai Supply Chain Management -esiintymään.</span><span class="sxs-lookup"><span data-stu-id="37c52-191">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="37c52-192">Etsi **Sähköisen laskutuksen lisäosan integrointi** -toimintoa **Toiminnonhallinta**-työtilassa.</span><span class="sxs-lookup"><span data-stu-id="37c52-192">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="37c52-193">Jos tämä toiminto ei näy sivulla, valitse **Tarkista päivitykset**.</span><span class="sxs-lookup"><span data-stu-id="37c52-193">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="37c52-194">Valitse toiminto ja valitse sitten **Ota käyttöön nyt**.</span><span class="sxs-lookup"><span data-stu-id="37c52-194">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="37c52-195">Palvelun päätepisteen URL-osoitteen määritys</span><span class="sxs-lookup"><span data-stu-id="37c52-195">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="37c52-196">Siirry kohtaan **Organisaation hallinta \> Määritys \> Sähköisten asiakirjojen parametrit**.</span><span class="sxs-lookup"><span data-stu-id="37c52-196">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="37c52-197">Kirjoita **Lähetyspalvelu** -välilehdessä **Palvelun päätepisteen URL** -kenttään asianmukainen Azure-alueen palvelun päätepiste, joka näkyy seuraavassa taulukossa.</span><span class="sxs-lookup"><span data-stu-id="37c52-197">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="37c52-198">Konesalin Azure-alue</span><span class="sxs-lookup"><span data-stu-id="37c52-198">Datacenter Azure geography</span></span> | <span data-ttu-id="37c52-199">Palvelun päätepisteen URL-osoite</span><span class="sxs-lookup"><span data-stu-id="37c52-199">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="37c52-200">Itä-Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="37c52-200">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="37c52-201">Länsi-Yhdysvallat</span><span class="sxs-lookup"><span data-stu-id="37c52-201">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="37c52-202">Pohjois-EU</span><span class="sxs-lookup"><span data-stu-id="37c52-202">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="37c52-203">Länsi-EU</span><span class="sxs-lookup"><span data-stu-id="37c52-203">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="37c52-204">Syötä **Ympäristö**-kenttään sähköisen laskutuksen lisäosan ympäristön nimi.</span><span class="sxs-lookup"><span data-stu-id="37c52-204">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="37c52-205">Valitse **Tallenna** ja sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="37c52-205">Select **Save**, and then close the page.</span></span>
