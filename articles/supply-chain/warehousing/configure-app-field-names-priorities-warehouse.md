---
title: Varastonhallinnan mobiilisovelluksen kenttien konfigurointi
description: Tässä ohjeaiheessa kerrotaan, miten varastonhallinnan mobiilisovelluksessa näytettävien kenttien nimet ja prioriteetit määritetään.
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: bc224d3fd6cf5b111f61066202090f10ba4a7e8a
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189247"
---
# <a name="configure-fields-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="01f62-103">Varastonhallinnan mobiilisovelluksen kenttien konfigurointi</span><span class="sxs-lookup"><span data-stu-id="01f62-103">Configure fields for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01f62-104">Tässä ohjeaiheessa kerrotaan, miten varastonhallinnan mobiilisovelluksessa näytettävien kenttien nimet ja prioriteetit määritetään.</span><span class="sxs-lookup"><span data-stu-id="01f62-104">This topic describes how to define and configure names and priorities of fields shown in the Warehouse Management mobile app.</span></span>

> [!NOTE]
> <span data-ttu-id="01f62-105">Tämä ohjeaihe koskee varastonhallintamoduulin ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="01f62-105">This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="01f62-106">Se ei koske inventaariohallintamoduulin ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="01f62-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="01f62-107">Varastonhallinnan mobiilisovellus on sovellus, jonka avulla voit suorittaa fyysisen varastoinnin tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="01f62-107">The Warehouse Management mobile app is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="01f62-108">Voit määrittää ja konfiguroida kenttien nimet, joita käytetään sovelluksessa, sekä määrittää prioriteetin, johon kenttien nimet tulisi liittää.</span><span class="sxs-lookup"><span data-stu-id="01f62-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="01f62-109">Tässä ohjeaiheessa kerrotaan, miten nämä varastonhallinnan mobiilisovelluksen kenttien nimet ja prioriteetit määritetään ja miten niitä käytetään varastointisovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="01f62-109">This topic explains how to define and configure these Warehouse Management mobile app field names and priorities, and how they are used.</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="01f62-110">Warehousing-sovelluksen kenttien nimien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="01f62-110">Configure warehouse app field names</span></span>

<span data-ttu-id="01f62-111">Jos käytät varastointisovellusta mobiililaitteessa, voit määrittää **Varastointisovelluksen kenttien nimet** -sivulla, miten metatiedot näytetään laitteessa.</span><span class="sxs-lookup"><span data-stu-id="01f62-111">When you use Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="01f62-112">Luo kaikkien varastoinnin mobiililaitteen työnkulussa käytettävien kenttien nimet valitsemalla uudessa yrityksessä **Luo oletusasetukset**, ja määritä sitten niihin ensisijainen syötetila ja syötteen tyyppi.</span><span class="sxs-lookup"><span data-stu-id="01f62-112">In a new company, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="01f62-113">Kun kaikkien kenttien nimet on luotu, voit valita syötteen seuraavista vaihtoehdoista.</span><span class="sxs-lookup"><span data-stu-id="01f62-113">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01f62-114">Vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="01f62-114">Option</span></span></th>
<th><span data-ttu-id="01f62-115">kuvaus</span><span class="sxs-lookup"><span data-stu-id="01f62-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="01f62-116">Ensisijainen syöttömenetelmä</span><span class="sxs-lookup"><span data-stu-id="01f62-116">Preferred input mode</span></span></td>
<td><span data-ttu-id="01f62-117">Tämä vaihtoehto määrittää, näytetäänkö skannauskenttä vai manuaalinen syöttökenttä valitulle kentän nimelle.</span><span class="sxs-lookup"><span data-stu-id="01f62-117">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="01f62-118">Tämä on tarpeen sen erottamiseksi, jos viivakoodeja käytetään tälle kentälle.</span><span class="sxs-lookup"><span data-stu-id="01f62-118">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="01f62-119"><strong>Huomautus:</strong> Niille kenttien nimille, joiden ensisijainen syöttötila on <strong>Skannaus</strong>, voit syöttää tiedot manuaalisesti jos viivakoodi on vioittunut tai lukukelvoton.</span><span class="sxs-lookup"><span data-stu-id="01f62-119"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01f62-120">Syötetyyppi</span><span class="sxs-lookup"><span data-stu-id="01f62-120">Input type</span></span></td>
<td><span data-ttu-id="01f62-121">Tämä vaihtoehto määrittää, mitä syötetilaa pitäisi käyttää valitulle kentän nimelle.</span><span class="sxs-lookup"><span data-stu-id="01f62-121">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="01f62-122">Käytettävissä on neljä asetusta:</span><span class="sxs-lookup"><span data-stu-id="01f62-122">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="01f62-123"><strong>Valinta</strong> - sisältää asetusluettelon, josta voi valita.</span><span class="sxs-lookup"><span data-stu-id="01f62-123"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="01f62-124">Tässä vaihtoehdossa kenttien nimiä ei voi muokata.</span><span class="sxs-lookup"><span data-stu-id="01f62-124">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="01f62-125"><strong>Päivämäärä</strong> - kenttien nimet, jotka on määritetty päivämääriksi, näyttävät päivämäärämuodon otsikon yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="01f62-125"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="01f62-126">Näin varastotyöntekijät näkevät, missä muodossa kirjoittaa päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="01f62-126">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="01f62-127">Tässä vaihtoehdossa kenttien nimiä ei voi muokata.</span><span class="sxs-lookup"><span data-stu-id="01f62-127">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="01f62-128"><strong>Alpha</strong> - jos tämä valitaan, laitteen näppäimistöä käytetään syötettäessä tietoja manuaalisesti sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="01f62-128"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="01f62-129">Näppäimistön käyttöä voidaan muuttaa sen mukaan, mitä laitetta käytetään.</span><span class="sxs-lookup"><span data-stu-id="01f62-129">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="01f62-130"><strong>Numeerinen</strong> - kentän nimille, jotka käyttävät vain numeroita, voit valita tämän vaihtoehdon näyttääksesi mukautetun numeronäppäimistön syöttökentän yhteydessä laitteen näppäimistön sijaan.</span><span class="sxs-lookup"><span data-stu-id="01f62-130"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="01f62-131">Warehousing-sovelluksen kenttäprioriteetin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="01f62-131">Configure warehouse app field priority</span></span>

