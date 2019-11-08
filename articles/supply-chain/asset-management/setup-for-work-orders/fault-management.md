---
title: Vikojen hallinta
description: Tässä ohjeaiheessa kerrotaan vikojen hallinnasta resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 78c062f9982ca7b18fa00d60928089d09a5d552d
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570952"
---
# <a name="fault-management"></a><span data-ttu-id="445ee-103">Vikojen hallinta</span><span class="sxs-lookup"><span data-stu-id="445ee-103">Fault management</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="445ee-104">Käyttöomaisuuden hallinnassa voit käyttää vian suunnittelua käyttöomaisuustyyppien vian oireiden, vika-alueiden ja vikatyyppien määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="445ee-104">In Asset Management, you can use the fault designer to set up fault symptoms, fault areas, and fault types on asset types.</span></span> <span data-ttu-id="445ee-105">Näin voit hallita käyttöomaisuudessa havaittuja virheitä.</span><span class="sxs-lookup"><span data-stu-id="445ee-105">In this way, you can manage faults that are detected on assets.</span></span> <span data-ttu-id="445ee-106">Lisäksi vian syyt ja virheiden korjausehdotukset voidaan kirjata työtilaukseen.</span><span class="sxs-lookup"><span data-stu-id="445ee-106">Additionally, fault causes and suggestions for fixing faults can be registered on a work order.</span></span>

<span data-ttu-id="445ee-107">Virheiden rekisteröintiä ja hallintaa koskeva prosessi koostuu näistä vaiheista.</span><span class="sxs-lookup"><span data-stu-id="445ee-107">The process for fault registration and management consists of these steps.</span></span>

1. <span data-ttu-id="445ee-108">Luo luettelo vikaoireista, vika-alueista ja vikatyypeistä, joita voi ilmetä käyttöomaisuustyypeissä.</span><span class="sxs-lookup"><span data-stu-id="445ee-108">Create a list of fault symptoms, fault areas, and fault types that might occur on your asset types.</span></span>
2. <span data-ttu-id="445ee-109">Määritä vian suunnittelussa oireet, vika-alueet ja vikatyypit.</span><span class="sxs-lookup"><span data-stu-id="445ee-109">In the fault designer, set up symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="445ee-110">Seuraavassa on joitakin esimerkkejä, joiden avulla voit ymmärtää vian oireiden, vika-alueiden ja vikatyyppien välisen eron.</span><span class="sxs-lookup"><span data-stu-id="445ee-110">Here are some examples to help you understand the difference between fault symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="445ee-111">**Vikojen oireet:**</span><span class="sxs-lookup"><span data-stu-id="445ee-111">**Fault symptoms:**</span></span>

- <span data-ttu-id="445ee-112">Epäsymmetriset jännitteet</span><span class="sxs-lookup"><span data-stu-id="445ee-112">Unbalanced voltages</span></span>
- <span data-ttu-id="445ee-113">Oikosulku</span><span class="sxs-lookup"><span data-stu-id="445ee-113">Short circuit</span></span>
- <span data-ttu-id="445ee-114">Melu</span><span class="sxs-lookup"><span data-stu-id="445ee-114">Noise</span></span>
- <span data-ttu-id="445ee-115">Vuoto</span><span class="sxs-lookup"><span data-stu-id="445ee-115">Leak</span></span>
- <span data-ttu-id="445ee-116">Tärinä</span><span class="sxs-lookup"><span data-stu-id="445ee-116">Vibrations</span></span>

<span data-ttu-id="445ee-117">**Vika-alueet:**</span><span class="sxs-lookup"><span data-stu-id="445ee-117">**Fault areas:**</span></span>

- <span data-ttu-id="445ee-118">Sähköinen</span><span class="sxs-lookup"><span data-stu-id="445ee-118">Electrical</span></span>
- <span data-ttu-id="445ee-119">Mekaaninen</span><span class="sxs-lookup"><span data-stu-id="445ee-119">Mechanical</span></span>
- <span data-ttu-id="445ee-120">Hydraulinen</span><span class="sxs-lookup"><span data-stu-id="445ee-120">Hydraulic</span></span>
- <span data-ttu-id="445ee-121">Pneumaattinen</span><span class="sxs-lookup"><span data-stu-id="445ee-121">Pneumatic</span></span>

