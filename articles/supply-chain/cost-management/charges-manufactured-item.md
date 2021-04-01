---
title: Näytä valmistetun nimikkeen kulut
description: Valmistetun nimikkeen vakiokustannukset kuvastavat toimintojen asetusaikoja sekä komponentteja, joilla on vakiomäärä tai hävikin vakiomäärä.
author: AndersGirke
manager: tfehr
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.custom: 274483
ms.assetid: 6f5b851b-c5a7-43ef-b380-0d316667c1ef
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: f8d7fd7488630d9d24d5d7dc31ea39a10385a290
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235505"
---
# <a name="display-charges-for-a-manufactured-item"></a><span data-ttu-id="f8b0b-103">Näytä valmistetun nimikkeen kulut</span><span class="sxs-lookup"><span data-stu-id="f8b0b-103">Display charges for a manufactured item</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8b0b-104">Valmistetun nimikkeen vakiokustannukset kuvastavat toimintojen asetusaikoja sekä komponentteja, joilla on vakiomäärä tai hävikin vakiomäärä.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-104">The constant costs of a manufactured item reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span>

<span data-ttu-id="f8b0b-105">Nimikkeen kulujen lasketun summan voi näyttää nimikkeen yksikkökustannuksissa.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-105">The calculated amount of an item's charges can be displayed with the item's unit costs.</span></span> <span data-ttu-id="f8b0b-106">Kulut näytetään toisinaan erillisissä kentissä, eikä niitä näytetä osana nimikkeen yksikkökustannusta.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-106">However, the charges are sometimes displayed as separate fields, and they are not included in the item's unit costs.</span></span> <span data-ttu-id="f8b0b-107">Kun kulut näytetään erillisissä kentissä, yhdessä kentässä näkyy kulujen kokonaissumma ja toisessa kustannuslaskennan eräkoko, jota käytettiin summan kuolettamisessa.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-107">When the charges appear as separate fields, one field displays the total amount of charges, and another field displays the costing lot size that is used to amortize the amount.</span></span> <span data-ttu-id="f8b0b-108">Kulut näytetään erillisissä kentissä esimerkiksi Nimikkeen hinta -sivulla.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-108">The Item price page, for example, displays the charges as two separate fields.</span></span> <span data-ttu-id="f8b0b-109">Valmis-sivulla näytetään kuitenkin nimikkeen yksikkökohtainen kokonaiskustannus; kuoletetut kustannukset sisältyvät yksikkökustannuksiin.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-109">However, the Complete page displays the item's total cost per unit, and the amortized costs are included in the unit costs.</span></span>

<span data-ttu-id="f8b0b-110">Valmistetun nimikkeen kulut sisältyvät aina nimikkeen yksikkökustannukseen standardikustannustarkoituksia varten.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-110">The charges for a manufactured item are always included in the item's unit cost for standard cost purposes.</span></span> <span data-ttu-id="f8b0b-111">Ne voi vaihtoehtoisesti sisällyttää suunniteltuihin kustannustarkoituksiin.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-111">They can optionally be included for planned cost purposes.</span></span> <span data-ttu-id="f8b0b-112">Kustannuslaskentaversion käytännön perusteella muut kulut on sisällytettävä valmistetun nimikkeen kustannuksiin.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-112">A policy in the costing version enforces the inclusion of charges in the cost of a manufactured item.</span></span> <span data-ttu-id="f8b0b-113">Kun aktivoit nimikkeen kustannustietueen, se päivittää kulut nimikkeen peruskustannustietoihin, jotka näkyvät Nimikkeen hinta -sivulla.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-113">When you activate an item's cost record, you update the charges for the item's base cost information, which is displayed in the Item price page.</span></span> <span data-ttu-id="f8b0b-114">Kulut näytetään erillisissä kentissä, eikä niitä näytetä osana nimikkeen yksikkökustannusta.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-114">The charges are displayed as two separate fields, and they are not included in the item's unit cost.</span></span> <span data-ttu-id="f8b0b-115">Kukin aktivointi päivittää nimikkeen peruskustannustiedot, vaikka aktivointi koskisi eri toimipaikkoja.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-115">Each activation updates the item's base cost information, even if the activation reflects different sites.</span></span> <span data-ttu-id="f8b0b-116">Tämän vuoksi peruskustannustietoihin kannattaa suhtautua viitetietoina.</span><span class="sxs-lookup"><span data-stu-id="f8b0b-116">Therefore, you should view the base cost information as reference information.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]