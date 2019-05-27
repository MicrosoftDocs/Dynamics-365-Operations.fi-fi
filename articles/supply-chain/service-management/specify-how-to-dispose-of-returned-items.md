---
title: Palautettujen nimikkeiden poistotavan määrittäminen
description: Palautettujen nimikkeiden poistotavan määrittäminen.
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6fcdfec083aeb9c58d63f6e03542758e4d07e4d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560091"
---
# <a name="specify-how-to-dispose-of-returned-items"></a><span data-ttu-id="76a4f-103">Palautettujen nimikkeiden poistotavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="76a4f-103">Specify how to dispose of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="76a4f-104">Kun käsittelet palautustilausta, sinun on määritettävä palautuksen syykoodi, jonka avulla tunnistetaan miksi tuote palautetaan.</span><span class="sxs-lookup"><span data-stu-id="76a4f-104">When you handle a return order, you must specify a reason return code to identify why the product is being returned.</span></span> <span data-ttu-id="76a4f-105">Sinun on myös myös määritettävä käsittelykoodi ja käsittelytoiminto määrittääksesi mitä itse palautetulle tuotteelle tulisi tehdä.</span><span class="sxs-lookup"><span data-stu-id="76a4f-105">You must also specify a disposition code and a disposition action to determine what should be done with the returned product itself.</span></span>

<span data-ttu-id="76a4f-106">Voit käyttää käsittelykoodia, kun luot palautustilauksen, rekisteröit nimikkeen saapumisen tai päivität pakkausluettelon nimikkeen saapumisen yhteydessä ja päätät karanteenitilauksen.</span><span class="sxs-lookup"><span data-stu-id="76a4f-106">A disposition code can be applied when you create the return order, register item arrival or packing-slip update an item arrival, and end a quarantine order.</span></span>

