---
title: Valmistetun nimikkeen vakiokustannusten kuolettaminen
description: "Valmistetun nimikkeen vakiokustannukset kuvastavat toimintojen asetusaikoja sekä komponentteja, joilla on vakiomäärä tai hävikin vakiomäärä."
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: AndersGirke
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 75c0f5bcff0aae63aa8c7dae9b0767f8c7e6a81c
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="amortize-constant-costs-for-a-manufactured-item"></a><span data-ttu-id="cc988-103">Valmistetun nimikkeen vakiokustannusten kuolettaminen</span><span class="sxs-lookup"><span data-stu-id="cc988-103">Amortize constant costs for a manufactured item</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="cc988-104">Valmistetun nimikkeen vakiokustannukset kuvastavat toimintojen asetusaikoja sekä komponentteja, joilla on vakiomäärä tai hävikin vakiomäärä.</span><span class="sxs-lookup"><span data-stu-id="cc988-104">A manufactured item’s constant costs reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span> 

<span data-ttu-id="cc988-105">Kustannuslaskelman eräkoon käsitettä käytetään kuoletettaessa näitä valmistetun nimikkeen laskettujen kustannusten vakiokustannuksia.</span><span class="sxs-lookup"><span data-stu-id="cc988-105">The concept of a costing lot size is used to amortize these constant costs in the calculated cost of a manufactured item.</span></span> <span data-ttu-id="cc988-106">Tällä käsitteellä on useita synonyymeja, kuten kirjanpidon eräkoko.</span><span class="sxs-lookup"><span data-stu-id="cc988-106">This concept has several synonyms, one of which is accounting lot size.</span></span> <span data-ttu-id="cc988-107">Myös vakiokustannusten kuoletuksen käsitteellä on useita synonyymeja, kuten suhteelliset vakiokustannukset.</span><span class="sxs-lookup"><span data-stu-id="cc988-107">The concept of amortizing constant costs also has several synonyms, one of which is proportional constant costs.</span></span>

<span data-ttu-id="cc988-108">Valmistetun nimikkeen kustannuslaskelman eräkokoa käytetään tuoterakennelaskelmassa.</span><span class="sxs-lookup"><span data-stu-id="cc988-108">The quantity of a costing lot size for a manufactured item is used in a bill of material (BOM) calculation.</span></span> <span data-ttu-id="cc988-109">Alla oleva kuva osoittaa, miten tuoterakennelaskelman käynnistys- ja suoritustapa vaikuttavat määrään:</span><span class="sxs-lookup"><span data-stu-id="cc988-109">The quantity depends on how you initiate and perform the BOM calculation, as illustrated by the following:</span></span>

