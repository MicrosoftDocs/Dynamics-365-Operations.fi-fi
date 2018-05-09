--- 
title: "Toimittajan laskun kirjaaminen ja täsmäyttäminen vastaanotettuihin määriin"
description: "Kun vastaanotat toimittajalta ostotilaukseen perustuvan laskun toimitetuista tavaroista tai palveluista, liiketoimintaprosessit voivat edellyttää, että tavarat tai palvelut on vastaanotettu ennen laskun hyväkymistä maksettavaksi."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fdf5b7bf1e1a8a442d7e763d3bb7d2c2429fc615
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a><span data-ttu-id="79aa3-103">Toimittajan laskun kirjaaminen ja täsmäyttäminen vastaanotettuihin määriin</span><span class="sxs-lookup"><span data-stu-id="79aa3-103">Record vendor invoice and match against received quantity</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="79aa3-104">Kun vastaanotat toimittajalta ostotilaukseen perustuvan laskun toimitetuista tavaroista tai palveluista, liiketoimintaprosessit voivat edellyttää, että tavarat tai palvelut on vastaanotettu ennen laskun hyväkymistä maksettavaksi.</span><span class="sxs-lookup"><span data-stu-id="79aa3-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="79aa3-105">Varmista ennen aloittamista, että laskun täsmäytyksen konfigurointiavain on valittuna.</span><span class="sxs-lookup"><span data-stu-id="79aa3-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="79aa3-106">Varmista Ostoreskontran parametrit -sivulla, että Ota käyttöön laskujen täsmäytyksen vahvistus -asetus on valittu, Kirjaa lasku, jossa on ristiriitoja -kentän arvoksi on määritetty Edellytä hyväksyntä ja Rivien vastaavuuskäytäntö -kentän arvoksi on määritetty Kolmisuuntainen vastaavuus.</span><span class="sxs-lookup"><span data-stu-id="79aa3-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="79aa3-107">Näissä toimintaohjeissa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="79aa3-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="79aa3-108">Nämä vaiheet suorittaa ostoreskontran esimies tai laskentapäällikön rooli.</span><span class="sxs-lookup"><span data-stu-id="79aa3-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="79aa3-109">Luo ostotilaus</span><span class="sxs-lookup"><span data-stu-id="79aa3-109">Create a purchase order</span></span>
1. <span data-ttu-id="79aa3-110">Siirry Kaikki ostotilaukset -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="79aa3-110">Go to All purchase orders.</span></span>
2. <span data-ttu-id="79aa3-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="79aa3-111">Click New.</span></span>
3. <span data-ttu-id="79aa3-112">Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="79aa3-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="79aa3-113">Kirjoita arvo Toimittajan tili -kenttään.</span><span class="sxs-lookup"><span data-stu-id="79aa3-113">In the Vendor account field, type a value.</span></span>
5. <span data-ttu-id="79aa3-114">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="79aa3-114">Click OK.</span></span>
6. <span data-ttu-id="79aa3-115">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="79aa3-115">Click Add line.</span></span>
7. <span data-ttu-id="79aa3-116">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="79aa3-116">In the Item number field, type a value.</span></span>
8. <span data-ttu-id="79aa3-117">Valitse toimintoruudussa Osta.</span><span class="sxs-lookup"><span data-stu-id="79aa3-117">On the Action Pane, click Purchase.</span></span>
9. <span data-ttu-id="79aa3-118">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="79aa3-118">Click Confirm.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="79aa3-119">Tuotteen vastaanoton kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="79aa3-119">Post a product receipt</span></span>
1. <span data-ttu-id="79aa3-120">Valitse toimintoruudussa Vastaanota.</span><span class="sxs-lookup"><span data-stu-id="79aa3-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="79aa3-121">Valitse Tuotteen vastaanotto.</span><span class="sxs-lookup"><span data-stu-id="79aa3-121">Click Product receipt.</span></span>
3. <span data-ttu-id="79aa3-122">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="79aa3-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="79aa3-123">Kirjoita arvo Tuotteen vastaanotto -kenttään.</span><span class="sxs-lookup"><span data-stu-id="79aa3-123">In the Product receipt field, type a value.</span></span>
5. <span data-ttu-id="79aa3-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="79aa3-124">Click OK.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="79aa3-125">Toimittajan laskun tallentaminen ja täsmäyttäminen tuotteen vastaanoton kanssa</span><span class="sxs-lookup"><span data-stu-id="79aa3-125">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="79aa3-126">Valitse toimintoruudussa Lasku.</span><span class="sxs-lookup"><span data-stu-id="79aa3-126">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="79aa3-127">Valitse Lasku.</span><span class="sxs-lookup"><span data-stu-id="79aa3-127">Click Invoice.</span></span>
3. <span data-ttu-id="79aa3-128">Kirjoita arvo Numero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="79aa3-128">In the Number field, type a value.</span></span>
4. <span data-ttu-id="79aa3-129">Valitse Oletusarvo kohteesta: Tilattu määrä, kun haluat avata valintaikkunan.</span><span class="sxs-lookup"><span data-stu-id="79aa3-129">Click Default from: Ordered quantity to open the drop dialog.</span></span>
5. <span data-ttu-id="79aa3-130">Valitse vaihtoehto Rivien oletusmäärä -kentässä.</span><span class="sxs-lookup"><span data-stu-id="79aa3-130">In the Default quantity for lines field, select an option.</span></span>
6. <span data-ttu-id="79aa3-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="79aa3-131">Click OK.</span></span>
7. <span data-ttu-id="79aa3-132">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="79aa3-132">Click Yes.</span></span>
8. <span data-ttu-id="79aa3-133">Valitse Täsmäytä tuotteiden vastaanotot.</span><span class="sxs-lookup"><span data-stu-id="79aa3-133">Click Match product receipts.</span></span>
9. <span data-ttu-id="79aa3-134">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="79aa3-134">Click OK.</span></span>
10. <span data-ttu-id="79aa3-135">Valitse toimintoruudussa Tarkista.</span><span class="sxs-lookup"><span data-stu-id="79aa3-135">On the Action Pane, click Review.</span></span>
11. <span data-ttu-id="79aa3-136">Valitse Täsmäytyksen tiedot.</span><span class="sxs-lookup"><span data-stu-id="79aa3-136">Click Matching details.</span></span>


