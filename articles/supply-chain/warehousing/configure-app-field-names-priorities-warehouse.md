---
title: Varastosovelluksen kenttien nimien määrittäminen
description: Tässä ohjeaiheessa kerrotaan, miten varastosovelluksen kenttien nimet ja prioriteetit määritetään Dynamics 365 Supply Chain Managementissa.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 4c22a4314c36ba7112456ef264df500af98996f3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232956"
---
# <a name="configure-app-field-names-in-the-warehouse-app"></a><span data-ttu-id="e354d-103">Varastosovelluksen kenttien nimien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e354d-103">Configure app field names in the warehouse app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e354d-104">Tässä ohjeaiheessa kerrotaan, miten varastosovelluksen kenttien nimet ja prioriteetit määritetään Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="e354d-104">This topic describes how to define and configure warehouse app field names and priorities in Dynamics 365 Supply Chain Management.</span></span> 

> [!NOTE]
> <span data-ttu-id="e354d-105">Tämä ohjeaihe koskee varastonhallintamoduulin ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="e354d-105">This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="e354d-106">Se ei koske inventaariohallintamoduulin ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="e354d-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="e354d-107">Varastointi on sovellus, jonka avulla voit suorittaa fyysisen varastoinnin tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="e354d-107">Warehousing is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="e354d-108">Voit määrittää ja konfiguroida kenttien nimet, joita käytetään sovelluksessa, sekä määrittää prioriteetin, johon kenttien nimet tulisi liittää.</span><span class="sxs-lookup"><span data-stu-id="e354d-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="e354d-109">Tässä ohjeaiheessa kerrotaan, miten nämä varastosovelluksen kenttien nimet ja prioriteetit määritetään ja miten niitä käytetään varastointisovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="e354d-109">This topic explains how to define and configure these warehouse app field names and priorities, and how they are used in Warehousing.</span></span> <span data-ttu-id="e354d-110">Lisätietoja yhteyden määrittämisestä varastosovellukseen on oppaassa [Varastosovelluksen asennuksen ja määrityksen yleiskatsaus](install-configure-warehousing-app.md).</span><span class="sxs-lookup"><span data-stu-id="e354d-110">For detailed information about how to configure the connection to FWarehousing, refer to the tutorial [Install and configure the warehouse app overview](install-configure-warehousing-app.md).</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="e354d-111">Warehousing-sovelluksen kenttien nimien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e354d-111">Configure warehouse app field names</span></span>

