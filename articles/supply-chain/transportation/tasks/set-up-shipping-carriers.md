---
title: Lähetyksen rahdinkuljettajien määrittäminen
description: Tässä menettelyssä kuvataan, kuinka voit asettaa rahdinkuljettajan ja määrittää tiedot, kuten palvelu, lähetystila, kuljetuksen maksuväline, kuljetusrajoitukset ja lähetyshinta.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c5ac13d17c97f20ee79e7faf57c570f02158424
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "314483"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="81419-103">Lähetyksen rahdinkuljettajien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="81419-103">Set up shipping carriers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="81419-104">Tässä menettelyssä kuvataan, kuinka voit asettaa rahdinkuljettajan ja määrittää tiedot, kuten palvelu, lähetystila, kuljetuksen maksuväline, kuljetusrajoitukset ja lähetyshinta.</span><span class="sxs-lookup"><span data-stu-id="81419-104">This procedure shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="81419-105">Kuljetuskoordinaattori voi sitten määrittää lähtevälle tai saapuvalle kuormalle rahdinkuljettajan.</span><span class="sxs-lookup"><span data-stu-id="81419-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="81419-106">Uuden lähetyksen rahdinkuljettajan luominen</span><span class="sxs-lookup"><span data-stu-id="81419-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="81419-107">Valitse Kuljetustenhallinta > Asetukset > Rahdinkuljettajat > Lähetyksen rahdinkuljettajat.</span><span class="sxs-lookup"><span data-stu-id="81419-107">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="81419-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="81419-108">Click New.</span></span>
3. <span data-ttu-id="81419-109">Syötä Lähetyksen rahdinkuljettaja -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="81419-109">In the Shipping carrier field, type a value.</span></span>
4. <span data-ttu-id="81419-110">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="81419-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="81419-111">Avaa haku Valitsemalla Tila-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="81419-111">In the Mode field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="81419-112">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="81419-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="81419-113">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="81419-113">In the list, click the link in the selected row.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="81419-114">Lähetyksen rahdinkuljettajan yleistietojen täyttäminen</span><span class="sxs-lookup"><span data-stu-id="81419-114">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="81419-115">Ota käyttöön Yleiskuvaus-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="81419-115">Toggle the expansion of the Overview section.</span></span>
2. <span data-ttu-id="81419-116">Valitse Aktivoi lähetyksen rahdinkuljettaja -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="81419-116">Check or uncheck the Activate shipping carrier checkbox.</span></span>
3. <span data-ttu-id="81419-117">Avaa haku valitsemalla Toimittaja-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="81419-117">In the Vendor field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="81419-118">Valitse toimittajan tili, johon lähetyksen rahdinkuljettaja liitetään.</span><span class="sxs-lookup"><span data-stu-id="81419-118">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="81419-119">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="81419-119">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="81419-120">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="81419-120">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="81419-121">Valitse vaihtoehto Kuljetuksen maksuvälineen tyyppi -kentässä.</span><span class="sxs-lookup"><span data-stu-id="81419-121">In the Transportation tender type field, select an option.</span></span>
    * <span data-ttu-id="81419-122">Valitse Manuaalinen kuljetuksen maksuvälineen käyttö -sivu tai valitse EDI, kun haluat päivittää maksuvälineen sähköistä tiedonsiirtoa (EDI = Electronic Data Interchange).</span><span class="sxs-lookup"><span data-stu-id="81419-122">Select Manual to use the Transportation Tender page, or select EDI to update the tender by using Electronic Data Interchange (EDI).</span></span>  
7. <span data-ttu-id="81419-123">Valitse Aktivoi rahdinkuljettajan luokitus -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="81419-123">Check or uncheck the Activate carrier rating checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="81419-124">Lähetyksen rahdinkuljettajan tarvitsemien palveluiden luominen</span><span class="sxs-lookup"><span data-stu-id="81419-124">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="81419-125">Ota käyttöön Palvelut-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="81419-125">Toggle the expansion of the Services section.</span></span>
2. <span data-ttu-id="81419-126">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="81419-126">Click New.</span></span>
3. <span data-ttu-id="81419-127">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="81419-127">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="81419-128">Syötä Rahdinkuljettajan palvelu -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="81419-128">In the Carrier service field, type a value.</span></span>
5. <span data-ttu-id="81419-129">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="81419-129">In the Name field, type a value.</span></span>
6. <span data-ttu-id="81419-130">Avaa haku valitsemalla Kuljetusmenetelmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="81419-130">In the Transportation method field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="81419-131">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="81419-131">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="81419-132">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="81419-132">In the list, click the link in the selected row.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="81419-133">Rahdinkuljettajan osoitteen määrittäminen (valinnainen)</span><span class="sxs-lookup"><span data-stu-id="81419-133">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="81419-134">Ota käyttöön Osoitteet-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="81419-134">Toggle the expansion of the Addresses section.</span></span>
2. <span data-ttu-id="81419-135">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="81419-135">Click New.</span></span>
3. <span data-ttu-id="81419-136">Kirjoita Nimi tai kuvaus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="81419-136">In the Name or description field, type a value.</span></span>
4. <span data-ttu-id="81419-137">Avaa haku valitsemalla Maa/alue-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="81419-137">In the Country/region field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="81419-138">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="81419-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="81419-139">Avaa haku valitsemalla Postinumero-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="81419-139">In the ZIP/postal code field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="81419-140">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="81419-140">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="81419-141">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="81419-141">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="81419-142">Kirjoita arvo Katuosoite-kenttään.</span><span class="sxs-lookup"><span data-stu-id="81419-142">In the Street field, type a value.</span></span>
10. <span data-ttu-id="81419-143">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="81419-143">Click OK.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="81419-144">Lähetyksen rahdinkuljettajan luokituksen profiilin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="81419-144">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="81419-145">Ota Luokituksen profiilit -osan laajennus käyttöön.</span><span class="sxs-lookup"><span data-stu-id="81419-145">Toggle the expansion of the Rating profiles section.</span></span>
2. <span data-ttu-id="81419-146">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="81419-146">Click New.</span></span>
3. <span data-ttu-id="81419-147">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="81419-147">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="81419-148">Syötä Luokituksen profiili -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="81419-148">In the Rating profile field, type a value.</span></span>
5. <span data-ttu-id="81419-149">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="81419-149">In the Name field, type a value.</span></span>
6. <span data-ttu-id="81419-150">Avaa haku napsauttamalla Toimipaikka-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="81419-150">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="81419-151">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="81419-151">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="81419-152">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="81419-152">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="81419-153">Avaa haku valitsemalla Varasto-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="81419-153">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="81419-154">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="81419-154">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="81419-155">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="81419-155">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="81419-156">Avaa haku valitsemalla Hinnan laskenta -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="81419-156">In the Rate engine field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="81419-157">Valitse hinnan laskenta rahdinkuljettajan yhteystietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="81419-157">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
13. <span data-ttu-id="81419-158">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="81419-158">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="81419-159">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="81419-159">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="81419-160">Avaa haku valitsemalla Hinnan päätiedot -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="81419-160">In the Rate master field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="81419-161">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="81419-161">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="81419-162">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="81419-162">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="81419-163">Avaa haku valitsemalla Siirtoajan laskenta -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="81419-163">In the Transit time engine field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="81419-164">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="81419-164">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="81419-165">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="81419-165">Click Save.</span></span>

