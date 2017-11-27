---
title: Myyntireskontran sulkeminen
description: "Seuraava ohjeaihe sisältää Myyntireskontra sulkeutuu -liiketoimintaprosessin osaa tukevien sivujen luettelon."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 59372
ms.assetid: c18d83e5-4adb-422a-91be-82a665d8288b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8532b778c89c972a833ac9ffe28243f15f01426c
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="close-accounts-receivable"></a><span data-ttu-id="a4812-103">Myyntireskontran sulkeminen</span><span class="sxs-lookup"><span data-stu-id="a4812-103">Close Accounts receivable</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="a4812-104">Seuraava taulukko sisältää Myyntireskontra sulkeutuu -liiketoimintaprosessin osaa tukevien sivujen luettelon.</span><span class="sxs-lookup"><span data-stu-id="a4812-104">The following table lists the pages that support the close Accounts receivable business process.</span></span>

> [!NOTE] 
> <span data-ttu-id="a4812-105">Joidenkin seuraavan taulukon sivujen avaaminen edellyttää, että annat tietoja tai määrität parametriasetuksia.</span><span class="sxs-lookup"><span data-stu-id="a4812-105">To open some of the pages in the table, you must enter information or specify parameter settings.</span></span>

<span data-ttu-id="a4812-106">**Liiketoimintaprosessin osan tehtävä**</span><span class="sxs-lookup"><span data-stu-id="a4812-106">**Business process component task**</span></span>                   

<span data-ttu-id="a4812-107">Sulje jaksot kirjanpidossa</span><span class="sxs-lookup"><span data-stu-id="a4812-107">Close periods in the general ledger</span></span>

