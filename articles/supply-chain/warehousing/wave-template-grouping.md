---
title: Aallon mallipohjan ryhmittely
description: Aaltomalliryhmityksen avulla järjestelmä voi käyttää aaltomalliasetelmia määrittämään, perustuen määrittämiisi kriteereihin miten se pitäisi jakaa vapautetut rivit ja liittää ne uusiin tai olemassa oleviin aaltoihin. Tämä ominaisuus voi olla hyödyllinen varastoissa, joissa aallot luodaan tiettyjen kriteerien perusteella, mutta jossa esimiehet luovat mieluummin aallot automaattisesti manuaalisen sijaan.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 520338683443105ffd1df7fc2569cd95a5f50879
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245127"
---
# <a name="wave-template-grouping"></a><span data-ttu-id="5099f-104">Aallon mallipohjan ryhmittely</span><span class="sxs-lookup"><span data-stu-id="5099f-104">Wave template grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5099f-105">Aaltomalliryhmityksen avulla järjestelmä voi käyttää [aaltomalli](tasks/configure-wave-processing.md)-asetelmia määrittämään, perustuen määrittämiisi kriteereihin miten se pitäisi jakaa vapautetut rivit ja liittää ne uusiin tai olemassa oleviin aaltoihin.</span><span class="sxs-lookup"><span data-stu-id="5099f-105">Wave template grouping enables the system to use [wave template](tasks/configure-wave-processing.md) setups to determine, based on criteria that you define, how it should split released lines and assign them to new or existing waves.</span></span> <span data-ttu-id="5099f-106">Tämä ominaisuus voi olla hyödyllinen varastoissa, joissa aallot luodaan tiettyjen kriteerien perusteella, mutta jossa esimiehet luovat mieluummin aallot automaattisesti manuaalisen sijaan.</span><span class="sxs-lookup"><span data-stu-id="5099f-106">This feature can be useful in warehouses where waves are created based on specific criteria, but where managers prefer to create waves automatically instead of manually.</span></span> <span data-ttu-id="5099f-107">Sen avulla järjestelmä voi lisätä jokaisen vastikään vapautetun lähetyksen ensimmäiseen aaltoon, joka havaitsee, että se vastaa ryhmittelykenttien arvoja.</span><span class="sxs-lookup"><span data-stu-id="5099f-107">It enables the system to add each newly released shipment to the first wave that it finds that has matching grouping field values.</span></span> <span data-ttu-id="5099f-108">Jos vastaavuutta ei löydy, järjestelmä luo uudelle siirrolle uuden aallon.</span><span class="sxs-lookup"><span data-stu-id="5099f-108">If no match is found, the system creates a new wave for the new shipment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5099f-109">Aaltomallin ryhmittelyä ei tueta *tuotannon raaka-aineiden keräily*- tai *Kanban-keräily*-työtyypeille.</span><span class="sxs-lookup"><span data-stu-id="5099f-109">Wave template grouping isn't supported for the work types *production raw material picking* or *Kanban picking*.</span></span> <span data-ttu-id="5099f-110">Tämä johtuu siitä, että aaltoryhmittely perustuu toimituksiin, eivätkä nämä työlajit käytä toimituksia.</span><span class="sxs-lookup"><span data-stu-id="5099f-110">This is because wave grouping is based on shipments and these work types don't use shipments.</span></span>

## <a name="turn-on-the-wave-template-grouping-feature"></a><span data-ttu-id="5099f-111">Aaltomallin ryhmittelytoiminnon ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="5099f-111">Turn on the Wave template grouping feature</span></span>

<span data-ttu-id="5099f-112">Ennen kuin voit käyttää *Aaltomallin ryhmittely* -toimintoa, sen pitää olla otettu käyttöön järjestelmässäsi.</span><span class="sxs-lookup"><span data-stu-id="5099f-112">Before you can use the *Wave template grouping* feature, it must be turned on in your system.</span></span> <span data-ttu-id="5099f-113">Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön, jos sitä vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="5099f-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="5099f-114">**Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="5099f-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="5099f-115">**Moduuli:** *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="5099f-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="5099f-116">**Toiminnon nimi:** *Aaltomallin ryhmittely*</span><span class="sxs-lookup"><span data-stu-id="5099f-116">**Feature name:** *Wave template grouping*</span></span>

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a><span data-ttu-id="5099f-117">Aaltomallin määrittäminen käyttämään aaltomallin ryhmittelyä</span><span class="sxs-lookup"><span data-stu-id="5099f-117">Set a wave template to use wave template grouping</span></span>

