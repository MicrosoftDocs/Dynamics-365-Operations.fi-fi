---
title: Huoltovälit
description: Huoltoväli ilmaisee tiheyden, jolla huoltosopimusriveille luodaan huoltotilausrivejä, kun huoltotilaukset luodaan.
author: ShylaThompson
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d8a186a4ac58115f3ff855e0a16429dc0778a18c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816385"
---
# <a name="service-intervals"></a><span data-ttu-id="5becb-103">Huoltovälit</span><span class="sxs-lookup"><span data-stu-id="5becb-103">Service intervals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5becb-104">Huoltosopimusväli ilmaisee tiheyden, jolla huoltosopimusriveille luodaan huoltotilausrivejä, kun huoltotilaukset luodaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="5becb-104">The service agreement interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders automatically.</span></span>

<span data-ttu-id="5becb-105">Kun luot huoltotilauksia automaattisesti, huoltotilausrivit luodaan huoltosopimusriville määrittämäsi aikavälin mukaisesti sopimusrivin aloituspäivämäärästä lähtien.</span><span class="sxs-lookup"><span data-stu-id="5becb-105">When you create service orders automatically, service order lines are created according to the interval that you have specified for the service agreement line from the start date of the agreement line.</span></span>

<span data-ttu-id="5becb-106">Jos **Huoltosopimus**-sivun **Väli**-kenttä on tyhjä, rivi on vain kerran tapahtuva tapahtuma eikä sitä käytetä toistuvien huoltotilausten luomiseen.</span><span class="sxs-lookup"><span data-stu-id="5becb-106">If the **Interval** field of a service agreement line in the **Service agreements** page is blank, the line is a one-time event, and it is not used to create service orders repeatedly.</span></span>

## <a name="example"></a><span data-ttu-id="5becb-107">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="5becb-107">Example</span></span>

<span data-ttu-id="5becb-108">Tämä esimerkki osoittaa, miten huoltoväli vaikuttaa huoltotilauksen huoltosopimuksen riveihin ja huoltotilauksen riveihin.</span><span class="sxs-lookup"><span data-stu-id="5becb-108">This example illustrates how a service interval will affect service agreement lines and service order lines on a service order.</span></span>

### <a name="create-a-service-agreement"></a><span data-ttu-id="5becb-109">Huoltosopimuksen luominen</span><span class="sxs-lookup"><span data-stu-id="5becb-109">Create a service agreement</span></span>

<span data-ttu-id="5becb-110">Luo ensiksi huoltosopimus ja valitse **Yhdistä huoltotilaukset** -asetukseksi **Huoltosopimuksen mukaan**.</span><span class="sxs-lookup"><span data-stu-id="5becb-110">First, you create a service agreement and set the **Combine service orders** option to **By service agreement**.</span></span>

1. <span data-ttu-id="5becb-111">Valitse **Huoltosopimukset**</span><span class="sxs-lookup"><span data-stu-id="5becb-111">Click **Service agreements**</span></span>
2. <span data-ttu-id="5becb-112">Luo uusi huoltosopimus valitsemalla **toimintoruudun** **Huoltosopimus**-välilehden **Uusi**-ryhmässä **Huoltosopimus**.</span><span class="sxs-lookup"><span data-stu-id="5becb-112">On the **Action Pane**, on the **Service agreement** tab, in the **New** group, click **Service agreement** to create a new service agreement.</span></span>
3. <span data-ttu-id="5becb-113">Kirjoita kuvaus, valitse projekti **Projektitunnus**-kentässä anna päivämäärä **Alkamispäivä**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="5becb-113">Enter a description, select a project in the **Project ID** field, and enter a date in the **Start date** field.</span></span>
4. <span data-ttu-id="5becb-114">Valitse **Yhdistä huoltotilaukset** -kentässä **Huoltosopimuksen mukaan**.</span><span class="sxs-lookup"><span data-stu-id="5becb-114">In the **Combine service orders** field, select **By service agreement**.</span></span>

