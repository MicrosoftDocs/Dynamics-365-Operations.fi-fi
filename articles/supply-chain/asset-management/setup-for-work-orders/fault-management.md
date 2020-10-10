---
title: Vikojen hallinta
description: Tässä ohjeaiheessa kerrotaan vikojen hallinnasta resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetFaultArea, EntAssetFaultDesigner, EntAssetFaultCopyFromObjectType, EntAssetFaultRemedy, EntAssetObjectFaultRelationRequestInfoPart, EntAssetObjectFaultRelationWorkOrderInfoPart, EntAssetFaultCreateCombinations, EntAssetObjectFaultSymptom, EntAssetObjectFaultSymptomListPage, EntAssetFaultType, EntAssetFaultSymptom, EntAssetFaultCause
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 72d6c8d750a5a0903017b4c77b3ce5d9521cf99b
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889358"
---
# <a name="fault-management"></a><span data-ttu-id="073e1-103">Vikojen hallinta</span><span class="sxs-lookup"><span data-stu-id="073e1-103">Fault management</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="073e1-104">Käyttöomaisuuden hallinnassa voit käyttää vian suunnittelua käyttöomaisuustyyppien vian oireiden, vika-alueiden ja vikatyyppien määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="073e1-104">In Asset Management, you can use the fault designer to set up fault symptoms, fault areas, and fault types on asset types.</span></span> <span data-ttu-id="073e1-105">Näin voit hallita käyttöomaisuudessa havaittuja virheitä.</span><span class="sxs-lookup"><span data-stu-id="073e1-105">In this way, you can manage faults that are detected on assets.</span></span> <span data-ttu-id="073e1-106">Lisäksi vian syyt ja virheiden korjausehdotukset voidaan kirjata työtilaukseen.</span><span class="sxs-lookup"><span data-stu-id="073e1-106">Additionally, fault causes and suggestions for fixing faults can be registered on a work order.</span></span>

<span data-ttu-id="073e1-107">Virheiden rekisteröintiä ja hallintaa koskeva prosessi koostuu näistä vaiheista.</span><span class="sxs-lookup"><span data-stu-id="073e1-107">The process for fault registration and management consists of these steps.</span></span>

1. <span data-ttu-id="073e1-108">Luo luettelo vikaoireista, vika-alueista ja vikatyypeistä, joita voi ilmetä käyttöomaisuustyypeissä.</span><span class="sxs-lookup"><span data-stu-id="073e1-108">Create a list of fault symptoms, fault areas, and fault types that might occur on your asset types.</span></span>
2. <span data-ttu-id="073e1-109">Määritä vian suunnittelussa oireet, vika-alueet ja vikatyypit.</span><span class="sxs-lookup"><span data-stu-id="073e1-109">In the fault designer, set up symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="073e1-110">Seuraavassa on joitakin esimerkkejä, joiden avulla voit ymmärtää vian oireiden, vika-alueiden ja vikatyyppien välisen eron.</span><span class="sxs-lookup"><span data-stu-id="073e1-110">Here are some examples to help you understand the difference between fault symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="073e1-111">**Vikojen oireet:**</span><span class="sxs-lookup"><span data-stu-id="073e1-111">**Fault symptoms:**</span></span>

- <span data-ttu-id="073e1-112">Epäsymmetriset jännitteet</span><span class="sxs-lookup"><span data-stu-id="073e1-112">Unbalanced voltages</span></span>
- <span data-ttu-id="073e1-113">Oikosulku</span><span class="sxs-lookup"><span data-stu-id="073e1-113">Short circuit</span></span>
- <span data-ttu-id="073e1-114">Melu</span><span class="sxs-lookup"><span data-stu-id="073e1-114">Noise</span></span>
- <span data-ttu-id="073e1-115">Vuoto</span><span class="sxs-lookup"><span data-stu-id="073e1-115">Leak</span></span>
- <span data-ttu-id="073e1-116">Tärinä</span><span class="sxs-lookup"><span data-stu-id="073e1-116">Vibrations</span></span>

<span data-ttu-id="073e1-117">**Vika-alueet:**</span><span class="sxs-lookup"><span data-stu-id="073e1-117">**Fault areas:**</span></span>

