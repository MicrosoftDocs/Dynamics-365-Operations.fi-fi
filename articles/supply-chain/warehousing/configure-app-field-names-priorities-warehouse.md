---
title: "Warehousing-sovelluksen kenttien nimien määrittäminen"
description: "Tässä ohjeaiheessa kerrotaan, miten varastosovelluksen kenttien nimet ja prioriteetit määritetään Finance and Operationsissa."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: bdfc651ea76ea0d35dd3fec43b44cdad177ed96d
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="configure-app-field-names-in-warehousing-app"></a><span data-ttu-id="1f8bf-103">Warehousing-sovelluksen kenttien nimien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1f8bf-103">Configure app field names in Warehousing app</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1f8bf-104">Tässä ohjeaiheessa kerrotaan, miten varastosovelluksen kenttien nimet ja prioriteetit määritetään Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-104">This topic describes how to define and configure warehouse app field names and priorities in Finance and Operations.</span></span> 

<span data-ttu-id="1f8bf-105">**Huomautus:** Tämä ohjeaihe koskee varastonhallintamoduulin ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-105">**Note:** This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="1f8bf-106">Se ei koske inventaariohallintamoduulin ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="1f8bf-107">Finance and Operations – varastointi on sovellus, jonka avulla voit suorittaa fyysisen varastoinnin tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-107">Finance and Operations - Warehousing is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="1f8bf-108">Voit määrittää ja konfiguroida kenttien nimet, joita käytetään sovelluksessa, sekä määrittää prioriteetin, johon kenttien nimet tulisi liittää.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="1f8bf-109">Tässä ohjeaiheessa kerrotaan, miten nämä varastosovelluksen kenttien nimet ja prioriteetit määritetään ja miten niitä käytetään Finance and Operationsin varastointisovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-109">This topic explains how to define and configure these warehouse app field names and priorities, and how they are used in Finance and Operations - Warehousing.</span></span> <span data-ttu-id="1f8bf-110">Lisätietoja yhteyden määrittämisestä Finance and Operationsin varastointisovellukseen on oppaassa [Finance and Operationsin varastointisovelluksen asennus ja määritys](install-configure-warehousing-app.md).</span><span class="sxs-lookup"><span data-stu-id="1f8bf-110">For detailed information about how to configure the connection to Finance and Operations  - Warehousing, refer to the tutorial [Install and configure Finance and Operations - Warehousing](install-configure-warehousing-app.md).</span></span>

<a name="configure-warehouse-app-field-names"></a><span data-ttu-id="1f8bf-111">Warehousing-sovelluksen kenttien nimien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1f8bf-111">Configure warehouse app field names</span></span>
===================================