<span data-ttu-id="445ee-122">**Vikatyypit:**</span><span class="sxs-lookup"><span data-stu-id="445ee-122">**Fault types:**</span></span>

- <span data-ttu-id="445ee-123">Viallinen päästaattorin käämitys</span><span class="sxs-lookup"><span data-stu-id="445ee-123">Faulty main stator winding</span></span>
- <span data-ttu-id="445ee-124">Viallinen diodi</span><span class="sxs-lookup"><span data-stu-id="445ee-124">Faulty diode</span></span>
- <span data-ttu-id="445ee-125">Likaiset käämit</span><span class="sxs-lookup"><span data-stu-id="445ee-125">Dirty windings</span></span>
- <span data-ttu-id="445ee-126">Viallinen generaattori</span><span class="sxs-lookup"><span data-stu-id="445ee-126">Defective generator</span></span>
- <span data-ttu-id="445ee-127">Viallinen anturi</span><span class="sxs-lookup"><span data-stu-id="445ee-127">Defective sensor</span></span>

## <a name="create-fault-symptoms"></a><span data-ttu-id="445ee-128">Vikojen oireiden luominen</span><span class="sxs-lookup"><span data-stu-id="445ee-128">Create fault symptoms</span></span>

<span data-ttu-id="445ee-129">Noudattamalla näitä ohjeita voit luoda luettelon oireista, joita voidaan käyttää vian suunnittelutoiminnossa.</span><span class="sxs-lookup"><span data-stu-id="445ee-129">Follow these steps to create a list of symptoms that can be used in the fault designer.</span></span>

1. <span data-ttu-id="445ee-130">Valitse **Resurssien hallinta** \> **Asetukset** \> **Vika** \> **Vikojen oireet**.</span><span class="sxs-lookup"><span data-stu-id="445ee-130">Select **Asset management** \> **Setup** \> **Fault** \> **Fault symptoms**.</span></span>
2. <span data-ttu-id="445ee-131">Luo tietue valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="445ee-131">Select **New** to create a record.</span></span>
3. <span data-ttu-id="445ee-132">Kirjoita **Vikojen oireet** -kenttään vian oireen nimi.</span><span class="sxs-lookup"><span data-stu-id="445ee-132">In the **Fault symptom** field, enter a name for the fault symptom.</span></span>
4. <span data-ttu-id="445ee-133">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="445ee-133">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="445ee-134">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="445ee-134">Select **Save**.</span></span>

## <a name="create-fault-areas"></a><span data-ttu-id="445ee-135">Vika-alueiden luominen</span><span class="sxs-lookup"><span data-stu-id="445ee-135">Create fault areas</span></span>

<span data-ttu-id="445ee-136">Noudattamalla näitä ohjeita voit luoda luettelon alueista tai sijainneista, joita voidaan käyttää vian suunnittelutoiminnossa.</span><span class="sxs-lookup"><span data-stu-id="445ee-136">Follow these steps to create a list of areas or locations that can be used in the fault designer.</span></span>

1. <span data-ttu-id="445ee-137">Valitse **Resurssien hallinta** \> **Asetukset** \> **Vika** \> **Vika-alueet**.</span><span class="sxs-lookup"><span data-stu-id="445ee-137">Select **Asset management** \> **Setup** \> **Fault** \> **Fault areas**.</span></span>
2. <span data-ttu-id="445ee-138">Luo tietue valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="445ee-138">Select **New** to create a record.</span></span>
3. <span data-ttu-id="445ee-139">Kirjoita **Vika-alue** -kenttään vika-alueen nimi.</span><span class="sxs-lookup"><span data-stu-id="445ee-139">In the **Fault area** field, enter a name for the fault area.</span></span>
4. <span data-ttu-id="445ee-140">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="445ee-140">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="445ee-141">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="445ee-141">Select **Save**.</span></span>

## <a name="create-fault-types"></a><span data-ttu-id="445ee-142">Luo vikatyypit</span><span class="sxs-lookup"><span data-stu-id="445ee-142">Create fault types</span></span>

