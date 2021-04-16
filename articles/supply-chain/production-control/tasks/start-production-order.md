---
title: Käynnistä tuotantotilaus
description: Tässä menettelyssä selvitetään, miten tuotantotilaus aloitetaan työnohjauksessa.
author: johanhoffmann
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: JmgRegistrationStartJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be1c389bc4193ef080dbeb1639b69acf466ef0de
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831863"
---
# <a name="start-a-production-order"></a><span data-ttu-id="3761e-103">Käynnistä tuotantotilaus</span><span class="sxs-lookup"><span data-stu-id="3761e-103">Start a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3761e-104">Tässä menettelyssä selvitetään, miten tuotantotilaus aloitetaan työnohjauksessa.</span><span class="sxs-lookup"><span data-stu-id="3761e-104">This procedure shows how to start a production order on the shop floor.</span></span> <span data-ttu-id="3761e-105">Tämän prosessin ajan ja materiaalin kulutus raportoidaan.</span><span class="sxs-lookup"><span data-stu-id="3761e-105">Time and material consumption are reported in this process.</span></span> <span data-ttu-id="3761e-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="3761e-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3761e-107">Tämä on viides seitsemästä tuotantotilauksen elinkaaresta kertovasta menettelystä.</span><span class="sxs-lookup"><span data-stu-id="3761e-107">This is the fifth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="start-a-production-order"></a><span data-ttu-id="3761e-108">Käynnistä tuotantotilaus</span><span class="sxs-lookup"><span data-stu-id="3761e-108">Start a production order</span></span>
1. <span data-ttu-id="3761e-109">Siirry kohtaan Tuotannonhallinta > Tuotantotilaukset > Kaikki tuotantotilaukset.</span><span class="sxs-lookup"><span data-stu-id="3761e-109">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="3761e-110">Valitse tuotantotilaus, jonka tila on Vapautettu.</span><span class="sxs-lookup"><span data-stu-id="3761e-110">Select a production order that has the Released status.</span></span>  
2. <span data-ttu-id="3761e-111">Valitse toimintoruudussa Tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="3761e-111">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="3761e-112">Valitse Käynnistys.</span><span class="sxs-lookup"><span data-stu-id="3761e-112">Click Start.</span></span>
    * <span data-ttu-id="3761e-113">Voit vahvistaa tällä sivulla tuotantotilauksen alkamisen.</span><span class="sxs-lookup"><span data-stu-id="3761e-113">On this page, you can confirm the start of the production order.</span></span>  
4. <span data-ttu-id="3761e-114">Valitse Yleiset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="3761e-114">Click the General tab.</span></span>
5. <span data-ttu-id="3761e-115">Lisää Työvaiheen</span><span class="sxs-lookup"><span data-stu-id="3761e-115">In the From Oper.</span></span> <span data-ttu-id="3761e-116">Nro</span><span class="sxs-lookup"><span data-stu-id="3761e-116">No.</span></span> <span data-ttu-id="3761e-117">-kenttään 10.</span><span class="sxs-lookup"><span data-stu-id="3761e-117">field, enter '10'.</span></span>
6. <span data-ttu-id="3761e-118">Valitse Automaattinen reitityksen kulutus -kentässä Aina.</span><span class="sxs-lookup"><span data-stu-id="3761e-118">In the Automatic route consumption field, select 'Always'.</span></span>
7. <span data-ttu-id="3761e-119">Valitse Kirjaa reitityskortti nyt -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="3761e-119">Click the Post route card now checkbox.</span></span>
8. <span data-ttu-id="3761e-120">Valitse Automaattinen tuoterakennekulutus -kentässä Aina.</span><span class="sxs-lookup"><span data-stu-id="3761e-120">In the Automatic BOM consumption field, select 'Always'.</span></span>
9. <span data-ttu-id="3761e-121">Valitse Kirjaa keräysluettelo nyt -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="3761e-121">Click the Post picking list now checkbox.</span></span>
10. <span data-ttu-id="3761e-122">Valitse Tulosta keräysluettelo -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="3761e-122">Click the Print picking list checkbox.</span></span>
11. <span data-ttu-id="3761e-123">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="3761e-123">Click OK.</span></span>
    * <span data-ttu-id="3761e-124">Tämä tulostettu keräysluettelo sisältää tuotantotilauksessa käytetyt materiaalit.</span><span class="sxs-lookup"><span data-stu-id="3761e-124">This is the printed picking list that shows the materials used for the production order.</span></span>  
