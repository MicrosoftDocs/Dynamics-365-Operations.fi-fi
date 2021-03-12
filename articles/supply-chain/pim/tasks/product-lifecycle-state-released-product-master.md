---
title: Tuotteen elinkaaren tilan liittäminen vapautettuun päätuotteeseen
description: Tässä menettelyssä kerrotaan, miten tuotteen elinkaaren tila liitetään julkaistuun päätuotteeseen ja sen variantteihin.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a9f8f519c54ffe4f1a2a44da51ac5d97c56182a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992217"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a><span data-ttu-id="399b9-103">Tuotteen elinkaaren tilan liittäminen vapautettuun päätuotteeseen</span><span class="sxs-lookup"><span data-stu-id="399b9-103">Assign a product lifecycle state to a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="399b9-104">Tässä menettelyssä kerrotaan, miten tuotteen elinkaaren tila liitetään julkaistuun päätuotteeseen ja sen variantteihin.</span><span class="sxs-lookup"><span data-stu-id="399b9-104">This procedure shows how to assign a product lifecycle state to a released product master and its variants.</span></span> <span data-ttu-id="399b9-105">Edellytykset: Sinun on toistettava ensin Uuden tuotteen elinkaaren tilan luominen -tehtäväopas ja varmistettava, että luotuna on vähintään yksi tuotteen elinkaaren tila, ennen kuin toistat tämän tehtäväoppaan.</span><span class="sxs-lookup"><span data-stu-id="399b9-105">Prerequisite: You need to play the task guide "Create a new product lifecycle state" first to make sure that you have at least one product lifecycle state created before you can play this task guide.</span></span>


## <a name="find-a-released-product-master"></a><span data-ttu-id="399b9-106">Etsi julkaistu päätuote</span><span class="sxs-lookup"><span data-stu-id="399b9-106">Find a released product master</span></span>
1. <span data-ttu-id="399b9-107">Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="399b9-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="399b9-108">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="399b9-108">In the list, find and select the desired record.</span></span>

> [!NOTE]
> <span data-ttu-id="399b9-109">Päätuotteen tuotteen alatyyppi on Päätuote.</span><span class="sxs-lookup"><span data-stu-id="399b9-109">A product master has the Product subtype Product master.</span></span>  

## <a name="update-the-lifecycle-state"></a><span data-ttu-id="399b9-110">Elinkaaren tilan päivittäminen</span><span class="sxs-lookup"><span data-stu-id="399b9-110">Update the lifecycle state</span></span>
1. <span data-ttu-id="399b9-111">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="399b9-111">Click Edit.</span></span>
2. <span data-ttu-id="399b9-112">Syötä tai valitse arvo Tuotteen elinkaaren tila -kenttään.</span><span class="sxs-lookup"><span data-stu-id="399b9-112">In the Product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="399b9-113">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="399b9-113">Click Save.</span></span>
4. <span data-ttu-id="399b9-114">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="399b9-114">Click Yes.</span></span>

> [!NOTE]
> <span data-ttu-id="399b9-115">Jos valittuna on Kyllä, kaikki liittyvät julkaistut tuotevariantit, joilla on sama alkuperäinen tila kuin julkaistulla päätuotteella, päivitetään myös uuden tuotteen elinkaaren tilan mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="399b9-115">If Yes is selected, all the related released product variants that have the same original status as the released product master are also updated to the new product lifecycle state.</span></span> <span data-ttu-id="399b9-116">Jos valittuna on Ei, kaikkien varianttien tila pysyy entisellään.</span><span class="sxs-lookup"><span data-stu-id="399b9-116">If No is selected, all variants keep their actual state.</span></span> <span data-ttu-id="399b9-117">Variantteja, joilla on eri tuotteen elinkaaren tila kuin julkaistulla päätuotteella, ei päivitetä.</span><span class="sxs-lookup"><span data-stu-id="399b9-117">Variants that have a different product lifecycle state from the released product master are not updated.</span></span>  

## <a name="verify-the-lifecycle-state-of-the-variants"></a><span data-ttu-id="399b9-118">Varianttien elinkaaren tilan tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="399b9-118">Verify the lifecycle state of the variants</span></span>
1. <span data-ttu-id="399b9-119">Valitse Vapautetut tuotevariantit.</span><span class="sxs-lookup"><span data-stu-id="399b9-119">Click Released product variants.</span></span>

> [!NOTE]
> <span data-ttu-id="399b9-120">Huomaa, että kaikki variantit ovat perineet valitun elinkaaren tilan julkaistulta päätuotteelta.</span><span class="sxs-lookup"><span data-stu-id="399b9-120">Note that all variants have inherited the selected lifecycle state from the released product master.</span></span>  

2. <span data-ttu-id="399b9-121">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="399b9-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="399b9-122">Syötä tai valitse arvo Tuotteen elinkaaren tila -kenttään.</span><span class="sxs-lookup"><span data-stu-id="399b9-122">In the Product lifecycle state field, enter or select a value.</span></span>

