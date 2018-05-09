---
title: "Välitön täydennys"
description: "Tässä ohjeaiheessa käsitellään varaston täydennystä välittömällä täydennyksellä, kun sijaintidirektiivi ei osoita varastoa."
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLocDirTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1f24ffbba0c28b241de66f484546844bc72b90c9
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="immediate-replenishment"></a><span data-ttu-id="9688c-103">Välitön täydennys</span><span class="sxs-lookup"><span data-stu-id="9688c-103">Immediate replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9688c-104">Välittömällä täydennyksellä voit täydentää varaston välittömästi sen jälkeen, kun suuntadirektiivirivi ei osoita varastoa.</span><span class="sxs-lookup"><span data-stu-id="9688c-104">Immediate replenishment lets you replenish inventory immediately after a location directive line fails to allocate inventory.</span></span> <span data-ttu-id="9688c-105">Täydennys perustuu yhteen riviin sijaintidirektiivin asetuksissa.</span><span class="sxs-lookup"><span data-stu-id="9688c-105">The replenishment is based on a single line in the setup of the location directive.</span></span> <span data-ttu-id="9688c-106">Jos varastoa ei ole käytettävissä siinä kyseisen rivin määrittämässä yksikössä, kyseisen mittayksikön täydennys tapahtuu heti.</span><span class="sxs-lookup"><span data-stu-id="9688c-106">If inventory isn't on hand in the unit of measure that is specified by that line, replenishment of that unit of measure occurs immediately.</span></span>

<span data-ttu-id="9688c-107">Välitön täydennys on vaihtoehtoinen menetelmä, jossa varaston kohdistus perustuu useisiin suuntadirektiivin riveihin ja jossa kysyntä summataan kohdistuksen lopussa ja täydennetään sijaintidirektiivin viimeisellä rivillä määritetyssä mittayksikössä.</span><span class="sxs-lookup"><span data-stu-id="9688c-107">Immediate replenishment provides an alternative to the method where the allocation of inventory is based on more lines in the location directive, and where the demand is summed at the end of the allocation and replenished in the unit of measure that is specified by the last line in the location directive.</span></span>

<span data-ttu-id="9688c-108">Välittömän täydennyksen etuna on, että täydennystä voidaan rajoittaa tiettyihin yksiköihin ja että määrä voidaan ohjata tiettyihin sijainteihin.</span><span class="sxs-lookup"><span data-stu-id="9688c-108">The benefits of using immediate replenishment are that replenishment can be limited by specific units and the quantity can be directed to specific locations.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="9688c-109">Liiketoimintaskenaario</span><span class="sxs-lookup"><span data-stu-id="9688c-109">Business scenario</span></span>

<span data-ttu-id="9688c-110">Varastossa voi esimerkiksi olla erilliset keräilyalueet mittayksiköille laatikko ja kappale.</span><span class="sxs-lookup"><span data-stu-id="9688c-110">For example, you have a warehouse that has separate picking areas for the "box" and "each" units of measure.</span></span> <span data-ttu-id="9688c-111">Haluat optimoida keräilyprosessin keräämällä ensin mahdollisimman monta laatikkoa ja sitten jäljellä olevan laatikkoa pienemmän määrän Kappale-alueelta.</span><span class="sxs-lookup"><span data-stu-id="9688c-111">You want to optimize the picking process by picking as many boxes as possible and then picking any remaining quantity that is less than a box from the "each" area.</span></span>

