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
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 75938e6fdf5fd8f10ac9719fc449a586c08d06b8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975938"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="b288d-103">Käyttöomaisuuserän jakaminen</span><span class="sxs-lookup"><span data-stu-id="b288d-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b288d-104">Tässä aiheessa kerrotaan miten jaetaan yhden käyttöomaisuuskirjan prosenttiosuus uuteen käyttöomaisuuskirjaan.</span><span class="sxs-lookup"><span data-stu-id="b288d-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="b288d-105">Käytössä ovat kirjanpitäjän rooli ja USMF:n esittelytiedot.</span><span class="sxs-lookup"><span data-stu-id="b288d-105">It uses the Accountant role and USMF demo data.</span></span>

## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="b288d-106">Luo uusi käyttöomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="b288d-106">Create a new fixed asset</span></span>

1. <span data-ttu-id="b288d-107">Valitse siirtymisruudussa **Moduulit \> Käyttöomaisuuserät \> Käyttöomaisuuserät \> Käyttöomaisuuserät**.</span><span class="sxs-lookup"><span data-stu-id="b288d-107">In the navigation pane, go to **Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="b288d-108">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b288d-108">Select **New**.</span></span>
3. <span data-ttu-id="b288d-109">Syötä tai valitse arvo **Käyttöomaisuusryhmä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="b288d-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="b288d-110">Huomaa, että käyttöomaisuusnumeroa käytetään jakoprosessissa myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="b288d-110">Note the fixed asset number to use in the split process later.</span></span>
4. <span data-ttu-id="b288d-111">Anna **Nimi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="b288d-111">In the **Name** field, enter a value.</span></span>
5. <span data-ttu-id="b288d-112">Sulje lomake.</span><span class="sxs-lookup"><span data-stu-id="b288d-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="b288d-113">Käyttöomaisuuserän jakaminen</span><span class="sxs-lookup"><span data-stu-id="b288d-113">Split a fixed asset</span></span>

<span data-ttu-id="b288d-114">Ennen kokonaan poistetun käyttöomaisuuden jakamista käyttöomaisuuskirjan tila **Suljettu** on vaihdettava manuaalisesti tilaan **Avoin**.</span><span class="sxs-lookup"><span data-stu-id="b288d-114">Before a fully depreciated asset is split, the asset book status should be manually changed from **Closed** to **Open**.</span></span> <span data-ttu-id="b288d-115">Tämä vaihe on pakollinen, koska kirjan tilan on oltava **Avoin**, jos käyttöomaisuuteen on kirjattava tapahtumia (kuten poistomyynti).</span><span class="sxs-lookup"><span data-stu-id="b288d-115">This step is required because the book status has to be **Open** if you must post transactions for the asset (for example, for a disposal sale).</span></span> <span data-ttu-id="b288d-116">Ota myös **Salli useita tapahtumia yhdessä tositteessa** -parametri käyttöön **Yleistiedot**-välilehdessä **Kirjanpidon parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="b288d-116">You must also turn on the **Allow multiple transactions within one voucher** parameter on the **General** tab of the **General ledger parameters** page.</span></span> <span data-ttu-id="b288d-117">Kun käyttöomaisuuskirjan tila on muutettu ja yhden tositteen useita tapahtumia on sallittu, jaa käyttöomaisuuserä suorittamalla seuraavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="b288d-117">After the asset book status is changed and multiple transactions within one voucher have been allowed, complete the following steps to split the asset.</span></span>

1. <span data-ttu-id="b288d-118">Etsi ja valitse luettelosta jaettavan käyttöomaisuuden linkki.</span><span class="sxs-lookup"><span data-stu-id="b288d-118">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="b288d-119">Valitse **Kirjat**.</span><span class="sxs-lookup"><span data-stu-id="b288d-119">Select **Books**.</span></span> <span data-ttu-id="b288d-120">Valitse kirja, joka jaetaan uudeksi käyttöomaisuuseräksi.</span><span class="sxs-lookup"><span data-stu-id="b288d-120">Select the book to split to the new asset.</span></span>
3. <span data-ttu-id="b288d-121">Valitse **Toiminnot**.</span><span class="sxs-lookup"><span data-stu-id="b288d-121">Select **Functions**.</span></span>
4. <span data-ttu-id="b288d-122">Valitse **Jaa käyttöomaisuus**.</span><span class="sxs-lookup"><span data-stu-id="b288d-122">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="b288d-123">Syötä tai valitse arvo **Käyttöomaisuuserään**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="b288d-123">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="b288d-124">Avaa haku napsauttamalla **Kirjaan**-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="b288d-124">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="b288d-125">Syötä **Tapahtumapäivä**-kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="b288d-125">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="b288d-126">Kirjoita numero **Prosentti**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b288d-126">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="b288d-127">Syötä tai valitse arvo **Kirjauskansion nimi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="b288d-127">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="b288d-128">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b288d-128">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="b288d-129">Kirjauskansiotapahtuman kirjaaminen</span><span class="sxs-lookup"><span data-stu-id="b288d-129">Post the journal transaction</span></span>

1. <span data-ttu-id="b288d-130">Valitse siirtymisruudussa **Moduulit \> Käyttöomaisuuserät \> Kirjauskansioviennit \> Käyttöomaisuuden kirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="b288d-130">In the navigation pane, go to **Modules \> Fixed assets \> Journal entries \> Fixed assets journal**.</span></span>
2. <span data-ttu-id="b288d-131">Valitse luettelosta jakoprosessissa luotu kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="b288d-131">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="b288d-132">Valitse **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="b288d-132">Select **Lines**.</span></span>

    - <span data-ttu-id="b288d-133">Tarkista luodut kirjauskansiorivit.</span><span class="sxs-lookup"><span data-stu-id="b288d-133">Verify the journal lines created.</span></span>
    - <span data-ttu-id="b288d-134">Alkuperäisen käyttöomaisuuserän hankinnan oikaisutapahtuma luodaan, kun arvoa halutaan nostaa määritetyn prosenttiosuuden verran jakoprosentin aikana.</span><span class="sxs-lookup"><span data-stu-id="b288d-134">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>
    - <span data-ttu-id="b288d-135">Uudelle käyttöomaisuuserälle luodaan hankintatapahtuma samalle summalle.</span><span class="sxs-lookup"><span data-stu-id="b288d-135">An Acquisition transaction is created for the new asset for the same amount.</span></span>

4. <span data-ttu-id="b288d-136">Valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="b288d-136">Select **Post**.</span></span>
