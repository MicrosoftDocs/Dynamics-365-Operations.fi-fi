---
title: IoT-analytiikan Azure-resurssien määrittäminen
description: Tässä ohjeaiheessa käsitellään IoT-analytiikkaa varten tarvittavien Microsoft Azure -resurssien luontia ja määrittämistä.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cd06410dd6260e6a371b0044546be7f8c9957c80
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989818"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a><span data-ttu-id="aa043-103">IoT-analytiikan Azure-resurssien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="aa043-103">Set up Azure resources for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aa043-104">Tässä ohjeaiheessa käsitellään IoT-analytiikkaa varten tarvittavien Microsoft Azure -resurssien luontia ja määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="aa043-104">This topic explains how to create and configure the Microsoft Azure resources that you require for IoT Intelligence.</span></span>

## <a name="create-azure-resources"></a><span data-ttu-id="aa043-105">Azure-resurssien luominen</span><span class="sxs-lookup"><span data-stu-id="aa043-105">Create Azure resources</span></span>

<span data-ttu-id="aa043-106">Luo seuraavien ohjeiden avulla IoT-keskitin, Redis-välimuisti ja avainsäilö, jota Microsoft Dynamics 365 Supply Chain Management voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="aa043-106">Follow these steps to create an IoT hub, a Redis cache, and a key vault that can be accessed by Microsoft Dynamics 365 Supply Chain Management.</span></span>

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a><span data-ttu-id="aa043-107">Vuokraajan Microsoft Dynamics ERP Microservices -sovellustunnuksen varmistaminen</span><span class="sxs-lookup"><span data-stu-id="aa043-107">Verify that the Microsoft Dynamics ERP Microservices first-party app ID is in your tenant</span></span>

<span data-ttu-id="aa043-108">Seuraavien ohjeiden avulla varmistaa, että Microsoft Dynamics ERP Microservices -sovelluksen sovellustunnus on vuokraajassa.</span><span class="sxs-lookup"><span data-stu-id="aa043-108">To verify that the app ID for the Microsoft Dynamics ERP Microservices first-party app is in your tenant, follow these steps.</span></span>

1. <span data-ttu-id="aa043-109">Kirjaudu Azure-portaalin osoitteessa <https://portal.azure.com>.</span><span class="sxs-lookup"><span data-stu-id="aa043-109">Sign in to the Azure portal at <https://portal.azure.com>.</span></span>
2. <span data-ttu-id="aa043-110">Siirry osoitteeseen **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="aa043-110">Go to **Azure Active Directory**.</span></span>
3. <span data-ttu-id="aa043-111">Valitse **Yrityssovellukset**.</span><span class="sxs-lookup"><span data-stu-id="aa043-111">Go to **Enterprise applications**.</span></span>
4. <span data-ttu-id="aa043-112">Valitse **Sovelluksen tyyppi** -kentässä **Microsoft-sovellukset**.</span><span class="sxs-lookup"><span data-stu-id="aa043-112">In the **Application type** field, select **Microsoft applications**.</span></span>
5. <span data-ttu-id="aa043-113">Kirjoita hakukenttään **Microsoft Dynamics ERP Microservices**.</span><span class="sxs-lookup"><span data-stu-id="aa043-113">In the search field, enter **Microsoft Dynamics ERP Microservices**.</span></span>
6. <span data-ttu-id="aa043-114">Varmista, että **Microsoft Dynamics ERP Microservices** on luettelossa.</span><span class="sxs-lookup"><span data-stu-id="aa043-114">Verify that **Microsoft Dynamics ERP Microservices** is in the list.</span></span> <span data-ttu-id="aa043-115">Muilla sovelluksilla on samankaltaisia nimiä.</span><span class="sxs-lookup"><span data-stu-id="aa043-115">Other applications have similar names.</span></span> <span data-ttu-id="aa043-116">Varmista tämän vuoksi, että löydät oikean sovelluksen.</span><span class="sxs-lookup"><span data-stu-id="aa043-116">Therefore, make sure that you find the correct application.</span></span> <span data-ttu-id="aa043-117">Sovelluksen tunnus on **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="aa043-117">The app ID is **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="aa043-118">Jos sovellus ei ole luettelossa, se on lisättävä vuokraajaan:</span><span class="sxs-lookup"><span data-stu-id="aa043-118">If the application isn't in the list, you must add it to your tenant:</span></span>

    1. <span data-ttu-id="aa043-119">Valitse Azure-portaalin työkalurivillä painike, jolla Azure-pilviliittymä avataan.</span><span class="sxs-lookup"><span data-stu-id="aa043-119">In the Azure portal, on the toolbar, select the button to open Azure Cloud Shell.</span></span>
    2. <span data-ttu-id="aa043-120">Suorita komento **Install-Module AzureAD**.</span><span class="sxs-lookup"><span data-stu-id="aa043-120">Run the command **Install-Module AzureAD**.</span></span> <span data-ttu-id="aa043-121">Asenna moduuli kirjoittamalla **Y**.</span><span class="sxs-lookup"><span data-stu-id="aa043-121">Enter **Y** to install the module.</span></span>
    3. <span data-ttu-id="aa043-122">Varmista, että moduuli on asennettu suorittamalla komento **Get-InstalledModule -Name "AzureAD"**.</span><span class="sxs-lookup"><span data-stu-id="aa043-122">Run the command **Get-InstalledModule -Name "AzureAD"** to verify that the module is installed.</span></span>
    4. <span data-ttu-id="aa043-123">Suorita todennus suorittamalla komento **Connect-AzureAD -Confirm**.</span><span class="sxs-lookup"><span data-stu-id="aa043-123">Run the command **Connect-AzureAD -Confirm** to run the authentication.</span></span>
    5. <span data-ttu-id="aa043-124">Suorita komento **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="aa043-124">Run the command **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="aa043-125">Toistamalla vaiheet 1–6 voit nyt varmistaa, että sovellustunnus on vuokraajassa.</span><span class="sxs-lookup"><span data-stu-id="aa043-125">You can now repeat steps 1 through 6 to verify that the app ID is in your tenant.</span></span>

