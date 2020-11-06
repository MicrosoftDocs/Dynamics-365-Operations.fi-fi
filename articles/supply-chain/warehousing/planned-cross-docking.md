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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: cc217f21a5fa70feb9ef9161f3ef2e2b6a333f35
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017756"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="244b6-104">Suunniteltu cross-docking</span><span class="sxs-lookup"><span data-stu-id="244b6-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="244b6-105">Tässä aiheessa kuvataan suunnitellun cross-dockingin lisäasetukset.</span><span class="sxs-lookup"><span data-stu-id="244b6-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="244b6-106">Cross-docking on varastoprosessi, jossa tilauksen edellyttämä varastomäärä ohjataan suoraan vastaanotosta tai luomisesta oikealle lähtevien laiturille tai valmistelualueelle.</span><span class="sxs-lookup"><span data-stu-id="244b6-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="244b6-107">Saapuvan lähdekoodin koko jäljellä oleva varasto ohjataan oikeaan varastosijaintiin tavallisen hyllytysprosessin kautta.</span><span class="sxs-lookup"><span data-stu-id="244b6-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="244b6-108">Cross-dockingin avulla työntekijät ohittavat saapuvan hyllytyksen ja lähtevien nimikkeiden varaston, joka on jo merkitty lähtevälle tilaukselle.</span><span class="sxs-lookup"><span data-stu-id="244b6-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="244b6-109">Näin ollen varastojen kosketuskertojen määrää vähennetään mahdollisuuksien mukaan.</span><span class="sxs-lookup"><span data-stu-id="244b6-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="244b6-110">Lisäksi, koska vuorovaikutus järjestelmän kanssa on vähäisempää, fyysisen varastoinnin työn aika- ja tilasäästöt lisääntyvät.</span><span class="sxs-lookup"><span data-stu-id="244b6-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="244b6-111">Ennen kuin cross-docking voidaan suorittaa, käyttäjän on konfiguroitava uusi cross-docking-malli, jossa on määritetty toimituslähde ja muut cross-docking-vaatimukset.</span><span class="sxs-lookup"><span data-stu-id="244b6-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="244b6-112">Kun lähtevä tilaus luodaan, rivi täytyy merkitä saman nimikkeen sisältävään saapuvaan tilaukseen.</span><span class="sxs-lookup"><span data-stu-id="244b6-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="244b6-113">Saapuvien tilausten vastaanoton yhteydessä cross-docking-asennus määrittää automaattisesti, että cross-docking on tarpeen, ja luo varasto- ja kuormitustyön tarvittavalle määrälle sijaintidirektiivin asetusten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="244b6-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="244b6-114">Varastotapahtumat **eivät** ole rekisteröimättömiä, kun crossing-dock-työ peruutetaan, vaikka tämän ominaisuuden asetus olisi käytössä varastonhallinnan parametreissa.</span><span class="sxs-lookup"><span data-stu-id="244b6-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-feature"></a><span data-ttu-id="244b6-115">Suunnitellun cross-docking-toiminnon ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="244b6-115">Turn on the Planned cross docking feature</span></span>

<span data-ttu-id="244b6-116">Ennen kuin voit käyttää laajennettua suunniteltua cross-dockingia, sinun on otettava järjestelmäsi toiminto käyttöön.</span><span class="sxs-lookup"><span data-stu-id="244b6-116">Before you can use advanced planned cross-docking, the feature must be turned on in your system.</span></span> <span data-ttu-id="244b6-117">Järjestelmänvalvojat voivat käyttää [Toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) työtilaa tarkistaakseen toiminnon tilan sekä laittaa sen päälle, jos sitä vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="244b6-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="244b6-118">Tässä tapauksessa toiminto näkyy seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="244b6-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="244b6-119">**Moduuli:** *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="244b6-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="244b6-120">**Toiminnon nimi:** *Suunniteltu cross-docking*</span><span class="sxs-lookup"><span data-stu-id="244b6-120">**Feature name:** *Planned cross docking*</span></span>

## <a name="setup"></a><span data-ttu-id="244b6-121">Määritys</span><span class="sxs-lookup"><span data-stu-id="244b6-121">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="244b6-122">Lataa kirjausmenetelmät uudelleen</span><span class="sxs-lookup"><span data-stu-id="244b6-122">Regenerate load posting methods</span></span>

