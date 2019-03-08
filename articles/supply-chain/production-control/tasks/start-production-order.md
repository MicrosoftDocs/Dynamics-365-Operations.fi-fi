---
title: Käynnistä tuotantotilaus
description: Tässä menettelyssä selvitetään, miten tuotantotilaus aloitetaan työnohjauksessa.
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f83091a9f3e96a9176860bd16fa5969507488a25
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "346223"
---
# <a name="start-a-production-order"></a><span data-ttu-id="1f19a-103">Käynnistä tuotantotilaus</span><span class="sxs-lookup"><span data-stu-id="1f19a-103">Start a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1f19a-104">Tässä menettelyssä selvitetään, miten tuotantotilaus aloitetaan työnohjauksessa.</span><span class="sxs-lookup"><span data-stu-id="1f19a-104">This procedure shows how to start a production order on the shop floor.</span></span> <span data-ttu-id="1f19a-105">Tämän prosessin ajan ja materiaalin kulutus raportoidaan.</span><span class="sxs-lookup"><span data-stu-id="1f19a-105">Time and material consumption are reported in this process.</span></span> <span data-ttu-id="1f19a-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="1f19a-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="1f19a-107">Tämä on viides seitsemästä tuotantotilauksen elinkaaresta kertovasta menettelystä.</span><span class="sxs-lookup"><span data-stu-id="1f19a-107">This is the fifth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="start-a-production-order"></a><span data-ttu-id="1f19a-108">Käynnistä tuotantotilaus</span><span class="sxs-lookup"><span data-stu-id="1f19a-108">Start a production order</span></span>
1. <span data-ttu-id="1f19a-109">Siirry kohtaan Tuotannonhallinta > Tuotantotilaukset > Kaikki tuotantotilaukset.</span><span class="sxs-lookup"><span data-stu-id="1f19a-109">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="1f19a-110">Valitse tuotantotilaus, jonka tila on Vapautettu.</span><span class="sxs-lookup"><span data-stu-id="1f19a-110">Select a production order that has the Released status.</span></span>  
2. <span data-ttu-id="1f19a-111">Valitse toimintoruudussa Tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="1f19a-111">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="1f19a-112">Valitse Käynnistys.</span><span class="sxs-lookup"><span data-stu-id="1f19a-112">Click Start.</span></span>
    * <span data-ttu-id="1f19a-113">Voit vahvistaa tällä sivulla tuotantotilauksen alkamisen.</span><span class="sxs-lookup"><span data-stu-id="1f19a-113">On this page, you can confirm the start of the production order.</span></span>  
4. <span data-ttu-id="1f19a-114">Valitse Yleiset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="1f19a-114">Click the General tab.</span></span>
5. <span data-ttu-id="1f19a-115">Lisää Työvaiheen</span><span class="sxs-lookup"><span data-stu-id="1f19a-115">In the From Oper.</span></span> <span data-ttu-id="1f19a-116">Nro</span><span class="sxs-lookup"><span data-stu-id="1f19a-116">No.</span></span> <span data-ttu-id="1f19a-117">-kenttään 10.</span><span class="sxs-lookup"><span data-stu-id="1f19a-117">field, enter '10'.</span></span>
6. <span data-ttu-id="1f19a-118">Valitse Automaattinen reitityksen kulutus -kentässä Aina.</span><span class="sxs-lookup"><span data-stu-id="1f19a-118">In the Automatic route consumption field, select 'Always'.</span></span>
7. <span data-ttu-id="1f19a-119">Valitse Kirjaa reitityskortti nyt -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="1f19a-119">Click the Post route card now checkbox.</span></span>
8. <span data-ttu-id="1f19a-120">Valitse Automaattinen tuoterakennekulutus -kentässä Aina.</span><span class="sxs-lookup"><span data-stu-id="1f19a-120">In the Automatic BOM consumption field, select 'Always'.</span></span>
9. <span data-ttu-id="1f19a-121">Valitse Kirjaa keräysluettelo nyt -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="1f19a-121">Click the Post picking list now checkbox.</span></span>
10. <span data-ttu-id="1f19a-122">Valitse Tulosta keräysluettelo -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="1f19a-122">Click the Print picking list checkbox.</span></span>
11. <span data-ttu-id="1f19a-123">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1f19a-123">Click OK.</span></span>
    * <span data-ttu-id="1f19a-124">Tämä tulostettu keräysluettelo sisältää tuotantotilauksessa käytetyt materiaalit.</span><span class="sxs-lookup"><span data-stu-id="1f19a-124">This is the printed picking list that shows the materials used for the production order.</span></span>  
