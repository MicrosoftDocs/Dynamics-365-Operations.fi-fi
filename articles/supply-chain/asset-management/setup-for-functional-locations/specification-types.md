---
title: Ylläpidon määritetyypit
description: Tässä ohjeaiheessa kerrotaan, kuinka määritetyypit luodaan resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationTypeCopy, EntAssetAttributeType, EntAssetAttributeTypeValue, EntAssetFunctionalLocationType
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b93c2ab284d5746f4ecd48cd8b8ffe59aea9f90
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217242"
---
# <a name="maintenance-attribute-types"></a><span data-ttu-id="7cdf0-103">Ylläpidon määritetyypit</span><span class="sxs-lookup"><span data-stu-id="7cdf0-103">Maintenance attribute types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="7cdf0-104">Tässä ohjeaiheessa kerrotaan, kuinka määritetyypit luodaan resurssien hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-104">This topic explains how to create attribute types in Asset Management.</span></span> <span data-ttu-id="7cdf0-105">Määritteiden avulla kuvataan eri elementtien ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-105">Attributes are used to describe the properties of various elements.</span></span> <span data-ttu-id="7cdf0-106">Voit määrittää määritteitä seuraaville elementeille:</span><span class="sxs-lookup"><span data-stu-id="7cdf0-106">You can set up attributes on the following elements:</span></span>

- [<span data-ttu-id="7cdf0-107">Toiminnalliset sijaintityypit</span><span class="sxs-lookup"><span data-stu-id="7cdf0-107">Functional location types</span></span>](../setup-for-functional-locations/functional-location-types.md)
- [<span data-ttu-id="7cdf0-108">Luo toiminnalliset sijainnit</span><span class="sxs-lookup"><span data-stu-id="7cdf0-108">Create functional locations</span></span>](../functional-locations/create-functional-locations.md)
- [<span data-ttu-id="7cdf0-109">Resurssityypit</span><span class="sxs-lookup"><span data-stu-id="7cdf0-109">Asset types</span></span>](../setup-for-objects/object-types.md)
- <span data-ttu-id="7cdf0-110">Resurssit</span><span class="sxs-lookup"><span data-stu-id="7cdf0-110">Assets</span></span>

<span data-ttu-id="7cdf0-111">Määritteet, jotka voit määrittää, vaihtelevat elementin mukaan.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-111">The attributes that you can set up vary, depending on the element.</span></span> <span data-ttu-id="7cdf0-112">Jos kyseessä on esimerkiksi toiminnallinen sijainti, voit määrittää sijainnin määrityksen ja sijainnin fyysisen koon määritteet.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-112">For example, for a functional location, you can set up attributes for the configuration and physical size of the location.</span></span> <span data-ttu-id="7cdf0-113">Voit määrittää resurssityypille tai resurssille määritteitä moottorin tilavuuteen, virrankulutukseen ja enimmäiskuormauskapasiteettiin eri olosuhteissa.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-113">For an asset type or an asset, you can set up attributes for engine volume, power consumption, and maximum load capacity under different conditions.</span></span>

## <a name="create-attribute-types"></a><span data-ttu-id="7cdf0-114">Luo ominaisuustyypit</span><span class="sxs-lookup"><span data-stu-id="7cdf0-114">Create attribute types</span></span>

<span data-ttu-id="7cdf0-115">Voit luoda omia määritetyyppejä.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-115">You can create your own attribute types.</span></span> <span data-ttu-id="7cdf0-116">Lisäksi voit siirtää tuotedimensiot **Määritetyypit**-sivulle.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-116">Additionally, you can transfer product dimensions to the **Attribute types** page.</span></span>

1. <span data-ttu-id="7cdf0-117">Valitse **Resurssien hallinta** \> **Asetukset** \> **Määritetyypit**.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-117">Select **Asset management** \> **Setup** \> **Attribute types**.</span></span>
2. <span data-ttu-id="7cdf0-118">Kun määrität määritetyyppejä ensimmäistä kertaa, valitse **Luo tuotedimensiot** siirtääksesi vakiotuotedimensiot automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-118">The first time that you set up attribute types, select **Create product dimensions** to automatically transfer standard product dimensions.</span></span>
3. <span data-ttu-id="7cdf0-119">Luo uusi määritetyyppi valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-119">Select **New** to create a new attribute type.</span></span>
4. <span data-ttu-id="7cdf0-120">Kirjoita **Määritetyyppi**-kenttään määritetyypin nimi.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-120">In the **Attribute type** field, enter a name for the attribute type.</span></span>
5. <span data-ttu-id="7cdf0-121">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-121">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="7cdf0-122">Valitse **Yksikkö**-kentässä asianmukainen määriteyksikkö tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-122">In the **Unit** field, select the relevant attribute unit, as required.</span></span>
7. <span data-ttu-id="7cdf0-123">Valitse **Tietotyyppi**-kentässä yksikön tietotyyppi.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-123">In the **Data type** field, select a data type for the unit.</span></span>
8. <span data-ttu-id="7cdf0-124">Jos olet valinnut tietotyypiksi **Merkkijono**, luo määritetyypille arvot noudattamalla seuraavia vaiheita:</span><span class="sxs-lookup"><span data-stu-id="7cdf0-124">If you selected **String** as the data type, follow these steps to create values for the attribute type:</span></span>

    1. <span data-ttu-id="7cdf0-125">Valitse määritetyyppi ja valitse sitten **Arvot**.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-125">Select the attribute type, and then select **Values**.</span></span>
    2. <span data-ttu-id="7cdf0-126">Valitse **Määritteen arvot**-kentässä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-126">In the **Attribute values** field, select **New**.</span></span>
    3. <span data-ttu-id="7cdf0-127">Valitse määritteen tyyppi (dimensio) **Määritteen tyyppi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-127">In the **Attribute type** field, select an attribute type (dimension).</span></span>
    4. <span data-ttu-id="7cdf0-128">Syötä liittyvä arvo **Arvo**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-128">In the **Value** field, enter a related value.</span></span>
    5. <span data-ttu-id="7cdf0-129">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-129">In the **Description** field, enter a description.</span></span>
    6. <span data-ttu-id="7cdf0-130">Tallenna tietue.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-130">Save the record.</span></span>
    7. <span data-ttu-id="7cdf0-131">Palaa **Määritetyypit** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-131">Return to the **Attribute types** page.</span></span>

9. <span data-ttu-id="7cdf0-132">Tallenna tietue.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-132">Save the record.</span></span>

    <span data-ttu-id="7cdf0-133">**Toiminnallisten sijaintien tyypit** -kentässä näkyy niiden toiminnallisten sijaintien määrä, jotka käyttävät määritetyyppiä.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-133">The **Functional location types** field shows the number of functional locations that are using the attribute type.</span></span> <span data-ttu-id="7cdf0-134">**Resurssityypit**-kentässä näkyy sitä käyttävien resurssityyppien määrä.</span><span class="sxs-lookup"><span data-stu-id="7cdf0-134">The **Asset types** field shows the number of asset types that are using it.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]