<span data-ttu-id="5099f-118">Voit määrittää aaltomalliryhmittelyn seuraavien [aaltomalli](tasks/configure-wave-processing.md)-ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="5099f-118">To make wave template grouping available, follow these steps to set up your [wave template](tasks/configure-wave-processing.md).</span></span>

1. <span data-ttu-id="5099f-119">Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aaltomallit**.</span><span class="sxs-lookup"><span data-stu-id="5099f-119">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="5099f-120">Valitse vasemmasta ruudusta aaltomalli, jonka haluat määrittää.</span><span class="sxs-lookup"><span data-stu-id="5099f-120">In the left pane, select the wave template to set up.</span></span> <span data-ttu-id="5099f-121">Jos valmistelet työskentelyä tämän ohjeaiheen mukaan myöhemmin tässä aiheessa käyttämällä demotietoja, valitse **62 toimituksen oletus** -malli.</span><span class="sxs-lookup"><span data-stu-id="5099f-121">If you're preparing to work through the scenario later in this topic by using demo data, select the **62 Shipping default** template.</span></span>
1. <span data-ttu-id="5099f-122">Valitse **Muokkaa**, jotta saat sivun muokkaustilaan.</span><span class="sxs-lookup"><span data-stu-id="5099f-122">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="5099f-123">Määritä **Yleiset**-pikavälilehdessä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="5099f-123">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="5099f-124">**Automatisoi aallonluonti:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="5099f-124">**Automate wave creation:** *Yes*</span></span>
    - <span data-ttu-id="5099f-125">**Määritä avoimiin aaltoihin:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="5099f-125">**Assign to open waves:** *Yes*</span></span>
    - <span data-ttu-id="5099f-126">**Käsittele aalto, kun se vapautetaan varastoon:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="5099f-126">**Process wave at release to warehouse:** *No*</span></span>

1. <span data-ttu-id="5099f-127">Valitse toimintoruudussa **Muokkaa kyselyä**, jotta voit avata kyselyvalintaikkunan.</span><span class="sxs-lookup"><span data-stu-id="5099f-127">On the Action Pane, select **Edit query** to open the query dialog box.</span></span>
1. <span data-ttu-id="5099f-128">Tarkista lajitteluehdot kyselyvalintaikkunan **Lajittelu**-välilehdessä ja varmista, että sääntö sisältää kentän, jota haluat käyttää aaltojen ryhmittelemiseen.</span><span class="sxs-lookup"><span data-stu-id="5099f-128">In the query dialog box, on the **Sorting** tab, review the sorting criteria, and make sure that there is a rule that includes the field that you want to use to group your waves.</span></span>

    <span data-ttu-id="5099f-129">Jos valmistelet toimintaskenaarion käyttöä demotietojen avulla, lisää rivi, jolla on seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="5099f-129">If you're preparing to work through the scenario by using demo data, add a row that has the following values:</span></span>

    - <span data-ttu-id="5099f-130">**Taulukko:** *Lähetykset*</span><span class="sxs-lookup"><span data-stu-id="5099f-130">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="5099f-131">**Johdettu taulu:** *Lähetykset*</span><span class="sxs-lookup"><span data-stu-id="5099f-131">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="5099f-132">**Kenttä:** *Rahdinkuljetuspalvelu*</span><span class="sxs-lookup"><span data-stu-id="5099f-132">**Field:** *Carrier service*</span></span>

        > [!NOTE]
        > <span data-ttu-id="5099f-133">Kun olet valinnut tämän arvon, näyttöön saattaa tulla seuraava sanoma: "Rahdinkuljetuspalvelukenttä ei ole indeksikenttä.</span><span class="sxs-lookup"><span data-stu-id="5099f-133">After you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="5099f-134">Haluatko lisätä lajittelun tähän? "</span><span class="sxs-lookup"><span data-stu-id="5099f-134">Do you want to add sorting on this?"</span></span> <span data-ttu-id="5099f-135">Lisää lajittelu valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="5099f-135">Select **Yes** to add sorting.</span></span>

    - <span data-ttu-id="5099f-136">**Hakusuunta:** *Laskeva*</span><span class="sxs-lookup"><span data-stu-id="5099f-136">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="5099f-137">Valitse **OK**, tallenna muutokset ja sulje kyselyvalintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="5099f-137">Select **OK** to save your changes and close the query dialog box.</span></span>
