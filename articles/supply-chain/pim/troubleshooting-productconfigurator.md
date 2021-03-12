---
title: Tuotteen määritystoiminnon vianmääritys
description: Tässä aiheessa käsitellään sellaisten ongelmien korjaamista, joita tuotteen määritystoiminnon käytössä voi esiintyä.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e6cfeb6a2b4166dfa9a5a5cc1b7d3d913b865ce2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999603"
---
# <a name="troubleshoot-the-product-configurator"></a><span data-ttu-id="73d29-103">Tuotteen määritystoiminnon vianmääritys</span><span class="sxs-lookup"><span data-stu-id="73d29-103">Troubleshoot the product configurator</span></span>

<span data-ttu-id="73d29-104">Tässä aiheessa käsitellään sellaisten ongelmien korjaamista, joita tuotteen määritystoiminnon käytössä voi esiintyä.</span><span class="sxs-lookup"><span data-stu-id="73d29-104">This topic describes how to fix issues that you might encounter while you work with the product configurator.</span></span>

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a><span data-ttu-id="73d29-105">Nimikkeen teksti korvataan, kun tuote määritetään myyntitilauksen rivillä.</span><span class="sxs-lookup"><span data-stu-id="73d29-105">Item text is overwritten when I configure a product on a sales order line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="73d29-106">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="73d29-106">Issue description</span></span>

<span data-ttu-id="73d29-107">Tämä ongelma esiintyy, kun luot myyntitilauksen rivin määritettävälle nimikkeelle ja muokkaat sitten nimikkeen tekstiä.</span><span class="sxs-lookup"><span data-stu-id="73d29-107">This issue occurs when you create a sales order line for a configurable item and then modify the item text.</span></span> <span data-ttu-id="73d29-108">Kun määrität nimikkeen ja valitset **OK**, teksti korvataan vakiotekstillä.</span><span class="sxs-lookup"><span data-stu-id="73d29-108">When you configure the item and then select **OK**, the text is overwritten with the standard text.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="73d29-109">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="73d29-109">Issue resolution</span></span>

<span data-ttu-id="73d29-110">Tämä toiminta on tarkoituksellista.</span><span class="sxs-lookup"><span data-stu-id="73d29-110">This behavior is expected.</span></span> <span data-ttu-id="73d29-111">Tekstikenttä sisältää variantin nimen, joka täytetään vasta, kun rivi on määritetty.</span><span class="sxs-lookup"><span data-stu-id="73d29-111">The text field includes the variant name, which is filled in only after you configure the line.</span></span> <span data-ttu-id="73d29-112">Tämän vuoksi tekstiä on muutettava vasta, kun rivi on määritetty, ei sitä ennen.</span><span class="sxs-lookup"><span data-stu-id="73d29-112">Therefore, you must change the text after you've configured the line, not before.</span></span>

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a><span data-ttu-id="73d29-113">Kokonaislukumääritteet pyöristetään virheellisesti, kun tuotemääritysmalleja lasketaan.</span><span class="sxs-lookup"><span data-stu-id="73d29-113">Integer attributes are incorrectly rounded when product configuration models are calculated.</span></span>

### <a name="issue-description"></a><span data-ttu-id="73d29-114">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="73d29-114">Issue description</span></span>

<span data-ttu-id="73d29-115">Tämä ongelma voi esiintyä, kun seuraavat toiminnot suoritetaan:</span><span class="sxs-lookup"><span data-stu-id="73d29-115">This issue can occur when you perform the following series of actions:</span></span>

1. <span data-ttu-id="73d29-116">Määritä tuotannon määritysmallin seuraavat määritteet:</span><span class="sxs-lookup"><span data-stu-id="73d29-116">Set up the following attributes on a production configuration model:</span></span>

    - <span data-ttu-id="73d29-117">Syöte (kokonaisluku)</span><span class="sxs-lookup"><span data-stu-id="73d29-117">Input (integer)</span></span>
    - <span data-ttu-id="73d29-118">Prosentti (desimaaliluku)</span><span class="sxs-lookup"><span data-stu-id="73d29-118">Percent (decimal)</span></span>
    - <span data-ttu-id="73d29-119">Tulos (kokonaisluku)</span><span class="sxs-lookup"><span data-stu-id="73d29-119">Result (integer)</span></span>

2. <span data-ttu-id="73d29-120">Luo laskelma, jossa on seuraava lauseke:</span><span class="sxs-lookup"><span data-stu-id="73d29-120">Create a calculation that has the following expression:</span></span>

    <span data-ttu-id="73d29-121">*Tulos* = *Syöte* × *prosentti* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="73d29-121">*Result* = *Input* × *Percent* ÷ 100</span></span>