- <span data-ttu-id="073e1-118">Sähköinen</span><span class="sxs-lookup"><span data-stu-id="073e1-118">Electrical</span></span>
- <span data-ttu-id="073e1-119">Mekaaninen</span><span class="sxs-lookup"><span data-stu-id="073e1-119">Mechanical</span></span>
- <span data-ttu-id="073e1-120">Hydraulinen</span><span class="sxs-lookup"><span data-stu-id="073e1-120">Hydraulic</span></span>
- <span data-ttu-id="073e1-121">Pneumaattinen</span><span class="sxs-lookup"><span data-stu-id="073e1-121">Pneumatic</span></span>

<span data-ttu-id="073e1-122">**Vikatyypit:**</span><span class="sxs-lookup"><span data-stu-id="073e1-122">**Fault types:**</span></span>

- <span data-ttu-id="073e1-123">Viallinen päästaattorin käämitys</span><span class="sxs-lookup"><span data-stu-id="073e1-123">Faulty main stator winding</span></span>
- <span data-ttu-id="073e1-124">Viallinen diodi</span><span class="sxs-lookup"><span data-stu-id="073e1-124">Faulty diode</span></span>
- <span data-ttu-id="073e1-125">Likaiset käämit</span><span class="sxs-lookup"><span data-stu-id="073e1-125">Dirty windings</span></span>
- <span data-ttu-id="073e1-126">Viallinen generaattori</span><span class="sxs-lookup"><span data-stu-id="073e1-126">Defective generator</span></span>
- <span data-ttu-id="073e1-127">Viallinen anturi</span><span class="sxs-lookup"><span data-stu-id="073e1-127">Defective sensor</span></span>

## <a name="create-fault-symptoms"></a><span data-ttu-id="073e1-128">Vikojen oireiden luominen</span><span class="sxs-lookup"><span data-stu-id="073e1-128">Create fault symptoms</span></span>

<span data-ttu-id="073e1-129">Noudattamalla näitä ohjeita voit luoda luettelon oireista, joita voidaan käyttää vian suunnittelutoiminnossa.</span><span class="sxs-lookup"><span data-stu-id="073e1-129">Follow these steps to create a list of symptoms that can be used in the fault designer.</span></span>

1. <span data-ttu-id="073e1-130">Valitse **Resurssien hallinta** \> **Asetukset** \> **Vika** \> **Vikojen oireet**.</span><span class="sxs-lookup"><span data-stu-id="073e1-130">Select **Asset management** \> **Setup** \> **Fault** \> **Fault symptoms**.</span></span>
2. <span data-ttu-id="073e1-131">Luo tietue valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="073e1-131">Select **New** to create a record.</span></span>
3. <span data-ttu-id="073e1-132">Kirjoita **Vikojen oireet** -kenttään vian oireen nimi.</span><span class="sxs-lookup"><span data-stu-id="073e1-132">In the **Fault symptom** field, enter a name for the fault symptom.</span></span>
4. <span data-ttu-id="073e1-133">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="073e1-133">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="073e1-134">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="073e1-134">Select **Save**.</span></span>

## <a name="create-fault-areas"></a><span data-ttu-id="073e1-135">Vika-alueiden luominen</span><span class="sxs-lookup"><span data-stu-id="073e1-135">Create fault areas</span></span>

<span data-ttu-id="073e1-136">Noudattamalla näitä ohjeita voit luoda luettelon alueista tai sijainneista, joita voidaan käyttää vian suunnittelutoiminnossa.</span><span class="sxs-lookup"><span data-stu-id="073e1-136">Follow these steps to create a list of areas or locations that can be used in the fault designer.</span></span>

1. <span data-ttu-id="073e1-137">Valitse **Resurssien hallinta** \> **Asetukset** \> **Vika** \> **Vika-alueet**.</span><span class="sxs-lookup"><span data-stu-id="073e1-137">Select **Asset management** \> **Setup** \> **Fault** \> **Fault areas**.</span></span>
2. <span data-ttu-id="073e1-138">Luo tietue valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="073e1-138">Select **New** to create a record.</span></span>
3. <span data-ttu-id="073e1-139">Kirjoita **Vika-alue** -kenttään vika-alueen nimi.</span><span class="sxs-lookup"><span data-stu-id="073e1-139">In the **Fault area** field, enter a name for the fault area.</span></span>
4. <span data-ttu-id="073e1-140">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="073e1-140">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="073e1-141">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="073e1-141">Select **Save**.</span></span>