1. <span data-ttu-id="5099f-138">Valitse Toimintoruudussa **Aaltomallinryhmittely**.</span><span class="sxs-lookup"><span data-stu-id="5099f-138">On the Action Pane, select **Wave template grouping**.</span></span>
1. <span data-ttu-id="5099f-139">Valitse **Aaltomallin ryhmittely** -sivulla **Ryhmän mukaan** -valintaruutu jokaiselle riville, jota haluat käyttää tilausrivien ryhmittelyyn tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="5099f-139">On the **Wave template grouping** page, select the **Group by** check box for each row that you want to use to group your order lines into waves, as required.</span></span> <span data-ttu-id="5099f-140">Jos valmistelet skenaarion käyttöä demotietojen avulla, valitse *Rahdinkuljetuspalvelu*-rivin **Ryhmittele**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="5099f-140">If you're preparing to work through the scenario by using demo data, select the **Group by** check box for the *Carrier service* row.</span></span>
1. <span data-ttu-id="5099f-141">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="5099f-141">Select **Save**.</span></span>
1. <span data-ttu-id="5099f-142">Lopeta **Aaltomallin ryhmittely** -sivu.</span><span class="sxs-lookup"><span data-stu-id="5099f-142">Close the **Wave template grouping** page.</span></span>
1. <span data-ttu-id="5099f-143">Tallenna mallit valitsemalla **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="5099f-143">Select **Save** to save your template.</span></span>

## <a name="scenario"></a><span data-ttu-id="5099f-144">Skenaario</span><span class="sxs-lookup"><span data-stu-id="5099f-144">Scenario</span></span>

<span data-ttu-id="5099f-145">Tässä osassa on skripti, jonka avulla voit selvittää, mitä toiminto tekee ja miten sitä käytetään.</span><span class="sxs-lookup"><span data-stu-id="5099f-145">This section provides a script that you can work through to learn what this feature does and how to work with it.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="5099f-146">Ota mallitiedot käyttöön</span><span class="sxs-lookup"><span data-stu-id="5099f-146">Make sample data available</span></span>

<span data-ttu-id="5099f-147">Tämän skenaarion käyttäminen tässä määritettyjen mallitietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon vakio-[demotiedot](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) on asennettu.</span><span class="sxs-lookup"><span data-stu-id="5099f-147">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="5099f-148">Sinun on myös valittava **USMF**-yritys ennen kuin aloitat.</span><span class="sxs-lookup"><span data-stu-id="5099f-148">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="5099f-149">Voit hyödyntää tätä skenaariota myös ohjeena, kun työskentelet tuotantojärjestelmän parissa ja käytät toimintoa.</span><span class="sxs-lookup"><span data-stu-id="5099f-149">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="5099f-150">Tässä tapauksessa sinun on kuitenkin korvattava omat arvosi, ja sinulta saattaa puuttua joitakin pakollisia tietoja, joita vakiodemotiedot sisältävät.</span><span class="sxs-lookup"><span data-stu-id="5099f-150">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="scenario-wave-template-grouping"></a><span data-ttu-id="5099f-151">Skenaario: Aallon mallipohjan ryhmittely</span><span class="sxs-lookup"><span data-stu-id="5099f-151">Scenario: Wave template grouping</span></span>

<span data-ttu-id="5099f-152">Tämä skenaario näyttää, miten Aaltomalli-ryhmittelyä käytetään luomaan automaattisesti useita aaltoja aaltomallissa määritettyjen kriteerien mukaan.</span><span class="sxs-lookup"><span data-stu-id="5099f-152">This scenario shows how to use wave template grouping to automatically create multiple waves, based on grouping criteria that are defined in a wave template.</span></span> <span data-ttu-id="5099f-153">Tässä skenaariossa aaltomalli määritetään järjestelmään, jolloin luodaan yksi aalto operaattoripalvelua kohden.</span><span class="sxs-lookup"><span data-stu-id="5099f-153">In this scenario, the wave template is set up in the system to create one wave per carrier service.</span></span>