<span data-ttu-id="244b6-123">Suunniteltu cross-docking toteutetaan kuormituksenkirjausmenetelmänä.</span><span class="sxs-lookup"><span data-stu-id="244b6-123">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="244b6-124">Kun olet määrittänyt toiminnon, menetelmät on luotava uudelleen.</span><span class="sxs-lookup"><span data-stu-id="244b6-124">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="244b6-125">Valitse **Varastonhallinta \> Asetukset \> Lataa kirjausmenetelmät**.</span><span class="sxs-lookup"><span data-stu-id="244b6-125">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="244b6-126">Valitse toimintoruudussa **Luo menetelmät uudelleen**.</span><span class="sxs-lookup"><span data-stu-id="244b6-126">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="244b6-127">Kun uudelleen luominen on suoritettu, näkyviin tulee menetelmä, jonka **menetelmän nimen** arvo on *planCrossDocking*.</span><span class="sxs-lookup"><span data-stu-id="244b6-127">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="244b6-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="244b6-128">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="244b6-129">Luo cross-docking-malli</span><span class="sxs-lookup"><span data-stu-id="244b6-129">Create a cross-docking template</span></span>

1. <span data-ttu-id="244b6-130">Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Cross-docking-mallit**.</span><span class="sxs-lookup"><span data-stu-id="244b6-130">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="244b6-131">Valitse toimintoruudussa **Uusi** ja luo malli.</span><span class="sxs-lookup"><span data-stu-id="244b6-131">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="244b6-132">Aseta otsikkorivillä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="244b6-132">In the header, set the following values:</span></span>

    - <span data-ttu-id="244b6-133">**Järjestys:** *1*</span><span class="sxs-lookup"><span data-stu-id="244b6-133">**Sequence:** *1*</span></span>

        <span data-ttu-id="244b6-134">Tämä kenttä määrittää, missä järjestyksessä mallit arvioidaan.</span><span class="sxs-lookup"><span data-stu-id="244b6-134">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="244b6-135">**Cross-docking-mallipohjan tunnus:** *51*</span><span class="sxs-lookup"><span data-stu-id="244b6-135">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="244b6-136">**Kuvaus:** *Varasto 51*</span><span class="sxs-lookup"><span data-stu-id="244b6-136">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="244b6-137">**Kysynnänvapautuskäytäntö:** *Ennen toimitusvastaanottoa*</span><span class="sxs-lookup"><span data-stu-id="244b6-137">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="244b6-138">**Varasto** : *51*</span><span class="sxs-lookup"><span data-stu-id="244b6-138">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="244b6-139">**Suunnittelu** -pikavälilehden määritys ohjaa mallin toimintaa.</span><span class="sxs-lookup"><span data-stu-id="244b6-139">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="244b6-140">Määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="244b6-140">Set the following values:</span></span>

    - <span data-ttu-id="244b6-141">**Tarvevaatimukset:** *Ei mitään*</span><span class="sxs-lookup"><span data-stu-id="244b6-141">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="244b6-142">Tämä kenttä määrittää kysynnän varaston tarpeet.</span><span class="sxs-lookup"><span data-stu-id="244b6-142">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="244b6-143">Jos tarve on linkitetty tarjontaan ennen luovutusta, valitse *Merkintä*.</span><span class="sxs-lookup"><span data-stu-id="244b6-143">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="244b6-144">Jos kysynnän on oltava tilaus-varattu toimitusta vasten ennen julkaisua, valitse *Tilauksen varaus*.</span><span class="sxs-lookup"><span data-stu-id="244b6-144">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="244b6-145">**Sijaintityyppi:** *Lähetyssijainnit*</span><span class="sxs-lookup"><span data-stu-id="244b6-145">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="244b6-146">Tässä kentässä määritetään, käyttävätkö cross-docking-työt lähetyksen varastointi-/lataussijainteja vai käytetäänkö sen omia valmistelu-/kuormitussijainteja sijaintidirektiivien avulla.</span><span class="sxs-lookup"><span data-stu-id="244b6-146">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="244b6-147">**Työmalli:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="244b6-147">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="244b6-148">Tämä kenttä määrittää työmallin, jota käytetään, kun cross-docking-työtä luodaan.</span><span class="sxs-lookup"><span data-stu-id="244b6-148">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="244b6-149">**Tarkista uudelleen toimituskuitissa:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="244b6-149">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="244b6-150">Tämä vaihtoehto määrittää, tuleeko toimitus vahvistaa uudelleen vastaanoton aikana.</span><span class="sxs-lookup"><span data-stu-id="244b6-150">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="244b6-151">Jos tämän asetuksen arvoksi on määritetty *Kyllä* , sekä enimmäisaikaikkuna että vanhenemispäivien alue tarkistetaan.</span><span class="sxs-lookup"><span data-stu-id="244b6-151">If this option is set to *Yes* , both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="244b6-152">**Vahvista aikaikkuna:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="244b6-152">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="244b6-153">Tämä vaihtoehto määrittää, arvioidaanko enimmäisaikaikkuna, kun toimituslähde valitaan.</span><span class="sxs-lookup"><span data-stu-id="244b6-153">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="244b6-154">Jos tämän asetuksen arvoksi on määritetty *Kyllä* , järjestelmän enimmäis- ja vähimmäisaikakenttiin liittyvät kentät ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="244b6-154">If this option is set to *Yes* , the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="244b6-155">**Enimmäisaikaikkuna** *5*</span><span class="sxs-lookup"><span data-stu-id="244b6-155">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="244b6-156">Tämä kenttä määrittää enimmäisajan, joka on sallittu toimitusten saapumisen ja kysynnän poistumisen välillä.</span><span class="sxs-lookup"><span data-stu-id="244b6-156">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="244b6-157">**Enimmäisaikaikkunayksikkö:** *Päivät*</span><span class="sxs-lookup"><span data-stu-id="244b6-157">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="244b6-158">**Vähimmäisaikaikkuna** *0*</span><span class="sxs-lookup"><span data-stu-id="244b6-158">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="244b6-159">Tämä kenttä määrittää vähimmäisajan, joka on sallittu toimitusten saapumisen ja kysynnän poistumisen välillä.</span><span class="sxs-lookup"><span data-stu-id="244b6-159">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="244b6-160">**Vähimmäisaikaikkunayksikkö:** *Päivät*</span><span class="sxs-lookup"><span data-stu-id="244b6-160">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="244b6-161">**Voimassaolon päättymisalue päivissä** *0*</span><span class="sxs-lookup"><span data-stu-id="244b6-161">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="244b6-162">*Ensimmäinen päättymispäivä (FEFO) -ehto:* Tässä kentässä määritetään varastossa tällä hetkellä olevan ensimmäisen vanhentumiserän vanhentumispäivämäärän ja vastaanotetun erän välinen päivien enimmäismäärä.</span><span class="sxs-lookup"><span data-stu-id="244b6-162">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="244b6-163">**Toimituslähteet** -pikavälilehdessä voit määrittää tämän mallin käytettävissä olevat toimituslajit.</span><span class="sxs-lookup"><span data-stu-id="244b6-163">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="244b6-164">Valitse **Uusi** ja määritä sitten seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="244b6-164">Select **New** , and then set the following values:</span></span>

    - <span data-ttu-id="244b6-165">**Järjestysnumero:** *1*</span><span class="sxs-lookup"><span data-stu-id="244b6-165">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="244b6-166">**Toimituslähde:** *Ostotilaus*</span><span class="sxs-lookup"><span data-stu-id="244b6-166">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="244b6-167">Työluokan luominen</span><span class="sxs-lookup"><span data-stu-id="244b6-167">Create a work class</span></span>