<span data-ttu-id="76a4f-107">Voit määrittää mitä tahansa tarvitsemiasi käsittelykoodeja liiketoimintaprosessien tukemiseen.</span><span class="sxs-lookup"><span data-stu-id="76a4f-107">You can define any disposition codes that you need in order to support the business processes.</span></span> <span data-ttu-id="76a4f-108">Seuraavassa taulukossa on joukko tavallisesti palautusnimikkeen käsittelyyn käytettyjä koodeja.</span><span class="sxs-lookup"><span data-stu-id="76a4f-108">The following table provides a set of typically used codes to assign return-item disposition.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="76a4f-109">Käsittelytyyppi</span><span class="sxs-lookup"><span data-stu-id="76a4f-109">Disposition type</span></span></p></th>
<th><p><span data-ttu-id="76a4f-110">Yleinen koodi</span><span class="sxs-lookup"><span data-stu-id="76a4f-110">Common code</span></span></p></th>
<th><p><span data-ttu-id="76a4f-111">kuvaus</span><span class="sxs-lookup"><span data-stu-id="76a4f-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="76a4f-112">Luovutus</span><span class="sxs-lookup"><span data-stu-id="76a4f-112">Disposal</span></span></p></td>
<td><p><span data-ttu-id="76a4f-113">Š</span><span class="sxs-lookup"><span data-stu-id="76a4f-113">SC</span></span></p></td>
<td><p><span data-ttu-id="76a4f-114">Hävitä/tuhoa</span><span class="sxs-lookup"><span data-stu-id="76a4f-114">Scrap/Destroy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76a4f-115">Luovutus</span><span class="sxs-lookup"><span data-stu-id="76a4f-115">Disposal</span></span></p></td>
<td><p><span data-ttu-id="76a4f-116">DC</span><span class="sxs-lookup"><span data-stu-id="76a4f-116">DC</span></span></p></td>
<td><p><span data-ttu-id="76a4f-117">Lahjoita hyväntekeväisyyteen</span><span class="sxs-lookup"><span data-stu-id="76a4f-117">Donate to Charity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76a4f-118">Luovutus</span><span class="sxs-lookup"><span data-stu-id="76a4f-118">Disposal</span></span></p></td>
<td><p><span data-ttu-id="76a4f-119">TD</span><span class="sxs-lookup"><span data-stu-id="76a4f-119">TD</span></span></p></td>
<td><p><span data-ttu-id="76a4f-120">Luovuta kolmannelle osapuolelle</span><span class="sxs-lookup"><span data-stu-id="76a4f-120">Third-Party Disposal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76a4f-121">Luovutus</span><span class="sxs-lookup"><span data-stu-id="76a4f-121">Disposal</span></span></p></td>
<td><p><span data-ttu-id="76a4f-122">SL</span><span class="sxs-lookup"><span data-stu-id="76a4f-122">SL</span></span></p></td>
<td><p><span data-ttu-id="76a4f-123">Romuta</span><span class="sxs-lookup"><span data-stu-id="76a4f-123">Salvage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76a4f-124">Luovutus</span><span class="sxs-lookup"><span data-stu-id="76a4f-124">Disposal</span></span></p></td>
<td><p><span data-ttu-id="76a4f-125">TS</span><span class="sxs-lookup"><span data-stu-id="76a4f-125">TS</span></span></p></td>
<td><p><span data-ttu-id="76a4f-126">Myy kolmannelle osapuolelle (jälkimarkkinat)</span><span class="sxs-lookup"><span data-stu-id="76a4f-126">Third-Party Sale (Secondary Markets)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76a4f-127">Korjaa/muokkaa</span><span class="sxs-lookup"><span data-stu-id="76a4f-127">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="76a4f-128">RW</span><span class="sxs-lookup"><span data-stu-id="76a4f-128">RW</span></span></p></td>
<td><p><span data-ttu-id="76a4f-129">Käytä uudelleen</span><span class="sxs-lookup"><span data-stu-id="76a4f-129">Rework</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76a4f-130">Korjaa/muokkaa</span><span class="sxs-lookup"><span data-stu-id="76a4f-130">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="76a4f-131">RF</span><span class="sxs-lookup"><span data-stu-id="76a4f-131">RF</span></span></p></td>
<td><p><span data-ttu-id="76a4f-132">Valmista uudelleen / kunnosta</span><span class="sxs-lookup"><span data-stu-id="76a4f-132">Remanufacture/Refurbish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76a4f-133">Korjaa/muokkaa</span><span class="sxs-lookup"><span data-stu-id="76a4f-133">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="76a4f-134">MD</span><span class="sxs-lookup"><span data-stu-id="76a4f-134">MD</span></span></p></td>
<td><p><span data-ttu-id="76a4f-135">Muokkaa</span><span class="sxs-lookup"><span data-stu-id="76a4f-135">Modify</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76a4f-136">Korjaa/muokkaa</span><span class="sxs-lookup"><span data-stu-id="76a4f-136">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="76a4f-137">RP</span><span class="sxs-lookup"><span data-stu-id="76a4f-137">RP</span></span></p></td>
<td><p><span data-ttu-id="76a4f-138">Korjaa</span><span class="sxs-lookup"><span data-stu-id="76a4f-138">Repair</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76a4f-139">Korjaa/muokkaa</span><span class="sxs-lookup"><span data-stu-id="76a4f-139">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="76a4f-140">VASTAKIRJAUS</span><span class="sxs-lookup"><span data-stu-id="76a4f-140">RV</span></span></p></td>
<td><p><span data-ttu-id="76a4f-141">Palauta myyjälle</span><span class="sxs-lookup"><span data-stu-id="76a4f-141">Return to Vendor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76a4f-142">Muu</span><span class="sxs-lookup"><span data-stu-id="76a4f-142">Other</span></span></p></td>
<td><p><span data-ttu-id="76a4f-143">AI</span><span class="sxs-lookup"><span data-stu-id="76a4f-143">AI</span></span></p></td>
<td><p><span data-ttu-id="76a4f-144">Käytä sellaisenaan</span><span class="sxs-lookup"><span data-stu-id="76a4f-144">Use as is</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76a4f-145">Muu</span><span class="sxs-lookup"><span data-stu-id="76a4f-145">Other</span></span></p></td>
<td><p><span data-ttu-id="76a4f-146">RS</span><span class="sxs-lookup"><span data-stu-id="76a4f-146">RS</span></span></p></td>
<td><p><span data-ttu-id="76a4f-147">Myy eteenpäin</span><span class="sxs-lookup"><span data-stu-id="76a4f-147">Resale</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76a4f-148">Muu</span><span class="sxs-lookup"><span data-stu-id="76a4f-148">Other</span></span></p></td>
<td><p><span data-ttu-id="76a4f-149">EX</span><span class="sxs-lookup"><span data-stu-id="76a4f-149">EX</span></span></p></td>
<td><p><span data-ttu-id="76a4f-150">Vaihda</span><span class="sxs-lookup"><span data-stu-id="76a4f-150">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76a4f-151">Muu</span><span class="sxs-lookup"><span data-stu-id="76a4f-151">Other</span></span></p></td>
<td><p><span data-ttu-id="76a4f-152">MS</span><span class="sxs-lookup"><span data-stu-id="76a4f-152">MS</span></span></p></td>
<td><p><span data-ttu-id="76a4f-153">Muut</span><span class="sxs-lookup"><span data-stu-id="76a4f-153">Miscellaneous</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="76a4f-154">Sinun on määritettävä jokaiselle määrittämällesi käsittelykoodille käsittelytoiminto.</span><span class="sxs-lookup"><span data-stu-id="76a4f-154">For each disposition code that you define, you must select a disposition action.</span></span> <span data-ttu-id="76a4f-155">Käsittelytoiminto määrittää käsittelykoodien fyysiset ja taloudelliset vaikutukset.</span><span class="sxs-lookup"><span data-stu-id="76a4f-155">The disposition action determines the physical and financial implications of the disposition codes.</span></span> <span data-ttu-id="76a4f-156">Käsittelytoiminto määrittää esimerkiksi palautetun nimikkeen fyysisen käsittelyn, palautetun nimikkeen taloudellisen vaikutuksen, ja jos asiakkaalle on lähetettävä korvaavaa nimike.</span><span class="sxs-lookup"><span data-stu-id="76a4f-156">For example, the disposition action determines the physical handling of the returned item, the financial effect of the returned item, and if a replacement item must be sent to the customer.</span></span> <span data-ttu-id="76a4f-157">Voit määrittää rajattoman määrän käsittelykoodeja yrityksesi tarpeiden mukaisesti, mutta valittavissa on vain vain kuusi ennalta asetettua käsittelytapahtumaa.</span><span class="sxs-lookup"><span data-stu-id="76a4f-157">You can define an unlimited number of disposition codes according to your business needs, but there are only six predefined disposition actions that you can select from.</span></span> <span data-ttu-id="76a4f-158">Seuraavassa taulukossa on esitelty käsittelytoiminnot ja niiden määritelmät.</span><span class="sxs-lookup"><span data-stu-id="76a4f-158">The following table provides the disposition actions and their definitions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="76a4f-159">Käsittelytoiminto</span><span class="sxs-lookup"><span data-stu-id="76a4f-159">Disposition action</span></span></p></th>
<th><p><span data-ttu-id="76a4f-160">kuvaus</span><span class="sxs-lookup"><span data-stu-id="76a4f-160">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="76a4f-161"><strong>Kredit</strong></span><span class="sxs-lookup"><span data-stu-id="76a4f-161"><strong>Credit</strong></span></span></p></td>
<td><p><span data-ttu-id="76a4f-162">Palauta nimike varastoon ja hyvitä asiakasta.</span><span class="sxs-lookup"><span data-stu-id="76a4f-162">Return the item to inventory and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76a4f-163"><strong>Vain hyvitys</strong></span><span class="sxs-lookup"><span data-stu-id="76a4f-163"><strong>Credit only</strong></span></span></p></td>
<td><p><span data-ttu-id="76a4f-164">Palauta hyvitys asiakkaalle ilman vaatimusta tai oletusta nimikkeen palauttamisesta.</span><span class="sxs-lookup"><span data-stu-id="76a4f-164">Credit the customer without requiring or expecting the item to be returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76a4f-165"><strong>Hävikki</strong></span><span class="sxs-lookup"><span data-stu-id="76a4f-165"><strong>Scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="76a4f-166">Hävitä nimike ja hyvitä asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="76a4f-166">Scrap the item and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76a4f-167"><strong>Korvaus ja hyvitys</strong></span><span class="sxs-lookup"><span data-stu-id="76a4f-167"><strong>Replace and credit</strong></span></span></p></td>
<td><p><span data-ttu-id="76a4f-168">Palauta nimike varastoon, luo korvaava tilaus ja hyvitä asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="76a4f-168">Return the item to inventory, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76a4f-169"><strong>Korvaus ja hävitys</strong></span><span class="sxs-lookup"><span data-stu-id="76a4f-169"><strong>Replace and scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="76a4f-170">Hävitä nimike, luo korvaava tilaus ja hyvitä asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="76a4f-170">Scrap the item, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76a4f-171"><strong>Palautus asiakkaalle</strong></span><span class="sxs-lookup"><span data-stu-id="76a4f-171"><strong>Return to customer</strong></span></span></p></td>
<td><p><span data-ttu-id="76a4f-172">Hylkää palautettu nimike ja palauta se asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="76a4f-172">Reject the returned item and return it to the customer.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="select-a-disposition-code-for-a-quarantine-order"></a><span data-ttu-id="76a4f-173">Karanteenitilauksen käsittelykoodin valitseminen</span><span class="sxs-lookup"><span data-stu-id="76a4f-173">Select a disposition code for a quarantine order</span></span>

