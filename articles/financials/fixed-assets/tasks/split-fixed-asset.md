---
title: Jaa käyttöomaisuuserä
description: Tässä tehtävän ohjauksessa jaetaan yhden käyttöomaisuuskirjan prosenttiosuus uuteen käyttöomaisuuskirjaan.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6be9de64265a4d7b5c91af3ee8acfce80c78e0f1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "333366"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="1a917-103">Jaa käyttöomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="1a917-103">Split a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1a917-104">Tässä tehtävän ohjauksessa jaetaan yhden käyttöomaisuuskirjan prosenttiosuus uuteen käyttöomaisuuskirjaan.</span><span class="sxs-lookup"><span data-stu-id="1a917-104">This task guide will split a percentage of one asset book to a new asset book.</span></span>  <span data-ttu-id="1a917-105">Käytössä ovat kirjanpitäjän rooli ja USMF:n esittelytiedot.</span><span class="sxs-lookup"><span data-stu-id="1a917-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="1a917-106">Luo uusi käyttöomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="1a917-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="1a917-107">Siirry kohtaan Käyttöomaisuudet > Käyttöomaisuudet > Käyttöomaisuudet.</span><span class="sxs-lookup"><span data-stu-id="1a917-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="1a917-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="1a917-108">Click New.</span></span>
3. <span data-ttu-id="1a917-109">Syötä tai valitse arvo Käyttöomaisuusryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="1a917-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="1a917-110">Huomaa, että käyttöomaisuusnumeroa käytetään jakoprosessissa myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="1a917-110">Note the fixed asset number to use in the split process later.</span></span>
5. <span data-ttu-id="1a917-111">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1a917-111">In the Name field, type a value.</span></span>
6. <span data-ttu-id="1a917-112">Sulje lomake.</span><span class="sxs-lookup"><span data-stu-id="1a917-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="1a917-113">Jaa käyttöomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="1a917-113">Split a fixed asset</span></span>
1. <span data-ttu-id="1a917-114">Etsi ja valitse luettelosta jaettava käyttöomaisuus.</span><span class="sxs-lookup"><span data-stu-id="1a917-114">In the list, find and select the fixed asset to split.</span></span>
2. <span data-ttu-id="1a917-115">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="1a917-115">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="1a917-116">Valitse Kirjat.</span><span class="sxs-lookup"><span data-stu-id="1a917-116">Click Books.</span></span>
    * <span data-ttu-id="1a917-117">Valitse kirja, joka jaetaan uudeksi käyttöomaisuuseräksi.</span><span class="sxs-lookup"><span data-stu-id="1a917-117">Select the book to split to the new asset.</span></span>  
4. <span data-ttu-id="1a917-118">Valitse Toiminnot.</span><span class="sxs-lookup"><span data-stu-id="1a917-118">Click Functions.</span></span>
5. <span data-ttu-id="1a917-119">Valitse Jaa käyttöomaisuus.</span><span class="sxs-lookup"><span data-stu-id="1a917-119">Click Split fixed asset.</span></span>
6. <span data-ttu-id="1a917-120">Syötä tai valitse arvo Käyttöomaisuuserään-kentässä.</span><span class="sxs-lookup"><span data-stu-id="1a917-120">In the To fixed asset field, enter or select a value.</span></span>
7. <span data-ttu-id="1a917-121">Avaa haku napsauttamalla Kirjaan-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="1a917-121">In the To book field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="1a917-122">Syötä Tapahtumapäivä-kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="1a917-122">In the Transaction date field, enter a date.</span></span>
9. <span data-ttu-id="1a917-123">Kirjoita numero Prosentti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1a917-123">In the Percent field, enter a number.</span></span>
10. <span data-ttu-id="1a917-124">Syötä tai valitse arvo Kirjauskansion nimi -kentässä.</span><span class="sxs-lookup"><span data-stu-id="1a917-124">In the Journal name field, enter or select a value.</span></span>
11. <span data-ttu-id="1a917-125">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1a917-125">Click OK.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="1a917-126">Kirjauskansiotapahtuman kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="1a917-126">Post the journal transaction</span></span>
1. <span data-ttu-id="1a917-127">Valitse Käyttöomaisuus > Kirjauskansioviennit > Käyttöomaisuuden kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="1a917-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="1a917-128">Valitse luettelosta jakoprosessissa luotu kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="1a917-128">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="1a917-129">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="1a917-129">Click Lines.</span></span>
    * <span data-ttu-id="1a917-130">Tarkista luodut kirjauskansiorivit.</span><span class="sxs-lookup"><span data-stu-id="1a917-130">Verify the journal lines created.</span></span>  <span data-ttu-id="1a917-131">Alkuperäisen käyttöomaisuuserän hankinnan oikaisutapahtuma luodaan, kun arvoa halutaan nostaa määritetyn prosenttiosuuden verran jakoprosentin aikana.</span><span class="sxs-lookup"><span data-stu-id="1a917-131">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  <span data-ttu-id="1a917-132">Uudelle käyttöomaisuuserälle luodaan hankintatapahtuma samalle summalle.</span><span class="sxs-lookup"><span data-stu-id="1a917-132">An Acquisition transaction is created for the new asset for the same amount.</span></span>  
4. <span data-ttu-id="1a917-133">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="1a917-133">Click Post.</span></span>

