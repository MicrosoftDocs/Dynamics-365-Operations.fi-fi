---
title: Suunniteltu cross-docking
description: Tässä ohjeaiheessa kuvataan suunniteltua cross-dockingia, jossa tilauksen edellyttämä varastomäärä ohjataan suoraan vastaanotosta tai luomisesta oikealle lähtevien laiturille tai valmistelualueelle. Saapuvan lähdekoodin koko jäljellä oleva varasto ohjataan oikeaan varastosijaintiin tavallisen hyllytysprosessin kautta.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 11e044e04e05c68af676bf97e6085e9975da5c1d
ms.sourcegitcommit: bef7bd2aac00d7eb837fd275d383b7a5c3f1c1ee
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/19/2021
ms.locfileid: "5911245"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="11345-104">Suunniteltu cross-docking</span><span class="sxs-lookup"><span data-stu-id="11345-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11345-105">Tässä aiheessa kuvataan suunnitellun cross-dockingin lisäasetukset.</span><span class="sxs-lookup"><span data-stu-id="11345-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="11345-106">Cross-docking on varastoprosessi, jossa tilauksen edellyttämä varastomäärä ohjataan suoraan vastaanotosta tai luomisesta oikealle lähtevien laiturille tai valmistelualueelle.</span><span class="sxs-lookup"><span data-stu-id="11345-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="11345-107">Saapuvan lähdekoodin koko jäljellä oleva varasto ohjataan oikeaan varastosijaintiin tavallisen hyllytysprosessin kautta.</span><span class="sxs-lookup"><span data-stu-id="11345-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="11345-108">Cross-dockingin avulla työntekijät ohittavat saapuvan hyllytyksen ja lähtevien nimikkeiden varaston, joka on jo merkitty lähtevälle tilaukselle.</span><span class="sxs-lookup"><span data-stu-id="11345-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="11345-109">Näin ollen varastojen kosketuskertojen määrää vähennetään mahdollisuuksien mukaan.</span><span class="sxs-lookup"><span data-stu-id="11345-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="11345-110">Lisäksi, koska vuorovaikutus järjestelmän kanssa on vähäisempää, fyysisen varastoinnin työn aika- ja tilasäästöt lisääntyvät.</span><span class="sxs-lookup"><span data-stu-id="11345-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="11345-111">Ennen kuin suoritat cross-dockingin, sinun on konfiguroitava uusi cross-docking-malli, jossa on määritetty toimituslähde ja muut cross-docking-vaatimukset.</span><span class="sxs-lookup"><span data-stu-id="11345-111">Before you can run cross-docking, you must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="11345-112">Kun lähtevä tilaus luodaan, rivi täytyy merkitä saman nimikkeen sisältävään saapuvaan tilaukseen.</span><span class="sxs-lookup"><span data-stu-id="11345-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span> <span data-ttu-id="11345-113">Voit valita cross docking -mallista direktiivinkoodikentän samalla tavalla kuin täydennys- ja ostotilauksia määritetään.</span><span class="sxs-lookup"><span data-stu-id="11345-113">You can select the directive code field on the cross-docking template, similar to the way you set up replenishment and purchase orders.</span></span>

<span data-ttu-id="11345-114">Saapuvien tilausten vastaanoton yhteydessä cross-docking-asennus määrittää automaattisesti, että cross-docking on tarpeen, ja luo varasto- ja kuormitustyön tarvittavalle määrälle sijaintidirektiivin asetusten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="11345-114">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="11345-115">Varastotapahtumat *eivät* ole rekisteröimättömiä, kun crossing-dock-työ peruutetaan, vaikka tämän ominaisuuden asetus olisi käytössä varastonhallinnan parametreissa.</span><span class="sxs-lookup"><span data-stu-id="11345-115">Inventory transactions are *not* unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-features"></a><span data-ttu-id="11345-116">Suunnitellun cross-docking-toimintojen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="11345-116">Turn on the planned cross docking features</span></span>

