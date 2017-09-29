--- 
title: "Siirtoasiakirjojen määrittäminen tavaroiden siirrolle yrityksen sisällä"
description: "Tässä menettelyssä kuvataan, miten yrityksen sisäisen tavaroidensiirron siirtoasiakirjat luodaan."
author: v-oloski
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2f10f627f33108b8750a1d71d24a99763178e2ef
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-the-transfer-documents-for-goods-movement-inside-a-company"></a><span data-ttu-id="acdad-103">Siirtoasiakirjojen määrittäminen tavaroiden siirrolle yrityksen sisällä</span><span class="sxs-lookup"><span data-stu-id="acdad-103">Set up the transfer documents for goods movement inside a company</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="acdad-104">Tässä menettelyssä kuvataan, miten yrityksen sisäisen tavaroidensiirron siirtoasiakirjat luodaan.</span><span class="sxs-lookup"><span data-stu-id="acdad-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="acdad-105">Tämä menettely on käytettävissä vain yrityksille, joiden ensisijainen osoite on Liettuassa.</span><span class="sxs-lookup"><span data-stu-id="acdad-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="acdad-106">Tämä menettely luotiin käyttämällä demotietojen DEMF-yritystä niin, että yrityksen ensisijainen osoite on Liettuassa.</span><span class="sxs-lookup"><span data-stu-id="acdad-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="acdad-107">"Yrityksen sisäisten tavaransiirtojen siirtoasiakirjojen määrittäminen" -menettely on suoritettava ennen, kuin suoritat tämän menettelyn.</span><span class="sxs-lookup"><span data-stu-id="acdad-107">Before you can complete this procedure, you must complete the “Set up transfer documents for goods movement inside a company” procedure.</span></span> <span data-ttu-id="acdad-108">Menettely on tarkoitettu varastokirjanpitäjille.</span><span class="sxs-lookup"><span data-stu-id="acdad-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="acdad-109">Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="acdad-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="acdad-110">Siirtotilauksen luonti</span><span class="sxs-lookup"><span data-stu-id="acdad-110">Create a transfer order</span></span>
1. <span data-ttu-id="acdad-111">Valitse Varastonhallinta > Saapuvat tilaukset > Siirtotilaus.</span><span class="sxs-lookup"><span data-stu-id="acdad-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="acdad-112">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="acdad-112">Click New.</span></span>
3. <span data-ttu-id="acdad-113">Anna tai valitse Varastosta-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="acdad-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="acdad-114">Anna tai valitse Varastoon-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="acdad-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="acdad-115">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="acdad-115">Click Add.</span></span>
6. <span data-ttu-id="acdad-116">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="acdad-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="acdad-117">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="acdad-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="acdad-118">Täytä siirtotilauksen kuljetustiedot</span><span class="sxs-lookup"><span data-stu-id="acdad-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="acdad-119">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="acdad-119">Click Save.</span></span>
2. <span data-ttu-id="acdad-120">Valitse toimintoruudussa Lähetys.</span><span class="sxs-lookup"><span data-stu-id="acdad-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="acdad-121">Valitse Kuljetustiedot.</span><span class="sxs-lookup"><span data-stu-id="acdad-121">Click Transportation details.</span></span>
4. <span data-ttu-id="acdad-122">Valitse Tulosta kuljetustiedot -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="acdad-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="acdad-123">Anna tai valitse Tuotteiden hyväksyjä -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="acdad-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="acdad-124">Kirjoita arvo Paketti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="acdad-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="acdad-125">Kirjoita arvo Lastin riskitaso -kenttään.</span><span class="sxs-lookup"><span data-stu-id="acdad-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="acdad-126">Syötä tai valitse arvo Rahdinkuljettaja-kenttään.</span><span class="sxs-lookup"><span data-stu-id="acdad-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="acdad-127">Syötä tai valitse arvo Malli-kentässä.</span><span class="sxs-lookup"><span data-stu-id="acdad-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="acdad-128">Kirjoita Rekisteröintinumero-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="acdad-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="acdad-129">Kirjoita Perävaunun rekisterinumero -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="acdad-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="acdad-130">Syötä tai valitse arvo Kuljettaja-kenttään.</span><span class="sxs-lookup"><span data-stu-id="acdad-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="acdad-131">Kirjoita arvo Kuljettajan nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="acdad-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="acdad-132">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="acdad-132">Click Save.</span></span>
15. <span data-ttu-id="acdad-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="acdad-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="acdad-134">Näytä kirjaamattoman siirtotilauksen pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="acdad-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="acdad-135">Valitse Pakkausluettelo.</span><span class="sxs-lookup"><span data-stu-id="acdad-135">Click Packing slip.</span></span>
2. <span data-ttu-id="acdad-136">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="acdad-136">Click OK.</span></span>
3. <span data-ttu-id="acdad-137">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="acdad-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="acdad-138">Näytä kirjatun siirtotilauksen pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="acdad-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="acdad-139">Valitse toimintoruudussa Siirtotilaus.</span><span class="sxs-lookup"><span data-stu-id="acdad-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="acdad-140">Valitse toimintoruudussa Lähetys.</span><span class="sxs-lookup"><span data-stu-id="acdad-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="acdad-141">Valitse Siirtotilauksen lähettäminen.</span><span class="sxs-lookup"><span data-stu-id="acdad-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="acdad-142">Valitse Yleiset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="acdad-142">Click the General tab.</span></span>
5. <span data-ttu-id="acdad-143">Valitse vaihtoehto Päivitä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="acdad-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="acdad-144">Valitse Yhteenveto-välilehti.</span><span class="sxs-lookup"><span data-stu-id="acdad-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="acdad-145">Kirjoita arvo Pakkausluettelo-kenttään.</span><span class="sxs-lookup"><span data-stu-id="acdad-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="acdad-146">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="acdad-146">Click OK.</span></span>
9. <span data-ttu-id="acdad-147">Valitse toimintoruudussa Lähetys.</span><span class="sxs-lookup"><span data-stu-id="acdad-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="acdad-148">Valitse Pakkausluettelo.</span><span class="sxs-lookup"><span data-stu-id="acdad-148">Click Packing slip.</span></span>
11. <span data-ttu-id="acdad-149">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="acdad-149">Click OK.</span></span>


