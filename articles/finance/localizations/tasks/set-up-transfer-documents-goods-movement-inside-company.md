---
title: Siirtoasiakirjojen määrittäminen tavaroiden siirrolle yrityksen sisällä
description: Tässä menettelyssä kuvataan, miten yrityksen sisäisen tavaroidensiirron siirtoasiakirjat luodaan.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe4dd04595c961e1c66178e6ac6955e945869ded
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185678"
---
# <a name="set-up-the-transfer-documents-for-goods-movement-inside-a-company"></a><span data-ttu-id="529e8-103">Siirtoasiakirjojen määrittäminen tavaroiden siirrolle yrityksen sisällä</span><span class="sxs-lookup"><span data-stu-id="529e8-103">Set up the transfer documents for goods movement inside a company</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="529e8-104">Tässä menettelyssä kuvataan, miten yrityksen sisäisen tavaroidensiirron siirtoasiakirjat luodaan.</span><span class="sxs-lookup"><span data-stu-id="529e8-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="529e8-105">Tämä menettely on käytettävissä vain yrityksille, joiden ensisijainen osoite on Liettuassa.</span><span class="sxs-lookup"><span data-stu-id="529e8-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="529e8-106">Tämä menettely luotiin käyttämällä demotietojen DEMF-yritystä niin, että yrityksen ensisijainen osoite on Liettuassa.</span><span class="sxs-lookup"><span data-stu-id="529e8-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="529e8-107">"Yrityksen sisäisten tavaransiirtojen siirtoasiakirjojen määrittäminen" -menettely on suoritettava ennen, kuin suoritat tämän menettelyn.</span><span class="sxs-lookup"><span data-stu-id="529e8-107">Before you can complete this procedure, you must complete the “Set up transfer documents for goods movement inside a company” procedure.</span></span> <span data-ttu-id="529e8-108">Menettely on tarkoitettu varastokirjanpitäjille.</span><span class="sxs-lookup"><span data-stu-id="529e8-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="529e8-109">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="529e8-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="529e8-110">Siirtotilauksen luonti</span><span class="sxs-lookup"><span data-stu-id="529e8-110">Create a transfer order</span></span>
1. <span data-ttu-id="529e8-111">Valitse Varastonhallinta > Saapuvat tilaukset > Siirtotilaus.</span><span class="sxs-lookup"><span data-stu-id="529e8-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="529e8-112">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="529e8-112">Click New.</span></span>
3. <span data-ttu-id="529e8-113">Anna tai valitse Varastosta-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="529e8-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="529e8-114">Anna tai valitse Varastoon-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="529e8-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="529e8-115">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="529e8-115">Click Add.</span></span>
6. <span data-ttu-id="529e8-116">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="529e8-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="529e8-117">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="529e8-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="529e8-118">Täytä siirtotilauksen kuljetustiedot</span><span class="sxs-lookup"><span data-stu-id="529e8-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="529e8-119">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="529e8-119">Click Save.</span></span>
2. <span data-ttu-id="529e8-120">Valitse toimintoruudussa Lähetys.</span><span class="sxs-lookup"><span data-stu-id="529e8-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="529e8-121">Valitse Kuljetustiedot.</span><span class="sxs-lookup"><span data-stu-id="529e8-121">Click Transportation details.</span></span>
4. <span data-ttu-id="529e8-122">Valitse Tulosta kuljetustiedot -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="529e8-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="529e8-123">Anna tai valitse Tuotteiden hyväksyjä -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="529e8-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="529e8-124">Kirjoita arvo Paketti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="529e8-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="529e8-125">Kirjoita arvo Lastin riskitaso -kenttään.</span><span class="sxs-lookup"><span data-stu-id="529e8-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="529e8-126">Syötä tai valitse arvo Rahdinkuljettaja-kenttään.</span><span class="sxs-lookup"><span data-stu-id="529e8-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="529e8-127">Syötä tai valitse arvo Malli-kentässä.</span><span class="sxs-lookup"><span data-stu-id="529e8-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="529e8-128">Kirjoita Rekisteröintinumero-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="529e8-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="529e8-129">Kirjoita Perävaunun rekisterinumero -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="529e8-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="529e8-130">Syötä tai valitse arvo Kuljettaja-kenttään.</span><span class="sxs-lookup"><span data-stu-id="529e8-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="529e8-131">Kirjoita arvo Kuljettajan nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="529e8-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="529e8-132">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="529e8-132">Click Save.</span></span>
15. <span data-ttu-id="529e8-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="529e8-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="529e8-134">Näytä kirjaamattoman siirtotilauksen pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="529e8-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="529e8-135">Valitse Pakkausluettelo.</span><span class="sxs-lookup"><span data-stu-id="529e8-135">Click Packing slip.</span></span>
2. <span data-ttu-id="529e8-136">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="529e8-136">Click OK.</span></span>
3. <span data-ttu-id="529e8-137">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="529e8-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="529e8-138">Näytä kirjatun siirtotilauksen pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="529e8-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="529e8-139">Valitse toimintoruudussa Siirtotilaus.</span><span class="sxs-lookup"><span data-stu-id="529e8-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="529e8-140">Valitse toimintoruudussa Lähetys.</span><span class="sxs-lookup"><span data-stu-id="529e8-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="529e8-141">Valitse Siirtotilauksen lähettäminen.</span><span class="sxs-lookup"><span data-stu-id="529e8-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="529e8-142">Valitse Yleiset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="529e8-142">Click the General tab.</span></span>
5. <span data-ttu-id="529e8-143">Valitse vaihtoehto Päivitä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="529e8-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="529e8-144">Valitse Yhteenveto-välilehti.</span><span class="sxs-lookup"><span data-stu-id="529e8-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="529e8-145">Kirjoita arvo Pakkausluettelo-kenttään.</span><span class="sxs-lookup"><span data-stu-id="529e8-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="529e8-146">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="529e8-146">Click OK.</span></span>
9. <span data-ttu-id="529e8-147">Valitse toimintoruudussa Lähetys.</span><span class="sxs-lookup"><span data-stu-id="529e8-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="529e8-148">Valitse Pakkausluettelo.</span><span class="sxs-lookup"><span data-stu-id="529e8-148">Click Packing slip.</span></span>
11. <span data-ttu-id="529e8-149">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="529e8-149">Click OK.</span></span>
