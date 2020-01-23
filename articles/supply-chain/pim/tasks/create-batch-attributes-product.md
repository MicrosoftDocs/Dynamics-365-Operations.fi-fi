---
title: Luo tuotteen erämääritteet
description: Tässä menettelyssä kerrotaan, miten erämäärite luodaan, oletusarvoväli määritetään ja määrite lisätään ryhmään.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsBatchAttrib
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d874b6b6e53164c00d9b4656d27b1060f4e3ba06
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934932"
---
# <a name="create-batch-attributes-for-a-product"></a><span data-ttu-id="93231-103">Luo tuotteen erämääritteet</span><span class="sxs-lookup"><span data-stu-id="93231-103">Create batch attributes for a product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="93231-104">Tässä menettelyssä kerrotaan, miten erämäärite luodaan, oletusarvoväli määritetään ja määrite lisätään ryhmään.</span><span class="sxs-lookup"><span data-stu-id="93231-104">This procedure shows how to create a batch attribute, assign default value ranges, and include the attribute in a group.</span></span> <span data-ttu-id="93231-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USP2.</span><span class="sxs-lookup"><span data-stu-id="93231-105">The demo data company used to create this procedure is the USP2 Company.</span></span>

1. <span data-ttu-id="93231-106">Siirry kohtaan Varastonhallinta > Asetukset > Erä > Erämääritteet.</span><span class="sxs-lookup"><span data-stu-id="93231-106">Go to Inventory management > Setup > Batch > Batch attributes.</span></span>
2. <span data-ttu-id="93231-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="93231-107">Click New.</span></span>
3. <span data-ttu-id="93231-108">Kirjoita arvo Määrite-kenttään.</span><span class="sxs-lookup"><span data-stu-id="93231-108">In the Attribute field, type a value.</span></span>
4. <span data-ttu-id="93231-109">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="93231-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="93231-110">Valitse Määritetyyppi-kentässä Murtoluku.</span><span class="sxs-lookup"><span data-stu-id="93231-110">In the Attribute type field, select 'Fraction'.</span></span>
    * <span data-ttu-id="93231-111">Tässä menettelyssä desimaaliarvot otetaan käyttöön murtolukulajin avulla.</span><span class="sxs-lookup"><span data-stu-id="93231-111">This procedure uses the Fraction type to enable decimal values.</span></span> <span data-ttu-id="93231-112">Voit valita muita määritetyyppejä.</span><span class="sxs-lookup"><span data-stu-id="93231-112">You can select other attribute types.</span></span> <span data-ttu-id="93231-113">Jos valitset luettelointityypin, luetteloon on syötettävä arvot, ennen kuin syötät arvon Kohde-kenttään.</span><span class="sxs-lookup"><span data-stu-id="93231-113">If you select the Enumeration type, you must enter values in the enumeration list before you can enter a value in the Target field.</span></span>  
6. <span data-ttu-id="93231-114">Syötä Vähintään-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="93231-114">In the Minimum field, enter a number.</span></span>
7. <span data-ttu-id="93231-115">Syötä Enintään-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="93231-115">In the Maximum field, enter a number.</span></span>
8. <span data-ttu-id="93231-116">Syötä Lisäys-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="93231-116">In the Increment field, enter a number.</span></span>
9. <span data-ttu-id="93231-117">Syötä Kohde-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="93231-117">In the Target field, type a value.</span></span>
10. <span data-ttu-id="93231-118">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="93231-118">Click Save.</span></span>
11. <span data-ttu-id="93231-119">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="93231-119">Close the page.</span></span>
12. <span data-ttu-id="93231-120">Siirry kohtaan Varastonhallinta > Asetukset > Erä > Erämääriteryhmät.</span><span class="sxs-lookup"><span data-stu-id="93231-120">Go to Inventory management > Setup > Batch > Batch attribute groups.</span></span>
13. <span data-ttu-id="93231-121">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="93231-121">Click New.</span></span>
14. <span data-ttu-id="93231-122">Kirjoita arvo Määriteryhmä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="93231-122">In the Attribute group field, type a value.</span></span>
15. <span data-ttu-id="93231-123">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="93231-123">In the Description field, type a value.</span></span>
16. <span data-ttu-id="93231-124">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="93231-124">Click Save.</span></span>
17. <span data-ttu-id="93231-125">Valitse Ryhmämääritteet.</span><span class="sxs-lookup"><span data-stu-id="93231-125">Click Group attributes.</span></span>
18. <span data-ttu-id="93231-126">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="93231-126">Click New.</span></span>
19. <span data-ttu-id="93231-127">Avaa haku valitsemalla Määrite-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="93231-127">In the Attribute field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="93231-128">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="93231-128">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="93231-129">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="93231-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="93231-130">Määrite voi kuulua mihin tahansa ryhmään.</span><span class="sxs-lookup"><span data-stu-id="93231-130">An attribute can be included in any of the groups.</span></span>  
22. <span data-ttu-id="93231-131">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="93231-131">Click Save.</span></span>
23. <span data-ttu-id="93231-132">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="93231-132">Close the page.</span></span>

