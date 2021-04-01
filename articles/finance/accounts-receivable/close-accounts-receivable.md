---
title: Myyntireskontran sulkeminen
description: Seuraava ohjeaihe sisältää Myyntireskontra sulkeutuu -liiketoimintaprosessin osaa tukevien sivujen luettelon.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 59372
ms.assetid: c18d83e5-4adb-422a-91be-82a665d8288b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5beab66bcb64322d75e7a2ef1d1f40b13c35a06f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244530"
---
# <a name="close-accounts-receivable"></a><span data-ttu-id="4647b-103">Myyntireskontran sulkeminen</span><span class="sxs-lookup"><span data-stu-id="4647b-103">Close Accounts receivable</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4647b-104">Seuraava taulukko sisältää Myyntireskontra sulkeutuu -liiketoimintaprosessin osaa tukevien sivujen luettelon.</span><span class="sxs-lookup"><span data-stu-id="4647b-104">The following table lists the pages that support the close Accounts receivable business process.</span></span>

> [!NOTE] 
> <span data-ttu-id="4647b-105">Joidenkin seuraavan taulukon sivujen avaaminen edellyttää, että annat tietoja tai määrität parametriasetuksia.</span><span class="sxs-lookup"><span data-stu-id="4647b-105">To open some of the pages in the table, you must enter information or specify parameter settings.</span></span>

<span data-ttu-id="4647b-106">**Liiketoimintaprosessin osan tehtävä**</span><span class="sxs-lookup"><span data-stu-id="4647b-106">**Business process component task**</span></span>                   

<span data-ttu-id="4647b-107">Sulje jaksot kirjanpidossa</span><span class="sxs-lookup"><span data-stu-id="4647b-107">Close periods in the general ledger</span></span>

