---
title: Siirtotilausten verotoiminnon tuki
description: Tässä aiheessa kuvataan siirtotilausten uutta verotoimintoa veron laskentapalvelua käyttäen.
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3a5c2b6fb48d98ba045c77ed034d976f7d89af98
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021366"
---
# <a name="tax-feature-support-for-transfer-orders"></a><span data-ttu-id="46c8f-103">Siirtotilausten verotoiminnon tuki</span><span class="sxs-lookup"><span data-stu-id="46c8f-103">Tax feature support for transfer orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="46c8f-104">Tässä ohjeaiheessa on tietoja verojen laskemisen ja kirjaamisen integroinnista siirtotilauksissa.</span><span class="sxs-lookup"><span data-stu-id="46c8f-104">This topic provides information about tax calculation and posting integration in transfer orders.</span></span> <span data-ttu-id="46c8f-105">Tämän toiminnon avulla voit määrittää verojen laskennan ja kirjauksen varastosiirtojen siirtotilauksissa.</span><span class="sxs-lookup"><span data-stu-id="46c8f-105">This functionality lets you set up tax calculation and posting in transfer orders for stock transfers.</span></span> <span data-ttu-id="46c8f-106">Euroopan unionin (EU) arvonlisäverosäädöksissä varastosiirtoja käsitellään yhteisön sisäisenä toimituksena ja yhteisön sisäisenä hankintana.</span><span class="sxs-lookup"><span data-stu-id="46c8f-106">Under European Union (EU) value-added tax (VAT) regulations, stock transfers are considered intra-community supply and intra-community acquisitions.</span></span>

<span data-ttu-id="46c8f-107">Tämän toiminnon konfiguroiminen ja käyttö edellyttää kolmen päävaiheen suoritusta:</span><span class="sxs-lookup"><span data-stu-id="46c8f-107">To configure and use this functionality, you must complete three main steps:</span></span>

1. <span data-ttu-id="46c8f-108">**RCS:n määritys:** Määritä Regulatory Configuration Servicessa siirtotilausten verokoodin määrittämisen verotoiminto, verokoodit ja verokoodien kohdistettavuus.</span><span class="sxs-lookup"><span data-stu-id="46c8f-108">**RCS setup:** In Regulatory Configuration Service, set up the tax feature, tax codes, and tax codes applicability for tax code determination in transfer orders.</span></span>
2. <span data-ttu-id="46c8f-109">**Financen asetukset:** Ota Microsoft Dynamics 365 Financessa käyttöön **Siirtotilauksen vero** -toiminto, määritä varaston veropalvelun parametrit ja määritä perusveroparametrit.</span><span class="sxs-lookup"><span data-stu-id="46c8f-109">**Finance setup:** In Microsoft Dynamics 365 Finance, turn on the **Tax in transfer order** feature, set up the tax service parameters for inventory, and set up core tax parameters.</span></span>
3. <span data-ttu-id="46c8f-110">**Varastoasetukset:** Määritä siirtotilaustapahtumien varastokonfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="46c8f-110">**Inventory setup:** Set up the inventory configuration for transfer order transactions.</span></span>

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a><span data-ttu-id="46c8f-111">RCS:n määrittäminen veroa ja siirtotilaustapahtumia varten</span><span class="sxs-lookup"><span data-stu-id="46c8f-111">Set up RCS for tax and transfer order transactions</span></span>

<span data-ttu-id="46c8f-112">Seuraavia ohjeita noudattamalla voit määrittää siirtotilauksen veron.</span><span class="sxs-lookup"><span data-stu-id="46c8f-112">Follow these steps to set up the tax that is involved in a transfer order.</span></span> <span data-ttu-id="46c8f-113">Tässä olevassa esimerkissä siirtotilaus on Alankomaista Belgiaan.</span><span class="sxs-lookup"><span data-stu-id="46c8f-113">In the example that is shown here, the transfer order is from the Netherlands to Belgium.</span></span>

1. <span data-ttu-id="46c8f-114">Valitse **Verotoiminnot**-sivun **Versiot**-välilehdestä luonnosominaisuuden versio ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-114">On the **Tax features** page, on the **Versions** tab, select the draft feature version, and then select **Edit**.</span></span>

    ![Muokkauksen valitseminen](../media/tax-feature-support-01.png)