| <span data-ttu-id="a4812-108">Sivun nimi</span><span class="sxs-lookup"><span data-stu-id="a4812-108">Page name</span></span>                            | <span data-ttu-id="a4812-109">Käyttö</span><span class="sxs-lookup"><span data-stu-id="a4812-109">Usage</span></span>                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------|
|<span data-ttu-id="a4812-110">Erätyö</span><span class="sxs-lookup"><span data-stu-id="a4812-110">Batch job</span></span>                             | <span data-ttu-id="a4812-111">Tarkastele tai luo erätöitä.</span><span class="sxs-lookup"><span data-stu-id="a4812-111">View or create batch jobs.</span></span> <span data-ttu-id="a4812-112">Erätyöt eivät ehkä ole valmiita ja haluat varmistaa, että kaikki kirjaukset on tehty.</span><span class="sxs-lookup"><span data-stu-id="a4812-112">Batch jobs might not be completed, and you want to make sure that all posting is completed.</span></span>                                                                                                               |
|<span data-ttu-id="a4812-113">Vahvista myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="a4812-113">Confirm sales order</span></span>                   | <span data-ttu-id="a4812-114">Päivitä myyntitilauksia.</span><span class="sxs-lookup"><span data-stu-id="a4812-114">Update sales orders.</span></span>                                                                       |
|<span data-ttu-id="a4812-115">Ulkomaanvaluutan uudelleenarvostus</span><span class="sxs-lookup"><span data-stu-id="a4812-115">Foreign currency revaluation</span></span>          | <span data-ttu-id="a4812-116">Luo tapahtumia, jotka päivittävät sellaisten avointen asiakastapahtumien arvon, joissa on käytössä vieras valuutta.</span><span class="sxs-lookup"><span data-stu-id="a4812-116">Generate transactions that update the value of open customer transactions in foreign currencies.</span></span>                                                                                                                         |
| <span data-ttu-id="a4812-117">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="a4812-117">Journal</span></span>                              | <span data-ttu-id="a4812-118">Kirjaa laskuja, maksuja ja velkakirjoja.</span><span class="sxs-lookup"><span data-stu-id="a4812-118">Post invoices, payments, and promissory notes.</span></span>                                             |
| <span data-ttu-id="a4812-119">Kirjaustosite</span><span class="sxs-lookup"><span data-stu-id="a4812-119">Journal voucher</span></span>                      |<ul><li><span data-ttu-id="a4812-120">**Maksukirjauskansio**: Luo, käsittele ja kirjaa maksuja.</span><span class="sxs-lookup"><span data-stu-id="a4812-120">**Payment journal** – Generate, process, and post payments.</span></span></li><li><span data-ttu-id="a4812-121">**Aseta vekselikirjauskansio**: Kirjaa vekseleitä.</span><span class="sxs-lookup"><span data-stu-id="a4812-121">**Draw bill of exchange journal** – Post bills of exchange.</span></span></li><li><span data-ttu-id="a4812-122">**Protestoi vekselikirjauskansio**: Kirjaa protestoituja vekseleitä.</span><span class="sxs-lookup"><span data-stu-id="a4812-122">**Protest bill of exchange journal** – Post protested bills of exchange.</span></span></li><li><span data-ttu-id="a4812-123">**Tarkista vekselikirjauskansio**: Kirjaa tarkistettuja vekseleitä.</span><span class="sxs-lookup"><span data-stu-id="a4812-123">**Redraw bill of exchange journal** – Post redrawn bills of exchange.</span></span></li><li><span data-ttu-id="a4812-124">**Maksusuoritusten kirjauskansio**: Kirjaa maksusuorituksia.</span><span class="sxs-lookup"><span data-stu-id="a4812-124">**Remittance journal** – Post remittances.</span></span></li><li><span data-ttu-id="a4812-125">**Selvitä vekselikirjauskansio**: Kirjaa selvitettyjä vekseleitä</span><span class="sxs-lookup"><span data-stu-id="a4812-125">**Settle bill of exchange journal** – Post settled bills of exchange</span></span></li></ul>                   |
| <span data-ttu-id="a4812-126">Pakkausluettelon kirjaus</span><span class="sxs-lookup"><span data-stu-id="a4812-126">Packing slip posting</span></span>                 | <span data-ttu-id="a4812-127">Päivitä myyntitilausten pakkausluetteloita.</span><span class="sxs-lookup"><span data-stu-id="a4812-127">Update packing slips for sales orders.</span></span>                                                     |
| <span data-ttu-id="a4812-128">Kirjaa vapaatekstilasku</span><span class="sxs-lookup"><span data-stu-id="a4812-128">Post free text invoice</span></span>               | <span data-ttu-id="a4812-129">Kirjaa vapaatekstilaskuja.</span><span class="sxs-lookup"><span data-stu-id="a4812-129">Post free text invoices.</span></span>                                                                   |
| <span data-ttu-id="a4812-130">Laskun kirjaus</span><span class="sxs-lookup"><span data-stu-id="a4812-130">Posting invoice</span></span>                      | <span data-ttu-id="a4812-131">Kirjaa myyntitilausten laskuja.</span><span class="sxs-lookup"><span data-stu-id="a4812-131">Post invoices for sales orders.</span></span>                                                            |
| <span data-ttu-id="a4812-132">Keräysluettelon kirjaus</span><span class="sxs-lookup"><span data-stu-id="a4812-132">Posting picking list</span></span>                 |<span data-ttu-id="a4812-133">Päivitä myyntitilausten keräysluetteloita.</span><span class="sxs-lookup"><span data-stu-id="a4812-133">Update picking lists for sales orders.</span></span>                                                      |

<span data-ttu-id="a4812-134">**Liiketoimintaprosessin osan tehtävä**</span><span class="sxs-lookup"><span data-stu-id="a4812-134">**Business process component task**</span></span>   

<span data-ttu-id="a4812-135">EU-myyntiluettelon luominen ja lähettäminen</span><span class="sxs-lookup"><span data-stu-id="a4812-135">Create and submit the EU sales list</span></span>

| <span data-ttu-id="a4812-136">Sivun nimi</span><span class="sxs-lookup"><span data-stu-id="a4812-136">Page name</span></span>                            | <span data-ttu-id="a4812-137">Käyttö</span><span class="sxs-lookup"><span data-stu-id="a4812-137">Usage</span></span>                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------|
|<span data-ttu-id="a4812-138">EU-myyntiluettelo</span><span class="sxs-lookup"><span data-stu-id="a4812-138">EU sales list</span></span>                         | <span data-ttu-id="a4812-139">Euroopan unionin (EU) myynnin ilmoittaminen veroviranomaiselle arvonlisäveron ilmoittamista varten.</span><span class="sxs-lookup"><span data-stu-id="a4812-139">Report on European Union (EU) sales to the tax authority for value-added tax (VAT) declaration purposes.</span></span>                                                                                                                           |