1. <span data-ttu-id="244b6-168">Valitse **Varastonhallinta \> Asetukset \> Työ \> Työluokka**.</span><span class="sxs-lookup"><span data-stu-id="244b6-168">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="244b6-169">Valitse toimintoruudussa **Uusi** ja luo työluokka.</span><span class="sxs-lookup"><span data-stu-id="244b6-169">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="244b6-170">Määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="244b6-170">Set the following values:</span></span>

    - <span data-ttu-id="244b6-171">**Työluokan tunnus:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="244b6-171">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="244b6-172">**Kuvaus:** *Cross Dock*</span><span class="sxs-lookup"><span data-stu-id="244b6-172">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="244b6-173">**Työtilaus tyyppi:** *Cross docking*</span><span class="sxs-lookup"><span data-stu-id="244b6-173">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="244b6-174">Luo työmalli</span><span class="sxs-lookup"><span data-stu-id="244b6-174">Create a work template</span></span>

1. <span data-ttu-id="244b6-175">Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työmallit**.</span><span class="sxs-lookup"><span data-stu-id="244b6-175">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="244b6-176">Aseta **Työtilaustyyppi** -kentän arvoksi *Cross-docking*.</span><span class="sxs-lookup"><span data-stu-id="244b6-176">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="244b6-177">Lisää **Yleiskuvaus** -välilehdelle uusi rivi valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="244b6-177">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="244b6-178">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="244b6-178">On the new line, set the following values:</span></span>

    - <span data-ttu-id="244b6-179">**Järjestysnumero:** *1*</span><span class="sxs-lookup"><span data-stu-id="244b6-179">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="244b6-180">**Työmalli:** *51 Cross Dock*</span><span class="sxs-lookup"><span data-stu-id="244b6-180">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="244b6-181">**Työmallin kuvaus:** *51 Cross Dock*</span><span class="sxs-lookup"><span data-stu-id="244b6-181">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="244b6-182">Valitse **Tallenna** , jos haluat, että **Työmallin tiedot** -pikavälilehti on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="244b6-182">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="244b6-183">Lisää uusi rivi ruudukkoon **Työmallin tiedot** -pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="244b6-183">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="244b6-184">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="244b6-184">On the new line, set the following values:</span></span>

    - <span data-ttu-id="244b6-185">**Työtyyppi:** *Poiminta*</span><span class="sxs-lookup"><span data-stu-id="244b6-185">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="244b6-186">**Työluokan tunnus:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="244b6-186">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="244b6-187">Lisää toinen rivi valitsemalla **Uusi** ja määritä sille seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="244b6-187">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="244b6-188">**Työtyyppi:** *Aseta*</span><span class="sxs-lookup"><span data-stu-id="244b6-188">**Work type:** *Put*</span></span>
    - <span data-ttu-id="244b6-189">**Työluokan tunnus:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="244b6-189">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="244b6-190">Valitse **Tallenna** ja vahvista, että *51 Cross Dock* -mallille on valittu **Kelvollinen** -valintaruutu .</span><span class="sxs-lookup"><span data-stu-id="244b6-190">Select **Save** , and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="244b6-191">*Poiminta* - ja *Hhyllytys* -työtyyppien työluokkien tunnusten on oltava samat.</span><span class="sxs-lookup"><span data-stu-id="244b6-191">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="244b6-192">Luo toimipaikkadirektiivit</span><span class="sxs-lookup"><span data-stu-id="244b6-192">Create location directives</span></span>

