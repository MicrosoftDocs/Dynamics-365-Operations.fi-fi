---
title: Valmistettujen nimikkeiden standardikustannusten ylläpitämisen valmistelutoimet
description: Tässä ohjeaiheessa käsitellään valmistettujen nimikkeiden ylläpitokustannusten valmisteluvaiheita.
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fbd7344f3d542cbd46e3568d8a7911ab4ab53b17
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545945"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a><span data-ttu-id="32a09-103">Valmistettujen nimikkeiden standardikustannusten ylläpitämisen valmistelutoimet</span><span class="sxs-lookup"><span data-stu-id="32a09-103">Prepare to maintain standard costs for manufactured items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32a09-104">Tässä ohjeaiheessa käsitellään valmistettujen nimikkeiden ylläpitokustannusten valmisteluvaiheita.</span><span class="sxs-lookup"><span data-stu-id="32a09-104">This topic describes the steps for preparing to maintain costs for manufactured items.</span></span> <span data-ttu-id="32a09-105">Valmistettujen nimikkeiden vaiheet vaihtelevat hieman ostettujen nimikkeiden vaiheista.</span><span class="sxs-lookup"><span data-stu-id="32a09-105">The steps for manufactured items differ slightly from the steps for purchased items.</span></span>

<span data-ttu-id="32a09-106">Valmistettuihin nimikkeisiin määritetyt menettelytavat voivat vaikuttaa valmistettujen päänimikkeiden kustannusten laskentaan.</span><span class="sxs-lookup"><span data-stu-id="32a09-106">Policies that are assigned to manufactured items can affect the cost calculations for the parent manufactured items.</span></span> <span data-ttu-id="32a09-107">Valmistele valmistettujen nimikkeiden ylläpitokustannukset seuraavien vaiheiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="32a09-107">To prepare to maintain costs for manufactured items, follow these steps.</span></span>

1. <span data-ttu-id="32a09-108">Määritä nimikemalliryhmä valmistettuun nimikkeeseen.</span><span class="sxs-lookup"><span data-stu-id="32a09-108">Assign an item model group to the manufactured item.</span></span> 

   <span data-ttu-id="32a09-109">Nimikemalliryhmä määrittää, että käytetään standardikustannuksia.</span><span class="sxs-lookup"><span data-stu-id="32a09-109">The item model group identifies that standard costs will be used.</span></span>

2. <span data-ttu-id="32a09-110">Määritä nimikeryhmä valmistettuun nimikkeeseen.</span><span class="sxs-lookup"><span data-stu-id="32a09-110">Assign an item group to the manufactured item.</span></span> 

   <span data-ttu-id="32a09-111">Nimikeryhmä sisältää valmistettua nimikettä koskevia kirjanpitotilejä.</span><span class="sxs-lookup"><span data-stu-id="32a09-111">The item group contains ledger accounts that apply to the manufactured item.</span></span> <span data-ttu-id="32a09-112">Standardikustannusvarastomallia käyttävän valmistetun nimikkeen kirjanpitotileissä on mukana useita tuotantovariansseja, kustannuksen muutoksen varianssi ja varastokustannuksen uudelleenarvostus.</span><span class="sxs-lookup"><span data-stu-id="32a09-112">The ledger accounts for a manufactured item that has a standard cost inventory model include several production variances, the cost change variance, and the inventory cost revaluation.</span></span>

3. <span data-ttu-id="32a09-113">Määritä varaston mittayksikkö nimikkeeseen.</span><span class="sxs-lookup"><span data-stu-id="32a09-113">Assign the inventory unit of measure to the item.</span></span> 

   <span data-ttu-id="32a09-114">Nimikkeen kustannukset ilmoitetaan aina nimikkeen varaston mittayksiköinä.</span><span class="sxs-lookup"><span data-stu-id="32a09-114">The item's costs are always expressed in the item's inventory unit of measure.</span></span>

4. <span data-ttu-id="32a09-115">Älä määritä kustannusryhmään valmistettuun nimikkeeseen, ellei nimikettä käsitellä ostettuna nimikkeenä.</span><span class="sxs-lookup"><span data-stu-id="32a09-115">Don't assign a cost group to the manufactured item unless the item will be treated as a purchased item.</span></span>

