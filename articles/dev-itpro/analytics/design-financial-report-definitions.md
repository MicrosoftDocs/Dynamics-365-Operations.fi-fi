---
title: Talousraporttien suunnittelutoiminnon raportin määritykset
description: Tässä artikkelissa on tietoja raportin määrityksistä. Raportin määritys on raporttiosa (tai rakenneosa), joka käyttää raportin luontiin rivin, sarakkeen ja valinnaisesti myös raportointipuun määritystä. Raportin määrityksessä on myös vaihtoehtoja ja asetuksia raportin mukauttamiseen.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 322f1cca32053224e1cd6dbaf29c098b983b5e1f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "327340"
---
# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="701f2-105">Talousraporttien suunnittelutoiminnon raportin määritykset</span><span class="sxs-lookup"><span data-stu-id="701f2-105">Report definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="701f2-106">Tässä artikkelissa on tietoja raportin määrityksistä.</span><span class="sxs-lookup"><span data-stu-id="701f2-106">This article provides information about report definitions.</span></span> <span data-ttu-id="701f2-107">Raportin määritys on raporttiosa (tai rakenneosa), joka käyttää raportin luontiin rivin, sarakkeen ja valinnaisesti myös raportointipuun määritystä.</span><span class="sxs-lookup"><span data-stu-id="701f2-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="701f2-108">Raportin määrityksessä on myös vaihtoehtoja ja asetuksia raportin mukauttamiseen.</span><span class="sxs-lookup"><span data-stu-id="701f2-108">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="701f2-109">Raportin määritys on raporttiosa (tai rakenneosa), joka käyttää raportin luontiin rivin, sarakkeen ja valinnaisesti myös raportointipuun määritystä.</span><span class="sxs-lookup"><span data-stu-id="701f2-109">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="701f2-110">Raporttimääritys sisältää myös vaihtoehtoja ja asetuksia, joiden avulla voit mukauttaa raporttia.</span><span class="sxs-lookup"><span data-stu-id="701f2-110">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="701f2-111">Kun olet määrittänyt rivi- ja sarakemääritykset, ne on yhdistettävä raportin määrityksessä.</span><span class="sxs-lookup"><span data-stu-id="701f2-111">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="701f2-112">Tällöin määritetään myös muita määrityksen osia, kuten erittelytaso ja raportin päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="701f2-112">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="701f2-113">Voit nyt tallentaa ja luoda raportin.</span><span class="sxs-lookup"><span data-stu-id="701f2-113">You can then save and generate a report.</span></span> <span data-ttu-id="701f2-114">Talousraportointi sisältää seuraavat erittelytasot:</span><span class="sxs-lookup"><span data-stu-id="701f2-114">Financial reporting offers the following levels of detail:</span></span>

- <span data-ttu-id="701f2-115">Taloushallinto</span><span class="sxs-lookup"><span data-stu-id="701f2-115">Financial</span></span>
- <span data-ttu-id="701f2-116">Taloudellinen ja Tili</span><span class="sxs-lookup"><span data-stu-id="701f2-116">Financial and Account</span></span>
- <span data-ttu-id="701f2-117">Taloudellinen, Tili ja Tapahtuma</span><span class="sxs-lookup"><span data-stu-id="701f2-117">Financial, Account, and Transaction</span></span>

