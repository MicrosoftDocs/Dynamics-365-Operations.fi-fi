---
title: IoT-analytiikan Azure-resurssien määrittäminen
description: Tässä ohjeaiheessa käsitellään IoT-analytiikkaa varten tarvittavien Microsoft Azure -resurssien luontia ja määrittämistä.
author: robinarh
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 33c28f8e7982c6ec9b892e975525de69fc637892
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881369"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a><span data-ttu-id="741ac-103">IoT-analytiikan Azure-resurssien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="741ac-103">Set up Azure resources for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="741ac-104">Tässä ohjeaiheessa käsitellään IoT-analytiikkaa varten tarvittavien Microsoft Azure -resurssien luontia ja määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="741ac-104">This topic explains how to create and configure the Microsoft Azure resources that you require for IoT Intelligence.</span></span>

## <a name="create-azure-resources"></a><span data-ttu-id="741ac-105">Azure-resurssien luominen</span><span class="sxs-lookup"><span data-stu-id="741ac-105">Create Azure resources</span></span>

<span data-ttu-id="741ac-106">Luo seuraavien ohjeiden avulla IoT-keskitin, Redis-välimuisti ja avainsäilö, jota Microsoft Dynamics 365 Supply Chain Management voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="741ac-106">Follow these steps to create an IoT hub, a Redis cache, and a key vault that can be accessed by Microsoft Dynamics 365 Supply Chain Management.</span></span>

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a><span data-ttu-id="741ac-107">Vuokraajan Microsoft Dynamics ERP Microservices -sovellustunnuksen varmistaminen</span><span class="sxs-lookup"><span data-stu-id="741ac-107">Verify that the Microsoft Dynamics ERP Microservices first-party app ID is in your tenant</span></span>

<span data-ttu-id="741ac-108">Seuraavien ohjeiden avulla varmistaa, että Microsoft Dynamics ERP Microservices -sovelluksen sovellustunnus on vuokraajassa.</span><span class="sxs-lookup"><span data-stu-id="741ac-108">To verify that the app ID for the Microsoft Dynamics ERP Microservices first-party app is in your tenant, follow these steps.</span></span>

1. <span data-ttu-id="741ac-109">Kirjaudu Azure-portaalin osoitteessa <https://portal.azure.com>.</span><span class="sxs-lookup"><span data-stu-id="741ac-109">Sign in to the Azure portal at <https://portal.azure.com>.</span></span>
2. <span data-ttu-id="741ac-110">Siirry osoitteeseen **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="741ac-110">Go to **Azure Active Directory**.</span></span>
3. <span data-ttu-id="741ac-111">Valitse **Yrityssovellukset**.</span><span class="sxs-lookup"><span data-stu-id="741ac-111">Go to **Enterprise applications**.</span></span>
4. <span data-ttu-id="741ac-112">Valitse **Sovelluksen tyyppi** -kentässä **Microsoft-sovellukset**.</span><span class="sxs-lookup"><span data-stu-id="741ac-112">In the **Application type** field, select **Microsoft applications**.</span></span>
5. <span data-ttu-id="741ac-113">Kirjoita hakukenttään **Microsoft Dynamics ERP Microservices**.</span><span class="sxs-lookup"><span data-stu-id="741ac-113">In the search field, enter **Microsoft Dynamics ERP Microservices**.</span></span>
6. <span data-ttu-id="741ac-114">Varmista, että **Microsoft Dynamics ERP Microservices** on luettelossa.</span><span class="sxs-lookup"><span data-stu-id="741ac-114">Verify that **Microsoft Dynamics ERP Microservices** is in the list.</span></span> <span data-ttu-id="741ac-115">Muilla sovelluksilla on samankaltaisia nimiä.</span><span class="sxs-lookup"><span data-stu-id="741ac-115">Other applications have similar names.</span></span> <span data-ttu-id="741ac-116">Varmista tämän vuoksi, että löydät oikean sovelluksen.</span><span class="sxs-lookup"><span data-stu-id="741ac-116">Therefore, make sure that you find the correct application.</span></span> <span data-ttu-id="741ac-117">Sovelluksen tunnus on **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="741ac-117">The app ID is **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="741ac-118">Jos sovellus ei ole luettelossa, se on lisättävä vuokraajaan:</span><span class="sxs-lookup"><span data-stu-id="741ac-118">If the application isn't in the list, you must add it to your tenant:</span></span>

    1. <span data-ttu-id="741ac-119">Valitse Azure-portaalin työkalurivillä painike, jolla Azure-pilviliittymä avataan.</span><span class="sxs-lookup"><span data-stu-id="741ac-119">In the Azure portal, on the toolbar, select the button to open Azure Cloud Shell.</span></span>
    2. <span data-ttu-id="741ac-120">Suorita komento **Install-Module AzureAD**.</span><span class="sxs-lookup"><span data-stu-id="741ac-120">Run the command **Install-Module AzureAD**.</span></span> <span data-ttu-id="741ac-121">Asenna moduuli kirjoittamalla **Y**.</span><span class="sxs-lookup"><span data-stu-id="741ac-121">Enter **Y** to install the module.</span></span>
    3. <span data-ttu-id="741ac-122">Varmista, että moduuli on asennettu suorittamalla komento **Get-InstalledModule -Name "AzureAD"**.</span><span class="sxs-lookup"><span data-stu-id="741ac-122">Run the command **Get-InstalledModule -Name "AzureAD"** to verify that the module is installed.</span></span>
    4. <span data-ttu-id="741ac-123">Suorita todennus suorittamalla komento **Connect-AzureAD -Confirm**.</span><span class="sxs-lookup"><span data-stu-id="741ac-123">Run the command **Connect-AzureAD -Confirm** to run the authentication.</span></span>
    5. <span data-ttu-id="741ac-124">Suorita komento **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="741ac-124">Run the command **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="741ac-125">Toistamalla vaiheet 1–6 voit nyt varmistaa, että sovellustunnus on vuokraajassa.</span><span class="sxs-lookup"><span data-stu-id="741ac-125">You can now repeat steps 1 through 6 to verify that the app ID is in your tenant.</span></span>

