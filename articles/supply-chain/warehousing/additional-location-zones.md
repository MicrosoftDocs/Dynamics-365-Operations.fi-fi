---
title: Sijainnin lisävyöhykkeet
description: Tässä aiheessa annetaan yleiskatsaus uusista sijainnin vyöhykkeistä, jotka on lisätty Microsoft Dynamics 365 Supply Chain Management -järjestelmään.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 6cf81939989b8faffcda51bbbd5bc6b27aec7eea
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016303"
---
# <a name="additional-location-zones"></a><span data-ttu-id="b4ffe-103">Sijainnin lisävyöhykkeet</span><span class="sxs-lookup"><span data-stu-id="b4ffe-103">Additional location zones</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4ffe-104">Kolme uutta vyöhykekenttää on saatavilla Microsoft Dynamics 365 Supply Chain Management -järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="b4ffe-104">Three new zone fields are available in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="b4ffe-105">Varaston esimiehet voivat käyttää niitä apuna varaston uusien järjestelyjen ja asettelujen määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="b4ffe-105">Warehouse managers can use them to define additional warehouse organizations or layouts.</span></span> <span data-ttu-id="b4ffe-106">Uudet vyöhykekentät voidaan asettaa manuaalisesti tai ohjatun **Sijaintien asetus** -toiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="b4ffe-106">The new zone fields can be set either manually or by using the **Location setup** wizard.</span></span> <span data-ttu-id="b4ffe-107">Niitä voidaan hyödyntää missä tahansa kyselyssä tai suodatuksessa, joka käyttää Sijainnit-taulukkoa.</span><span class="sxs-lookup"><span data-stu-id="b4ffe-107">They can be used in any query or filtering that uses the Locations table.</span></span>

<span data-ttu-id="b4ffe-108">Vyöhykekenttien käyttö ei vaadi lisäasetuksia.</span><span class="sxs-lookup"><span data-stu-id="b4ffe-108">No additional setup is required to use the zone fields.</span></span>

## <a name="turn-on-the-additional-location-zone-feature"></a><span data-ttu-id="b4ffe-109">Lisävyöhyketoiminnon käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="b4ffe-109">Turn on the Additional location zone feature</span></span>

<span data-ttu-id="b4ffe-110">Ennen kuin voit käyttää *Sijainnin lisävyöhyke* -toimintoa, sen pitää olla otettu käyttöön järjestelmässäsi.</span><span class="sxs-lookup"><span data-stu-id="b4ffe-110">Before you can use the *Additional location zone* feature, it must be turned on in your system.</span></span> <span data-ttu-id="b4ffe-111">Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön, jos sitä vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="b4ffe-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="b4ffe-112">**Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="b4ffe-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b4ffe-113">**Moduuli:** *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="b4ffe-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="b4ffe-114">**Toiminnon nimi:** *Sijainnin lisävyöhyke*</span><span class="sxs-lookup"><span data-stu-id="b4ffe-114">**Feature name:** *Additional location zone*</span></span>

## <a name="use-location-zones"></a><span data-ttu-id="b4ffe-115">Sijainnin vyöhykkeiden käyttäminen</span><span class="sxs-lookup"><span data-stu-id="b4ffe-115">Use location zones</span></span>

1. <span data-ttu-id="b4ffe-116">Siirry kohtaan **Varastonhallinta \> Asetukset \> Varasto \> Ohjattu sijaintien asetustoiminto**.</span><span class="sxs-lookup"><span data-stu-id="b4ffe-116">Go to **Warehouse management \> Setup \> Warehouse \> Location setup wizard**.</span></span>
2. <span data-ttu-id="b4ffe-117">Määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="b4ffe-117">Set the following values:</span></span>

    - <span data-ttu-id="b4ffe-118">Valitse **Varasto** -kentässä _62_.</span><span class="sxs-lookup"><span data-stu-id="b4ffe-118">In the **Warehouse** field, select _62_.</span></span>
    - <span data-ttu-id="b4ffe-119">Valitse **Vyöhyketunnus** -kentässä _KERROS_.</span><span class="sxs-lookup"><span data-stu-id="b4ffe-119">In the **Zone ID** field, select _FLOOR_.</span></span>
    - <span data-ttu-id="b4ffe-120">Valitse **Lisävyöhyke 1** -kentässä _VALITSEVYÖHYKE1_.</span><span class="sxs-lookup"><span data-stu-id="b4ffe-120">In the **Additional Zone 1** field, select _PICKZONE1_.</span></span>
    - <span data-ttu-id="b4ffe-121">Valitse **Lisävyöhyke 2** -kentässä _VERKKOKAUPPA1_.</span><span class="sxs-lookup"><span data-stu-id="b4ffe-121">In the **Additional Zone 2** field, select _WEBSHOP1_.</span></span>
    - <span data-ttu-id="b4ffe-122">Valitse **Sijainnin profiilitunnus** -kentässä _KERROS_.</span><span class="sxs-lookup"><span data-stu-id="b4ffe-122">In the **Location profile ID** field, select _FLOOR_.</span></span>

3. <span data-ttu-id="b4ffe-123">Valitse **Kerros** -niminen rivi.</span><span class="sxs-lookup"><span data-stu-id="b4ffe-123">Select the **Floor** line.</span></span>
4. <span data-ttu-id="b4ffe-124">Syötä **Ensimmäinen numero** -kenttään arvo _1_.</span><span class="sxs-lookup"><span data-stu-id="b4ffe-124">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="b4ffe-125">Syötä **Viimeinen numero** -kenttään arvo _3_.</span><span class="sxs-lookup"><span data-stu-id="b4ffe-125">In the **To number** field, enter _3_.</span></span>
5. <span data-ttu-id="b4ffe-126">Valitse **Käytävä** -niminen rivi.</span><span class="sxs-lookup"><span data-stu-id="b4ffe-126">Select the **Aisle** line.</span></span>
6. <span data-ttu-id="b4ffe-127">Syötä **Ensimmäinen numero** -kenttään arvo _1_.</span><span class="sxs-lookup"><span data-stu-id="b4ffe-127">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="b4ffe-128">Syötä **Viimeinen numero** -kenttään arvo _5_.</span><span class="sxs-lookup"><span data-stu-id="b4ffe-128">In the **To number** field, enter _5_.</span></span>
7. <span data-ttu-id="b4ffe-129">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="b4ffe-129">Select **Create**.</span></span>
8. <span data-ttu-id="b4ffe-130">Näyttöön tulee sanomia, joissa todetaan, että uusia sijainteja on lisätty.</span><span class="sxs-lookup"><span data-stu-id="b4ffe-130">You receive messages that state that new locations have been added.</span></span> <span data-ttu-id="b4ffe-131">Valitse **Näytä sanomat** -painike, jos haluat nähdä sanomat.</span><span class="sxs-lookup"><span data-stu-id="b4ffe-131">Select the **Show messages** button to view the messages.</span></span>
9. <span data-ttu-id="b4ffe-132">Valitse **Varastonhallinta \> Asetukset \> Varasto \> Sijainnit**.</span><span class="sxs-lookup"><span data-stu-id="b4ffe-132">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span> <span data-ttu-id="b4ffe-133">Uudet sijainnit näkyvät luettelossa, ja kaikki vyöhykekentät (aiemmin luotu vyöhykekenttä ja uudet lisävyöhykekentät) ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="b4ffe-133">The new locations appear in the list, and all zone fields are available (that is, the existing zone field and the new additional zone fields).</span></span>
