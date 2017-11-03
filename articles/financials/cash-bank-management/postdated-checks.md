---
title: "Myöhemmäksi päivätyt sekit"
description: "Tässä artikkelissa on tietoja myöhemmäksi päivättyjen sekkien tuesta Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionissa. Myöhemmäksi päivätyt sekit ovat sekkejä, jotka on asetettu tulevan päivämäärän omaavien maksujen vastaanottamista varten. Tämän vuoksi sekkiä ei voi lunastaa ennen määritettyä päivämäärää."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: afa181830fb822c85dedbc8009fec903d1b98479
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="postdated-checks"></a><span data-ttu-id="d1094-105">Myöhemmäksi päivätyt sekit</span><span class="sxs-lookup"><span data-stu-id="d1094-105">Postdated checks</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d1094-106">Tässä artikkelissa on tietoja myöhemmäksi päivättyjen sekkien tuesta Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionissa.</span><span class="sxs-lookup"><span data-stu-id="d1094-106">This article provides information about support for postdated checks in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="d1094-107">Myöhemmäksi päivätyt sekit ovat sekkejä, jotka on asetettu tulevan päivämäärän omaavien maksujen vastaanottamista varten.</span><span class="sxs-lookup"><span data-stu-id="d1094-107">Postdated checks are checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="d1094-108">Tämän vuoksi sekkiä ei voi lunastaa ennen määritettyä päivämäärää.</span><span class="sxs-lookup"><span data-stu-id="d1094-108">Therefore, the check can't be cashed until the specified date.</span></span>