12. <span data-ttu-id="1f19a-125">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1f19a-125">Close the page.</span></span>

## <a name="validate-the-picking-list"></a><span data-ttu-id="1f19a-126">Vahvista keräysluettelo.</span><span class="sxs-lookup"><span data-stu-id="1f19a-126">Validate the picking list</span></span>
1. <span data-ttu-id="1f19a-127">Valitse toimintoruudussa Näytä.</span><span class="sxs-lookup"><span data-stu-id="1f19a-127">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="1f19a-128">Valitse Keräysluettelo.</span><span class="sxs-lookup"><span data-stu-id="1f19a-128">Click Picking list.</span></span>
3. <span data-ttu-id="1f19a-129">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="1f19a-129">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="1f19a-130">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="1f19a-130">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="1f19a-131">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="1f19a-131">Click Edit.</span></span>
6. <span data-ttu-id="1f19a-132">Lisää Kulutus-kenttään luku.</span><span class="sxs-lookup"><span data-stu-id="1f19a-132">In the Consumption field, enter a number.</span></span>
7. <span data-ttu-id="1f19a-133">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="1f19a-133">Click Post.</span></span>
8. <span data-ttu-id="1f19a-134">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1f19a-134">Click OK.</span></span>
    * <span data-ttu-id="1f19a-135">Tuotantotilauksen kuluttamat materiaalit kirjataan keräysluettelon kirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="1f19a-135">In the picking list journal, the materials consumed by the production order are posted.</span></span> <span data-ttu-id="1f19a-136">Voit tehdä ennen kirjauskansioon kirjausta oikaisuja, jos arvioidun määrän ja todellisen kulutetun määrän välillä on ero.</span><span class="sxs-lookup"><span data-stu-id="1f19a-136">Before posting the journal, you can make adjustments if there is a difference between the estimated quantity and the actual consumed quantity.</span></span>  
9. <span data-ttu-id="1f19a-137">Valitse Ruudukkoruutu-välilehti.</span><span class="sxs-lookup"><span data-stu-id="1f19a-137">Click the GridPanel tab.</span></span>
10. <span data-ttu-id="1f19a-138">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1f19a-138">Close the page.</span></span>

## <a name="verify-the-route-card-journal"></a><span data-ttu-id="1f19a-139">Tarkista reitityskorttikirjauskansio</span><span class="sxs-lookup"><span data-stu-id="1f19a-139">Verify the route card journal</span></span>
1. <span data-ttu-id="1f19a-140">Valitse toimintoruudussa Näytä.</span><span class="sxs-lookup"><span data-stu-id="1f19a-140">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="1f19a-141">Valitse Reitityskortti.</span><span class="sxs-lookup"><span data-stu-id="1f19a-141">Click Route card.</span></span>
3. <span data-ttu-id="1f19a-142">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="1f19a-142">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="1f19a-143">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="1f19a-143">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="1f19a-144">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="1f19a-144">Click Edit.</span></span>
6. <span data-ttu-id="1f19a-145">Lisää Tunnit-kenttään luku.</span><span class="sxs-lookup"><span data-stu-id="1f19a-145">In the Hours field, enter a number.</span></span>
7. <span data-ttu-id="1f19a-146">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="1f19a-146">Click Post.</span></span>
8. <span data-ttu-id="1f19a-147">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1f19a-147">Click OK.</span></span>
    * <span data-ttu-id="1f19a-148">Yksittäisiin toimintoihin käytetty aika kirjataan reitityskorttikirjauskansioon</span><span class="sxs-lookup"><span data-stu-id="1f19a-148">In the Route card journal, the time spent on the individual operations is recorded.</span></span> <span data-ttu-id="1f19a-149">Myös hyväksyttyjen ja virheellisten määrä voidaan raportoida.</span><span class="sxs-lookup"><span data-stu-id="1f19a-149">Good and error quantity can also be reported.</span></span>  