<span data-ttu-id="5becb-115">Nyt olet luonut seuraavan huoltosopimuksen:</span><span class="sxs-lookup"><span data-stu-id="5becb-115">You have now created the following service agreement:</span></span>

| <span data-ttu-id="5becb-116">Project</span><span class="sxs-lookup"><span data-stu-id="5becb-116">Project</span></span>      | <span data-ttu-id="5becb-117">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="5becb-117">Start date</span></span>                                                                         |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5becb-118">Oma projekti</span><span class="sxs-lookup"><span data-stu-id="5becb-118">Your project</span></span> | <span data-ttu-id="5becb-119">Projektille määritetty päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="5becb-119">The date you specified for the project.</span></span> <span data-ttu-id="5becb-120">Tässä esimerkissä käytetään kuluvaa päivämäärää.</span><span class="sxs-lookup"><span data-stu-id="5becb-120">In this example, the current date is used.</span></span> |

### <a name="create-a-service-agreement-line"></a><span data-ttu-id="5becb-121">Huoltosopimusrivin luominen</span><span class="sxs-lookup"><span data-stu-id="5becb-121">Create a service agreement line</span></span>

<span data-ttu-id="5becb-122">Seuraavaksi luot huoltosopimusrivin, jonka tapahtumalajina on **Tunti**.</span><span class="sxs-lookup"><span data-stu-id="5becb-122">Next, you create a service agreement line that has the transaction type **Hour**.</span></span>

<span data-ttu-id="5becb-123">Esimerkin tämän osan viimeistely edellyttää, että luot 10 päivän huoltovälin **Huoltovälit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="5becb-123">To complete this part of the example, you must create a service interval of 10 days in the **Service intervals** page.</span></span> 

1. <span data-ttu-id="5becb-124">Valitse juuri luomasi huoltosopimus.</span><span class="sxs-lookup"><span data-stu-id="5becb-124">Select the service agreement that you just created.</span></span> 
2. <span data-ttu-id="5becb-125">Luo **Huoltosopimukset**-sivun alaruutuun uusi rivi valitsemalla **Rivit**-pikavälilehdessä **Lisää**-painike.</span><span class="sxs-lookup"><span data-stu-id="5becb-125">On the **Lines** FastTab, click the **Add** button to create a new line in the lower pane of the **Service agreements** page.</span></span>
3. <span data-ttu-id="5becb-126">Valitse **Tapahtumalaji**-kentässä **Tunti**.</span><span class="sxs-lookup"><span data-stu-id="5becb-126">In the **Transaction type** field, select **Hour**.</span></span>
4. <span data-ttu-id="5becb-127">Valitse **Työntekijä**-kentässä työntekijä, joka toimittaa huollon.</span><span class="sxs-lookup"><span data-stu-id="5becb-127">In the **Worker** field, select the worker who will deliver the service.</span></span>
5. <span data-ttu-id="5becb-128">Valitse **Huoltoväli**-kentässä 10 päivän väli.</span><span class="sxs-lookup"><span data-stu-id="5becb-128">In the **Service interval** field, select the 10 days interval.</span></span>

<span data-ttu-id="5becb-129">Olet nyt luonut huoltosopimusrivin, jossa on seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="5becb-129">You have now created a service agreement line with the following information:</span></span>

| <span data-ttu-id="5becb-130">Tapahtumalaji</span><span class="sxs-lookup"><span data-stu-id="5becb-130">Transaction type</span></span> | <span data-ttu-id="5becb-131">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="5becb-131">Start date</span></span>                               | <span data-ttu-id="5becb-132">Huoltoväli</span><span class="sxs-lookup"><span data-stu-id="5becb-132">Service interval</span></span> |
|------------------|------------------------------------------|------------------|
| <span data-ttu-id="5becb-133">Tunti</span><span class="sxs-lookup"><span data-stu-id="5becb-133">Hour</span></span>             | <span data-ttu-id="5becb-134">Nykyinen päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="5becb-134">The current date.</span></span>                        | <span data-ttu-id="5becb-135">Joka 10. päivä</span><span class="sxs-lookup"><span data-stu-id="5becb-135">Every 10 days</span></span>    |
| <span data-ttu-id="5becb-136">Työntekijä</span><span class="sxs-lookup"><span data-stu-id="5becb-136">Worker</span></span>           | <span data-ttu-id="5becb-137">Huollon suorittava työntekijä.</span><span class="sxs-lookup"><span data-stu-id="5becb-137">The worker who will perform the service.</span></span> |                  |

