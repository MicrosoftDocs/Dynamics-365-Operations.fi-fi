---
title: Standardikustannusten kustannuslaskelmaversioiden rajoitukset
description: Tässä ohjeaiheessa käsitellään standardikustannusten kustannuslaskelmaversiota koskevia rajoituksia.
author: AndersGirke
manager: tfehr
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f8f5707b6f51372684606d135c0643b36e3a94f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245248"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a><span data-ttu-id="32fd7-103">Standardikustannusten kustannuslaskelmaversioiden rajoitukset</span><span class="sxs-lookup"><span data-stu-id="32fd7-103">Restrictions on costing versions for standard costs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32fd7-104">Tässä ohjeaiheessa käsitellään standardikustannusten kustannuslaskelmaversiota koskevia rajoituksia.</span><span class="sxs-lookup"><span data-stu-id="32fd7-104">This topic describes the restrictions that apply to a costing version for standard costs.</span></span> 

<span data-ttu-id="32fd7-105">Seuraavilla rajoituksilla voidaan varmistaa standardikustannuksen laskennan periaatteiden noudattaminen:</span><span class="sxs-lookup"><span data-stu-id="32fd7-105">The following restrictions help guarantee adherence to standard costing principles:</span></span>

-  <span data-ttu-id="32fd7-106">Kulut on sisällytettävä nimikkeen kustannukseen.</span><span class="sxs-lookup"><span data-stu-id="32fd7-106">Charges must be included in an item's cost.</span></span> <span data-ttu-id="32fd7-107">Valmistetun nimikkeen kulut tulevat tuoterakenteen ja reittitietojen kuoletetuista standardikustannuksista.</span><span class="sxs-lookup"><span data-stu-id="32fd7-107">The charges for a manufactured item represent the amortized constant costs in the bill of materials (BOM) and route information.</span></span> <span data-ttu-id="32fd7-108">Tämän vuoksi on sisällytettävä yksikkökustannukseen.</span><span class="sxs-lookup"><span data-stu-id="32fd7-108">Therefore, the charges must be included in the unit cost.</span></span> <span data-ttu-id="32fd7-109">Myös ostetun nimikkeen kulut sisällytetään nimikkeen yksikkökustannukseen.</span><span class="sxs-lookup"><span data-stu-id="32fd7-109">The charges for a purchased item are also included in the item's unit cost.</span></span>

-  <span data-ttu-id="32fd7-110">Valmistettujen nimikkeiden standardikustannusten laskennan on perustuttava standardikustannusten kustannuslaskelmaversiossa oleviin kustannustietueisiin.</span><span class="sxs-lookup"><span data-stu-id="32fd7-110">Calculation of standard costs for manufactured items must be based on the cost records in a costing version for standard costs.</span></span> <span data-ttu-id="32fd7-111">Vaihtoehtoisia kustannustietojen lähteitä voi käyttää vain suunniteltujen kustannusten kustannuslaskelmaversion kanssa, kuten ostettujen nimikkeiden ostohintakauppasopimusten kanssa.</span><span class="sxs-lookup"><span data-stu-id="32fd7-111">Alternative sources of cost data can be used only with a costing version for planned costs, such as purchase price trade agreements for purchased items.</span></span> <span data-ttu-id="32fd7-112">Tuoterakenteen laskentaryhmä määrittää vaihtoehtoiset kustannustietolähteet.</span><span class="sxs-lookup"><span data-stu-id="32fd7-112">Alternative sources of cost data are defined by the BOM calculation group.</span></span>

-  <span data-ttu-id="32fd7-113">Tuoterakennelaskelmat on tehtävä yksitasoisena hajotustilana.</span><span class="sxs-lookup"><span data-stu-id="32fd7-113">BOM calculations must be performed in a single-level explosion mode.</span></span>

<span data-ttu-id="32fd7-114">Vakiokustannusten nimikekustannustiedot voi kopioida toiseen kustannuslaskelmaversioon, joka sisältää vakiokustannuksia tai suunniteltuja kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="32fd7-114">The item cost data for standard costs can be copied to another costing version that contains standard costs or planned costs.</span></span> <span data-ttu-id="32fd7-115">Suunniteltujen kustannusten nimikekustannustietoja ei kuitenkaan voi kopioida standardikustannuksia sisältävään kustannuslaskelmaversioon, koska tässä ohjeaiheessa luetellut rajoitukset eivät koskisi suunniteltuja kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="32fd7-115">However, the item cost data for planned costs can't be copied to a cost version that contains standard costs, because the restrictions that are listed earlier in this topic don't apply to planned costs.</span></span>

<a name="related-topics"></a><span data-ttu-id="32fd7-116">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="32fd7-116">Related topics</span></span>
--------

[<span data-ttu-id="32fd7-117">Kustannuslaskelmaversiot – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="32fd7-117">Costing versions overview</span></span>](costing-versions.md)

[<span data-ttu-id="32fd7-118">Standardikustannusten päivittäminen muussa kuin valmistusympäristössä</span><span class="sxs-lookup"><span data-stu-id="32fd7-118">Update standard costs in a non-manufacturing environment</span></span>](update-standard-costs-non-manufacturing-environment.md)

[<span data-ttu-id="32fd7-119">Valmistettujen nimikkeiden standardikustannusten ylläpitämisen valmistelutoimet</span><span class="sxs-lookup"><span data-stu-id="32fd7-119">Prepare to maintain standard costs for manufactured items</span></span>](update-standard-costs-manufacturing-environment.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]