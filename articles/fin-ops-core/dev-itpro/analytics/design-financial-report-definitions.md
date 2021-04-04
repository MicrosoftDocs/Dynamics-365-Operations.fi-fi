---
title: Talousraporttien suunnittelutoiminnon raportin määritykset
description: Tässä artikkelissa on tietoja raportin määrityksistä.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 073df430892e01d4842b2af147b0ae2765b1c66a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570339"
---
# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="57b97-103">Talousraporttien suunnittelutoiminnon raportin määritykset</span><span class="sxs-lookup"><span data-stu-id="57b97-103">Report definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57b97-104">Tässä artikkelissa on tietoja raportin määrityksistä.</span><span class="sxs-lookup"><span data-stu-id="57b97-104">This article provides information about report definitions.</span></span> <span data-ttu-id="57b97-105">Raportin määritys on raporttiosa (tai rakenneosa), joka käyttää raportin luontiin rivin, sarakkeen ja valinnaisesti myös raportointipuun määritystä.</span><span class="sxs-lookup"><span data-stu-id="57b97-105">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="57b97-106">Raportin määrityksessä on myös vaihtoehtoja ja asetuksia raportin mukauttamiseen.</span><span class="sxs-lookup"><span data-stu-id="57b97-106">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="57b97-107">Raportin määritys on raporttiosa (tai rakenneosa), joka käyttää raportin luontiin rivin, sarakkeen ja valinnaisesti myös raportointipuun määritystä.</span><span class="sxs-lookup"><span data-stu-id="57b97-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="57b97-108">Raporttimääritys sisältää myös vaihtoehtoja ja asetuksia, joiden avulla voit mukauttaa raporttia.</span><span class="sxs-lookup"><span data-stu-id="57b97-108">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="57b97-109">Kun olet määrittänyt rivi- ja sarakemääritykset, ne on yhdistettävä raportin määrityksessä.</span><span class="sxs-lookup"><span data-stu-id="57b97-109">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="57b97-110">Tällöin määritetään myös muita määrityksen osia, kuten erittelytaso ja raportin päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="57b97-110">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="57b97-111">Voit nyt tallentaa ja luoda raportin.</span><span class="sxs-lookup"><span data-stu-id="57b97-111">You can then save and generate a report.</span></span> <span data-ttu-id="57b97-112">Talousraportointi sisältää seuraavat erittelytasot:</span><span class="sxs-lookup"><span data-stu-id="57b97-112">Financial reporting offers the following levels of detail:</span></span>

- <span data-ttu-id="57b97-113">Taloushallinto</span><span class="sxs-lookup"><span data-stu-id="57b97-113">Financial</span></span>
- <span data-ttu-id="57b97-114">Taloudellinen ja Tili</span><span class="sxs-lookup"><span data-stu-id="57b97-114">Financial and Account</span></span>
- <span data-ttu-id="57b97-115">Taloudellinen, Tili ja Tapahtuma</span><span class="sxs-lookup"><span data-stu-id="57b97-115">Financial, Account, and Transaction</span></span>

