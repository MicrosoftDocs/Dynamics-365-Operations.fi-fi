---
title: Viittaukset alkuperäisiin laskuihin hyvityslaskuissa
description: Tässä aiheessa kerrotaan, miten liittyvissä hyvityslaskuissa määritetään ja tulostetaan alkuperäiset laskunumerot.
author: ilkond
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 673288f04b33aa2a578f9e2e7913dbe7ac309644
ms.sourcegitcommit: 7cdec5469ff0da145ac4e01caf3287d0627ae2dc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2021
ms.locfileid: "5099999"
---
# <a name="references-to-original-invoices-in-credit-notes"></a><span data-ttu-id="0aeab-103">Viittaukset alkuperäisiin laskuihin hyvityslaskuissa</span><span class="sxs-lookup"><span data-stu-id="0aeab-103">References to original invoices in credit notes</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="0aeab-104">Joissakin maissa ja joillakin alueilla on lakisääteinen vaatimus, että tulostetut hyvityslaskut sisältävät viittauksia alkuperäisiin laskuihin.</span><span class="sxs-lookup"><span data-stu-id="0aeab-104">In some countries and regions, there is a legal requirement that printed credit notes include references to the original invoices.</span></span> <span data-ttu-id="0aeab-105">Tässä aiheessa kerrotaan, miten liittyvissä hyvityslaskuissa määritetään ja tulostetaan alkuperäiset laskunumerot.</span><span class="sxs-lookup"><span data-stu-id="0aeab-105">This topic explains how to set up and print the original invoice numbers in related credit notes.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0aeab-106">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="0aeab-106">Prerequisites</span></span>

