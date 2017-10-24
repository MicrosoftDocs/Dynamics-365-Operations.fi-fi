---
title: "Vähittäismyyntihierarkiat"
description: "Tässä artikkelissa käsitellään Microsoft Dynamics 365 for Retailin vähittäismyyntihierarkioita."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 817696566473bc5f31a7ff11c04291351dfd4764
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="retail-hierarchies"></a><span data-ttu-id="03f32-103">Vähittäismyyntihierarkiat</span><span class="sxs-lookup"><span data-stu-id="03f32-103">Retail hierarchies</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="03f32-104">Tässä artikkelissa käsitellään Microsoft Dynamics 365 for Retailin vähittäismyyntihierarkioita.</span><span class="sxs-lookup"><span data-stu-id="03f32-104">This article describes retail hierarchies in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="03f32-105">Voit luoda vähittäismyyntiluokan hierarkian, jonka avulla voit järjestää vähittäismyyntikanavissa myymiäsi tuotteita.</span><span class="sxs-lookup"><span data-stu-id="03f32-105">You can create a retail category hierarchy to organize the products that you sell through your retail channels.</span></span> <span data-ttu-id="03f32-106">Vähittäismyynnin tuotehierarkioiden avulla voit luokitella tai ryhmitellä tuotteita.</span><span class="sxs-lookup"><span data-stu-id="03f32-106">You can use retail product hierarchies to categorize or group products.</span></span> <span data-ttu-id="03f32-107">Tuotteiden avulla voit luoda edelleen tuotevalikoimia ja asiakkaiden kanta-asiakasohjelmia.</span><span class="sxs-lookup"><span data-stu-id="03f32-107">You can then use these products to create product assortments and customer loyalty programs.</span></span> <span data-ttu-id="03f32-108">Voit myös määrittää tuotteiden määritteitä ja ominaisuuksia sekä hinnoittelurakenteen, sisällyttää tuotteita kampanjoihin ja käyttää niitä raportoinnissa.</span><span class="sxs-lookup"><span data-stu-id="03f32-108">You can also assign product attributes and properties, assign a pricing structure, include the products in product promotions, and use the products for reporting.</span></span> <span data-ttu-id="03f32-109">Voit luoda yhden vähittäismyynnin luokkahierarkian edustamaan kaikkia organisaatiosi tuotteita ja luokkia ja käyttää sitten tätä luokkahierarkiaa useisiin tarkoituksiin.</span><span class="sxs-lookup"><span data-stu-id="03f32-109">You can create one retail category hierarchy to represent all the products and categories in your organization, and then use that category hierarchy for multiple purposes.</span></span> <span data-ttu-id="03f32-110">Voit myös vaihtoehtoisesti luoda useita vähittäismyynnin luokkahierarkioita erikoistarkoituksiin, kuten tuotekampanjoihin.</span><span class="sxs-lookup"><span data-stu-id="03f32-110">Alternatively, you can create multiple retail category hierarchies for special purposes, such as product promotions.</span></span> <span data-ttu-id="03f32-111">Vähittäismyynnin tuotehierarkiaa luotaessa on määritettävä luokkahierarkian tarkoituksen määrittävä luokkahierarkian tyyppi.</span><span class="sxs-lookup"><span data-stu-id="03f32-111">When you create a retail product hierarchy, you must assign a category hierarchy type to identify the purpose of the category hierarchy.</span></span> <span data-ttu-id="03f32-112">Esimerkiksi kun tuotteita selataan luokittain verkossa tai myyntipisteissä, viittaukset koskevat vain tuotehierarkioita, joiden tyypiksi on määritetty **Vähittäismyynnin siirtymishierarkia**.</span><span class="sxs-lookup"><span data-stu-id="03f32-112">For example, only product hierarchies that are assigned the **Retail navigation hierarchy** type are referenced when you browse products by category online or in point of sale (POS).</span></span>

## <a name="retail-hierarchy-types"></a><span data-ttu-id="03f32-113">Vähittäismyyntihierarkian tyypit</span><span class="sxs-lookup"><span data-stu-id="03f32-113">Retail hierarchy types</span></span>
<span data-ttu-id="03f32-114">Seuraavassa taulukossa on kuvattu käytettävissä olevia vähittäismyynnin luokkahierarkioiden tyyppejä ja niiden tarkoitusta.</span><span class="sxs-lookup"><span data-stu-id="03f32-114">The following table lists the types of retail category hierarchies that are available and the general purpose of each type.</span></span>

