---
title: Määrityksistä poikkeamisia koskevat karanteenivyöhykkeet
description: Tässä aiheessa kuvataan, kuinka voit luoda ja käyttää karanteenivyöhykkeitä määrityksistä poikkeamisille.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93ca74ec4586fffa3b9156aadab887629283b98a
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956643"
---
# <a name="quarantine-zones-for-nonconformances"></a><span data-ttu-id="b9599-103">Määrityksistä poikkeamisia koskevat karanteenivyöhykkeet</span><span class="sxs-lookup"><span data-stu-id="b9599-103">Quarantine zones for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9599-104">Tässä aiheessa kuvataan, kuinka voit luoda ja käyttää karanteenivyöhykkeitä määrityksistä poikkeamisille.</span><span class="sxs-lookup"><span data-stu-id="b9599-104">This topic describes how to create and use quarantine zones for nonconformances.</span></span>

<span data-ttu-id="b9599-105">Määritä **Karanteenivyöhykkeet**-sivulla vyöhykkeet, jotka voidaan liittää määrityksistä poikkeamiseen.</span><span class="sxs-lookup"><span data-stu-id="b9599-105">You use the **Quarantine zones** page to define zones that can be assigned to nonconformances.</span></span> <span data-ttu-id="b9599-106">Kun luot määrityksistä poikkeamisen, voit määrittää **Karanteenivyöhyke**- ja **Karanteenityyppi**-kentät **Yleinen**-välilehdellä **Määrityksistä poikkeamisen** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="b9599-106">When you create a nonconformance, you can set the **Quarantine zone** and **Quarantine type** fields on the **General** tab of the **Non conformances** page.</span></span> <span data-ttu-id="b9599-107">**Karanteenivyöhyke**-kentässä näkyy yleensä alue tai sijainti, jossa nimike sijaitsee.</span><span class="sxs-lookup"><span data-stu-id="b9599-107">The **Quarantine zone** field typically indicates the area or location where the item is located.</span></span> <span data-ttu-id="b9599-108">**Karanteenityyppi**-kentässä nimike määritetään joko arvolla *Rajoitettu käyttö* tai *Käyttökelvoton*.</span><span class="sxs-lookup"><span data-stu-id="b9599-108">The **Quarantine type** field defines the item as either *Restricted usage* or *Unusable*.</span></span>

<span data-ttu-id="b9599-109">Kun tulostat määrityksistä poikkeamisen tai korjausraportin määrityksistä poikkeamiselle, voit tarkastella karanteenivyöhykettä, jolla nimike sijaitsee.</span><span class="sxs-lookup"><span data-stu-id="b9599-109">When you print a nonconformance or corrections report for a nonconformance, you can view the quarantine zone where the item is located.</span></span>

<span data-ttu-id="b9599-110">Voit myös tulostaa määrityksistä poikkeamisen tunnisteen määrityksistä poikkeamiselle.</span><span class="sxs-lookup"><span data-stu-id="b9599-110">You can also print a nonconformance tag for a nonconformance.</span></span> <span data-ttu-id="b9599-111">Tässä raportissa näkyy määritetty karanteenivyöhyke ja käyttötiedot, jotka ohjaavat viallisen materiaalin käsittelyssä.</span><span class="sxs-lookup"><span data-stu-id="b9599-111">This report shows the assigned quarantine zone and information about usage to provide guidance about how defective material should be handled.</span></span> <span data-ttu-id="b9599-112">Karanteenivyöhykkeet voivat vastata varastopaikkoja tai operatiivisia resursseja.</span><span class="sxs-lookup"><span data-stu-id="b9599-112">The quarantine zones might correspond to inventory locations or operations resources.</span></span>

## <a name="examples-of-quarantine-zones"></a><span data-ttu-id="b9599-113">Esimerkkejä karanteenivyöhykkeistä</span><span class="sxs-lookup"><span data-stu-id="b9599-113">Examples of quarantine zones</span></span>

