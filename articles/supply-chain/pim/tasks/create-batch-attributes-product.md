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
ms.openlocfilehash: b61c91de926509f657074797030cbc3a1d1ed446
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147891"
---
# <a name="create-batch-attributes-for-a-product"></a><span data-ttu-id="6f293-103">Luo tuotteen erämääritteet</span><span class="sxs-lookup"><span data-stu-id="6f293-103">Create batch attributes for a product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6f293-104">Tässä menettelyssä kerrotaan, miten erämäärite luodaan, oletusarvoväli määritetään ja määrite lisätään ryhmään.</span><span class="sxs-lookup"><span data-stu-id="6f293-104">This procedure shows how to create a batch attribute, assign default value ranges, and include the attribute in a group.</span></span> <span data-ttu-id="6f293-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USP2.</span><span class="sxs-lookup"><span data-stu-id="6f293-105">The demo data company used to create this procedure is the USP2 Company.</span></span>

1. <span data-ttu-id="6f293-106">Siirry kohtaan Varastonhallinta > Asetukset > Erä > Erämääritteet.</span><span class="sxs-lookup"><span data-stu-id="6f293-106">Go to Inventory management > Setup > Batch > Batch attributes.</span></span>
2. <span data-ttu-id="6f293-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="6f293-107">Click New.</span></span>
3. <span data-ttu-id="6f293-108">Kirjoita arvo Määrite-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6f293-108">In the Attribute field, type a value.</span></span>
4. <span data-ttu-id="6f293-109">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6f293-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6f293-110">Valitse Määritetyyppi-kentässä Murtoluku.</span><span class="sxs-lookup"><span data-stu-id="6f293-110">In the Attribute type field, select 'Fraction'.</span></span>
    * <span data-ttu-id="6f293-111">Tässä menettelyssä desimaaliarvot otetaan käyttöön murtolukulajin avulla.</span><span class="sxs-lookup"><span data-stu-id="6f293-111">This procedure uses the Fraction type to enable decimal values.</span></span> <span data-ttu-id="6f293-112">Voit valita muita määritetyyppejä.</span><span class="sxs-lookup"><span data-stu-id="6f293-112">You can select other attribute types.</span></span> <span data-ttu-id="6f293-113">Jos valitset luettelointityypin, luetteloon on syötettävä arvot, ennen kuin syötät arvon Kohde-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6f293-113">If you select the Enumeration type, you must enter values in the enumeration list before you can enter a value in the Target field.</span></span>  
6. <span data-ttu-id="6f293-114">Syötä Vähintään-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="6f293-114">In the Minimum field, enter a number.</span></span>
7. <span data-ttu-id="6f293-115">Syötä Enintään-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="6f293-115">In the Maximum field, enter a number.</span></span>
8. <span data-ttu-id="6f293-116">Syötä Lisäys-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="6f293-116">In the Increment field, enter a number.</span></span>
9. <span data-ttu-id="6f293-117">Syötä Kohde-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="6f293-117">In the Target field, type a value.</span></span>
10. <span data-ttu-id="6f293-118">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="6f293-118">Click Save.</span></span>
11. <span data-ttu-id="6f293-119">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6f293-119">Close the page.</span></span>
12. <span data-ttu-id="6f293-120">Siirry kohtaan Varastonhallinta > Asetukset > Erä > Erämääriteryhmät.</span><span class="sxs-lookup"><span data-stu-id="6f293-120">Go to Inventory management > Setup > Batch > Batch attribute groups.</span></span>
13. <span data-ttu-id="6f293-121">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="6f293-121">Click New.</span></span>
14. <span data-ttu-id="6f293-122">Kirjoita arvo Määriteryhmä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6f293-122">In the Attribute group field, type a value.</span></span>
15. <span data-ttu-id="6f293-123">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6f293-123">In the Description field, type a value.</span></span>
16. <span data-ttu-id="6f293-124">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="6f293-124">Click Save.</span></span>
17. <span data-ttu-id="6f293-125">Valitse Ryhmämääritteet.</span><span class="sxs-lookup"><span data-stu-id="6f293-125">Click Group attributes.</span></span>
18. <span data-ttu-id="6f293-126">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="6f293-126">Click New.</span></span>
19. <span data-ttu-id="6f293-127">Avaa haku valitsemalla Määrite-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="6f293-127">In the Attribute field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="6f293-128">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="6f293-128">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="6f293-129">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="6f293-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6f293-130">Määrite voi kuulua mihin tahansa ryhmään.</span><span class="sxs-lookup"><span data-stu-id="6f293-130">An attribute can be included in any of the groups.</span></span>  
22. <span data-ttu-id="6f293-131">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="6f293-131">Click Save.</span></span>
23. <span data-ttu-id="6f293-132">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6f293-132">Close the page.</span></span>