<span data-ttu-id="57b97-116">Tapahtumatiedot eivät kuitenkaan välttämättä ole käytettävissä raporteissa. Tämä riippuu siitä, miten tiedot tallennetaan Microsoft Dynamics ERP -järjestelmään.</span><span class="sxs-lookup"><span data-stu-id="57b97-116">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="57b97-117">Luo raportin määritys</span><span class="sxs-lookup"><span data-stu-id="57b97-117">Create a report definition</span></span>
1. <span data-ttu-id="57b97-118">Valitse raportin suunnitteluohjelman **Tiedosto** -valikosta **Uusi**, ja valitse sitten **Raportin määritys**.</span><span class="sxs-lookup"><span data-stu-id="57b97-118">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2. <span data-ttu-id="57b97-119">Määritä tarvittavat tiedot **Raportti**, **Tuotos ja Jakelu**, **Ylä- ja alatunnisteet** ja **Asetukset** -välilehdille.</span><span class="sxs-lookup"><span data-stu-id="57b97-119">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="57b97-120">Raportin määrityksen sisältö</span><span class="sxs-lookup"><span data-stu-id="57b97-120">Contents of a report definition</span></span>
<span data-ttu-id="57b97-121">Seuraavassa taulukossa kuvataan raportin määrityksen välilehdet sekä tietojen käyttötapa.</span><span class="sxs-lookup"><span data-stu-id="57b97-121">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="57b97-122">Sarkain</span><span class="sxs-lookup"><span data-stu-id="57b97-122">Tab</span></span></th>
<th><span data-ttu-id="57b97-123">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="57b97-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57b97-124">Raportti</span><span class="sxs-lookup"><span data-stu-id="57b97-124">Report</span></span></td>
<td><span data-ttu-id="57b97-125">Luo raportti, määritä raportti tai muokkaa aiemmin luotua raporttia.</span><span class="sxs-lookup"><span data-stu-id="57b97-125">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57b97-126">Tuotos ja Jakelu</span><span class="sxs-lookup"><span data-stu-id="57b97-126">Output and Distribution</span></span></td>
<td><span data-ttu-id="57b97-127">Muuttaa tuotoksen tyypin ja raportin kohteen.</span><span class="sxs-lookup"><span data-stu-id="57b97-127">Change the output type and destination of the report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57b97-128">Ylä- ja alatunnisteet</span><span class="sxs-lookup"><span data-stu-id="57b97-128">Headers and Footers</span></span></td>
<td><span data-ttu-id="57b97-129">Määrittää ja muotoilee raportin ylä- ja alatunnisteet.</span><span class="sxs-lookup"><span data-stu-id="57b97-129">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="57b97-130">Voit esimerkiksi lisätä tekstiä tai kuvia tunnisteisiin.</span><span class="sxs-lookup"><span data-stu-id="57b97-130">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="57b97-131">Talousraportointi tukee .bmp-, .jpg- ja .png-kuvatiedostoja.</span><span class="sxs-lookup"><span data-stu-id="57b97-131">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="57b97-132">Voit myös käyttää automaattisia koodeja lisätäksesi muita tietoja, kuten yrityksen nimen, raportin nimen tai sivunumeron.</span><span class="sxs-lookup"><span data-stu-id="57b97-132">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57b97-133">Asetukset</span><span class="sxs-lookup"><span data-stu-id="57b97-133">Settings</span></span></td>
<td><span data-ttu-id="57b97-134">Määritä raportin määritysasetukset, joihin voi sisältyä seuraavia asetuksia:</span><span class="sxs-lookup"><span data-stu-id="57b97-134">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="57b97-135">Muotoilu ja pyöristyssummat</span><span class="sxs-lookup"><span data-stu-id="57b97-135">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="57b97-136">Raporttierittelyn muoto</span><span class="sxs-lookup"><span data-stu-id="57b97-136">Format detail reports</span></span></li>
<li><span data-ttu-id="57b97-137">Raporttipuiden muoto</span><span class="sxs-lookup"><span data-stu-id="57b97-137">Format reporting trees</span></span></li>
<li><span data-ttu-id="57b97-138">Luo poikkeusraportti</span><span class="sxs-lookup"><span data-stu-id="57b97-138">Generate an exception report</span></span></li>
<li><span data-ttu-id="57b97-139">Valuuttamuunnoksen määritys</span><span class="sxs-lookup"><span data-stu-id="57b97-139">Specify currency conversion</span></span></li>
<li><span data-ttu-id="57b97-140">Välisumma- ja suodatintilitiedot</span><span class="sxs-lookup"><span data-stu-id="57b97-140">Subtotal and filter account details</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="57b97-141">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="57b97-141">Additional resources</span></span>

[<span data-ttu-id="57b97-142">Talousraportointi</span><span class="sxs-lookup"><span data-stu-id="57b97-142">Financial reporting</span></span>](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]