### <a name="create-a-key-vault-resource"></a><span data-ttu-id="aa043-126">Avainsäilöresurssin luominen</span><span class="sxs-lookup"><span data-stu-id="aa043-126">Create a key vault resource</span></span>

<span data-ttu-id="aa043-127">Voit luoda avainsäilöresurssin seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="aa043-127">To create a key vault resource, follow these steps.</span></span>

1. <span data-ttu-id="aa043-128">Luo resurssiryhmä Azure-portaalissa tai siirry siihen.</span><span class="sxs-lookup"><span data-stu-id="aa043-128">In the Azure portal, create or go to a resource group.</span></span>
2. <span data-ttu-id="aa043-129">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="aa043-129">Select **Add**.</span></span>
3. <span data-ttu-id="aa043-130">Kirjoita **Uusi**-sivun hakukenttään **Avainsäilö**.</span><span class="sxs-lookup"><span data-stu-id="aa043-130">On the **New** page, in the search field, enter **Key vault**.</span></span> <span data-ttu-id="aa043-131">Valitse sitten **Luo**.</span><span class="sxs-lookup"><span data-stu-id="aa043-131">Then select **Create**.</span></span>
4. <span data-ttu-id="aa043-132">Anna nimi **Luo avainsäilö** -sivun **Avainsäilön nimi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="aa043-132">On the **Create key vault** page, in the **Key vault name** field, enter a name.</span></span>
5. <span data-ttu-id="aa043-133">Tarkista oletusarvot ja valitse sitten **Tarkista ja luo**.</span><span class="sxs-lookup"><span data-stu-id="aa043-133">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="aa043-134">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="aa043-134">Select **Create**.</span></span>

<span data-ttu-id="aa043-135">Avainsäilö luodaan taustalla.</span><span class="sxs-lookup"><span data-stu-id="aa043-135">The key vault is created in the background.</span></span>

### <a name="create-an-iot-hub-resource"></a><span data-ttu-id="aa043-136">IoT-resurssin luominen</span><span class="sxs-lookup"><span data-stu-id="aa043-136">Create an IoT hub resource</span></span>

<span data-ttu-id="aa043-137">Voit luoda IoT-keskitinresurssin seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="aa043-137">To create an IoT hub resource, follow these steps.</span></span>