2. <span data-ttu-id="46c8f-116">Valitse **Verotoimintojen asetukset** -sivun **Verokoodit**-välilehdestä **Lisää** luodaksesi uusia verokoodeja.</span><span class="sxs-lookup"><span data-stu-id="46c8f-116">On the **Tax features setup** page, on the **Tax codes** tab, select **Add** to create new tax codes.</span></span> <span data-ttu-id="46c8f-117">Tässä esimerkissä luodaan kolme verokoodia: **NL-Exempt**, **BE-RC-21** ja **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-117">For this example, three tax codes are created: **NL-Exempt**, **BE-RC-21**, and **BE-RC+21**.</span></span>

    - <span data-ttu-id="46c8f-118">Kun siirtotilaus lähetetään Alankomaiden varastosta, käytetään Alankomaiden ALV-vapautuskoodia  (**NL-Exempt**).</span><span class="sxs-lookup"><span data-stu-id="46c8f-118">When a transfer order is shipped from a warehouse in the Netherlands, the Netherlands VAT exempted tax code (**NL-Exempt**) is applied.</span></span>
      
        <span data-ttu-id="46c8f-119">Luo verokoodi **NL-Exempt**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-119">Create the tax code **NL-Exempt**.</span></span>
        1. <span data-ttu-id="46c8f-120">Valitse **Lisää** ja kirjoita **Verokoodi**-kenttään **NL-Exempt**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-120">Select **Add**, enter **NL-Exempt** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="46c8f-121">Valitse **Verokomponentti**-kentässä **Nettosumman mukaan**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-121">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="46c8f-122">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-122">Select **Save**.</span></span>
        4. <span data-ttu-id="46c8f-123">Valitse **Prosentti**-välilehdessä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-123">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="46c8f-124">Vaihda **On veroton** -arvoksi **Kyllä** **Yleiset**-osassa.</span><span class="sxs-lookup"><span data-stu-id="46c8f-124">Swtich **Is Exempt** to **Yes** in the **General** section.</span></span>

        ![NL-Exempt-verokoodi](../media/tax-feature-support-02.png)

    - <span data-ttu-id="46c8f-126">Kun siirtotilaus vastaanotetaan Belgian varastossa, käänteisen veloituksen menetelmää käytetään **BE-RC-21**- ja **BE-RC+21**-verokoodien avulla.</span><span class="sxs-lookup"><span data-stu-id="46c8f-126">When a transfer order is received at a Belgium warehouse, the reverse charge mechanism is applied by using the **BE-RC-21** and **BE-RC+21** tax codes.</span></span>
        
        <span data-ttu-id="46c8f-127">Luo verokoodi **BE-RC-21**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-127">Create the tax code **BE-RC-21**.</span></span>      
        1. <span data-ttu-id="46c8f-128">Valitse **Lisää** ja kirjoita **Verokoodi**-kenttään **BE-RC-21**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-128">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="46c8f-129">Valitse **Verokomponentti**-kentässä **Nettosumman mukaan**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-129">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="46c8f-130">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-130">Select **Save**.</span></span>
        4. <span data-ttu-id="46c8f-131">Valitse **Prosentti**-välilehdessä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-131">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="46c8f-132">Kirjoita **Veroprosentti**-kenttään **-21**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-132">Enter **-21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="46c8f-133">Vaihda **On käänteinen veloitus** -arvoksi **Kyllä** **Yleiset**-osassa.</span><span class="sxs-lookup"><span data-stu-id="46c8f-133">Swtich **Is Reverse Charge** to **Yes** in the **General** section.</span></span>
        7. <span data-ttu-id="46c8f-134">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-134">Select **Save**.</span></span>

        ![BE-RC-21-verokoodi käänteiselle veloitukselle](../media/tax-feature-support-03.png)
        
        <span data-ttu-id="46c8f-136">Luo verokoodi **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-136">Create the tax code **BE-RC+21**.</span></span>
        1. <span data-ttu-id="46c8f-137">Valitse **Lisää** ja kirjoita **Verokoodi**-kenttään **BE-RC-21**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-137">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="46c8f-138">Valitse **Verokomponentti**-kentässä **Nettosumman mukaan**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-138">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="46c8f-139">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-139">Select **Save**.</span></span>
        4. <span data-ttu-id="46c8f-140">Valitse **Prosentti**-välilehdessä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-140">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="46c8f-141">Kirjoita **Veroprosentti**-kenttään **21**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-141">Enter **21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="46c8f-142">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-142">Select **Save**.</span></span>

        ![BE-RC+21-verokoodi käänteiselle veloitukselle](../media/tax-feature-support-04.png)

