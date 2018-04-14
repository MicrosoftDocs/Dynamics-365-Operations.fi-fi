--- 
title: Kopioi oheistuotteet aiemmasta luodusta reseptiversiosta
description: "Tässä menettelyssä näytetään, miten voit kopioida rinnakkaistuotteet aiemmin luodusta reseptiversiosta toiseen, vapautetun tuotteen reseptiversioon."
author: YuyuScheller
manager: AnnBe
ms.date: 06/06/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e6ca0de2956e7e2b76f1286b0d01a3a2e3f3d53d
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="copy-co-products-from-an-existing-formula-version"></a><span data-ttu-id="f160b-103">Kopioi oheistuotteet aiemmasta luodusta reseptiversiosta</span><span class="sxs-lookup"><span data-stu-id="f160b-103">Copy co-products from an existing formula version</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f160b-104">Tässä menettelyssä näytetään, miten voit kopioida rinnakkaistuotteet aiemmin luodusta reseptiversiosta toiseen, vapautetun tuotteen reseptiversioon.</span><span class="sxs-lookup"><span data-stu-id="f160b-104">This procedure shows how to copy co-products from an existing formula version to a different formula version for a released product.</span></span> <span data-ttu-id="f160b-105">Edellytyksenä on vähintään, että rinnakkaistuotteisiin on liitetty vähintään yksi reseptiversio.</span><span class="sxs-lookup"><span data-stu-id="f160b-105">It is a prerequisite that there is at least one formula version associated with co-products.</span></span> <span data-ttu-id="f160b-106">Tämän menettelyn luomisessa käytetty USP2-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="f160b-106">The demo data company USP2 is used to create this procedure.</span></span>


## <a name="find-a-released-product"></a><span data-ttu-id="f160b-107">Etsi vapautettu tuote</span><span class="sxs-lookup"><span data-stu-id="f160b-107">Find a released product</span></span>
1. <span data-ttu-id="f160b-108">Siirry Vapautetut tuotteet -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="f160b-108">Go to Released products.</span></span>
2. <span data-ttu-id="f160b-109">Valitse Näytä suodattimet.</span><span class="sxs-lookup"><span data-stu-id="f160b-109">Click Show filters.</span></span>
    * <span data-ttu-id="f160b-110">Olet lisäämässä Tuotantotyyppi-kentän suodattimen valintaikkunaan.</span><span class="sxs-lookup"><span data-stu-id="f160b-110">You are about to add the field Production type in the filter dialog box.</span></span>  
3. <span data-ttu-id="f160b-111">Lisää Tuotantotyyppi-kenttä napsauttamalla Lisää suodatinkenttä.</span><span class="sxs-lookup"><span data-stu-id="f160b-111">Click Add a filter field to add the field Production type.</span></span>
    * <span data-ttu-id="f160b-112">Seuraavassa vaiheessa kaava on lisättävä manuaalisesti Tuotantotyyppi-kenttään ennen, kuin napsautat Käytä-painiketta.</span><span class="sxs-lookup"><span data-stu-id="f160b-112">In the next step, you need to manually enter Formula in the Production type field before you select Apply.</span></span> <span data-ttu-id="f160b-113">Tämä asettaa julkaistujen tuotteiden luettelon suodatuksen.</span><span class="sxs-lookup"><span data-stu-id="f160b-113">This sets the filter on the list of released products.</span></span>  
4. <span data-ttu-id="f160b-114">Kirjoita kaava manuaalisesti Tuotantotyyppi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f160b-114">Manually enter Formula in the Production type field.</span></span>
5. <span data-ttu-id="f160b-115">Valitse Apply.</span><span class="sxs-lookup"><span data-stu-id="f160b-115">Click Apply.</span></span>

## <a name="select-a-released-product"></a><span data-ttu-id="f160b-116">Valitse vapautettu tuote</span><span class="sxs-lookup"><span data-stu-id="f160b-116">Select a released product</span></span>
1. <span data-ttu-id="f160b-117">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="f160b-117">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="f160b-118">Valitse Reseptiversiot.</span><span class="sxs-lookup"><span data-stu-id="f160b-118">Click Formula versions.</span></span>
    * <span data-ttu-id="f160b-119">Valitse teknisen suunnittelun toimintoruudussa Reseptiversiot.</span><span class="sxs-lookup"><span data-stu-id="f160b-119">On the Engineering Action Pane, click Formula versions.</span></span>  

## <a name="copy-co-products"></a><span data-ttu-id="f160b-120">Kopioi oheistuotteet</span><span class="sxs-lookup"><span data-stu-id="f160b-120">Copy co-products</span></span>
1. <span data-ttu-id="f160b-121">Valitse toimintoruudussa Reseptiversio.</span><span class="sxs-lookup"><span data-stu-id="f160b-121">On the Action Pane, click Formula version.</span></span>
2. <span data-ttu-id="f160b-122">Valitse Oheistuotteet.</span><span class="sxs-lookup"><span data-stu-id="f160b-122">Click Co-products.</span></span>
3. <span data-ttu-id="f160b-123">Valitse Kopioi.</span><span class="sxs-lookup"><span data-stu-id="f160b-123">Click Copy.</span></span>
4. <span data-ttu-id="f160b-124">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="f160b-124">In the Item number field, enter or select a value.</span></span>
5. <span data-ttu-id="f160b-125">Anna tai valitse arvo Reseptiversio-kentässä.</span><span class="sxs-lookup"><span data-stu-id="f160b-125">In the Formula version field, enter or select a value.</span></span>
6. <span data-ttu-id="f160b-126">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f160b-126">Click OK.</span></span>
7. <span data-ttu-id="f160b-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f160b-127">Close the page.</span></span>