| <span data-ttu-id="4647b-108">Sivun nimi</span><span class="sxs-lookup"><span data-stu-id="4647b-108">Page name</span></span>                            | <span data-ttu-id="4647b-109">Käyttö</span><span class="sxs-lookup"><span data-stu-id="4647b-109">Usage</span></span>                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------|
|<span data-ttu-id="4647b-110">Erätyö</span><span class="sxs-lookup"><span data-stu-id="4647b-110">Batch job</span></span>                             | <span data-ttu-id="4647b-111">Tarkastele tai luo erätöitä.</span><span class="sxs-lookup"><span data-stu-id="4647b-111">View or create batch jobs.</span></span> <span data-ttu-id="4647b-112">Erätyöt eivät ehkä ole valmiita ja haluat varmistaa, että kaikki kirjaukset on tehty.</span><span class="sxs-lookup"><span data-stu-id="4647b-112">Batch jobs might not be completed, and you want to make sure that all posting is completed.</span></span>                                                                                                               |
|<span data-ttu-id="4647b-113">Vahvista myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="4647b-113">Confirm sales order</span></span>                   | <span data-ttu-id="4647b-114">Päivitä myyntitilauksia.</span><span class="sxs-lookup"><span data-stu-id="4647b-114">Update sales orders.</span></span>                                                                       |
|<span data-ttu-id="4647b-115">Ulkomaanvaluutan uudelleenarvostus</span><span class="sxs-lookup"><span data-stu-id="4647b-115">Foreign currency revaluation</span></span>          | <span data-ttu-id="4647b-116">Luo tapahtumia, jotka päivittävät sellaisten avointen asiakastapahtumien arvon, joissa on käytössä vieras valuutta.</span><span class="sxs-lookup"><span data-stu-id="4647b-116">Generate transactions that update the value of open customer transactions in foreign currencies.</span></span>                                                                                                                         |
| <span data-ttu-id="4647b-117">Kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="4647b-117">Journal</span></span>                              | <span data-ttu-id="4647b-118">Kirjaa laskuja, maksuja ja velkakirjoja.</span><span class="sxs-lookup"><span data-stu-id="4647b-118">Post invoices, payments, and promissory notes.</span></span>                                             |
| <span data-ttu-id="4647b-119">Kirjaustosite</span><span class="sxs-lookup"><span data-stu-id="4647b-119">Journal voucher</span></span>                      |<ul><li><span data-ttu-id="4647b-120">**Maksukirjauskansio**: Luo, käsittele ja kirjaa maksuja.</span><span class="sxs-lookup"><span data-stu-id="4647b-120">**Payment journal** – Generate, process, and post payments.</span></span></li><li><span data-ttu-id="4647b-121">**Aseta vekselikirjauskansio**: Kirjaa vekseleitä.</span><span class="sxs-lookup"><span data-stu-id="4647b-121">**Draw bill of exchange journal** – Post bills of exchange.</span></span></li><li><span data-ttu-id="4647b-122">**Protestoi vekselikirjauskansio**: Kirjaa protestoituja vekseleitä.</span><span class="sxs-lookup"><span data-stu-id="4647b-122">**Protest bill of exchange journal** – Post protested bills of exchange.</span></span></li><li><span data-ttu-id="4647b-123">**Tarkista vekselikirjauskansio**: Kirjaa tarkistettuja vekseleitä.</span><span class="sxs-lookup"><span data-stu-id="4647b-123">**Redraw bill of exchange journal** – Post redrawn bills of exchange.</span></span></li><li><span data-ttu-id="4647b-124">**Maksusuoritusten kirjauskansio**: Kirjaa maksusuorituksia.</span><span class="sxs-lookup"><span data-stu-id="4647b-124">**Remittance journal** – Post remittances.</span></span></li><li><span data-ttu-id="4647b-125">**Selvitä vekselikirjauskansio**: Kirjaa selvitettyjä vekseleitä</span><span class="sxs-lookup"><span data-stu-id="4647b-125">**Settle bill of exchange journal** – Post settled bills of exchange</span></span></li></ul>                   |
| <span data-ttu-id="4647b-126">Pakkausluettelon kirjaus</span><span class="sxs-lookup"><span data-stu-id="4647b-126">Packing slip posting</span></span>                 | <span data-ttu-id="4647b-127">Päivitä myyntitilausten pakkausluetteloita.</span><span class="sxs-lookup"><span data-stu-id="4647b-127">Update packing slips for sales orders.</span></span>                                                     |
| <span data-ttu-id="4647b-128">Kirjaa vapaatekstilasku</span><span class="sxs-lookup"><span data-stu-id="4647b-128">Post free text invoice</span></span>               | <span data-ttu-id="4647b-129">Kirjaa vapaatekstilaskuja.</span><span class="sxs-lookup"><span data-stu-id="4647b-129">Post free text invoices.</span></span>                                                                   |
| <span data-ttu-id="4647b-130">Laskun kirjaus</span><span class="sxs-lookup"><span data-stu-id="4647b-130">Posting invoice</span></span>                      | <span data-ttu-id="4647b-131">Kirjaa myyntitilausten laskuja.</span><span class="sxs-lookup"><span data-stu-id="4647b-131">Post invoices for sales orders.</span></span>                                                            |
| <span data-ttu-id="4647b-132">Keräysluettelon kirjaus</span><span class="sxs-lookup"><span data-stu-id="4647b-132">Posting picking list</span></span>                 |<span data-ttu-id="4647b-133">Päivitä myyntitilausten keräysluetteloita.</span><span class="sxs-lookup"><span data-stu-id="4647b-133">Update picking lists for sales orders.</span></span>                                                      |

<span data-ttu-id="4647b-134">**Liiketoimintaprosessin osan tehtävä**</span><span class="sxs-lookup"><span data-stu-id="4647b-134">**Business process component task**</span></span>   

<span data-ttu-id="4647b-135">EU-myyntiluettelon luominen ja lähettäminen</span><span class="sxs-lookup"><span data-stu-id="4647b-135">Create and submit the EU sales list</span></span>

| <span data-ttu-id="4647b-136">Sivun nimi</span><span class="sxs-lookup"><span data-stu-id="4647b-136">Page name</span></span>                            | <span data-ttu-id="4647b-137">Käyttö</span><span class="sxs-lookup"><span data-stu-id="4647b-137">Usage</span></span>                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------|
|<span data-ttu-id="4647b-138">EU-myyntiluettelo</span><span class="sxs-lookup"><span data-stu-id="4647b-138">EU sales list</span></span>                         | <span data-ttu-id="4647b-139">Euroopan unionin (EU) myynnin ilmoittaminen veroviranomaiselle arvonlisäveron ilmoittamista varten.</span><span class="sxs-lookup"><span data-stu-id="4647b-139">Report on European Union (EU) sales to the tax authority for value-added tax (VAT) declaration purposes.</span></span>                                                                                                                           |








[!INCLUDE[footer-include](../../includes/footer-banner.md)]