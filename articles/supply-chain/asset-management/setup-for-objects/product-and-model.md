---
title: Resurssien valmistajat ja mallit
description: Tässä ohje aiheessa kerrotaan, kuinka voit määrittää resurssin valmistajat ja niihin liittyvät mallit resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetProductLookup, EntAssetModelLookup, EntAssetProduct
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cec4f644af4a087464635d9a7ca825eb354747eb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259959"
---
# <a name="asset-manufacturers-and-models"></a><span data-ttu-id="232ce-103">Resurssien valmistajat ja mallit</span><span class="sxs-lookup"><span data-stu-id="232ce-103">Asset manufacturers and models</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="232ce-104">Tässä ohje aiheessa kerrotaan, kuinka voit määrittää resurssin valmistajat ja niihin liittyvät mallit resurssien hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="232ce-104">This topic explains how to set up asset manufacturers and related models in Asset Management.</span></span> <span data-ttu-id="232ce-105">Mallit voivat liittyä resurssityyppeihin.</span><span class="sxs-lookup"><span data-stu-id="232ce-105">Models can be related to asset types.</span></span>

## <a name="set-up-product-model-relations"></a><span data-ttu-id="232ce-106">Määritä tuote-malli-suhteet</span><span class="sxs-lookup"><span data-stu-id="232ce-106">Set up product-model relations</span></span>