<span data-ttu-id="9688c-112">Voit käyttää tässä tapauksessa välitöntä täydennystä.</span><span class="sxs-lookup"><span data-stu-id="9688c-112">In this case, you can use immediate replenishment.</span></span> <span data-ttu-id="9688c-113">Voit määrittää suuntadirektiivissä välittömän täydennyksen laatikoille, jotta kysynnän täydennystä käytetään heti, kun kysynnän määrään varten kerättäviä laatikoita ei ole tarpeeksi.</span><span class="sxs-lookup"><span data-stu-id="9688c-113">In the location directive, you can set up immediate replenishment for boxes so that demand replenishment is used as soon as there is a shortage of boxes that can be picked for the demand quantity.</span></span> <span data-ttu-id="9688c-114">Voit optimoida tällä tavoin keräilyprosessin siten, että keräily sisältää mahdollisimman monta laatikkoa.</span><span class="sxs-lookup"><span data-stu-id="9688c-114">In this way, you optimize the picking process so that picking includes as many boxes as possible.</span></span> <span data-ttu-id="9688c-115">Välitön täydennys luo laatikoiden täydennyksen eikä kysyntää siirretä, joten määrät kerätään Kappale-mittayksikössä.</span><span class="sxs-lookup"><span data-stu-id="9688c-115">Immediate replenishment will generate replenishment of the boxes, and the demand won't be passed on so that the quantities are picked in the "each" unit of measure.</span></span> <span data-ttu-id="9688c-116">Toisin sanoen vain ne määrät, jotka on tarkoitus kerätä Kappale-mittayksikössä (eli laatikkoa pienemmät määrät) kerätään Kappale-alueelta.</span><span class="sxs-lookup"><span data-stu-id="9688c-116">In other words, only the quantities that are supposed to be picked in the "each" unit of measure (that is, quantities that are less than a box) will be picked from the "each" area.</span></span> <span data-ttu-id="9688c-117">Jos puute ilmenee Laatikko-alueella, voit kerätä kokonaiskysynnän mukaan mahdollisimman monta laatikkoa.</span><span class="sxs-lookup"><span data-stu-id="9688c-117">If a shortage occurs in the "box" area, you can pick as many boxes as possible out of the total demand.</span></span> <span data-ttu-id="9688c-118">Jäljellä olevat määrät kerätään Kappale-alueelta.</span><span class="sxs-lookup"><span data-stu-id="9688c-118">The remaining quantities will then be picked from the "each" area.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="9688c-119">Käyttö</span><span class="sxs-lookup"><span data-stu-id="9688c-119">Where it applies</span></span>

<span data-ttu-id="9688c-120">Välitöntä täydennystä käytetään aallon suorituksen aikana, jos kohdistus epäonnistuu sijaintidirektiivin riville, jolle on täydennysmalli on määritetty.</span><span class="sxs-lookup"><span data-stu-id="9688c-120">Immediate replenishment is used during wave execution if allocation fails for a location directive line that a replenishment template is set for.</span></span>

## <a name="set-up-immediate-replenishment"></a><span data-ttu-id="9688c-121">Välittömän täydennyksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="9688c-121">Set up immediate replenishment</span></span>

- <span data-ttu-id="9688c-122">Valitse ensin **Varastonhallinta** \> **Asetukset** \> **Sijaintidirektiivit** ja sitten **Rivit**-välilehden **Välittömän täydennyksen malli** -luettelossa aaltokysynnän täydennysmalli.</span><span class="sxs-lookup"><span data-stu-id="9688c-122">Go to **Warehouse management** \> **Setup** \> **Location directives**, and then, on the **Lines** tab, in the **Immediate replenishment template** list, select a replenishment template for wave demand.</span></span>

<span data-ttu-id="9688c-123">Täydennysmallia käytetään, jos sijaintidirektiivin rivi ei käytä kohdistettua mittayksikköä.</span><span class="sxs-lookup"><span data-stu-id="9688c-123">The replenishment template is applied if the location directive line fails to allocate a dedicated unit of measure.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="9688c-124">Vianmääritys</span><span class="sxs-lookup"><span data-stu-id="9688c-124">Troubleshooting</span></span>

<span data-ttu-id="9688c-125">Jos sijaintidirektiiviriville valitaan välitön kohdistus mutta mitään täydennystyötä ei luoda, kun käytät kyseisen sijaintidirektiivirivin kysynnän täydennyksen malleja, syy on todennäköisesti jompikumpi seuraavista:</span><span class="sxs-lookup"><span data-stu-id="9688c-125">If immediate replenishment is selected for a location directive line, but no replenishment work is generated when you use demand replenishment templates for that location directive line, two main causes must be investigated:</span></span>

- <span data-ttu-id="9688c-126">Varmista, että käytetty kysynnän täydennyksen malli on määritetty käyttämään oikeita **Täydennys**-tyypin sijainti- ja työmalleja.</span><span class="sxs-lookup"><span data-stu-id="9688c-126">Make sure that the demand replenishment template that is applied is set up to use the correct location templates and work templates of the **Replenishment** type.</span></span>
- <span data-ttu-id="9688c-127">Varmista, käytettävissä olevaa varastoa on riittävästi niissä sijainneissa, joissa kysynnän täydennyksen malli hakee käytettävissä olevaa varastoa täydennystä varten.</span><span class="sxs-lookup"><span data-stu-id="9688c-127">Make sure that there is enough on-hand inventory at the locations where the demand replenishment template searches for on-hand inventory for replenishment.</span></span>

