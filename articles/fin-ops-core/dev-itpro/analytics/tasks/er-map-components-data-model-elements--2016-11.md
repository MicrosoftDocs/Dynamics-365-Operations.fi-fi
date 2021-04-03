---
title: ER Luodun muodon osien yhdistäminen tietomallielementteihin (marraskuu 2016)
description: Tässä aiheessa käsitellään tietomallin elementtien yhdistämistä luodun sähköisen raportoinnin (ER) määrityksen osiin.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e3d6bcf229f9020ff4dd0479e486f465ffd6383
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570837"
---
# <a name="er-map-components-of-the-created-format-to-data-model-elements-november-2016"></a><span data-ttu-id="df6ba-103">ER Luodun muodon osien yhdistäminen tietomallielementteihin (marraskuu 2016)</span><span class="sxs-lookup"><span data-stu-id="df6ba-103">ER Map components of the created format to data model elements (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="df6ba-104">Seuraavassa menettelyssä selitetään, miten käyttäjä, jolla on joko järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi yhdistää tietomallielementtejä sellaisen luodun sähköisen raportoinnin (ER) -konfiguraation osiin, joka määrittää maksujen liiketoimintatoimialueen sähköisen asiakirjamuodon.</span><span class="sxs-lookup"><span data-stu-id="df6ba-104">The following procedure shows how a user in either the System administrator or Electronic reporting developer role can map data model elements to components of the created Electronic reporting (ER) configuration, which defines an electronic document format for the payments business domain.</span></span> <span data-ttu-id="df6ba-105">Tällä muodolla luodaan myöhemmin sähköisiä asiakirjoja maksujen käsittelyä varten.</span><span class="sxs-lookup"><span data-stu-id="df6ba-105">This format will be used later to generate electronic documents for processing payments.</span></span> <span data-ttu-id="df6ba-106">Tässä esimerkissä luodaan muotokonfiguraatio malliyritykselle Litware Inc.</span><span class="sxs-lookup"><span data-stu-id="df6ba-106">In this example, you will create a format configuration for the sample company, 'Litware, Inc.'.</span></span> <span data-ttu-id="df6ba-107">Nämä vaiheet voidaan suorittaa mille tahansa yritykselle, koska kaikki yritykset jakavat ER-konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="df6ba-107">These steps can be performed in any company as ER configurations are shared for all companies.</span></span> <span data-ttu-id="df6ba-108">Voit suorittaa nämä vaiheet, jos Uuden muotokonfiguraation luominen- tehtäväoppaan vaiheet on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="df6ba-108">To complete these steps, you must first complete the steps in the "Create a format configuration" task guide.</span></span>


## <a name="select-a-format-configuration"></a><span data-ttu-id="df6ba-109">Muotokonfiguraation valitseminen</span><span class="sxs-lookup"><span data-stu-id="df6ba-109">Select a format configuration</span></span>
1. <span data-ttu-id="df6ba-110">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="df6ba-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="df6ba-111">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="df6ba-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="df6ba-112">Laajenna puussa solmu Payments (simplified model).</span><span class="sxs-lookup"><span data-stu-id="df6ba-112">In the tree, expand 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="df6ba-113">Valitse puussa solmu Payments (simplified model)\BACS (UK fictitious).</span><span class="sxs-lookup"><span data-stu-id="df6ba-113">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
5. <span data-ttu-id="df6ba-114">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="df6ba-114">Click Designer.</span></span>