### <a name="create-a-key-vault-resource"></a><span data-ttu-id="741ac-126">Avainsäilöresurssin luominen</span><span class="sxs-lookup"><span data-stu-id="741ac-126">Create a key vault resource</span></span>

<span data-ttu-id="741ac-127">Voit luoda avainsäilöresurssin seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="741ac-127">To create a key vault resource, follow these steps.</span></span>

1. <span data-ttu-id="741ac-128">Luo resurssiryhmä Azure-portaalissa tai siirry siihen.</span><span class="sxs-lookup"><span data-stu-id="741ac-128">In the Azure portal, create or go to a resource group.</span></span>
2. <span data-ttu-id="741ac-129">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="741ac-129">Select **Add**.</span></span>
3. <span data-ttu-id="741ac-130">Kirjoita **Uusi**-sivun hakukenttään **Avainsäilö**.</span><span class="sxs-lookup"><span data-stu-id="741ac-130">On the **New** page, in the search field, enter **Key vault**.</span></span> <span data-ttu-id="741ac-131">Valitse sitten **Luo**.</span><span class="sxs-lookup"><span data-stu-id="741ac-131">Then select **Create**.</span></span>
4. <span data-ttu-id="741ac-132">Anna nimi **Luo avainsäilö** -sivun **Avainsäilön nimi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="741ac-132">On the **Create key vault** page, in the **Key vault name** field, enter a name.</span></span>
5. <span data-ttu-id="741ac-133">Tarkista oletusarvot ja valitse sitten **Tarkista ja luo**.</span><span class="sxs-lookup"><span data-stu-id="741ac-133">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="741ac-134">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="741ac-134">Select **Create**.</span></span>

<span data-ttu-id="741ac-135">Avainsäilö luodaan taustalla.</span><span class="sxs-lookup"><span data-stu-id="741ac-135">The key vault is created in the background.</span></span>

### <a name="create-an-iot-hub-resource"></a><span data-ttu-id="741ac-136">IoT-resurssin luominen</span><span class="sxs-lookup"><span data-stu-id="741ac-136">Create an IoT hub resource</span></span>

<span data-ttu-id="741ac-137">Voit luoda IoT-keskitinresurssin seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="741ac-137">To create an IoT hub resource, follow these steps.</span></span>

