---
title: Myyntireskontran sulkeminen
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 59372
ms.assetid: c18d83e5-4adb-422a-91be-82a665d8288b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2b2e827df0c679855af9624f8a2fb36cb23f359a
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="close-accounts-receivable"></a><span data-ttu-id="ebca6-102">Myyntireskontran sulkeminen</span><span class="sxs-lookup"><span data-stu-id="ebca6-102">Close Accounts receivable</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="ebca6-103">Seuraava taulukko sisältää Myyntireskontra sulkeutuu -liiketoimintaprosessin osaa tukevien sivujen luettelon.</span><span class="sxs-lookup"><span data-stu-id="ebca6-103">The following table lists the pages that support the close Accounts receivable business process.</span></span>

> [!NOTE] 
> <span data-ttu-id="ebca6-104">Joidenkin seuraavan taulukon sivujen avaaminen edellyttää, että annat tietoja tai määrität parametriasetuksia.</span><span class="sxs-lookup"><span data-stu-id="ebca6-104">To open some of the pages in the table, you must enter information or specify parameter settings.</span></span>

<span data-ttu-id="ebca6-105">**Liiketoimintaprosessin osan tehtävä**</span><span class="sxs-lookup"><span data-stu-id="ebca6-105">**Business process component task**</span></span>                   

<span data-ttu-id="ebca6-106">Sulje jaksot kirjanpidossa</span><span class="sxs-lookup"><span data-stu-id="ebca6-106">Close periods in the general ledger</span></span>

