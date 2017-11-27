---
title: "Määritä rivinimikkeen työnkulku"
description: "Tässä aiheessa kerrotaan rivinimiketyönkulkuelementin määrittämisestä."
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d30d6aeda6be7bc81763c0b3f20c568d3fc81526
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="configure-a-line-item-workflow"></a><span data-ttu-id="77d69-103">Määritä rivinimikkeen työnkulku</span><span class="sxs-lookup"><span data-stu-id="77d69-103">Configure a line-item workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="77d69-104">Tässä aiheessa kerrotaan rivinimiketyönkulkuelementin määrittämisestä.</span><span class="sxs-lookup"><span data-stu-id="77d69-104">This topic explains how to configure a line-item workflow element.</span></span>

<span data-ttu-id="77d69-105">Rivinimiketyönkulkuelementti konfiguroidaan työnkulkueditorissa napsauttamalla elementtiä hiiren kakkospainikkeella ja valitsemalla **Ominaisuudet**, joka avaa **Ominaisuudet**-sivun.</span><span class="sxs-lookup"><span data-stu-id="77d69-105">To configure a line-item workflow element, in the workflow editor, right-click the element, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="77d69-106">Seuraavien ohjeiden avulla voit sitten määrittää rivinimiketyönkulkuelementin eri ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="77d69-106">Then use the following procedures to configure the properties of the line-item workflow element.</span></span>

## <a name="name-the-line-item-workflow-element"></a><span data-ttu-id="77d69-107">rivinimiketyönkulkuelementin nimeäminen.</span><span class="sxs-lookup"><span data-stu-id="77d69-107">Name the line-item workflow element</span></span>
<span data-ttu-id="77d69-108">Kirjoita näiden ohjeiden avulla nimi rivinimiketyönkulkuelementille.</span><span class="sxs-lookup"><span data-stu-id="77d69-108">Follow these steps to enter a name for the line-item workflow element.</span></span>

1.  <span data-ttu-id="77d69-109">Napsauta vasemmassa ruudussa **Perusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="77d69-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="77d69-110">Kirjoita **Nimi**-kenttään rivinimiketyönkulkuelementin yksilöivä nimi.</span><span class="sxs-lookup"><span data-stu-id="77d69-110">In the **Name** field, enter a unique name for the line-item workflow element.</span></span>

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a><span data-ttu-id="77d69-111">Määritä, käytetäänkö samaa työnkulkua käsittelemään kaikki nimikkeet</span><span class="sxs-lookup"><span data-stu-id="77d69-111">Specify whether the same workflow is used to process all line items</span></span>
<span data-ttu-id="77d69-112">Voit määrittää seuraavasti, käytetäänkö samaa työnkulkua kaikkien nimikkeiden käsittelyyn asiakirjassa.</span><span class="sxs-lookup"><span data-stu-id="77d69-112">Follow these steps to specify whether the same workflow is used to process all the line items on a document.</span></span>

1.  <span data-ttu-id="77d69-113">Napsauta vasemmassa ruudussa **Perusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="77d69-113">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="77d69-114">Jos saman työnkulku käsittelee kaikki nimikkeet asiakirjassa, valitse **Käynnistä kaikille rivinimikkeille sama työnkulku**.</span><span class="sxs-lookup"><span data-stu-id="77d69-114">If the same workflow should process all the line items on a document, click **Invoke a single workflow for all line-items**.</span></span> <span data-ttu-id="77d69-115">Valitse työnkulku, joka käsittelee rivinimikkeet.</span><span class="sxs-lookup"><span data-stu-id="77d69-115">Then select the workflow to use to process the line items.</span></span>
3.  <span data-ttu-id="77d69-116">Jos tietty työnkulku käsittelee nimikkeet, jotka täyttävät tietyt ehdot, valitse **Käynnistä kullekin rivinimikkeelle eri työnkulku**.</span><span class="sxs-lookup"><span data-stu-id="77d69-116">If a specific workflow should process line items that meet a specific set of conditions, click **Invoke a workflow for each line-item**.</span></span> <span data-ttu-id="77d69-117">Noudata näitä ohjeita ja määritä ehtojoukko:</span><span class="sxs-lookup"><span data-stu-id="77d69-117">Then follow these steps to define the set of conditions:</span></span>
    1.  <span data-ttu-id="77d69-118">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="77d69-118">Click **Add**.</span></span>
    2.  <span data-ttu-id="77d69-119">Valitse ehto taulukosta.</span><span class="sxs-lookup"><span data-stu-id="77d69-119">Select the condition in the table.</span></span>
    3.  <span data-ttu-id="77d69-120">**Ehdon nimi** -välilehdessä kirjoita nimi ehtojoukolle, jotka määrität.</span><span class="sxs-lookup"><span data-stu-id="77d69-120">On the **Condition name** tab, enter a name for the set of conditions that you're defining.</span></span>
    4.  <span data-ttu-id="77d69-121">Kirjoita ehto valitsemalla **Lisää ehto**.</span><span class="sxs-lookup"><span data-stu-id="77d69-121">Click **Add condition** to enter a condition.</span></span>
    5.  <span data-ttu-id="77d69-122">Kirjoita kaikki muut tarvittavat ehdot.</span><span class="sxs-lookup"><span data-stu-id="77d69-122">Enter any additional conditions that are required.</span></span>
    6.  <span data-ttu-id="77d69-123">Voit tarkistaa, onko antamasi ehtojoukko määritetty oikein, valitsemalla **Testi**.</span><span class="sxs-lookup"><span data-stu-id="77d69-123">To verify that the set of conditions that you entered is configured correctly, click **Test**.</span></span> <span data-ttu-id="77d69-124">Valitse tietue **Testaa työnkulun ehto** -sivun **Tarkista ehto** -alueella ja valitse sitten **Testi**.</span><span class="sxs-lookup"><span data-stu-id="77d69-124">On the **Test workflow condition** page, in the **Validate condition** area, select a record, and then click **Test**.</span></span> <span data-ttu-id="77d69-125">Järjestelmä arvioi, täyttääkö tietue määrittämäsi ehdot.</span><span class="sxs-lookup"><span data-stu-id="77d69-125">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span> <span data-ttu-id="77d69-126">Palaa **Ominaisuudet**-sivulle valitsemalla **OK** tai **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="77d69-126">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

    <span data-ttu-id="77d69-127">Valitse **työnkulku** - välilehdessä työnkulku käsittelemään nimikkeet, jotka täyttävät määrittämäsi ehtojoukon.</span><span class="sxs-lookup"><span data-stu-id="77d69-127">On the **Workflow** tab, select the workflow select the workflow to use to process line items that meet the set of conditions that you defined.</span></span>





