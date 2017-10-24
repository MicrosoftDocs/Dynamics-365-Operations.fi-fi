---
title: "Käyttöomaisuuserien tapahtuma-asetukset"
description: "Tässä artikkelissa kerrotaan käyttöomaisuustapahtumien luomisessa käytettävät menetelmät."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3d16b43eda0157e63a0d30fe806dac9a359d5fa4
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="fixed-asset-transaction-options"></a><span data-ttu-id="867f0-103">Käyttöomaisuuserien tapahtuma-asetukset</span><span class="sxs-lookup"><span data-stu-id="867f0-103">Fixed asset transaction options</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="867f0-104">Tässä artikkelissa kerrotaan käyttöomaisuustapahtumien luomisessa käytettävät menetelmät.</span><span class="sxs-lookup"><span data-stu-id="867f0-104">This article describes the different methods available to create fixed asset transactions.</span></span>

<span data-ttu-id="867f0-105">Voit määrittää käyttöomaisuuden integrointiin ostoreskontran, myyntireskontran, hankinnan ja kirjanpidon kanssa.</span><span class="sxs-lookup"><span data-stu-id="867f0-105">You can set up Fixed assets for integration with Accounts payable, Accounts receivable, Procurement and sourcing, and General ledger.</span></span> <span data-ttu-id="867f0-106">Varastossa olevia nimikkeitä voi myös siirtää käyttöomaisuuteen sisäistä käyttöä varten.</span><span class="sxs-lookup"><span data-stu-id="867f0-106">You can also transfer items in Inventory management to Fixed assets if you want to use those items internally.</span></span>

## <a name="accounts-payable"></a><span data-ttu-id="867f0-107">Ostoreskontra</span><span class="sxs-lookup"><span data-stu-id="867f0-107">Accounts payable</span></span>
<span data-ttu-id="867f0-108">Voit määrittää käyttöomaisuustapahtumia Kirjaustosite-sivulla.</span><span class="sxs-lookup"><span data-stu-id="867f0-108">You can enter Fixed assets transactions in the Journal voucher page.</span></span> <span data-ttu-id="867f0-109">Tämä sivu voidaan avata Laskukirjauskansio-sivulta.</span><span class="sxs-lookup"><span data-stu-id="867f0-109">This page can be opened from the Invoice journal page.</span></span> <span data-ttu-id="867f0-110">Voit avata Kirjaustosite-sivun myös Hyväksyttyjen laskujen kirjauskansio -sivulta.</span><span class="sxs-lookup"><span data-stu-id="867f0-110">You can also open the Journal voucher page from the Invoice approval journal page.</span></span> <span data-ttu-id="867f0-111">Valitse Vastatilityyppi-kentässä Käyttöomaisuudet.</span><span class="sxs-lookup"><span data-stu-id="867f0-111">In the Offset account type field, select Fixed assets.</span></span> <span data-ttu-id="867f0-112">Valitse sitten Vastatili-kentässä käyttöomaisuuserän numero.</span><span class="sxs-lookup"><span data-stu-id="867f0-112">Then, in the Offset account field, select a fixed asset number.</span></span> <span data-ttu-id="867f0-113">Anna Käyttöomaisuudet-välilehteen Tapahtumatyyppi- ja Kirja-kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="867f0-113">On the Fixed assets tab, enter values in the Transaction type and Book fields.</span></span>

## <a name="accounts-receivable"></a><span data-ttu-id="867f0-114">Myyntireskontra</span><span class="sxs-lookup"><span data-stu-id="867f0-114">Accounts receivable</span></span>
<span data-ttu-id="867f0-115">Voit määrittää käyttöomaisuustapahtumia Vapaatekstilasku-sivulla.</span><span class="sxs-lookup"><span data-stu-id="867f0-115">You can enter Fixed assets transactions in the Free text invoice page.</span></span>  <span data-ttu-id="867f0-116">Valitse rivinimike Vapaatekstilasku-sivun Laskurivit-ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="867f0-116">In the Free text invoice page, in the Invoice lines grid, select a line item.</span></span> <span data-ttu-id="867f0-117">Valitse Rivin erittely -pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="867f0-117">Click the Line details FastTab.</span></span> <span data-ttu-id="867f0-118">Kirjoita poistotapahtuman käyttöomaisuuserän numero ja kirja.</span><span class="sxs-lookup"><span data-stu-id="867f0-118">Enter the fixed asset number and book for the disposal transaction.</span></span> <span data-ttu-id="867f0-119">Vapaatekstilaskujen käyttöomaisuustapahtumatyyppi on aina Poistomyynti.</span><span class="sxs-lookup"><span data-stu-id="867f0-119">For free text invoices, the fixed asset transaction type is always Disposal - sale.</span></span>