<span data-ttu-id="e354d-112">Jos käytät varastointisovellusta mobiililaitteessa, voit määrittää **Varastointisovelluksen kenttien nimet** -sivulla, miten metatiedot näytetään laitteessa.</span><span class="sxs-lookup"><span data-stu-id="e354d-112">When you use Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="e354d-113">Luo kaikkien varastoinnin mobiililaitteen työnkulussa käytettävien kenttien nimet valitsemalla uudessa yrityksessä **Luo oletusasetukset**, ja määritä sitten niihin ensisijainen syötetila ja syötteen tyyppi.</span><span class="sxs-lookup"><span data-stu-id="e354d-113">In a new company, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="e354d-114">Kun kaikkien kenttien nimet on luotu, voit valita syötteen seuraavista vaihtoehdoista.</span><span class="sxs-lookup"><span data-stu-id="e354d-114">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e354d-115">Vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="e354d-115">Option</span></span></th>
<th><span data-ttu-id="e354d-116">kuvaus</span><span class="sxs-lookup"><span data-stu-id="e354d-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e354d-117">Ensisijainen syöttömenetelmä</span><span class="sxs-lookup"><span data-stu-id="e354d-117">Preferred input mode</span></span></td>
<td><span data-ttu-id="e354d-118">Tämä vaihtoehto määrittää, näytetäänkö skannauskenttä vai manuaalinen syöttökenttä valitulle kentän nimelle.</span><span class="sxs-lookup"><span data-stu-id="e354d-118">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="e354d-119">Tämä on tarpeen sen erottamiseksi, jos viivakoodeja käytetään tälle kentälle.</span><span class="sxs-lookup"><span data-stu-id="e354d-119">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="e354d-120"><strong>Huomautus:</strong> Niille kenttien nimille, joiden ensisijainen syöttötila on <strong>Skannaus</strong>, voit syöttää tiedot manuaalisesti jos viivakoodi on vioittunut tai lukukelvoton.</span><span class="sxs-lookup"><span data-stu-id="e354d-120"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e354d-121">Syötetyyppi</span><span class="sxs-lookup"><span data-stu-id="e354d-121">Input type</span></span></td>
<td><span data-ttu-id="e354d-122">Tämä vaihtoehto määrittää, mitä syötetilaa pitäisi käyttää valitulle kentän nimelle.</span><span class="sxs-lookup"><span data-stu-id="e354d-122">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="e354d-123">Käytettävissä on neljä asetusta:</span><span class="sxs-lookup"><span data-stu-id="e354d-123">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="e354d-124"><strong>Valinta</strong> - sisältää asetusluettelon, josta voi valita.</span><span class="sxs-lookup"><span data-stu-id="e354d-124"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="e354d-125">Tässä vaihtoehdossa kenttien nimiä ei voi muokata.</span><span class="sxs-lookup"><span data-stu-id="e354d-125">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="e354d-126"><strong>Päivämäärä</strong> - kenttien nimet, jotka on määritetty päivämääriksi, näyttävät päivämäärämuodon otsikon yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="e354d-126"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="e354d-127">Näin varastotyöntekijät näkevät, missä muodossa kirjoittaa päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="e354d-127">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="e354d-128">Tässä vaihtoehdossa kenttien nimiä ei voi muokata.</span><span class="sxs-lookup"><span data-stu-id="e354d-128">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="e354d-129"><strong>Alpha</strong> - jos tämä valitaan, laitteen näppäimistöä käytetään syötettäessä tietoja manuaalisesti sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="e354d-129"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="e354d-130">Näppäimistön käyttöä voidaan muuttaa sen mukaan, mitä laitetta käytetään.</span><span class="sxs-lookup"><span data-stu-id="e354d-130">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="e354d-131"><strong>Numeerinen</strong> - kentän nimille, jotka käyttävät vain numeroita, voit valita tämän vaihtoehdon näyttääksesi mukautetun numeronäppäimistön syöttökentän yhteydessä laitteen näppäimistön sijaan.</span><span class="sxs-lookup"><span data-stu-id="e354d-131"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="e354d-132">Warehousing-sovelluksen kenttäprioriteetin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e354d-132">Configure warehouse app field priority</span></span>