1. <span data-ttu-id="244b6-193">Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.</span><span class="sxs-lookup"><span data-stu-id="244b6-193">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="244b6-194">Aseta vasemmassa ruudussa **Työtilaustyyppi** -kentän arvoksi *Cross-docking*.</span><span class="sxs-lookup"><span data-stu-id="244b6-194">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="244b6-195">Valitse toimintoruudussa **Uusi** ja määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="244b6-195">On the Action Pane, select **New** , and set the following values:</span></span>

    - <span data-ttu-id="244b6-196">**Järjestysnumero:** *1*</span><span class="sxs-lookup"><span data-stu-id="244b6-196">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="244b6-197">**Nimi:** *51 Cross Dock Put*</span><span class="sxs-lookup"><span data-stu-id="244b6-197">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="244b6-198">**Työtyyppi:** *Aseta*</span><span class="sxs-lookup"><span data-stu-id="244b6-198">**Work type:** *Put*</span></span>
    - <span data-ttu-id="244b6-199">**Toimipaikka:** *5*</span><span class="sxs-lookup"><span data-stu-id="244b6-199">**Site:** *5*</span></span>
    - <span data-ttu-id="244b6-200">**Varasto** : *51*</span><span class="sxs-lookup"><span data-stu-id="244b6-200">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="244b6-201">Valitse **Tallenna** , jos haluat, että **Rivit** -pikavälilehti on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="244b6-201">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="244b6-202">Lisää uusi rivi ruudukkoon **Rivit** -pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="244b6-202">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="244b6-203">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="244b6-203">On the new line, set the following values:</span></span>

    - <span data-ttu-id="244b6-204">**Määrästä:** *1*</span><span class="sxs-lookup"><span data-stu-id="244b6-204">**From quantity:** *1*</span></span>
    - <span data-ttu-id="244b6-205">**Määrälle:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="244b6-205">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="244b6-206">Valitse **Tallenna** , jos haluat, että **Paikkadirektiivitoimenpiteet** -pikavälilehti on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="244b6-206">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="244b6-207">Lisää uusi rivi ruudukkoon **Sijaintidirektiivin toiminnot** -pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="244b6-207">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="244b6-208">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="244b6-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="244b6-209">**Nimi:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="244b6-209">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="244b6-210">**Kiinteän sijainnin käyttö:** *Kiinteät ja muut kuin kiinteät sijainnit*</span><span class="sxs-lookup"><span data-stu-id="244b6-210">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="244b6-211">Valitse **Tallenna** , jos haluat, että **Sijaintidirektiivin toiminnot** -työkalurivin **Muokkaa kyselyä** -painike on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="244b6-211">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="244b6-212">Avaa kyselyeditori valitsemalla **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="244b6-212">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="244b6-213">Varmista **Alue** -välilehdessä, että seuraavat kaksi riviä on konfiguroitu:</span><span class="sxs-lookup"><span data-stu-id="244b6-213">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="244b6-214">Rivi 1:</span><span class="sxs-lookup"><span data-stu-id="244b6-214">Line 1:</span></span>

        - <span data-ttu-id="244b6-215">**Taulu:** *Sijainnit*</span><span class="sxs-lookup"><span data-stu-id="244b6-215">**Table:** *Locations*</span></span>
        - <span data-ttu-id="244b6-216">**Johdettu taulu:** *Sijainnit*</span><span class="sxs-lookup"><span data-stu-id="244b6-216">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="244b6-217">**Kenttä:** *Varasto*</span><span class="sxs-lookup"><span data-stu-id="244b6-217">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="244b6-218">**Ehdot:** *51*</span><span class="sxs-lookup"><span data-stu-id="244b6-218">**Criteria:** *51*</span></span>

    - <span data-ttu-id="244b6-219">Rivi 2:</span><span class="sxs-lookup"><span data-stu-id="244b6-219">Line 2:</span></span>

        - <span data-ttu-id="244b6-220">**Taulu:** *Sijainnit*</span><span class="sxs-lookup"><span data-stu-id="244b6-220">**Table:** *Locations*</span></span>
        - <span data-ttu-id="244b6-221">**Johdettu taulu:** *Sijainnit*</span><span class="sxs-lookup"><span data-stu-id="244b6-221">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="244b6-222">**Kenttä:** *Sijainti*</span><span class="sxs-lookup"><span data-stu-id="244b6-222">**Field:** *Location*</span></span>
        - <span data-ttu-id="244b6-223">**Kriteerit:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="244b6-223">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="244b6-224">Valitse **OK** sulkeaksesi kyselyeditorin.</span><span class="sxs-lookup"><span data-stu-id="244b6-224">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="244b6-225">Luo mobiililaitteen valikkovaihtoehto</span><span class="sxs-lookup"><span data-stu-id="244b6-225">Create a mobile device menu item</span></span>