## <a name="procurement-and-sourcing"></a><span data-ttu-id="867f0-120">Hankinta</span><span class="sxs-lookup"><span data-stu-id="867f0-120">Procurement and sourcing</span></span>
<span data-ttu-id="867f0-121">Voit määrittää käyttöomaisuustapahtumia Ostotilaus-sivulla.</span><span class="sxs-lookup"><span data-stu-id="867f0-121">You can enter Fixed assets transactions in the Purchase order page.</span></span> <span data-ttu-id="867f0-122">Luo ostotilaus antamalla vaaditut tiedot ja valitse sitten OK.</span><span class="sxs-lookup"><span data-stu-id="867f0-122">Enter the required information to create a purchase order, and then click OK.</span></span> <span data-ttu-id="867f0-123">Valitse Ostotilaus-sivulla Rivin erittely -pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="867f0-123">In the Purchase order page, click the Line details FastTab.</span></span> <span data-ttu-id="867f0-124">Anna sitten Käyttöomaisuudet-välilehdessä käyttöomaisuuden tiedot.</span><span class="sxs-lookup"><span data-stu-id="867f0-124">Then, on the Fixed assets tab, enter information about the fixed asset.</span></span> 

<span data-ttu-id="867f0-125">Kirjaa hankintatapahtuma olemassa olevalle käyttöomaisuuserälle määrittämällä kirja numero, kirja ja tapahtumatyyppi.</span><span class="sxs-lookup"><span data-stu-id="867f0-125">To post an acquisition transaction for an existing fixed asset, specify the fixed asset number, book, and transaction type.</span></span> <span data-ttu-id="867f0-126">Käyttöomaisuutta ei voi kirjata, jos jokin näistä tiedoista puuttuu.</span><span class="sxs-lookup"><span data-stu-id="867f0-126">The fixed asset cannot be posted if any of this information is missing.</span></span> <span data-ttu-id="867f0-127">Kirjaa hankintatapahtuma uudelle käyttöomaisuuserälle valitsemalla Uusi käyttöomaisuus? -asetus ja valitsemalla sitten käyttöomaisuuserä, johon uusi omaisuuserä liitetään.</span><span class="sxs-lookup"><span data-stu-id="867f0-127">To post an acquisition transaction for a new fixed asset, select the New fixed asset? option, and then select the fixed asset group to assign the new asset to.</span></span> <span data-ttu-id="867f0-128">Käyttöomaisuuskentät eivät ole käytettävissä, jos nimike kuuluu varastomalliryhmään, joka käyttää muuta vakiovarastomallia.</span><span class="sxs-lookup"><span data-stu-id="867f0-128">However, no fixed asset fields are available for a line if the item is in an inventory model group that uses a standard cost inventory model.</span></span> <span data-ttu-id="867f0-129">Käyttöomaisuuden parametrit -sivulla määritetyt asetukset määrittävät lisäksi, voitko kirjata hankintatapahtumia ostomoduuleista.</span><span class="sxs-lookup"><span data-stu-id="867f0-129">Additionally, the options that are defined in the Fixed assets parameters page determine whether you can post acquisition transactions from the purchasing modules.</span></span> 

<span data-ttu-id="867f0-130">Jos käyttöomaisuuserien hankinnoissa käytetään ostotilauskirjauskansiota tai Siirto varastosta käyttöomaisuuteen -kirjauskansiota, sillä on vaikutusta varastoarvoon.</span><span class="sxs-lookup"><span data-stu-id="867f0-130">When a purchase order or the Inventory to fixed assets journal is used to acquire fixed assets, the inventory value is affected.</span></span>

## <a name="general-ledger"></a><span data-ttu-id="867f0-131">Kirjanpito</span><span class="sxs-lookup"><span data-stu-id="867f0-131">General ledger</span></span>
<span data-ttu-id="867f0-132">Käyttöomaisuustapahtumatyyppejä voi kirjata Kirjauskansio-sivulla.</span><span class="sxs-lookup"><span data-stu-id="867f0-132">Any fixed asset transaction type can be posted in the General journal page.</span></span> <span data-ttu-id="867f0-133">Voit käyttää myös käyttöomaisuuden kirjauskansioita kirjaamaan käyttöomaisuustapahtumat.</span><span class="sxs-lookup"><span data-stu-id="867f0-133">You can also use journals in Fixed assets to post fixed asset transactions.</span></span>

## <a name="options-for-entering-fixed-asset-transaction-types"></a><span data-ttu-id="867f0-134">Käyttöomaisuustapahtumatyyppien kirjausvaihtoehtotyypit</span><span class="sxs-lookup"><span data-stu-id="867f0-134">Options for entering fixed asset transaction types</span></span>