## <a name="create-fault-types"></a><span data-ttu-id="073e1-142">Luo vikatyypit</span><span class="sxs-lookup"><span data-stu-id="073e1-142">Create fault types</span></span>

<span data-ttu-id="073e1-143">Noudattamalla näitä ohjeita voit luoda luettelon vikatyypeistä, joita voidaan käyttää vian suunnittelutoiminnossa.</span><span class="sxs-lookup"><span data-stu-id="073e1-143">Follow these steps to create a list of fault types that can be used in the fault designer.</span></span>

1. <span data-ttu-id="073e1-144">Valitse **Resurssien hallinta** \> **Asetukset** \> **Vika** \> **Vikatyypit**.</span><span class="sxs-lookup"><span data-stu-id="073e1-144">Select **Asset management** \> **Setup** \> **Fault** \> **Fault types**.</span></span>
2. <span data-ttu-id="073e1-145">Luo tietue valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="073e1-145">Select **New** to create a record.</span></span>
3. <span data-ttu-id="073e1-146">Syötä **Vikatyyppi**-kenttään vikatyypin nimi.</span><span class="sxs-lookup"><span data-stu-id="073e1-146">In the **Fault type** field, enter a name for the fault type.</span></span>
4. <span data-ttu-id="073e1-147">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="073e1-147">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="073e1-148">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="073e1-148">Select **Save**.</span></span>

## <a name="set-up-the-fault-designer"></a><span data-ttu-id="073e1-149">Vian suunnittelutoiminnon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="073e1-149">Set up the fault designer</span></span>

<span data-ttu-id="073e1-150">Vian suunnittelussa määritetään käyttöomaisuustyyppien vikatiedot.</span><span class="sxs-lookup"><span data-stu-id="073e1-150">In the fault designer, you set up fault data on asset types.</span></span>

1. <span data-ttu-id="073e1-151">Valitse **Resurssien hallinta** \> **Asetukset** \> **Vika** \> **Vian suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="073e1-151">Select **Asset management** \> **Setup** \> **Fault** \> **Fault designer**.</span></span>
2. <span data-ttu-id="073e1-152">Valitse vasemmanpuoleisesta ruudusta käyttöomaisuustyyppi, jolle haluat määrittää vikatietueen.</span><span class="sxs-lookup"><span data-stu-id="073e1-152">In the left pane, select the type of asset to set up a fault record for.</span></span>
3. <span data-ttu-id="073e1-153">Valitse **Vian oire** -pikavälilehdessä **Lisää rivi** ja valitse sitten **Vian oire-** kentästä vian oire.</span><span class="sxs-lookup"><span data-stu-id="073e1-153">On the **Fault symptom** FastTab, select **Add line**, and then, in the **Fault symptom** field, select a fault symptom.</span></span>
4. <span data-ttu-id="073e1-154">Valitse **Vika-alue** -pikavälilehdessä **Lisää rivi** ja valitse sitten **Vika-alue** -kentästä vian oire.</span><span class="sxs-lookup"><span data-stu-id="073e1-154">On the **Fault area** FastTab, select **Add line**, and then, in the **Fault area** field select a fault area.</span></span>
5. <span data-ttu-id="073e1-155">Valitse **Vikatyyppi** -pikavälilehdessä **Lisää rivi** ja valitse sitten **Vikatyyppi** -kentästä vikatyyppi.</span><span class="sxs-lookup"><span data-stu-id="073e1-155">On the **Fault type** FastTab, select **Add line**, and then, in the **Fault type** field, select a fault type.</span></span>
6. <span data-ttu-id="073e1-156">Voit luoda nopeasti kaikkien aiemmin luotujen vian oireiden, vika-alueiden ja vikatyyppien yhdistelmiä valitun käyttöomaisuustyypin osalta valitsemalla **Luo vikayhdistelmät**.</span><span class="sxs-lookup"><span data-stu-id="073e1-156">To quickly create combinations of all existing fault symptoms, areas, and types for the selected asset type, select **Create fault combinations**.</span></span> <span data-ttu-id="073e1-157">Tämä toiminto on hyödyllinen, jos olet lisännyt useita vian oireita, vika-alueita ja vikatyyppejä.</span><span class="sxs-lookup"><span data-stu-id="073e1-157">This function is useful if you've added many fault symptoms, areas, and types.</span></span> <span data-ttu-id="073e1-158">On helpompaa poistaa niiden yhdistelmien rivit, jotka eivät liity käyttöomaisuuslajiin, kuin luoda uusia rivejä manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="073e1-158">It's easier to delete the lines for any combinations that aren't relevant to the asset type than to create new lines manually.</span></span>

    > [!NOTE]
    > <span data-ttu-id="073e1-159">Jos haluat kopioida vian oireiden, -alueiden ja -tyyppien määritykset yhdestä käyttöomaisuuslajista valittuun käyttöomaisuustyyppiin, valitse **Kopioi resurssityypistä**.</span><span class="sxs-lookup"><span data-stu-id="073e1-159">To copy the setup of fault symptoms, areas, and types from one asset type to the selected asset type, select **Copy from asset type**.</span></span>