<span data-ttu-id="01f62-132">**Varastosovelluksen kenttäprioriteetti** -sivulla voit määrittää kenttänimet eri prioriteettiryhmiin.</span><span class="sxs-lookup"><span data-stu-id="01f62-132">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="01f62-133">Näin voit päättää, mitä tietoja näytetään sivulla päätehtäväsivulla silloin, kun fyysisen varastoinnin työntekijät suorittavat tehtäviä sovelluksen avulla.</span><span class="sxs-lookup"><span data-stu-id="01f62-133">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="01f62-134">Jos valitset **Luo oletusasetukset**, järjestelmä luo oletusarvoiset prioriteettiryhmät.</span><span class="sxs-lookup"><span data-stu-id="01f62-134">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="01f62-135">On mahdollista luoda niin monta prioriteettiryhmiä kuin on tarpeen, mutta tehtäväsivulla näytetään vain kolme prioriteettiryhmää.</span><span class="sxs-lookup"><span data-stu-id="01f62-135">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="01f62-136">Kun järjestelmä lähettää metatietoja sovellukseen, se määrittää kunkin kentän suhteellisen prioriteetin sen prioriteettiryhmän mukaan, ja sovellus näyttää ensimmäiset kolme metatietojen sisältämää prioriteettiryhmää.</span><span class="sxs-lookup"><span data-stu-id="01f62-136">When the system sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="01f62-137">Loput metatiedot näytetään toissijaisten tietojen sivulla.</span><span class="sxs-lookup"><span data-stu-id="01f62-137">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="01f62-138">Seuraavassa taulukossa on esimerkit viidestä prioriteettiryhmästä.</span><span class="sxs-lookup"><span data-stu-id="01f62-138">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01f62-139">Prioriteettiryhmä</span><span class="sxs-lookup"><span data-stu-id="01f62-139">Priority group</span></span></th>
<th><span data-ttu-id="01f62-140">Määritetyt kentät</span><span class="sxs-lookup"><span data-stu-id="01f62-140">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="01f62-141">Prioriteetti 10</span><span class="sxs-lookup"><span data-stu-id="01f62-141">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="01f62-142">Nimike</span><span class="sxs-lookup"><span data-stu-id="01f62-142">Item</span></span></li>
<li><span data-ttu-id="01f62-143">Määrä</span><span class="sxs-lookup"><span data-stu-id="01f62-143">Quantity</span></span></li>
<li><span data-ttu-id="01f62-144">Mittayksikkö</span><span class="sxs-lookup"><span data-stu-id="01f62-144">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="01f62-145">Prioriteetti 20</span><span class="sxs-lookup"><span data-stu-id="01f62-145">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="01f62-146">Sijainti klusterissa</span><span class="sxs-lookup"><span data-stu-id="01f62-146">Cluster position</span></span></li>
<li><span data-ttu-id="01f62-147">Klusteri</span><span class="sxs-lookup"><span data-stu-id="01f62-147">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="01f62-148">Prioriteetti 30</span><span class="sxs-lookup"><span data-stu-id="01f62-148">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="01f62-149">Nimikkeen kuvaus</span><span class="sxs-lookup"><span data-stu-id="01f62-149">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="01f62-150">Prioriteetti 40</span><span class="sxs-lookup"><span data-stu-id="01f62-150">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="01f62-151">Konfiguraatio</span><span class="sxs-lookup"><span data-stu-id="01f62-151">Configuration</span></span></li>
<li><span data-ttu-id="01f62-152">Väri</span><span class="sxs-lookup"><span data-stu-id="01f62-152">Color</span></span></li>
<li><span data-ttu-id="01f62-153">Koko</span><span class="sxs-lookup"><span data-stu-id="01f62-153">Size</span></span></li>
<li><span data-ttu-id="01f62-154">Tyyli</span><span class="sxs-lookup"><span data-stu-id="01f62-154">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="01f62-155">Prioriteetti 50</span><span class="sxs-lookup"><span data-stu-id="01f62-155">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="01f62-156">Paikka</span><span class="sxs-lookup"><span data-stu-id="01f62-156">Location</span></span></li>
<li><span data-ttu-id="01f62-157">Rekisterikilpi</span><span class="sxs-lookup"><span data-stu-id="01f62-157">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="01f62-158">Esimerkiksi kun varastotyöntekijä suorittaa tehtävän mobiililaitteella ja jos metatiedot, jotka näytetään sovelluksessa, koostuu seuraavista kentistä:</span><span class="sxs-lookup"><span data-stu-id="01f62-158">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="01f62-159">Nimike</span><span class="sxs-lookup"><span data-stu-id="01f62-159">Item</span></span>
-   <span data-ttu-id="01f62-160">Määrä</span><span class="sxs-lookup"><span data-stu-id="01f62-160">Quantity</span></span>
-   <span data-ttu-id="01f62-161">Mittayksikkö</span><span class="sxs-lookup"><span data-stu-id="01f62-161">Unit of measure</span></span>
-   <span data-ttu-id="01f62-162">Nimikkeen kuvaus</span><span class="sxs-lookup"><span data-stu-id="01f62-162">Item description</span></span>
-   <span data-ttu-id="01f62-163">Koko ja sijainti</span><span class="sxs-lookup"><span data-stu-id="01f62-163">Size and Location</span></span>