1. <span data-ttu-id="232ce-107">Valitse **Resurssien hallinta**\>**Asetukset** \> **Resurssit** \> **valmistaja ja malli**. </span><span class="sxs-lookup"><span data-stu-id="232ce-107">Select **Asset management** \> **Setup** \> **Assets** \> **Manufacturer and model**.</span></span>
2. <span data-ttu-id="232ce-108">Luo uusi tuote valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="232ce-108">Select **New** to create a new product.</span></span>
3. <span data-ttu-id="232ce-109">Syötä **Valmistaja**-kenttään resurssin valmistajan nimi.</span><span class="sxs-lookup"><span data-stu-id="232ce-109">In the **Manufacturer** field, enter a name for the asset manufacturer.</span></span>
4. <span data-ttu-id="232ce-110">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="232ce-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="232ce-111">Valitse **Mallit**-pikavälilehdellä **Lisää** luodaksesi resurssimallin, joka liittyy resurssin valmistajaan.</span><span class="sxs-lookup"><span data-stu-id="232ce-111">On the **Models** FastTab, select **Add** to create an asset model that should be related to the asset manufacturer.</span></span>
6. <span data-ttu-id="232ce-112">Syötä **Malli**-kenttään resurssin mallin nimi.</span><span class="sxs-lookup"><span data-stu-id="232ce-112">In the **Model** field, enter a name for the asset model.</span></span>
7. <span data-ttu-id="232ce-113">Syötä **Kuvaus**-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="232ce-113">In the **Description** field, enter a description.</span></span>
8. <span data-ttu-id="232ce-114">Valitse **Resurssityyppi**-kentässä resurssityyppi, johon valmistajan mallin tulisi liittyä.</span><span class="sxs-lookup"><span data-stu-id="232ce-114">In the **Asset type** field, select the asset type that the manufacturer model should be related to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="232ce-115">Voit myös määrittää resurssityyppien, valmistajien ja mallien suhteet **Resurssityypit**-haussa.</span><span class="sxs-lookup"><span data-stu-id="232ce-115">You can also set up relations for asset types, manufacturers, and models in the **Asset types** lookup.</span></span> <span data-ttu-id="232ce-116">Lisätietoja on kohdassa [Resurssityypit](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="232ce-116">For more information, see [Asset types](../setup-for-objects/object-types.md).</span></span>

    <span data-ttu-id="232ce-117">**Tiedot**-pikavälilehdessä **Mallit**-kentässä näkyy valitulle resurssin valmistajalle asetettujen resurssin mallien määrä.</span><span class="sxs-lookup"><span data-stu-id="232ce-117">In the **Details** FastTab, the **Models** field shows the number of asset models that are set up on the selected asset manufacturer.</span></span> <span data-ttu-id="232ce-118">**Resurssit**-kenttä näyttää niiden resurssien määrän, jotka käyttävät valittua valmistajaa.</span><span class="sxs-lookup"><span data-stu-id="232ce-118">The **Assets** field shows the number of assets that are using the selected manufacturer.</span></span>
    
    <span data-ttu-id="232ce-119">**Resurssit**-kenttä näyttää niiden objektien määrän, jotka käyttävät valittua mallia.</span><span class="sxs-lookup"><span data-stu-id="232ce-119">The **Assets** field shows the number of objects that are using the manufacturer model.</span></span>

> [!NOTE]
> <span data-ttu-id="232ce-120">Resurssityypillä ei voi olla resurssin valmistajan mallin suhteita, se voi liittyä yhteen resurssin valmistajan malliin tai se voi liittyä useisiin resurssin valmistajan malleihin.</span><span class="sxs-lookup"><span data-stu-id="232ce-120">An asset type can have no asset manufacturer model relations, it can be related to one asset manufacturer model, or it can be related multiple asset manufacturer models.</span></span> <span data-ttu-id="232ce-121">Jos resurssin tyyppi liittyy vähintään yhteen valmistajan malliin, vain ne yhdistelmät, jotka on määritetty **Valmistajan malli** -haussa, voidaan valita kyseisillä resurssien hallintasivuilla, joilla resurssityypin, valmistajan ja mallin yhdistelmä voidaan määrittää.</span><span class="sxs-lookup"><span data-stu-id="232ce-121">If an asset type is related to at least one manufacturer model, only the combinations that are set up in the **Manufacturer model** lookup can be selected on those Asset Management pages where a combination of an asset type, manufacturer, and model can be set up.</span></span> <span data-ttu-id="232ce-122">Näitä sivuja ovat **Kaikki resurssit**, **Resurssien palvelutasot** **Oletustyötyypit** ja **Ylläpitobudjetin rivit**.</span><span class="sxs-lookup"><span data-stu-id="232ce-122">These pages include **All assets**, **Asset service levels**, **Job type defaults**, and **Maintenance budget lines**.</span></span> <span data-ttu-id="232ce-123">Jos jotkin resurssityypit eivät liity mihinkään valmistajan malliin, sivuilla näkyvät vain ne resurssityypit ja valmistajan mallit, joilla ei myöskään ole suhdetta resurssityyppeihin.</span><span class="sxs-lookup"><span data-stu-id="232ce-123">If some asset types aren't related to any manufacturer model, only those asset types, and manufacturer models that also have no relation to asset types, are shown on the pages.</span></span>

## <a name="select-a-manufacturer-and-model-on-an-object"></a><span data-ttu-id="232ce-124">Valitse objektin valmistaja ja malli</span><span class="sxs-lookup"><span data-stu-id="232ce-124">Select a manufacturer and model on an object</span></span>

1. <span data-ttu-id="232ce-125">Valitse **Resurssien hallinta** \> **Yhteiset** \> **Resurssit** \> **Kaikki resurssit**.</span><span class="sxs-lookup"><span data-stu-id="232ce-125">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="232ce-126">Valitse **Resurssi**-sarakkeessa resurssin linkki.</span><span class="sxs-lookup"><span data-stu-id="232ce-126">In the **Asset** column, select the link for the asset.</span></span> <span data-ttu-id="232ce-127">Näyttöön tulee **Tiedot** -sivu.</span><span class="sxs-lookup"><span data-stu-id="232ce-127">The **Details** page appears.</span></span>
3. <span data-ttu-id="232ce-128">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="232ce-128">Select **Edit**.</span></span>
4. <span data-ttu-id="232ce-129">Valitse **Yleiset**-pikavälilehdessä **valmistaja**- ja **Malli**-kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="232ce-129">On the **General** FastTab, select values in the **Manufacturer** and **Model** fields.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]