1.  <span data-ttu-id="76a4f-174">Valitse **Varastonhallinta** \> **Kausittainen** \> **Laadunhallinta** \> **Karanteenitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="76a4f-174">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="76a4f-175">Jos kyseessä on aiemmin luotu karanteenitilaus, valitse **Käsittelykoodi**-kenttä **Yleiskatsaus**-välilehdestä.</span><span class="sxs-lookup"><span data-stu-id="76a4f-175">For an existing quarantine order, select an action from the **Disposition code** field on the **Overview** tab.</span></span>



## <a name="see-also"></a><span data-ttu-id="76a4f-176">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="76a4f-176">See also</span></span>

<span data-ttu-id="76a4f-177">[Karanteenitilaus (lomake)](https://technet.microsoft.com/en-us/library/aa554073(v=ax.60))</span><span class="sxs-lookup"><span data-stu-id="76a4f-177">[Quarantine order (form)](https://technet.microsoft.com/en-us/library/aa554073(v=ax.60))</span></span>

<span data-ttu-id="76a4f-178">[Käsittelykoodit (lomake)](https://technet.microsoft.com/en-us/library/hh597113\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="76a4f-178">[Disposition codes (form)](https://technet.microsoft.com/en-us/library/hh597113\(v=ax.60\))</span></span>

  


