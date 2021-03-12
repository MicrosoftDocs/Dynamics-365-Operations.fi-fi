---
title: Dynamics 365 Supply Chain Managementin (Resurssien hallinta) integrointi Dynamics 365 Guidesin kanssa
description: Tässä ohjeaiheessa kerrotaan, miten Microsoft  Dynamics 365 Supply Chain Managementin käyttöomaisuudenhallintamoduuli integroidaan Dynamics 365 Guidesin kanssa, jotta voidaan hyödyntää päivittäisissä huolto- ja ylläpitotyökuluissa yhdistetyn todellisuuden oppaita.
author: kamaybac
manager: tfehr
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: ae26012d236a44bfa0c8453bdc660671ddee82a4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000281"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a><span data-ttu-id="98bba-103">Dynamics 365 Supply Chain Managementin (Resurssien hallinta) integrointi Dynamics 365 Guidesin kanssa</span><span class="sxs-lookup"><span data-stu-id="98bba-103">Integrate Dynamics 365 Supply Chain Management (Asset management) with Dynamics 365 Guides</span></span>

<span data-ttu-id="98bba-104">Microsoft Dynamics 365 Supply Chain Managementin **käyttöomaisuudenhallinta**-moduuli integroidaan Dynamics 365 Guidesin kanssa, jotta voidaan hyödyntää päivittäisissä huolto- ja ylläpitotyökuluissa yhdistetyn todellisuuden oppaita.</span><span class="sxs-lookup"><span data-stu-id="98bba-104">You can integrate the **Asset management** module in Microsoft Dynamics 365 Supply Chain Management with Dynamics 365 Guides to take advantage of mixed-reality guides in your day-to-day service and maintenance workflows.</span></span> <span data-ttu-id="98bba-105">Jos opas liittyy käyttöomaisuuden hallinnan työtilaukseen, työntekijä, joka avaa työtilauksen ylläpidon tarkistusluettelon Supply Chain Managementin (Dynamics 365) -mobiilisovelluksessa, näkee, että opas on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="98bba-105">If a guide is associated with an Asset Management work order, a worker who opens the work order's maintenance checklist in the Supply Chain Management (Dynamics 365) mobile app sees that a guide is available.</span></span> <span data-ttu-id="98bba-106">Työntekijä voi sitten etsiä ja avata oppaan Dynamics 365 Guidesin HoloLens-sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="98bba-106">The worker can then find and open the guide in the Dynamics 365 Guides HoloLens app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="98bba-107">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="98bba-107">Prerequisites</span></span>

<span data-ttu-id="98bba-108">Ennen kuin voit liittää ohjeita käyttöomaisuuden hallinnan työtilauksiin, sinun on täytettävä seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="98bba-108">Before you can attach guides to Asset management work orders, you must complete these prerequisites:</span></span>