- <span data-ttu-id="0aeab-107">Ota **Toimintohallinta**-työtilassa **Myynti- ja projektilaskuraporttien hyvityslaskutusasettelu** -ominaisuus käyttöön.</span><span class="sxs-lookup"><span data-stu-id="0aeab-107">In the **Feature management** workspace, turn on the **Credit invoicing layout for sales and project invoice reports** feature.</span></span> <span data-ttu-id="0aeab-108">Lisätietoja on kohdassa [Toiminnon hallinnan yleiskatsaus](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0aeab-108">For more information, see [Feature management overview](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="0aeab-109">Tarvittavien tiedostojen tulostettavat muodot on konfiguroitava tulostuksenhallinnassa.</span><span class="sxs-lookup"><span data-stu-id="0aeab-109">The printable formats of the required documents must be configured in Print management.</span></span>

<span data-ttu-id="0aeab-110">Tässä ohjeaiheessa kuvatut toiminnot koskevat seuraavia asiakirjoja:</span><span class="sxs-lookup"><span data-stu-id="0aeab-110">The functionality that is described in this topic applies to the following documents:</span></span>

<span data-ttu-id="0aeab-111">**Myyntireskontra**</span><span class="sxs-lookup"><span data-stu-id="0aeab-111">**Accounts receivable**</span></span>

- <span data-ttu-id="0aeab-112">Vapaamuotoinen hyvityslasku</span><span class="sxs-lookup"><span data-stu-id="0aeab-112">Free text credit note</span></span>
- <span data-ttu-id="0aeab-113">Asiakkaan hyvityslasku</span><span class="sxs-lookup"><span data-stu-id="0aeab-113">Customer credit note</span></span>

<span data-ttu-id="0aeab-114">**Projektinhallinta ja kirjanpito**</span><span class="sxs-lookup"><span data-stu-id="0aeab-114">**Project management and accounting**</span></span>

- <span data-ttu-id="0aeab-115">Projektin hyvityslasku</span><span class="sxs-lookup"><span data-stu-id="0aeab-115">Project credit note</span></span>

## <a name="configure-accounts-receivable-parameters"></a><span data-ttu-id="0aeab-116">Myyntireskontran parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0aeab-116">Configure Accounts receivable parameters</span></span>

<span data-ttu-id="0aeab-117">Seuraavia ohjeita noudattamalla voit määrittää parametrin, joka määrittää, tulostetaanko liittyviin hyvityslaskuihin viitteet alkuperäisiin laskuihin.</span><span class="sxs-lookup"><span data-stu-id="0aeab-117">Follow these steps to set the parameter that controls whether references to the original invoices are printed in related credit notes.</span></span>

1. <span data-ttu-id="0aeab-118">Valitse **Myyntireskontra** \> **Määritys** \> **Myyntireskontran parametrit**.</span><span class="sxs-lookup"><span data-stu-id="0aeab-118">Go to **Accounts receivable** \> **Setup** \> **Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="0aeab-119">Määritä **Päivitykset**-välilehden **Lasku**-pikavälilehdessä **Käytä myynti- ja projektilaskuraporteissa hyvityslaskutusasettelua** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="0aeab-119">On the **Updates** tab, on the **Invoice** FastTab, set the **Apply the credit invoicing layout into sales and project invoice reports** option to **Yes**.</span></span>

![Myyntireskontran parametrien määrittäminen](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a><span data-ttu-id="0aeab-121">Viittausten määrittäminen alkuperäisiin laskuihin</span><span class="sxs-lookup"><span data-stu-id="0aeab-121">Define references to original invoices</span></span>

<span data-ttu-id="0aeab-122">Seuraavien menetelmien avulla voit määrittää viittaukset alkuperäisiin laskuihin tiedostotyypin perusteella.</span><span class="sxs-lookup"><span data-stu-id="0aeab-122">Use the following procedures to define references to original invoices, based on the document type.</span></span>

### <a name="free-text-credit-note"></a><span data-ttu-id="0aeab-123">Vapaamuotoinen hyvityslasku</span><span class="sxs-lookup"><span data-stu-id="0aeab-123">Free text credit note</span></span>

1. <span data-ttu-id="0aeab-124">Siirry kohtaan **Myyntisaamiset** \> **Laskut** \> **Kaikki vapaatekstilaskut**.</span><span class="sxs-lookup"><span data-stu-id="0aeab-124">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="0aeab-125">Luo uusi hyvityslasku tai valitse aiemmin luotu hyvityslasku.</span><span class="sxs-lookup"><span data-stu-id="0aeab-125">Create a new credit note, or select an existing credit note.</span></span>
3. <span data-ttu-id="0aeab-126">Avaa lasku.</span><span class="sxs-lookup"><span data-stu-id="0aeab-126">Open the invoice.</span></span>
4. <span data-ttu-id="0aeab-127">Valitse Toimintoruudun **Laskutus**-välilehden **Toiminnot**-ryhmässä **Hyvityslaskutus**.</span><span class="sxs-lookup"><span data-stu-id="0aeab-127">On the Action Pane, on the **Invoice** tab, in the **Functions** group, select **Credit invoicing**.</span></span>
5. <span data-ttu-id="0aeab-128">Kirjoita viittaus alkuperäiseen laskuun ja valitse korjauksen syy.</span><span class="sxs-lookup"><span data-stu-id="0aeab-128">Enter the reference to the original invoice, and select the reason for the correction.</span></span>

![Vapaatekstilaskun viitteen määrittäminen](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a><span data-ttu-id="0aeab-130">Asiakkaan hyvityslasku</span><span class="sxs-lookup"><span data-stu-id="0aeab-130">Customer credit note</span></span>

1. <span data-ttu-id="0aeab-131">Valitse **Myyntireskontra** \> **Tilaukset** \> **Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="0aeab-131">Go to **Accounts receivable** \> **Orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="0aeab-132">Valitse ja avaa laskutettu myyntitilaus, joka on korjattava.</span><span class="sxs-lookup"><span data-stu-id="0aeab-132">Select and open the invoiced sales order that must be corrected.</span></span>
3. <span data-ttu-id="0aeab-133">Valitse Toimintoruudun **Myynti**-välilehden **Hyvityslasku**-ryhmässä **Hyvityslasku**.</span><span class="sxs-lookup"><span data-stu-id="0aeab-133">On the Action Pane, on the **Sell** tab, in the **Credit note** group, select **Credit note**.</span></span>
4. <span data-ttu-id="0aeab-134">Anna korjauksen syy.</span><span class="sxs-lookup"><span data-stu-id="0aeab-134">Enter the reason for the correction.</span></span> <span data-ttu-id="0aeab-135">Viittaus alkuperäiseen laskuun määritetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="0aeab-135">The reference to the original invoice is automatically established.</span></span>

![Myyntitilauksen viitteen määrittäminen](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a><span data-ttu-id="0aeab-137">Projektin hyvityslasku</span><span class="sxs-lookup"><span data-stu-id="0aeab-137">Project credit note</span></span>

1. <span data-ttu-id="0aeab-138">Valitse **Projektinhallinta ja kirjanpito** \> **Projektin laskut** \> **Projektin laskut**.</span><span class="sxs-lookup"><span data-stu-id="0aeab-138">Go to **Project management and accounting** \> **Project invoices** \> **Project invoices**.</span></span>
2. <span data-ttu-id="0aeab-139">Valitse ja avaa projektilasku, joka on korjattava.</span><span class="sxs-lookup"><span data-stu-id="0aeab-139">Select and open the project invoice that must be corrected.</span></span>
3. <span data-ttu-id="0aeab-140">Valitse Toimintoruudun **Projektilasku**-välilehden **Toiminnot**-ryhmässä **Valitse hyvityslaskua varten**.</span><span class="sxs-lookup"><span data-stu-id="0aeab-140">On the Action Pane, on the **Project invoice** tab, in the **Functions** group, select **Select for credit note**.</span></span>
4. <span data-ttu-id="0aeab-141">Valitse **Hyvityslaskutus**.</span><span class="sxs-lookup"><span data-stu-id="0aeab-141">Select **Credit invoicing**.</span></span>
5. <span data-ttu-id="0aeab-142">Anna korjauksen syy.</span><span class="sxs-lookup"><span data-stu-id="0aeab-142">Enter the reason for the correction.</span></span> <span data-ttu-id="0aeab-143">Viittaus alkuperäiseen laskuun määritetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="0aeab-143">The reference to the original invoice is automatically established.</span></span>

![Projektilaskun viitteen määrittäminen](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a><span data-ttu-id="0aeab-145">Hyvityslaskujen tulostaminen</span><span class="sxs-lookup"><span data-stu-id="0aeab-145">Printing credit notes</span></span>

<span data-ttu-id="0aeab-146">Kun tulostat vapaateksti-, asiakas- ja projektihyvityslaskuja, ne sisältävät viitteen alkuperäiseen laskuun sekä korjauksen syyn.</span><span class="sxs-lookup"><span data-stu-id="0aeab-146">When you print free text, customer, and project credit notes, they will include the reference to the original invoice and the correction reason.</span></span>

![Tulostettu hyvityslasku](media/credit-note-FTI.jpg)

> [!NOTE]
> <span data-ttu-id="0aeab-148">Varmista, että tiedostojen tulostettavat muodot on määritetty oikein sillä olettamuksella, että viitteet alkuperäisiin laskuihin tulostetaan.</span><span class="sxs-lookup"><span data-stu-id="0aeab-148">Make sure that the printable formats of the documents are correctly configured, on the assumption that references to original invoices will be printed.</span></span>