1. <span data-ttu-id="244b6-226">Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.</span><span class="sxs-lookup"><span data-stu-id="244b6-226">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="244b6-227">Valitse vasemmanpuoleisen ruudun valikkovaihtoehtojen luettelosta **Oston hyllytys**.</span><span class="sxs-lookup"><span data-stu-id="244b6-227">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="244b6-228">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="244b6-228">Select **Edit**.</span></span>
1. <span data-ttu-id="244b6-229">Lisää uusi rivi ruudukkoon **Työlajit** -pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="244b6-229">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="244b6-230">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="244b6-230">On the new line, set the following values:</span></span>

    - <span data-ttu-id="244b6-231">**Työluokan tunnus:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="244b6-231">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="244b6-232">**Työtilaus tyyppi:** *Cross docking*</span><span class="sxs-lookup"><span data-stu-id="244b6-232">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="244b6-233">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="244b6-233">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="244b6-234">Skenaario</span><span class="sxs-lookup"><span data-stu-id="244b6-234">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="244b6-235">Ostotilauksen luominen</span><span class="sxs-lookup"><span data-stu-id="244b6-235">Create a purchase order</span></span>

<span data-ttu-id="244b6-236">Noudattamalla näitä ohjeita voit luoda ostotilauksen toimituslähteeksi.</span><span class="sxs-lookup"><span data-stu-id="244b6-236">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="244b6-237">Siirry kohtaan **Hankinta ja alihankinta \> Ostotilaukset \> Kaikki ostotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="244b6-237">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="244b6-238">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="244b6-238">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="244b6-239">Aseta **Luo ostotilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="244b6-239">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="244b6-240">**Toimittajan tili:** *104*</span><span class="sxs-lookup"><span data-stu-id="244b6-240">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="244b6-241">**Varasto** : *51*</span><span class="sxs-lookup"><span data-stu-id="244b6-241">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="244b6-242">Valitse **OK** ja kirjoita tilausnumero muistiin.</span><span class="sxs-lookup"><span data-stu-id="244b6-242">Select **OK** , and make a note of the order number.</span></span>
1. <span data-ttu-id="244b6-243">**Ostotilausrivit** -pikavälilehdelle lisätään uusi rivi.</span><span class="sxs-lookup"><span data-stu-id="244b6-243">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="244b6-244">Määritä tälle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="244b6-244">On this line, set the following values:</span></span>

    - <span data-ttu-id="244b6-245">**Nimiketunnus:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="244b6-245">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="244b6-246">**Määrä** *5*</span><span class="sxs-lookup"><span data-stu-id="244b6-246">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="244b6-247">Luo myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="244b6-247">Create a sales order</span></span>

