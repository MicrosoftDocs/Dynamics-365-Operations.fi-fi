--- 
title: "Jaa käyttöomaisuuserä"
description: "Tässä tehtävän ohjauksessa jaetaan yhden käyttöomaisuuskirjan prosenttiosuus uuteen käyttöomaisuuskirjaan."
author: saraschi2
manager: AnnBe
ms.date: 10/19/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b4c1b39bcae1fa3830f3a217d1ad89e84cd72134
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="545ad-103">Jaa käyttöomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="545ad-103">Split a fixed asset</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="545ad-104">Tässä tehtävän ohjauksessa jaetaan yhden käyttöomaisuuskirjan prosenttiosuus uuteen käyttöomaisuuskirjaan.</span><span class="sxs-lookup"><span data-stu-id="545ad-104">This task guide will split a percentage of one asset book to a new asset book.</span></span>  <span data-ttu-id="545ad-105">Käytössä ovat kirjanpitäjän rooli ja USMF:n esittelytiedot.</span><span class="sxs-lookup"><span data-stu-id="545ad-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="545ad-106">Luo uusi käyttöomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="545ad-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="545ad-107">Siirry kohtaan Käyttöomaisuudet > Käyttöomaisuudet > Käyttöomaisuudet.</span><span class="sxs-lookup"><span data-stu-id="545ad-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="545ad-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="545ad-108">Click New.</span></span>
3. <span data-ttu-id="545ad-109">Syötä tai valitse arvo Käyttöomaisuusryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="545ad-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="545ad-110">Huomaa, että käyttöomaisuusnumeroa käytetään jakoprosessissa myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="545ad-110">Note the fixed asset number to use in the split process later.</span></span>
5. <span data-ttu-id="545ad-111">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="545ad-111">In the Name field, type a value.</span></span>
6. <span data-ttu-id="545ad-112">Sulje lomake.</span><span class="sxs-lookup"><span data-stu-id="545ad-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="545ad-113">Jaa käyttöomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="545ad-113">Split a fixed asset</span></span>
1. <span data-ttu-id="545ad-114">Etsi ja valitse luettelosta jaettava käyttöomaisuus.</span><span class="sxs-lookup"><span data-stu-id="545ad-114">In the list, find and select the fixed asset to split.</span></span>
2. <span data-ttu-id="545ad-115">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="545ad-115">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="545ad-116">Valitse Kirjat.</span><span class="sxs-lookup"><span data-stu-id="545ad-116">Click Books.</span></span>
    * <span data-ttu-id="545ad-117">Valitse kirja, joka jaetaan uudeksi käyttöomaisuuseräksi.</span><span class="sxs-lookup"><span data-stu-id="545ad-117">Select the book to split to the new asset.</span></span>  
4. <span data-ttu-id="545ad-118">Valitse Toiminnot.</span><span class="sxs-lookup"><span data-stu-id="545ad-118">Click Functions.</span></span>
5. <span data-ttu-id="545ad-119">Valitse Jaa käyttöomaisuus.</span><span class="sxs-lookup"><span data-stu-id="545ad-119">Click Split fixed asset.</span></span>
6. <span data-ttu-id="545ad-120">Syötä tai valitse arvo Käyttöomaisuuserään-kentässä.</span><span class="sxs-lookup"><span data-stu-id="545ad-120">In the To fixed asset field, enter or select a value.</span></span>
7. <span data-ttu-id="545ad-121">Avaa haku napsauttamalla Kirjaan-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="545ad-121">In the To book field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="545ad-122">Syötä Tapahtumapäivä-kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="545ad-122">In the Transaction date field, enter a date.</span></span>
9. <span data-ttu-id="545ad-123">Kirjoita numero Prosentti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="545ad-123">In the Percent field, enter a number.</span></span>
10. <span data-ttu-id="545ad-124">Syötä tai valitse arvo Kirjauskansion nimi -kentässä.</span><span class="sxs-lookup"><span data-stu-id="545ad-124">In the Journal name field, enter or select a value.</span></span>
11. <span data-ttu-id="545ad-125">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="545ad-125">Click OK.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="545ad-126">Kirjauskansiotapahtuman kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="545ad-126">Post the journal transaction</span></span>
1. <span data-ttu-id="545ad-127">Valitse Käyttöomaisuus > Kirjauskansioviennit > Käyttöomaisuuden kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="545ad-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="545ad-128">Valitse luettelosta jakoprosessissa luotu kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="545ad-128">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="545ad-129">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="545ad-129">Click Lines.</span></span>
    * <span data-ttu-id="545ad-130">Tarkista luodut kirjauskansiorivit.</span><span class="sxs-lookup"><span data-stu-id="545ad-130">Verify the journal lines created.</span></span>  <span data-ttu-id="545ad-131">Alkuperäisen käyttöomaisuuserän hankinnan oikaisutapahtuma luodaan, kun arvoa halutaan nostaa määritetyn prosenttiosuuden verran jakoprosentin aikana.</span><span class="sxs-lookup"><span data-stu-id="545ad-131">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  <span data-ttu-id="545ad-132">Uudelle käyttöomaisuuserälle luodaan hankintatapahtuma samalle summalle.</span><span class="sxs-lookup"><span data-stu-id="545ad-132">An Acquisition transaction is created for the new asset for the same amount.</span></span>  
4. <span data-ttu-id="545ad-133">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="545ad-133">Click Post.</span></span>


