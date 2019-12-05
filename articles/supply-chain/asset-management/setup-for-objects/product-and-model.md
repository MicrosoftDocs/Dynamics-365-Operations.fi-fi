---
title: Resurssien valmistajat ja mallit
description: Tässä ohje aiheessa kerrotaan, kuinka voit määrittää resurssin valmistajat ja niihin liittyvät mallit resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b77605070387871335c480e25cbe23af1155d6e8
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812165"
---
# <a name="asset-manufacturers-and-models"></a><span data-ttu-id="5e886-103">Resurssien valmistajat ja mallit</span><span class="sxs-lookup"><span data-stu-id="5e886-103">Asset manufacturers and models</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="5e886-104">Tässä ohje aiheessa kerrotaan, kuinka voit määrittää resurssin valmistajat ja niihin liittyvät mallit resurssien hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="5e886-104">This topic explains how to set up asset manufacturers and related models in Asset Management.</span></span> <span data-ttu-id="5e886-105">Mallit voivat liittyä resurssityyppeihin.</span><span class="sxs-lookup"><span data-stu-id="5e886-105">Models can be related to asset types.</span></span>

## <a name="set-up-product-model-relations"></a><span data-ttu-id="5e886-106">Määritä tuote-malli-suhteet</span><span class="sxs-lookup"><span data-stu-id="5e886-106">Set up product-model relations</span></span>

1. <span data-ttu-id="5e886-107">Valitse **Resurssien hallinta**\>**Asetukset** \> **Resurssit** \> **valmistaja ja malli**. </span><span class="sxs-lookup"><span data-stu-id="5e886-107">Select **Asset management** \> **Setup** \> **Assets** \> **Manufacturer and model**.</span></span>
2. <span data-ttu-id="5e886-108">Luo uusi tuote valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="5e886-108">Select **New** to create a new product.</span></span>
3. <span data-ttu-id="5e886-109">Syötä **Valmistaja**-kenttään resurssin valmistajan nimi.</span><span class="sxs-lookup"><span data-stu-id="5e886-109">In the **Manufacturer** field, enter a name for the asset manufacturer.</span></span>
4. <span data-ttu-id="5e886-110">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="5e886-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="5e886-111">Valitse **Mallit**-pikavälilehdellä **Lisää** luodaksesi resurssimallin, joka liittyy resurssin valmistajaan.</span><span class="sxs-lookup"><span data-stu-id="5e886-111">On the **Models** FastTab, select **Add** to create an asset model that should be related to the asset manufacturer.</span></span>
6. <span data-ttu-id="5e886-112">Syötä **Malli**-kenttään resurssin mallin nimi.</span><span class="sxs-lookup"><span data-stu-id="5e886-112">In the **Model** field, enter a name for the asset model.</span></span>
7. <span data-ttu-id="5e886-113">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="5e886-113">In the **Description** field, enter a description.</span></span>
8. <span data-ttu-id="5e886-114">Valitse **Resurssityyppi**-kentässä resurssityyppi, johon valmistajan mallin tulisi liittyä.</span><span class="sxs-lookup"><span data-stu-id="5e886-114">In the **Asset type** field, select the asset type that the manufacturer model should be related to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5e886-115">Voit myös määrittää resurssityyppien, valmistajien ja mallien suhteet **Resurssityypit**-haussa.</span><span class="sxs-lookup"><span data-stu-id="5e886-115">You can also set up relations for asset types, manufacturers, and models in the **Asset types** lookup.</span></span> <span data-ttu-id="5e886-116">Lisätietoja on kohdassa [Resurssityypit](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="5e886-116">For more information, see [Asset types](../setup-for-objects/object-types.md).</span></span>

    <span data-ttu-id="5e886-117">**Tiedot**-pikavälilehdessä **Mallit**-kentässä näkyy valitulle resurssin valmistajalle asetettujen resurssin mallien määrä.</span><span class="sxs-lookup"><span data-stu-id="5e886-117">In the **Details** FastTab, the **Models** field shows the number of asset models that are set up on the selected asset manufacturer.</span></span> <span data-ttu-id="5e886-118">**Resurssit**-kenttä näyttää niiden resurssien määrän, jotka käyttävät valittua valmistajaa.</span><span class="sxs-lookup"><span data-stu-id="5e886-118">The **Assets** field shows the number of assets that are using the selected manufacturer.</span></span>
    
    <span data-ttu-id="5e886-119">**Resurssit**-kenttä näyttää niiden objektien määrän, jotka käyttävät valittua mallia.</span><span class="sxs-lookup"><span data-stu-id="5e886-119">The **Assets** field shows the number of objects that are using the manufacturer model.</span></span>