1. <span data-ttu-id="741ac-138">Luo resurssiryhmä tai siirry siihen.</span><span class="sxs-lookup"><span data-stu-id="741ac-138">Create or go to a resource group.</span></span>
2. <span data-ttu-id="741ac-139">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="741ac-139">Select **Add**.</span></span>
3. <span data-ttu-id="741ac-140">Kirjoita **Uusi**-sivun hakukenttään **IoT-keskitin**.</span><span class="sxs-lookup"><span data-stu-id="741ac-140">On the **New** page, in the search field, enter **Iot Hub**.</span></span> <span data-ttu-id="741ac-141">Valitse sitten **Luo**.</span><span class="sxs-lookup"><span data-stu-id="741ac-141">Then select **Create**.</span></span>
4. <span data-ttu-id="741ac-142">Anna **IoT-keskittimen nimi**-kenttään nimi.</span><span class="sxs-lookup"><span data-stu-id="741ac-142">In the **IoT hub name** field, enter a name.</span></span>
5. <span data-ttu-id="741ac-143">Tarkista oletusarvot ja valitse sitten **Tarkista ja luo**.</span><span class="sxs-lookup"><span data-stu-id="741ac-143">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="741ac-144">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="741ac-144">Select **Create**.</span></span>

<span data-ttu-id="741ac-145">IoT-keskitin luodaan taustalla.</span><span class="sxs-lookup"><span data-stu-id="741ac-145">The IoT hub is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="741ac-146">Kutakin ympäristöä varten kannattaa luoda vain yksi IoT-keskitinresurssi.</span><span class="sxs-lookup"><span data-stu-id="741ac-146">We recommend that you create only one IoT hub resource per environment.</span></span>

### <a name="create-a-redis-cache-resource"></a><span data-ttu-id="741ac-147">Redis-välimuistiresurssin luominen</span><span class="sxs-lookup"><span data-stu-id="741ac-147">Create a Redis cache resource</span></span>

<span data-ttu-id="741ac-148">Voit luoda Redis-välimuistiresurssin seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="741ac-148">To create a Redis cache resource, follow these steps.</span></span>

1. <span data-ttu-id="741ac-149">Luo resurssiryhmä tai siirry siihen.</span><span class="sxs-lookup"><span data-stu-id="741ac-149">Create or go to a resource group.</span></span>
2. <span data-ttu-id="741ac-150">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="741ac-150">Select **Add**.</span></span>
3. <span data-ttu-id="741ac-151">Kirjoita **Uusi**-sivun hakukenttään **Azuren Redis-välimuisti**.</span><span class="sxs-lookup"><span data-stu-id="741ac-151">On the **New** page, in the search field, enter **Azure Cache for Redis**.</span></span> <span data-ttu-id="741ac-152">Valitse sitten **Luo**.</span><span class="sxs-lookup"><span data-stu-id="741ac-152">Then select **Create**.</span></span>
4. <span data-ttu-id="741ac-153">Anna nimi **DNS-nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="741ac-153">In the **DNS name** field, enter a name.</span></span>
5. <span data-ttu-id="741ac-154">Tarkista oletusarvot ja valitse sitten **Luo**.</span><span class="sxs-lookup"><span data-stu-id="741ac-154">Review the default values, and then select **Create**.</span></span>

<span data-ttu-id="741ac-155">Redis-välimuisti luodaan taustalla.</span><span class="sxs-lookup"><span data-stu-id="741ac-155">The Redis cache is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="741ac-156">Kutakin ympäristöä varten kannattaa luoda vain yksi Redis-välimuisti.</span><span class="sxs-lookup"><span data-stu-id="741ac-156">We recommend that you create only one Redis cache per environment.</span></span>

<span data-ttu-id="741ac-157">Kaikki resurssit on nyt luotu.</span><span class="sxs-lookup"><span data-stu-id="741ac-157">All the resources have now been created.</span></span>

## <a name="configure-the-azure-resources"></a><span data-ttu-id="741ac-158">Azure-resurssien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="741ac-158">Configure the Azure resources</span></span>

### <a name="configure-the-iot-hub"></a><span data-ttu-id="741ac-159">IoT-keskittimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="741ac-159">Configure the IoT hub</span></span>

<span data-ttu-id="741ac-160">IoT-keskitin määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="741ac-160">To configure the IoT hub, follow these steps.</span></span>