1. <span data-ttu-id="aa043-138">Luo resurssiryhmä tai siirry siihen.</span><span class="sxs-lookup"><span data-stu-id="aa043-138">Create or go to a resource group.</span></span>
2. <span data-ttu-id="aa043-139">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="aa043-139">Select **Add**.</span></span>
3. <span data-ttu-id="aa043-140">Kirjoita **Uusi**-sivun hakukenttään **IoT-keskitin**.</span><span class="sxs-lookup"><span data-stu-id="aa043-140">On the **New** page, in the search field, enter **Iot Hub**.</span></span> <span data-ttu-id="aa043-141">Valitse sitten **Luo**.</span><span class="sxs-lookup"><span data-stu-id="aa043-141">Then select **Create**.</span></span>
4. <span data-ttu-id="aa043-142">Anna **IoT-keskittimen nimi**-kenttään nimi.</span><span class="sxs-lookup"><span data-stu-id="aa043-142">In the **IoT hub name** field, enter a name.</span></span>
5. <span data-ttu-id="aa043-143">Tarkista oletusarvot ja valitse sitten **Tarkista ja luo**.</span><span class="sxs-lookup"><span data-stu-id="aa043-143">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="aa043-144">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="aa043-144">Select **Create**.</span></span>

<span data-ttu-id="aa043-145">IoT-keskitin luodaan taustalla.</span><span class="sxs-lookup"><span data-stu-id="aa043-145">The IoT hub is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="aa043-146">Kutakin ympäristöä varten kannattaa luoda vain yksi IoT-keskitinresurssi.</span><span class="sxs-lookup"><span data-stu-id="aa043-146">We recommend that you create only one IoT hub resource per environment.</span></span>

### <a name="create-a-redis-cache-resource"></a><span data-ttu-id="aa043-147">Redis-välimuistiresurssin luominen</span><span class="sxs-lookup"><span data-stu-id="aa043-147">Create a Redis cache resource</span></span>

<span data-ttu-id="aa043-148">Voit luoda Redis-välimuistiresurssin seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="aa043-148">To create a Redis cache resource, follow these steps.</span></span>

1. <span data-ttu-id="aa043-149">Luo resurssiryhmä tai siirry siihen.</span><span class="sxs-lookup"><span data-stu-id="aa043-149">Create or go to a resource group.</span></span>
2. <span data-ttu-id="aa043-150">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="aa043-150">Select **Add**.</span></span>
3. <span data-ttu-id="aa043-151">Kirjoita **Uusi**-sivun hakukenttään **Azuren Redis-välimuisti**.</span><span class="sxs-lookup"><span data-stu-id="aa043-151">On the **New** page, in the search field, enter **Azure Cache for Redis**.</span></span> <span data-ttu-id="aa043-152">Valitse sitten **Luo**.</span><span class="sxs-lookup"><span data-stu-id="aa043-152">Then select **Create**.</span></span>
4. <span data-ttu-id="aa043-153">Anna nimi **DNS-nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aa043-153">In the **DNS name** field, enter a name.</span></span>
5. <span data-ttu-id="aa043-154">Tarkista oletusarvot ja valitse sitten **Luo**.</span><span class="sxs-lookup"><span data-stu-id="aa043-154">Review the default values, and then select **Create**.</span></span>

<span data-ttu-id="aa043-155">Redis-välimuisti luodaan taustalla.</span><span class="sxs-lookup"><span data-stu-id="aa043-155">The Redis cache is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="aa043-156">Kutakin ympäristöä varten kannattaa luoda vain yksi Redis-välimuisti.</span><span class="sxs-lookup"><span data-stu-id="aa043-156">We recommend that you create only one Redis cache per environment.</span></span>

<span data-ttu-id="aa043-157">Kaikki resurssit on nyt luotu.</span><span class="sxs-lookup"><span data-stu-id="aa043-157">All the resources have now been created.</span></span>

## <a name="configure-the-azure-resources"></a><span data-ttu-id="aa043-158">Azure-resurssien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="aa043-158">Configure the Azure resources</span></span>

### <a name="configure-the-iot-hub"></a><span data-ttu-id="aa043-159">IoT-keskittimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="aa043-159">Configure the IoT hub</span></span>

<span data-ttu-id="aa043-160">IoT-keskitin määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="aa043-160">To configure the IoT hub, follow these steps.</span></span>

