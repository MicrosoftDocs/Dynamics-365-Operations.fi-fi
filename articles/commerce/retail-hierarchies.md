---
title: Vähittäismyyntihierarkiat
description: Tässä artikkelissa käsitellään Dynamics 365 Commercein jälleenmyyntihierarkioita.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: OMHierarchyManager
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: cf8db2c828f99dfd4c220966e31894dcd6eda572
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022422"
---
# <a name="retail-hierarchies"></a><span data-ttu-id="6a067-103">Vähittäismyyntihierarkiat</span><span class="sxs-lookup"><span data-stu-id="6a067-103">Retail hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6a067-104">Tässä artikkelissa käsitellään Dynamics 365 Commercen hierarkioita.</span><span class="sxs-lookup"><span data-stu-id="6a067-104">This article describes hierarchies in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6a067-105">Voit luoda kategoriahierarkian kanavien kautta myymiesi tuotteiden organisoimiseksi.</span><span class="sxs-lookup"><span data-stu-id="6a067-105">You can create a category hierarchy to organize the products that you sell through your channels.</span></span> <span data-ttu-id="6a067-106">Tuotehierarkioiden avulla voit luokitella tai ryhmitellä tuotteita.</span><span class="sxs-lookup"><span data-stu-id="6a067-106">You can use product hierarchies to categorize or group products.</span></span> <span data-ttu-id="6a067-107">Tuotteiden avulla voit luoda edelleen tuotevalikoimia ja asiakkaiden kanta-asiakasohjelmia.</span><span class="sxs-lookup"><span data-stu-id="6a067-107">You can then use these products to create product assortments and customer loyalty programs.</span></span> <span data-ttu-id="6a067-108">Voit myös määrittää tuotteiden määritteitä ja ominaisuuksia sekä hinnoittelurakenteen, sisällyttää tuotteita kampanjoihin ja käyttää niitä raportoinnissa.</span><span class="sxs-lookup"><span data-stu-id="6a067-108">You can also assign product attributes and properties, assign a pricing structure, include the products in product promotions, and use the products for reporting.</span></span> <span data-ttu-id="6a067-109">Voit luoda yhden luokkahierarkian edustamaan kaikkia organisaatiosi tuotteita sekä luokkia ja käyttää sitten tätä luokkahierarkiaa useisiin tarkoituksiin.</span><span class="sxs-lookup"><span data-stu-id="6a067-109">You can create one category hierarchy to represent all the products and categories in your organization, and then use that category hierarchy for multiple purposes.</span></span> <span data-ttu-id="6a067-110">Voit myös vaihtoehtoisesti luoda useita luokkahierarkioita erikoistarkoituksiin, kuten tuotteiden myynninedistämiseen.</span><span class="sxs-lookup"><span data-stu-id="6a067-110">Alternatively, you can create multiple category hierarchies for special purposes, such as product promotions.</span></span> <span data-ttu-id="6a067-111">Tuotehierarkiaa luotaessa on määritettävä luokkahierarkian tarkoituksen määrittävä luokkahierarkian tyyppi.</span><span class="sxs-lookup"><span data-stu-id="6a067-111">When you create a product hierarchy, you must assign a category hierarchy type to identify the purpose of the category hierarchy.</span></span> <span data-ttu-id="6a067-112">Esimerkiksi kun tuotteita selataan luokittain verkossa tai myyntipisteissä, viittaukset koskevat vain tuotehierarkioita, joiden tyypiksi on määritetty **Kaupan siirtymishierarkia**.</span><span class="sxs-lookup"><span data-stu-id="6a067-112">For example, only product hierarchies that are assigned the **Commerce navigation hierarchy** type are referenced when you browse products by category online or in point of sale (POS).</span></span>

## <a name="hierarchy-types"></a><span data-ttu-id="6a067-113">Hierarkiatyypit</span><span class="sxs-lookup"><span data-stu-id="6a067-113">Hierarchy types</span></span>

<span data-ttu-id="6a067-114">Seuraavassa taulukossa on kuvattu käytettävissä olevia luokkahierarkioiden tyyppejä ja niiden tarkoitusta.</span><span class="sxs-lookup"><span data-stu-id="6a067-114">The following table lists the types of category hierarchies that are available and the general purpose of each type.</span></span>