-   <span data-ttu-id="cc988-110">Nimikkeen tuoterakennelaskelman laskelman oletusmäärä: Nimikkeen varaston vakiotilausmäärä toimii nimikkeen kustannuslaskelman eräkoon oletusmääränä, mutta oletusmäärä voi olla suurempi, jolloin se kuvastaa nimikkeen tilausmäärän kerrannaisia</span><span class="sxs-lookup"><span data-stu-id="cc988-110">Default calculation quantity in an item’s BOM calculation − The item’s standard order quantity for inventory acts as the costing lot size, but the default value might be a greater quantity to reflect the item’s order quantity multiple.</span></span> <span data-ttu-id="cc988-111">Nimikkeen vakiotilausmäärä ja kerrannaiset voidaan määrittää nimikkeen oletustilausasetuksissa tai toimipaikkakohtaisissa tilausasetuksissa.</span><span class="sxs-lookup"><span data-stu-id="cc988-111">The item’s standard order quantity and multiple can be defined within its default order settings or site-specific order settings.</span></span>
-   <span data-ttu-id="cc988-112">Nimikkeen tuoterakennelaskelman määritetty laskelman määrä: Määritetty laskelman määrä toimii nimikkeen kustannuslaskelman eräkokona.</span><span class="sxs-lookup"><span data-stu-id="cc988-112">Specified calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item.</span></span> <span data-ttu-id="cc988-113">Laskelman oletusmääränä käytetään alun perin nimikkeen vakiotilausmäärää, mutta se voidaan ohittaa manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="cc988-113">The calculation quantity initially uses the item’s standard order quantity, but the default value can be manually overridden.</span></span> <span data-ttu-id="cc988-114">Määritetty laskelman määrä edustaa määritetyn nimikkeen kustannuslaskelman eräkokoa. Se edustaa myös tuotannon tuoterakennerivityypin valmistettujen komponenttien kustannuslaskelman eräkokoa.</span><span class="sxs-lookup"><span data-stu-id="cc988-114">The specified calculation quantity represents the costing lot size for the specified item, and for manufactured components that have a BOM line type of production.</span></span> <span data-ttu-id="cc988-115">Tämä johtuu siitä, että oletettavasti komponentteja valmistetaan täsmälleen sama määrä.</span><span class="sxs-lookup"><span data-stu-id="cc988-115">This is because it is assumed that the component will be produced to the exact quantity.</span></span> <span data-ttu-id="cc988-116">Muiden valmistettujen komponenttien (joiden tuoterakennerivityyppi on nimike) kustannuslaskelman eräkoko vastaa kyseisten komponenttien oletustilausmäärää.</span><span class="sxs-lookup"><span data-stu-id="cc988-116">The costing lot size for other manufactured components that have a BOM line type of item will reflect their standard order quantity.</span></span>
-   <span data-ttu-id="cc988-117">Nimikkeen tuoterakennelaskelman määritetty valmistus myyntitilaukselle -määrä: Määritetty laskelman määrä toimii nimikkeen ja sen valmistettujen komponenttien kustannuslaskelman eräkokona, kun tuoterakennelaskelmat käyttävät valmistus myyntitilaukselle -hajotustilaa.</span><span class="sxs-lookup"><span data-stu-id="cc988-117">Specified make-to-order calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item and its manufactured components when BOM calculations use a make-to-order explosion mode.</span></span> <span data-ttu-id="cc988-118">Järjestelmä olettaa, että valmistettavia komponentteja tuotetaan täsmälleen sama määrä, aivan kuten valmistettavia komponentteja, joiden tuoterakennerivin tyyppi on tuotanto.</span><span class="sxs-lookup"><span data-stu-id="cc988-118">It is assumed that the manufactured components will be produced to the exact quantity, just like a manufactured component that has a BOM line type of production.</span></span>
-   <span data-ttu-id="cc988-119">Tilauskohtaisen tuoterakennelaskelman määritetty laskelman määrä: Tilauskohtainen tuoterakennelaskelma voidaan suorittaa myyntitilauksen, myyntitarjouksen tai huoltotilauksen rivinimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="cc988-119">Specified calculation quantity in an order-specific BOM calculation − An order-specific BOM calculation can be performed for a line item on a sales order, sales quotation, or service order.</span></span> <span data-ttu-id="cc988-120">Määritetyn laskelman määrän oletusmääränä käytetään alkuperäisen rivinimikkeen määrää, mutta se voidaan ohittaa manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="cc988-120">The specified calculation quantity uses the quantity on the originating line item, but the default quantity can be overridden.</span></span> <span data-ttu-id="cc988-121">Voit valita, käyttääkö tilauskohtainen tuoterakennelaskelma valmistus myyntitilaukselle -hajotustilaa vai monirivistä hajotustilaa.</span><span class="sxs-lookup"><span data-stu-id="cc988-121">You can select whether the order-specific BOM calculation uses a make-to-order or multilevel explosion mode.</span></span>

<span data-ttu-id="cc988-122">Valmistetun nimikkeen kuoletettujen vakiokustannusten laskettu summa sisältyy kuluihin.</span><span class="sxs-lookup"><span data-stu-id="cc988-122">The calculated amount of a manufactured item’s amortized constant costs is termed charges.</span></span>






