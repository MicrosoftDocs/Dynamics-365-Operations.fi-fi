--- 
title: Laskujen ja avaintietojen tarkistaminen ostoreskontrassa
description: "Kun vastaanotat toimittajalta ostotilaukseen perustuvan laskun toimitetuista tavaroista tai palveluista, liiketoimintaprosessit voivat edellyttää, että tavarat tai palvelut on vastaanotettu ennen laskun hyväkymistä maksettavaksi."
author: saraschi2
manager: AnnBe
ms.date: 02/16/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 5cd9448c95b7ec0c4a82aca3d21d961259dfb109
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a><span data-ttu-id="a8db0-103">Laskujen ja avaintietojen tarkistaminen ostoreskontrassa</span><span class="sxs-lookup"><span data-stu-id="a8db0-103">Audit invoices and key data in accounts payable</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a8db0-104">Kun vastaanotat toimittajalta ostotilaukseen perustuvan laskun toimitetuista tavaroista tai palveluista, liiketoimintaprosessit voivat edellyttää, että tavarat tai palvelut on vastaanotettu ennen laskun hyväkymistä maksettavaksi.</span><span class="sxs-lookup"><span data-stu-id="a8db0-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="a8db0-105">Varmista ennen aloittamista, että laskun täsmäytyksen konfigurointiavain on valittuna.</span><span class="sxs-lookup"><span data-stu-id="a8db0-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="a8db0-106">Varmista Ostoreskontran parametrit -sivulla, että Ota käyttöön laskujen täsmäytyksen vahvistus -asetus on valittu, Kirjaa lasku, jossa on ristiriitoja -kentän arvoksi on määritetty Edellytä hyväksyntä ja Rivien vastaavuuskäytäntö -kentän arvoksi on määritetty Kolmisuuntainen vastaavuus.</span><span class="sxs-lookup"><span data-stu-id="a8db0-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="a8db0-107">Näissä toimintaohjeissa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="a8db0-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="a8db0-108">Nämä vaiheet suorittaa ostoreskontran esimies tai laskentapäällikön rooli.</span><span class="sxs-lookup"><span data-stu-id="a8db0-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="a8db0-109">Luo ostotilaus</span><span class="sxs-lookup"><span data-stu-id="a8db0-109">Create a purchase order</span></span>
1. <span data-ttu-id="a8db0-110">Siirry Kaikki ostotilaukset -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="a8db0-110">Go to All purchase orders.</span></span>
2. <span data-ttu-id="a8db0-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="a8db0-111">Click New.</span></span>
3. <span data-ttu-id="a8db0-112">Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="a8db0-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a8db0-113">Kirjoita arvo Toimittajan tili -kenttään.</span><span class="sxs-lookup"><span data-stu-id="a8db0-113">In the Vendor account field, type a value.</span></span>
5. <span data-ttu-id="a8db0-114">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a8db0-114">Click OK.</span></span>
6. <span data-ttu-id="a8db0-115">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="a8db0-115">Click Add line.</span></span>
7. <span data-ttu-id="a8db0-116">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a8db0-116">In the Item number field, type a value.</span></span>
8. <span data-ttu-id="a8db0-117">Valitse toimintoruudussa Osta.</span><span class="sxs-lookup"><span data-stu-id="a8db0-117">On the Action Pane, click Purchase.</span></span>
9. <span data-ttu-id="a8db0-118">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="a8db0-118">Click Confirm.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="a8db0-119">Tuotteen vastaanoton kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="a8db0-119">Post a product receipt</span></span>
1. <span data-ttu-id="a8db0-120">Valitse toimintoruudussa Vastaanota.</span><span class="sxs-lookup"><span data-stu-id="a8db0-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="a8db0-121">Valitse Tuotteen vastaanotto.</span><span class="sxs-lookup"><span data-stu-id="a8db0-121">Click Product receipt.</span></span>
3. <span data-ttu-id="a8db0-122">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="a8db0-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="a8db0-123">Kirjoita arvo Tuotteen vastaanotto -kenttään.</span><span class="sxs-lookup"><span data-stu-id="a8db0-123">In the Product receipt field, type a value.</span></span>
5. <span data-ttu-id="a8db0-124">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a8db0-124">Click OK.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="a8db0-125">Toimittajan laskun tallentaminen ja täsmäyttäminen tuotteen vastaanoton kanssa</span><span class="sxs-lookup"><span data-stu-id="a8db0-125">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="a8db0-126">Valitse toimintoruudussa Lasku.</span><span class="sxs-lookup"><span data-stu-id="a8db0-126">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="a8db0-127">Valitse Lasku.</span><span class="sxs-lookup"><span data-stu-id="a8db0-127">Click Invoice.</span></span>
3. <span data-ttu-id="a8db0-128">Kirjoita arvo Numero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a8db0-128">In the Number field, type a value.</span></span>
4. <span data-ttu-id="a8db0-129">Valitse Oletusarvo kohteesta: Tilattu määrä, kun haluat avata valintaikkunan.</span><span class="sxs-lookup"><span data-stu-id="a8db0-129">Click Default from: Ordered quantity to open the drop dialog.</span></span>
5. <span data-ttu-id="a8db0-130">Valitse vaihtoehto Rivien oletusmäärä -kentässä.</span><span class="sxs-lookup"><span data-stu-id="a8db0-130">In the Default quantity for lines field, select an option.</span></span>
6. <span data-ttu-id="a8db0-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a8db0-131">Click OK.</span></span>
7. <span data-ttu-id="a8db0-132">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="a8db0-132">Click Yes.</span></span>
8. <span data-ttu-id="a8db0-133">Valitse Täsmäytä tuotteiden vastaanotot.</span><span class="sxs-lookup"><span data-stu-id="a8db0-133">Click Match product receipts.</span></span>
9. <span data-ttu-id="a8db0-134">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a8db0-134">Click OK.</span></span>
10. <span data-ttu-id="a8db0-135">Valitse toimintoruudussa Tarkista.</span><span class="sxs-lookup"><span data-stu-id="a8db0-135">On the Action Pane, click Review.</span></span>
11. <span data-ttu-id="a8db0-136">Valitse Täsmäytyksen tiedot.</span><span class="sxs-lookup"><span data-stu-id="a8db0-136">Click Matching details.</span></span>


