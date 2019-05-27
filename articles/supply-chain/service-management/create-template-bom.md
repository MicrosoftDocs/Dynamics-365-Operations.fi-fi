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
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566582"
---
# <a name="create-a-template-bom"></a><span data-ttu-id="54cce-103">Mallituoterakenteen luominen</span><span class="sxs-lookup"><span data-stu-id="54cce-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="54cce-104">Mallituoterakenteen voi luoda millä tahansa seuraavista menetelmistä.</span><span class="sxs-lookup"><span data-stu-id="54cce-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="54cce-105">Kaikissa menetelmissä **Aloituspäivämäärä**- ja **Lopetuspäivämäärä**-kentät ovat valinnaisia ja vain tiedoksi.</span><span class="sxs-lookup"><span data-stu-id="54cce-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="54cce-106">Mallituoterakenteen luominen manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="54cce-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="54cce-107">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltokohteet** \> **Mallituoterakenteet**.</span><span class="sxs-lookup"><span data-stu-id="54cce-107">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="54cce-108">Avaa **Luo mallituoterakenne** -lomake painamalla CTRL + N -näppäinyhdistelmää.</span><span class="sxs-lookup"><span data-stu-id="54cce-108">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="54cce-109">Valitse **Kopioi tuoterakenteen rivit viitteestä** -kohdassa **Manuaalinen**-vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="54cce-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="54cce-110">Syötä **Nimikenumero**-kenttään **Tuoterakenne**-tyyppinen nimike.</span><span class="sxs-lookup"><span data-stu-id="54cce-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="54cce-111">Kirjoita **Nimi**-kenttään mallin nimi.</span><span class="sxs-lookup"><span data-stu-id="54cce-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="54cce-112">Kirjoita **Aloituspäivämäärä**- ja **Lopetuspäivämäärä**-kenttiin päivämääräväli, jolloin mallituoterakenne on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="54cce-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="54cce-113">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="54cce-113">Click **OK**.</span></span>

<span data-ttu-id="54cce-114">Järjestelmä luo uuden tyhjän mallituoterakenteen.</span><span class="sxs-lookup"><span data-stu-id="54cce-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="54cce-115">Mallituoterakenteen luominen toisen mallituoterakenteen perusteella</span><span class="sxs-lookup"><span data-stu-id="54cce-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="54cce-116">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltokohteet** \> **Mallituoterakenteet**.</span><span class="sxs-lookup"><span data-stu-id="54cce-116">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="54cce-117">Avaa **Luo mallituoterakenne** -lomake painamalla CTRL + N -näppäinyhdistelmää.</span><span class="sxs-lookup"><span data-stu-id="54cce-117">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="54cce-118">Valitse **Kopioi tuoterakenteen rivit viitteestä** -kohdassa **Mallituoterakenne**-vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="54cce-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="54cce-119">Valitse **Viitenumero**-kentässä aiemmin luotu mallituoterakenne, jonka haluat kopioida uuteen mallituoterakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="54cce-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="54cce-120">Kirjoita **Nimi**-kenttään mallin nimi.</span><span class="sxs-lookup"><span data-stu-id="54cce-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="54cce-121">Kirjoita **Aloituspäivämäärä**- ja **Lopetuspäivämäärä**-kenttiin päivämääräväli, jolloin mallituoterakenne on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="54cce-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="54cce-122">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="54cce-122">Click **OK**.</span></span>

<span data-ttu-id="54cce-123">Järjestelmä luo uuden mallituoterakenteen käyttämällä rivejä, jotka vastaavat alkuperäistä mallituoterakennetta.</span><span class="sxs-lookup"><span data-stu-id="54cce-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="54cce-124">Mallituoterakenteen luominen nimikkeen tuoterakenteen perusteella</span><span class="sxs-lookup"><span data-stu-id="54cce-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="54cce-125">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltokohteet** \> **Mallituoterakenteet**.</span><span class="sxs-lookup"><span data-stu-id="54cce-125">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="54cce-126">Avaa **Luo mallituoterakenne** -lomake painamalla CTRL + N -näppäinyhdistelmää.</span><span class="sxs-lookup"><span data-stu-id="54cce-126">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="54cce-127">Valitse **Kopioi tuoterakenteen rivit viitteestä** -kohdassa **Tuoterakenne**.</span><span class="sxs-lookup"><span data-stu-id="54cce-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="54cce-128">Valitse **Viitenumero**-kentässä tuoterakenteen versio.</span><span class="sxs-lookup"><span data-stu-id="54cce-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="54cce-129">Tuoterakenne-tyyppinen nimike kopioidaan kohtaan **Nimikenumero**.</span><span class="sxs-lookup"><span data-stu-id="54cce-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="54cce-130">Kirjoita **Nimi**-kenttään mallin nimi.</span><span class="sxs-lookup"><span data-stu-id="54cce-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="54cce-131">Kirjoita **Aloituspäivämäärä**- ja **Lopetuspäivämäärä**-kenttiin päivämääräväli, jolloin mallituoterakenne on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="54cce-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="54cce-132">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="54cce-132">Click **OK**.</span></span>

<span data-ttu-id="54cce-133">Uusi mallituoterakenne luodaan käyttämällä rivejä, jotka vastaavat **Tuoterakenteet**-kohdassa mainitun tuoterakenteen rivejä.</span><span class="sxs-lookup"><span data-stu-id="54cce-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="54cce-134">Mallituoterakenteen luominen tuotannon tuoterakenteen perusteella</span><span class="sxs-lookup"><span data-stu-id="54cce-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="54cce-135">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltokohteet** \> **Mallituoterakenteet**.</span><span class="sxs-lookup"><span data-stu-id="54cce-135">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="54cce-136">Avaa **Luo mallituoterakenne** -lomake painamalla CTRL + N -näppäinyhdistelmää.</span><span class="sxs-lookup"><span data-stu-id="54cce-136">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="54cce-137">Valitse **Kopioi tuoterakenteen rivit viitteestä** -kohdassa **Tuotanto**.</span><span class="sxs-lookup"><span data-stu-id="54cce-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="54cce-138">Valitse **Viitenumero**-kentässä tuotannon tuoterakenne.</span><span class="sxs-lookup"><span data-stu-id="54cce-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="54cce-139">Kirjoita **Nimi**-kenttään mallin nimi.</span><span class="sxs-lookup"><span data-stu-id="54cce-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="54cce-140">Kirjoita **Aloituspäivämäärä**- ja **Lopetuspäivämäärä**-kenttiin päivämääräväli, jolloin mallituoterakenne on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="54cce-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="54cce-141">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="54cce-141">Click **OK**.</span></span>

<span data-ttu-id="54cce-142">Uusi mallituoterakenne luodaan käyttämällä rivejä, jotka vastaavat **Tuoterakenne**-kohdassa mainitun tuoterakenteen rivejä.</span><span class="sxs-lookup"><span data-stu-id="54cce-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="54cce-143">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="54cce-143">See also</span></span>

[<span data-ttu-id="54cce-144">Mallituoterakenteet </span><span class="sxs-lookup"><span data-stu-id="54cce-144">Template BOMs</span></span>](template-boms.md)

  