<span data-ttu-id="11345-117">Jos järjestelmäsi ei vielä sisällä tässä aiheessa kuvattuja ominaisuuksia, avaa [Ominaisuuksien hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja ota seuraavat ominaisuudet käyttöön seuraavassa järjestyksessä:</span><span class="sxs-lookup"><span data-stu-id="11345-117">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the following features in the following order:</span></span>

1. <span data-ttu-id="11345-118">*Suunniteltu cross-docking*</span><span class="sxs-lookup"><span data-stu-id="11345-118">*Planned cross docking*</span></span>
1. <span data-ttu-id="11345-119">*Cross docking -mallit ja sijaintidirektiivit*</span><span class="sxs-lookup"><span data-stu-id="11345-119">*Cross docking templates with location directives*</span></span>
    > [!NOTE]
    > <span data-ttu-id="11345-120">Tämän ominaisuuden avulla **direktiivin koodi** kenttä voidaan määrittää cross docking -mallissa samalla tavalla kuin täydennysmallien määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="11345-120">This feature enables the **Directive code** field to be specified on the cross-docking template, similar to the way you set up replenishment templates.</span></span> <span data-ttu-id="11345-121">Tämän ominaisuuden ottaminen käyttöön estää sinua lisäämästä lopullisen *hyllytys* rivin cross-docking-työmalliriveille direktiivinkoodia.</span><span class="sxs-lookup"><span data-stu-id="11345-121">Enabling this feature prevents you from adding a directive code on the cross-docking work template lines for the final *Put* line.</span></span> <span data-ttu-id="11345-122">Näin varmistetaan, että työn luonnin aikana voidaan määrittää lopullinen sijainti, ennen kuin otetaan huomioon työmallit.</span><span class="sxs-lookup"><span data-stu-id="11345-122">This ensures that the final put location can be determined during work creation before considering work templates.</span></span>

## <a name="setup"></a><span data-ttu-id="11345-123">Luo perustiedot</span><span class="sxs-lookup"><span data-stu-id="11345-123">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="11345-124">Lataa kirjausmenetelmät uudelleen</span><span class="sxs-lookup"><span data-stu-id="11345-124">Regenerate load posting methods</span></span>

<span data-ttu-id="11345-125">Suunniteltu cross-docking toteutetaan kuormituksenkirjausmenetelmänä.</span><span class="sxs-lookup"><span data-stu-id="11345-125">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="11345-126">Kun olet määrittänyt toiminnon, menetelmät on luotava uudelleen.</span><span class="sxs-lookup"><span data-stu-id="11345-126">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="11345-127">Valitse **Varastonhallinta \> Asetukset \> Lataa kirjausmenetelmät**.</span><span class="sxs-lookup"><span data-stu-id="11345-127">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="11345-128">Valitse toimintoruudussa **Luo menetelmät uudelleen**.</span><span class="sxs-lookup"><span data-stu-id="11345-128">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="11345-129">Kun uudelleen luominen on suoritettu, näkyviin tulee menetelmä, jonka **menetelmän nimen** arvo on *planCrossDocking*.</span><span class="sxs-lookup"><span data-stu-id="11345-129">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="11345-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="11345-130">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="11345-131">Luo cross-docking-malli</span><span class="sxs-lookup"><span data-stu-id="11345-131">Create a cross-docking template</span></span>

1. <span data-ttu-id="11345-132">Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Cross-docking-mallit**.</span><span class="sxs-lookup"><span data-stu-id="11345-132">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="11345-133">Valitse toimintoruudussa **Uusi** ja luo malli.</span><span class="sxs-lookup"><span data-stu-id="11345-133">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="11345-134">Aseta otsikkorivillä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="11345-134">In the header, set the following values:</span></span>

    - <span data-ttu-id="11345-135">**Järjestys:** *1*</span><span class="sxs-lookup"><span data-stu-id="11345-135">**Sequence:** *1*</span></span>

        <span data-ttu-id="11345-136">Tämä kenttä määrittää, missä järjestyksessä mallit arvioidaan.</span><span class="sxs-lookup"><span data-stu-id="11345-136">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="11345-137">**Cross-docking-mallipohjan tunnus:** *51*</span><span class="sxs-lookup"><span data-stu-id="11345-137">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="11345-138">**Kuvaus:** *Varasto 51*</span><span class="sxs-lookup"><span data-stu-id="11345-138">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="11345-139">**Kysynnänvapautuskäytäntö:** *Ennen toimitusvastaanottoa*</span><span class="sxs-lookup"><span data-stu-id="11345-139">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="11345-140">**Varasto**: *51*</span><span class="sxs-lookup"><span data-stu-id="11345-140">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="11345-141">**Suunnittelu**-pikavälilehden määritys ohjaa mallin toimintaa.</span><span class="sxs-lookup"><span data-stu-id="11345-141">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="11345-142">Määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="11345-142">Set the following values:</span></span>

    - <span data-ttu-id="11345-143">**Tarvevaatimukset:** *Ei mitään*</span><span class="sxs-lookup"><span data-stu-id="11345-143">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="11345-144">Tämä kenttä määrittää kysynnän varaston tarpeet.</span><span class="sxs-lookup"><span data-stu-id="11345-144">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="11345-145">Jos tarve on linkitetty tarjontaan ennen luovutusta, valitse *Merkintä*.</span><span class="sxs-lookup"><span data-stu-id="11345-145">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="11345-146">Jos kysynnän on oltava tilaus-varattu toimitusta vasten ennen julkaisua, valitse *Tilauksen varaus*.</span><span class="sxs-lookup"><span data-stu-id="11345-146">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="11345-147">**Sijaintityyppi:** *Lähetyssijainnit*</span><span class="sxs-lookup"><span data-stu-id="11345-147">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="11345-148">Tässä kentässä määritetään, käyttävätkö cross-docking-työt lähetyksen varastointi-/lataussijainteja vai käytetäänkö sen omia valmistelu-/kuormitussijainteja sijaintidirektiivien avulla.</span><span class="sxs-lookup"><span data-stu-id="11345-148">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="11345-149">**Työmalli:** Jätä tämä kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="11345-149">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="11345-150">Tämä kenttä määrittää työmallin, jota käytetään, kun cross-docking-työtä luodaan.</span><span class="sxs-lookup"><span data-stu-id="11345-150">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="11345-151">**Tarkista uudelleen toimituskuitissa:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="11345-151">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="11345-152">Tämä vaihtoehto määrittää, tuleeko toimitus vahvistaa uudelleen vastaanoton aikana.</span><span class="sxs-lookup"><span data-stu-id="11345-152">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="11345-153">Jos tämän asetuksen arvoksi on määritetty *Kyllä*, sekä enimmäisaikaikkuna että vanhenemispäivien alue tarkistetaan.</span><span class="sxs-lookup"><span data-stu-id="11345-153">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="11345-154">**Direktiivikoodi:** Jätä tämä kenttä tyhjäksi</span><span class="sxs-lookup"><span data-stu-id="11345-154">**Directive code:** Leave this field blank</span></span>

        <span data-ttu-id="11345-155">Tämä vaihtoehto on käytössä *cross docking -malleilla ja sijaintidirektiivi* -toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="11345-155">This option is enabled by the *Cross docking templates with location directives* feature.</span></span> <span data-ttu-id="11345-156">Järjestelmän käyttää sijaintidirektiivejä parhaan paikan määrittämiseen cross-docking varaston siirtämiselle.</span><span class="sxs-lookup"><span data-stu-id="11345-156">The system uses location directives to help determine the best location to move cross-docking inventory to.</span></span> <span data-ttu-id="11345-157">Voit määrittää sen määrittämällä jokaiselle asiaankuuluvalle cross-docking-mallille direktiivikoodin.</span><span class="sxs-lookup"><span data-stu-id="11345-157">You can set it up by assigning a directive code to each relevant cross-docking template.</span></span> <span data-ttu-id="11345-158">Jos direktiivikoodi on määritetty, järjestelmä etsii sijaintidirektiivit direktiivikoodin perusteella, kun työ luodaan.</span><span class="sxs-lookup"><span data-stu-id="11345-158">If a directive code is set, the system will search location directives by directive code when work is generated.</span></span> <span data-ttu-id="11345-159">Näin voit rajata tietyssä cross docking -mallissa käytettävät sijaintiohjeet.</span><span class="sxs-lookup"><span data-stu-id="11345-159">In this way, you can limit location directives that are used for a particular cross-docking template.</span></span>

    - <span data-ttu-id="11345-160">**Vahvista aikaikkuna:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="11345-160">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="11345-161">Tämä vaihtoehto määrittää, arvioidaanko enimmäisaikaikkuna, kun toimituslähde valitaan.</span><span class="sxs-lookup"><span data-stu-id="11345-161">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="11345-162">Jos tämän asetuksen arvoksi on määritetty *Kyllä*, järjestelmän enimmäis- ja vähimmäisaikakenttiin liittyvät kentät ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="11345-162">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="11345-163">**Enimmäisaikaikkuna** *5*</span><span class="sxs-lookup"><span data-stu-id="11345-163">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="11345-164">Tämä kenttä määrittää enimmäisajan, joka on sallittu toimitusten saapumisen ja kysynnän poistumisen välillä.</span><span class="sxs-lookup"><span data-stu-id="11345-164">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="11345-165">**Enimmäisaikaikkunayksikkö:** *Päivät*</span><span class="sxs-lookup"><span data-stu-id="11345-165">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="11345-166">**Vähimmäisaikaikkuna** *0*</span><span class="sxs-lookup"><span data-stu-id="11345-166">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="11345-167">Tämä kenttä määrittää vähimmäisajan, joka on sallittu toimitusten saapumisen ja kysynnän poistumisen välillä.</span><span class="sxs-lookup"><span data-stu-id="11345-167">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="11345-168">**Vähimmäisaikaikkunayksikkö:** *Päivät*</span><span class="sxs-lookup"><span data-stu-id="11345-168">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="11345-169">**Voimassaolon päättymisalue päivissä** *0*</span><span class="sxs-lookup"><span data-stu-id="11345-169">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="11345-170">*Ensimmäinen päättymispäivä (FEFO) -ehto:* Tässä kentässä määritetään varastossa tällä hetkellä olevan ensimmäisen vanhentumiserän vanhentumispäivämäärän ja vastaanotetun erän välinen päivien enimmäismäärä.</span><span class="sxs-lookup"><span data-stu-id="11345-170">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="11345-171">**Toimituslähteet**-pikavälilehdessä voit määrittää tämän mallin käytettävissä olevat toimituslajit.</span><span class="sxs-lookup"><span data-stu-id="11345-171">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="11345-172">Valitse **Uusi** ja määritä sitten seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="11345-172">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="11345-173">**Järjestysnumero:** *1*</span><span class="sxs-lookup"><span data-stu-id="11345-173">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="11345-174">**Toimituslähde:** *Ostotilaus*</span><span class="sxs-lookup"><span data-stu-id="11345-174">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="11345-175">Työluokan luominen</span><span class="sxs-lookup"><span data-stu-id="11345-175">Create a work class</span></span>

1. <span data-ttu-id="11345-176">Valitse **Varastonhallinta \> Asetukset \> Työ \> Työluokka**.</span><span class="sxs-lookup"><span data-stu-id="11345-176">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="11345-177">Valitse toimintoruudussa **Uusi** ja luo työluokka.</span><span class="sxs-lookup"><span data-stu-id="11345-177">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="11345-178">Määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="11345-178">Set the following values:</span></span>

    - <span data-ttu-id="11345-179">**Työluokan tunnus:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="11345-179">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="11345-180">**Kuvaus:** *Cross Dock*</span><span class="sxs-lookup"><span data-stu-id="11345-180">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="11345-181">**Työtilaus tyyppi:** *Cross docking*</span><span class="sxs-lookup"><span data-stu-id="11345-181">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="11345-182">Luo työmalli</span><span class="sxs-lookup"><span data-stu-id="11345-182">Create a work template</span></span>

1. <span data-ttu-id="11345-183">Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työmallit**.</span><span class="sxs-lookup"><span data-stu-id="11345-183">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="11345-184">Aseta **Työtilaustyyppi**-kentän arvoksi *Cross-docking*.</span><span class="sxs-lookup"><span data-stu-id="11345-184">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="11345-185">Lisää **Yleiskuvaus**-välilehdelle uusi rivi valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="11345-185">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="11345-186">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="11345-186">On the new line, set the following values:</span></span>

    - <span data-ttu-id="11345-187">**Järjestysnumero:** *1*</span><span class="sxs-lookup"><span data-stu-id="11345-187">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="11345-188">**Työmalli:** *51 Cross Dock*</span><span class="sxs-lookup"><span data-stu-id="11345-188">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="11345-189">**Työmallin kuvaus:** *51 Cross Dock*</span><span class="sxs-lookup"><span data-stu-id="11345-189">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="11345-190">Valitse **Tallenna**, jos haluat, että **Työmallin tiedot** -pikavälilehti on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="11345-190">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="11345-191">Lisää uusi rivi ruudukkoon **Työmallin tiedot** -pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="11345-191">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="11345-192">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="11345-192">On the new line, set the following values:</span></span>

    - <span data-ttu-id="11345-193">**Työtyyppi:** *Poiminta*</span><span class="sxs-lookup"><span data-stu-id="11345-193">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="11345-194">**Työluokan tunnus:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="11345-194">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="11345-195">Lisää toinen rivi valitsemalla **Uusi** ja määritä sille seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="11345-195">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="11345-196">**Työtyyppi:** *Aseta*</span><span class="sxs-lookup"><span data-stu-id="11345-196">**Work type:** *Put*</span></span>
    - <span data-ttu-id="11345-197">**Työluokan tunnus:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="11345-197">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="11345-198">Valitse **Tallenna** ja vahvista, että *51 Cross Dock* -mallille on valittu **Kelvollinen**-valintaruutu .</span><span class="sxs-lookup"><span data-stu-id="11345-198">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="11345-199">*Poiminta*- ja *Hhyllytys*-työtyyppien työluokkien tunnusten on oltava samat.</span><span class="sxs-lookup"><span data-stu-id="11345-199">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="11345-200">Luo toimipaikkadirektiivit</span><span class="sxs-lookup"><span data-stu-id="11345-200">Create location directives</span></span>

1. <span data-ttu-id="11345-201">Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.</span><span class="sxs-lookup"><span data-stu-id="11345-201">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="11345-202">Aseta vasemmassa ruudussa **Työtilaustyyppi**-kentän arvoksi *Cross-docking*.</span><span class="sxs-lookup"><span data-stu-id="11345-202">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="11345-203">Valitse toimintoruudussa **Uusi** ja määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="11345-203">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="11345-204">**Järjestysnumero:** *1*</span><span class="sxs-lookup"><span data-stu-id="11345-204">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="11345-205">**Nimi:** *51 Cross Dock Put*</span><span class="sxs-lookup"><span data-stu-id="11345-205">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="11345-206">**Työtyyppi:** *Aseta*</span><span class="sxs-lookup"><span data-stu-id="11345-206">**Work type:** *Put*</span></span>
    - <span data-ttu-id="11345-207">**Toimipaikka:** *5*</span><span class="sxs-lookup"><span data-stu-id="11345-207">**Site:** *5*</span></span>
    - <span data-ttu-id="11345-208">**Varasto**: *51*</span><span class="sxs-lookup"><span data-stu-id="11345-208">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="11345-209">Valitse **Tallenna**, jos haluat, että **Rivit**-pikavälilehti on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="11345-209">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="11345-210">Lisää uusi rivi ruudukkoon **Rivit**-pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="11345-210">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="11345-211">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="11345-211">On the new line, set the following values:</span></span>

    - <span data-ttu-id="11345-212">**Määrästä:** *1*</span><span class="sxs-lookup"><span data-stu-id="11345-212">**From quantity:** *1*</span></span>
    - <span data-ttu-id="11345-213">**Määrälle:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="11345-213">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="11345-214">Valitse **Tallenna**, jos haluat, että **Paikkadirektiivitoimenpiteet**-pikavälilehti on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="11345-214">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="11345-215">Lisää uusi rivi ruudukkoon **Sijaintidirektiivin toiminnot** -pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="11345-215">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="11345-216">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="11345-216">On the new line, set the following values:</span></span>

    - <span data-ttu-id="11345-217">**Nimi:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="11345-217">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="11345-218">**Kiinteän sijainnin käyttö:** *Kiinteät ja muut kuin kiinteät sijainnit*</span><span class="sxs-lookup"><span data-stu-id="11345-218">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="11345-219">Valitse **Tallenna**, jos haluat, että **Sijaintidirektiivin toiminnot** -työkalurivin **Muokkaa kyselyä** -painike on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="11345-219">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="11345-220">Avaa kyselyeditori valitsemalla **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="11345-220">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="11345-221">Varmista **Alue** -välilehdessä, että seuraavat kaksi riviä on konfiguroitu:</span><span class="sxs-lookup"><span data-stu-id="11345-221">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="11345-222">Rivi 1:</span><span class="sxs-lookup"><span data-stu-id="11345-222">Line 1:</span></span>

        - <span data-ttu-id="11345-223">**Taulu:** *Sijainnit*</span><span class="sxs-lookup"><span data-stu-id="11345-223">**Table:** *Locations*</span></span>
        - <span data-ttu-id="11345-224">**Johdettu taulu:** *Sijainnit*</span><span class="sxs-lookup"><span data-stu-id="11345-224">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="11345-225">**Kenttä:** *Varasto*</span><span class="sxs-lookup"><span data-stu-id="11345-225">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="11345-226">**Ehdot:** *51*</span><span class="sxs-lookup"><span data-stu-id="11345-226">**Criteria:** *51*</span></span>

    - <span data-ttu-id="11345-227">Rivi 2:</span><span class="sxs-lookup"><span data-stu-id="11345-227">Line 2:</span></span>

        - <span data-ttu-id="11345-228">**Taulu:** *Sijainnit*</span><span class="sxs-lookup"><span data-stu-id="11345-228">**Table:** *Locations*</span></span>
        - <span data-ttu-id="11345-229">**Johdettu taulu:** *Sijainnit*</span><span class="sxs-lookup"><span data-stu-id="11345-229">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="11345-230">**Kenttä:** *Sijainti*</span><span class="sxs-lookup"><span data-stu-id="11345-230">**Field:** *Location*</span></span>
        - <span data-ttu-id="11345-231">**Kriteerit:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="11345-231">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="11345-232">Valitse **OK** sulkeaksesi kyselyeditorin.</span><span class="sxs-lookup"><span data-stu-id="11345-232">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="11345-233">Luo mobiililaitteen valikkovaihtoehto</span><span class="sxs-lookup"><span data-stu-id="11345-233">Create a mobile device menu item</span></span>

1. <span data-ttu-id="11345-234">Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.</span><span class="sxs-lookup"><span data-stu-id="11345-234">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="11345-235">Valitse vasemmanpuoleisen ruudun valikkovaihtoehtojen luettelosta **Oston hyllytys**.</span><span class="sxs-lookup"><span data-stu-id="11345-235">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="11345-236">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="11345-236">Select **Edit**.</span></span>
1. <span data-ttu-id="11345-237">Lisää uusi rivi ruudukkoon **Työlajit**-pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="11345-237">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="11345-238">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="11345-238">On the new line, set the following values:</span></span>

    - <span data-ttu-id="11345-239">**Työluokan tunnus:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="11345-239">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="11345-240">**Työtilaus tyyppi:** *Cross docking*</span><span class="sxs-lookup"><span data-stu-id="11345-240">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="11345-241">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="11345-241">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="11345-242">Skenaario</span><span class="sxs-lookup"><span data-stu-id="11345-242">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="11345-243">Ostotilauksen luominen</span><span class="sxs-lookup"><span data-stu-id="11345-243">Create a purchase order</span></span>

<span data-ttu-id="11345-244">Noudattamalla näitä ohjeita voit luoda ostotilauksen toimituslähteeksi.</span><span class="sxs-lookup"><span data-stu-id="11345-244">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="11345-245">Siirry kohtaan **Hankinta ja alihankinta \> Ostotilaukset \> Kaikki ostotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="11345-245">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="11345-246">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="11345-246">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="11345-247">Aseta **Luo ostotilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="11345-247">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="11345-248">**Toimittajan tili:** *104*</span><span class="sxs-lookup"><span data-stu-id="11345-248">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="11345-249">**Varasto**: *51*</span><span class="sxs-lookup"><span data-stu-id="11345-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="11345-250">Valitse **OK** ja kirjoita tilausnumero muistiin.</span><span class="sxs-lookup"><span data-stu-id="11345-250">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="11345-251">**Ostotilausrivit**-pikavälilehdelle lisätään uusi rivi.</span><span class="sxs-lookup"><span data-stu-id="11345-251">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="11345-252">Määritä tälle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="11345-252">On this line, set the following values:</span></span>

    - <span data-ttu-id="11345-253">**Nimiketunnus:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="11345-253">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="11345-254">**Määrä** *5*</span><span class="sxs-lookup"><span data-stu-id="11345-254">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="11345-255">Luo myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="11345-255">Create a sales order</span></span>

<span data-ttu-id="11345-256">Noudattamalla näitä ohjeita voit luoda myyntitilauksen kysynnän lähteeksi.</span><span class="sxs-lookup"><span data-stu-id="11345-256">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="11345-257">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="11345-257">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="11345-258">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="11345-258">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="11345-259">Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="11345-259">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="11345-260">**Asiakastili:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="11345-260">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="11345-261">**Varasto**: *51*</span><span class="sxs-lookup"><span data-stu-id="11345-261">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="11345-262">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="11345-262">Select **OK**.</span></span>
1. <span data-ttu-id="11345-263">**Myyntitilausrivit**-pikavälilehdelle lisätään uusi rivi.</span><span class="sxs-lookup"><span data-stu-id="11345-263">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="11345-264">Määritä tälle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="11345-264">On this line, set the following values:</span></span>

    - <span data-ttu-id="11345-265">**Nimiketunnus:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="11345-265">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="11345-266">**Määrä** *3*</span><span class="sxs-lookup"><span data-stu-id="11345-266">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="11345-267">Luo suunniteltu cross-docking</span><span class="sxs-lookup"><span data-stu-id="11345-267">Create planned cross-docking</span></span>

<span data-ttu-id="11345-268">Seuraavien vaiheiden avulla voit luoda suunnitellun cross-dockingin myyntitilauksesta.</span><span class="sxs-lookup"><span data-stu-id="11345-268">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="11345-269">Valitse juuri luomasi myynti tilauksen **Myyntitilaustiedot** -sivulta toimenpideruudun **Varasto**-välilehden **Toiminnot**-ryhmästä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="11345-269">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="11345-270">Vapauta varastoon -toiminto luo myyntitilausriville lähetys- ja kuormitusrivin sekä yrittää kohdistaa varaston.</span><span class="sxs-lookup"><span data-stu-id="11345-270">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="11345-271">Näyttöön avautuu tietosanoma.</span><span class="sxs-lookup"><span data-stu-id="11345-271">You receive an informational message.</span></span> <span data-ttu-id="11345-272">Näyttöön tulee myös seuraava varoitussanoma: "Aallolle XXXX ei luotu työtä.</span><span class="sxs-lookup"><span data-stu-id="11345-272">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="11345-273">Lisätietoja on työn luonnin historialokissa."</span><span class="sxs-lookup"><span data-stu-id="11345-273">See the work creation history log for details."</span></span> <span data-ttu-id="11345-274">Tämä toiminta on odotettavissa, koska varastossa ei ole varastoa.</span><span class="sxs-lookup"><span data-stu-id="11345-274">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="11345-275">Valitse **Myyntitilausrivit**-pikavälilehdellä **Varasto**-valikosta **Lähetyksen tiedot**.</span><span class="sxs-lookup"><span data-stu-id="11345-275">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="11345-276">Näkyviin tulee **Lähetyksen tiedot** -sivu, jossa näkyy myyntitilaukselle luotu lähetys.</span><span class="sxs-lookup"><span data-stu-id="11345-276">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="11345-277">Huomaa, että **Suunniteltu cross-docking-määrä** -kentän arvo on *3* **Lataa rivit** -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="11345-277">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="11345-278">Koska varastossa ei ollut käytettävissä varastoa, mutta voimassa oleva toimituslähde saapuu cross-docking-mallissa määritettyyn aikaikkunaan, cross-docking-määrä on luotu.</span><span class="sxs-lookup"><span data-stu-id="11345-278">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="11345-279">Voit tarkastella luotuja cross-docking-tietoja valitsemalla **Lataa rivit** -pikavälilehdessä **Suunniteltu cross-docking**.</span><span class="sxs-lookup"><span data-stu-id="11345-279">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="11345-280">Prossessoi cross-docking</span><span class="sxs-lookup"><span data-stu-id="11345-280">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="11345-281">Ostotilauksen vastaanotto varastoinnin mobiilisovelluksessa</span><span class="sxs-lookup"><span data-stu-id="11345-281">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="11345-282">Järjestelmä vastaanottaa ostotilauksesta viiden määrän vastaanottosijaintiin ja luo kaksi työkappaletta.</span><span class="sxs-lookup"><span data-stu-id="11345-282">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="11345-283">Ensimmäisen luotavan työtunnuksen **Työtilaustyypin** arvo on *Cross docking* ja se on linkitetty myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="11345-283">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="11345-284">Sen määrä on 3 ja se ohjataan lopulliseen lähetyssijaintiin, jotta se voidaan lähettää heti.</span><span class="sxs-lookup"><span data-stu-id="11345-284">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="11345-285">Toisen luotavan työtunnuksen **Työtilaustyypin** arvo on *Ostotilaukset* ja se on linkitetty ostotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="11345-285">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="11345-286">Sen jäljellä oleva määrä on 2, se ei ollut cross-dockattu ja se ohjataan hyllytyksen varastointiin.</span><span class="sxs-lookup"><span data-stu-id="11345-286">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="11345-287">Kirjaudu kannettavaan laitteeseen käyttäjänä varastossa *51*.</span><span class="sxs-lookup"><span data-stu-id="11345-287">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="11345-288">Siirry kohtaan **Saapuva \> Oston vastaanotto**.</span><span class="sxs-lookup"><span data-stu-id="11345-288">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="11345-289">Syötä **PONum**-kenttään ostotilauksen numero.</span><span class="sxs-lookup"><span data-stu-id="11345-289">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="11345-290">Kirjoita **Määrä**-kenttään *5*.</span><span class="sxs-lookup"><span data-stu-id="11345-290">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="11345-291">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="11345-291">Select **OK**.</span></span>
1. <span data-ttu-id="11345-292">Määritä seuraavalla sivulla **Nimike**-kentän arvoksi *A0001*.</span><span class="sxs-lookup"><span data-stu-id="11345-292">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="11345-293">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="11345-293">Select **OK**.</span></span>
1. <span data-ttu-id="11345-294">Vahvista seuraavalla sivulla **PONum**-, **Nimike**- ja **Määrä**-arvot valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="11345-294">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="11345-295">Näyttöön tulee Työ valmis -sanoma.</span><span class="sxs-lookup"><span data-stu-id="11345-295">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="11345-296">Valitse **Peruuta**, jos haluat poistua.</span><span class="sxs-lookup"><span data-stu-id="11345-296">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="11345-297">Hyllytys cross-dockingiin ja irtotavaraan</span><span class="sxs-lookup"><span data-stu-id="11345-297">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="11345-298">Tällä hetkellä molemmilla työtunnuksilla on sama kohderekisterikilpi.</span><span class="sxs-lookup"><span data-stu-id="11345-298">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="11345-299">Jotta voit suorittaa seuraavat vaiheet, sinun on saatava työtunnus ja kohderekisterikilpitunnus.</span><span class="sxs-lookup"><span data-stu-id="11345-299">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="11345-300">Voit saada nämä tiedot ostotilausrivin ja myyntitilausrivin työtiedoista.</span><span class="sxs-lookup"><span data-stu-id="11345-300">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="11345-301">Vaihtoehtoisesti voit siirtyä kohtaan **Varastonhallinta \> Työ \> Työtiedot** ja suodattaa työt, joissa **Varasto**-arvo on *51*.</span><span class="sxs-lookup"><span data-stu-id="11345-301">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="11345-302">Siirry mobiililaitteen **Saapuva \> Ostohyllytys**-kohtaan ja kirjoita työn kohderekisterikilpi.</span><span class="sxs-lookup"><span data-stu-id="11345-302">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="11345-303">Kirjoita **Tunnus**-kenttään työtietojen kohderekisteritunnus.</span><span class="sxs-lookup"><span data-stu-id="11345-303">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="11345-304">Cross-docking-keräyssivulla näkyy keräilysijainti (*RECV*), kohderekisterikilpi (*rekisterikilpi*), nimike (*A0001*) ja määrä (*3*).</span><span class="sxs-lookup"><span data-stu-id="11345-304">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="11345-305">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="11345-305">Select **OK**.</span></span>
1. <span data-ttu-id="11345-306">Kirjoita **Kohde-RK**-kenttään sen rekisterikilven tunnus, joka on tarkoitus sijoittaa (cross-dockata) lähetyssijaintiin.</span><span class="sxs-lookup"><span data-stu-id="11345-306">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="11345-307">Voit valita haluamasi rekisterikilven tunnuksen.</span><span class="sxs-lookup"><span data-stu-id="11345-307">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="11345-308">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="11345-308">Select **OK**.</span></span>
1. <span data-ttu-id="11345-309">Kirjoita seuraavalla sivulla **Tunnus**-kenttään kohderekisteritunnus.</span><span class="sxs-lookup"><span data-stu-id="11345-309">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="11345-310">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="11345-310">Select **OK**.</span></span>
1. <span data-ttu-id="11345-311">Vahvista jäljellä olevan määrän 2 poimintatyö ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="11345-311">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="11345-312">Valitse seuraavalla sivulla **Valmis**, kun haluat lopettaa poimintaprosessin ja aloittaa hyllytysprosessin.</span><span class="sxs-lookup"><span data-stu-id="11345-312">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="11345-313">Mobiilisovellus esittää sinulle sijainnin ja rekisterikilven, johon kohde sijoitetaan.</span><span class="sxs-lookup"><span data-stu-id="11345-313">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="11345-314">Vahvista irtotavaran **Hyllytys** valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="11345-314">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="11345-315">Varmista seuraavalla sivulla, että cross-dockingin **Hyllytys** on käytössä valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="11345-315">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="11345-316">Näyttöön tulee Työ valmis -sanoma.</span><span class="sxs-lookup"><span data-stu-id="11345-316">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="11345-317">Valitse **Peruuta**, jos haluat poistua.</span><span class="sxs-lookup"><span data-stu-id="11345-317">Select **Cancel** to exit.</span></span>

<span data-ttu-id="11345-318">Seuraavassa kuvassa näkyy, miten tehty cross-docking-työ saattaa näkyä Microsoft Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="11345-318">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="11345-319">![Cross-docking-työ päättynyt](media/PlannedCrossDockingWork.png "Cross-docking-työ päättynyt")</span><span class="sxs-lookup"><span data-stu-id="11345-319">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]