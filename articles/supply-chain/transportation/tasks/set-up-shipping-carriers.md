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
ms.search.form: TMSShippingCarrierCustomerAccount,TMSCarrier
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1ec19288f01ceb0bb3021cf549af1c38746785c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233580"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="fca91-103">Lähetyksen rahdinkuljettajien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="fca91-103">Set up shipping carriers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fca91-104">Tässä aiheessa kuvataan, kuinka voit asettaa rahdinkuljettajan ja määrittää tiedot, kuten palvelu, lähetystila, kuljetuksen maksuväline, kuljetusrajoitukset ja lähetyshinta.</span><span class="sxs-lookup"><span data-stu-id="fca91-104">This topic shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="fca91-105">Kuljetuskoordinaattori voi sitten määrittää lähtevälle tai saapuvalle kuormalle rahdinkuljettajan.</span><span class="sxs-lookup"><span data-stu-id="fca91-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="fca91-106">Uuden lähetyksen rahdinkuljettajan luominen</span><span class="sxs-lookup"><span data-stu-id="fca91-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="fca91-107">Valitse **Siirtymisruutu > Moduulit > Kuljetustenhallinta > Asetukset > Rahdinkuljettajat > Lähetyksen rahdinkuljettajat**.</span><span class="sxs-lookup"><span data-stu-id="fca91-107">Go to **Navigation pane > Modules > Transportation management > Setup > Carriers > Shipping carriers**.</span></span>
2. <span data-ttu-id="fca91-108">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="fca91-108">Select **New** on the Action Pane.</span></span>
3. <span data-ttu-id="fca91-109">Syötä **Lähetyksen rahdinkuljettaja** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="fca91-109">In the **Shipping carrier** field, type a value.</span></span>
4. <span data-ttu-id="fca91-110">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="fca91-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="fca91-111">Valitse **Tila**-kentästä vaihtoehto avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="fca91-111">In the **Mode** field, select an option from the drop-down menu.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="fca91-112">Lähetyksen rahdinkuljettajan yleistietojen täyttäminen</span><span class="sxs-lookup"><span data-stu-id="fca91-112">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="fca91-113">Ota käyttöön **Yleiskuvaus**-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="fca91-113">Toggle the expansion of the **Overview** section.</span></span>
2. <span data-ttu-id="fca91-114">Valitse **Aktivoi lähetyksen rahdinkuljettaja** -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="fca91-114">Check or uncheck the **Activate shipping carrier** checkbox.</span></span>
3. <span data-ttu-id="fca91-115">Valitse **Toimittajan tili**-kentästä vaihtoehto avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="fca91-115">In the **Vendor account** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="fca91-116">Valitse toimittajan tili, johon lähetyksen rahdinkuljettaja liitetään.</span><span class="sxs-lookup"><span data-stu-id="fca91-116">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="fca91-117">Valitse vaihtoehto **Kuljetuksen maksuvälineen tyyppi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="fca91-117">In the **Transportation tender type** field, select an option.</span></span> <span data-ttu-id="fca91-118">Valitse **Manuaalinen** käyttääksesi Kuljetuksen maksuväline -sivua tai valitse **EDI**, kun haluat päivittää maksuvälineen sähköistä tiedonsiirtoa (EDI = Electronic Data Interchange) käyttäen.</span><span class="sxs-lookup"><span data-stu-id="fca91-118">Select **Manual** to use the Transportation Tender page, or select **EDI** to update the tender by using Electronic Data Interchange (EDI).</span></span>  
5. <span data-ttu-id="fca91-119">Valitse **Aktivoi rahdinkuljettajan luokitus** -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="fca91-119">Check or uncheck the **Activate carrier rating** checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="fca91-120">Lähetyksen rahdinkuljettajan tarvitsemien palveluiden luominen</span><span class="sxs-lookup"><span data-stu-id="fca91-120">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="fca91-121">Ota käyttöön **Palvelut**-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="fca91-121">Toggle the expansion of the **Services** section.</span></span>
2. <span data-ttu-id="fca91-122">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="fca91-122">Select **New**.</span></span>
3. <span data-ttu-id="fca91-123">Syötä **Rahdinkuljettajan palvelu** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="fca91-123">In the **Carrier service** field, type a value.</span></span>
4. <span data-ttu-id="fca91-124">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="fca91-124">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="fca91-125">Valitse **Kuljetusmenetelmä**-kentästä vaihtoehto avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="fca91-125">In the **Transportation method** field, select an option from the drop-down menu.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="fca91-126">Rahdinkuljettajan osoitteen määrittäminen (valinnainen)</span><span class="sxs-lookup"><span data-stu-id="fca91-126">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="fca91-127">Ota käyttöön **Osoitteet**-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="fca91-127">Toggle the expansion of the **Addresses** section.</span></span>
2. <span data-ttu-id="fca91-128">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="fca91-128">Select **New**.</span></span>
3. <span data-ttu-id="fca91-129">Kirjoita **Nimi tai kuvaus** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="fca91-129">In the **Name or description** field, type a value.</span></span>
4. <span data-ttu-id="fca91-130">Valitse **Maa/alue**-kentästä vaihtoehto avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="fca91-130">In the **Country/region** field, select an option from the drop-down menu.</span></span>
5. <span data-ttu-id="fca91-131">Valitse **Postinumero**-kentästä vaihtoehto avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="fca91-131">In the **ZIP/postal code** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="fca91-132">Kirjoita arvo **Katuosoite**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="fca91-132">In the **Street** field, type a value.</span></span>
7. <span data-ttu-id="fca91-133">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="fca91-133">Select **OK**.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="fca91-134">Lähetyksen rahdinkuljettajan luokituksen profiilin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="fca91-134">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="fca91-135">Ota **Luokituksen profiilit** -osan laajennus käyttöön.</span><span class="sxs-lookup"><span data-stu-id="fca91-135">Toggle the expansion of the **Rating profiles** section.</span></span>
2. <span data-ttu-id="fca91-136">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="fca91-136">Select **New**.</span></span>
3. <span data-ttu-id="fca91-137">Syötä **Luokituksen profiili** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="fca91-137">In the **Rating profile** field, type a value.</span></span>
4. <span data-ttu-id="fca91-138">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="fca91-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="fca91-139">Valitse **Toimipaikka**-kentästä vaihtoehto avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="fca91-139">In the **Site** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="fca91-140">Valitse **Varasto**-kentästä vaihtoehto avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="fca91-140">In the **Warehouse** field, select an option from the drop-down menu.</span></span>
7. <span data-ttu-id="fca91-141">Valitse **Hinnan laskenta**-kentästä vaihtoehto avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="fca91-141">In the **Rate engine** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="fca91-142">Valitse hinnan laskenta rahdinkuljettajan yhteystietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="fca91-142">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
8. <span data-ttu-id="fca91-143">Valitse **Hinnan päätiedot**-kentästä vaihtoehto avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="fca91-143">In the **Rate master** field, select an option from the drop-down menu.</span></span>
9. <span data-ttu-id="fca91-144">Valitse **Siirtoajan laskenta**-kentästä vaihtoehto avattavasta valikosta.</span><span class="sxs-lookup"><span data-stu-id="fca91-144">In the **Transit time engine** field, select an option from the drop-down menu.</span></span>
10. <span data-ttu-id="fca91-145">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="fca91-145">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]