3. <span data-ttu-id="46c8f-144">Määritä verokoodien kohdistettavuus.</span><span class="sxs-lookup"><span data-stu-id="46c8f-144">Define the applicability of the tax codes.</span></span>

    1. <span data-ttu-id="46c8f-145">Valitse **Sarakkeiden hallinta** ja valitse sitten sarakkeet, joita käytetään käytettävyystaulun muodostamiseksi.</span><span class="sxs-lookup"><span data-stu-id="46c8f-145">Select **Manage columns**, and then select columns that should be used to build the applicability table.</span></span>

        > [!NOTE]
        > <span data-ttu-id="46c8f-146">Varmista, että lisäät tauluun **Liiketoimintaprosessi**- ja **Veron suunta** -sarakkeet.</span><span class="sxs-lookup"><span data-stu-id="46c8f-146">Be sure to add the **Business process** and **Tax directions** columns to the table.</span></span> <span data-ttu-id="46c8f-147">Molemmat sarakkeet ovat olennaista siirtotilausten verojen toiminnallisuudessa.</span><span class="sxs-lookup"><span data-stu-id="46c8f-147">Both columns are essential to the functionality for tax in transfer orders.</span></span>

    2. <span data-ttu-id="46c8f-148">Lisää kohdistettavuusssäännöt.</span><span class="sxs-lookup"><span data-stu-id="46c8f-148">Add applicability rules.</span></span> <span data-ttu-id="46c8f-149">Älä jätä **Verokoodit**-, **Veroryhmä**- tai **Nimikkeen veroryhmä** -kenttiä tyhjiksi.</span><span class="sxs-lookup"><span data-stu-id="46c8f-149">Don't leave the **Tax codes**, **Tax group**, and **Item tax group** fields blank.</span></span>
        
        <span data-ttu-id="46c8f-150">Lisää uusi sääntö siirtotilauslähetykseen.</span><span class="sxs-lookup"><span data-stu-id="46c8f-150">Add a new rule for transfer order shipment.</span></span>
        1. <span data-ttu-id="46c8f-151">Valitse **Soveltuvuussäännöt**-välilehdessä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-151">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="46c8f-152">Ota sääntö käyttöön siirtotilausta varten valitsemalla **Liiketoimintaprosessi**-kentässä **Varasto**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-152">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="46c8f-153">Kirjoita **Toimitus maasta/alueelta** -kenttään **NLD**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-153">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="46c8f-154">Kirjoita **Toimitus maahan/alueelle** -kenttään **BEL**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-154">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="46c8f-155">Valitse **Veron suunta**-kentässä **Tulos**, jos haluat, että sääntöä sovelletaan siirtotilauksen toimitukseen.</span><span class="sxs-lookup"><span data-stu-id="46c8f-155">In the **Tax direction** field, select **Output** to make the rule applicable to transfer order shipment.</span></span>
        6. <span data-ttu-id="46c8f-156">Valitse **Verokoodit**-kentässä **NL-Exempt**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-156">In the **Tax codes** field, select **NL-Exempt**.</span></span>
        7. <span data-ttu-id="46c8f-157">Syötä **Veroryhmä**- ja **Nimikkeen veroryhmä** -kentissä liittyvä arvonlisäveroryhmä ja nimikkeen arvonlisäveroryhmä, jotka on määritetty Finance-järjestelmässäsi.</span><span class="sxs-lookup"><span data-stu-id="46c8f-157">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>
        
        <span data-ttu-id="46c8f-158">Lisää toinen sääntö siirtotilauksen vastaanottoon.</span><span class="sxs-lookup"><span data-stu-id="46c8f-158">Add another rule for transfer order receipt.</span></span>
        1. <span data-ttu-id="46c8f-159">Valitse **Soveltuvuussäännöt**-välilehdessä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-159">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="46c8f-160">Ota sääntö käyttöön siirtotilausta varten valitsemalla **Liiketoimintaprosessi**-kentässä **Varasto**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-160">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="46c8f-161">Kirjoita **Toimitus maasta/alueelta** -kenttään **NLD**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-161">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="46c8f-162">Kirjoita **Toimitus maahan/alueelle** -kenttään **BEL**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-162">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="46c8f-163">Valitse **Veron suunta**-kentässä **Syöte**, jos haluat, että sääntöä sovelletaan siirtotilauksen vastaanottoon.</span><span class="sxs-lookup"><span data-stu-id="46c8f-163">In the **Tax direction** field, select **Input** to make the rule applicable to transfer order receipt.</span></span>
        6. <span data-ttu-id="46c8f-164">Valitse **Verokoodit**-kentästä **BE-RC+21** ja **BE-RC-21**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-164">In the **Tax codes** field, select **BE-RC+21** and **BE-RC-21**.</span></span>
        7. <span data-ttu-id="46c8f-165">Syötä **Veroryhmä**- ja **Nimikkeen veroryhmä** -kentissä liittyvä arvonlisäveroryhmä ja nimikkeen arvonlisäveroryhmä, jotka on määritetty Finance-järjestelmässäsi.</span><span class="sxs-lookup"><span data-stu-id="46c8f-165">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>

        ![Soveltuvuussäännöt](../media/image5.png)