7. <span data-ttu-id="073e1-160">Tallenna muutokset valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="073e1-160">Select **Save** to save your changes.</span></span>

![Vian suunnittelutoimintosivu](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a><span data-ttu-id="073e1-162">Luo vian syyt</span><span class="sxs-lookup"><span data-stu-id="073e1-162">Create fault causes</span></span>

<span data-ttu-id="073e1-163">Seuraavien vaiheiden avulla voit luoda luettelon tunnetuista vikojen syistä, jotka voidaan lisätä työtilaukseen tai ylläpitopyyntöön.</span><span class="sxs-lookup"><span data-stu-id="073e1-163">Follow these steps to create a list of known fault causes that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="073e1-164">Valitse **Resurssien hallinta** \> **Asetukset** \> **Vika** \> **Vian syyt**.</span><span class="sxs-lookup"><span data-stu-id="073e1-164">Select **Asset management** \> **Setup** \> **Fault** \> **Fault causes**.</span></span>
2. <span data-ttu-id="073e1-165">Luo tietue valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="073e1-165">Select **New** to create a record.</span></span>
3. <span data-ttu-id="073e1-166">Syötä **Vian syy**-kenttään vian syyn nimi.</span><span class="sxs-lookup"><span data-stu-id="073e1-166">In the **Fault cause** field, enter a name for the fault cause.</span></span>
4. <span data-ttu-id="073e1-167">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="073e1-167">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="073e1-168">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="073e1-168">Select **Save**.</span></span>

## <a name="create-fault-remedies"></a><span data-ttu-id="073e1-169">Vian korjaustoimenpiteiden luominen</span><span class="sxs-lookup"><span data-stu-id="073e1-169">Create fault remedies</span></span>

<span data-ttu-id="073e1-170">Seuraavien vaiheiden avulla voit luoda luettelon korjausehdotuksista, jotka voidaan lisätä työtilaukseen tai ylläpitopyyntöön.</span><span class="sxs-lookup"><span data-stu-id="073e1-170">Follow these steps to create a list of suggestions for remedy and repair that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="073e1-171">Valitse **Resurssien hallinta** \> **Asetukset** \> **Vika** \> **Vian korjaukset**.</span><span class="sxs-lookup"><span data-stu-id="073e1-171">Select **Asset management** \> **Setup** \> **Fault** \> **Fault remedies**.</span></span>
2. <span data-ttu-id="073e1-172">Luo tietue valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="073e1-172">Select **New** to create a record.</span></span>
3. <span data-ttu-id="073e1-173">Kirjoita **Vian korjaus** -kenttään vian korjauksen nimi.</span><span class="sxs-lookup"><span data-stu-id="073e1-173">In the **Fault remedy** field, enter a name for the fault remedy.</span></span>
4. <span data-ttu-id="073e1-174">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="073e1-174">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="073e1-175">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="073e1-175">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="073e1-176">Voit muuttaa vian oireiden, alueiden, tyyppien, syiden ja korjaustoimenpiteiden nimiä tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="073e1-176">You can change the names of your fault symptoms, areas, types, causes, and remedies as you require.</span></span> <span data-ttu-id="073e1-177">Nimen muutokset näkyvät automaattisesti liittyvissä vikarekisteröinneissä.</span><span class="sxs-lookup"><span data-stu-id="073e1-177">The name changes are automatically reflected in the related fault registrations.</span></span>
