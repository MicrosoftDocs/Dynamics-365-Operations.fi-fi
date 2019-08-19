---
title: Täsmäytä rahti manuaalisesti
description: Tässä menettelyssä kuvataan, miten rahti täsmäytetään manuaalisesti.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb9c850aa045b72137b8a1d3c8cdae51cf2fd7b6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843238"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="cd737-103">Täsmäytä rahti manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="cd737-103">Reconcile freight manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cd737-104">Tässä menettelyssä kuvataan, miten rahti täsmäytetään manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="cd737-104">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="cd737-105">Kuljetuskoordinaattori tekee tämän yleensä.</span><span class="sxs-lookup"><span data-stu-id="cd737-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="cd737-106">Voit käyttää tätä menettelyä USMF:n esittely-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="cd737-106">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="cd737-107">Valitse täsmäytettävä kuorma</span><span class="sxs-lookup"><span data-stu-id="cd737-107">Select a load to reconcile</span></span>
1. <span data-ttu-id="cd737-108">Valitse Kuljetustenhallinta > Suunnittelu > Kuormasuunnittelun työtila.</span><span class="sxs-lookup"><span data-stu-id="cd737-108">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="cd737-109">Poista Piilota toimitettu ja vastaanotettu -valintaruudun valinta.</span><span class="sxs-lookup"><span data-stu-id="cd737-109">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="cd737-110">Valitse luettelossa kuorma, jonka tunnus on 00006.</span><span class="sxs-lookup"><span data-stu-id="cd737-110">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="cd737-111">Luo kuljettajan lasku</span><span class="sxs-lookup"><span data-stu-id="cd737-111">Create a carrier invoice</span></span>
    * <span data-ttu-id="cd737-112">Jos rahti täsmäytetään manuaalisesti ja et vastaanota kuljettajan laskuja automaattisesti, voit luoda laskun rahtilaskun perusteella.</span><span class="sxs-lookup"><span data-stu-id="cd737-112">If you reconcile freight manually and don’t receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="cd737-113">Valitse Aiheeseen liittyviä tietoja.</span><span class="sxs-lookup"><span data-stu-id="cd737-113">Click Related information.</span></span>
2. <span data-ttu-id="cd737-114">Valitse Rahtilaskun tiedot.</span><span class="sxs-lookup"><span data-stu-id="cd737-114">Click Freight bill details.</span></span>
3. <span data-ttu-id="cd737-115">Valitse Luo rahtilasku.</span><span class="sxs-lookup"><span data-stu-id="cd737-115">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="cd737-116">Kirjoita Lasku-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="cd737-116">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="cd737-117">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="cd737-117">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="cd737-118">Täsmäytä lasku</span><span class="sxs-lookup"><span data-stu-id="cd737-118">Reconcile the invoice</span></span>
    * <span data-ttu-id="cd737-119">Kuljettajan lasku ja rahtilasku täsmäytetään rivi kerrallaan.</span><span class="sxs-lookup"><span data-stu-id="cd737-119">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="cd737-120">Valitse Täsmäytä rahtilaskut ja laskut.</span><span class="sxs-lookup"><span data-stu-id="cd737-120">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="cd737-121">Laajenna Laskun tiedot -osa.</span><span class="sxs-lookup"><span data-stu-id="cd737-121">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="cd737-122">Laajenna Täsmäyttämättömän rahtilaskun tiedot -osa.</span><span class="sxs-lookup"><span data-stu-id="cd737-122">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="cd737-123">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="cd737-123">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="cd737-124">Valitse Täsmäytä.</span><span class="sxs-lookup"><span data-stu-id="cd737-124">Click Match.</span></span>
6. <span data-ttu-id="cd737-125">Laajenna Täsmäytetyn rahtilaskun tiedot -osa.</span><span class="sxs-lookup"><span data-stu-id="cd737-125">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="cd737-126">Lähetä lasku hyväksyttäväksi</span><span class="sxs-lookup"><span data-stu-id="cd737-126">Submit the invoice for approval</span></span>
1. <span data-ttu-id="cd737-127">Valitse Lähetä hyväksyttäväksi.</span><span class="sxs-lookup"><span data-stu-id="cd737-127">Click Submit for approval.</span></span>
2. <span data-ttu-id="cd737-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="cd737-128">Close the page.</span></span>
3. <span data-ttu-id="cd737-129">Poista Piilota hyväksytyt -valintaruudun valinta.</span><span class="sxs-lookup"><span data-stu-id="cd737-129">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="cd737-130">Valitse Toimittajan laskun kirjauskansiot.</span><span class="sxs-lookup"><span data-stu-id="cd737-130">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="cd737-131">Avaa Viitekirjauskansion numero -kentän linkki napsauttamalla.</span><span class="sxs-lookup"><span data-stu-id="cd737-131">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="cd737-132">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="cd737-132">Click Lines.</span></span>