4. <span data-ttu-id="46c8f-167">Täydennä ja julkaise uusi vero-ominaisuusversio.</span><span class="sxs-lookup"><span data-stu-id="46c8f-167">Complete and publish the new tax feature version.</span></span>

    <span data-ttu-id="46c8f-168">[![Uuden version tilan muuttaminen](../media/image6.png)](../media/image6.png)</span><span class="sxs-lookup"><span data-stu-id="46c8f-168">[![Changing the status of the new version](../media/image6.png)](../media/image6.png)</span></span>

## <a name="set-up-finance-for-transfer-order-transactions"></a><span data-ttu-id="46c8f-169">Financen määrittäminen siirtotilaustapahtumia varten</span><span class="sxs-lookup"><span data-stu-id="46c8f-169">Set up Finance for transfer order transactions</span></span>

<span data-ttu-id="46c8f-170">Ota käyttöön ja määritä verot siirtotilauksille seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="46c8f-170">Follow these steps to enable and set up taxes for transfer orders.</span></span>

1. <span data-ttu-id="46c8f-171">Valitse Financessa **Työtilat** \> **Ominaisuuden hallinta**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-171">In Finance, go to **Workspaces** \> **Feature management**.</span></span>
2. <span data-ttu-id="46c8f-172">Etsi ja valitse luettelosta **Siirtotilauksen vero** -ominaisuus ja ota se sitten käyttöön valitsemalla **Ota käyttöön nyt**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-172">In the list, find and select the **Tax in transfer order** feature, and then select **Enable now** to turn it on.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="46c8f-173">**Siirtotilauksen vero** -ominaisuus on täysin riippuvainen veropalvelusta.</span><span class="sxs-lookup"><span data-stu-id="46c8f-173">The **Tax in transfer order** feature is fully dependent on the tax service.</span></span> <span data-ttu-id="46c8f-174">Siksi se voidaan ottaa käyttöön vasta, kun olet asentanut veropalvelun.</span><span class="sxs-lookup"><span data-stu-id="46c8f-174">Therefore, it can be turned on only after you've installed the tax service.</span></span>

    ![Siirtotilauksen vero -ominaisuus](../media/image7.png)

3. <span data-ttu-id="46c8f-176">Ota veropalvelu käyttöön ja valitse **Varasto**-liiketoimintaprosessi.</span><span class="sxs-lookup"><span data-stu-id="46c8f-176">Enable the tax service, and select the **Inventory** business process.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="46c8f-177">Tämä vaihe on suoritettava jokaiselle Financen oikeushenkilölle, jossa haluat veropalvelun ja Siirtotilauksen vero -toiminnon olevan käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="46c8f-177">You must complete this step for each legal entity in Finance where you want the tax service and the functionality for tax in transfer orders to be available.</span></span>

    1. <span data-ttu-id="46c8f-178">Siirry kohtaan **Vero** \> **Asetukset** \> **Veromääritys** \> **Veropalvelun määritys**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-178">Go to **Tax** \> **Setup** \> **Tax configuration** \> **Tax service setup**.</span></span>
    2. <span data-ttu-id="46c8f-179">Valitse **Liiketoimintaprosessi**-kentässä **Varasto**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-179">In the **Business process** field, select **Inventory**.</span></span>

    ![Liiketoimintaprosessi-kentän määrittäminen](../media/image8.png)

