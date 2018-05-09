---
title: Luo tuotantotilaus
description: "Tässä menettelyssä näytetään, miten tuotantotilaus luodaan."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d53b3f205a1564102b346b3673eca34b98df740a
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-production-order"></a><span data-ttu-id="05cc5-103">Luo tuotantotilaus</span><span class="sxs-lookup"><span data-stu-id="05cc5-103">Create a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="05cc5-104">Tässä menettelyssä näytetään, miten tuotantotilaus luodaan.</span><span class="sxs-lookup"><span data-stu-id="05cc5-104">This procedure shows how to create a production order.</span></span> <span data-ttu-id="05cc5-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="05cc5-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="05cc5-106">Tämä on ensimmäinen seitsemästä tuotantotilauksen elinkaaresta kertovasta menettelystä.</span><span class="sxs-lookup"><span data-stu-id="05cc5-106">This is the first procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="05cc5-107">Luo tuotantotilaus</span><span class="sxs-lookup"><span data-stu-id="05cc5-107">Create a production order</span></span>
1. <span data-ttu-id="05cc5-108">Siirry kohtaan Tuotannonhallinta > Tuotantotilaukset > Kaikki tuotantotilaukset.</span><span class="sxs-lookup"><span data-stu-id="05cc5-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="05cc5-109">Valitse Uusi tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="05cc5-109">Click New production order.</span></span>
3. <span data-ttu-id="05cc5-110">Kirjoita Nimiketunnus-kenttään D0001.</span><span class="sxs-lookup"><span data-stu-id="05cc5-110">In the Item number field, type 'D0001'.</span></span>
4. <span data-ttu-id="05cc5-111">Syötä päivämäärä Toimitus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="05cc5-111">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="05cc5-112">Toimituspäivämäärä osoittaa, milloin tuotantotilauksen tulee päättyä, jotta se voidaan toimittaa ajoissa.</span><span class="sxs-lookup"><span data-stu-id="05cc5-112">The delivery date indicates when the production order should end in order to deliver on time.</span></span> <span data-ttu-id="05cc5-113">Tätä päivämäärää käytetään ajoitusprosessissa.</span><span class="sxs-lookup"><span data-stu-id="05cc5-113">This date can be used in the scheduling process.</span></span> <span data-ttu-id="05cc5-114">Voit ajoittaa tilauksen esimerkiksi toimituspäivämäärästä taaksepäin.</span><span class="sxs-lookup"><span data-stu-id="05cc5-114">For example, you can schedule the order backward from the delivery date.</span></span>  
5. <span data-ttu-id="05cc5-115">Valitse määräksi 20.</span><span class="sxs-lookup"><span data-stu-id="05cc5-115">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="05cc5-116">Huomautus: Tuoterakenteen numero -kentässä näkyy automaattisesti nykyisen nimikkeen jonkin aktiivisen tuoterakenteen numero. Voit vaihtaa tuotantotilauksen tuoterakenteen valitsemalla aktiivisen tuoterakenteen hyväksyttyjen tuoterakenneversioiden luettelosta.</span><span class="sxs-lookup"><span data-stu-id="05cc5-116">Note: The BOM number field automatically displays the number of any active BOM for the current item, but you can change the BOM for the production order by selecting an active BOM from the list of approved BOM versions.</span></span>    <span data-ttu-id="05cc5-117">Reitin numero -kentässä näkyy automaattisesti nykyisen nimikkeen jonkin aktiivisen reitin numero. Voit vaihtaa tuotantotilauksen reitin valitsemalla aktiivisen reitin hyväksyttyjen reittiversioiden luettelosta.</span><span class="sxs-lookup"><span data-stu-id="05cc5-117">The Route number field automatically displays the number of any active Route for the current item, but you can change the Route for the production order by selecting an active Route from the list of approved Route versions.</span></span>  
6. <span data-ttu-id="05cc5-118">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="05cc5-118">Click Create.</span></span>