<span data-ttu-id="01f62-164">Yllä olevassa taulukossa määritettyjen varastosovelluksen kenttäprioriteettien perusteella seuraavat 3 tietoriviä näytetään tehtäväsivulla:</span><span class="sxs-lookup"><span data-stu-id="01f62-164">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="01f62-165">Rivi 1: Nimike, Määrä, Mittayksikkö</span><span class="sxs-lookup"><span data-stu-id="01f62-165">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="01f62-166">Rivi 2: Nimikkeen kuvaus</span><span class="sxs-lookup"><span data-stu-id="01f62-166">Row 2: Item description</span></span>
-   <span data-ttu-id="01f62-167">Rivi 3: koko</span><span class="sxs-lookup"><span data-stu-id="01f62-167">Row 3: Size</span></span>

<span data-ttu-id="01f62-168">Jäljellä olevat metatiedot, esimerkiksi sijainti, ei näy tehtäväsivulla, mutta kylläkin tietosivulla.</span><span class="sxs-lookup"><span data-stu-id="01f62-168">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="01f62-169">Lisätietoja ja esimerkkejä käyttöliittymästä saat blogikirjoituksesta [Finance and Operationsin varastointisovelluksen julkaisu](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="01f62-169">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="01f62-170">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="01f62-170">Additional resources</span></span>

[<span data-ttu-id="01f62-171">Varastonhallinnan mobiilisovelluksen asentaminen ja yhteyden muodostaminen</span><span class="sxs-lookup"><span data-stu-id="01f62-171">Install and connect the Warehouse Management mobile app</span></span>](../warehousing/install-configure-warehouse-management-app.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]