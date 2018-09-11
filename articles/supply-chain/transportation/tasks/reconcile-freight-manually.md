--- 
title: "Täsmäytä rahti manuaalisesti"
description: "Tässä menettelyssä kuvataan, miten rahti täsmäytetään manuaalisesti."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 3d871ab5395cbaf5e5039dcf8ebf39ade6752a29
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2018

---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="a895c-103">Täsmäytä rahti manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="a895c-103">Reconcile freight manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a895c-104">Tässä menettelyssä kuvataan, miten rahti täsmäytetään manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="a895c-104">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="a895c-105">Kuljetuskoordinaattori tekee tämän yleensä.</span><span class="sxs-lookup"><span data-stu-id="a895c-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="a895c-106">Voit käyttää tätä menettelyä USMF:n esittely-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="a895c-106">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="a895c-107">Valitse täsmäytettävä kuorma</span><span class="sxs-lookup"><span data-stu-id="a895c-107">Select a load to reconcile</span></span>
1. <span data-ttu-id="a895c-108">Valitse Kuljetustenhallinta > Suunnittelu > Kuormasuunnittelun työtila.</span><span class="sxs-lookup"><span data-stu-id="a895c-108">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="a895c-109">Poista Piilota toimitettu ja vastaanotettu -valintaruudun valinta.</span><span class="sxs-lookup"><span data-stu-id="a895c-109">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="a895c-110">Valitse luettelossa kuorma, jonka tunnus on 00006.</span><span class="sxs-lookup"><span data-stu-id="a895c-110">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="a895c-111">Luo kuljettajan lasku</span><span class="sxs-lookup"><span data-stu-id="a895c-111">Create a carrier invoice</span></span>
    * <span data-ttu-id="a895c-112">Jos rahti täsmäytetään manuaalisesti ja et vastaanota kuljettajan laskuja automaattisesti, voit luoda laskun rahtilaskun perusteella.</span><span class="sxs-lookup"><span data-stu-id="a895c-112">If you reconcile freight manually and don’t receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="a895c-113">Valitse Aiheeseen liittyviä tietoja.</span><span class="sxs-lookup"><span data-stu-id="a895c-113">Click Related information.</span></span>
2. <span data-ttu-id="a895c-114">Valitse Rahtilaskun tiedot.</span><span class="sxs-lookup"><span data-stu-id="a895c-114">Click Freight bill details.</span></span>
3. <span data-ttu-id="a895c-115">Valitse Luo rahtilasku.</span><span class="sxs-lookup"><span data-stu-id="a895c-115">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="a895c-116">Kirjoita Lasku-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="a895c-116">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="a895c-117">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a895c-117">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="a895c-118">Täsmäytä lasku</span><span class="sxs-lookup"><span data-stu-id="a895c-118">Reconcile the invoice</span></span>
    * <span data-ttu-id="a895c-119">Kuljettajan lasku ja rahtilasku täsmäytetään rivi kerrallaan.</span><span class="sxs-lookup"><span data-stu-id="a895c-119">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="a895c-120">Valitse Täsmäytä rahtilaskut ja laskut.</span><span class="sxs-lookup"><span data-stu-id="a895c-120">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="a895c-121">Laajenna Laskun tiedot -osa.</span><span class="sxs-lookup"><span data-stu-id="a895c-121">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="a895c-122">Laajenna Täsmäyttämättömän rahtilaskun tiedot -osa.</span><span class="sxs-lookup"><span data-stu-id="a895c-122">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="a895c-123">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="a895c-123">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="a895c-124">Valitse Täsmäytä.</span><span class="sxs-lookup"><span data-stu-id="a895c-124">Click Match.</span></span>
6. <span data-ttu-id="a895c-125">Laajenna Täsmäytetyn rahtilaskun tiedot -osa.</span><span class="sxs-lookup"><span data-stu-id="a895c-125">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="a895c-126">Lähetä lasku hyväksyttäväksi</span><span class="sxs-lookup"><span data-stu-id="a895c-126">Submit the invoice for approval</span></span>
1. <span data-ttu-id="a895c-127">Valitse Lähetä hyväksyttäväksi.</span><span class="sxs-lookup"><span data-stu-id="a895c-127">Click Submit for approval.</span></span>
2. <span data-ttu-id="a895c-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a895c-128">Close the page.</span></span>
3. <span data-ttu-id="a895c-129">Poista Piilota hyväksytyt -valintaruudun valinta.</span><span class="sxs-lookup"><span data-stu-id="a895c-129">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="a895c-130">Valitse Toimittajan laskun kirjauskansiot.</span><span class="sxs-lookup"><span data-stu-id="a895c-130">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="a895c-131">Avaa Viitekirjauskansion numero -kentän linkki napsauttamalla.</span><span class="sxs-lookup"><span data-stu-id="a895c-131">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="a895c-132">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="a895c-132">Click Lines.</span></span>