| <span data-ttu-id="867f0-135">Tapahtumatyyppi</span><span class="sxs-lookup"><span data-stu-id="867f0-135">Transaction type</span></span>                    | <span data-ttu-id="867f0-136">Moduuli</span><span class="sxs-lookup"><span data-stu-id="867f0-136">Module</span></span>                   | <span data-ttu-id="867f0-137">Optiot</span><span class="sxs-lookup"><span data-stu-id="867f0-137">Options</span></span>                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| <span data-ttu-id="867f0-138">Hankinta, hankintaoikaisu</span><span class="sxs-lookup"><span data-stu-id="867f0-138">Acquisition, Acquisition adjustment</span></span> | <span data-ttu-id="867f0-139">Käyttöomaisuudet</span><span class="sxs-lookup"><span data-stu-id="867f0-139">Fixed assets</span></span>             | <span data-ttu-id="867f0-140">Käyttöomaisuudet, Siirto varastosta käyttöomaisuuteen</span><span class="sxs-lookup"><span data-stu-id="867f0-140">Fixed assets, Inventory to fixed assets</span></span>   |
|                                     | <span data-ttu-id="867f0-141">Kirjanpito</span><span class="sxs-lookup"><span data-stu-id="867f0-141">General ledger</span></span>           | <span data-ttu-id="867f0-142">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="867f0-142">General journal</span></span>                           |
|                                     | <span data-ttu-id="867f0-143">Ostoreskontra</span><span class="sxs-lookup"><span data-stu-id="867f0-143">Accounts payable</span></span>         | <span data-ttu-id="867f0-144">Laskukirjauskansio, hyväksyttyjen laskujen kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="867f0-144">Invoice journal, Invoice approval journal</span></span> |
|                                     | <span data-ttu-id="867f0-145">Hankinta</span><span class="sxs-lookup"><span data-stu-id="867f0-145">Procurement and sourcing</span></span> | <span data-ttu-id="867f0-146">Ostotilaus</span><span class="sxs-lookup"><span data-stu-id="867f0-146">Purchase order</span></span>                            |
| <span data-ttu-id="867f0-147">Poisto</span><span class="sxs-lookup"><span data-stu-id="867f0-147">Depreciation</span></span>                        | <span data-ttu-id="867f0-148">Käyttöomaisuudet</span><span class="sxs-lookup"><span data-stu-id="867f0-148">Fixed assets</span></span>             | <span data-ttu-id="867f0-149">Käyttöomaisuudet</span><span class="sxs-lookup"><span data-stu-id="867f0-149">Fixed assets</span></span>                              |
|                                     | <span data-ttu-id="867f0-150">Kirjanpito</span><span class="sxs-lookup"><span data-stu-id="867f0-150">General ledger</span></span>           | <span data-ttu-id="867f0-151">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="867f0-151">General journal</span></span>                           |
| <span data-ttu-id="867f0-152">Luovutus</span><span class="sxs-lookup"><span data-stu-id="867f0-152">Disposal</span></span>                            | <span data-ttu-id="867f0-153">Käyttöomaisuuserät</span><span class="sxs-lookup"><span data-stu-id="867f0-153">Fixed assets</span></span>             | <span data-ttu-id="867f0-154">Käyttöomaisuuserät</span><span class="sxs-lookup"><span data-stu-id="867f0-154">Fixed assets</span></span>                              |
| <span data-ttu-id="867f0-155">** **</span><span class="sxs-lookup"><span data-stu-id="867f0-155">** **</span></span>                               | <span data-ttu-id="867f0-156">Kirjanpito</span><span class="sxs-lookup"><span data-stu-id="867f0-156">General ledger</span></span>           | <span data-ttu-id="867f0-157">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="867f0-157">General journal</span></span>                           |
| <span data-ttu-id="867f0-158">** **</span><span class="sxs-lookup"><span data-stu-id="867f0-158">** **</span></span>                               | <span data-ttu-id="867f0-159">Myyntireskontra</span><span class="sxs-lookup"><span data-stu-id="867f0-159">Accounts receivable</span></span>      | <span data-ttu-id="867f0-160">Vapaatekstilasku</span><span class="sxs-lookup"><span data-stu-id="867f0-160">Free text invoice</span></span>                         |



<span data-ttu-id="867f0-161">Lisätietoja on ohjeaiheessa [Käyttöomaisuuden integrointi](fixed-asset-integration.md).</span><span class="sxs-lookup"><span data-stu-id="867f0-161">For more information, see [Fixed assets integration](fixed-asset-integration.md).</span></span>