| <span data-ttu-id="6a067-115">Luokkahierarkian tyyppi</span><span class="sxs-lookup"><span data-stu-id="6a067-115">Category hierarchy type</span></span>       | <span data-ttu-id="6a067-116">Tarkoitus</span><span class="sxs-lookup"><span data-stu-id="6a067-116">Purpose</span></span> |
|-------------------------------|---------|
| <span data-ttu-id="6a067-117">Tuotehierarkia</span><span class="sxs-lookup"><span data-stu-id="6a067-117">Product hierarchy</span></span>      | <span data-ttu-id="6a067-118">Valitse tämä hierarkiatyyppi, jos haluat määrittää organisaatiollesi yleisen tuotehierarkian.</span><span class="sxs-lookup"><span data-stu-id="6a067-118">Use this hierarchy type to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="6a067-119">Tätä hierarkiatyyppiä voi käyttää markkinoinnissa, hinnoittelussa ja kampanjoissa, raportoinnissa sekä valikoiman suunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="6a067-119">You can use this hierarchy type for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="6a067-120">Vain yksi tuotehierarkia voidaan määrittää tälle hierarkiatyypille.</span><span class="sxs-lookup"><span data-stu-id="6a067-120">Only one product hierarchy can be assigned this hierarchy type.</span></span> |
| <span data-ttu-id="6a067-121">Lisähierarkia</span><span class="sxs-lookup"><span data-stu-id="6a067-121">Supplemental hierarchy</span></span> | <span data-ttu-id="6a067-122">Tätä hierarkiatyyppiä voi käyttää muissa luotavissa luokkahierarkioissa.</span><span class="sxs-lookup"><span data-stu-id="6a067-122">Use this hierarchy type for any additional category hierarchies that you want to create.</span></span> <span data-ttu-id="6a067-123">Esimerkiksi keväisin järjestetään usein uimapukukampanjoita.</span><span class="sxs-lookup"><span data-stu-id="6a067-123">For example, in the spring, you have a promotion for swimwear.</span></span> <span data-ttu-id="6a067-124">Liitä silloin uima-asutuotteet erilliseen luokkahierarkiaan ja käytä kampanjahinnoittelua eri tuoteluokkiin.</span><span class="sxs-lookup"><span data-stu-id="6a067-124">Therefore, you include your swimwear products in a separate category hierarchy and apply the promotional pricing to the various product categories.</span></span> |
| <span data-ttu-id="6a067-125">Siirtymishierarkia</span><span class="sxs-lookup"><span data-stu-id="6a067-125">Navigation hierarchy</span></span>   | <span data-ttu-id="6a067-126">Tämän hierarkiatyypin avulla voit ryhmitellä ja järjestää tuotteita luokiksi niin, että niitä voidaan selata verkossa tai myyntipisteessä.</span><span class="sxs-lookup"><span data-stu-id="6a067-126">Use this hierarchy type to group and organize products into categories so that the products can be browsed online or in POS.</span></span> |

<span data-ttu-id="6a067-127">Jäsentelemällä tuotteita luokkahierarkian avulla voit määrittää ja ylläpitää tuotemääritteitä ja -ominaisuuksia luokkatasolla.</span><span class="sxs-lookup"><span data-stu-id="6a067-127">By using a category hierarchy to structure your products, you can set up and maintain product attributes and properties at the category level.</span></span> <span data-ttu-id="6a067-128">Nämä määritteet ja ominaisuudet sisältävät tuotedimensioiden asetukset sekä myyntipisteasetukset.</span><span class="sxs-lookup"><span data-stu-id="6a067-128">These attributes and properties include settings for product dimensions and POS settings.</span></span> <span data-ttu-id="6a067-129">Luokkiin määritettävät tuotteet perivät määrittämäsi määritteet ja ominaisuudet automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="6a067-129">Any products that you assign to the categories automatically inherit the attributes and properties that you define.</span></span> <span data-ttu-id="6a067-130">Voit myös kopioida minkä tahansa tuotteen ominaisuusasetukset useisiin valitun luokan tuotteisiin samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="6a067-130">You can also copy the property settings for any product to multiple products in a selected category at the same time.</span></span>
