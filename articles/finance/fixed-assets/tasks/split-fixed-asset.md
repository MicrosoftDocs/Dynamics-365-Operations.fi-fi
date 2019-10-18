---
title: Käyttöomaisuuserän jakaminen
description: Tässä aiheessa kerrotaan miten jaetaan yhden käyttöomaisuuskirjan prosenttiosuus uuteen käyttöomaisuuskirjaan.
author: saraschi2
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4e001a6fdf390c6211ba85aa327b60dcdf16d9e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177505"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="d5d17-103">Käyttöomaisuuserän jakaminen</span><span class="sxs-lookup"><span data-stu-id="d5d17-103">Split a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d5d17-104">Tässä aiheessa kerrotaan miten jaetaan yhden käyttöomaisuuskirjan prosenttiosuus uuteen käyttöomaisuuskirjaan.</span><span class="sxs-lookup"><span data-stu-id="d5d17-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="d5d17-105">Käytössä ovat kirjanpitäjän rooli ja USMF:n esittelytiedot.</span><span class="sxs-lookup"><span data-stu-id="d5d17-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="d5d17-106">Luo uusi käyttöomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="d5d17-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="d5d17-107">Siirry siirtymisruudussa kohtaan **Moduulit > Käyttöomaisuuserät > Käyttöomaisuuserät > Käyttöomaisuuserät**.</span><span class="sxs-lookup"><span data-stu-id="d5d17-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="d5d17-108">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="d5d17-108">Select **New**.</span></span>
3. <span data-ttu-id="d5d17-109">Syötä tai valitse arvo **Käyttöomaisuusryhmä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="d5d17-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="d5d17-110">Huomaa, että käyttöomaisuusnumeroa käytetään jakoprosessissa myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="d5d17-110">Note the fixed asset number to use in the split process later.</span></span>  
4. <span data-ttu-id="d5d17-111">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="d5d17-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="d5d17-112">Sulje lomake.</span><span class="sxs-lookup"><span data-stu-id="d5d17-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="d5d17-113">Käyttöomaisuuserän jakaminen</span><span class="sxs-lookup"><span data-stu-id="d5d17-113">Split a fixed asset</span></span>
1. <span data-ttu-id="d5d17-114">Etsi ja valitse luettelosta jaettavan käyttöomaisuuden linkki.</span><span class="sxs-lookup"><span data-stu-id="d5d17-114">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="d5d17-115">Valitse **Kirjat**.</span><span class="sxs-lookup"><span data-stu-id="d5d17-115">Select **Books**.</span></span> <span data-ttu-id="d5d17-116">Valitse kirja, joka jaetaan uudeksi käyttöomaisuuseräksi.</span><span class="sxs-lookup"><span data-stu-id="d5d17-116">Select the book to split to the new asset.</span></span>  
3. <span data-ttu-id="d5d17-117">Valitse **Toiminnot**.</span><span class="sxs-lookup"><span data-stu-id="d5d17-117">Select **Functions**.</span></span>
4. <span data-ttu-id="d5d17-118">Valitse **Jaa käyttöomaisuus**.</span><span class="sxs-lookup"><span data-stu-id="d5d17-118">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="d5d17-119">Syötä tai valitse arvo **Käyttöomaisuuserään**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="d5d17-119">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="d5d17-120">Avaa haku napsauttamalla **Kirjaan**-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="d5d17-120">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="d5d17-121">Syötä **Tapahtumapäivä**-kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="d5d17-121">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="d5d17-122">Kirjoita numero **Prosentti**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="d5d17-122">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="d5d17-123">Syötä tai valitse arvo **Kirjauskansion nimi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="d5d17-123">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="d5d17-124">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="d5d17-124">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="d5d17-125">Kirjauskansiotapahtuman kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="d5d17-125">Post the journal transaction</span></span>
1. <span data-ttu-id="d5d17-126">Siirry siirtymisruudussa kohtaan **Moduulit > Käyttöomaisuuserät > Kirjauskansioviennit > Käyttöomaisuuden kirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="d5d17-126">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="d5d17-127">Valitse luettelosta jakoprosessissa luotu kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="d5d17-127">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="d5d17-128">Valitse **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="d5d17-128">Select **Lines**.</span></span>

    - <span data-ttu-id="d5d17-129">Tarkista luodut kirjauskansiorivit.</span><span class="sxs-lookup"><span data-stu-id="d5d17-129">Verify the journal lines created.</span></span>  
    - <span data-ttu-id="d5d17-130">Alkuperäisen käyttöomaisuuserän hankinnan oikaisutapahtuma luodaan, kun arvoa halutaan nostaa määritetyn prosenttiosuuden verran jakoprosentin aikana.</span><span class="sxs-lookup"><span data-stu-id="d5d17-130">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  
    - <span data-ttu-id="d5d17-131">Uudelle käyttöomaisuuserälle luodaan hankintatapahtuma samalle summalle.</span><span class="sxs-lookup"><span data-stu-id="d5d17-131">An Acquisition transaction is created for the new asset for the same amount.</span></span>  

4. <span data-ttu-id="d5d17-132">Valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="d5d17-132">Select **Post**.</span></span>