<span data-ttu-id="5099f-154">Ennen kuin aloitat, valmistele aaltomalli [Määritä aaltomalli käyttääksesi aaltomallin ryhmittelyä](#set-up-template) -kohdassa aiemmin tässä ohjeaiheessa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="5099f-154">Before you begin, prepare your wave template as described in the [Set a wave template to use wave template grouping](#set-up-template) section earlier in this topic.</span></span> <span data-ttu-id="5099f-155">Jos aiot käyttää tämän skenaarion demotietoja, varmista, että käytät tässä toimintosarjassa ehdotettuja demotietoarvoja.</span><span class="sxs-lookup"><span data-stu-id="5099f-155">If you will be working with demo data for this scenario, be sure to use the demo data values that are suggested in that procedure.</span></span> <span data-ttu-id="5099f-156">Tämän asetuksen avulla voit ryhmitellä aallot kullekin myyntitilaukselle määritetyn rahdinkuljetuspalvelun mukaan.</span><span class="sxs-lookup"><span data-stu-id="5099f-156">This setup will group your waves according to the carrier service that is set for each sales order.</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="5099f-157">Luo myyntitilaus 1</span><span class="sxs-lookup"><span data-stu-id="5099f-157">Create sales order 1</span></span>

1. <span data-ttu-id="5099f-158">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="5099f-158">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="5099f-159">Luo uusi myyntitilaus valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="5099f-159">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="5099f-160">Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="5099f-160">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="5099f-161">Aseta **Asiakas**-pikavälilehdessä **Asiakastili**-kentän arvoksi *US-004*.</span><span class="sxs-lookup"><span data-stu-id="5099f-161">On the **Customer** FastTab, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="5099f-162">Aseta **Yleinen**-pikavälilehden **Varasto**-kentässä arvoksi *62*.</span><span class="sxs-lookup"><span data-stu-id="5099f-162">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="5099f-163">Valitse **OK** luodaksesi uuden myyntitilauksen ja sulje **Luo myyntitilaus** -valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="5099f-163">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="5099f-164">Uusi myyntitilaus avataan **Rivit**-näkymässä.</span><span class="sxs-lookup"><span data-stu-id="5099f-164">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="5099f-165">Kirjoita myyntitilauksen numero muistiin.</span><span class="sxs-lookup"><span data-stu-id="5099f-165">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="5099f-166">Vaihda **Otsikko**-näkymään.</span><span class="sxs-lookup"><span data-stu-id="5099f-166">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="5099f-167">Määritä **Toimitus**-pikavälilehden **Kuljetus**-osassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="5099f-167">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="5099f-168">**Rahdinkuljettaja:** *Lentorahti*</span><span class="sxs-lookup"><span data-stu-id="5099f-168">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="5099f-169">**Rahdinkuljetuspalvelu:** *Ilma*</span><span class="sxs-lookup"><span data-stu-id="5099f-169">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="5099f-170">Siirry takaisin **Rivit**-näkymään.</span><span class="sxs-lookup"><span data-stu-id="5099f-170">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="5099f-171">Valitse **Myyntitilausrivit**-osasta **Lisää rivi** lisätäksesi ruudukkoon rivin.</span><span class="sxs-lookup"><span data-stu-id="5099f-171">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="5099f-172">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="5099f-172">On the new line, set the following values:</span></span>

    - <span data-ttu-id="5099f-173">**Nimiketunnus:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="5099f-173">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="5099f-174">**Määrä** *2*</span><span class="sxs-lookup"><span data-stu-id="5099f-174">**Quantity:** *2*</span></span>

1. <span data-ttu-id="5099f-175">Valitse uusi tilausrivi ja valitse sitten ruudukon yläpuolella olevasta **Varasto**-valikosta **Varaus**.</span><span class="sxs-lookup"><span data-stu-id="5099f-175">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="5099f-176">Valitse **Varaus**-sivun toimintoruudusta **Varaa erä**, jos haluat varata koko valitun rivin määrän varastosta.</span><span class="sxs-lookup"><span data-stu-id="5099f-176">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="5099f-177">Palaa myyntitilaukseen sulkemalla **Varaus**-sivun.</span><span class="sxs-lookup"><span data-stu-id="5099f-177">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="5099f-178">Valitse toimintoruudussa **Varasto**-välilehden **Toiminnot**-ryhmässä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="5099f-178">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="5099f-179">Näyttöön tulee tietosanoma, jossa näkyy tämän tilauksen lähetys ja aalto.</span><span class="sxs-lookup"><span data-stu-id="5099f-179">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="5099f-180">Kirjoita muistiin aallon tunnusnumero ja lähetyksen tunnusnumerot.</span><span class="sxs-lookup"><span data-stu-id="5099f-180">Make a note of the wave ID number and the shipment ID numbers.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a><span data-ttu-id="5099f-181">Näytä myyntitilauksesta 1 luotu aalto</span><span class="sxs-lookup"><span data-stu-id="5099f-181">View the wave that was created from sales order 1</span></span>

1. <span data-ttu-id="5099f-182">Valitse **Varastonhallinta \> Lähtevät aallot \> Lähetysaallot \> Kaikki aallot**.</span><span class="sxs-lookup"><span data-stu-id="5099f-182">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="5099f-183">Valitse myyntitilauksesta luodun aallon tunnus.</span><span class="sxs-lookup"><span data-stu-id="5099f-183">Select the wave ID that was created from the sales order.</span></span>
1. <span data-ttu-id="5099f-184">Valitse aallon tunnus -linkki ja avaa aallon tiedot -sivu.</span><span class="sxs-lookup"><span data-stu-id="5099f-184">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="5099f-185">Huomaa, että lähetys on lisätty **Aallon rivit** -pikavälilehteen.</span><span class="sxs-lookup"><span data-stu-id="5099f-185">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="5099f-186">Luo myyntitilaus 2</span><span class="sxs-lookup"><span data-stu-id="5099f-186">Create sales order 2</span></span>

1. <span data-ttu-id="5099f-187">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="5099f-187">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="5099f-188">Luo uusi myyntitilaus valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="5099f-188">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="5099f-189">Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="5099f-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="5099f-190">Aseta **Asiakas**-pikavälilehdessä **Asiakastili**-kentän arvoksi *US-005*.</span><span class="sxs-lookup"><span data-stu-id="5099f-190">On the **Customer** FastTab, set the **Customer account** field to *US-005*.</span></span>
    - <span data-ttu-id="5099f-191">Aseta **Yleinen**-pikavälilehden **Varasto**-kentässä arvoksi *62*.</span><span class="sxs-lookup"><span data-stu-id="5099f-191">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="5099f-192">Valitse **OK** luodaksesi uuden myyntitilauksen ja sulje **Luo myyntitilaus** -valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="5099f-192">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="5099f-193">Uusi myyntitilaus avataan **Rivit**-näkymässä.</span><span class="sxs-lookup"><span data-stu-id="5099f-193">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="5099f-194">Kirjoita myyntitilauksen numero muistiin.</span><span class="sxs-lookup"><span data-stu-id="5099f-194">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="5099f-195">Vaihda **Otsikko**-näkymään.</span><span class="sxs-lookup"><span data-stu-id="5099f-195">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="5099f-196">Määritä **Toimitus**-pikavälilehden **Kuljetus**-osassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="5099f-196">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="5099f-197">**Lähetyksen rahdinkuljettaja:** *Kukkakuljetus*</span><span class="sxs-lookup"><span data-stu-id="5099f-197">**Shipping carrier:** *Flower moving*</span></span>
    - <span data-ttu-id="5099f-198">**Rahdinkuljetuspalvelu:** *Standardi*</span><span class="sxs-lookup"><span data-stu-id="5099f-198">**Carrier service:** *Std*</span></span>

1. <span data-ttu-id="5099f-199">Siirry takaisin **Rivit**-näkymään.</span><span class="sxs-lookup"><span data-stu-id="5099f-199">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="5099f-200">Valitse **Myyntitilausrivit**-osasta **Lisää rivi** lisätäksesi ruudukkoon rivin.</span><span class="sxs-lookup"><span data-stu-id="5099f-200">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="5099f-201">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="5099f-201">On the new line, set the following values:</span></span>

    - <span data-ttu-id="5099f-202">**Nimiketunnus:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="5099f-202">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="5099f-203">**Määrä** *1*</span><span class="sxs-lookup"><span data-stu-id="5099f-203">**Quantity:** *1*</span></span>

1. <span data-ttu-id="5099f-204">Valitse uusi tilausrivi ja valitse sitten ruudukon yläpuolella olevasta **Varasto**-valikosta **Varaus**.</span><span class="sxs-lookup"><span data-stu-id="5099f-204">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="5099f-205">Valitse **Varaus**-sivun toimintoruudusta **Varaa erä**, jos haluat varata koko valitun rivin määrän varastosta.</span><span class="sxs-lookup"><span data-stu-id="5099f-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="5099f-206">Palaa myyntitilaukseen sulkemalla **Varaus**-sivun.</span><span class="sxs-lookup"><span data-stu-id="5099f-206">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="5099f-207">Valitse toimintoruudussa **Varasto**-välilehden **Toiminnot**-ryhmässä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="5099f-207">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="5099f-208">Näyttöön tulee tietosanoma, jossa näkyy tämän tilauksen lähetys ja aalto.</span><span class="sxs-lookup"><span data-stu-id="5099f-208">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="5099f-209">Kirjoita muistiin aallon tunnusnumero ja lähetyksen tunnusnumerot.</span><span class="sxs-lookup"><span data-stu-id="5099f-209">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="5099f-210">Huomaa, että aallon tunnus eroaa ensimmäisen myyntitilauksen aallon tunnuksesta.</span><span class="sxs-lookup"><span data-stu-id="5099f-210">Notice that the wave ID differs from the wave ID of the first sales order.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a><span data-ttu-id="5099f-211">Näytä myyntitilauksesta 2 luotu aalto</span><span class="sxs-lookup"><span data-stu-id="5099f-211">View the wave that was created from sales order 2</span></span>

1. <span data-ttu-id="5099f-212">Valitse **Varastonhallinta \> Lähtevät aallot \> Lähetysaallot \> Kaikki aallot**.</span><span class="sxs-lookup"><span data-stu-id="5099f-212">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="5099f-213">Valitse toisesta myyntitilauksesta luodun aallon tunnus.</span><span class="sxs-lookup"><span data-stu-id="5099f-213">Select the wave ID that was created from the second sales order.</span></span>
1. <span data-ttu-id="5099f-214">Valitse aallon tunnus -linkki ja avaa aallon tiedot -sivu.</span><span class="sxs-lookup"><span data-stu-id="5099f-214">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="5099f-215">Huomaa, että lähetys on lisätty **Aallon rivit** -pikavälilehteen.</span><span class="sxs-lookup"><span data-stu-id="5099f-215">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

<span data-ttu-id="5099f-216">Tälle siirrolle on luotu uusi aalto, koska se käyttää eri rahdin kuljetuspalvelua kuin ensimmäinen myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="5099f-216">A new wave was created for this shipment, because it uses a different carrier service than the first sales order.</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="5099f-217">Luo myyntitilaus 3</span><span class="sxs-lookup"><span data-stu-id="5099f-217">Create sales order 3</span></span>

1. <span data-ttu-id="5099f-218">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="5099f-218">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="5099f-219">Luo uusi myyntitilaus valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="5099f-219">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="5099f-220">Aseta **Luo myyntitilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="5099f-220">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="5099f-221">Aseta **Asiakas**-pikavälilehdessä **Asiakastili**-kentän arvoksi *US-006*.</span><span class="sxs-lookup"><span data-stu-id="5099f-221">On the **Customer** FastTab, set the **Customer account** field to *US-006*.</span></span>
    - <span data-ttu-id="5099f-222">Aseta **Yleinen**-pikavälilehden **Varasto**-kentässä arvoksi *62*.</span><span class="sxs-lookup"><span data-stu-id="5099f-222">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="5099f-223">Valitse **OK** luodaksesi uuden myyntitilauksen ja sulje **Luo myyntitilaus** -valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="5099f-223">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="5099f-224">Uusi myyntitilaus avataan **Rivit**-näkymässä.</span><span class="sxs-lookup"><span data-stu-id="5099f-224">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="5099f-225">Kirjoita myyntitilauksen numero muistiin.</span><span class="sxs-lookup"><span data-stu-id="5099f-225">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="5099f-226">Vaihda **Otsikko**-näkymään.</span><span class="sxs-lookup"><span data-stu-id="5099f-226">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="5099f-227">Määritä **Toimitus**-pikavälilehden **Kuljetus**-osassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="5099f-227">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="5099f-228">**Rahdinkuljettaja:** *Lentorahti*</span><span class="sxs-lookup"><span data-stu-id="5099f-228">**Shipping carrier:** *Air Cargo*</span></span>
    - <span data-ttu-id="5099f-229">**Rahdinkuljetuspalvelu:** *Ilma*</span><span class="sxs-lookup"><span data-stu-id="5099f-229">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="5099f-230">Siirry takaisin **Rivit**-näkymään.</span><span class="sxs-lookup"><span data-stu-id="5099f-230">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="5099f-231">Valitse **Myyntitilausrivit**-osasta **Lisää rivi** lisätäksesi ruudukkoon rivin.</span><span class="sxs-lookup"><span data-stu-id="5099f-231">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="5099f-232">Määritä uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="5099f-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="5099f-233">**Nimiketunnus:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="5099f-233">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="5099f-234">**Määrä** *1*</span><span class="sxs-lookup"><span data-stu-id="5099f-234">**Quantity:** *1*</span></span>

1. <span data-ttu-id="5099f-235">Valitse uusi tilausrivi ja valitse sitten ruudukon yläpuolella olevasta **Varasto**-valikosta **Varaus**.</span><span class="sxs-lookup"><span data-stu-id="5099f-235">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="5099f-236">Valitse **Varaus**-sivun toimintoruudusta **Varaa erä**, jos haluat varata koko valitun rivin määrän varastosta.</span><span class="sxs-lookup"><span data-stu-id="5099f-236">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="5099f-237">Palaa myyntitilaukseen sulkemalla **Varaus**-sivun.</span><span class="sxs-lookup"><span data-stu-id="5099f-237">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="5099f-238">Valitse toimintoruudussa **Varasto**-välilehden **Toiminnot**-ryhmässä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="5099f-238">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="5099f-239">Näyttöön tulee tietosanoma, jossa näkyy tämän tilauksen lähetys ja aalto.</span><span class="sxs-lookup"><span data-stu-id="5099f-239">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="5099f-240">Kirjoita muistiin aallon tunnusnumero ja lähetyksen tunnusnumerot.</span><span class="sxs-lookup"><span data-stu-id="5099f-240">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="5099f-241">Lähetys on määritetty ensimmäisestä myyntitilauksesta olemassa olevalle aallolle.</span><span class="sxs-lookup"><span data-stu-id="5099f-241">The shipment has been assigned to the existing wave from the first sales order.</span></span>

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a><span data-ttu-id="5099f-242">Näytä myyntitilausten 1 ja 3 aalto</span><span class="sxs-lookup"><span data-stu-id="5099f-242">View the wave for sales orders 1 and 3</span></span>

1. <span data-ttu-id="5099f-243">Valitse **Varastonhallinta \> Lähtevät aallot \> Lähetysaallot \> Kaikki aallot**.</span><span class="sxs-lookup"><span data-stu-id="5099f-243">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="5099f-244">Valitse kolmannesta myyntitilauksesta luodun aallon tunnus.</span><span class="sxs-lookup"><span data-stu-id="5099f-244">Select the wave ID that was created from the third sales order.</span></span>
1. <span data-ttu-id="5099f-245">Valitse aallon tunnus -linkki ja avaa aallon tiedot -sivu.</span><span class="sxs-lookup"><span data-stu-id="5099f-245">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="5099f-246">Huomaa, että lähetys on lisätty **Aallon rivit** -pikavälilehteen yhdessä ensimmäisen myyntitilauksen toimituksen kanssa.</span><span class="sxs-lookup"><span data-stu-id="5099f-246">Notice that the shipment has been added to the **Wave lines** FastTab, together with the shipment for the first sales order.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]