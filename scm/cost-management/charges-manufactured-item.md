---
title: "Näytä valmistetun nimikkeen kulut"
description: "Valmistetun nimikkeen vakiokustannukset kuvastavat toimintojen asetusaikoja sekä komponentteja, joilla on vakiomäärä tai hävikin vakiomäärä."
author: YuyuScheller
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 274483
ms.assetid: 6f5b851b-c5a7-43ef-b380-0d316667c1ef
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 9f41939554cd22045940af937f227f43ba098394
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---

# <a name="display-charges-for-a-manufactured-item"></a><span data-ttu-id="80bec-103">Näytä valmistetun nimikkeen kulut</span><span class="sxs-lookup"><span data-stu-id="80bec-103">Display charges for a manufactured item</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="80bec-104">Valmistetun nimikkeen vakiokustannukset kuvastavat toimintojen asetusaikoja sekä komponentteja, joilla on vakiomäärä tai hävikin vakiomäärä.</span><span class="sxs-lookup"><span data-stu-id="80bec-104">The constant costs of a manufactured item reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span>

<span data-ttu-id="80bec-105">Nimikkeen kulujen lasketun summan voi näyttää nimikkeen yksikkökustannuksissa.</span><span class="sxs-lookup"><span data-stu-id="80bec-105">The calculated amount of an item's charges can be displayed with the item's unit costs.</span></span> <span data-ttu-id="80bec-106">Kulut näytetään toisinaan erillisissä kentissä, eikä niitä näytetä osana nimikkeen yksikkökustannusta.</span><span class="sxs-lookup"><span data-stu-id="80bec-106">However, the charges are sometimes displayed as separate fields, and they are not included in the item's unit costs.</span></span> <span data-ttu-id="80bec-107">Kun kulut näytetään erillisissä kentissä, yhdessä kentässä näkyy kulujen kokonaissumma ja toisessa kustannuslaskennan eräkoko, jota käytettiin summan kuolettamisessa.</span><span class="sxs-lookup"><span data-stu-id="80bec-107">When the charges appear as separate fields, one field displays the total amount of charges, and another field displays the costing lot size that is used to amortize the amount.</span></span> <span data-ttu-id="80bec-108">Kulut näytetään erillisissä kentissä esimerkiksi Nimikkeen hinta -sivulla.</span><span class="sxs-lookup"><span data-stu-id="80bec-108">The Item price page, for example, displays the charges as two separate fields.</span></span> <span data-ttu-id="80bec-109">Valmis-sivulla näytetään kuitenkin nimikkeen yksikkökohtainen kokonaiskustannus; kuoletetut kustannukset sisältyvät yksikkökustannuksiin.</span><span class="sxs-lookup"><span data-stu-id="80bec-109">However, the Complete page displays the item's total cost per unit, and the amortized costs are included in the unit costs.</span></span>
<span data-ttu-id="80bec-110">Valmistetun nimikkeen kulut sisältyvät aina nimikkeen yksikkökustannukseen standardikustannustarkoituksia varten.</span><span class="sxs-lookup"><span data-stu-id="80bec-110">The charges for a manufactured item are always included in the item's unit cost for standard cost purposes.</span></span> <span data-ttu-id="80bec-111">Ne voi vaihtoehtoisesti sisällyttää suunniteltuihin kustannustarkoituksiin.</span><span class="sxs-lookup"><span data-stu-id="80bec-111">They can optionally be included for planned cost purposes.</span></span> <span data-ttu-id="80bec-112">Kustannuslaskentaversion käytännön perusteella muut kulut on sisällytettävä valmistetun nimikkeen kustannuksiin.</span><span class="sxs-lookup"><span data-stu-id="80bec-112">A policy in the costing version enforces the inclusion of charges in the cost of a manufactured item.</span></span> <span data-ttu-id="80bec-113">Kun aktivoit nimikkeen kustannustietueen, se päivittää kulut nimikkeen peruskustannustietoihin, jotka näkyvät Nimikkeen hinta -sivulla.</span><span class="sxs-lookup"><span data-stu-id="80bec-113">When you activate an item's cost record, you update the charges for the item's base cost information, which is displayed in the Item price page.</span></span> <span data-ttu-id="80bec-114">Kulut näytetään erillisissä kentissä, eikä niitä näytetä osana nimikkeen yksikkökustannusta.</span><span class="sxs-lookup"><span data-stu-id="80bec-114">The charges are displayed as two separate fields, and they are not included in the item's unit cost.</span></span> <span data-ttu-id="80bec-115">Kukin aktivointi päivittää nimikkeen peruskustannustiedot, vaikka aktivointi koskisi eri toimipaikkoja.</span><span class="sxs-lookup"><span data-stu-id="80bec-115">Each activation updates the item's base cost information, even if the activation reflects different sites.</span></span> <span data-ttu-id="80bec-116">Tämän vuoksi peruskustannustietoihin kannattaa suhtautua viitetietoina.</span><span class="sxs-lookup"><span data-stu-id="80bec-116">Therefore, you should view the base cost information as reference information.</span></span>