<span data-ttu-id="445ee-143">Noudattamalla näitä ohjeita voit luoda luettelon vikatyypeistä, joita voidaan käyttää vian suunnittelutoiminnossa.</span><span class="sxs-lookup"><span data-stu-id="445ee-143">Follow these steps to create a list of fault types that can be used in the fault designer.</span></span>

1. <span data-ttu-id="445ee-144">Valitse **Resurssien hallinta** \> **Asetukset** \> **Vika** \> **Vikatyypit**.</span><span class="sxs-lookup"><span data-stu-id="445ee-144">Select **Asset management** \> **Setup** \> **Fault** \> **Fault types**.</span></span>
2. <span data-ttu-id="445ee-145">Luo tietue valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="445ee-145">Select **New** to create a record.</span></span>
3. <span data-ttu-id="445ee-146">Syötä **Vikatyyppi**-kenttään vikatyypin nimi.</span><span class="sxs-lookup"><span data-stu-id="445ee-146">In the **Fault type** field, enter a name for the fault type.</span></span>
4. <span data-ttu-id="445ee-147">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="445ee-147">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="445ee-148">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="445ee-148">Select **Save**.</span></span>

## <a name="set-up-the-fault-designer"></a><span data-ttu-id="445ee-149">Vian suunnittelutoiminnon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="445ee-149">Set up the fault designer</span></span>

<span data-ttu-id="445ee-150">Vian suunnittelussa määritetään käyttöomaisuustyyppien vikatiedot.</span><span class="sxs-lookup"><span data-stu-id="445ee-150">In the fault designer, you set up fault data on asset types.</span></span>

1. <span data-ttu-id="445ee-151">Valitse **Resurssien hallinta** \> **Asetukset** \> **Vika** \> **Vian suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="445ee-151">Select **Asset management** \> **Setup** \> **Fault** \> **Fault designer**.</span></span>
2. <span data-ttu-id="445ee-152">Valitse vasemmanpuoleisesta ruudusta käyttöomaisuustyyppi, jolle haluat määrittää vikatietueen.</span><span class="sxs-lookup"><span data-stu-id="445ee-152">In the left pane, select the type of asset to set up a fault record for.</span></span>
3. <span data-ttu-id="445ee-153">Valitse **Vian oire** -pikavälilehdessä **Lisää rivi** ja valitse sitten **Vian oire-** kentästä vian oire.</span><span class="sxs-lookup"><span data-stu-id="445ee-153">On the **Fault symptom** FastTab, select **Add line**, and then, in the **Fault symptom** field, select a fault symptom.</span></span>
4. <span data-ttu-id="445ee-154">Valitse **Vika-alue** -pikavälilehdessä **Lisää rivi** ja valitse sitten **Vika-alue** -kentästä vian oire.</span><span class="sxs-lookup"><span data-stu-id="445ee-154">On the **Fault area** FastTab, select **Add line**, and then, in the **Fault area** field select a fault area.</span></span>
5. <span data-ttu-id="445ee-155">Valitse **Vikatyyppi** -pikavälilehdessä **Lisää rivi** ja valitse sitten **Vikatyyppi** -kentästä vikatyyppi.</span><span class="sxs-lookup"><span data-stu-id="445ee-155">On the **Fault type** FastTab, select **Add line**, and then, in the **Fault type** field, select a fault type.</span></span>
6. <span data-ttu-id="445ee-156">Voit luoda nopeasti kaikkien aiemmin luotujen vian oireiden, vika-alueiden ja vikatyyppien yhdistelmiä valitun käyttöomaisuustyypin osalta valitsemalla **Luo vikayhdistelmät**.</span><span class="sxs-lookup"><span data-stu-id="445ee-156">To quickly create combinations of all existing fault symptoms, areas, and types for the selected asset type, select **Create fault combinations**.</span></span> <span data-ttu-id="445ee-157">Tämä toiminto on hyödyllinen, jos olet lisännyt useita vian oireita, vika-alueita ja vikatyyppejä.</span><span class="sxs-lookup"><span data-stu-id="445ee-157">This function is useful if you've added many fault symptoms, areas, and types.</span></span> <span data-ttu-id="445ee-158">On helpompaa poistaa niiden yhdistelmien rivit, jotka eivät liity käyttöomaisuuslajiin, kuin luoda uusia rivejä manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="445ee-158">It's easier to delete the lines for any combinations that aren't relevant to the asset type than to create new lines manually.</span></span>

    > [!NOTE]
    > <span data-ttu-id="445ee-159">Jos haluat kopioida vian oireiden, -alueiden ja -tyyppien määritykset yhdestä käyttöomaisuuslajista valittuun käyttöomaisuustyyppiin, valitse **Kopioi resurssityypistä**.</span><span class="sxs-lookup"><span data-stu-id="445ee-159">To copy the setup of fault symptoms, areas, and types from one asset type to the selected asset type, select **Copy from asset type**.</span></span>