<span data-ttu-id="e354d-133">**Varastosovelluksen kenttäprioriteetti** -sivulla voit määrittää kenttänimet eri prioriteettiryhmiin.</span><span class="sxs-lookup"><span data-stu-id="e354d-133">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="e354d-134">Näin voit päättää, mitä tietoja näytetään sivulla päätehtäväsivulla silloin, kun fyysisen varastoinnin työntekijät suorittavat tehtäviä sovelluksen avulla.</span><span class="sxs-lookup"><span data-stu-id="e354d-134">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="e354d-135">Jos valitset **Luo oletusasetukset**, järjestelmä luo oletusarvoiset prioriteettiryhmät.</span><span class="sxs-lookup"><span data-stu-id="e354d-135">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="e354d-136">On mahdollista luoda niin monta prioriteettiryhmiä kuin on tarpeen, mutta tehtäväsivulla näytetään vain kolme prioriteettiryhmää.</span><span class="sxs-lookup"><span data-stu-id="e354d-136">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="e354d-137">Kun järjestelmä lähettää metatietoja sovellukseen, se määrittää kunkin kentän suhteellisen prioriteetin sen prioriteettiryhmän mukaan, ja sovellus näyttää ensimmäiset kolme metatietojen sisältämää prioriteettiryhmää.</span><span class="sxs-lookup"><span data-stu-id="e354d-137">When the system sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="e354d-138">Loput metatiedot näytetään toissijaisten tietojen sivulla.</span><span class="sxs-lookup"><span data-stu-id="e354d-138">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="e354d-139">Seuraavassa taulukossa on esimerkit viidestä prioriteettiryhmästä.</span><span class="sxs-lookup"><span data-stu-id="e354d-139">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e354d-140">Prioriteettiryhmä</span><span class="sxs-lookup"><span data-stu-id="e354d-140">Priority group</span></span></th>
<th><span data-ttu-id="e354d-141">Määritetyt kentät</span><span class="sxs-lookup"><span data-stu-id="e354d-141">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="e354d-142">Prioriteetti 10</span><span class="sxs-lookup"><span data-stu-id="e354d-142">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="e354d-143">Nimike</span><span class="sxs-lookup"><span data-stu-id="e354d-143">Item</span></span></li>
<li><span data-ttu-id="e354d-144">Määrä</span><span class="sxs-lookup"><span data-stu-id="e354d-144">Quantity</span></span></li>
<li><span data-ttu-id="e354d-145">Mittayksikkö</span><span class="sxs-lookup"><span data-stu-id="e354d-145">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="e354d-146">Prioriteetti 20</span><span class="sxs-lookup"><span data-stu-id="e354d-146">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="e354d-147">Sijainti klusterissa</span><span class="sxs-lookup"><span data-stu-id="e354d-147">Cluster position</span></span></li>
<li><span data-ttu-id="e354d-148">Klusteri</span><span class="sxs-lookup"><span data-stu-id="e354d-148">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="e354d-149">Prioriteetti 30</span><span class="sxs-lookup"><span data-stu-id="e354d-149">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="e354d-150">Nimikkeen kuvaus</span><span class="sxs-lookup"><span data-stu-id="e354d-150">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="e354d-151">Prioriteetti 40</span><span class="sxs-lookup"><span data-stu-id="e354d-151">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="e354d-152">Konfiguraatio</span><span class="sxs-lookup"><span data-stu-id="e354d-152">Configuration</span></span></li>
<li><span data-ttu-id="e354d-153">Väri</span><span class="sxs-lookup"><span data-stu-id="e354d-153">Color</span></span></li>
<li><span data-ttu-id="e354d-154">Koko</span><span class="sxs-lookup"><span data-stu-id="e354d-154">Size</span></span></li>
<li><span data-ttu-id="e354d-155">Tyyli</span><span class="sxs-lookup"><span data-stu-id="e354d-155">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="e354d-156">Prioriteetti 50</span><span class="sxs-lookup"><span data-stu-id="e354d-156">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="e354d-157">Paikka</span><span class="sxs-lookup"><span data-stu-id="e354d-157">Location</span></span></li>
<li><span data-ttu-id="e354d-158">Rekisterikilpi</span><span class="sxs-lookup"><span data-stu-id="e354d-158">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e354d-159">Esimerkiksi kun varastotyöntekijä suorittaa tehtävän mobiililaitteella ja jos metatiedot, jotka näytetään sovelluksessa, koostuu seuraavista kentistä:</span><span class="sxs-lookup"><span data-stu-id="e354d-159">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="e354d-160">Nimike</span><span class="sxs-lookup"><span data-stu-id="e354d-160">Item</span></span>
-   <span data-ttu-id="e354d-161">Määrä</span><span class="sxs-lookup"><span data-stu-id="e354d-161">Quantity</span></span>
-   <span data-ttu-id="e354d-162">Mittayksikkö</span><span class="sxs-lookup"><span data-stu-id="e354d-162">Unit of measure</span></span>
-   <span data-ttu-id="e354d-163">Nimikkeen kuvaus</span><span class="sxs-lookup"><span data-stu-id="e354d-163">Item description</span></span>
-   <span data-ttu-id="e354d-164">Koko ja sijainti</span><span class="sxs-lookup"><span data-stu-id="e354d-164">Size and Location</span></span>

<span data-ttu-id="e354d-165">Yllä olevassa taulukossa määritettyjen varastosovelluksen kenttäprioriteettien perusteella seuraavat 3 tietoriviä näytetään tehtäväsivulla:</span><span class="sxs-lookup"><span data-stu-id="e354d-165">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="e354d-166">Rivi 1: Nimike, Määrä, Mittayksikkö</span><span class="sxs-lookup"><span data-stu-id="e354d-166">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="e354d-167">Rivi 2: Nimikkeen kuvaus</span><span class="sxs-lookup"><span data-stu-id="e354d-167">Row 2: Item description</span></span>
-   <span data-ttu-id="e354d-168">Rivi 3: koko</span><span class="sxs-lookup"><span data-stu-id="e354d-168">Row 3: Size</span></span>

<span data-ttu-id="e354d-169">Jäljellä olevat metatiedot, esimerkiksi sijainti, ei näy tehtäväsivulla, mutta kylläkin tietosivulla.</span><span class="sxs-lookup"><span data-stu-id="e354d-169">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="e354d-170">Lisätietoja ja esimerkkejä käyttöliittymästä saat blogikirjoituksesta [Finance and Operationsin varastointisovelluksen julkaisu](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="e354d-170">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="additional-resources"></a><span data-ttu-id="e354d-171">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e354d-171">Additional resources</span></span>
--------

[<span data-ttu-id="e354d-172">Varastosovelluksen asentamisen ja määrittämisen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="e354d-172">Install and configure the warehouse app overview</span></span>](install-configure-warehousing-app.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]