- <span data-ttu-id="98bba-109">[Asenna Dynamics 365 Supply Chain Management -sovelluksen](../../fin-ops-core/fin-ops/index.md) versio 10.0.9 tai uudempi.</span><span class="sxs-lookup"><span data-stu-id="98bba-109">[Set up Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) version 10.0.9 or later.</span></span>
- <span data-ttu-id="98bba-110">[Ota käyttöön kaksoiskirjoituslähde Supply Chain Management -sovelluksissa](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="98bba-110">[Turn on dual-write for Supply Chain Management apps](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span></span>
- <span data-ttu-id="98bba-111">[Ota väliversio käyttöön](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) **MRGuidesFeature** -ominaisuudesta.</span><span class="sxs-lookup"><span data-stu-id="98bba-111">[Turn on flight](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) for the **MRGuidesFeature** feature.</span></span> <span data-ttu-id="98bba-112">(Tuotantoympäristöissä on ensin lähetettävä tukipyyntö, jotta vuokralaisesi lisätään flighting-ryhmään.)</span><span class="sxs-lookup"><span data-stu-id="98bba-112">(For production environments, you must first submit a support ticket to have your tenant added to the flighting group.)</span></span>
- <span data-ttu-id="98bba-113">[Ota seuraavat konfigurointiavaimet käyttöön](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) **käyttöoikeuksienmääritys** -sivulla:</span><span class="sxs-lookup"><span data-stu-id="98bba-113">[Turn on the following configuration keys](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) on the **License configuration** page:</span></span>

    - <span data-ttu-id="98bba-114">Resurssienhallinta \> Resurssienhallinnan yhdistetty todellisuus</span><span class="sxs-lookup"><span data-stu-id="98bba-114">Asset management \> Asset management mixed reality</span></span>
    - <span data-ttu-id="98bba-115">Yhdistetty todellisuus \> Yhdistetyn todellisuuden opas</span><span class="sxs-lookup"><span data-stu-id="98bba-115">Mixed reality \> Mixed reality guide</span></span>

- <span data-ttu-id="98bba-116">[Asenna Dynamics 365 Guides -sovelluksen](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) versio 200.0.0.96 tai uudempi.</span><span class="sxs-lookup"><span data-stu-id="98bba-116">[Set up Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 200.0.0.96 or later.</span></span>

## <a name="use-dynamics-365-guides-with-asset-management"></a><span data-ttu-id="98bba-117">Käytä Dynamics 365 Guidesia resurssienhallinnan kanssa</span><span class="sxs-lookup"><span data-stu-id="98bba-117">Use Dynamics 365 Guides with Asset management</span></span>

<span data-ttu-id="98bba-118">Jos haluat liittää oppaan, käytä resurssienhallinnassa ylläpidon tarkistuslistaa.</span><span class="sxs-lookup"><span data-stu-id="98bba-118">To associate a guide, you use a maintenance checklist line in Asset management.</span></span> <span data-ttu-id="98bba-119">Voit luoda liitoksen ylläpidon tarkistuslistamallin, ylläpitotyön tyypin tai työtilauksen kautta, koska kaikki kolme sisältävät ylläpidon tarkistuslistarivejä.</span><span class="sxs-lookup"><span data-stu-id="98bba-119">You can create the association through a maintenance checklist template, a maintenance job type, or a work order, because all three contain maintenance checklist lines.</span></span> <span data-ttu-id="98bba-120">Voit säästää aikaa mallin avulla, koska malli voidaan liittää kaikkiin sitä käyttävien kunnossapitotöiden tyyppeihin.</span><span class="sxs-lookup"><span data-stu-id="98bba-120">You can save time by using a template, because a template can be associated with all the maintenance job types that use it.</span></span> <span data-ttu-id="98bba-121">Esimerkiksi kunnossapitotyötyyppiin liittyvä opas liitetään automaattisesti kaikkiin työtilauksiin, jotka määrittävät tämän työlajin.</span><span class="sxs-lookup"><span data-stu-id="98bba-121">For example, a guide that is associated with a maintenance job type is automatically associated with all work orders that specify that job type.</span></span> <span data-ttu-id="98bba-122">Toisaalta työtilaukseen suoraan liittyvä opas on olemassa vain kyseisessä työtilauksessa.</span><span class="sxs-lookup"><span data-stu-id="98bba-122">On the other hand, a guide that is associated directly with a work order exists only for that work order.</span></span>

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a><span data-ttu-id="98bba-123">Oppaan ja ylläpidon tarkistuslistamallin kytkeminen</span><span class="sxs-lookup"><span data-stu-id="98bba-123">Associate a guide with a maintenance checklist template</span></span>

<span data-ttu-id="98bba-124">Seuraa näitä ohjeita, oppaan ja ylläpidon tarkistuslistamallin kytkemiseksi.</span><span class="sxs-lookup"><span data-stu-id="98bba-124">To associate a guide with a maintenance checklist template, follow these steps.</span></span>

1. <span data-ttu-id="98bba-125">Luo opas Dynamics 365 Guides -PC:n ja HoloLens-sovellusten avulla.</span><span class="sxs-lookup"><span data-stu-id="98bba-125">Create a guide by using the Dynamics 365 Guides PC and HoloLens apps.</span></span> <span data-ttu-id="98bba-126">Lisätietoja kunkin oppaan luomisesta on seuraavissa ohjeaiheissa.</span><span class="sxs-lookup"><span data-stu-id="98bba-126">For information about how to create a guide, see the following topics:</span></span>

    - [<span data-ttu-id="98bba-127">Oppaan luominen PC-sovelluksen avulla</span><span class="sxs-lookup"><span data-stu-id="98bba-127">Use the PC app to create a guide</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/pc-app-overview)
    - [<span data-ttu-id="98bba-128">Aseta hologrammit HoloLens-sovelluksen avulla</span><span class="sxs-lookup"><span data-stu-id="98bba-128">Use the HoloLens app to place your holograms</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/hololens-app-overview)

1. <span data-ttu-id="98bba-129">Luo toimitusketjun hallinnassa [ylläpidon tarkistuslistamalli](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).</span><span class="sxs-lookup"><span data-stu-id="98bba-129">In Supply Chain Management, [create a maintenance checklist template](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).</span></span>
1. <span data-ttu-id="98bba-130">Liitä uusi ylläpidon tarkistuslistarivillä luomasi opas ylläpidon tarkistuslistamalliin:</span><span class="sxs-lookup"><span data-stu-id="98bba-130">Associate the guide that you created with a maintenance checklist line in the new maintenance checklist template:</span></span>

    1. <span data-ttu-id="98bba-131">Valitse **Ylläpidon tarkistuslistarivit** -pikavälilehdessä rivi, johon haluat liittää oppaan.</span><span class="sxs-lookup"><span data-stu-id="98bba-131">On the **Maintenance checklist lines** FastTab, select the line that you want to associate the guide with.</span></span>
    1. <span data-ttu-id="98bba-132">Valitse **Liittyvät Oppaat** -pikavälilehdessä **Lisää opas**.</span><span class="sxs-lookup"><span data-stu-id="98bba-132">On the **Associated guides** FastTab, select **Add Guide**.</span></span>

        <span data-ttu-id="98bba-133">![Oppaan ja ylläpidon tarkistuslistarivin kytkeminen](media/am-guides-integration-add-guide.png "Oppaan ja ylläpidon tarkistuslistarivin kytkeminen")</span><span class="sxs-lookup"><span data-stu-id="98bba-133">![Associate a guide with a maintenance checklist line](media/am-guides-integration-add-guide.png "Associate a guide with a maintenance checklist line")</span></span>

    1. <span data-ttu-id="98bba-134">Valitse **Nimi**-kentässä opas ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="98bba-134">In the **Name** field, select a guide, and then select **Save**.</span></span>

        <span data-ttu-id="98bba-135">![Valitse opas nimikentästä](media/am-guides-integration-select-guide.png "Valitse opas nimikentästä")</span><span class="sxs-lookup"><span data-stu-id="98bba-135">![Select a guide in the Name field](media/am-guides-integration-select-guide.png "Select a guide in the Name field")</span></span>

1. <span data-ttu-id="98bba-136">Työtyypin ja ylläpidon tarkistuslistamallin kytkeminen:</span><span class="sxs-lookup"><span data-stu-id="98bba-136">Associate the maintenance checklist template with a job type:</span></span>

    1. <span data-ttu-id="98bba-137">[Luo ylläpitotöiden tyyppi](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type) tai valitse aiemmin luotu ylläpitotyön tyyppi.</span><span class="sxs-lookup"><span data-stu-id="98bba-137">[Create a maintenance job type](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type), or select an existing maintenance job type.</span></span>
    1. <span data-ttu-id="98bba-138">Valitse toimintoruudun **Ylläpitotöiden tyypin oletusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="98bba-138">On the Action Pane, select **Maintenance job type defaults**.</span></span>

        <span data-ttu-id="98bba-139">![Ylläpitotyön tyyppien oletusten painike](media/am-guides-integration-job-defaults.png "Ylläpitotyön tyyppien oletusten painike")</span><span class="sxs-lookup"><span data-stu-id="98bba-139">![Maintenance job type defaults button](media/am-guides-integration-job-defaults.png "Maintenance job type defaults button")</span></span>

    1. <span data-ttu-id="98bba-140">Luo rivi ja valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="98bba-140">Create a line, and then select **Save**.</span></span>

        <span data-ttu-id="98bba-141">![Luo rivi](media/am-guides-integration-add-line.png "Luo rivi")</span><span class="sxs-lookup"><span data-stu-id="98bba-141">![Create a line](media/am-guides-integration-add-line.png "Create a line")</span></span>

    1. <span data-ttu-id="98bba-142">Valitse toimintoruudussa **Ylläpidon tarkistuslista**.</span><span class="sxs-lookup"><span data-stu-id="98bba-142">On the Action Pane, select **Maintenance checklist**.</span></span>

        <span data-ttu-id="98bba-143">![Ylläpidon tarkistuslistapainike](media/am-guides-integration-maintenance-checklist.png "Ylläpidon tarkistuslistapainike")</span><span class="sxs-lookup"><span data-stu-id="98bba-143">![Maintenance checklist button](media/am-guides-integration-maintenance-checklist.png "Maintenance checklist button")</span></span>

    1. <span data-ttu-id="98bba-144">Lisää **ylläpidon tarkistuslistarivit** -pikavälilehdessä rivi ja muuta sitten **Tyyppi**-kentän arvoksi **Malli**.</span><span class="sxs-lookup"><span data-stu-id="98bba-144">On the **Maintenance checklist lines** FastTab, add a line, and then change the value of the **Type** field to **Template**.</span></span>

        <span data-ttu-id="98bba-145">![Muuta tyypin arvo](media/am-guides-integration-checklist-lines.png "Muuta tyypin arvo")</span><span class="sxs-lookup"><span data-stu-id="98bba-145">![Change the Type value](media/am-guides-integration-checklist-lines.png "Change the Type value")</span></span>

    1. <span data-ttu-id="98bba-146">Valitse **Rivitiedot**-pikavälilehden **Malli**-kentässä malli, johon opas on liitetty, ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="98bba-146">On the **Line details** FastTab, in the **Template** field, select the template that you associated the guide with, and then select **Save**.</span></span>

        <span data-ttu-id="98bba-147">![Valitse malli](media/am-guides-integration-checklist-line-details.png "Valitse malli")</span><span class="sxs-lookup"><span data-stu-id="98bba-147">![Select the template](media/am-guides-integration-checklist-line-details.png "Select the template")</span></span>

1. <span data-ttu-id="98bba-148">[Luo työtilaus](work-orders/manually-created-workorders.md#create-work-order) ja valitse sitten ylläpitotyön tyyppi, joka käyttää oppaaseen liitettyä ylläpidon tarkistuslistamallia.</span><span class="sxs-lookup"><span data-stu-id="98bba-148">[Create a work order](work-orders/manually-created-workorders.md#create-work-order), and then select the maintenance job type that uses the maintenance checklist template that you associated the guide with.</span></span> <span data-ttu-id="98bba-149">Opas liitetään automaattisesti työtilaukseen.</span><span class="sxs-lookup"><span data-stu-id="98bba-149">The guide is automatically associated with the work order.</span></span>

    <span data-ttu-id="98bba-150">![Valitse ylläpitotyön tyyppi](media/am-guides-integration-create-work-order.png "Valitse ylläpitotyön tyyppi")</span><span class="sxs-lookup"><span data-stu-id="98bba-150">![Select a maintenance job type](media/am-guides-integration-create-work-order.png "Select a maintenance job type")</span></span>

1. <span data-ttu-id="98bba-151">Näytä työtilaukseen ja työntekijöihin liittyvä opas:</span><span class="sxs-lookup"><span data-stu-id="98bba-151">View the guide that is associated with the work order and workers:</span></span>

    1. <span data-ttu-id="98bba-152">Avaa [resurssinhallinnan mobiilityötila](asset-management-mobile-workspace.md), jotta voit käyttää työtilausta.</span><span class="sxs-lookup"><span data-stu-id="98bba-152">Open the [Asset management mobile workspace](asset-management-mobile-workspace.md) to access the work order.</span></span>
    1. <span data-ttu-id="98bba-153">[Avaa työtilauksen ylläpidon tarkistuslista](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job).</span><span class="sxs-lookup"><span data-stu-id="98bba-153">[Open the maintenance checklist](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) for the work order.</span></span>
    1. <span data-ttu-id="98bba-154">Valitse tarkistuslistarivi tarkastellaksesi liittyvää opasta.</span><span class="sxs-lookup"><span data-stu-id="98bba-154">Select a checklist line to see the associated guide.</span></span>

        <span data-ttu-id="98bba-155">![Tarkistuslistariviin liittyvä opas](media/am-guides-integration-show-guide.png "Tarkistuslistariviin liittyvä opas")</span><span class="sxs-lookup"><span data-stu-id="98bba-155">![Guide associated with a checklist line](media/am-guides-integration-show-guide.png "Guide associated with a checklist line")</span></span>

    1. <span data-ttu-id="98bba-156">Avaa HoloLens-tehtäväopas.</span><span class="sxs-lookup"><span data-stu-id="98bba-156">Open the guide on HoloLens.</span></span>

        <span data-ttu-id="98bba-157">![Avaa HoloLens-tehtäväopas](media/am-guides-integration-hololens-select.png "Avaa HoloLens-tehtäväopas")</span><span class="sxs-lookup"><span data-stu-id="98bba-157">![Open the guide on HoloLens](media/am-guides-integration-hololens-select.png "Open the guide on HoloLens")</span></span>

> [!NOTE]
> <span data-ttu-id="98bba-158">Voit liittää oppaan myös suoraan työtilauksen tai työlajin ylläpidon tarkistuslistaan.</span><span class="sxs-lookup"><span data-stu-id="98bba-158">You can also associate a guide directly in the maintenance checklist of a work order or a job type.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="98bba-159">On tunnettu ongelma, että kun liität ylläpidon tarkistuslistamallin ja oletusylläpitotyötyypin, malliin linkitetty opas ei näy **ylläpitotyötyypin oletukset**-sivun **liitetyt oppaat**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="98bba-159">There is a known issue where, when you associate a maintenance checklist template with a default maintenance job type, the guide that is linked to the template doesn't appear on the **Associated guides** FastTab of the **Maintenance job type defaults** page.</span></span> <span data-ttu-id="98bba-160">Opas tulee kuitenkin näkyviin sen jälkeen, kun työlajia käytetään **Liittyvät oppaat** -pikavälilehden työtilaukseen.</span><span class="sxs-lookup"><span data-stu-id="98bba-160">However, the guide will appear after that job type is applied to a work order on the **Associated guides** FastTab.</span></span>

## <a name="see-also"></a><span data-ttu-id="98bba-161">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="98bba-161">See also</span></span>

- [<span data-ttu-id="98bba-162">Kaksoiskirjoituksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="98bba-162">Dual-write overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [<span data-ttu-id="98bba-163">Resurssien hallinnan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="98bba-163">Asset management overview</span></span>](index.md)
