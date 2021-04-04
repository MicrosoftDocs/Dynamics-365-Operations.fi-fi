---
title: Mallituoterakenteen luominen
description: Mallituoterakenteen voi luoda monella eri tavalla.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5afcb8171b674281faf8100d5c01fdff8d6ff764
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470759"
---
# <a name="create-a-template-bom"></a><span data-ttu-id="0e936-103">Mallituoterakenteen luominen</span><span class="sxs-lookup"><span data-stu-id="0e936-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="0e936-104">Mallituoterakenteen voi luoda millä tahansa seuraavista menetelmistä.</span><span class="sxs-lookup"><span data-stu-id="0e936-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="0e936-105">Kaikissa menetelmissä **Aloituspäivämäärä**- ja **Lopetuspäivämäärä**-kentät ovat valinnaisia ja vain tiedoksi.</span><span class="sxs-lookup"><span data-stu-id="0e936-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="0e936-106">Mallituoterakenteen luominen manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="0e936-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="0e936-107">Avaa **Huoltohallinta** \> **Asetukset** \> **Huoltokohteet** \> **Mallituoterakenteet**.</span><span class="sxs-lookup"><span data-stu-id="0e936-107">Go to **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="0e936-108">Valitse **Uusi** avataksesi **Luo mallituoterakenne** -lomakkeen.</span><span class="sxs-lookup"><span data-stu-id="0e936-108">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="0e936-109">Valitse **Kopioi tuoterakenteen rivit viitteestä** -kohdassa **Manuaalinen**-vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="0e936-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="0e936-110">Syötä **Nimikenumero**-kenttään **Tuoterakenne**-tyyppinen nimike.</span><span class="sxs-lookup"><span data-stu-id="0e936-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="0e936-111">Kirjoita **Nimi**-kenttään mallin nimi.</span><span class="sxs-lookup"><span data-stu-id="0e936-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="0e936-112">Kirjoita **Aloituspäivämäärä**- ja **Lopetuspäivämäärä**-kenttiin päivämääräväli, jolloin mallituoterakenne on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="0e936-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="0e936-113">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e936-113">Select **OK**.</span></span>

<span data-ttu-id="0e936-114">Järjestelmä luo uuden tyhjän mallituoterakenteen.</span><span class="sxs-lookup"><span data-stu-id="0e936-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="0e936-115">Mallituoterakenteen luominen toisen mallituoterakenteen perusteella</span><span class="sxs-lookup"><span data-stu-id="0e936-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="0e936-116">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltokohteet** \> **Mallituoterakenteet**.</span><span class="sxs-lookup"><span data-stu-id="0e936-116">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="0e936-117">Valitse **Uusi** avataksesi **Luo mallituoterakenne** -lomakkeen.</span><span class="sxs-lookup"><span data-stu-id="0e936-117">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="0e936-118">Valitse **Kopioi tuoterakenteen rivit viitteestä** -kohdassa **Mallituoterakenne**-vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="0e936-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="0e936-119">Valitse **Viitenumero**-kentässä aiemmin luotu mallituoterakenne, jonka haluat kopioida uuteen mallituoterakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="0e936-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="0e936-120">Kirjoita **Nimi**-kenttään mallin nimi.</span><span class="sxs-lookup"><span data-stu-id="0e936-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="0e936-121">Kirjoita **Aloituspäivämäärä**- ja **Lopetuspäivämäärä**-kenttiin päivämääräväli, jolloin mallituoterakenne on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="0e936-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="0e936-122">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e936-122">Select **OK**.</span></span>

<span data-ttu-id="0e936-123">Järjestelmä luo uuden mallituoterakenteen käyttämällä rivejä, jotka vastaavat alkuperäistä mallituoterakennetta.</span><span class="sxs-lookup"><span data-stu-id="0e936-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="0e936-124">Mallituoterakenteen luominen nimikkeen tuoterakenteen perusteella</span><span class="sxs-lookup"><span data-stu-id="0e936-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="0e936-125">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltokohteet** \> **Mallituoterakenteet**.</span><span class="sxs-lookup"><span data-stu-id="0e936-125">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="0e936-126">Valitse **Uusi** avataksesi **Luo mallituoterakenne** -lomakkeen.</span><span class="sxs-lookup"><span data-stu-id="0e936-126">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="0e936-127">Valitse **Kopioi tuoterakenteen rivit viitteestä** -kohdassa **Tuoterakenne**.</span><span class="sxs-lookup"><span data-stu-id="0e936-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="0e936-128">Valitse **Viitenumero**-kentässä tuoterakenteen versio.</span><span class="sxs-lookup"><span data-stu-id="0e936-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="0e936-129">Tuoterakenne-tyyppinen nimike kopioidaan kohtaan **Nimikenumero**.</span><span class="sxs-lookup"><span data-stu-id="0e936-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="0e936-130">Kirjoita **Nimi**-kenttään mallin nimi.</span><span class="sxs-lookup"><span data-stu-id="0e936-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="0e936-131">Kirjoita **Aloituspäivämäärä**- ja **Lopetuspäivämäärä**-kenttiin päivämääräväli, jolloin mallituoterakenne on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="0e936-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="0e936-132">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e936-132">Select **OK**.</span></span>

<span data-ttu-id="0e936-133">Uusi mallituoterakenne luodaan käyttämällä rivejä, jotka vastaavat **Tuoterakenteet**-kohdassa mainitun tuoterakenteen rivejä.</span><span class="sxs-lookup"><span data-stu-id="0e936-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="0e936-134">Mallituoterakenteen luominen tuotannon tuoterakenteen perusteella</span><span class="sxs-lookup"><span data-stu-id="0e936-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="0e936-135">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltokohteet** \> **Mallituoterakenteet**.</span><span class="sxs-lookup"><span data-stu-id="0e936-135">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="0e936-136">Valitse **Uusi** avataksesi **Luo mallituoterakenne** -lomakkeen.</span><span class="sxs-lookup"><span data-stu-id="0e936-136">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="0e936-137">Valitse **Kopioi tuoterakenteen rivit viitteestä** -kohdassa **Tuotanto**.</span><span class="sxs-lookup"><span data-stu-id="0e936-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="0e936-138">Valitse **Viitenumero**-kentässä tuotannon tuoterakenne.</span><span class="sxs-lookup"><span data-stu-id="0e936-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="0e936-139">Kirjoita **Nimi**-kenttään mallin nimi.</span><span class="sxs-lookup"><span data-stu-id="0e936-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="0e936-140">Kirjoita **Aloituspäivämäärä**- ja **Lopetuspäivämäärä**-kenttiin päivämääräväli, jolloin mallituoterakenne on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="0e936-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="0e936-141">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e936-141">Select **OK**.</span></span>

<span data-ttu-id="0e936-142">Uusi mallituoterakenne luodaan käyttämällä rivejä, jotka vastaavat **Tuoterakenne**-kohdassa mainitun tuoterakenteen rivejä.</span><span class="sxs-lookup"><span data-stu-id="0e936-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="0e936-143">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="0e936-143">See also</span></span>

[<span data-ttu-id="0e936-144">Mallituoterakenteet </span><span class="sxs-lookup"><span data-stu-id="0e936-144">Template BOMs</span></span>](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]