<span data-ttu-id="701f2-118">Tapahtumatiedot eivät kuitenkaan välttämättä ole käytettävissä raporteissa. Tämä riippuu siitä, miten tiedot tallennetaan Microsoft Dynamics ERP -järjestelmään.</span><span class="sxs-lookup"><span data-stu-id="701f2-118">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="701f2-119">Luo raportin määritys</span><span class="sxs-lookup"><span data-stu-id="701f2-119">Create a report definition</span></span>
1. <span data-ttu-id="701f2-120">Valitse raportin suunnitteluohjelman **Tiedosto** -valikosta **Uusi**, ja valitse sitten **Raportin määritys**.</span><span class="sxs-lookup"><span data-stu-id="701f2-120">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2. <span data-ttu-id="701f2-121">Määritä tarvittavat tiedot **Raportti**, **Tuotos ja Jakelu**, **Ylä- ja alatunnisteet** ja **Asetukset** -välilehdille.</span><span class="sxs-lookup"><span data-stu-id="701f2-121">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="701f2-122">Raportin määrityksen sisältö</span><span class="sxs-lookup"><span data-stu-id="701f2-122">Contents of a report definition</span></span>
<span data-ttu-id="701f2-123">Seuraavassa taulukossa kuvataan raportin määrityksen välilehdet sekä tietojen käyttötapa.</span><span class="sxs-lookup"><span data-stu-id="701f2-123">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="701f2-124">Sarkain</span><span class="sxs-lookup"><span data-stu-id="701f2-124">Tab</span></span></th>
<th><span data-ttu-id="701f2-125">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="701f2-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="701f2-126">Raportti</span><span class="sxs-lookup"><span data-stu-id="701f2-126">Report</span></span></td>
<td><span data-ttu-id="701f2-127">Luo raportti, määritä raportti tai muokkaa aiemmin luotua raporttia.</span><span class="sxs-lookup"><span data-stu-id="701f2-127">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="701f2-128">Tuotos ja Jakelu</span><span class="sxs-lookup"><span data-stu-id="701f2-128">Output and Distribution</span></span></td>
<td><span data-ttu-id="701f2-129">Muuttaa tuotoksen tyypin ja raportin kohteen.</span><span class="sxs-lookup"><span data-stu-id="701f2-129">Change the output type and destination of the report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="701f2-130">Ylä- ja alatunnisteet</span><span class="sxs-lookup"><span data-stu-id="701f2-130">Headers and Footers</span></span></td>
<td><span data-ttu-id="701f2-131">Määrittää ja muotoilee raportin ylä- ja alatunnisteet.</span><span class="sxs-lookup"><span data-stu-id="701f2-131">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="701f2-132">Voit esimerkiksi lisätä tekstiä tai kuvia tunnisteisiin.</span><span class="sxs-lookup"><span data-stu-id="701f2-132">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="701f2-133">Talousraportointi tukee .bmp-, .jpg- ja .png-kuvatiedostoja.</span><span class="sxs-lookup"><span data-stu-id="701f2-133">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="701f2-134">Voit myös käyttää automaattisia koodeja lisätäksesi muita tietoja, kuten yrityksen nimen, raportin nimen tai sivunumeron.</span><span class="sxs-lookup"><span data-stu-id="701f2-134">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="701f2-135">Asetukset</span><span class="sxs-lookup"><span data-stu-id="701f2-135">Settings</span></span></td>
<td><span data-ttu-id="701f2-136">Määritä raportin määritysasetukset, joihin voi sisältyä seuraavia asetuksia:</span><span class="sxs-lookup"><span data-stu-id="701f2-136">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="701f2-137">Muotoilu ja pyöristyssummat</span><span class="sxs-lookup"><span data-stu-id="701f2-137">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="701f2-138">Raporttierittelyn muoto</span><span class="sxs-lookup"><span data-stu-id="701f2-138">Format detail reports</span></span></li>
<li><span data-ttu-id="701f2-139">Raporttipuiden muoto</span><span class="sxs-lookup"><span data-stu-id="701f2-139">Format reporting trees</span></span></li>
<li><span data-ttu-id="701f2-140">Luo poikkeusraportti</span><span class="sxs-lookup"><span data-stu-id="701f2-140">Generate an exception report</span></span></li>
<li><span data-ttu-id="701f2-141">Valuuttamuunnoksen määritys</span><span class="sxs-lookup"><span data-stu-id="701f2-141">Specify currency conversion</span></span></li>
<li><span data-ttu-id="701f2-142">Välisumma- ja suodatintilitiedot</span><span class="sxs-lookup"><span data-stu-id="701f2-142">Subtotal and filter account details</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="701f2-143">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="701f2-143">Additional resources</span></span>

[<span data-ttu-id="701f2-144">Talousraportointi</span><span class="sxs-lookup"><span data-stu-id="701f2-144">Financial reporting</span></span>](financial-reporting-intro.md)