<span data-ttu-id="d1094-109">Microsoft Dynamics 365 for Finance and Operations tukee myöhemmäksi päivättyjen sekkien koko hallintasykliä sekä myyntireskontrassa että ostoreskontrassa seuraavassa taulukossa esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="d1094-109">Microsoft Dynamics 365 for Finance and Operations supports the full management cycle for postdated checks in both Accounts receivable and Accounts payable, as shown in the following table.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d1094-110">Skenaario</span><span class="sxs-lookup"><span data-stu-id="d1094-110">Scenario</span></span></th>
<th><span data-ttu-id="d1094-111">Erittely</span><span class="sxs-lookup"><span data-stu-id="d1094-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d1094-112">Aseta jälkeen päin päivitetyt laskut</span><span class="sxs-lookup"><span data-stu-id="d1094-112">Set up postdated checks</span></span></td>
<td><span data-ttu-id="d1094-113">Määritä uusi maksutapa ja maksurutiini lähetettyjen ja vastaanotettujen sekkien sekä ennakonpidätyksen selvitystileille.</span><span class="sxs-lookup"><span data-stu-id="d1094-113">You must set up a new payment method, and specify the payment routine for clearing accounts for issued checks, received checks, and withholding tax.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d1094-114">Kirjaa ja lähetä toimittajalle jälkeen päin päivitetty lasku</span><span class="sxs-lookup"><span data-stu-id="d1094-114">Register and post a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="d1094-115">Rekisteröi toimittajalle kirjoittamasi myöhemmäksi päivätyn sekin tiedot.</span><span class="sxs-lookup"><span data-stu-id="d1094-115">Register the details of a postdated check that you issue to a vendor.</span></span> <span data-ttu-id="d1094-116">Kun maksu kirjataan, toimittajan velka siirretään, mutta pankkitiliä ei vielä hyvitetä.</span><span class="sxs-lookup"><span data-stu-id="d1094-116">When the payment is posted, the vendor liability is recognized, but the bank account isn’t yet credit.</span></span> <span data-ttu-id="d1094-117">Sen sijaan käytetään selvitystiliä.</span><span class="sxs-lookup"><span data-stu-id="d1094-117">Instead, a clearing account is used for this purpose.</span></span> </td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d1094-118">Rekisteröi ja kirjaa asiakkaan myöhemmäksi päivitetty sekki</span><span class="sxs-lookup"><span data-stu-id="d1094-118">Register and post a postdated check for a customer</span></span></td>
<td><span data-ttu-id="d1094-119">Rekisteröi asiakkaalta saadun myöhemmäksi päivätyn sekin tiedot.</span><span class="sxs-lookup"><span data-stu-id="d1094-119">Register the details of a postdated check that you receive from a customer.</span></span> <span data-ttu-id="d1094-120">Kun maksu kirjataan, asiakkaan saatava on kredit, mutta pankkitiliä ei vielä veloiteta.</span><span class="sxs-lookup"><span data-stu-id="d1094-120">When the payment is posted, the customer receivable is credit, but the bank account isn’t yet debit.</span></span> <span data-ttu-id="d1094-121">Sen sijaan käytetään selvitystiliä.</span><span class="sxs-lookup"><span data-stu-id="d1094-121">Instead, a clearing account is used for this purpose.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d1094-122">Kirjaa ja lähetä asiakkaalle tai toimittajalle myöhäisemmäksi päivätty korvaava sekki</span><span class="sxs-lookup"><span data-stu-id="d1094-122">Register and post a replacement postdated check for a customer or a vendor</span></span></td>
<td>
<span data-ttu-id="d1094-123">Jos toimittajalle lähetetty tai asiakkaalta vastaanotettu alkuperäinen sekki on kadonnut tai vahingoittunut, voit asettaa korvaavan myöhemmäksi päivätyn sekin.</span><span class="sxs-lookup"><span data-stu-id="d1094-123">If your original check to a vendor or from a customer is lost or damaged, you can issue a replacement postdated check.</span></span> <span data-ttu-id="d1094-124">Kun rekisteröit sekin tiedot, määritä viittaus alkuperäiseen sekkiin ja osoita, että uusi sekki korvaa alkuperäisen sekin.</span><span class="sxs-lookup"><span data-stu-id="d1094-124">When you register the check details, provide a reference to the original check, and indicate that the new check is a replacement for the original.</span></span> <span data-ttu-id="d1094-125">Voit myös kirjata korvaavan sekin.</span><span class="sxs-lookup"><span data-stu-id="d1094-125">You can also post the replacement check.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d1094-126">Asiakkaan myöhemmäksi päivätyn sekin siirtäminen toimittajalle</span><span class="sxs-lookup"><span data-stu-id="d1094-126">Transfer a customer postdated check to a vendor</span></span></td>
<td><span data-ttu-id="d1094-127">Kun vastaanotat asiakkaalta myöhemmäksi päivätyn sekin, voit siirtää kyseisen sekin toimittajalle maksuna.</span><span class="sxs-lookup"><span data-stu-id="d1094-127">When you receive a postdated check from a customer, you can transfer that check to a vendor as a payment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d1094-128">Sovi jälkeen päin päivitetty lasku asiakkaalle tai toimittajalle</span><span class="sxs-lookup"><span data-stu-id="d1094-128">Settle a postdated check for a customer or a vendor</span></span></td>
<td><span data-ttu-id="d1094-129">Tilitä asiakkaan tai toimittajan välitilille kirjattu myöhemmäksi päivätty sekki sitten, kun sekki lopulta erääntyy.</span><span class="sxs-lookup"><span data-stu-id="d1094-129">Settle a postdated check that is posted to a bridging account for a customer or a vendor when the check finally matures.</span></span> <span data-ttu-id="d1094-130">Kun sekki on tilitetty, pankille määritetään veloitus tai hyvitys aiemmin käytetylle selvitystilille.</span><span class="sxs-lookup"><span data-stu-id="d1094-130">When the check is settled, the bank is finally debit or credit against the clearing account that was used earlier.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d1094-131">Peruuta toimittajalle osoitettu myöhemmäksi päivätty shekki</span><span class="sxs-lookup"><span data-stu-id="d1094-131">Cancel a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="d1094-132">Voit peruuttaa myöhemmäksi päivätyn sekin seuraavissa tilanteissa: - pankki palauttaa sekin</span><span class="sxs-lookup"><span data-stu-id="d1094-132">You can cancel a posted postdated check in these situations: - The check is returned by the bank.</span></span>
<span data-ttu-id="d1094-133">- sekki on kohdistettu väärään laskuun</span><span class="sxs-lookup"><span data-stu-id="d1094-133">- The check is applied to an incorrect invoice.</span></span>
<span data-ttu-id="d1094-134">- sekkiä vastaan on tehty käteismaksu.</span><span class="sxs-lookup"><span data-stu-id="d1094-134">- A cash payment is made against the check.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="d1094-135">Myöhemmäksi päivätyn sekkimaksun lopetus</span><span class="sxs-lookup"><span data-stu-id="d1094-135">Stop payment for a postdated check</span></span></td>
<td><span data-ttu-id="d1094-136">Voit lopettaa toimittajalle myönnetyn myöhemmäksi päivätyn sekkimaksun esimerkiksi seuraavista syistä: varat eivät riitä, sopimusehtojen toimittajan kanssa muuttuvat, toimittaja on toimittanut viallisia tavaroita tai tavaroita palautetaan toimittajalle.</span><span class="sxs-lookup"><span data-stu-id="d1094-136">You can stop payment on a postdated check that was issued to a vendor, for reasons such as not sufficient funds, changes in the terms of the agreement with the vendor, supply of defective goods by the vendor, or return of goods to the vendor.</span></span> <span data-ttu-id="d1094-137">Voit lopettaa maksun vain niiden sekkien osalta, joita ei ole lunastettu.</span><span class="sxs-lookup"><span data-stu-id="d1094-137">You can stop payment only on checks that haven’t cleared.</span></span></td>
</tr>
</tbody>
</table>



<span data-ttu-id="d1094-138">Lisätietoja on seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="d1094-138">For more information, see the following topics:</span></span>

[<span data-ttu-id="d1094-139">Määritä jälkeen päin päivitetyt sekit</span><span class="sxs-lookup"><span data-stu-id="d1094-139">Set up postdated checks</span></span>](tasks/set-up-postdated-checks.md)

[<span data-ttu-id="d1094-140">Rekisteröi ja kirjaa asiakkaan myöhemmäksi päivitetty sekki</span><span class="sxs-lookup"><span data-stu-id="d1094-140">Register and post a postdated check for a customer</span></span>](tasks/register-post-postdated-check-customer.md)

[<span data-ttu-id="d1094-141">Tilitä asiakkaalta jälkeen päin päivitetty lasku</span><span class="sxs-lookup"><span data-stu-id="d1094-141">Settle a postdated check from a customer</span></span>](tasks/settle-postdated-check-customer.md)

[<span data-ttu-id="d1094-142">Rekisteröi ja kirjaa toimittajan myöhemmäksi päivitetty sekki</span><span class="sxs-lookup"><span data-stu-id="d1094-142">Register and post a postdated check for a vendor</span></span>](tasks/register-post-postdated-check-vendor.md) 

[<span data-ttu-id="d1094-143">Tilitä toimittajalle jälkeen päin päivitetty lasku</span><span class="sxs-lookup"><span data-stu-id="d1094-143">Settle a postdated check for a vendor</span></span>](tasks/settle-postdated-check-vendor.md)




