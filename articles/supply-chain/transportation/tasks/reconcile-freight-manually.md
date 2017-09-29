--- 
title: "Täsmäytä rahti manuaalisesti"
description: "Tässä menettelyssä kuvataan, miten rahti täsmäytetään manuaalisesti."
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 15148725664d839694ede8419213d881c7be83dd
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="87f0f-103">Täsmäytä rahti manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="87f0f-103">Reconcile freight manually</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="87f0f-104">Tässä menettelyssä kuvataan, miten rahti täsmäytetään manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="87f0f-104">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="87f0f-105">Kuljetuskoordinaattori tekee tämän yleensä.</span><span class="sxs-lookup"><span data-stu-id="87f0f-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="87f0f-106">Voit käyttää tätä menettelyä USMF:n esittely-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="87f0f-106">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="87f0f-107">Valitse täsmäytettävä kuorma</span><span class="sxs-lookup"><span data-stu-id="87f0f-107">Select a load to reconcile</span></span>
1. <span data-ttu-id="87f0f-108">Valitse Kuljetustenhallinta > Suunnittelu > Kuormasuunnittelun työtila.</span><span class="sxs-lookup"><span data-stu-id="87f0f-108">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="87f0f-109">Poista Piilota toimitettu ja vastaanotettu -valintaruudun valinta.</span><span class="sxs-lookup"><span data-stu-id="87f0f-109">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="87f0f-110">Valitse luettelossa kuorma, jonka tunnus on 00006.</span><span class="sxs-lookup"><span data-stu-id="87f0f-110">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="87f0f-111">Luo kuljettajan lasku</span><span class="sxs-lookup"><span data-stu-id="87f0f-111">Create a carrier invoice</span></span>
    * <span data-ttu-id="87f0f-112">Jos rahti täsmäytetään manuaalisesti ja et vastaanota kuljettajan laskuja automaattisesti, voit luoda laskun rahtilaskun perusteella.</span><span class="sxs-lookup"><span data-stu-id="87f0f-112">If you reconcile freight manually and don’t receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="87f0f-113">Valitse Aiheeseen liittyviä tietoja.</span><span class="sxs-lookup"><span data-stu-id="87f0f-113">Click Related information.</span></span>
2. <span data-ttu-id="87f0f-114">Valitse Rahtilaskun tiedot.</span><span class="sxs-lookup"><span data-stu-id="87f0f-114">Click Freight bill details.</span></span>
3. <span data-ttu-id="87f0f-115">Valitse Luo rahtilasku.</span><span class="sxs-lookup"><span data-stu-id="87f0f-115">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="87f0f-116">Kirjoita Lasku-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="87f0f-116">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="87f0f-117">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="87f0f-117">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="87f0f-118">Täsmäytä lasku</span><span class="sxs-lookup"><span data-stu-id="87f0f-118">Reconcile the invoice</span></span>
    * <span data-ttu-id="87f0f-119">Kuljettajan lasku ja rahtilasku täsmäytetään rivi kerrallaan.</span><span class="sxs-lookup"><span data-stu-id="87f0f-119">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="87f0f-120">Valitse Täsmäytä rahtilaskut ja laskut.</span><span class="sxs-lookup"><span data-stu-id="87f0f-120">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="87f0f-121">Laajenna Laskun tiedot -osa.</span><span class="sxs-lookup"><span data-stu-id="87f0f-121">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="87f0f-122">Laajenna Täsmäyttämättömän rahtilaskun tiedot -osa.</span><span class="sxs-lookup"><span data-stu-id="87f0f-122">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="87f0f-123">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="87f0f-123">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="87f0f-124">Valitse Täsmäytä.</span><span class="sxs-lookup"><span data-stu-id="87f0f-124">Click Match.</span></span>
6. <span data-ttu-id="87f0f-125">Laajenna Täsmäytetyn rahtilaskun tiedot -osa.</span><span class="sxs-lookup"><span data-stu-id="87f0f-125">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="87f0f-126">Lähetä lasku hyväksyttäväksi</span><span class="sxs-lookup"><span data-stu-id="87f0f-126">Submit the invoice for approval</span></span>
1. <span data-ttu-id="87f0f-127">Valitse Lähetä hyväksyttäväksi.</span><span class="sxs-lookup"><span data-stu-id="87f0f-127">Click Submit for approval.</span></span>
2. <span data-ttu-id="87f0f-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="87f0f-128">Close the page.</span></span>
3. <span data-ttu-id="87f0f-129">Poista Piilota hyväksytyt -valintaruudun valinta.</span><span class="sxs-lookup"><span data-stu-id="87f0f-129">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="87f0f-130">Valitse Toimittajan laskun kirjauskansiot.</span><span class="sxs-lookup"><span data-stu-id="87f0f-130">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="87f0f-131">Avaa Viitekirjauskansion numero -kentän linkki napsauttamalla.</span><span class="sxs-lookup"><span data-stu-id="87f0f-131">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="87f0f-132">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="87f0f-132">Click Lines.</span></span>