### <a name="example-1"></a><span data-ttu-id="b9599-114">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="b9599-114">Example 1</span></span>

<span data-ttu-id="b9599-115">Työskentelet elektroniikan valmistusyhtiössä, joka tuottaa ja jakelee televisioita, kaiuttimia ja mediasoittimia.</span><span class="sxs-lookup"><span data-stu-id="b9599-115">You work at an electronics manufacturing company that produces and distributes televisions, speakers, and media players.</span></span> <span data-ttu-id="b9599-116">Tässä tapauksessa voit määrittää karanteenivyöhykkeen niin, että se vastaa kutakin tuotetyyppiä.</span><span class="sxs-lookup"><span data-stu-id="b9599-116">In this case, you can configure a quarantine zone to represent each type of product.</span></span>

### <a name="example-2"></a><span data-ttu-id="b9599-117">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="b9599-117">Example 2</span></span>

<span data-ttu-id="b9599-118">Kolmea lokeroa ja kahta hyllykköä käytetään määrityksistä poikkeavien nimikkeiden varastoimiseen.</span><span class="sxs-lookup"><span data-stu-id="b9599-118">Three bins and two racks are used to store items that are nonconforming.</span></span> <span data-ttu-id="b9599-119">Tässä tapauksessa voit määrittää viisi karanteenivyöhykettä, yhden kullekin lokerolle ja kullekin hyllykölle.</span><span class="sxs-lookup"><span data-stu-id="b9599-119">In this case, you can configure five quarantine zones, one for each bin and each rack.</span></span>

## <a name="create-a-quarantine-zone"></a><span data-ttu-id="b9599-120">Luo karanteenivyöhyke</span><span class="sxs-lookup"><span data-stu-id="b9599-120">Create a quarantine zone</span></span>

1. <span data-ttu-id="b9599-121">Valitse **Varastonhallinta \> Asetukset \> Laadunhallinta \> Karanteenivyöhykkeet**.</span><span class="sxs-lookup"><span data-stu-id="b9599-121">Go to **Inventory management \> Setup \> Quality management \> Quarantine zones**.</span></span>
1. <span data-ttu-id="b9599-122">Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b9599-122">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="b9599-123">Määritä sitten uudelle rivillä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="b9599-123">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="b9599-124">**Karanteenivyöhyke** – Syötä karanteenivyöhykkeen yksilöivä tunnus tai nimi.</span><span class="sxs-lookup"><span data-stu-id="b9599-124">**Quarantine zone** – Enter a unique ID or name for the quarantine zone.</span></span>
    - <span data-ttu-id="b9599-125">**Kuvaus** – Anna karanteenivyöhykkeen yksityiskohtainen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="b9599-125">**Description** – Enter a detailed description of the quarantine zone.</span></span>

1. <span data-ttu-id="b9599-126">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b9599-126">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b9599-127">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b9599-127">Additional resources</span></span>

- [<span data-ttu-id="b9599-128">Laadunhallinnan yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="b9599-128">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="b9599-129">Laadun ja määrityksistä poikkeamisen hallinnan ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="b9599-129">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="b9599-130">Määrityksistä poikkeamisia hyväksyvät työntekijät</span><span class="sxs-lookup"><span data-stu-id="b9599-130">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="b9599-131">Määrityksistä poikkeamisten ongelmatyypit</span><span class="sxs-lookup"><span data-stu-id="b9599-131">Problem types for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="b9599-132">Määrityksistä poikkeamisten diagnostiikkatyypit</span><span class="sxs-lookup"><span data-stu-id="b9599-132">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="b9599-133">Määrityksistä poikkeamisten laatukulut</span><span class="sxs-lookup"><span data-stu-id="b9599-133">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="b9599-134">Toiminnot määrityksistä poikkeamisille</span><span class="sxs-lookup"><span data-stu-id="b9599-134">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="b9599-135">Laadunhallinta varastoprosesseja varten</span><span class="sxs-lookup"><span data-stu-id="b9599-135">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
