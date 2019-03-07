---
title: Kopioi oheistuotteet aiemmasta luodusta reseptiversiosta
description: Tässä menettelyssä näytetään, miten voit kopioida rinnakkaistuotteet aiemmin luodusta reseptiversiosta toiseen, vapautetun tuotteen reseptiversioon.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, PmfFormulaCoBy, BOMRouteCopyDialog
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 179c12da0c2ddc7b5e2f2fdddd21168eac121811
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "319244"
---
# <a name="copy-co-products-from-an-existing-formula-version"></a><span data-ttu-id="805e1-103">Kopioi oheistuotteet aiemmasta luodusta reseptiversiosta</span><span class="sxs-lookup"><span data-stu-id="805e1-103">Copy co-products from an existing formula version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="805e1-104">Tässä menettelyssä näytetään, miten voit kopioida rinnakkaistuotteet aiemmin luodusta reseptiversiosta toiseen, vapautetun tuotteen reseptiversioon.</span><span class="sxs-lookup"><span data-stu-id="805e1-104">This procedure shows how to copy co-products from an existing formula version to a different formula version for a released product.</span></span> <span data-ttu-id="805e1-105">Edellytyksenä on vähintään, että rinnakkaistuotteisiin on liitetty vähintään yksi reseptiversio.</span><span class="sxs-lookup"><span data-stu-id="805e1-105">It is a prerequisite that there is at least one formula version associated with co-products.</span></span> <span data-ttu-id="805e1-106">Tämän menettelyn luomisessa käytetty USP2-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="805e1-106">The demo data company USP2 is used to create this procedure.</span></span>


## <a name="find-a-released-product"></a><span data-ttu-id="805e1-107">Etsi vapautettu tuote</span><span class="sxs-lookup"><span data-stu-id="805e1-107">Find a released product</span></span>
1. <span data-ttu-id="805e1-108">Siirry Vapautetut tuotteet -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="805e1-108">Go to Released products.</span></span>
2. <span data-ttu-id="805e1-109">Valitse Näytä suodattimet.</span><span class="sxs-lookup"><span data-stu-id="805e1-109">Click Show filters.</span></span>
    * <span data-ttu-id="805e1-110">Olet lisäämässä Tuotantotyyppi-kentän suodattimen valintaikkunaan.</span><span class="sxs-lookup"><span data-stu-id="805e1-110">You are about to add the field Production type in the filter dialog box.</span></span>  
3. <span data-ttu-id="805e1-111">Lisää Tuotantotyyppi-kenttä napsauttamalla Lisää suodatinkenttä.</span><span class="sxs-lookup"><span data-stu-id="805e1-111">Click Add a filter field to add the field Production type.</span></span>
    * <span data-ttu-id="805e1-112">Seuraavassa vaiheessa kaava on lisättävä manuaalisesti Tuotantotyyppi-kenttään ennen, kuin napsautat Käytä-painiketta.</span><span class="sxs-lookup"><span data-stu-id="805e1-112">In the next step, you need to manually enter Formula in the Production type field before you select Apply.</span></span> <span data-ttu-id="805e1-113">Tämä asettaa julkaistujen tuotteiden luettelon suodatuksen.</span><span class="sxs-lookup"><span data-stu-id="805e1-113">This sets the filter on the list of released products.</span></span>  
4. <span data-ttu-id="805e1-114">Kirjoita kaava manuaalisesti Tuotantotyyppi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="805e1-114">Manually enter Formula in the Production type field.</span></span>
5. <span data-ttu-id="805e1-115">Valitse Apply.</span><span class="sxs-lookup"><span data-stu-id="805e1-115">Click Apply.</span></span>

## <a name="select-a-released-product"></a><span data-ttu-id="805e1-116">Valitse vapautettu tuote</span><span class="sxs-lookup"><span data-stu-id="805e1-116">Select a released product</span></span>
1. <span data-ttu-id="805e1-117">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="805e1-117">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="805e1-118">Valitse Reseptiversiot.</span><span class="sxs-lookup"><span data-stu-id="805e1-118">Click Formula versions.</span></span>
    * <span data-ttu-id="805e1-119">Valitse teknisen suunnittelun toimintoruudussa Reseptiversiot.</span><span class="sxs-lookup"><span data-stu-id="805e1-119">On the Engineering Action Pane, click Formula versions.</span></span>  

## <a name="copy-co-products"></a><span data-ttu-id="805e1-120">Kopioi oheistuotteet</span><span class="sxs-lookup"><span data-stu-id="805e1-120">Copy co-products</span></span>
1. <span data-ttu-id="805e1-121">Valitse toimintoruudussa Reseptiversio.</span><span class="sxs-lookup"><span data-stu-id="805e1-121">On the Action Pane, click Formula version.</span></span>
2. <span data-ttu-id="805e1-122">Valitse Oheistuotteet.</span><span class="sxs-lookup"><span data-stu-id="805e1-122">Click Co-products.</span></span>
3. <span data-ttu-id="805e1-123">Valitse Kopioi.</span><span class="sxs-lookup"><span data-stu-id="805e1-123">Click Copy.</span></span>
4. <span data-ttu-id="805e1-124">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="805e1-124">In the Item number field, enter or select a value.</span></span>
5. <span data-ttu-id="805e1-125">Anna tai valitse arvo Reseptiversio-kentässä.</span><span class="sxs-lookup"><span data-stu-id="805e1-125">In the Formula version field, enter or select a value.</span></span>
6. <span data-ttu-id="805e1-126">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="805e1-126">Click OK.</span></span>
7. <span data-ttu-id="805e1-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="805e1-127">Close the page.</span></span>

