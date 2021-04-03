---
title: Suunniteltu cross-docking
description: Tässä ohjeaiheessa kuvataan suunniteltua cross-dockingia, jossa tilauksen edellyttämä varastomäärä ohjataan suoraan vastaanotosta tai luomisesta oikealle lähtevien laiturille tai valmistelualueelle. Saapuvan lähdekoodin koko jäljellä oleva varasto ohjataan oikeaan varastosijaintiin tavallisen hyllytysprosessin kautta.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 722b004e607cb2e6b7de292d92b67b18c2024696
ms.sourcegitcommit: 70b1567d316f19c15a4b032b4897f15c8dcdca09
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/08/2021
ms.locfileid: "5556263"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="6be13-104">Suunniteltu cross-docking</span><span class="sxs-lookup"><span data-stu-id="6be13-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6be13-105">Tässä aiheessa kuvataan suunnitellun cross-dockingin lisäasetukset.</span><span class="sxs-lookup"><span data-stu-id="6be13-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="6be13-106">Cross-docking on varastoprosessi, jossa tilauksen edellyttämä varastomäärä ohjataan suoraan vastaanotosta tai luomisesta oikealle lähtevien laiturille tai valmistelualueelle.</span><span class="sxs-lookup"><span data-stu-id="6be13-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="6be13-107">Saapuvan lähdekoodin koko jäljellä oleva varasto ohjataan oikeaan varastosijaintiin tavallisen hyllytysprosessin kautta.</span><span class="sxs-lookup"><span data-stu-id="6be13-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="6be13-108">Cross-dockingin avulla työntekijät ohittavat saapuvan hyllytyksen ja lähtevien nimikkeiden varaston, joka on jo merkitty lähtevälle tilaukselle.</span><span class="sxs-lookup"><span data-stu-id="6be13-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="6be13-109">Näin ollen varastojen kosketuskertojen määrää vähennetään mahdollisuuksien mukaan.</span><span class="sxs-lookup"><span data-stu-id="6be13-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="6be13-110">Lisäksi, koska vuorovaikutus järjestelmän kanssa on vähäisempää, fyysisen varastoinnin työn aika- ja tilasäästöt lisääntyvät.</span><span class="sxs-lookup"><span data-stu-id="6be13-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="6be13-111">Ennen kuin cross-docking voidaan suorittaa, käyttäjän on konfiguroitava uusi cross-docking-malli, jossa on määritetty toimituslähde ja muut cross-docking-vaatimukset.</span><span class="sxs-lookup"><span data-stu-id="6be13-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="6be13-112">Kun lähtevä tilaus luodaan, rivi täytyy merkitä saman nimikkeen sisältävään saapuvaan tilaukseen.</span><span class="sxs-lookup"><span data-stu-id="6be13-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="6be13-113">Saapuvien tilausten vastaanoton yhteydessä cross-docking-asennus määrittää automaattisesti, että cross-docking on tarpeen, ja luo varasto- ja kuormitustyön tarvittavalle määrälle sijaintidirektiivin asetusten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="6be13-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="6be13-114">Varastotapahtumat **eivät** ole rekisteröimättömiä, kun crossing-dock-työ peruutetaan, vaikka tämän ominaisuuden asetus olisi käytössä varastonhallinnan parametreissa.</span><span class="sxs-lookup"><span data-stu-id="6be13-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-features"></a><span data-ttu-id="6be13-115">Suunnitellun cross-docking-toimintojen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="6be13-115">Turn on the planned cross docking features</span></span>