<span data-ttu-id="1f8bf-112">Kun käytät Finance and Operationsin varastointisovellusta mobiililaitteessa, voit määrittää **Varastointisovelluksen kenttien nimet** -sivulla, miten metatiedot näytetään laitteessa.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-112">When you use Finance and Operations - Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="1f8bf-113">Luo kaikkien varastoinnin mobiililaitteen työnkulussa käytettävien kenttien nimet valitsemalla uudessa Finance and Operations -yrityksessä **Luo oletusasetukset**, ja määritä sitten niihin ensisijainen syötetila ja syötteen tyyppi.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-113">In a new company in Finance and Operations, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="1f8bf-114">Kun kaikkien kenttien nimet on luotu, voit valita syötteen seuraavista vaihtoehdoista.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-114">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1f8bf-115">Vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="1f8bf-115">Option</span></span></th>
<th><span data-ttu-id="1f8bf-116">kuvaus</span><span class="sxs-lookup"><span data-stu-id="1f8bf-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1f8bf-117">Ensisijainen syöttömenetelmä</span><span class="sxs-lookup"><span data-stu-id="1f8bf-117">Preferred input mode</span></span></td>
<td><span data-ttu-id="1f8bf-118">Tämä vaihtoehto määrittää, näytetäänkö skannauskenttä vai manuaalinen syöttökenttä valitulle kentän nimelle.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-118">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="1f8bf-119">Tämä on tarpeen sen erottamiseksi, jos viivakoodeja käytetään tälle kentälle.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-119">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="1f8bf-120"><strong>Huomautus:</strong> Niille kenttien nimille, joiden ensisijainen syöttötila on <strong>Skannaus</strong>, voit syöttää tiedot manuaalisesti jos viivakoodi on vioittunut tai lukukelvoton.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-120"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f8bf-121">Syötetyyppi</span><span class="sxs-lookup"><span data-stu-id="1f8bf-121">Input type</span></span></td>
<td><span data-ttu-id="1f8bf-122">Tämä vaihtoehto määrittää, mitä syötetilaa pitäisi käyttää valitulle kentän nimelle.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-122">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="1f8bf-123">Käytettävissä on neljä asetusta:</span><span class="sxs-lookup"><span data-stu-id="1f8bf-123">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="1f8bf-124"><strong>Valinta</strong> - sisältää asetusluettelon, josta voi valita.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-124"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="1f8bf-125">Tässä vaihtoehdossa kenttien nimiä ei voi muokata.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-125">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="1f8bf-126"><strong>Päivämäärä</strong> - kenttien nimet, jotka on määritetty päivämääriksi, näyttävät päivämäärämuodon otsikon yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-126"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="1f8bf-127">Näin varastotyöntekijät näkevät, missä muodossa kirjoittaa päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-127">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="1f8bf-128">Tässä vaihtoehdossa kenttien nimiä ei voi muokata.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-128">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="1f8bf-129"><strong>Alpha</strong> - jos tämä valitaan, laitteen näppäimistöä käytetään syötettäessä tietoja manuaalisesti sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-129"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="1f8bf-130">Näppäimistön käyttöä voidaan muuttaa sen mukaan, mitä laitetta käytetään.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-130">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="1f8bf-131"><strong>Numeerinen</strong> - kentän nimille, jotka käyttävät vain numeroita, voit valita tämän vaihtoehdon näyttääksesi mukautetun numeronäppäimistön syöttökentän yhteydessä laitteen näppäimistön sijaan.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-131"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="1f8bf-132">Warehousing-sovelluksen kenttäprioriteetin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1f8bf-132">Configure warehouse app field priority</span></span>
======================================