<span data-ttu-id="244b6-248">Noudattamalla näitä ohjeita voit luoda myyntitilauksen kysynnän lähteeksi.</span><span class="sxs-lookup"><span data-stu-id="244b6-248">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="244b6-249">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="244b6-249">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="244b6-250">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="244b6-250">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="244b6-251">Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="244b6-251">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="244b6-252">**Asiakastili:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="244b6-252">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="244b6-253">**Varasto** : *51*</span><span class="sxs-lookup"><span data-stu-id="244b6-253">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="244b6-254">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="244b6-254">Select **OK**.</span></span>
1. <span data-ttu-id="244b6-255">**Myyntitilausrivit** -pikavälilehdelle lisätään uusi rivi.</span><span class="sxs-lookup"><span data-stu-id="244b6-255">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="244b6-256">Määritä tälle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="244b6-256">On this line, set the following values:</span></span>

    - <span data-ttu-id="244b6-257">**Nimiketunnus:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="244b6-257">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="244b6-258">**Määrä** *3*</span><span class="sxs-lookup"><span data-stu-id="244b6-258">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="244b6-259">Luo suunniteltu cross-docking</span><span class="sxs-lookup"><span data-stu-id="244b6-259">Create planned cross-docking</span></span>

<span data-ttu-id="244b6-260">Seuraavien vaiheiden avulla voit luoda suunnitellun cross-dockingin myyntitilauksesta.</span><span class="sxs-lookup"><span data-stu-id="244b6-260">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="244b6-261">Valitse juuri luomasi myynti tilauksen **Myyntitilaustiedot** -sivulta toimenpideruudun **Varasto** -välilehden **Toiminnot** -ryhmästä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="244b6-261">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="244b6-262">Vapauta varastoon -toiminto luo myyntitilausriville lähetys- ja kuormitusrivin sekä yrittää kohdistaa varaston.</span><span class="sxs-lookup"><span data-stu-id="244b6-262">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="244b6-263">Näyttöön avautuu tietosanoma.</span><span class="sxs-lookup"><span data-stu-id="244b6-263">You receive an informational message.</span></span> <span data-ttu-id="244b6-264">Näyttöön tulee myös seuraava varoitussanoma: "Aallolle XXXX ei luotu työtä.</span><span class="sxs-lookup"><span data-stu-id="244b6-264">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="244b6-265">Lisätietoja on työn luonnin historialokissa."</span><span class="sxs-lookup"><span data-stu-id="244b6-265">See the work creation history log for details."</span></span> <span data-ttu-id="244b6-266">Tämä toiminta on odotettavissa, koska varastossa ei ole varastoa.</span><span class="sxs-lookup"><span data-stu-id="244b6-266">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="244b6-267">Valitse **Myyntitilausrivit** -pikavälilehdellä **Varasto** -valikosta **Lähetyksen tiedot**.</span><span class="sxs-lookup"><span data-stu-id="244b6-267">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="244b6-268">Näkyviin tulee **Lähetyksen tiedot** -sivu, jossa näkyy myyntitilaukselle luotu lähetys.</span><span class="sxs-lookup"><span data-stu-id="244b6-268">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="244b6-269">Huomaa, että **Suunniteltu cross-docking-määrä** -kentän arvo on *3* **Lataa rivit** -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="244b6-269">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="244b6-270">Koska varastossa ei ollut käytettävissä varastoa, mutta voimassa oleva toimituslähde saapuu cross-docking-mallissa määritettyyn aikaikkunaan, cross-docking-määrä on luotu.</span><span class="sxs-lookup"><span data-stu-id="244b6-270">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="244b6-271">Voit tarkastella luotuja cross-docking-tietoja valitsemalla **Lataa rivit** -pikavälilehdessä **Suunniteltu cross-docking**.</span><span class="sxs-lookup"><span data-stu-id="244b6-271">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="244b6-272">Prossessoi cross-docking</span><span class="sxs-lookup"><span data-stu-id="244b6-272">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="244b6-273">Ostotilauksen vastaanotto varastoinnin mobiilisovelluksessa</span><span class="sxs-lookup"><span data-stu-id="244b6-273">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="244b6-274">Järjestelmä vastaanottaa ostotilauksesta viiden määrän vastaanottosijaintiin ja luo kaksi työkappaletta.</span><span class="sxs-lookup"><span data-stu-id="244b6-274">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="244b6-275">Ensimmäisen luotavan työtunnuksen **Työtilaustyypin** arvo on *Cross docking* ja se on linkitetty myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="244b6-275">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="244b6-276">Sen määrä on 3 ja se ohjataan lopulliseen lähetyssijaintiin, jotta se voidaan lähettää heti.</span><span class="sxs-lookup"><span data-stu-id="244b6-276">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="244b6-277">Toisen luotavan työtunnuksen **Työtilaustyypin** arvo on *Ostotilaukset* ja se on linkitetty ostotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="244b6-277">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="244b6-278">Sen jäljellä oleva määrä on 2, se ei ollut cross-dockattu ja se ohjataan hyllytyksen varastointiin.</span><span class="sxs-lookup"><span data-stu-id="244b6-278">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="244b6-279">Kirjaudu kannettavaan laitteeseen käyttäjänä varastossa *51*.</span><span class="sxs-lookup"><span data-stu-id="244b6-279">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="244b6-280">Siirry kohtaan **Saapuva \> Oston vastaanotto**.</span><span class="sxs-lookup"><span data-stu-id="244b6-280">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="244b6-281">Syötä **PONum** -kenttään ostotilauksen numero.</span><span class="sxs-lookup"><span data-stu-id="244b6-281">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="244b6-282">Kirjoita **Määrä** -kenttään *5*.</span><span class="sxs-lookup"><span data-stu-id="244b6-282">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="244b6-283">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="244b6-283">Select **OK**.</span></span>
1. <span data-ttu-id="244b6-284">Määritä seuraavalla sivulla **Nimike** -kentän arvoksi *A0001*.</span><span class="sxs-lookup"><span data-stu-id="244b6-284">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="244b6-285">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="244b6-285">Select **OK**.</span></span>
1. <span data-ttu-id="244b6-286">Vahvista seuraavalla sivulla **PONum** -, **Nimike** - ja **Määrä** -arvot valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="244b6-286">On the next page, confirm the **PONum** , **Item** , and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="244b6-287">Näyttöön tulee Työ valmis -sanoma.</span><span class="sxs-lookup"><span data-stu-id="244b6-287">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="244b6-288">Valitse **Peruuta** , jos haluat poistua.</span><span class="sxs-lookup"><span data-stu-id="244b6-288">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="244b6-289">Hyllytys cross-dockingiin ja irtotavaraan</span><span class="sxs-lookup"><span data-stu-id="244b6-289">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="244b6-290">Tällä hetkellä molemmilla työtunnuksilla on sama kohderekisterikilpi.</span><span class="sxs-lookup"><span data-stu-id="244b6-290">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="244b6-291">Jotta voit suorittaa seuraavat vaiheet, sinun on saatava työtunnus ja kohderekisterikilpitunnus.</span><span class="sxs-lookup"><span data-stu-id="244b6-291">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="244b6-292">Voit saada nämä tiedot ostotilausrivin ja myyntitilausrivin työtiedoista.</span><span class="sxs-lookup"><span data-stu-id="244b6-292">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="244b6-293">Vaihtoehtoisesti voit siirtyä kohtaan **Varastonhallinta \> Työ \> Työtiedot** ja suodattaa työt, joissa **Varasto** -arvo on *51*.</span><span class="sxs-lookup"><span data-stu-id="244b6-293">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="244b6-294">Siirry mobiililaitteen **Saapuva \> Ostohyllytys** -kohtaan ja kirjoita työn kohderekisterikilpi.</span><span class="sxs-lookup"><span data-stu-id="244b6-294">On the mobile device, go to **Inbound \> Purchase put-away** , and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="244b6-295">Kirjoita **Tunnus** -kenttään työtietojen kohderekisteritunnus.</span><span class="sxs-lookup"><span data-stu-id="244b6-295">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="244b6-296">Cross-docking-keräyssivulla näkyy keräilysijainti ( *RECV* ), kohderekisterikilpi ( *rekisterikilpi* ), nimike ( *A0001* ) ja määrä ( *3* ).</span><span class="sxs-lookup"><span data-stu-id="244b6-296">The cross-docking pick page shows the picking location ( *RECV* ), target license plate ( *license plate* ), item ( *A0001* ), and quantity ( *3* ).</span></span>

