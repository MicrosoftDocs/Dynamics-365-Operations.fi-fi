---
title: Laskujen ja avaintietojen tarkistaminen ostoreskontrassa
description: Tässä aiheessa näytetään, miten ostoreskontran laskut ja keskeiset tiedot voidaan tarkistaa.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5bb89f0adce41b045b1f573c4c0e841f78b2248c
ms.sourcegitcommit: 95d06006142e6bf83351fb075b413fdc2074d5ee
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761546"
---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a><span data-ttu-id="5bf98-103">Laskujen ja avaintietojen tarkistaminen ostoreskontrassa</span><span class="sxs-lookup"><span data-stu-id="5bf98-103">Audit invoices and key data in accounts payable</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5bf98-104">Kun vastaanotat toimittajalta ostotilaukseen perustuvan laskun toimitetuista tavaroista tai palveluista, liiketoimintaprosessit voivat edellyttää, että tavarat tai palvelut on vastaanotettu ennen laskun hyväkymistä maksettavaksi.</span><span class="sxs-lookup"><span data-stu-id="5bf98-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="5bf98-105">Varmista ennen aloittamista, että laskun täsmäytyksen konfigurointiavain on valittuna.</span><span class="sxs-lookup"><span data-stu-id="5bf98-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="5bf98-106">Varmista **Ostoreskontran parametrit** -sivulla, että Ota käyttöön laskujen täsmäytyksen vahvistus -asetus on valittu, **Kirjaa lasku, jossa on ristiriitoja** -kentän arvoksi on määritetty **Edellytä hyväksyntä** ja **Rivien vastaavuuskäytäntö** -kentän arvoksi on määritetty **Kolmisuuntainen vastaavuus**.</span><span class="sxs-lookup"><span data-stu-id="5bf98-106">In the **Accounts payable parameters** page, ensure that the Enable invoice matching validation option is selected, the **Post invoice with discrepancies** field is set to **Require approval**, and the **Line matching policy** field is set to **Three-way matching**.</span></span>

<span data-ttu-id="5bf98-107">Näissä toimintaohjeissa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="5bf98-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="5bf98-108">Nämä vaiheet suorittaa ostoreskontran esimies tai laskentapäällikön rooli.</span><span class="sxs-lookup"><span data-stu-id="5bf98-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="5bf98-109">Luo ostotilaus</span><span class="sxs-lookup"><span data-stu-id="5bf98-109">Create a purchase order</span></span>
1. <span data-ttu-id="5bf98-110">Valitse **Kaikki ostotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="5bf98-110">Go to **All purchase orders**.</span></span>
2. <span data-ttu-id="5bf98-111">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="5bf98-111">Click **New**.</span></span>
3. <span data-ttu-id="5bf98-112">Kirjoita arvo **Toimittajan tili** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="5bf98-112">In the **Vendor account** field, type a value.</span></span>
4. <span data-ttu-id="5bf98-113">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="5bf98-113">Click **OK**.</span></span>
5. <span data-ttu-id="5bf98-114">Valitse **Lisää rivi**.</span><span class="sxs-lookup"><span data-stu-id="5bf98-114">Click **Add line**.</span></span>
6. <span data-ttu-id="5bf98-115">Kirjoita arvo **Nimiketunnus**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="5bf98-115">In the **Item number** field, type a value.</span></span>
7. <span data-ttu-id="5bf98-116">Valitse toimintoruudussa **Osto**.</span><span class="sxs-lookup"><span data-stu-id="5bf98-116">On the Action Pane, click **Purchase**.</span></span>
8. <span data-ttu-id="5bf98-117">Valitse **Vahvista**.</span><span class="sxs-lookup"><span data-stu-id="5bf98-117">Click **Confirm**.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="5bf98-118">Tuotteen vastaanoton kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="5bf98-118">Post a product receipt</span></span>
1. <span data-ttu-id="5bf98-119">Valitse toimintoruudussa **Vastaanota**.</span><span class="sxs-lookup"><span data-stu-id="5bf98-119">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="5bf98-120">Valitse **Tuotteen vastaanotto**.</span><span class="sxs-lookup"><span data-stu-id="5bf98-120">Click **Product receipt**.</span></span>
3. <span data-ttu-id="5bf98-121">Kirjoita arvo **Tuotteen vastaanotto** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="5bf98-121">In the **Product receipt** field, type a value.</span></span>
4. <span data-ttu-id="5bf98-122">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="5bf98-122">Click **OK**.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="5bf98-123">Toimittajan laskun tallentaminen ja täsmäyttäminen tuotteen vastaanoton kanssa</span><span class="sxs-lookup"><span data-stu-id="5bf98-123">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="5bf98-124">Valitse toimintoruudussa **Lasku > Lasku**.</span><span class="sxs-lookup"><span data-stu-id="5bf98-124">On the Action Pane, click **Invoice > Invoice**.</span></span>
2. <span data-ttu-id="5bf98-125">Kirjoita arvo **Numero**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="5bf98-125">In the **Number** field, type a value.</span></span>
3. <span data-ttu-id="5bf98-126">Avaa valintaikkuna valitsemalla **Oletusarvo kohteesta: Tilattu määrä**.</span><span class="sxs-lookup"><span data-stu-id="5bf98-126">Click **Default from: Ordered quantity** to open the drop dialog.</span></span>
4. <span data-ttu-id="5bf98-127">Valitse vaihtoehto **Rivien oletusmäärä** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="5bf98-127">In the **Default quantity for lines** field, select an option.</span></span>
5. <span data-ttu-id="5bf98-128">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="5bf98-128">Click **OK**.</span></span>
6. <span data-ttu-id="5bf98-129">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="5bf98-129">Click **Yes**.</span></span>
7. <span data-ttu-id="5bf98-130">Valitse **Täsmäytä tuotteiden vastaanotot**.</span><span class="sxs-lookup"><span data-stu-id="5bf98-130">Click **Match product receipts**.</span></span>
8. <span data-ttu-id="5bf98-131">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="5bf98-131">Click **OK**.</span></span>
9. <span data-ttu-id="5bf98-132">Valitse toimintoruudussa **Tarkista**.</span><span class="sxs-lookup"><span data-stu-id="5bf98-132">On the Action Pane, click **Review**.</span></span>
10. <span data-ttu-id="5bf98-133">Valitse **Täsmäytyksen tiedot**.</span><span class="sxs-lookup"><span data-stu-id="5bf98-133">Click **Matching details**.</span></span>