> [!NOTE]
> <span data-ttu-id="5e886-120">Resurssityypillä ei voi olla resurssin valmistajan mallin suhteita, se voi liittyä yhteen resurssin valmistajan malliin tai se voi liittyä useisiin resurssin valmistajan malleihin.</span><span class="sxs-lookup"><span data-stu-id="5e886-120">An asset type can have no asset manufacturer model relations, it can be related to one asset manufacturer model, or it can be related multiple asset manufacturer models.</span></span> <span data-ttu-id="5e886-121">Jos resurssin tyyppi liittyy vähintään yhteen valmistajan malliin, vain ne yhdistelmät, jotka on määritetty **Valmistajan malli** -haussa, voidaan valita kyseisillä resurssien hallintasivuilla, joilla resurssityypin, valmistajan ja mallin yhdistelmä voidaan määrittää.</span><span class="sxs-lookup"><span data-stu-id="5e886-121">If an asset type is related to at least one manufacturer model, only the combinations that are set up in the **Manufacturer model** lookup can be selected on those Asset Management pages where a combination of an asset type, manufacturer, and model can be set up.</span></span> <span data-ttu-id="5e886-122">Näitä sivuja ovat **Kaikki resurssit**, **Resurssien palvelutasot** **Oletustyötyypit** ja **Ylläpitobudjetin rivit**.</span><span class="sxs-lookup"><span data-stu-id="5e886-122">These pages include **All assets**, **Asset service levels**, **Job type defaults**, and **Maintenance budget lines**.</span></span> <span data-ttu-id="5e886-123">Jos jotkin resurssityypit eivät liity mihinkään valmistajan malliin, sivuilla näkyvät vain ne resurssityypit ja valmistajan mallit, joilla ei myöskään ole suhdetta resurssityyppeihin.</span><span class="sxs-lookup"><span data-stu-id="5e886-123">If some asset types aren't related to any manufacturer model, only those asset types, and manufacturer models that also have no relation to asset types, are shown on the pages.</span></span>

## <a name="select-a-manufacturer-and-model-on-an-object"></a><span data-ttu-id="5e886-124">Valitse objektin valmistaja ja malli</span><span class="sxs-lookup"><span data-stu-id="5e886-124">Select a manufacturer and model on an object</span></span>

1. <span data-ttu-id="5e886-125">Valitse **Resurssien hallinta** \> **Yhteiset** \> **Resurssit** \> **Kaikki resurssit**.</span><span class="sxs-lookup"><span data-stu-id="5e886-125">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="5e886-126">Valitse **Resurssi**-sarakkeessa resurssin linkki.</span><span class="sxs-lookup"><span data-stu-id="5e886-126">In the **Asset** column, select the link for the asset.</span></span> <span data-ttu-id="5e886-127">Näyttöön tulee **Tiedot** -sivu.</span><span class="sxs-lookup"><span data-stu-id="5e886-127">The **Details** page appears.</span></span>
3. <span data-ttu-id="5e886-128">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="5e886-128">Select **Edit**.</span></span>
4. <span data-ttu-id="5e886-129">Valitse **Yleiset**-pikavälilehdessä **valmistaja**- ja **Malli**-kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="5e886-129">On the **General** FastTab, select values in the **Manufacturer** and **Model** fields.</span></span>