<span data-ttu-id="5becb-138">Riville ei ole määritetty aikaikkunaa.</span><span class="sxs-lookup"><span data-stu-id="5becb-138">There is no time window specified for the line.</span></span> 

### <a name="create-planned-service-orders"></a><span data-ttu-id="5becb-139">Suunniteltujen huoltotilausten luominen</span><span class="sxs-lookup"><span data-stu-id="5becb-139">Create planned service orders</span></span>

<span data-ttu-id="5becb-140">Voit nyt luoda tulevan kuukauden suunnitellut huoltotilaukset ja huoltotilausrivit.</span><span class="sxs-lookup"><span data-stu-id="5becb-140">You can now create planned service orders and service order lines for the coming month.</span></span>

1. <span data-ttu-id="5becb-141">Valitse **Huoltosopimukset**-sivun **toimintoruudun** **Toimita**-välilehdessä **Suunnitellut huoltotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="5becb-141">In the **Service agreements** page, on the **Action Pane**, on the **Deliver** tab, click **Planned service orders**.</span></span>
2. <span data-ttu-id="5becb-142">Anna **Huoltotilausten luominen** -sivulla kuluva päivämäärä **Päivämäärästä**-kentässä ja kuukauden päässä kuluvasta päivästä oleva päivämäärä **Päivämäärään**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="5becb-142">In the **Create service orders** page, enter the current date in the **From date** field and a date that is one month from the current date in the **To date** field.</span></span>
3. <span data-ttu-id="5becb-143">Siirrä **Tunti**-liukusäädin **Kyllä**-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="5becb-143">Set the **Hour** slider to **Yes**.</span></span> 
4. <span data-ttu-id="5becb-144">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="5becb-144">Click **OK**.</span></span>

<span data-ttu-id="5becb-145">Koska huoltotilausta ei ole ryhmitelty (jonka määrittää **Yhdistä huoltotilaukset** -kentän **Huoltosopimuksen mukaan** -asetus), kullekin huoltotilaukselle luodaan yksi huoltotilausrivi.</span><span class="sxs-lookup"><span data-stu-id="5becb-145">Because there is no grouping on the service order (defined by the **By service agreement** option in the **Combine service orders** field), one service order line is created per service order.</span></span>

### <a name="service-orders-created"></a><span data-ttu-id="5becb-146">Luodut huoltotilaukset</span><span class="sxs-lookup"><span data-stu-id="5becb-146">Service orders created</span></span>

<span data-ttu-id="5becb-147">**Luo huoltotilaukset** -valintaikkunassa määritetylle aikavälille on luotu kolme huoltotilausriviä.</span><span class="sxs-lookup"><span data-stu-id="5becb-147">Three service order lines have been created within the time frame that you specified in the **Create service orders** dialog box.</span></span> <span data-ttu-id="5becb-148">Voit tarkastella huoltotilausrivejä **Huoltosopimukset**-sivulla (**toimintoruutu** \> **Toimita**-välilehti \>**Näytä**-painike).</span><span class="sxs-lookup"><span data-stu-id="5becb-148">You can view the service order lines in the **Service agreements** page (**Action Pane** \> **Deliver** tab \>**View** button).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5becb-149">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="5becb-149">Related topics</span></span>

[<span data-ttu-id="5becb-150">Huoltovälien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5becb-150">Set up service intervals</span></span>](set-up-service-intervals.md)  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]