4. <span data-ttu-id="46c8f-181">Varmista, että käänteinen veloitusmekanismi on määritetty.</span><span class="sxs-lookup"><span data-stu-id="46c8f-181">Verify that the reverse charge mechanism is set up.</span></span> <span data-ttu-id="46c8f-182">Siirry kohtaan **Kirjanpito** \> **Asetukset** \> **Parametrit** ja varmista sitten **Käänteinen veloitus** -välilehdessä, että **Ota käänteinen veloitus käyttöön** -asetuksen arvo on **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-182">Go to **General ledger** \> **Setup** \> **Parameters**, and then, on the **Reverse charge** tab, verify that the **Enable reverse charge** option is set to **Yes**.</span></span>

    ![Ota käänteinen veloitus käyttöön -asetus](../media/image9.png)

5. <span data-ttu-id="46c8f-184">Varmista, että liittyvät verokoodit, veroryhmät, nimikkeen veroryhmät ja ALV-rekisterinumerot on määritetty Financessa veropalvelun ohjeistuksen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="46c8f-184">Verify that the related tax codes, tax groups, item tax groups, and VAT registration numbers have been set up in Finance according to the tax service guidance.</span></span>
6. <span data-ttu-id="46c8f-185">Määritä väliaikainen siirtotili.</span><span class="sxs-lookup"><span data-stu-id="46c8f-185">Set up an interim transit account.</span></span> <span data-ttu-id="46c8f-186">Tämä vaihe on pakollinen vain, jos siirtotilaukseen sovellettavaa veroa ei sovelleta verovapautukseen tai käännetyn veloituksen verojen mekanismiin.</span><span class="sxs-lookup"><span data-stu-id="46c8f-186">This step is required only when the tax that is applied to a transfer order isn't applicable to a tax exempted or reverse charge mechanism.</span></span>

    1. <span data-ttu-id="46c8f-187">Siirry kohtaan **Vero** \> **Asetukset** \> **Arvonlisävero** \> **Kirjanpidon kirjausryhmät**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-187">Go to **Tax** \> **Setup** \> **Sales tax** \> **Ledger posting groups**.</span></span>
    2. <span data-ttu-id="46c8f-188">Valitse **Väliaikainen siirto** -kentästä kirjanpitotili.</span><span class="sxs-lookup"><span data-stu-id="46c8f-188">In the **Interim transit** field, select a ledger account.</span></span>

    ![Väliaikaisen siirtotilin valinta](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a><span data-ttu-id="46c8f-190">Perusvaraston määrittäminen siirtotilaustapahtumia varten</span><span class="sxs-lookup"><span data-stu-id="46c8f-190">Set up basic inventory for transfer order transactions</span></span>

<span data-ttu-id="46c8f-191">Näiden vaiheiden avulla voit määrittää perusvaraston, joka ottaa siirtotilaustapahtumat käyttöön.</span><span class="sxs-lookup"><span data-stu-id="46c8f-191">Follow these steps to set up basic inventory to enable transfer order transactions.</span></span>

1. <span data-ttu-id="46c8f-192">Luo lähetys- ja vastaanottotoimipaikat eri maiden tai alueiden varastoille ja lisää kunkin toimipaikan ensisijainen osoite.</span><span class="sxs-lookup"><span data-stu-id="46c8f-192">Create ship-from and ship-to sites for your warehouses in different countries or regions, and add the primary address for each site.</span></span>

    1. <span data-ttu-id="46c8f-193">Valitse **Varastonhallinta** \> **Asetukset** \> **Varasto** \> **Toimipaikat**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-193">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Sites**.</span></span>
    2. <span data-ttu-id="46c8f-194">Valitse **Uusi**, jos haluat luoda toimipaikan, jonka liität varastoon myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="46c8f-194">Select **New** to create the site that you will assign to a warehouse later.</span></span>
    3. <span data-ttu-id="46c8f-195">Toista vaihe 2 kaikille muille toimipaikoille, jotka sinun on luotava.</span><span class="sxs-lookup"><span data-stu-id="46c8f-195">Repeat step 2 for all the other sites that you must create.</span></span>

    > [!NOTE]
    > <span data-ttu-id="46c8f-196">Yhden luodun toimipaikan nimi on oltava **Siirto**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-196">One of the sites that you create should be named **Transit**.</span></span> <span data-ttu-id="46c8f-197">Tämän menettelyn myöhemmässä vaiheessa tämä toimipaikka määritetään siirtovarastoon, jotta veroihin liittyvät varastotositteet voidaan kirjata siirtotilausten toimitus- ja vastaanottotapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="46c8f-197">In later steps of this procedure, you will assign this site to the transit warehouse, so that tax-related inventory vouchers can be posted in "ship" and "receive" transactions for transfer orders.</span></span> <span data-ttu-id="46c8f-198">Siirtopaikan osoite ei ole merkityksellinen verolaskelman kannalta.</span><span class="sxs-lookup"><span data-stu-id="46c8f-198">The address of the transit site is irrelevant to tax calculation.</span></span> <span data-ttu-id="46c8f-199">Tämän vuoksi kenttä voidaan jättää tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="46c8f-199">Therefore, you can leave it blank.</span></span>

    ![Toimipaikkojen määritys](../media/image11.png)

2. <span data-ttu-id="46c8f-201">Luo lähetys-, siirto- ja vastaanottovarastot.</span><span class="sxs-lookup"><span data-stu-id="46c8f-201">Create ship-from, transit, and ship-to warehouses.</span></span> <span data-ttu-id="46c8f-202">Kaikki fyysisessä varastossa ylläpidettävät osoitetiedot ohittavat toimipaikan osoitteen veronlaskennan aikana.</span><span class="sxs-lookup"><span data-stu-id="46c8f-202">Any address information that is maintained in a warehouse will override the site address during tax calculation.</span></span>

    1. <span data-ttu-id="46c8f-203">Valitse **Varastonhallinta** \> **Asetukset** \> **Varasto** \> **Varastot**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-203">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Warehouses**.</span></span>
    2. <span data-ttu-id="46c8f-204">Valitse **Uusi**, jos haluat luoda fyysisien varaston ja liittää sen vastaavaan toimipaikkaan.</span><span class="sxs-lookup"><span data-stu-id="46c8f-204">Select **New** to create a warehouse, and assign it to the corresponding site.</span></span>
    3. <span data-ttu-id="46c8f-205">Toista vaihe 2, jos haluat luoda fyysisen varaston kullekin toimipaikalle tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="46c8f-205">Repeat step 2 to create a warehouse for each site as required.</span></span>

    ![Fyysisiten varastojen määrittäminen](../media/image12.png)

    > [!NOTE]
    > <span data-ttu-id="46c8f-207">Lähetysvarastolle siirtovarasto on valittava **Siirtovarasto**-kentässä siirtotilaustapahtumia varten.</span><span class="sxs-lookup"><span data-stu-id="46c8f-207">For a ship-from warehouse, a transit warehouse must be selected in the **Transit warehouse** field for transfer order transactions.</span></span>
    >
    > ![Siirtovaraston valitseminen](../media/image13.png)

3. <span data-ttu-id="46c8f-209">Varmista, että siirtotilaustapahtumien varastokirjauskonfiguraatio on määritetty.</span><span class="sxs-lookup"><span data-stu-id="46c8f-209">Verify that the inventory posting configuration is set up for transfer order transactions.</span></span>

    1. <span data-ttu-id="46c8f-210">Siirry kohtaan **Varastonhallinta** \> **Määritys** \> **Kirjaus** \> **Kirjaus**.</span><span class="sxs-lookup"><span data-stu-id="46c8f-210">Go to **Inventory management** \> **Setup** \> **Posting** \> **Posting**.</span></span>
    2. <span data-ttu-id="46c8f-211">Varmista **Varasto**-välilehdessä, että kirjanpitotili on määritetty sekä **Varasto-otto**- että **Varastovastaanotto** -kirjausta varten.</span><span class="sxs-lookup"><span data-stu-id="46c8f-211">On the **Inventory** tab, verify that a ledger account is set up for both **Inventory issue** and **Inventory receipt** posting.</span></span>

        ![Varasto-oton ja varastovastaanoton kirjauksen määrittäminen](../media/image14.png)

    3. <span data-ttu-id="46c8f-213">Varmista, että kirjanpitotilille on määritetty **Yksiköiden väliset saatavat** -kirjaus.</span><span class="sxs-lookup"><span data-stu-id="46c8f-213">Verify that a ledger account is set up for **Inter-unit payable** posting.</span></span>

        ![Yksiköiden väliset saatavat -kirjauksen määrittäminen](../media/image15.png)

    4. <span data-ttu-id="46c8f-215">Varmista, että kirjanpitotilille on määritetty **Yksiköiden väliset maksettavat** -kirjaus.</span><span class="sxs-lookup"><span data-stu-id="46c8f-215">Verify that a ledger account is set up for **Inter-unit receivable** posting.</span></span>

        ![Yksiköiden väliset maksettavat -kirjauksen määrittäminen](../media/image16.png)