1. <span data-ttu-id="aa043-161">Valitse resursseissa IoT-keskitinresurssi.</span><span class="sxs-lookup"><span data-stu-id="aa043-161">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="aa043-162">Valitse vasemmassa siirtymisruudussa **Sisäiset päätepisteet**.</span><span class="sxs-lookup"><span data-stu-id="aa043-162">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="aa043-163">Liitä seuraavat kuluttajaryhmät **Kuluttajaryhmät**-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="aa043-163">Under **Consumer groups**, paste the following consumer groups.</span></span> <span data-ttu-id="aa043-164">Nämä kuluttajaryhmät vastaavat heti käytettävissä olevia skenaarioita.</span><span class="sxs-lookup"><span data-stu-id="aa043-164">These consumer groups correspond to the out-of-box scenarios.</span></span>

    + <span data-ttu-id="aa043-165">microsoft.dynamics.iotintelligence-1</span><span class="sxs-lookup"><span data-stu-id="aa043-165">microsoft.dynamics.iotintelligence-1</span></span>
    + <span data-ttu-id="aa043-166">microsoft.dynamics.iotintelligence-2</span><span class="sxs-lookup"><span data-stu-id="aa043-166">microsoft.dynamics.iotintelligence-2</span></span>
    + <span data-ttu-id="aa043-167">microsoft.dynamics.iotintelligence-3</span><span class="sxs-lookup"><span data-stu-id="aa043-167">microsoft.dynamics.iotintelligence-3</span></span>

### <a name="configure-the-key-vault"></a><span data-ttu-id="aa043-168">Avainsäilön määrittäminen</span><span class="sxs-lookup"><span data-stu-id="aa043-168">Configure the key vault</span></span>

<span data-ttu-id="aa043-169">Avainsäilö määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="aa043-169">To configure the key vault, follow these steps.</span></span>

1. <span data-ttu-id="aa043-170">Valitse resursseissa avainsäilöresurssi.</span><span class="sxs-lookup"><span data-stu-id="aa043-170">In your resources, select the key vault resource.</span></span>
2. <span data-ttu-id="aa043-171">Valitse vasemmassa siirtymisruudussa **Käyttöoikeuskäytännöt**.</span><span class="sxs-lookup"><span data-stu-id="aa043-171">In the left navigation pane, select **Access policies**.</span></span>
3. <span data-ttu-id="aa043-172">Valitse **Lisää käyttöoikeuskäytäntö**.</span><span class="sxs-lookup"><span data-stu-id="aa043-172">Select **Add an access policy**.</span></span>
4. <span data-ttu-id="aa043-173">Valitse **Lisää käyttöoikeuskäytäntö** -sivun **Salauskoodin käyttöoikeudet** -kentässä **Hae** ja **Luettelo**.</span><span class="sxs-lookup"><span data-stu-id="aa043-173">On the **Add access policy** page, in the **Secret permissions** field, select **Get** and **List**.</span></span>
5. <span data-ttu-id="aa043-174">Valitse **Valitse päänimi**.</span><span class="sxs-lookup"><span data-stu-id="aa043-174">Click in the **Select principal**.</span></span>
6. <span data-ttu-id="aa043-175">Hae ja valitse **Päänimi**-valintaikkunassa **Microsoft Dynamics ERP Microservices**.</span><span class="sxs-lookup"><span data-stu-id="aa043-175">In the **Principal** dialog box, search for and select **Microsoft Dynamics ERP Microservices**.</span></span> <span data-ttu-id="aa043-176">Valitse sitten **Valitse**.</span><span class="sxs-lookup"><span data-stu-id="aa043-176">Then select **Select**.</span></span>
7. <span data-ttu-id="aa043-177">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="aa043-177">Select **Add**.</span></span>
8. <span data-ttu-id="aa043-178">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="aa043-178">Select **Save**.</span></span>

<span data-ttu-id="aa043-179">Sovelluksen on nyt avainsäilön salauskoodien käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="aa043-179">The app now has access to the secrets in the key vault.</span></span>

### <a name="save-the-iot-hub-connection-string-secret"></a><span data-ttu-id="aa043-180">IoT-keskittimen yhteysmerkkijonon salauskoodin tallentaminen</span><span class="sxs-lookup"><span data-stu-id="aa043-180">Save the IoT hub connection string secret</span></span>

<span data-ttu-id="aa043-181">IoT-keskittimen yhteysmerkkijonon salauskoodi tallennetaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="aa043-181">To save the secret for the IoT hub connection string, follow these steps.</span></span>