5. <span data-ttu-id="32a09-116">Määritä tuoterakenteen laskentaryhmä valmistettuun nimikkeeseen.</span><span class="sxs-lookup"><span data-stu-id="32a09-116">Assign a bill of materials (BOM) calculation group to the manufactured item.</span></span> 

   <span data-ttu-id="32a09-117">Nimikkeen tuoterakenteen laskentaryhmä määrittää sovellettavat varoitusehdot.</span><span class="sxs-lookup"><span data-stu-id="32a09-117">The item's BOM calculation group defines warning conditions that apply.</span></span> <span data-ttu-id="32a09-118">Tällä tavoin tuoterakenteen laskennan valmistumisen jälkeen voidaan muodostaa varoitussanomia mahdollista laskentavirheiden lähteistä.</span><span class="sxs-lookup"><span data-stu-id="32a09-118">In that way, when a BOM calculation is done, warning messages can be generated about possible sources of calculation errors.</span></span> <span data-ttu-id="32a09-119">Varoitussanoma voi esimerkiksi ilmoittaa, että valittua tuoterakennetta tai reittiä ei ole.</span><span class="sxs-lookup"><span data-stu-id="32a09-119">For example, a warning message can identify when an active BOM or route doesn't exist.</span></span> <span data-ttu-id="32a09-120">Tuoterakenteen laskentaryhmä sisältää hajotuksen lopettamisen menettelytavan, joka määrittää, milloin valmistettua nimikettä on käsiteltävä ostettuna nimikkeenä.</span><span class="sxs-lookup"><span data-stu-id="32a09-120">The BOM calculation group contains a stop explosion policy that indicates when a manufactured item should be treated as a purchased item.</span></span>

6. <span data-ttu-id="32a09-121">Jos valmistetulla nimikkeellä on vakiokustannukset, määritä sille vakiotilausmäärä.</span><span class="sxs-lookup"><span data-stu-id="32a09-121">If the manufactured item has constant costs, assign a standard order quantity to it.</span></span> 

   <span data-ttu-id="32a09-122">Vakiotilausmäärä on kirjanpidon eräkoko vakiokustannusten kuolettamisessa.</span><span class="sxs-lookup"><span data-stu-id="32a09-122">The standard order quantity is an accounting lot size for amortizing constant costs.</span></span> <span data-ttu-id="32a09-123">Esimerkkejä vakiokustannuksista ovat reititystyövaiheiden määritysajat ja tuoterakenteen komponenttien vakiomäärä.</span><span class="sxs-lookup"><span data-stu-id="32a09-123">Examples of constant costs include setup times in routing operations and a constant component quantity in the BOM.</span></span>

7. <span data-ttu-id="32a09-124">Määritä valmistetun nimikkeen tuoterakenne.</span><span class="sxs-lookup"><span data-stu-id="32a09-124">Define the BOM for the manufactured item.</span></span> 

   <span data-ttu-id="32a09-125">Valmistetulle nimikkeelle voi määrittää tuoterakenneversioita.</span><span class="sxs-lookup"><span data-stu-id="32a09-125">One or more BOM versions can be defined for the manufactured item.</span></span> <span data-ttu-id="32a09-126">Varmista, että haluamasi versiot on merkitty hyväksytyiksi ja aktiivisiksi ja että niillä on haluamasi voimaantulopäivät.</span><span class="sxs-lookup"><span data-stu-id="32a09-126">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="32a09-127">Tuoterakenneversio voi olla koko yrityksen laajuinen tai toimipaikkakohtainen.</span><span class="sxs-lookup"><span data-stu-id="32a09-127">The BOM version can be company-wide or site-specific.</span></span>

8. <span data-ttu-id="32a09-128">Määritä valmistetun nimikkeen reititys.</span><span class="sxs-lookup"><span data-stu-id="32a09-128">Define the routing for the manufactured item.</span></span> 

   <span data-ttu-id="32a09-129">Valmistetulle nimikkeelle voi määrittää reititysversioita.</span><span class="sxs-lookup"><span data-stu-id="32a09-129">One or more route versions can be defined for the manufactured item.</span></span> <span data-ttu-id="32a09-130">Varmista, että haluamasi versiot on merkitty hyväksytyiksi ja aktiivisiksi ja että niillä on haluamasi voimaantulopäivät.</span><span class="sxs-lookup"><span data-stu-id="32a09-130">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="32a09-131">Reititysversion täytyy olla toimipaikkakohtainen.</span><span class="sxs-lookup"><span data-stu-id="32a09-131">The route version must be site-specific.</span></span>

<span data-ttu-id="32a09-132">Jos haluat käyttää reititystietoja kustannuslaskelmissa, valmisteluun tarvitaan lisävaiheita.</span><span class="sxs-lookup"><span data-stu-id="32a09-132">If you want to use routing information for costing purposes, additional preparation steps are required.</span></span> <span data-ttu-id="32a09-133">Esimerkiksi reitityksen työvaiheisiin määritettävien kustannusluokkien täytyy olla oikeita ja valmiita.</span><span class="sxs-lookup"><span data-stu-id="32a09-133">For example, the cost categories that are assigned to routing operations must be correct and completed.</span></span>

<a name="related-topics"></a><span data-ttu-id="32a09-134">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="32a09-134">Related topics</span></span>
--------

[<span data-ttu-id="32a09-135">Valmistetun nimikkeen vakiokustannusten kuolettaminen</span><span class="sxs-lookup"><span data-stu-id="32a09-135">Amortize constant costs for a manufactured item</span></span>](amortize-constant-costs-manufactured-item.md)

[<span data-ttu-id="32a09-136">Tuotettavissa tai hankittavissa olevien tuotteiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="32a09-136">Set up products that can be produced or procured</span></span>](manufactured-items-treated-as-purchased-items.md)