| <span data-ttu-id="ebca6-107">Sivun nimi</span><span class="sxs-lookup"><span data-stu-id="ebca6-107">Page name</span></span>                            | <span data-ttu-id="ebca6-108">Käyttö</span><span class="sxs-lookup"><span data-stu-id="ebca6-108">Usage</span></span>                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------|
|<span data-ttu-id="ebca6-109">Erätyö</span><span class="sxs-lookup"><span data-stu-id="ebca6-109">Batch job</span></span>                             | <span data-ttu-id="ebca6-110">Tarkastele tai luo erätöitä.</span><span class="sxs-lookup"><span data-stu-id="ebca6-110">View or create batch jobs.</span></span> <span data-ttu-id="ebca6-111">Erätyöt eivät ehkä ole valmiita ja haluat varmistaa, että kaikki kirjaukset on tehty.</span><span class="sxs-lookup"><span data-stu-id="ebca6-111">Batch jobs might not be completed, and you want make sure that all posting is completed.</span></span>                                                                                                               |
|<span data-ttu-id="ebca6-112">Vahvista myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="ebca6-112">Confirm sales order</span></span>                   | <span data-ttu-id="ebca6-113">Päivitä myyntitilauksia.</span><span class="sxs-lookup"><span data-stu-id="ebca6-113">Update sales orders.</span></span>                                                                       |
|<span data-ttu-id="ebca6-114">Ulkomaanvaluutan uudelleenarvostus</span><span class="sxs-lookup"><span data-stu-id="ebca6-114">Foreign currency revaluation</span></span>          | <span data-ttu-id="ebca6-115">Luo tapahtumia, jotka päivittävät sellaisten avointen asiakastapahtumien arvon, joissa on käytössä vieras valuutta.</span><span class="sxs-lookup"><span data-stu-id="ebca6-115">Generate transactions that update the value of open customer transactions in foreign currencies.</span></span>                                                                                                                         |
| <span data-ttu-id="ebca6-116">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="ebca6-116">Journal</span></span>                              | <span data-ttu-id="ebca6-117">Kirjaa laskuja, maksuja ja velkakirjoja.</span><span class="sxs-lookup"><span data-stu-id="ebca6-117">Post invoices, payments, and promissory notes.</span></span>                                             |
| <span data-ttu-id="ebca6-118">Kirjaustosite</span><span class="sxs-lookup"><span data-stu-id="ebca6-118">Journal voucher</span></span>                      |<ul><li><span data-ttu-id="ebca6-119">**Maksukirjauskansio**: Luo, käsittele ja kirjaa maksuja.</span><span class="sxs-lookup"><span data-stu-id="ebca6-119">**Payment journal** – Generate, process, and post payments.</span></span></li><li><span data-ttu-id="ebca6-120">**Aseta vekselikirjauskansio**: Kirjaa vekseleitä.</span><span class="sxs-lookup"><span data-stu-id="ebca6-120">**Draw bill of exchange journal** – Post bills of exchange.</span></span></li><li><span data-ttu-id="ebca6-121">**Protestoi vekselikirjauskansio**: Kirjaa protestoituja vekseleitä.</span><span class="sxs-lookup"><span data-stu-id="ebca6-121">**Protest bill of exchange journal** – Post protested bills of exchange.</span></span></li><li><span data-ttu-id="ebca6-122">**Tarkista vekselikirjauskansio**: Kirjaa tarkistettuja vekseleitä.</span><span class="sxs-lookup"><span data-stu-id="ebca6-122">**Redraw bill of exchange journal** – Post redrawn bills of exchange.</span></span></li><li><span data-ttu-id="ebca6-123">**Maksusuoritusten kirjauskansio**: Kirjaa maksusuorituksia.</span><span class="sxs-lookup"><span data-stu-id="ebca6-123">**Remittance journal** – Post remittances.</span></span></li><li><span data-ttu-id="ebca6-124">**Selvitä vekselikirjauskansio**: Kirjaa selvitettyjä vekseleitä</span><span class="sxs-lookup"><span data-stu-id="ebca6-124">**Settle bill of exchange journal** – Post settled bills of exchange</span></span></li></ul>                   |
| <span data-ttu-id="ebca6-125">Pakkausluettelon kirjaus</span><span class="sxs-lookup"><span data-stu-id="ebca6-125">Packing slip posting</span></span>                 | <span data-ttu-id="ebca6-126">Päivitä myyntitilausten pakkausluetteloita.</span><span class="sxs-lookup"><span data-stu-id="ebca6-126">Update packing slips for sales orders.</span></span>                                                     |
| <span data-ttu-id="ebca6-127">Kirjaa vapaatekstilasku</span><span class="sxs-lookup"><span data-stu-id="ebca6-127">Post free text invoice</span></span>               | <span data-ttu-id="ebca6-128">Kirjaa vapaatekstilaskuja.</span><span class="sxs-lookup"><span data-stu-id="ebca6-128">Post free text invoices.</span></span>                                                                   |
| <span data-ttu-id="ebca6-129">Laskun kirjaus</span><span class="sxs-lookup"><span data-stu-id="ebca6-129">Posting invoice</span></span>                      | <span data-ttu-id="ebca6-130">Kirjaa myyntitilausten laskuja.</span><span class="sxs-lookup"><span data-stu-id="ebca6-130">Post invoices for sales orders.</span></span>                                                            |
| <span data-ttu-id="ebca6-131">Keräysluettelon kirjaus</span><span class="sxs-lookup"><span data-stu-id="ebca6-131">Posting picking list</span></span>                 |<span data-ttu-id="ebca6-132">Päivitä myyntitilausten keräysluetteloita.</span><span class="sxs-lookup"><span data-stu-id="ebca6-132">Update picking lists for sales orders.</span></span>                                                      |

<span data-ttu-id="ebca6-133">**Liiketoimintaprosessin osan tehtävä**</span><span class="sxs-lookup"><span data-stu-id="ebca6-133">**Business process component task**</span></span>   

<span data-ttu-id="ebca6-134">EU-myyntiluettelon luominen ja lähettäminen</span><span class="sxs-lookup"><span data-stu-id="ebca6-134">Create and submit the EU sales list</span></span>

| <span data-ttu-id="ebca6-135">Sivun nimi</span><span class="sxs-lookup"><span data-stu-id="ebca6-135">Page name</span></span>                            | <span data-ttu-id="ebca6-136">Käyttö</span><span class="sxs-lookup"><span data-stu-id="ebca6-136">Usage</span></span>                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------|
|<span data-ttu-id="ebca6-137">EU-myyntiluettelo</span><span class="sxs-lookup"><span data-stu-id="ebca6-137">EU sales list</span></span>                         | <span data-ttu-id="ebca6-138">Euroopan unionin (EU) myynnin ilmoittaminen veroviranomaiselle arvonlisäveron ilmoittamista varten.</span><span class="sxs-lookup"><span data-stu-id="ebca6-138">Report on European Union (EU) sales to the tax authority for value-added tax (VAT) declaration purposes.</span></span>                                                                                                                           |