12. <span data-ttu-id="3761e-125">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3761e-125">Close the page.</span></span>

## <a name="validate-the-picking-list"></a><span data-ttu-id="3761e-126">Vahvista keräysluettelo.</span><span class="sxs-lookup"><span data-stu-id="3761e-126">Validate the picking list</span></span>
1. <span data-ttu-id="3761e-127">Valitse toimintoruudussa Näytä.</span><span class="sxs-lookup"><span data-stu-id="3761e-127">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="3761e-128">Valitse Keräysluettelo.</span><span class="sxs-lookup"><span data-stu-id="3761e-128">Click Picking list.</span></span>
3. <span data-ttu-id="3761e-129">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="3761e-129">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="3761e-130">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="3761e-130">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="3761e-131">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="3761e-131">Click Edit.</span></span>
6. <span data-ttu-id="3761e-132">Lisää Kulutus-kenttään luku.</span><span class="sxs-lookup"><span data-stu-id="3761e-132">In the Consumption field, enter a number.</span></span>
7. <span data-ttu-id="3761e-133">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="3761e-133">Click Post.</span></span>
8. <span data-ttu-id="3761e-134">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="3761e-134">Click OK.</span></span>
    * <span data-ttu-id="3761e-135">Tuotantotilauksen kuluttamat materiaalit kirjataan keräysluettelon kirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="3761e-135">In the picking list journal, the materials consumed by the production order are posted.</span></span> <span data-ttu-id="3761e-136">Voit tehdä ennen kirjauskansioon kirjausta oikaisuja, jos arvioidun määrän ja todellisen kulutetun määrän välillä on ero.</span><span class="sxs-lookup"><span data-stu-id="3761e-136">Before posting the journal, you can make adjustments if there is a difference between the estimated quantity and the actual consumed quantity.</span></span>  
9. <span data-ttu-id="3761e-137">Valitse Ruudukkoruutu-välilehti.</span><span class="sxs-lookup"><span data-stu-id="3761e-137">Click the GridPanel tab.</span></span>
10. <span data-ttu-id="3761e-138">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3761e-138">Close the page.</span></span>

## <a name="verify-the-route-card-journal"></a><span data-ttu-id="3761e-139">Tarkista reitityskorttikirjauskansio</span><span class="sxs-lookup"><span data-stu-id="3761e-139">Verify the route card journal</span></span>
1. <span data-ttu-id="3761e-140">Valitse toimintoruudussa Näytä.</span><span class="sxs-lookup"><span data-stu-id="3761e-140">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="3761e-141">Valitse Reitityskortti.</span><span class="sxs-lookup"><span data-stu-id="3761e-141">Click Route card.</span></span>
3. <span data-ttu-id="3761e-142">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="3761e-142">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="3761e-143">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="3761e-143">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="3761e-144">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="3761e-144">Click Edit.</span></span>
6. <span data-ttu-id="3761e-145">Lisää Tunnit-kenttään luku.</span><span class="sxs-lookup"><span data-stu-id="3761e-145">In the Hours field, enter a number.</span></span>
7. <span data-ttu-id="3761e-146">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="3761e-146">Click Post.</span></span>
8. <span data-ttu-id="3761e-147">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="3761e-147">Click OK.</span></span>
    * <span data-ttu-id="3761e-148">Yksittäisiin toimintoihin käytetty aika kirjataan reitityskorttikirjauskansioon</span><span class="sxs-lookup"><span data-stu-id="3761e-148">In the Route card journal, the time spent on the individual operations is recorded.</span></span> <span data-ttu-id="3761e-149">Myös hyväksyttyjen ja virheellisten määrä voidaan raportoida.</span><span class="sxs-lookup"><span data-stu-id="3761e-149">Good and error quantity can also be reported.</span></span>  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]