<span data-ttu-id="1f8bf-133">**Varastosovelluksen kenttäprioriteetti** -sivulla voit määrittää kenttänimet eri prioriteettiryhmiin.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-133">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="1f8bf-134">Näin voit päättää, mitä tietoja näytetään sivulla päätehtäväsivulla silloin, kun fyysisen varastoinnin työntekijät suorittavat tehtäviä sovelluksen avulla.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-134">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="1f8bf-135">Jos valitset **Luo oletusasetukset**, järjestelmä luo oletusarvoiset prioriteettiryhmät.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-135">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="1f8bf-136">On mahdollista luoda niin monta prioriteettiryhmiä kuin on tarpeen, mutta tehtäväsivulla näytetään vain kolme prioriteettiryhmää.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-136">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="1f8bf-137">Kun Finance and Operations lähettää metatietoja sovellukseen, se määrittää kunkin kentän suhteellisen prioriteetin sen prioriteettiryhmän mukaan, ja sovellus näyttää ensimmäiset kolme metatietojen sisältämää prioriteettiryhmää.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-137">When Finance and Operations sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="1f8bf-138">Loput metatiedot näytetään toissijaisten tietojen sivulla.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-138">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="1f8bf-139">Seuraavassa taulukossa on esimerkit viidestä prioriteettiryhmästä.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-139">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1f8bf-140">Prioriteettiryhmä</span><span class="sxs-lookup"><span data-stu-id="1f8bf-140">Priority group</span></span></th>
<th><span data-ttu-id="1f8bf-141">Määritetyt kentät</span><span class="sxs-lookup"><span data-stu-id="1f8bf-141">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="1f8bf-142">Prioriteetti 10</span><span class="sxs-lookup"><span data-stu-id="1f8bf-142">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="1f8bf-143">Nimike</span><span class="sxs-lookup"><span data-stu-id="1f8bf-143">Item</span></span></li>
<li><span data-ttu-id="1f8bf-144">Määrä</span><span class="sxs-lookup"><span data-stu-id="1f8bf-144">Quantity</span></span></li>
<li><span data-ttu-id="1f8bf-145">Mittayksikkö</span><span class="sxs-lookup"><span data-stu-id="1f8bf-145">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="1f8bf-146">Prioriteetti 20</span><span class="sxs-lookup"><span data-stu-id="1f8bf-146">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="1f8bf-147">Sijainti klusterissa</span><span class="sxs-lookup"><span data-stu-id="1f8bf-147">Cluster position</span></span></li>
<li><span data-ttu-id="1f8bf-148">Klusteri</span><span class="sxs-lookup"><span data-stu-id="1f8bf-148">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="1f8bf-149">Prioriteetti 30</span><span class="sxs-lookup"><span data-stu-id="1f8bf-149">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="1f8bf-150">Nimikkeen kuvaus</span><span class="sxs-lookup"><span data-stu-id="1f8bf-150">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="1f8bf-151">Prioriteetti 40</span><span class="sxs-lookup"><span data-stu-id="1f8bf-151">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="1f8bf-152">Konfiguraatio</span><span class="sxs-lookup"><span data-stu-id="1f8bf-152">Configuration</span></span></li>
<li><span data-ttu-id="1f8bf-153">Väri</span><span class="sxs-lookup"><span data-stu-id="1f8bf-153">Color</span></span></li>
<li><span data-ttu-id="1f8bf-154">Koko</span><span class="sxs-lookup"><span data-stu-id="1f8bf-154">Size</span></span></li>
<li><span data-ttu-id="1f8bf-155">Tyyli</span><span class="sxs-lookup"><span data-stu-id="1f8bf-155">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="1f8bf-156">Prioriteetti 50</span><span class="sxs-lookup"><span data-stu-id="1f8bf-156">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="1f8bf-157">Paikka</span><span class="sxs-lookup"><span data-stu-id="1f8bf-157">Location</span></span></li>
<li><span data-ttu-id="1f8bf-158">Rekisterikilpi</span><span class="sxs-lookup"><span data-stu-id="1f8bf-158">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1f8bf-159">Esimerkiksi kun varastotyöntekijä suorittaa tehtävän mobiililaitteella ja jos metatiedot, jotka näytetään sovelluksessa, koostuu seuraavista kentistä:</span><span class="sxs-lookup"><span data-stu-id="1f8bf-159">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="1f8bf-160">Nimike</span><span class="sxs-lookup"><span data-stu-id="1f8bf-160">Item</span></span>
-   <span data-ttu-id="1f8bf-161">Määrä</span><span class="sxs-lookup"><span data-stu-id="1f8bf-161">Quantity</span></span>
-   <span data-ttu-id="1f8bf-162">Mittayksikkö</span><span class="sxs-lookup"><span data-stu-id="1f8bf-162">Unit of measure</span></span>
-   <span data-ttu-id="1f8bf-163">Nimikkeen kuvaus</span><span class="sxs-lookup"><span data-stu-id="1f8bf-163">Item description</span></span>
-   <span data-ttu-id="1f8bf-164">Koko ja sijainti</span><span class="sxs-lookup"><span data-stu-id="1f8bf-164">Size and Location</span></span>

<span data-ttu-id="1f8bf-165">Yllä olevassa taulukossa määritettyjen varastosovelluksen kenttäprioriteettien perusteella seuraavat 3 tietoriviä näytetään tehtäväsivulla:</span><span class="sxs-lookup"><span data-stu-id="1f8bf-165">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="1f8bf-166">Rivi 1: Nimike, Määrä, Mittayksikkö</span><span class="sxs-lookup"><span data-stu-id="1f8bf-166">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="1f8bf-167">Rivi 2: Nimikkeen kuvaus</span><span class="sxs-lookup"><span data-stu-id="1f8bf-167">Row 2: Item description</span></span>
-   <span data-ttu-id="1f8bf-168">Rivi 3: koko</span><span class="sxs-lookup"><span data-stu-id="1f8bf-168">Row 3: Size</span></span>

<span data-ttu-id="1f8bf-169">Jäljellä olevat metatiedot, esimerkiksi sijainti, ei näy tehtäväsivulla, mutta kylläkin tietosivulla.</span><span class="sxs-lookup"><span data-stu-id="1f8bf-169">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="1f8bf-170">Lisätietoja ja esimerkkejä käyttöliittymästä saat blogikirjoituksesta [Finance and Operationsin varastointisovelluksen julkaisu](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="1f8bf-170">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="see-also"></a><span data-ttu-id="1f8bf-171">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="1f8bf-171">See also</span></span>
--------

[<span data-ttu-id="1f8bf-172">Microsoft Dynamics 365 for Finance and Operationsin varastointisovelluksen asentaminen ja määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1f8bf-172">Install and configure Microsoft Dynamics 365 for Finance and Operations – Warehousing</span></span>](install-configure-warehousing-app.md)




