---
title: Mallituoterakenteen luominen
description: Mallituoterakenteen voi luoda monella eri tavalla.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89c5d45ac27a8678c51fb63c0326c2802a094596
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "320992"
---
# <a name="create-a-template-bom"></a><span data-ttu-id="80e63-103">Mallituoterakenteen luominen</span><span class="sxs-lookup"><span data-stu-id="80e63-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="80e63-104">Mallituoterakenteen voi luoda millä tahansa seuraavista menetelmistä.</span><span class="sxs-lookup"><span data-stu-id="80e63-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="80e63-105">Kaikissa menetelmissä **Aloituspäivämäärä**- ja **Lopetuspäivämäärä**-kentät ovat valinnaisia ja vain tiedoksi.</span><span class="sxs-lookup"><span data-stu-id="80e63-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="80e63-106">Mallituoterakenteen luominen manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="80e63-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="80e63-107">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltokohteet** \> **Mallituoterakenteet**.</span><span class="sxs-lookup"><span data-stu-id="80e63-107">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="80e63-108">Avaa **Luo mallituoterakenne** -lomake painamalla CTRL + N -näppäinyhdistelmää.</span><span class="sxs-lookup"><span data-stu-id="80e63-108">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="80e63-109">Valitse **Kopioi tuoterakenteen rivit viitteestä** -kohdassa **Manuaalinen**-vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="80e63-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="80e63-110">Syötä **Nimikenumero**-kenttään **Tuoterakenne**-tyyppinen nimike.</span><span class="sxs-lookup"><span data-stu-id="80e63-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="80e63-111">Kirjoita **Nimi**-kenttään mallin nimi.</span><span class="sxs-lookup"><span data-stu-id="80e63-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="80e63-112">Kirjoita **Aloituspäivämäärä**- ja **Lopetuspäivämäärä**-kenttiin päivämääräväli, jolloin mallituoterakenne on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="80e63-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="80e63-113">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="80e63-113">Click **OK**.</span></span>

<span data-ttu-id="80e63-114">Järjestelmä luo uuden tyhjän mallituoterakenteen.</span><span class="sxs-lookup"><span data-stu-id="80e63-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="80e63-115">Mallituoterakenteen luominen toisen mallituoterakenteen perusteella</span><span class="sxs-lookup"><span data-stu-id="80e63-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="80e63-116">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltokohteet** \> **Mallituoterakenteet**.</span><span class="sxs-lookup"><span data-stu-id="80e63-116">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="80e63-117">Avaa **Luo mallituoterakenne** -lomake painamalla CTRL + N -näppäinyhdistelmää.</span><span class="sxs-lookup"><span data-stu-id="80e63-117">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="80e63-118">Valitse **Kopioi tuoterakenteen rivit viitteestä** -kohdassa **Mallituoterakenne**-vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="80e63-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="80e63-119">Valitse **Viitenumero**-kentässä aiemmin luotu mallituoterakenne, jonka haluat kopioida uuteen mallituoterakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="80e63-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="80e63-120">Kirjoita **Nimi**-kenttään mallin nimi.</span><span class="sxs-lookup"><span data-stu-id="80e63-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="80e63-121">Kirjoita **Aloituspäivämäärä**- ja **Lopetuspäivämäärä**-kenttiin päivämääräväli, jolloin mallituoterakenne on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="80e63-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="80e63-122">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="80e63-122">Click **OK**.</span></span>

<span data-ttu-id="80e63-123">Järjestelmä luo uuden mallituoterakenteen käyttämällä rivejä, jotka vastaavat alkuperäistä mallituoterakennetta.</span><span class="sxs-lookup"><span data-stu-id="80e63-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="80e63-124">Mallituoterakenteen luominen nimikkeen tuoterakenteen perusteella</span><span class="sxs-lookup"><span data-stu-id="80e63-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="80e63-125">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltokohteet** \> **Mallituoterakenteet**.</span><span class="sxs-lookup"><span data-stu-id="80e63-125">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="80e63-126">Avaa **Luo mallituoterakenne** -lomake painamalla CTRL + N -näppäinyhdistelmää.</span><span class="sxs-lookup"><span data-stu-id="80e63-126">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="80e63-127">Valitse **Kopioi tuoterakenteen rivit viitteestä** -kohdassa **Tuoterakenne**.</span><span class="sxs-lookup"><span data-stu-id="80e63-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="80e63-128">Valitse **Viitenumero**-kentässä tuoterakenteen versio.</span><span class="sxs-lookup"><span data-stu-id="80e63-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="80e63-129">Tuoterakenne-tyyppinen nimike kopioidaan kohtaan **Nimikenumero**.</span><span class="sxs-lookup"><span data-stu-id="80e63-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="80e63-130">Kirjoita **Nimi**-kenttään mallin nimi.</span><span class="sxs-lookup"><span data-stu-id="80e63-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="80e63-131">Kirjoita **Aloituspäivämäärä**- ja **Lopetuspäivämäärä**-kenttiin päivämääräväli, jolloin mallituoterakenne on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="80e63-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="80e63-132">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="80e63-132">Click **OK**.</span></span>

<span data-ttu-id="80e63-133">Uusi mallituoterakenne luodaan käyttämällä rivejä, jotka vastaavat **Tuoterakenteet**-kohdassa mainitun tuoterakenteen rivejä.</span><span class="sxs-lookup"><span data-stu-id="80e63-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="80e63-134">Mallituoterakenteen luominen tuotannon tuoterakenteen perusteella</span><span class="sxs-lookup"><span data-stu-id="80e63-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="80e63-135">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltokohteet** \> **Mallituoterakenteet**.</span><span class="sxs-lookup"><span data-stu-id="80e63-135">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="80e63-136">Avaa **Luo mallituoterakenne** -lomake painamalla CTRL + N -näppäinyhdistelmää.</span><span class="sxs-lookup"><span data-stu-id="80e63-136">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="80e63-137">Valitse **Kopioi tuoterakenteen rivit viitteestä** -kohdassa **Tuotanto**.</span><span class="sxs-lookup"><span data-stu-id="80e63-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="80e63-138">Valitse **Viitenumero**-kentässä tuotannon tuoterakenne.</span><span class="sxs-lookup"><span data-stu-id="80e63-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="80e63-139">Kirjoita **Nimi**-kenttään mallin nimi.</span><span class="sxs-lookup"><span data-stu-id="80e63-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="80e63-140">Kirjoita **Aloituspäivämäärä**- ja **Lopetuspäivämäärä**-kenttiin päivämääräväli, jolloin mallituoterakenne on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="80e63-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="80e63-141">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="80e63-141">Click **OK**.</span></span>

<span data-ttu-id="80e63-142">Uusi mallituoterakenne luodaan käyttämällä rivejä, jotka vastaavat **Tuoterakenne**-kohdassa mainitun tuoterakenteen rivejä.</span><span class="sxs-lookup"><span data-stu-id="80e63-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="80e63-143">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="80e63-143">See also</span></span>

[<span data-ttu-id="80e63-144">Mallituoterakenteet </span><span class="sxs-lookup"><span data-stu-id="80e63-144">Template BOMs</span></span>](template-boms.md)

  