1. <span data-ttu-id="aa043-182">Valitse resursseissa IoT-keskitinresurssi.</span><span class="sxs-lookup"><span data-stu-id="aa043-182">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="aa043-183">Valitse vasemmassa siirtymisruudussa **Sisäiset päätepisteet**.</span><span class="sxs-lookup"><span data-stu-id="aa043-183">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="aa043-184">Kopioi **Tapahtuman keskittimen kanssa yhteensopiva päätepiste** -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="aa043-184">Copy the value in the **Event Hub-compatible endpoint** field.</span></span>
4. <span data-ttu-id="aa043-185">Siirry avainsäilöresurssiin.</span><span class="sxs-lookup"><span data-stu-id="aa043-185">Go to the key vault resource.</span></span>
5. <span data-ttu-id="aa043-186">Valitse vasemmassa siirtymisruudussa **Salauskoodit**.</span><span class="sxs-lookup"><span data-stu-id="aa043-186">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="aa043-187">Valitse **Luo tai tuo**.</span><span class="sxs-lookup"><span data-stu-id="aa043-187">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="aa043-188">Anna nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aa043-188">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="aa043-189">Liitä **Arvo**-kenttään aiemmin kopioitu päätepisteen arvo.</span><span class="sxs-lookup"><span data-stu-id="aa043-189">In the **Value** field, paste the endpoint value that you copied earlier.</span></span>
9. <span data-ttu-id="aa043-190">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="aa043-190">Select **Create**.</span></span>

### <a name="save-the-redis-cache-connection-string-secret"></a><span data-ttu-id="aa043-191">Redis-välimuistin yhteysmerkkijonon salauskoodin tallentaminen</span><span class="sxs-lookup"><span data-stu-id="aa043-191">Save the Redis cache connection string secret</span></span>

<span data-ttu-id="aa043-192">Redis-välimuistin yhteysmerkkijonon salauskoodi tallennetaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="aa043-192">To save the secret for the Redis cache connection string, follow these steps.</span></span>

1. <span data-ttu-id="aa043-193">Valitse resursseissa Redis-välimuistiresurssi.</span><span class="sxs-lookup"><span data-stu-id="aa043-193">In your resources, select the Redis cache resource.</span></span>
2. <span data-ttu-id="aa043-194">Valitse **Käyttöoikeusavaimet**.</span><span class="sxs-lookup"><span data-stu-id="aa043-194">Select **Access keys**.</span></span>
3. <span data-ttu-id="aa043-195">Kopioi **Ensisijainen yhteysmerkkijono** -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="aa043-195">Copy the value in the **Primary connection string** field.</span></span>
4. <span data-ttu-id="aa043-196">Siirry avainsäilöresurssiin.</span><span class="sxs-lookup"><span data-stu-id="aa043-196">Go to the key vault resource.</span></span>
5. <span data-ttu-id="aa043-197">Valitse vasemmassa siirtymisruudussa **Salauskoodit**.</span><span class="sxs-lookup"><span data-stu-id="aa043-197">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="aa043-198">Valitse **Luo tai tuo**.</span><span class="sxs-lookup"><span data-stu-id="aa043-198">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="aa043-199">Anna nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="aa043-199">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="aa043-200">Liitä **Arvo**-kenttään aiemmin kopioitu yhteysmerkkijono.</span><span class="sxs-lookup"><span data-stu-id="aa043-200">In the **Value** field, paste the connection string that you copied earlier.</span></span>
9. <span data-ttu-id="aa043-201">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="aa043-201">Select **Create**.</span></span>

> [!NOTE]
> <span data-ttu-id="aa043-202">Aina kun yhteysmerkkijono päivitetään, myös salauskoodin arvo on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="aa043-202">Whenever you update one of the connection strings, you must also update the secret values.</span></span>

<span data-ttu-id="aa043-203">Pakolliset Azure-resurssit on nyt valmisteltu.</span><span class="sxs-lookup"><span data-stu-id="aa043-203">You've now finished provisioning the required Azure resources.</span></span> <span data-ttu-id="aa043-204">Seuraavaksi [asennetaan IoT-analytiikkalisäosa Microsoft Dynamics Lifecycle Servicesiin (LCS)](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="aa043-204">The next step is to [install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>
