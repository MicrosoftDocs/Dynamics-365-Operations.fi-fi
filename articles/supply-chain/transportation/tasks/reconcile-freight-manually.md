---
title: Täsmäytä rahti manuaalisesti
description: Tässä menettelyssä kuvataan, miten rahti täsmäytetään manuaalisesti.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a0ff9aa1070272dd2cee357fb4fc001ffff8df1
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206170"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="09c1b-103">Rahdin manuaalinen täsmäytys</span><span class="sxs-lookup"><span data-stu-id="09c1b-103">Reconcile freight manually</span></span>

<span data-ttu-id="09c1b-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="09c1b-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="09c1b-105">Tässä menettelyssä kuvataan, miten rahti täsmäytetään manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="09c1b-105">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="09c1b-106">Kuljetuskoordinaattori tekee tämän yleensä.</span><span class="sxs-lookup"><span data-stu-id="09c1b-106">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="09c1b-107">Voit käyttää tätä menettelyä USMF:n esittely-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="09c1b-107">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="09c1b-108">Valitse täsmäytettävä kuorma</span><span class="sxs-lookup"><span data-stu-id="09c1b-108">Select a load to reconcile</span></span>
1. <span data-ttu-id="09c1b-109">Valitse Kuljetustenhallinta > Suunnittelu > Kuormasuunnittelun työtila.</span><span class="sxs-lookup"><span data-stu-id="09c1b-109">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="09c1b-110">Poista Piilota toimitettu ja vastaanotettu -valintaruudun valinta.</span><span class="sxs-lookup"><span data-stu-id="09c1b-110">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="09c1b-111">Valitse luettelossa kuorma, jonka tunnus on 00006.</span><span class="sxs-lookup"><span data-stu-id="09c1b-111">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="09c1b-112">Luo kuljettajan lasku</span><span class="sxs-lookup"><span data-stu-id="09c1b-112">Create a carrier invoice</span></span>
<span data-ttu-id="09c1b-113">Jos rahti täsmäytetään manuaalisesti ja et vastaanota kuljettajan laskuja automaattisesti, voit luoda laskun rahtilaskun perusteella.</span><span class="sxs-lookup"><span data-stu-id="09c1b-113">If you reconcile freight manually and don't receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="09c1b-114">Valitse Aiheeseen liittyviä tietoja.</span><span class="sxs-lookup"><span data-stu-id="09c1b-114">Click Related information.</span></span>
2. <span data-ttu-id="09c1b-115">Valitse Rahtilaskun tiedot.</span><span class="sxs-lookup"><span data-stu-id="09c1b-115">Click Freight bill details.</span></span>
3. <span data-ttu-id="09c1b-116">Valitse Luo rahtilasku.</span><span class="sxs-lookup"><span data-stu-id="09c1b-116">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="09c1b-117">Kirjoita Lasku-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="09c1b-117">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="09c1b-118">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="09c1b-118">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="09c1b-119">Täsmäytä lasku</span><span class="sxs-lookup"><span data-stu-id="09c1b-119">Reconcile the invoice</span></span>
<span data-ttu-id="09c1b-120">Kuljettajan lasku ja rahtilasku täsmäytetään rivi kerrallaan.</span><span class="sxs-lookup"><span data-stu-id="09c1b-120">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="09c1b-121">Valitse Täsmäytä rahtilaskut ja laskut.</span><span class="sxs-lookup"><span data-stu-id="09c1b-121">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="09c1b-122">Laajenna Laskun tiedot -osa.</span><span class="sxs-lookup"><span data-stu-id="09c1b-122">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="09c1b-123">Laajenna Täsmäyttämättömän rahtilaskun tiedot -osa.</span><span class="sxs-lookup"><span data-stu-id="09c1b-123">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="09c1b-124">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="09c1b-124">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="09c1b-125">Valitse Täsmäytä.</span><span class="sxs-lookup"><span data-stu-id="09c1b-125">Click Match.</span></span>
6. <span data-ttu-id="09c1b-126">Laajenna Täsmäytetyn rahtilaskun tiedot -osa.</span><span class="sxs-lookup"><span data-stu-id="09c1b-126">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="09c1b-127">Lähetä lasku hyväksyttäväksi</span><span class="sxs-lookup"><span data-stu-id="09c1b-127">Submit the invoice for approval</span></span>
1. <span data-ttu-id="09c1b-128">Valitse Lähetä hyväksyttäväksi.</span><span class="sxs-lookup"><span data-stu-id="09c1b-128">Click Submit for approval.</span></span>
2. <span data-ttu-id="09c1b-129">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="09c1b-129">Close the page.</span></span>
3. <span data-ttu-id="09c1b-130">Poista Piilota hyväksytyt -valintaruudun valinta.</span><span class="sxs-lookup"><span data-stu-id="09c1b-130">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="09c1b-131">Valitse Toimittajan laskun kirjauskansiot.</span><span class="sxs-lookup"><span data-stu-id="09c1b-131">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="09c1b-132">Avaa Viitekirjauskansion numero -kentän linkki napsauttamalla.</span><span class="sxs-lookup"><span data-stu-id="09c1b-132">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="09c1b-133">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="09c1b-133">Click Lines.</span></span>