1. <span data-ttu-id="741ac-161">Valitse resursseissa IoT-keskitinresurssi.</span><span class="sxs-lookup"><span data-stu-id="741ac-161">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="741ac-162">Valitse vasemmassa siirtymisruudussa **Sisäiset päätepisteet**.</span><span class="sxs-lookup"><span data-stu-id="741ac-162">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="741ac-163">Liitä seuraavat kuluttajaryhmät **Kuluttajaryhmät**-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="741ac-163">Under **Consumer groups**, paste the following consumer groups.</span></span> <span data-ttu-id="741ac-164">Nämä kuluttajaryhmät vastaavat heti käytettävissä olevia skenaarioita.</span><span class="sxs-lookup"><span data-stu-id="741ac-164">These consumer groups correspond to the out-of-box scenarios.</span></span>

    + <span data-ttu-id="741ac-165">microsoft.dynamics.iotintelligence-1</span><span class="sxs-lookup"><span data-stu-id="741ac-165">microsoft.dynamics.iotintelligence-1</span></span>
    + <span data-ttu-id="741ac-166">microsoft.dynamics.iotintelligence-2</span><span class="sxs-lookup"><span data-stu-id="741ac-166">microsoft.dynamics.iotintelligence-2</span></span>
    + <span data-ttu-id="741ac-167">microsoft.dynamics.iotintelligence-3</span><span class="sxs-lookup"><span data-stu-id="741ac-167">microsoft.dynamics.iotintelligence-3</span></span>

### <a name="configure-the-key-vault"></a><span data-ttu-id="741ac-168">Avainsäilön määrittäminen</span><span class="sxs-lookup"><span data-stu-id="741ac-168">Configure the key vault</span></span>

<span data-ttu-id="741ac-169">Avainsäilö määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="741ac-169">To configure the key vault, follow these steps.</span></span>

1. <span data-ttu-id="741ac-170">Valitse resursseissa avainsäilöresurssi.</span><span class="sxs-lookup"><span data-stu-id="741ac-170">In your resources, select the key vault resource.</span></span>
2. <span data-ttu-id="741ac-171">Valitse vasemmassa siirtymisruudussa **Käyttöoikeuskäytännöt**.</span><span class="sxs-lookup"><span data-stu-id="741ac-171">In the left navigation pane, select **Access policies**.</span></span>
3. <span data-ttu-id="741ac-172">Valitse **Lisää käyttöoikeuskäytäntö**.</span><span class="sxs-lookup"><span data-stu-id="741ac-172">Select **Add an access policy**.</span></span>
4. <span data-ttu-id="741ac-173">Valitse **Lisää käyttöoikeuskäytäntö** -sivun **Salauskoodin käyttöoikeudet** -kentässä **Hae** ja **Luettelo**.</span><span class="sxs-lookup"><span data-stu-id="741ac-173">On the **Add access policy** page, in the **Secret permissions** field, select **Get** and **List**.</span></span>
5. <span data-ttu-id="741ac-174">Valitse **Valitse päänimi**.</span><span class="sxs-lookup"><span data-stu-id="741ac-174">Click in the **Select principal**.</span></span>
6. <span data-ttu-id="741ac-175">Hae ja valitse **Päänimi**-valintaikkunassa **Microsoft Dynamics ERP Microservices**.</span><span class="sxs-lookup"><span data-stu-id="741ac-175">In the **Principal** dialog box, search for and select **Microsoft Dynamics ERP Microservices**.</span></span> <span data-ttu-id="741ac-176">Valitse sitten **Valitse**.</span><span class="sxs-lookup"><span data-stu-id="741ac-176">Then select **Select**.</span></span>
7. <span data-ttu-id="741ac-177">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="741ac-177">Select **Add**.</span></span>
8. <span data-ttu-id="741ac-178">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="741ac-178">Select **Save**.</span></span>

<span data-ttu-id="741ac-179">Sovelluksen on nyt avainsäilön salauskoodien käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="741ac-179">The app now has access to the secrets in the key vault.</span></span>

### <a name="save-the-iot-hub-connection-string-secret"></a><span data-ttu-id="741ac-180">IoT-keskittimen yhteysmerkkijonon salauskoodin tallentaminen</span><span class="sxs-lookup"><span data-stu-id="741ac-180">Save the IoT hub connection string secret</span></span>

<span data-ttu-id="741ac-181">IoT-keskittimen yhteysmerkkijonon salauskoodi tallennetaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="741ac-181">To save the secret for the IoT hub connection string, follow these steps.</span></span>

