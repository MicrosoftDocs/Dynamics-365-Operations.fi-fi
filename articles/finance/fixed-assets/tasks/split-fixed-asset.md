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
ms.openlocfilehash: 40703622bc8c7a21451d31e7606596c5edbe90f7
ms.sourcegitcommit: 51e626675b0130fa32a84ce2d9119b68ea928018
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4000290"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="7ef59-103">Käyttöomaisuuserän jakaminen</span><span class="sxs-lookup"><span data-stu-id="7ef59-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7ef59-104">Tässä aiheessa kerrotaan miten jaetaan yhden käyttöomaisuuskirjan prosenttiosuus uuteen käyttöomaisuuskirjaan.</span><span class="sxs-lookup"><span data-stu-id="7ef59-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="7ef59-105">Käytössä ovat kirjanpitäjän rooli ja USMF:n esittelytiedot.</span><span class="sxs-lookup"><span data-stu-id="7ef59-105">It uses the Accountant role and USMF demo data.</span></span>

## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="7ef59-106">Luo uusi käyttöomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="7ef59-106">Create a new fixed asset</span></span>

1. <span data-ttu-id="7ef59-107">Valitse siirtymisruudussa **Moduulit \> Käyttöomaisuuserät \> Käyttöomaisuuserät \> Käyttöomaisuuserät**.</span><span class="sxs-lookup"><span data-stu-id="7ef59-107">In the navigation pane, go to **Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="7ef59-108">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="7ef59-108">Select **New**.</span></span>
3. <span data-ttu-id="7ef59-109">Syötä tai valitse arvo **Käyttöomaisuusryhmä** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="7ef59-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="7ef59-110">Huomaa, että käyttöomaisuusnumeroa käytetään jakoprosessissa myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="7ef59-110">Note the fixed asset number to use in the split process later.</span></span>
4. <span data-ttu-id="7ef59-111">Anna **Nimi** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="7ef59-111">In the **Name** field, enter a value.</span></span>
5. <span data-ttu-id="7ef59-112">Sulje lomake.</span><span class="sxs-lookup"><span data-stu-id="7ef59-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="7ef59-113">Käyttöomaisuuserän jakaminen</span><span class="sxs-lookup"><span data-stu-id="7ef59-113">Split a fixed asset</span></span>

<span data-ttu-id="7ef59-114">Ennen kokonaan poistetun käyttöomaisuuden jakamista käyttöomaisuuskirjan tila **Suljettu** on vaihdettava manuaalisesti tilaan **Avoin**.</span><span class="sxs-lookup"><span data-stu-id="7ef59-114">Before a fully depreciated asset is split, the asset book status should be manually changed from **Closed** to **Open**.</span></span> <span data-ttu-id="7ef59-115">Tämä vaihe on pakollinen, koska kirjan tilan on oltava **Avoin** , jos käyttöomaisuuteen on kirjattava tapahtumia (kuten poistomyynti).</span><span class="sxs-lookup"><span data-stu-id="7ef59-115">This step is required because the book status has to be **Open** if you must post transactions for the asset (for example, for a disposal sale).</span></span> <span data-ttu-id="7ef59-116">Kun käyttöomaisuuskirjan tila on vaihdettu, jaa käyttöomaisuus seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="7ef59-116">After the asset book status is changed, follow these steps to split the asset.</span></span>

1. <span data-ttu-id="7ef59-117">Etsi ja valitse luettelosta jaettavan käyttöomaisuuden linkki.</span><span class="sxs-lookup"><span data-stu-id="7ef59-117">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="7ef59-118">Valitse **Kirjat**.</span><span class="sxs-lookup"><span data-stu-id="7ef59-118">Select **Books**.</span></span> <span data-ttu-id="7ef59-119">Valitse kirja, joka jaetaan uudeksi käyttöomaisuuseräksi.</span><span class="sxs-lookup"><span data-stu-id="7ef59-119">Select the book to split to the new asset.</span></span>
3. <span data-ttu-id="7ef59-120">Valitse **Toiminnot**.</span><span class="sxs-lookup"><span data-stu-id="7ef59-120">Select **Functions**.</span></span>
4. <span data-ttu-id="7ef59-121">Valitse **Jaa käyttöomaisuus**.</span><span class="sxs-lookup"><span data-stu-id="7ef59-121">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="7ef59-122">Syötä tai valitse arvo **Käyttöomaisuuserään** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="7ef59-122">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="7ef59-123">Avaa haku napsauttamalla **Kirjaan** -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="7ef59-123">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="7ef59-124">Syötä **Tapahtumapäivä** -kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="7ef59-124">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="7ef59-125">Kirjoita numero **Prosentti** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="7ef59-125">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="7ef59-126">Syötä tai valitse arvo **Kirjauskansion nimi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="7ef59-126">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="7ef59-127">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="7ef59-127">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="7ef59-128">Kirjauskansiotapahtuman kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="7ef59-128">Post the journal transaction</span></span>

1. <span data-ttu-id="7ef59-129">Valitse siirtymisruudussa **Moduulit \> Käyttöomaisuuserät \> Kirjauskansioviennit \> Käyttöomaisuuden kirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="7ef59-129">In the navigation pane, go to **Modules \> Fixed assets \> Journal entries \> Fixed assets journal**.</span></span>
2. <span data-ttu-id="7ef59-130">Valitse luettelosta jakoprosessissa luotu kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="7ef59-130">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="7ef59-131">Valitse **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="7ef59-131">Select **Lines**.</span></span>

    - <span data-ttu-id="7ef59-132">Tarkista luodut kirjauskansiorivit.</span><span class="sxs-lookup"><span data-stu-id="7ef59-132">Verify the journal lines created.</span></span>
    - <span data-ttu-id="7ef59-133">Alkuperäisen käyttöomaisuuserän hankinnan oikaisutapahtuma luodaan, kun arvoa halutaan nostaa määritetyn prosenttiosuuden verran jakoprosentin aikana.</span><span class="sxs-lookup"><span data-stu-id="7ef59-133">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>
    - <span data-ttu-id="7ef59-134">Uudelle käyttöomaisuuserälle luodaan hankintatapahtuma samalle summalle.</span><span class="sxs-lookup"><span data-stu-id="7ef59-134">An Acquisition transaction is created for the new asset for the same amount.</span></span>

4. <span data-ttu-id="7ef59-135">Valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="7ef59-135">Select **Post**.</span></span>