7. <span data-ttu-id="445ee-160">Tallenna muutokset valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="445ee-160">Select **Save** to save your changes.</span></span>

![Vian suunnittelutoimintosivu](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a><span data-ttu-id="445ee-162">Luo vian syyt</span><span class="sxs-lookup"><span data-stu-id="445ee-162">Create fault causes</span></span>

<span data-ttu-id="445ee-163">Seuraavien vaiheiden avulla voit luoda luettelon tunnetuista vikojen syistä, jotka voidaan lisätä työtilaukseen tai ylläpitopyyntöön.</span><span class="sxs-lookup"><span data-stu-id="445ee-163">Follow these steps to create a list of known fault causes that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="445ee-164">Valitse **Resurssien hallinta** \> **Asetukset** \> **Vika** \> **Vian syyt**.</span><span class="sxs-lookup"><span data-stu-id="445ee-164">Select **Asset management** \> **Setup** \> **Fault** \> **Fault causes**.</span></span>
2. <span data-ttu-id="445ee-165">Luo tietue valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="445ee-165">Select **New** to create a record.</span></span>
3. <span data-ttu-id="445ee-166">Syötä **Vian syy**-kenttään vian syyn nimi.</span><span class="sxs-lookup"><span data-stu-id="445ee-166">In the **Fault cause** field, enter a name for the fault cause.</span></span>
4. <span data-ttu-id="445ee-167">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="445ee-167">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="445ee-168">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="445ee-168">Select **Save**.</span></span>

## <a name="create-fault-remedies"></a><span data-ttu-id="445ee-169">Vian korjaustoimenpiteiden luominen</span><span class="sxs-lookup"><span data-stu-id="445ee-169">Create fault remedies</span></span>

<span data-ttu-id="445ee-170">Seuraavien vaiheiden avulla voit luoda luettelon korjausehdotuksista, jotka voidaan lisätä työtilaukseen tai ylläpitopyyntöön.</span><span class="sxs-lookup"><span data-stu-id="445ee-170">Follow these steps to create a list of suggestions for remedy and repair that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="445ee-171">Valitse **Resurssien hallinta** \> **Asetukset** \> **Vika** \> **Vian korjaukset**.</span><span class="sxs-lookup"><span data-stu-id="445ee-171">Select **Asset management** \> **Setup** \> **Fault** \> **Fault remedies**.</span></span>
2. <span data-ttu-id="445ee-172">Luo tietue valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="445ee-172">Select **New** to create a record.</span></span>
3. <span data-ttu-id="445ee-173">Kirjoita **Vian korjaus** -kenttään vian korjauksen nimi.</span><span class="sxs-lookup"><span data-stu-id="445ee-173">In the **Fault remedy** field, enter a name for the fault remedy.</span></span>
4. <span data-ttu-id="445ee-174">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="445ee-174">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="445ee-175">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="445ee-175">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="445ee-176">Voit muuttaa vian oireiden, alueiden, tyyppien, syiden ja korjaustoimenpiteiden nimiä tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="445ee-176">You can change the names of your fault symptoms, areas, types, causes, and remedies as you require.</span></span> <span data-ttu-id="445ee-177">Nimen muutokset näkyvät automaattisesti liittyvissä vikarekisteröinneissä.</span><span class="sxs-lookup"><span data-stu-id="445ee-177">The name changes are automatically reflected in the related fault registrations.</span></span>