<span data-ttu-id="73d29-122">Tässä tapauksessa kokonaislukutulosta ei aina pyöristetä oikein.</span><span class="sxs-lookup"><span data-stu-id="73d29-122">In this case, the integer result isn't always correctly rounded.</span></span> <span data-ttu-id="73d29-123">Syöte on esimerkiksi 1 000 ja prosentti 2,40.</span><span class="sxs-lookup"><span data-stu-id="73d29-123">For example, the input is 1,000, and the percentage is 2.40.</span></span> <span data-ttu-id="73d29-124">Tämän vuoksi kokonaislukutuloksen odotetaan olevan 24, koska 2,40 prosenttia 1 000:sta on 24 (tai 24,00 desimaalimuodossa).</span><span class="sxs-lookup"><span data-stu-id="73d29-124">Therefore, you expect the integer result to be 24, because 2.40 percent of 1,000 is 24 (or 24.00 in decimal form).</span></span> <span data-ttu-id="73d29-125">Sen sijaan tuloksena näkyy 23.</span><span class="sxs-lookup"><span data-stu-id="73d29-125">Instead, the result is shown as 23.</span></span> <span data-ttu-id="73d29-126">Kun prosenttina on sen sijaan 2,39, tulokseksi pyöristetään 24 eikä 23.</span><span class="sxs-lookup"><span data-stu-id="73d29-126">However, when the percentage is 2.39, the calculation is rounded to 24 instead of 23.</span></span> <span data-ttu-id="73d29-127">Kun prosenttina on 2,50, laskelma pyöristystulos on odotettu 25.</span><span class="sxs-lookup"><span data-stu-id="73d29-127">When the percentage is 2.50, the calculation is rounded to 25, as expected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="73d29-128">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="73d29-128">Issue resolution</span></span>

<span data-ttu-id="73d29-129">Tämä ongelma johtuu tavasta, jolla Microsoft Solver Foundation ilmaisee luvut sisäisesti murtolukuja käyttämällä.</span><span class="sxs-lookup"><span data-stu-id="73d29-129">This issue occurs because of the way that Microsoft Solver Foundation internally represents numbers by using fractions.</span></span> <span data-ttu-id="73d29-130">Edellisen esimerkin laskutoimituksen tulos prosentteina on 2,40, joka ilmaistaan muodossa 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375.</span><span class="sxs-lookup"><span data-stu-id="73d29-130">For the preceding example, the result of the calculation where the percentage is 2.40 is represented as 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375.</span></span> <span data-ttu-id="73d29-131">Kun .NET näyttää tämän arvon kokonaislukuja, tuloksena 23.</span><span class="sxs-lookup"><span data-stu-id="73d29-131">When .NET casts this value as an integer, it will return 23.</span></span>

<span data-ttu-id="73d29-132">Tätä toimintaa ei muuteta, koska muut skenaariot tarvitsevat sitä.</span><span class="sxs-lookup"><span data-stu-id="73d29-132">This behavior won't be changed, because other scenarios depend on it.</span></span> <span data-ttu-id="73d29-133">Edellisen esimerkin ongelman voi korjata ottamalla käyttöön lisädesimaalimääritteen ja laskelman.</span><span class="sxs-lookup"><span data-stu-id="73d29-133">For the preceding example, you can fix the issue by introducing an additional decimal attribute and a calculation.</span></span>

<span data-ttu-id="73d29-134">Voit esimerkiksi määrittää tuotannon määritysmallin seuraavat määritteet:</span><span class="sxs-lookup"><span data-stu-id="73d29-134">For example, you can set up the following attributes on a production configuration model:</span></span>

- <span data-ttu-id="73d29-135">Syöte (kokonaisluku)</span><span class="sxs-lookup"><span data-stu-id="73d29-135">Input (integer)</span></span>
- <span data-ttu-id="73d29-136">Prosentti (desimaaliluku)</span><span class="sxs-lookup"><span data-stu-id="73d29-136">Percent (decimal)</span></span>
- <span data-ttu-id="73d29-137">ResultDecimal (desimaali)</span><span class="sxs-lookup"><span data-stu-id="73d29-137">ResultDecimal (decimal)</span></span>
- <span data-ttu-id="73d29-138">ResultInteger (kokonaisluku)</span><span class="sxs-lookup"><span data-stu-id="73d29-138">ResultInteger (integer)</span></span>

<span data-ttu-id="73d29-139">Voit sitten lisätä seuraavat laskelmat:</span><span class="sxs-lookup"><span data-stu-id="73d29-139">You can then add the following calculations:</span></span>

- <span data-ttu-id="73d29-140">*ResultDecimal* = *Syöte* × *Prosentti* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="73d29-140">*ResultDecimal* = *Input* × *Percent* ÷ 100</span></span>
- <span data-ttu-id="73d29-141">*ResultInteger* = *ResultDecimal*</span><span class="sxs-lookup"><span data-stu-id="73d29-141">*ResultInteger* = *ResultDecimal*</span></span>