| <span data-ttu-id="03f32-115">Luokkahierarkian tyyppi</span><span class="sxs-lookup"><span data-stu-id="03f32-115">Category hierarchy type</span></span>       | <span data-ttu-id="03f32-116">Tarkoitus</span><span class="sxs-lookup"><span data-stu-id="03f32-116">Purpose</span></span>                                                                                                                                                                                                                                                                                                            |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03f32-117">Vähittäismyynnin tuotehierarkia</span><span class="sxs-lookup"><span data-stu-id="03f32-117">Retail product hierarchy</span></span>      | <span data-ttu-id="03f32-118">Valitse tämä hierarkiatyyppi, jos haluat määrittää organisaatiollesi yleisen tuotehierarkian.</span><span class="sxs-lookup"><span data-stu-id="03f32-118">Use this hierarchy type to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="03f32-119">Tätä hierarkiatyyppiä voi käyttää markkinoinnissa, hinnoittelussa ja kampanjoissa, raportoinnissa sekä valikoiman suunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="03f32-119">You can use this hierarchy type for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="03f32-120">Vain yksi vähittäismyynnin tuotehierarkia voidaan määrittää tälle hierarkiatyypille.</span><span class="sxs-lookup"><span data-stu-id="03f32-120">Only one retail product hierarchy can be assigned this hierarchy type.</span></span>                                       |
| <span data-ttu-id="03f32-121">Vähittäismyynnin lisähierarkia</span><span class="sxs-lookup"><span data-stu-id="03f32-121">Supplemental retail hierarchy</span></span> | <span data-ttu-id="03f32-122">Tätä hierarkiatyyppiä voi käyttää muissa luotavissa vähittäismyynnin luokkahierarkioissa.</span><span class="sxs-lookup"><span data-stu-id="03f32-122">Use this hierarchy type for any additional retail category hierarchies that you want to create.</span></span> <span data-ttu-id="03f32-123">Esimerkiksi keväisin järjestetään usein uimapukukampanjoita.</span><span class="sxs-lookup"><span data-stu-id="03f32-123">For example, in the spring, you have a promotion for swimwear.</span></span> <span data-ttu-id="03f32-124">Liitä silloin uima-asutuotteet erilliseen luokkahierarkiaan ja käytä kampanjahinnoittelua eri tuoteluokkiin.</span><span class="sxs-lookup"><span data-stu-id="03f32-124">Therefore, you include your swimwear products in a separate category hierarchy and apply the promotional pricing to the various product categories.</span></span> |
| <span data-ttu-id="03f32-125">Vähittäismyynnin siirtymishierarkia</span><span class="sxs-lookup"><span data-stu-id="03f32-125">Retail navigation hierarchy</span></span>   | <span data-ttu-id="03f32-126">Tämän hierarkiatyypin avulla voit ryhmitellä ja järjestää tuotteita luokiksi niin, että niitä voidaan selata verkossa tai myyntipisteessä.</span><span class="sxs-lookup"><span data-stu-id="03f32-126">Use this hierarchy type to group and organize products into categories so that the products can be browsed online or in POS.</span></span>                                                                                                                                                                                       |

<span data-ttu-id="03f32-127">Jäsentelemällä tuotteita vähittäismyynnin luokkahierarkian avulla voit määrittää ja ylläpitää tuotemääritteitä ja -ominaisuuksia luokkatasolla.</span><span class="sxs-lookup"><span data-stu-id="03f32-127">By using a retail category hierarchy to structure your products, you can set up and maintain product attributes and properties at the category level.</span></span> <span data-ttu-id="03f32-128">Nämä määritteet ja ominaisuudet sisältävät tuotedimensioiden asetukset sekä myyntipisteasetukset.</span><span class="sxs-lookup"><span data-stu-id="03f32-128">These attributes and properties include settings for product dimensions and POS settings.</span></span> <span data-ttu-id="03f32-129">Luokkiin määritettävät tuotteet perivät määrittämäsi määritteet ja ominaisuudet automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="03f32-129">Any products that you assign to the categories automatically inherit the attributes and properties that you define.</span></span> <span data-ttu-id="03f32-130">Voit myös kopioida minkä tahansa tuotteen ominaisuusasetukset useisiin valitun luokan tuotteisiin samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="03f32-130">You can also copy the property settings for any product to multiple products in a selected category at the same time.</span></span>