## <a name="map-format-components-to-data-model-elements"></a><span data-ttu-id="df6ba-115">Muotokomponenttien yhdistäminen tietomallielementteihin</span><span class="sxs-lookup"><span data-stu-id="df6ba-115">Map format components to data model elements</span></span>
1. <span data-ttu-id="df6ba-116">Valitse Laajenna tai tiivistä.</span><span class="sxs-lookup"><span data-stu-id="df6ba-116">Click Expand/collapse.</span></span>
2. <span data-ttu-id="df6ba-117">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="df6ba-117">Click the Mapping tab.</span></span>
3. <span data-ttu-id="df6ba-118">Laajenna puussa solmu model.</span><span class="sxs-lookup"><span data-stu-id="df6ba-118">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="df6ba-119">Valitse puussa Xml\Sanoma\ProcessingDate\DateTime.</span><span class="sxs-lookup"><span data-stu-id="df6ba-119">In the tree, select 'Xml\Message\ProcessingDate\DateTime'.</span></span>
5. <span data-ttu-id="df6ba-120">Valitse puussa malli\ProcessingDateTime.</span><span class="sxs-lookup"><span data-stu-id="df6ba-120">In the tree, select 'model\ProcessingDateTime'.</span></span>
6. <span data-ttu-id="df6ba-121">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="df6ba-121">Click Bind.</span></span>
7. <span data-ttu-id="df6ba-122">Valitse puussa Xml\Sanoma\MessageId\Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="df6ba-122">In the tree, select 'Xml\Message\MessageId\String'.</span></span>
8. <span data-ttu-id="df6ba-123">Valitse puussa malli\MessageIdentification.</span><span class="sxs-lookup"><span data-stu-id="df6ba-123">In the tree, select 'model\MessageIdentification'.</span></span>
9. <span data-ttu-id="df6ba-124">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="df6ba-124">Click Bind.</span></span>
10. <span data-ttu-id="df6ba-125">Laajenna puussa solmu model\Payments.</span><span class="sxs-lookup"><span data-stu-id="df6ba-125">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="df6ba-126">Valitse puussa Xml\Sanoma\Maksut\Nimike\Summa\Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="df6ba-126">In the tree, select 'Xml\Message\Payments\Item\Amount\String'.</span></span>
12. <span data-ttu-id="df6ba-127">Valitse puussa malli\Maksut\InstructedAmount.</span><span class="sxs-lookup"><span data-stu-id="df6ba-127">In the tree, select 'model\Payments\InstructedAmount'.</span></span>
13. <span data-ttu-id="df6ba-128">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="df6ba-128">Click Bind.</span></span>
14. <span data-ttu-id="df6ba-129">Valitse puussa Xml\Sanoma\Maksut\Nimike\TransDate\DateTime.</span><span class="sxs-lookup"><span data-stu-id="df6ba-129">In the tree, select 'Xml\Message\Payments\Item\TransDate\DateTime'.</span></span>
15. <span data-ttu-id="df6ba-130">Valitse puussa malli\Maksut\TransactionDate.</span><span class="sxs-lookup"><span data-stu-id="df6ba-130">In the tree, select 'model\Payments\TransactionDate'.</span></span>
16. <span data-ttu-id="df6ba-131">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="df6ba-131">Click Bind.</span></span>
17. <span data-ttu-id="df6ba-132">Valitse puussa Xml\Sanoma\Maksut\Nimike\Kuvaus\Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="df6ba-132">In the tree, select 'Xml\Message\Payments\Item\Description\String'.</span></span>
18. <span data-ttu-id="df6ba-133">Valitse puussa solmu model\Payments\Description.</span><span class="sxs-lookup"><span data-stu-id="df6ba-133">In the tree, select 'model\Payments\Description'.</span></span>
19. <span data-ttu-id="df6ba-134">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="df6ba-134">Click Bind.</span></span>
20. <span data-ttu-id="df6ba-135">Valitse puussa Xml\Sanoma\Maksut\Nimike\Valuutta\Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="df6ba-135">In the tree, select 'Xml\Message\Payments\Item\Currency\String'.</span></span>
21. <span data-ttu-id="df6ba-136">Valitse puussa solmu Malli\Maksut\Kuvaus.</span><span class="sxs-lookup"><span data-stu-id="df6ba-136">In the tree, select 'model\Payments\Currency'.</span></span>
22. <span data-ttu-id="df6ba-137">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="df6ba-137">Click Bind.</span></span>
23. <span data-ttu-id="df6ba-138">Valitse puussa Xml\Sanoma\Maksut\Nimike\Tunnus.</span><span class="sxs-lookup"><span data-stu-id="df6ba-138">In the tree, select 'Xml\Message\Payments\Item\Id'.</span></span>
24. <span data-ttu-id="df6ba-139">Valitse puussa malli\Maksut\End2EndID'.</span><span class="sxs-lookup"><span data-stu-id="df6ba-139">In the tree, select 'model\Payments\End2EndID'.</span></span>
25. <span data-ttu-id="df6ba-140">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="df6ba-140">Click Bind.</span></span>
26. <span data-ttu-id="df6ba-141">Laajenna puussa solmu model\Payments\Creditor.</span><span class="sxs-lookup"><span data-stu-id="df6ba-141">In the tree, expand 'model\Payments\Creditor'.</span></span>
27. <span data-ttu-id="df6ba-142">Laajenna puussa solmu model\Payments\Creditor\Account.</span><span class="sxs-lookup"><span data-stu-id="df6ba-142">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
28. <span data-ttu-id="df6ba-143">Laajenna puussa solmu expand 'model\Payments\Creditor\Agent.</span><span class="sxs-lookup"><span data-stu-id="df6ba-143">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
29. <span data-ttu-id="df6ba-144">Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja\Nimi\Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="df6ba-144">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
30. <span data-ttu-id="df6ba-145">Valitse puussa solmu model\Payments\Creditor\Name.</span><span class="sxs-lookup"><span data-stu-id="df6ba-145">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
31. <span data-ttu-id="df6ba-146">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="df6ba-146">Click Bind.</span></span>
32. <span data-ttu-id="df6ba-147">Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja\Pankki\RoutingNumber\String.</span><span class="sxs-lookup"><span data-stu-id="df6ba-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber\String'.</span></span>
33. <span data-ttu-id="df6ba-148">Valitse puussa malli\Maksut\Laskuttaja\Edustaja\RoutingNumber.</span><span class="sxs-lookup"><span data-stu-id="df6ba-148">In the tree, select 'model\Payments\Creditor\Agent\RoutingNumber'.</span></span>
34. <span data-ttu-id="df6ba-149">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="df6ba-149">Click Bind.</span></span>
35. <span data-ttu-id="df6ba-150">Valitse puussa Xml\Sanoma\Maksut\Nimike\Toimittaja\Pankki\AccountNumber\Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="df6ba-150">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber\String'.</span></span>
36. <span data-ttu-id="df6ba-151">Valitse puussa solmu model\Payments\Creditor\Account\Number.</span><span class="sxs-lookup"><span data-stu-id="df6ba-151">In the tree, select 'model\Payments\Creditor\Account\Number'.</span></span>
37. <span data-ttu-id="df6ba-152">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="df6ba-152">Click Bind.</span></span>
38. <span data-ttu-id="df6ba-153">Valitse puussa Xml\Sanoma\Maksut\Nimike\Maksaja\Nimi\Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="df6ba-153">In the tree, select 'Xml\Message\Payments\Item\Payer\Name\String'.</span></span>
39. <span data-ttu-id="df6ba-154">Laajenna puussa solmu model\Payments\Debtor.</span><span class="sxs-lookup"><span data-stu-id="df6ba-154">In the tree, expand 'model\Payments\Debtor'.</span></span>
40. <span data-ttu-id="df6ba-155">Laajenna puussa solmu model\Payments\Debtor\Account.</span><span class="sxs-lookup"><span data-stu-id="df6ba-155">In the tree, expand 'model\Payments\Debtor\Account'.</span></span>
41. <span data-ttu-id="df6ba-156">Laajenna puussa solmu model\Payments\Debtor\Agent.</span><span class="sxs-lookup"><span data-stu-id="df6ba-156">In the tree, expand 'model\Payments\Debtor\Agent'.</span></span>
42. <span data-ttu-id="df6ba-157">Valitse puussa solmu model\Payments\Debtor\Name.</span><span class="sxs-lookup"><span data-stu-id="df6ba-157">In the tree, select 'model\Payments\Debtor\Name'.</span></span>
43. <span data-ttu-id="df6ba-158">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="df6ba-158">Click Bind.</span></span>
44. <span data-ttu-id="df6ba-159">Valitse puussa Xml\Sanoma\Maksut\Nimike\Maksaja\Pankki\RoutingNumber\Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="df6ba-159">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber\String'.</span></span>
45. <span data-ttu-id="df6ba-160">Valitse puussa malli\Maksut\Maksaja\Edustaja\RoutingNumber.</span><span class="sxs-lookup"><span data-stu-id="df6ba-160">In the tree, select 'model\Payments\Debtor\Agent\RoutingNumber'.</span></span>
46. <span data-ttu-id="df6ba-161">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="df6ba-161">Click Bind.</span></span>
47. <span data-ttu-id="df6ba-162">Valitse puussa Xml\Sanoma\Maksut\Nimike\Maksaja\Pankki\AccountNumber\Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="df6ba-162">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber\String'.</span></span>
48. <span data-ttu-id="df6ba-163">Valitse puussa solmu model\Payments\Debtor\Account\Number.</span><span class="sxs-lookup"><span data-stu-id="df6ba-163">In the tree, select 'model\Payments\Debtor\Account\Number'.</span></span>
49. <span data-ttu-id="df6ba-164">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="df6ba-164">Click Bind.</span></span>
50. <span data-ttu-id="df6ba-165">Valitse puussa Xml\Sanoma\Maksut\Nimike.</span><span class="sxs-lookup"><span data-stu-id="df6ba-165">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="df6ba-166">Laajenna puussa solmu model\Payments.</span><span class="sxs-lookup"><span data-stu-id="df6ba-166">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="df6ba-167">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="df6ba-167">Click Bind.</span></span>
53. <span data-ttu-id="df6ba-168">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="df6ba-168">Click Save.</span></span>