<span data-ttu-id="6be13-116">Jos järjestelmäsi ei vielä sisällä tässä aiheessa kuvattuja ominaisuuksia, avaa [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja ota seuraavat ominaisuudet käyttöön seuraavassa järjestyksessä:</span><span class="sxs-lookup"><span data-stu-id="6be13-116">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the following features in the following order:</span></span>

1. <span data-ttu-id="6be13-117">*Suunniteltu cross-docking*</span><span class="sxs-lookup"><span data-stu-id="6be13-117">*Planned cross docking*</span></span>
2. <span data-ttu-id="6be13-118">*Cross docking -mallit ja sijaintidirektiivit*</span><span class="sxs-lookup"><span data-stu-id="6be13-118">*Cross docking templates with location directives*</span></span>

## <a name="setup"></a><span data-ttu-id="6be13-119">Luo perustiedot</span><span class="sxs-lookup"><span data-stu-id="6be13-119">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="6be13-120">Lataa kirjausmenetelmät uudelleen</span><span class="sxs-lookup"><span data-stu-id="6be13-120">Regenerate load posting methods</span></span>

<span data-ttu-id="6be13-121">Suunniteltu cross-docking toteutetaan kuormituksenkirjausmenetelmänä.</span><span class="sxs-lookup"><span data-stu-id="6be13-121">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="6be13-122">Kun olet määrittänyt toiminnon, menetelmät on luotava uudelleen.</span><span class="sxs-lookup"><span data-stu-id="6be13-122">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="6be13-123">Valitse **Varastonhallinta \> Asetukset \> Lataa kirjausmenetelmät**.</span><span class="sxs-lookup"><span data-stu-id="6be13-123">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="6be13-124">Valitse toimintoruudussa **Luo menetelmät uudelleen**.</span><span class="sxs-lookup"><span data-stu-id="6be13-124">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="6be13-125">Kun uudelleen luominen on suoritettu, näkyviin tulee menetelmä, jonka **menetelmän nimen** arvo on *planCrossDocking*.</span><span class="sxs-lookup"><span data-stu-id="6be13-125">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="6be13-126">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6be13-126">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="6be13-127">Luo cross-docking-malli</span><span class="sxs-lookup"><span data-stu-id="6be13-127">Create a cross-docking template</span></span>

1. <span data-ttu-id="6be13-128">Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Cross-docking-mallit**.</span><span class="sxs-lookup"><span data-stu-id="6be13-128">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="6be13-129">Valitse toimintoruudussa **Uusi** ja luo malli.</span><span class="sxs-lookup"><span data-stu-id="6be13-129">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="6be13-130">Aseta otsikkorivillä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6be13-130">In the header, set the following values:</span></span>

    - <span data-ttu-id="6be13-131">**Järjestys:** *1*</span><span class="sxs-lookup"><span data-stu-id="6be13-131">**Sequence:** *1*</span></span>

        <span data-ttu-id="6be13-132">Tämä kenttä määrittää, missä järjestyksessä mallit arvioidaan.</span><span class="sxs-lookup"><span data-stu-id="6be13-132">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="6be13-133">**Cross-docking-mallipohjan tunnus:** *51*</span><span class="sxs-lookup"><span data-stu-id="6be13-133">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="6be13-134">**Kuvaus:** *Varasto 51*</span><span class="sxs-lookup"><span data-stu-id="6be13-134">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="6be13-135">**Kysynnänvapautuskäytäntö:** *Ennen toimitusvastaanottoa*</span><span class="sxs-lookup"><span data-stu-id="6be13-135">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="6be13-136">**Varasto**: *51*</span><span class="sxs-lookup"><span data-stu-id="6be13-136">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="6be13-137">**Suunnittelu**-pikavälilehden määritys ohjaa mallin toimintaa.</span><span class="sxs-lookup"><span data-stu-id="6be13-137">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="6be13-138">Määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6be13-138">Set the following values:</span></span>

    - <span data-ttu-id="6be13-139">**Tarvevaatimukset:** *Ei mitään*</span><span class="sxs-lookup"><span data-stu-id="6be13-139">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="6be13-140">Tämä kenttä määrittää kysynnän varaston tarpeet.</span><span class="sxs-lookup"><span data-stu-id="6be13-140">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="6be13-141">Jos tarve on linkitetty tarjontaan ennen luovutusta, valitse *Merkintä*.</span><span class="sxs-lookup"><span data-stu-id="6be13-141">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="6be13-142">Jos kysynnän on oltava tilaus-varattu toimitusta vasten ennen julkaisua, valitse *Tilauksen varaus*.</span><span class="sxs-lookup"><span data-stu-id="6be13-142">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="6be13-143">**Sijaintityyppi:** *Lähetyssijainnit*</span><span class="sxs-lookup"><span data-stu-id="6be13-143">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="6be13-144">Tässä kentässä määritetään, käyttävätkö cross-docking-työt lähetyksen varastointi-/lataussijainteja vai käytetäänkö sen omia valmistelu-/kuormitussijainteja sijaintidirektiivien avulla.</span><span class="sxs-lookup"><span data-stu-id="6be13-144">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="6be13-145">**Työmalli:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="6be13-145">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="6be13-146">Tämä kenttä määrittää työmallin, jota käytetään, kun cross-docking-työtä luodaan.</span><span class="sxs-lookup"><span data-stu-id="6be13-146">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="6be13-147">**Tarkista uudelleen toimituskuitissa:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="6be13-147">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="6be13-148">Tämä vaihtoehto määrittää, tuleeko toimitus vahvistaa uudelleen vastaanoton aikana.</span><span class="sxs-lookup"><span data-stu-id="6be13-148">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="6be13-149">Jos tämän asetuksen arvoksi on määritetty *Kyllä*, sekä enimmäisaikaikkuna että vanhenemispäivien alue tarkistetaan.</span><span class="sxs-lookup"><span data-stu-id="6be13-149">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="6be13-150">**Direktiivikoodi** Jätä tämä kenttä tyhjäksi</span><span class="sxs-lookup"><span data-stu-id="6be13-150">**Directive code** Leave this field blank</span></span>

        <span data-ttu-id="6be13-151">Tämä valinta sallii järjestelmän käyttää sijaintidirektiivejä parhaan paikan määrittämiseen cross-docking varaston siirtämiselle.</span><span class="sxs-lookup"><span data-stu-id="6be13-151">This option enables the system to use location directives to help determine the best location to move cross-docking inventory to.</span></span> <span data-ttu-id="6be13-152">Voit määrittää sen määrittämällä jokaiselle asiaankuuluvalle cross-docking-mallille direktiivikoodin.</span><span class="sxs-lookup"><span data-stu-id="6be13-152">You can set it up by assigning a directive code to each relevant cross-docking template.</span></span> <span data-ttu-id="6be13-153">Kukin direktiivikoodi määrittää yksilöivän sijaintidirektiivin.</span><span class="sxs-lookup"><span data-stu-id="6be13-153">Each directive code identifies a unique location directive.</span></span>

    - <span data-ttu-id="6be13-154">**Vahvista aikaikkuna:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="6be13-154">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="6be13-155">Tämä vaihtoehto määrittää, arvioidaanko enimmäisaikaikkuna, kun toimituslähde valitaan.</span><span class="sxs-lookup"><span data-stu-id="6be13-155">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="6be13-156">Jos tämän asetuksen arvoksi on määritetty *Kyllä*, järjestelmän enimmäis- ja vähimmäisaikakenttiin liittyvät kentät ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="6be13-156">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="6be13-157">**Enimmäisaikaikkuna** *5*</span><span class="sxs-lookup"><span data-stu-id="6be13-157">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="6be13-158">Tämä kenttä määrittää enimmäisajan, joka on sallittu toimitusten saapumisen ja kysynnän poistumisen välillä.</span><span class="sxs-lookup"><span data-stu-id="6be13-158">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="6be13-159">**Enimmäisaikaikkunayksikkö:** *Päivät*</span><span class="sxs-lookup"><span data-stu-id="6be13-159">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="6be13-160">**Vähimmäisaikaikkuna** *0*</span><span class="sxs-lookup"><span data-stu-id="6be13-160">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="6be13-161">Tämä kenttä määrittää vähimmäisajan, joka on sallittu toimitusten saapumisen ja kysynnän poistumisen välillä.</span><span class="sxs-lookup"><span data-stu-id="6be13-161">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="6be13-162">**Vähimmäisaikaikkunayksikkö:** *Päivät*</span><span class="sxs-lookup"><span data-stu-id="6be13-162">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="6be13-163">**Voimassaolon päättymisalue päivissä** *0*</span><span class="sxs-lookup"><span data-stu-id="6be13-163">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="6be13-164">*Ensimmäinen päättymispäivä (FEFO) -ehto:* Tässä kentässä määritetään varastossa tällä hetkellä olevan ensimmäisen vanhentumiserän vanhentumispäivämäärän ja vastaanotetun erän välinen päivien enimmäismäärä.</span><span class="sxs-lookup"><span data-stu-id="6be13-164">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="6be13-165">**Toimituslähteet**-pikavälilehdessä voit määrittää tämän mallin käytettävissä olevat toimituslajit.</span><span class="sxs-lookup"><span data-stu-id="6be13-165">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="6be13-166">Valitse **Uusi** ja määritä sitten seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6be13-166">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="6be13-167">**Järjestysnumero:** *1*</span><span class="sxs-lookup"><span data-stu-id="6be13-167">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="6be13-168">**Toimituslähde:** *Ostotilaus*</span><span class="sxs-lookup"><span data-stu-id="6be13-168">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="6be13-169">Työluokan luominen</span><span class="sxs-lookup"><span data-stu-id="6be13-169">Create a work class</span></span>

1. <span data-ttu-id="6be13-170">Valitse **Varastonhallinta \> Asetukset \> Työ \> Työluokka**.</span><span class="sxs-lookup"><span data-stu-id="6be13-170">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="6be13-171">Valitse toimintoruudussa **Uusi** ja luo työluokka.</span><span class="sxs-lookup"><span data-stu-id="6be13-171">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="6be13-172">Määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6be13-172">Set the following values:</span></span>

    - <span data-ttu-id="6be13-173">**Työluokan tunnus:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="6be13-173">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="6be13-174">**Kuvaus:** *Cross Dock*</span><span class="sxs-lookup"><span data-stu-id="6be13-174">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="6be13-175">**Työtilaus tyyppi:** *Cross docking*</span><span class="sxs-lookup"><span data-stu-id="6be13-175">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="6be13-176">Luo työmalli</span><span class="sxs-lookup"><span data-stu-id="6be13-176">Create a work template</span></span>

1. <span data-ttu-id="6be13-177">Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työmallit**.</span><span class="sxs-lookup"><span data-stu-id="6be13-177">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="6be13-178">Aseta **Työtilaustyyppi**-kentän arvoksi *Cross-docking*.</span><span class="sxs-lookup"><span data-stu-id="6be13-178">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="6be13-179">Lisää **Yleiskuvaus**-välilehdelle uusi rivi valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6be13-179">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="6be13-180">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6be13-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="6be13-181">**Järjestysnumero:** *1*</span><span class="sxs-lookup"><span data-stu-id="6be13-181">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="6be13-182">**Työmalli:** *51 Cross Dock*</span><span class="sxs-lookup"><span data-stu-id="6be13-182">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="6be13-183">**Työmallin kuvaus:** *51 Cross Dock*</span><span class="sxs-lookup"><span data-stu-id="6be13-183">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="6be13-184">Valitse **Tallenna**, jos haluat, että **Työmallin tiedot** -pikavälilehti on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="6be13-184">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="6be13-185">Lisää uusi rivi ruudukkoon **Työmallin tiedot** -pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6be13-185">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="6be13-186">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6be13-186">On the new line, set the following values:</span></span>

    - <span data-ttu-id="6be13-187">**Työtyyppi:** *Poiminta*</span><span class="sxs-lookup"><span data-stu-id="6be13-187">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="6be13-188">**Työluokan tunnus:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="6be13-188">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="6be13-189">Lisää toinen rivi valitsemalla **Uusi** ja määritä sille seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6be13-189">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="6be13-190">**Työtyyppi:** *Aseta*</span><span class="sxs-lookup"><span data-stu-id="6be13-190">**Work type:** *Put*</span></span>
    - <span data-ttu-id="6be13-191">**Työluokan tunnus:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="6be13-191">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="6be13-192">Valitse **Tallenna** ja vahvista, että *51 Cross Dock* -mallille on valittu **Kelvollinen**-valintaruutu .</span><span class="sxs-lookup"><span data-stu-id="6be13-192">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="6be13-193">*Poiminta*- ja *Hhyllytys*-työtyyppien työluokkien tunnusten on oltava samat.</span><span class="sxs-lookup"><span data-stu-id="6be13-193">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="6be13-194">Luo toimipaikkadirektiivit</span><span class="sxs-lookup"><span data-stu-id="6be13-194">Create location directives</span></span>

1. <span data-ttu-id="6be13-195">Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.</span><span class="sxs-lookup"><span data-stu-id="6be13-195">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="6be13-196">Aseta vasemmassa ruudussa **Työtilaustyyppi**-kentän arvoksi *Cross-docking*.</span><span class="sxs-lookup"><span data-stu-id="6be13-196">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="6be13-197">Valitse toimintoruudussa **Uusi** ja määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6be13-197">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="6be13-198">**Järjestysnumero:** *1*</span><span class="sxs-lookup"><span data-stu-id="6be13-198">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="6be13-199">**Nimi:** *51 Cross Dock Put*</span><span class="sxs-lookup"><span data-stu-id="6be13-199">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="6be13-200">**Työtyyppi:** *Aseta*</span><span class="sxs-lookup"><span data-stu-id="6be13-200">**Work type:** *Put*</span></span>
    - <span data-ttu-id="6be13-201">**Toimipaikka:** *5*</span><span class="sxs-lookup"><span data-stu-id="6be13-201">**Site:** *5*</span></span>
    - <span data-ttu-id="6be13-202">**Varasto**: *51*</span><span class="sxs-lookup"><span data-stu-id="6be13-202">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="6be13-203">Valitse **Tallenna**, jos haluat, että **Rivit**-pikavälilehti on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="6be13-203">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="6be13-204">Lisää uusi rivi ruudukkoon **Rivit**-pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6be13-204">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="6be13-205">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6be13-205">On the new line, set the following values:</span></span>

    - <span data-ttu-id="6be13-206">**Määrästä:** *1*</span><span class="sxs-lookup"><span data-stu-id="6be13-206">**From quantity:** *1*</span></span>
    - <span data-ttu-id="6be13-207">**Määrälle:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="6be13-207">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="6be13-208">Valitse **Tallenna**, jos haluat, että **Paikkadirektiivitoimenpiteet**-pikavälilehti on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="6be13-208">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="6be13-209">Lisää uusi rivi ruudukkoon **Sijaintidirektiivin toiminnot** -pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6be13-209">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="6be13-210">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6be13-210">On the new line, set the following values:</span></span>

    - <span data-ttu-id="6be13-211">**Nimi:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="6be13-211">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="6be13-212">**Kiinteän sijainnin käyttö:** *Kiinteät ja muut kuin kiinteät sijainnit*</span><span class="sxs-lookup"><span data-stu-id="6be13-212">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="6be13-213">Valitse **Tallenna**, jos haluat, että **Sijaintidirektiivin toiminnot** -työkalurivin **Muokkaa kyselyä** -painike on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="6be13-213">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="6be13-214">Avaa kyselyeditori valitsemalla **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="6be13-214">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="6be13-215">Varmista **Alue** -välilehdessä, että seuraavat kaksi riviä on konfiguroitu:</span><span class="sxs-lookup"><span data-stu-id="6be13-215">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="6be13-216">Rivi 1:</span><span class="sxs-lookup"><span data-stu-id="6be13-216">Line 1:</span></span>

        - <span data-ttu-id="6be13-217">**Taulu:** *Sijainnit*</span><span class="sxs-lookup"><span data-stu-id="6be13-217">**Table:** *Locations*</span></span>
        - <span data-ttu-id="6be13-218">**Johdettu taulu:** *Sijainnit*</span><span class="sxs-lookup"><span data-stu-id="6be13-218">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="6be13-219">**Kenttä:** *Varasto*</span><span class="sxs-lookup"><span data-stu-id="6be13-219">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="6be13-220">**Ehdot:** *51*</span><span class="sxs-lookup"><span data-stu-id="6be13-220">**Criteria:** *51*</span></span>

    - <span data-ttu-id="6be13-221">Rivi 2:</span><span class="sxs-lookup"><span data-stu-id="6be13-221">Line 2:</span></span>

        - <span data-ttu-id="6be13-222">**Taulu:** *Sijainnit*</span><span class="sxs-lookup"><span data-stu-id="6be13-222">**Table:** *Locations*</span></span>
        - <span data-ttu-id="6be13-223">**Johdettu taulu:** *Sijainnit*</span><span class="sxs-lookup"><span data-stu-id="6be13-223">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="6be13-224">**Kenttä:** *Sijainti*</span><span class="sxs-lookup"><span data-stu-id="6be13-224">**Field:** *Location*</span></span>
        - <span data-ttu-id="6be13-225">**Kriteerit:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="6be13-225">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="6be13-226">Valitse **OK** sulkeaksesi kyselyeditorin.</span><span class="sxs-lookup"><span data-stu-id="6be13-226">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="6be13-227">Luo mobiililaitteen valikkovaihtoehto</span><span class="sxs-lookup"><span data-stu-id="6be13-227">Create a mobile device menu item</span></span>

1. <span data-ttu-id="6be13-228">Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.</span><span class="sxs-lookup"><span data-stu-id="6be13-228">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="6be13-229">Valitse vasemmanpuoleisen ruudun valikkovaihtoehtojen luettelosta **Oston hyllytys**.</span><span class="sxs-lookup"><span data-stu-id="6be13-229">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="6be13-230">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="6be13-230">Select **Edit**.</span></span>
1. <span data-ttu-id="6be13-231">Lisää uusi rivi ruudukkoon **Työlajit**-pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6be13-231">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="6be13-232">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6be13-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="6be13-233">**Työluokan tunnus:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="6be13-233">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="6be13-234">**Työtilaus tyyppi:** *Cross docking*</span><span class="sxs-lookup"><span data-stu-id="6be13-234">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="6be13-235">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="6be13-235">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="6be13-236">Skenaario</span><span class="sxs-lookup"><span data-stu-id="6be13-236">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="6be13-237">Ostotilauksen luominen</span><span class="sxs-lookup"><span data-stu-id="6be13-237">Create a purchase order</span></span>

<span data-ttu-id="6be13-238">Noudattamalla näitä ohjeita voit luoda ostotilauksen toimituslähteeksi.</span><span class="sxs-lookup"><span data-stu-id="6be13-238">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="6be13-239">Siirry kohtaan **Hankinta ja alihankinta \> Ostotilaukset \> Kaikki ostotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="6be13-239">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="6be13-240">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6be13-240">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="6be13-241">Aseta **Luo ostotilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6be13-241">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="6be13-242">**Toimittajan tili:** *104*</span><span class="sxs-lookup"><span data-stu-id="6be13-242">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="6be13-243">**Varasto**: *51*</span><span class="sxs-lookup"><span data-stu-id="6be13-243">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="6be13-244">Valitse **OK** ja kirjoita tilausnumero muistiin.</span><span class="sxs-lookup"><span data-stu-id="6be13-244">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="6be13-245">**Ostotilausrivit**-pikavälilehdelle lisätään uusi rivi.</span><span class="sxs-lookup"><span data-stu-id="6be13-245">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="6be13-246">Määritä tälle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6be13-246">On this line, set the following values:</span></span>

    - <span data-ttu-id="6be13-247">**Nimiketunnus:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="6be13-247">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="6be13-248">**Määrä** *5*</span><span class="sxs-lookup"><span data-stu-id="6be13-248">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="6be13-249">Luo myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="6be13-249">Create a sales order</span></span>

<span data-ttu-id="6be13-250">Noudattamalla näitä ohjeita voit luoda myyntitilauksen kysynnän lähteeksi.</span><span class="sxs-lookup"><span data-stu-id="6be13-250">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="6be13-251">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="6be13-251">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="6be13-252">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6be13-252">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="6be13-253">Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6be13-253">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="6be13-254">**Asiakastili:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="6be13-254">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="6be13-255">**Varasto**: *51*</span><span class="sxs-lookup"><span data-stu-id="6be13-255">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="6be13-256">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6be13-256">Select **OK**.</span></span>
1. <span data-ttu-id="6be13-257">**Myyntitilausrivit**-pikavälilehdelle lisätään uusi rivi.</span><span class="sxs-lookup"><span data-stu-id="6be13-257">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="6be13-258">Määritä tälle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="6be13-258">On this line, set the following values:</span></span>

    - <span data-ttu-id="6be13-259">**Nimiketunnus:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="6be13-259">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="6be13-260">**Määrä** *3*</span><span class="sxs-lookup"><span data-stu-id="6be13-260">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="6be13-261">Luo suunniteltu cross-docking</span><span class="sxs-lookup"><span data-stu-id="6be13-261">Create planned cross-docking</span></span>

<span data-ttu-id="6be13-262">Seuraavien vaiheiden avulla voit luoda suunnitellun cross-dockingin myyntitilauksesta.</span><span class="sxs-lookup"><span data-stu-id="6be13-262">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="6be13-263">Valitse juuri luomasi myynti tilauksen **Myyntitilaustiedot** -sivulta toimenpideruudun **Varasto**-välilehden **Toiminnot**-ryhmästä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="6be13-263">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="6be13-264">Vapauta varastoon -toiminto luo myyntitilausriville lähetys- ja kuormitusrivin sekä yrittää kohdistaa varaston.</span><span class="sxs-lookup"><span data-stu-id="6be13-264">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="6be13-265">Näyttöön avautuu tietosanoma.</span><span class="sxs-lookup"><span data-stu-id="6be13-265">You receive an informational message.</span></span> <span data-ttu-id="6be13-266">Näyttöön tulee myös seuraava varoitussanoma: "Aallolle XXXX ei luotu työtä.</span><span class="sxs-lookup"><span data-stu-id="6be13-266">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="6be13-267">Lisätietoja on työn luonnin historialokissa."</span><span class="sxs-lookup"><span data-stu-id="6be13-267">See the work creation history log for details."</span></span> <span data-ttu-id="6be13-268">Tämä toiminta on odotettavissa, koska varastossa ei ole varastoa.</span><span class="sxs-lookup"><span data-stu-id="6be13-268">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="6be13-269">Valitse **Myyntitilausrivit**-pikavälilehdellä **Varasto**-valikosta **Lähetyksen tiedot**.</span><span class="sxs-lookup"><span data-stu-id="6be13-269">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="6be13-270">Näkyviin tulee **Lähetyksen tiedot** -sivu, jossa näkyy myyntitilaukselle luotu lähetys.</span><span class="sxs-lookup"><span data-stu-id="6be13-270">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="6be13-271">Huomaa, että **Suunniteltu cross-docking-määrä** -kentän arvo on *3* **Lataa rivit** -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="6be13-271">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="6be13-272">Koska varastossa ei ollut käytettävissä varastoa, mutta voimassa oleva toimituslähde saapuu cross-docking-mallissa määritettyyn aikaikkunaan, cross-docking-määrä on luotu.</span><span class="sxs-lookup"><span data-stu-id="6be13-272">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="6be13-273">Voit tarkastella luotuja cross-docking-tietoja valitsemalla **Lataa rivit** -pikavälilehdessä **Suunniteltu cross-docking**.</span><span class="sxs-lookup"><span data-stu-id="6be13-273">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="6be13-274">Prossessoi cross-docking</span><span class="sxs-lookup"><span data-stu-id="6be13-274">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="6be13-275">Ostotilauksen vastaanotto varastoinnin mobiilisovelluksessa</span><span class="sxs-lookup"><span data-stu-id="6be13-275">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="6be13-276">Järjestelmä vastaanottaa ostotilauksesta viiden määrän vastaanottosijaintiin ja luo kaksi työkappaletta.</span><span class="sxs-lookup"><span data-stu-id="6be13-276">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="6be13-277">Ensimmäisen luotavan työtunnuksen **Työtilaustyypin** arvo on *Cross docking* ja se on linkitetty myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="6be13-277">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="6be13-278">Sen määrä on 3 ja se ohjataan lopulliseen lähetyssijaintiin, jotta se voidaan lähettää heti.</span><span class="sxs-lookup"><span data-stu-id="6be13-278">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="6be13-279">Toisen luotavan työtunnuksen **Työtilaustyypin** arvo on *Ostotilaukset* ja se on linkitetty ostotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="6be13-279">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="6be13-280">Sen jäljellä oleva määrä on 2, se ei ollut cross-dockattu ja se ohjataan hyllytyksen varastointiin.</span><span class="sxs-lookup"><span data-stu-id="6be13-280">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="6be13-281">Kirjaudu kannettavaan laitteeseen käyttäjänä varastossa *51*.</span><span class="sxs-lookup"><span data-stu-id="6be13-281">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="6be13-282">Siirry kohtaan **Saapuva \> Oston vastaanotto**.</span><span class="sxs-lookup"><span data-stu-id="6be13-282">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="6be13-283">Syötä **PONum**-kenttään ostotilauksen numero.</span><span class="sxs-lookup"><span data-stu-id="6be13-283">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="6be13-284">Kirjoita **Määrä**-kenttään *5*.</span><span class="sxs-lookup"><span data-stu-id="6be13-284">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="6be13-285">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6be13-285">Select **OK**.</span></span>
1. <span data-ttu-id="6be13-286">Määritä seuraavalla sivulla **Nimike**-kentän arvoksi *A0001*.</span><span class="sxs-lookup"><span data-stu-id="6be13-286">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="6be13-287">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6be13-287">Select **OK**.</span></span>
1. <span data-ttu-id="6be13-288">Vahvista seuraavalla sivulla **PONum**-, **Nimike**- ja **Määrä**-arvot valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="6be13-288">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="6be13-289">Näyttöön tulee Työ valmis -sanoma.</span><span class="sxs-lookup"><span data-stu-id="6be13-289">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="6be13-290">Valitse **Peruuta**, jos haluat poistua.</span><span class="sxs-lookup"><span data-stu-id="6be13-290">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="6be13-291">Hyllytys cross-dockingiin ja irtotavaraan</span><span class="sxs-lookup"><span data-stu-id="6be13-291">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="6be13-292">Tällä hetkellä molemmilla työtunnuksilla on sama kohderekisterikilpi.</span><span class="sxs-lookup"><span data-stu-id="6be13-292">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="6be13-293">Jotta voit suorittaa seuraavat vaiheet, sinun on saatava työtunnus ja kohderekisterikilpitunnus.</span><span class="sxs-lookup"><span data-stu-id="6be13-293">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="6be13-294">Voit saada nämä tiedot ostotilausrivin ja myyntitilausrivin työtiedoista.</span><span class="sxs-lookup"><span data-stu-id="6be13-294">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="6be13-295">Vaihtoehtoisesti voit siirtyä kohtaan **Varastonhallinta \> Työ \> Työtiedot** ja suodattaa työt, joissa **Varasto**-arvo on *51*.</span><span class="sxs-lookup"><span data-stu-id="6be13-295">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="6be13-296">Siirry mobiililaitteen **Saapuva \> Ostohyllytys**-kohtaan ja kirjoita työn kohderekisterikilpi.</span><span class="sxs-lookup"><span data-stu-id="6be13-296">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="6be13-297">Kirjoita **Tunnus**-kenttään työtietojen kohderekisteritunnus.</span><span class="sxs-lookup"><span data-stu-id="6be13-297">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="6be13-298">Cross-docking-keräyssivulla näkyy keräilysijainti (*RECV*), kohderekisterikilpi (*rekisterikilpi*), nimike (*A0001*) ja määrä (*3*).</span><span class="sxs-lookup"><span data-stu-id="6be13-298">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="6be13-299">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6be13-299">Select **OK**.</span></span>
1. <span data-ttu-id="6be13-300">Kirjoita **Kohde-RK**-kenttään sen rekisterikilven tunnus, joka on tarkoitus sijoittaa (cross-dockata) lähetyssijaintiin.</span><span class="sxs-lookup"><span data-stu-id="6be13-300">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="6be13-301">Voit valita haluamasi rekisterikilven tunnuksen.</span><span class="sxs-lookup"><span data-stu-id="6be13-301">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="6be13-302">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6be13-302">Select **OK**.</span></span>
1. <span data-ttu-id="6be13-303">Kirjoita seuraavalla sivulla **Tunnus**-kenttään kohderekisteritunnus.</span><span class="sxs-lookup"><span data-stu-id="6be13-303">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="6be13-304">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6be13-304">Select **OK**.</span></span>
1. <span data-ttu-id="6be13-305">Vahvista jäljellä olevan määrän 2 poimintatyö ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6be13-305">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="6be13-306">Valitse seuraavalla sivulla **Valmis**, kun haluat lopettaa poimintaprosessin ja aloittaa hyllytysprosessin.</span><span class="sxs-lookup"><span data-stu-id="6be13-306">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="6be13-307">Mobiilisovellus esittää sinulle sijainnin ja rekisterikilven, johon kohde sijoitetaan.</span><span class="sxs-lookup"><span data-stu-id="6be13-307">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="6be13-308">Vahvista irtotavaran **Hyllytys** valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="6be13-308">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="6be13-309">Varmista seuraavalla sivulla, että cross-dockingin **Hyllytys** on käytössä valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="6be13-309">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="6be13-310">Näyttöön tulee Työ valmis -sanoma.</span><span class="sxs-lookup"><span data-stu-id="6be13-310">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="6be13-311">Valitse **Peruuta**, jos haluat poistua.</span><span class="sxs-lookup"><span data-stu-id="6be13-311">Select **Cancel** to exit.</span></span>

<span data-ttu-id="6be13-312">Seuraavassa kuvassa näkyy, miten tehty cross-docking-työ saattaa näkyä Microsoft Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="6be13-312">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="6be13-313">![Cross-docking-työ päättynyt](media/PlannedCrossDockingWork.png "Cross-docking-työ päättynyt")</span><span class="sxs-lookup"><span data-stu-id="6be13-313">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]