---
title: Lähetyksen rahdinkuljettajien määrittäminen
description: Tässä aiheessa kuvataan, kuinka voit asettaa rahdinkuljettajan ja määrittää tiedot, kuten palvelu, lähetystila, kuljetuksen maksuväline, kuljetusrajoitukset ja lähetyshinta.
author: ShylaThompson
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e6a29dce877a53d125c5a151da6cfbb13d46b29
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201591"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="8d02f-103">Lähetyksen rahdinkuljettajien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8d02f-103">Set up shipping carriers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8d02f-104">Tässä aiheessa kuvataan, kuinka voit asettaa rahdinkuljettajan ja määrittää tiedot, kuten palvelu, lähetystila, kuljetuksen maksuväline, kuljetusrajoitukset ja lähetyshinta.</span><span class="sxs-lookup"><span data-stu-id="8d02f-104">This topic shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="8d02f-105">Kuljetuskoordinaattori voi sitten määrittää lähtevälle tai saapuvalle kuormalle rahdinkuljettajan.</span><span class="sxs-lookup"><span data-stu-id="8d02f-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="8d02f-106">Uuden lähetyksen rahdinkuljettajan luominen</span><span class="sxs-lookup"><span data-stu-id="8d02f-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="8d02f-107">Valitse **Siirtymisruutu > Moduulit > Kuljetustenhallinta > Asetukset > Rahdinkuljettajat > Lähetyksen rahdinkuljettajat**.</span><span class="sxs-lookup"><span data-stu-id="8d02f-107">Go to **Navigation pane > Modules > Transportation management > Setup > Carriers > Shipping carriers**.</span></span>
2. <span data-ttu-id="8d02f-108">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="8d02f-108">Select **New** in the Action pane.</span></span>
3. <span data-ttu-id="8d02f-109">Syötä **Lähetyksen rahdinkuljettaja** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="8d02f-109">In the **Shipping carrier** field, type a value.</span></span>
4. <span data-ttu-id="8d02f-110">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8d02f-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="8d02f-111">Valitse **Tila**-kentästä vaihtoehto avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="8d02f-111">In the **Mode** field, select an option from the drop-down menu.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="8d02f-112">Lähetyksen rahdinkuljettajan yleistietojen täyttäminen</span><span class="sxs-lookup"><span data-stu-id="8d02f-112">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="8d02f-113">Ota käyttöön **Yleiskuvaus**-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="8d02f-113">Toggle the expansion of the **Overview** section.</span></span>
2. <span data-ttu-id="8d02f-114">Valitse **Aktivoi lähetyksen rahdinkuljettaja** -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="8d02f-114">Check or uncheck the **Activate shipping carrier** checkbox.</span></span>
3. <span data-ttu-id="8d02f-115">Valitse **Toimittajan tili**-kentästä vaihtoehto avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="8d02f-115">In the **Vendor account** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="8d02f-116">Valitse toimittajan tili, johon lähetyksen rahdinkuljettaja liitetään.</span><span class="sxs-lookup"><span data-stu-id="8d02f-116">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="8d02f-117">Valitse vaihtoehto **Kuljetuksen maksuvälineen tyyppi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="8d02f-117">In the **Transportation tender type** field, select an option.</span></span> <span data-ttu-id="8d02f-118">Valitse **Manuaalinen** käyttääksesi Kuljetuksen maksuväline -sivua tai valitse **EDI**, kun haluat päivittää maksuvälineen sähköistä tiedonsiirtoa (EDI = Electronic Data Interchange) käyttäen.</span><span class="sxs-lookup"><span data-stu-id="8d02f-118">Select **Manual** to use the Transportation Tender page, or select **EDI** to update the tender by using Electronic Data Interchange (EDI).</span></span>  
5. <span data-ttu-id="8d02f-119">Valitse **Aktivoi rahdinkuljettajan luokitus** -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="8d02f-119">Check or uncheck the **Activate carrier rating** checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="8d02f-120">Lähetyksen rahdinkuljettajan tarvitsemien palveluiden luominen</span><span class="sxs-lookup"><span data-stu-id="8d02f-120">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="8d02f-121">Ota käyttöön **Palvelut**-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="8d02f-121">Toggle the expansion of the **Services** section.</span></span>
2. <span data-ttu-id="8d02f-122">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="8d02f-122">Select **New**.</span></span>
3. <span data-ttu-id="8d02f-123">Syötä **Rahdinkuljettajan palvelu** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="8d02f-123">In the **Carrier service** field, type a value.</span></span>
4. <span data-ttu-id="8d02f-124">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8d02f-124">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="8d02f-125">Valitse **Kuljetusmenetelmä**-kentästä vaihtoehto avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="8d02f-125">In the **Transportation method** field, select an option from the drop-down menu.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="8d02f-126">Rahdinkuljettajan osoitteen määrittäminen (valinnainen)</span><span class="sxs-lookup"><span data-stu-id="8d02f-126">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="8d02f-127">Ota käyttöön **Osoitteet**-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="8d02f-127">Toggle the expansion of the **Addresses** section.</span></span>
2. <span data-ttu-id="8d02f-128">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="8d02f-128">Select **New**.</span></span>
3. <span data-ttu-id="8d02f-129">Kirjoita **Nimi tai kuvaus** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="8d02f-129">In the **Name or description** field, type a value.</span></span>
4. <span data-ttu-id="8d02f-130">Valitse **Maa/alue**-kentästä vaihtoehto avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="8d02f-130">In the **Country/region** field, select an option from the drop-down menu.</span></span>
5. <span data-ttu-id="8d02f-131">Valitse **Postinumero**-kentästä vaihtoehto avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="8d02f-131">In the **ZIP/postal code** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="8d02f-132">Kirjoita arvo **Katuosoite**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8d02f-132">In the **Street** field, type a value.</span></span>
7. <span data-ttu-id="8d02f-133">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d02f-133">Select **OK**.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="8d02f-134">Lähetyksen rahdinkuljettajan luokituksen profiilin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="8d02f-134">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="8d02f-135">Ota **Luokituksen profiilit** -osan laajennus käyttöön.</span><span class="sxs-lookup"><span data-stu-id="8d02f-135">Toggle the expansion of the **Rating profiles** section.</span></span>
2. <span data-ttu-id="8d02f-136">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="8d02f-136">Select **New**.</span></span>
3. <span data-ttu-id="8d02f-137">Syötä **Luokituksen profiili** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="8d02f-137">In the **Rating profile** field, type a value.</span></span>
4. <span data-ttu-id="8d02f-138">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8d02f-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="8d02f-139">Valitse **Toimipaikka**-kentästä vaihtoehto avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="8d02f-139">In the **Site** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="8d02f-140">Valitse **Varasto**-kentästä vaihtoehto avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="8d02f-140">In the **Warehouse** field, select an option from the drop-down menu.</span></span>
7. <span data-ttu-id="8d02f-141">Valitse **Hinnan laskenta**-kentästä vaihtoehto avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="8d02f-141">In the **Rate engine** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="8d02f-142">Valitse hinnan laskenta rahdinkuljettajan yhteystietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="8d02f-142">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
8. <span data-ttu-id="8d02f-143">Valitse **Hinnan päätiedot**-kentästä vaihtoehto avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="8d02f-143">In the **Rate master** field, select an option from the drop-down menu.</span></span>
9. <span data-ttu-id="8d02f-144">Valitse **Siirtoajan laskenta**-kentästä vaihtoehto avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="8d02f-144">In the **Transit time engine** field, select an option from the drop-down menu.</span></span>
10. <span data-ttu-id="8d02f-145">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="8d02f-145">Select **Save**.</span></span>