## <a name="validate-format-mapping"></a><span data-ttu-id="df6ba-169">Muotoyhdistämismäärityksen tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="df6ba-169">Validate format mapping</span></span>
1. <span data-ttu-id="df6ba-170">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="df6ba-170">Click Validate.</span></span>
    * <span data-ttu-id="df6ba-171">Varmista, että kaikki sidokset ovat kunnossa tarkistamalla uudet yhdistämismääritykset.</span><span class="sxs-lookup"><span data-stu-id="df6ba-171">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="df6ba-172">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="df6ba-172">Close the page.</span></span>

## <a name="change-status-of-the-current-version-of-format-configuration"></a><span data-ttu-id="df6ba-173">Muotokonfiguraation nykyisen version tilan muuttaminen</span><span class="sxs-lookup"><span data-stu-id="df6ba-173">Change status of the current version of format configuration</span></span>
<span data-ttu-id="df6ba-174">Seuraavissa vaiheissa muutetaan muotokonfiguraation tila Luonnos-tilasta Valmis-tilaksi. Tällöin sitä voi käyttää maksuasiakirjojen luontiin.</span><span class="sxs-lookup"><span data-stu-id="df6ba-174">In the next steps, you'll change the status of the format configuration from Draft to Completed to make it available for payment document generation.</span></span>  
1. <span data-ttu-id="df6ba-175">Voit muuttaa tilaa valitsemalla Muuta.</span><span class="sxs-lookup"><span data-stu-id="df6ba-175">Click Change status.</span></span>
2. <span data-ttu-id="df6ba-176">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="df6ba-176">Click Complete.</span></span>
3. <span data-ttu-id="df6ba-177">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="df6ba-177">In the Description field, type a value.</span></span>
    * <span data-ttu-id="df6ba-178">Esimerkki: versio 1.</span><span class="sxs-lookup"><span data-stu-id="df6ba-178">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="df6ba-179">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="df6ba-179">Click OK.</span></span>
