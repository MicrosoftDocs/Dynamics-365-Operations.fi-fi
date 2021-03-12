---
title: Kopioi oheistuotteet aiemmasta luodusta reseptiversiosta
description: Tässä menettelyssä näytetään, miten voit kopioida rinnakkaistuotteet aiemmin luodusta reseptiversiosta toiseen, vapautetun tuotteen reseptiversioon.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, PmfFormulaCoBy, BOMRouteCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a16a6c8651b401dddfa47c0eb29efb0c3a49038
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981328"
---
# <a name="copy-co-products-from-an-existing-formula-version"></a><span data-ttu-id="be6c8-103">Kopioi oheistuotteet aiemmasta luodusta reseptiversiosta</span><span class="sxs-lookup"><span data-stu-id="be6c8-103">Copy co-products from an existing formula version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="be6c8-104">Tässä menettelyssä näytetään, miten voit kopioida rinnakkaistuotteet aiemmin luodusta reseptiversiosta toiseen, vapautetun tuotteen reseptiversioon.</span><span class="sxs-lookup"><span data-stu-id="be6c8-104">This procedure shows how to copy co-products from an existing formula version to a different formula version for a released product.</span></span> <span data-ttu-id="be6c8-105">Edellytyksenä on vähintään, että rinnakkaistuotteisiin on liitetty vähintään yksi reseptiversio.</span><span class="sxs-lookup"><span data-stu-id="be6c8-105">It is a prerequisite that there is at least one formula version associated with co-products.</span></span> <span data-ttu-id="be6c8-106">Tämän menettelyn luomisessa käytetty USP2-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="be6c8-106">The demo data company USP2 is used to create this procedure.</span></span>


## <a name="find-a-released-product"></a><span data-ttu-id="be6c8-107">Etsi vapautettu tuote</span><span class="sxs-lookup"><span data-stu-id="be6c8-107">Find a released product</span></span>
1. <span data-ttu-id="be6c8-108">Siirry Vapautetut tuotteet -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="be6c8-108">Go to Released products.</span></span>
2. <span data-ttu-id="be6c8-109">Valitse Näytä suodattimet.</span><span class="sxs-lookup"><span data-stu-id="be6c8-109">Click Show filters.</span></span>
    * <span data-ttu-id="be6c8-110">Olet lisäämässä Tuotantotyyppi-kentän suodattimen valintaikkunaan.</span><span class="sxs-lookup"><span data-stu-id="be6c8-110">You are about to add the field Production type in the filter dialog box.</span></span>  
3. <span data-ttu-id="be6c8-111">Lisää Tuotantotyyppi-kenttä napsauttamalla Lisää suodatinkenttä.</span><span class="sxs-lookup"><span data-stu-id="be6c8-111">Click Add a filter field to add the field Production type.</span></span>
    * <span data-ttu-id="be6c8-112">Seuraavassa vaiheessa kaava on lisättävä manuaalisesti Tuotantotyyppi-kenttään ennen, kuin napsautat Käytä-painiketta.</span><span class="sxs-lookup"><span data-stu-id="be6c8-112">In the next step, you need to manually enter Formula in the Production type field before you select Apply.</span></span> <span data-ttu-id="be6c8-113">Tämä asettaa julkaistujen tuotteiden luettelon suodatuksen.</span><span class="sxs-lookup"><span data-stu-id="be6c8-113">This sets the filter on the list of released products.</span></span>  
4. <span data-ttu-id="be6c8-114">Kirjoita kaava manuaalisesti Tuotantotyyppi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="be6c8-114">Manually enter Formula in the Production type field.</span></span>
5. <span data-ttu-id="be6c8-115">Valitse Apply.</span><span class="sxs-lookup"><span data-stu-id="be6c8-115">Click Apply.</span></span>

## <a name="select-a-released-product"></a><span data-ttu-id="be6c8-116">Valitse vapautettu tuote</span><span class="sxs-lookup"><span data-stu-id="be6c8-116">Select a released product</span></span>
1. <span data-ttu-id="be6c8-117">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="be6c8-117">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="be6c8-118">Valitse Reseptiversiot.</span><span class="sxs-lookup"><span data-stu-id="be6c8-118">Click Formula versions.</span></span>
    * <span data-ttu-id="be6c8-119">Valitse teknisen suunnittelun toimintoruudussa Reseptiversiot.</span><span class="sxs-lookup"><span data-stu-id="be6c8-119">On the Engineering Action Pane, click Formula versions.</span></span>  

## <a name="copy-co-products"></a><span data-ttu-id="be6c8-120">Kopioi oheistuotteet</span><span class="sxs-lookup"><span data-stu-id="be6c8-120">Copy co-products</span></span>
1. <span data-ttu-id="be6c8-121">Valitse toimintoruudussa Reseptiversio.</span><span class="sxs-lookup"><span data-stu-id="be6c8-121">On the Action Pane, click Formula version.</span></span>
2. <span data-ttu-id="be6c8-122">Valitse Oheistuotteet.</span><span class="sxs-lookup"><span data-stu-id="be6c8-122">Click Co-products.</span></span>
3. <span data-ttu-id="be6c8-123">Valitse Kopioi.</span><span class="sxs-lookup"><span data-stu-id="be6c8-123">Click Copy.</span></span>
4. <span data-ttu-id="be6c8-124">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="be6c8-124">In the Item number field, enter or select a value.</span></span>
5. <span data-ttu-id="be6c8-125">Anna tai valitse arvo Reseptiversio-kentässä.</span><span class="sxs-lookup"><span data-stu-id="be6c8-125">In the Formula version field, enter or select a value.</span></span>
6. <span data-ttu-id="be6c8-126">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="be6c8-126">Click OK.</span></span>
7. <span data-ttu-id="be6c8-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="be6c8-127">Close the page.</span></span>