1. <span data-ttu-id="741ac-182">Valitse resursseissa IoT-keskitinresurssi.</span><span class="sxs-lookup"><span data-stu-id="741ac-182">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="741ac-183">Valitse vasemmassa siirtymisruudussa **Sisäiset päätepisteet**.</span><span class="sxs-lookup"><span data-stu-id="741ac-183">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="741ac-184">Kopioi **Tapahtuman keskittimen kanssa yhteensopiva päätepiste** -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="741ac-184">Copy the value in the **Event Hub-compatible endpoint** field.</span></span>
4. <span data-ttu-id="741ac-185">Siirry avainsäilöresurssiin.</span><span class="sxs-lookup"><span data-stu-id="741ac-185">Go to the key vault resource.</span></span>
5. <span data-ttu-id="741ac-186">Valitse vasemmassa siirtymisruudussa **Salauskoodit**.</span><span class="sxs-lookup"><span data-stu-id="741ac-186">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="741ac-187">Valitse **Luo tai tuo**.</span><span class="sxs-lookup"><span data-stu-id="741ac-187">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="741ac-188">Anna nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="741ac-188">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="741ac-189">Liitä **Arvo**-kenttään aiemmin kopioitu päätepisteen arvo.</span><span class="sxs-lookup"><span data-stu-id="741ac-189">In the **Value** field, paste the endpoint value that you copied earlier.</span></span>
9. <span data-ttu-id="741ac-190">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="741ac-190">Select **Create**.</span></span>

### <a name="save-the-redis-cache-connection-string-secret"></a><span data-ttu-id="741ac-191">Redis-välimuistin yhteysmerkkijonon salauskoodin tallentaminen</span><span class="sxs-lookup"><span data-stu-id="741ac-191">Save the Redis cache connection string secret</span></span>

<span data-ttu-id="741ac-192">Redis-välimuistin yhteysmerkkijonon salauskoodi tallennetaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="741ac-192">To save the secret for the Redis cache connection string, follow these steps.</span></span>

1. <span data-ttu-id="741ac-193">Valitse resursseissa Redis-välimuistiresurssi.</span><span class="sxs-lookup"><span data-stu-id="741ac-193">In your resources, select the Redis cache resource.</span></span>
2. <span data-ttu-id="741ac-194">Valitse **Käyttöoikeusavaimet**.</span><span class="sxs-lookup"><span data-stu-id="741ac-194">Select **Access keys**.</span></span>
3. <span data-ttu-id="741ac-195">Kopioi **Ensisijainen yhteysmerkkijono** -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="741ac-195">Copy the value in the **Primary connection string** field.</span></span>
4. <span data-ttu-id="741ac-196">Siirry avainsäilöresurssiin.</span><span class="sxs-lookup"><span data-stu-id="741ac-196">Go to the key vault resource.</span></span>
5. <span data-ttu-id="741ac-197">Valitse vasemmassa siirtymisruudussa **Salauskoodit**.</span><span class="sxs-lookup"><span data-stu-id="741ac-197">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="741ac-198">Valitse **Luo tai tuo**.</span><span class="sxs-lookup"><span data-stu-id="741ac-198">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="741ac-199">Anna nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="741ac-199">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="741ac-200">Liitä **Arvo**-kenttään aiemmin kopioitu yhteysmerkkijono.</span><span class="sxs-lookup"><span data-stu-id="741ac-200">In the **Value** field, paste the connection string that you copied earlier.</span></span>
9. <span data-ttu-id="741ac-201">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="741ac-201">Select **Create**.</span></span>

> [!NOTE]
> <span data-ttu-id="741ac-202">Aina kun yhteysmerkkijono päivitetään, myös salauskoodin arvo on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="741ac-202">Whenever you update one of the connection strings, you must also update the secret values.</span></span>

<span data-ttu-id="741ac-203">Pakolliset Azure-resurssit on nyt valmisteltu.</span><span class="sxs-lookup"><span data-stu-id="741ac-203">You've now finished provisioning the required Azure resources.</span></span> <span data-ttu-id="741ac-204">Seuraavaksi [asennetaan IoT-analytiikkalisäosa Microsoft Dynamics Lifecycle Servicesiin (LCS)](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="741ac-204">The next step is to [install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