5. <span data-ttu-id="df6ba-180">Valitse nykyisen konfiguraation valmis versio.</span><span class="sxs-lookup"><span data-stu-id="df6ba-180">Select completed version of the current configuration.</span></span>
    * <span data-ttu-id="df6ba-181">Huomaa, että konfiguraatio tallennetaan suoritettuna versiona 1.1: tietomallin versioon 1 perustuva muodon versio 1.</span><span class="sxs-lookup"><span data-stu-id="df6ba-181">Note that the configuration is saved as completed version 1.1: version 1 of the format based on the version 1 of the data model.</span></span>  

## <a name="define-effective-date-for-completed-version-of-format"></a><span data-ttu-id="df6ba-182">Muodon valmiin version voimaantulopäivämäärän määrittäminen</span><span class="sxs-lookup"><span data-stu-id="df6ba-182">Define effective date for completed version of format</span></span>
<span data-ttu-id="df6ba-183">Jokainen muotoversio voidaan määrittää käytettäväksi tietystä päivämäärästä alkaen.</span><span class="sxs-lookup"><span data-stu-id="df6ba-183">Each format version can be configured as available for usage starting from a certain date.</span></span> <span data-ttu-id="df6ba-184">Kun tiettynä päivänä on useita aktiivisia muotoversioita, käyttöön valitaan uusin muoto (versionumeron perusteella).</span><span class="sxs-lookup"><span data-stu-id="df6ba-184">When more than one format version is active on a certain date, the latest format (based on version number) will be selected for usage.</span></span> <span data-ttu-id="df6ba-185">Oikean version valinnassa käytetään istunnon päivämääräarvoa.</span><span class="sxs-lookup"><span data-stu-id="df6ba-185">The session date value is used for proper version selection.</span></span>  

## <a name="restrict-access-to-created-format-from-companies"></a><span data-ttu-id="df6ba-186">Luodun muodon käytön rajoittaminen yrityksiltä</span><span class="sxs-lookup"><span data-stu-id="df6ba-186">Restrict access to created format from companies</span></span>
1. <span data-ttu-id="df6ba-187">Laajenna ISO maa-/aluekoodit -osa.</span><span class="sxs-lookup"><span data-stu-id="df6ba-187">Expand the ISO Country/region codes section.</span></span>
    * <span data-ttu-id="df6ba-188">Kunkin muodon käyttöoikeutta voidaan rajoittaa määrittämällä maat/alueet, joissa muoto on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="df6ba-188">Each format access can be restricted by identifying particular countries/regions in which a format is applicable.</span></span> <span data-ttu-id="df6ba-189">Kun tietyn muodon maiden ja alueiden luettelo on tyhjä, muotoa voi käyttää missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="df6ba-189">When the list of countries/regions for particular format is empty, this format can be used in any company.</span></span> <span data-ttu-id="df6ba-190">Kun ISO-maa- ja -aluekoodeja lisätään maiden ja alueiden luetteloon, muotoa voi käyttää yrityksissä vain, jos niiden ensisijainen osoite on kyseisessä maassa tai kyseisellä alueella.</span><span class="sxs-lookup"><span data-stu-id="df6ba-190">When some ISO country/region codes are inserted in the list of countries/regions, the format can only be use in companies if the primary address is in the country/region.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]