1. <span data-ttu-id="244b6-297">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="244b6-297">Select **OK**.</span></span>
1. <span data-ttu-id="244b6-298">Kirjoita **Kohde-RK** -kenttään sen rekisterikilven tunnus, joka on tarkoitus sijoittaa (cross-dockata) lähetyssijaintiin.</span><span class="sxs-lookup"><span data-stu-id="244b6-298">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="244b6-299">Voit valita haluamasi rekisterikilven tunnuksen.</span><span class="sxs-lookup"><span data-stu-id="244b6-299">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="244b6-300">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="244b6-300">Select **OK**.</span></span>
1. <span data-ttu-id="244b6-301">Kirjoita seuraavalla sivulla **Tunnus** -kenttään kohderekisteritunnus.</span><span class="sxs-lookup"><span data-stu-id="244b6-301">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="244b6-302">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="244b6-302">Select **OK**.</span></span>
1. <span data-ttu-id="244b6-303">Vahvista jäljellä olevan määrän 2 poimintatyö ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="244b6-303">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="244b6-304">Valitse seuraavalla sivulla **Valmis** , kun haluat lopettaa poimintaprosessin ja aloittaa hyllytysprosessin.</span><span class="sxs-lookup"><span data-stu-id="244b6-304">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="244b6-305">Mobiilisovellus esittää sinulle sijainnin ja rekisterikilven, johon kohde sijoitetaan.</span><span class="sxs-lookup"><span data-stu-id="244b6-305">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="244b6-306">Vahvista irtotavaran **Hyllytys** valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="244b6-306">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="244b6-307">Varmista seuraavalla sivulla, että cross-dockingin **Hyllytys** on käytössä valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="244b6-307">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="244b6-308">Näyttöön tulee Työ valmis -sanoma.</span><span class="sxs-lookup"><span data-stu-id="244b6-308">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="244b6-309">Valitse **Peruuta** , jos haluat poistua.</span><span class="sxs-lookup"><span data-stu-id="244b6-309">Select **Cancel** to exit.</span></span>

<span data-ttu-id="244b6-310">Seuraavassa kuvassa näkyy, miten tehty cross-docking-työ saattaa näkyä Microsoft Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="244b6-310">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="244b6-311">![Cross-docking-työ päättynyt](media/PlannedCrossDockingWork.png "Cross-docking-työ päättynyt")</span><span class="sxs-lookup"><span data-stu-id="244b6-311">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>