## <a name="validate-the-production-order"></a><span data-ttu-id="05cc5-119">Tuotantotilaus tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="05cc5-119">Validate the production order</span></span>
1. <span data-ttu-id="05cc5-120">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="05cc5-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="05cc5-121">Valitse juuri luomasi tuotantotilauksen numeron linkkiä.</span><span class="sxs-lookup"><span data-stu-id="05cc5-121">Click the link for the production order number that you have just created.</span></span> <span data-ttu-id="05cc5-122">Tilauksen tietojen sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="05cc5-122">This will open the details page for the order.</span></span>  
2. <span data-ttu-id="05cc5-123">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="05cc5-123">Click Edit.</span></span>
3. <span data-ttu-id="05cc5-124">Syötä päivämäärä Toimitus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="05cc5-124">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="05cc5-125">Voit muuttaa esimerkiksi tuotantotilauksen toimituspäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="05cc5-125">For example, you can change the delivery date for the production order.</span></span>  
4. <span data-ttu-id="05cc5-126">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="05cc5-126">Click Save.</span></span>
5. <span data-ttu-id="05cc5-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="05cc5-127">Close the page.</span></span>

## <a name="update-the-bom"></a><span data-ttu-id="05cc5-128">Tuoterakenteen päivittäminen</span><span class="sxs-lookup"><span data-stu-id="05cc5-128">Update the BOM</span></span>
1. <span data-ttu-id="05cc5-129">Valitse toimintoruudussa Tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="05cc5-129">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="05cc5-130">Valitse Tuoterakenne.</span><span class="sxs-lookup"><span data-stu-id="05cc5-130">Click BOM.</span></span>
    * <span data-ttu-id="05cc5-131">Avaa tuoterakenteen sivu, kun haluat tarkistaa oletustiedoista tuotantotilauksen luomisen yhteydessä kopioidut tuotantorakennetiedot.</span><span class="sxs-lookup"><span data-stu-id="05cc5-131">Open the BOM page to validate the BOM data that was copied from the default data when the production order was created.</span></span> <span data-ttu-id="05cc5-132">Tässä menettelyssä tuoterakenteen määrä on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="05cc5-132">In this procedure, you need to update the quantity for a BOM.</span></span>  
3. <span data-ttu-id="05cc5-133">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="05cc5-133">Click Edit.</span></span>
4. <span data-ttu-id="05cc5-134">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="05cc5-134">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="05cc5-135">Tuoterakennerivin määrän muuttaminen vaikuttaa tuotantotilauksen materiaalikulutuksen kustannusarvioon.</span><span class="sxs-lookup"><span data-stu-id="05cc5-135">Changing the quantity on the BOM line affects the cost estimate of material consumption for the production order.</span></span>  
5. <span data-ttu-id="05cc5-136">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="05cc5-136">Click Save.</span></span>
6. <span data-ttu-id="05cc5-137">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="05cc5-137">Close the page.</span></span>

## <a name="update-the-production-route"></a><span data-ttu-id="05cc5-138">Tuotantoreitin päivittäminen</span><span class="sxs-lookup"><span data-stu-id="05cc5-138">Update the production route</span></span>
1. <span data-ttu-id="05cc5-139">Valitse toimintoruudussa Tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="05cc5-139">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="05cc5-140">Valitse Reitti.</span><span class="sxs-lookup"><span data-stu-id="05cc5-140">Click Route.</span></span>
    * <span data-ttu-id="05cc5-141">Avaa reitin sivu, kun haluat tarkistaa oletustiedoista tilauksen luomisen yhteydessä kopioidut tuotantoreitin tiedot.</span><span class="sxs-lookup"><span data-stu-id="05cc5-141">Open the Route page to validate the data of the production route that was copied from the default data when the order was created.</span></span> <span data-ttu-id="05cc5-142">Tässä menettelyssä päivitetään yhden tuotantoreitin työvaiheen määrä.</span><span class="sxs-lookup"><span data-stu-id="05cc5-142">In this procedure, you need to update the quantity for one of the operations in the production route.</span></span>  
3. <span data-ttu-id="05cc5-143">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="05cc5-143">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="05cc5-144">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="05cc5-144">Click Edit.</span></span>
5. <span data-ttu-id="05cc5-145">Syötä Prosessimäärä-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="05cc5-145">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="05cc5-146">Prosessin muuttaminen vaikuttaa reitin arvioituun kulutukseen ja tuotantotilauksen kustannuksiin.</span><span class="sxs-lookup"><span data-stu-id="05cc5-146">Changing the process time affects the estimated route consumption and the cost of the production order.</span></span>  
6. <span data-ttu-id="05cc5-147">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="05cc5-147">Click Save.</span></span>
7. <span data-ttu-id="05cc5-148">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="05cc5-148">Close the page.</span></span>

