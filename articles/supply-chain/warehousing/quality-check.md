---
title: Laaduntarkistus
description: Tässä ohjeaiheessa on tietoja laaduntarkistusominaisuudesta. Tämän ominaisuuden avulla varaston työntekijät voivat tehdä nopeita laaduntarkistuksia samalla, kun nimikkeitä vastaanotetaan laiturialueelle.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSQualityCheckTemplate, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSQualityCheckResult
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: dfb71f74732d65409003c4f6f74145442a1efa3f
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4427471"
---
# <a name="quality-check"></a><span data-ttu-id="36874-104">Laaduntarkistus</span><span class="sxs-lookup"><span data-stu-id="36874-104">Quality check</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36874-105">*Laaduntarkistusominaisuuden* avulla varaston työntekijät voivat tehdä nopeita laaduntarkistuksia samalla, kun nimikkeitä vastaanotetaan laiturialueelle.</span><span class="sxs-lookup"><span data-stu-id="36874-105">The *Quality check* feature lets warehouse workers do quick spot checks for quality while they receive items to the inbound dock area.</span></span> <span data-ttu-id="36874-106">Nämä nopeat tarkistukset ovat hyödyllisiä silloin, kun työntekijät tarkastavat pakkauksia tai nimikkeen muuten helposti tunnistettavissa olevia osia.</span><span class="sxs-lookup"><span data-stu-id="36874-106">These spot checks are beneficial when workers inspect packaging or other easily recognizable parts of an item.</span></span> <span data-ttu-id="36874-107">Ominaisuuden avulla työntekijät voivat katsoa nopeasti, onko jokin selvästi viallinen tai vioittunut, ennen kuin he varastoivat nimikkeet hyllytyssijaintiin.</span><span class="sxs-lookup"><span data-stu-id="36874-107">The feature guides workers to take a quick look to see whether anything is obviously faulty or damaged before they stock the inventory in its putaway location.</span></span>

<span data-ttu-id="36874-108">Tämä ominaisuus on vakiolaaduntarkastusprosessin vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="36874-108">This feature is an alternative to the standard quality check process.</span></span> <span data-ttu-id="36874-109">Se on aiempaa joustavampi ja nopeampi.</span><span class="sxs-lookup"><span data-stu-id="36874-109">It offers more flexibility and faster processing.</span></span>

<span data-ttu-id="36874-110">Jos tämä ominaisuus on käytössä, saapumis- ja laaduntarkistus tapahtuvat seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="36874-110">When you use this feature, the arrival and quality check occur in the following way:</span></span>

1. <span data-ttu-id="36874-111">Kun lähetys saapuu, varastotyöntekijä rekisteröi saapumisen.</span><span class="sxs-lookup"><span data-stu-id="36874-111">When a shipment arrives, a warehouse worker registers the arrival.</span></span> <span data-ttu-id="36874-112">Työntekijä myös skannaa rekisterikilven ja rekisteröi sijainnin.</span><span class="sxs-lookup"><span data-stu-id="36874-112">The worker also scans a license plate to register the location.</span></span>
1. <span data-ttu-id="36874-113">Työntekijä tekee nopean laaduntarkistuksen ja tallentaa rekisterikilven tuloksen (hyväksytty tai hylätty).</span><span class="sxs-lookup"><span data-stu-id="36874-113">The worker does a quick quality check and records the result (pass or fail) for that license plate.</span></span>
1. <span data-ttu-id="36874-114">Yksi seuraavista toiminnoista tapahtuu:</span><span class="sxs-lookup"><span data-stu-id="36874-114">One of the following actions occurs:</span></span>

    - <span data-ttu-id="36874-115">Jos laaduntarkistus on hyväksytty, rekisterikilpi hyväksytään ja saatetaan vastaanottosijaintiin tavalliseen tapaan.</span><span class="sxs-lookup"><span data-stu-id="36874-115">If the quality check is passed, the license plate is accepted and guided to a receiving location, as usual.</span></span>
    - <span data-ttu-id="36874-116">Jos laaduntarkistus epäonnistuu, rekisterikilpi hylätään ja sen olemassa oleva hyllytystyö ohjataan uudelleen vaihtoehtoiseen sijaintiin lisätarkastusta varten.</span><span class="sxs-lookup"><span data-stu-id="36874-116">If the quality check is failed, the license plate is rejected, and existing putaway work for it is redirected to an alternate location for further inspection.</span></span> <span data-ttu-id="36874-117">Uusi laatutilaus luodaan.</span><span class="sxs-lookup"><span data-stu-id="36874-117">A new quality order is created.</span></span> <span data-ttu-id="36874-118">Jos haluat tarkastella laatutilausta, joka on luotu epäonnistuneesta laaduntarkistuksesta, siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Laatutilaukset**.</span><span class="sxs-lookup"><span data-stu-id="36874-118">To view the quality order that is created from the failed quality check, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="36874-119">Tämä prosessi voidaan määrittää myös siten, että kaikki skannatut rekisterikilvet ohjataan välittömästi laaduntarkistussijaintiin.</span><span class="sxs-lookup"><span data-stu-id="36874-119">This process can also be set up so that all scanned license plates are immediately diverted to the quality check location.</span></span>

## <a name="turn-on-the-quality-check-feature"></a><span data-ttu-id="36874-120">Laaduntarkistusominaisuuden ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="36874-120">Turn on the Quality check feature</span></span>

<span data-ttu-id="36874-121">Ennen kuin käytät *laaduntarkistusominaisuutta*, se on otettava käyttöön järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="36874-121">Before you can use the *Quality check* feature, it must be turned on in your system.</span></span> <span data-ttu-id="36874-122">Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön, jos sitä vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="36874-122">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="36874-123">**Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="36874-123">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="36874-124">**Moduuli:** *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="36874-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="36874-125">**Ominaisuuden nimi:** *Laaduntarkistus*</span><span class="sxs-lookup"><span data-stu-id="36874-125">**Feature name:** *Quality check*</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="36874-126">Määritä ominaisuus tälle esimerkkiskenaariolle</span><span class="sxs-lookup"><span data-stu-id="36874-126">Set up the feature for the example scenario</span></span>

<span data-ttu-id="36874-127">Tässä ohjeaiheessa on ohjeita ja esimerkki, jossa kerrotaan *laaduntarkistustoiminnon* määrityksestä ja tässä ohjeaiheessa myöhemmin olevan esimerkkiskenaarion näytetietojen valmistelemisesta.</span><span class="sxs-lookup"><span data-stu-id="36874-127">This section provides guidelines and an example that shows how to set up the *Quality check* feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="36874-128">Ota mallitiedot käyttöön</span><span class="sxs-lookup"><span data-stu-id="36874-128">Make sample data available</span></span>

<span data-ttu-id="36874-129">[Esimerkkiskenaarion](#example-scenario) käyttäminen tässä määritettyjen mallitietojen ja -arvojen avulla edellyttää, että käytössä on järjestelmä, johon [vakiodemotiedot](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) on asennettu.</span><span class="sxs-lookup"><span data-stu-id="36874-129">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="36874-130">Sinun on myös valittava **USMF**-yritys ennen kuin aloitat.</span><span class="sxs-lookup"><span data-stu-id="36874-130">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="quality-check-template"></a><a name="quality-template"></a><span data-ttu-id="36874-131">Laaduntarkistusmalli</span><span class="sxs-lookup"><span data-stu-id="36874-131">Quality check template</span></span>

<span data-ttu-id="36874-132">Laaduntarkistusmalli määrittää laadun nopeiden tarkistusten säännöt vastaanoton yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="36874-132">The quality check template defines the rules for doing quick spot checks for quality at the time of receiving.</span></span>

1. <span data-ttu-id="36874-133">Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Laaduntarkistusmallit**.</span><span class="sxs-lookup"><span data-stu-id="36874-133">Go to **Warehouse management \> Setup \> Work \> Quality check template**.</span></span>
1. <span data-ttu-id="36874-134">Valitse **Uusi** lisätäksesi mallin ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="36874-134">Select **New** to add a template to the grid.</span></span>
1. <span data-ttu-id="36874-135">Määritä uusi malli määrittämällä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="36874-135">Set the following values to define the new template:</span></span>

    - <span data-ttu-id="36874-136">**Laaduntarkistusmallin nimi:** *Laituritarkistus*</span><span class="sxs-lookup"><span data-stu-id="36874-136">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="36874-137">Kirjoita nimi, joka määrittää tässä mallissa käytetyt käytännöt.</span><span class="sxs-lookup"><span data-stu-id="36874-137">Enter a name that identifies the policies applied for this template.</span></span>

    - <span data-ttu-id="36874-138">**Hyväksymiskäytäntö:** *Kehote käyttäjälle*</span><span class="sxs-lookup"><span data-stu-id="36874-138">**Acceptance policy:** *Prompt user*</span></span>

        <span data-ttu-id="36874-139">Määritä, pyydetäänkö käyttäjiä hyväksymään tai hylkäämään varaston laatu työn käsittely yhteydessä vai hylätäänkö laatu automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="36874-139">Specify whether users should be prompted to accept or reject the quality of the inventory while they process the work, or whether the quality should automatically be rejected.</span></span> <span data-ttu-id="36874-140">Käytettävissä olevat vaihtoehdot ovat *Automaattinen hylkääminen* ja *Kehote käyttäjälle*.</span><span class="sxs-lookup"><span data-stu-id="36874-140">The available options are *Auto reject* and *Prompt user*.</span></span>

    - <span data-ttu-id="36874-141">**Laadun käsittelykäytäntö:** *Luo laatutilaus*</span><span class="sxs-lookup"><span data-stu-id="36874-141">**Quality processing policy:** *Create quality order*</span></span>

        <span data-ttu-id="36874-142">Valitse käytäntö, jota käytetään varaston laadun hylkäyksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="36874-142">Select the policy that should be used when the quality of the inventory is rejected.</span></span> <span data-ttu-id="36874-143">Käytettävissä ovat seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="36874-143">The following options are available:</span></span>

        - <span data-ttu-id="36874-144">*Luo vain työ* – Luo vain työ varastosiirtoja varten.</span><span class="sxs-lookup"><span data-stu-id="36874-144">*Create work only* – Just create work to facilitate inventory movement.</span></span>
        - <span data-ttu-id="36874-145">*Luo laatutilaus* – Luo laatutilaus laatutestejä varten.</span><span class="sxs-lookup"><span data-stu-id="36874-145">*Create quality order* – Create a quality order to facilitate quality tests.</span></span>

    - <span data-ttu-id="36874-146">**Testiryhmä:** *Kehys*</span><span class="sxs-lookup"><span data-stu-id="36874-146">**Test group:** *Enclosure*</span></span>

        <span data-ttu-id="36874-147">Määritä testiryhmä, jota käytetään luotavassa laatutilauksessa.</span><span class="sxs-lookup"><span data-stu-id="36874-147">Specify the test group that should be used in the quality order that is created.</span></span> <span data-ttu-id="36874-148">Testiryhmät määritetään **Varastonhallinta**-moduulissa.</span><span class="sxs-lookup"><span data-stu-id="36874-148">Test groups are set up in the **Inventory management** module.</span></span>

        <span data-ttu-id="36874-149">Ota testiryhmän **Destruktiivinen teksti** -vaihtoehto pois käytöstä.</span><span class="sxs-lookup"><span data-stu-id="36874-149">Leave the **Destructive text** option turned off for the test group.</span></span> <span data-ttu-id="36874-150">Tämä vaihtoehto määrittää, tuhotaanko näytteet osana testiryhmän testejä.</span><span class="sxs-lookup"><span data-stu-id="36874-150">This option defines whether the sample will be destroyed as part of the tests in the test group.</span></span> <span data-ttu-id="36874-151">Jos käytetään destruktiivista testiä, järjestelmä luo varastotapahtuman, kun laatutilaus luodaan nimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="36874-151">If a destructive test is used, the system generates an inventory transaction when a quality order is created for an item.</span></span> <span data-ttu-id="36874-152">Uusi varastotapahtuma ennustaa testimäärän aiheuttaman varastovähennyksen.</span><span class="sxs-lookup"><span data-stu-id="36874-152">The new inventory transaction predicts the inventory reduction for the test quantity.</span></span> <span data-ttu-id="36874-153">Varastonvähennys tapahtuu, kun laatutilaus viimeistellään vahvistusvaiheessa.</span><span class="sxs-lookup"><span data-stu-id="36874-153">The inventory reduction occurs when the quality order is completed through the validation step.</span></span> <span data-ttu-id="36874-154">Varastotapahtuma määritetään laatutilaukseksi.</span><span class="sxs-lookup"><span data-stu-id="36874-154">The inventory transaction is identified as a quality order.</span></span>

### <a name="work-class--quality-check"></a><a name="work-class"></a><span data-ttu-id="36874-155">Työluokka – laaduntarkistus</span><span class="sxs-lookup"><span data-stu-id="36874-155">Work class – Quality check</span></span>

<span data-ttu-id="36874-156">Työluokilla ohjataan ja/tai rajoitetaan työtilausrivityyppejä, joita varastotyötekijät voivat käsitellä mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="36874-156">Work classes are used to direct and/or limit the type of work order lines that warehouse workers can process on a mobile device.</span></span>

1. <span data-ttu-id="36874-157">Valitse **Varastonhallinta \> Asetukset \> Työ \> Työluokka**.</span><span class="sxs-lookup"><span data-stu-id="36874-157">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="36874-158">Luo työluokka valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="36874-158">Select **New** to create a work class.</span></span>
1. <span data-ttu-id="36874-159">Aseta otsikkorivillä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="36874-159">In the header, set the following values:</span></span>

    - <span data-ttu-id="36874-160">**Työluokan tunnus:** *QC-tarkistus*</span><span class="sxs-lookup"><span data-stu-id="36874-160">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="36874-161">Anna työluokalle nimi.</span><span class="sxs-lookup"><span data-stu-id="36874-161">Enter a name that identifies the work class.</span></span>

    - <span data-ttu-id="36874-162">**Kuvaus:** *QC-tarkistus*</span><span class="sxs-lookup"><span data-stu-id="36874-162">**Description:** *QC Check*</span></span>

        <span data-ttu-id="36874-163">Anna lyhyt kuvaus, joka osoittaa käytettävän työluokan.</span><span class="sxs-lookup"><span data-stu-id="36874-163">Enter a short description that indicates what the work class is used for.</span></span>

    - <span data-ttu-id="36874-164">**Työtilauksen tyyppi:** *Laaduntarkistuksen laatu*</span><span class="sxs-lookup"><span data-stu-id="36874-164">**Work order type:** *Quality in quality check*</span></span>

        <span data-ttu-id="36874-165">Valitse työluokan luoma työtilaustyyppi.</span><span class="sxs-lookup"><span data-stu-id="36874-165">Select the type of work order that is created by the work class.</span></span> <span data-ttu-id="36874-166">Kun määrität laadunvalvontatyön, valitse aina *Laaduntarkistuksen laatu*.</span><span class="sxs-lookup"><span data-stu-id="36874-166">When you set up quality control work, always select *Quality in quality check*.</span></span>

1. <span data-ttu-id="36874-167">Jätä **Sallitut hyllytyssijainnit** -pikavälilehden **Sijaintityyppi**-kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="36874-167">On the **Valid put location types** FastTab, leave the **Location type** field blank.</span></span>

    <span data-ttu-id="36874-168">Jos valitset sijaintityypin, rajoitat niitä sijainteja, joissa nimikkeet voidaan hyllyttää keräilyn jälkeen.</span><span class="sxs-lookup"><span data-stu-id="36874-168">If you select a location type, you limit the locations where items can be put after they are picked.</span></span> <span data-ttu-id="36874-169">Tätä kenttää käytetään, kun sijaintidirektiivi yrittää ratkaista sijainnin tai jos varastotyöntekijä määrittää manuaalisesti sijainnin mobiililaitteen valikkosijainnin valikon vaihtoehdossa.</span><span class="sxs-lookup"><span data-stu-id="36874-169">This field is used when a location directive tries to resolve the location, or when a warehouse worker manually specifies the location for the mobile device menu item.</span></span>

<span data-ttu-id="36874-170">Lisätietoja työluokista ja niiden luomisesta on kohdassa [Työluokan luominen](tasks/create-work-class.md).</span><span class="sxs-lookup"><span data-stu-id="36874-170">For more information about work classes and how to create them, see [Create a work class](tasks/create-work-class.md).</span></span>

### <a name="work-template"></a><span data-ttu-id="36874-171">Työmalli</span><span class="sxs-lookup"><span data-stu-id="36874-171">Work template</span></span>

<span data-ttu-id="36874-172">Työmallen avulla voit määrittää työtoiminnot, jotka on suoritettava varastossa.</span><span class="sxs-lookup"><span data-stu-id="36874-172">Work templates let you define the work operations that must be performed in the warehouse.</span></span> <span data-ttu-id="36874-173">Yleensä varastotyötoiminnot kostuvat toimintopareista: varaston työntekijä keräilee käsillä olevan varaston yhdessä sijainnissa ja asettaa sitten keräillyt varastotuotteet toiseen paikkaan.</span><span class="sxs-lookup"><span data-stu-id="36874-173">Typically, warehouse work operations consist of a pair of actions: a warehouse worker picks on-hand inventory up in one location and then puts the picked inventory down in another location.</span></span> <span data-ttu-id="36874-174">Laadunvalvonnan työmalli määrittää laaduntarkistusten työtoiminnot.</span><span class="sxs-lookup"><span data-stu-id="36874-174">A work template for quality control defines the work operations for doing quality checks.</span></span>

#### <a name="purchase-orders"></a><span data-ttu-id="36874-175">Ostotilaukset</span><span class="sxs-lookup"><span data-stu-id="36874-175">Purchase orders</span></span>

1. <span data-ttu-id="36874-176">Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työmallit**.</span><span class="sxs-lookup"><span data-stu-id="36874-176">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="36874-177">Määritä otsikossa **Työtilaustyyppi**-kentän arvoksi *Ostotilaukset*.</span><span class="sxs-lookup"><span data-stu-id="36874-177">In the header, set the **Work order type** field to *Purchase orders*.</span></span>
1. <span data-ttu-id="36874-178">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="36874-178">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="36874-179">Valitse työmalli, jonka tulee sisältää laaduntarkistusvaihe.</span><span class="sxs-lookup"><span data-stu-id="36874-179">Select a work template that should include a quality check step.</span></span> <span data-ttu-id="36874-180">Valitse **Yleiskatsaus**-osan **Työmalli**-kentässä *51 - ostotilauksen vastaanotto*.</span><span class="sxs-lookup"><span data-stu-id="36874-180">In the **Overview** section, in the **Work template** field, select *51 PO Receipt*.</span></span>
1. <span data-ttu-id="36874-181">Huomaa, että **Työmallin tiedot** -osan ruudukossa on kaksi riviä. Toinen rivi on *keräilyä* ja toinen *hyllytystä* varten.</span><span class="sxs-lookup"><span data-stu-id="36874-181">In the **Work template details** section, notice that the grid has two existing lines: one for *Pick* and one for *Put*.</span></span>
1. <span data-ttu-id="36874-182">Valitse **Työmallin tiedot** -osassa **Uusi**, jos haluat lisätä ruudukkoon laadunvalvonnan rivin.</span><span class="sxs-lookup"><span data-stu-id="36874-182">In the **Work template details** section, select **New** to add a row for quality control to the grid.</span></span> <span data-ttu-id="36874-183">Huomaa, että uuden rivin **Rivinumero**-kentän arvoksi on määritetty *3*.</span><span class="sxs-lookup"><span data-stu-id="36874-183">Notice that the **Line number** field for the new line is set to *3*.</span></span>
1. <span data-ttu-id="36874-184">Määritä uudelle riville seuraavat arvot.</span><span class="sxs-lookup"><span data-stu-id="36874-184">On the new line, set the following values.</span></span> <span data-ttu-id="36874-185">Hyväksy jäljellä olevien kenttien oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="36874-185">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="36874-186">**Työtyyppi:** *Laaduntarkistus*</span><span class="sxs-lookup"><span data-stu-id="36874-186">**Work type:** *Quality check*</span></span>
    - <span data-ttu-id="36874-187">**Työluokan tunnus:** *Osto*</span><span class="sxs-lookup"><span data-stu-id="36874-187">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="36874-188">**Laaduntarkistusmallin nimi:** *Laituritarkistus*</span><span class="sxs-lookup"><span data-stu-id="36874-188">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="36874-189">Valitse työluokan yksilöivä tunniste.</span><span class="sxs-lookup"><span data-stu-id="36874-189">Select the unique ID for the work class.</span></span> <span data-ttu-id="36874-190">Voit käyttää tätä arvoa mobiililaitteen valikkokohteiden määrittämiseen ja sen tyyppiseen työhön, jota valikkokohteet voivat käsitellä.</span><span class="sxs-lookup"><span data-stu-id="36874-190">You use this value to configure the menu items on the mobile device and the types of work that those menu items can process.</span></span>

1. <span data-ttu-id="36874-191">Valitse toimintoruudussa **Tallenna**, jos haluat tallentaa tähänastisen työn.</span><span class="sxs-lookup"><span data-stu-id="36874-191">On the Action Pane, select **Save** to save your work so far.</span></span>

    <span data-ttu-id="36874-192">Näyttöön tulee seuraava sanoma: "Virheellinen - Laaduntarkistus on tehtävä heti keräilyn jälkeen."</span><span class="sxs-lookup"><span data-stu-id="36874-192">You receive an informational message that states, "Invalid - Quality check must come directly after a pick."</span></span> <span data-ttu-id="36874-193">Tämän vuoksi juuri lisätyn rivin **Rivinumero**-arvo on muutettava.</span><span class="sxs-lookup"><span data-stu-id="36874-193">Therefore, you must change the **Line number** value for the line that you just added.</span></span>

1. <span data-ttu-id="36874-194">Muuta uuden rivin **Rivinumero**-arvoa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="36874-194">Follow these steps to change the **Line number** value for the new line:</span></span>

    1. <span data-ttu-id="36874-195">Valitse **Työmallin tiedot** -osassa rivi, jonka **Työtyyppi**-kentän arvoksi on määritetty *Laaduntarkistus*.</span><span class="sxs-lookup"><span data-stu-id="36874-195">In the **Work template details** section, select the line where the **Work type** field is set to *Quality check*.</span></span>
    2. <span data-ttu-id="36874-196">Valitse **Siirry ylös**- tai **Siirry alas** -painike, jos haluat siirtää *Laaduntarkistus*-riviä niin, että se on *Keräily*-rivin jälkeen.</span><span class="sxs-lookup"><span data-stu-id="36874-196">Select the **Move up** or **Move down** button to move the *Quality check* line so that it's after the *Pick* line.</span></span>

1. <span data-ttu-id="36874-197">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="36874-197">On the Action Pane, select **Save**.</span></span>

#### <a name="quality-in-quality-check"></a><span data-ttu-id="36874-198">Laatu laaduntarkistuksessa</span><span class="sxs-lookup"><span data-stu-id="36874-198">Quality in quality check</span></span>

<span data-ttu-id="36874-199">Luo seuraavaksi työmalli laaduntarkistukselle.</span><span class="sxs-lookup"><span data-stu-id="36874-199">Next, create a work template for the quality check.</span></span>

1. <span data-ttu-id="36874-200">Muuta **Työmallit**-sivulla **Työtilaustyyppi**-kentän arvoksi *Laaduntarkistuksen laatu*.</span><span class="sxs-lookup"><span data-stu-id="36874-200">In the header of the **Work templates** page, change the value of the **Work order type** field to *Quality in quality check*.</span></span>
1. <span data-ttu-id="36874-201">Lisää **Yleiskatsaus**-osan ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="36874-201">On the Action Pane, select **New** to add a row to the grid in the **Overview** section.</span></span>
1. <span data-ttu-id="36874-202">Aseta uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="36874-202">In the new row, set the following values:</span></span>

    - <span data-ttu-id="36874-203">**Työmalli:** *51 - laaduntarkistus*</span><span class="sxs-lookup"><span data-stu-id="36874-203">**Work template:** *51 Quality Check*</span></span>

        <span data-ttu-id="36874-204">Anna mallille nimi.</span><span class="sxs-lookup"><span data-stu-id="36874-204">Enter a name for the template.</span></span>

    - <span data-ttu-id="36874-205">**Työmallin kuvaus:** *51 - laaduntarkistus*</span><span class="sxs-lookup"><span data-stu-id="36874-205">**Work template description:** *51 Quality Check*</span></span>

1. <span data-ttu-id="36874-206">Valitse toimintoruudussa **Tallenna**, jos haluat, että **Työmallin tiedot** -osa on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="36874-206">On the Action Pane, select **Save** to make the **Work template details** section available.</span></span>
1. <span data-ttu-id="36874-207">Kun uusi malli on vielä valittuna **Yleiskatsaus**-osassa, valitse **Uusi** **Työmallin tiedot** -osassa ja lisää ruudukkoon rivi.</span><span class="sxs-lookup"><span data-stu-id="36874-207">While the new template is still selected in the **Overview** section, select **New** in the **Work template details** section to add a row to the grid there.</span></span>
1. <span data-ttu-id="36874-208">Aseta uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="36874-208">In the new row, set the following values:</span></span>

    - <span data-ttu-id="36874-209">**Työtyyppi:** *Poiminta*</span><span class="sxs-lookup"><span data-stu-id="36874-209">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="36874-210">**Työluokan tunnus:** *QC-tarkistus*</span><span class="sxs-lookup"><span data-stu-id="36874-210">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="36874-211">Valitse aiemmin laadunvalvontatyölle luodun [työluokan](#work-class) nimi.</span><span class="sxs-lookup"><span data-stu-id="36874-211">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="36874-212">Valitse **Työmallin tiedot** -osassa uudelleen **Uusi** ja lisää toinen rivi.</span><span class="sxs-lookup"><span data-stu-id="36874-212">In the **Work template details** section, select **New** again to add another row.</span></span>
1. <span data-ttu-id="36874-213">Aseta uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="36874-213">In the new row, set the following values:</span></span>

    - <span data-ttu-id="36874-214">**Työtyyppi:** *Aseta*</span><span class="sxs-lookup"><span data-stu-id="36874-214">**Work type:** *Put*</span></span>
    - <span data-ttu-id="36874-215">**Työluokan tunnus:** *QC-tarkistus*</span><span class="sxs-lookup"><span data-stu-id="36874-215">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="36874-216">Valitse aiemmin laadunvalvontatyölle luodun [työluokan](#work-class) nimi.</span><span class="sxs-lookup"><span data-stu-id="36874-216">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="36874-217">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="36874-217">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="36874-218">Katso lisätietoja työmalleista artikkelista [Varastotyön hallinta työmallien ja sijaintidirektiivien avulla](control-warehouse-location-directives.md).</span><span class="sxs-lookup"><span data-stu-id="36874-218">For more information about work templates, see [Control warehouse work by using work templates and location directives](control-warehouse-location-directives.md)</span></span>

### <a name="location-directive--quality-failures"></a><span data-ttu-id="36874-219">Sijaintidirektiivi – laadun virheet</span><span class="sxs-lookup"><span data-stu-id="36874-219">Location directive – Quality failures</span></span>

<span data-ttu-id="36874-220">Sijaintidirektiivit ovat sääntöjä, jotka auttavat tunnistamaan keräily- ja poispanosijainnit varaston siirrossa.</span><span class="sxs-lookup"><span data-stu-id="36874-220">Location directives are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="36874-221">Esimerkiksi myyntitilaustapahtumassa sijaintidirektiivi määrittää, mistä nimikkeet kerätään, ja minne kerätyt nimikkeet sijoitetaan.</span><span class="sxs-lookup"><span data-stu-id="36874-221">For example, in a sales order transaction, a location directive determines where the items will be picked and where the picked items will be put.</span></span> <span data-ttu-id="36874-222">Sinun on määritettävä sijaintidirektiivin sääntö, jotta voit määrittää, miten epäonnistuneita laaduntarkistuksia käsitellään.</span><span class="sxs-lookup"><span data-stu-id="36874-222">You must configure a location directive rule to define how failed quality checks will be handled.</span></span>

1. <span data-ttu-id="36874-223">Valitse **Varastonhallinta \> Asetukset \> Sijaintidirektiivit**.</span><span class="sxs-lookup"><span data-stu-id="36874-223">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="36874-224">Määritä vasemmanpuoleisessa ruudussa **Työtilaustyyppi**-kentän arvoksi *Ostotilaukset*, jos haluat käsitellä tämäntyyppisiä direktiivejä.</span><span class="sxs-lookup"><span data-stu-id="36874-224">In the left pane, set the **Work order type** field to *Purchase orders* to work with location directives of that type.</span></span>
1. <span data-ttu-id="36874-225">Luo laaduntarkistusten sijaintidirektiivi valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="36874-225">On the Action Pane, select **New** to create a location directive for quality checks.</span></span>
1. <span data-ttu-id="36874-226">Aseta otsikkorivillä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="36874-226">In the header, set the following values:</span></span>

    - <span data-ttu-id="36874-227">**Järjestysnumero:** Hyväksy oletusarvo.</span><span class="sxs-lookup"><span data-stu-id="36874-227">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="36874-228">**Nimi:** *51 - kohdelaatu*</span><span class="sxs-lookup"><span data-stu-id="36874-228">**Name:** *51 To Quality*</span></span>

1. <span data-ttu-id="36874-229">Määritä **Sijaintidirektiivit**-pikavälilehdessä seuraavat arvot.</span><span class="sxs-lookup"><span data-stu-id="36874-229">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="36874-230">Hyväksy jäljellä olevien kenttien oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="36874-230">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="36874-231">**Työtyyppi:** *Aseta*</span><span class="sxs-lookup"><span data-stu-id="36874-231">**Work type:** *Put*</span></span>
    - <span data-ttu-id="36874-232">**Toimipaikka:** *5*</span><span class="sxs-lookup"><span data-stu-id="36874-232">**Site:** *5*</span></span>
    - <span data-ttu-id="36874-233">**Varasto**: *51*</span><span class="sxs-lookup"><span data-stu-id="36874-233">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="36874-234">Valitse toimintoruudussa **Tallenna**, jos haluat tallentaa direktiivin ja määrittää **Rivit**-pikavälilehden käytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="36874-234">On the Action Pane select **Save** to save your directive and make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="36874-235">Lisää uusi rivi ruudukkoon **Rivit**-pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="36874-235">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="36874-236">Määritä uudelle riville seuraavat arvot.</span><span class="sxs-lookup"><span data-stu-id="36874-236">On the new line, set the following values.</span></span> <span data-ttu-id="36874-237">Hyväksy jäljellä olevien kenttien oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="36874-237">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="36874-238">**Määrästä:** *1*</span><span class="sxs-lookup"><span data-stu-id="36874-238">**From quantity:** *1*</span></span>
    - <span data-ttu-id="36874-239">**Määrälle:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="36874-239">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="36874-240">Valitse toimintoruudussa **Tallenna**, jos haluat tallentaa uuden rivin ja määrittää **Sijaintidirektiivin toiminnot** -pikavälilehden käytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="36874-240">On the Action Pane, select **Save** to save the new line and make the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="36874-241">Kun uusi rivi on yhä valittuna **Rivit**-pikavälilehdessä, valitse **Uusi** **Sijaintidirektiivin toiminnot** -pikavälilehdessä ja lisää siellä ruudukkoon uusi rivi. Tämän jälkeen voit määrittää riville toiminnon.</span><span class="sxs-lookup"><span data-stu-id="36874-241">While the new line is still selected on the **Lines** FastTab, select **New** on the **Location directive actions** FastTab to add a row to the grid there, so that you can set up an action for the line.</span></span>
1. <span data-ttu-id="36874-242">Määritä uuden rivin **Nimi**-kentän arvoksi *Laatu*.</span><span class="sxs-lookup"><span data-stu-id="36874-242">In the new row, set the **Name** field to *Quality*.</span></span> <span data-ttu-id="36874-243">Hyväksy jäljellä olevien kenttien oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="36874-243">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="36874-244">Valitse toimintoruudussa **Tallenna**, jos haluat, että **Sijaintidirektiivin toiminnot** -pikavälilehden **Muokkaa kyselyä** -painike on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="36874-244">On the Action Pane, select **Save** to make the **Edit query** button on the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="36874-245">Kun juuri lisäämäsi rivi on yhä valittuna **Sijaintidirektiivin toiminnot** -pikavälilehdessä, valitse **Muokkaa kyselyä** ja avaa valintaruutu, jossa voit muokata toiminnon kyselyä.</span><span class="sxs-lookup"><span data-stu-id="36874-245">While the line that you just added is still selected on the **Location directive actions** FastTab, select **Edit query** to open a dialog box where you can edit the query for the action.</span></span>
1. <span data-ttu-id="36874-246">Valitse **Alue**-välilehdessä **Lisää**, jos haluat lisätä uuden rivin kyselyyn.</span><span class="sxs-lookup"><span data-stu-id="36874-246">On the **Range** tab, select **Add** to add a row to the query.</span></span>
1. <span data-ttu-id="36874-247">Aseta uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="36874-247">In the new row, set the following values:</span></span>

    - <span data-ttu-id="36874-248">**Taulu:** *Sijainnit*</span><span class="sxs-lookup"><span data-stu-id="36874-248">**Table:** *Locations*</span></span>
    - <span data-ttu-id="36874-249">**Johdettu taulu:** *Sijainnit*</span><span class="sxs-lookup"><span data-stu-id="36874-249">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="36874-250">**Kenttä:** *Sijainti*</span><span class="sxs-lookup"><span data-stu-id="36874-250">**Field:** *Location*</span></span>
    - <span data-ttu-id="36874-251">**Kriteerit:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="36874-251">**Criteria:** *QMS*</span></span>

    <span data-ttu-id="36874-252">*QMS*-sijainti on laadun varastosijainti.</span><span class="sxs-lookup"><span data-stu-id="36874-252">The *QMS* location is a warehouse location for quality.</span></span>

1. <span data-ttu-id="36874-253">Sulje valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="36874-253">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="36874-254">Nyt sinun on muutettava ostotilauksen sijaintidirektiivien järjestystä varastolle *51*.</span><span class="sxs-lookup"><span data-stu-id="36874-254">You must now change the sequence of purchase order location directives for warehouse *51*.</span></span> <span data-ttu-id="36874-255">Tallenna uusi *51 - kohdelaatu* -sijaintidirektiivi, päivitä sivu ja valitse sijaintidirektiivi luettelosta.</span><span class="sxs-lookup"><span data-stu-id="36874-255">Save the new *51 To Quality* location directive, refresh the page, and select the location directive in the list.</span></span> <span data-ttu-id="36874-256">Käytä sitten toimintoruudun **Siirrä ylös**- ja **Siirrä alas** -painikkeita, jos haluat sijoittaa sijaintidirektiivin varastoon *51* alla mainitussa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="36874-256">Then use the **Move up** and **Move down** buttons on the Action Pane to put the location directive for warehouse *51* in the following order.</span></span> <span data-ttu-id="36874-257">(Ennen kuin valitset **Siirrä ylös**- tai **Siirrä alas** -painikkeen, valitse sijaintidirektiivi luettelosta.)</span><span class="sxs-lookup"><span data-stu-id="36874-257">(Before you select **Move up** or **Move down**, you must select a location directive in the list.)</span></span>

    1. <span data-ttu-id="36874-258">51 - kohdelaatu</span><span class="sxs-lookup"><span data-stu-id="36874-258">51 To Quality</span></span>
    2. <span data-ttu-id="36874-259">51 - ostotilaus, suora</span><span class="sxs-lookup"><span data-stu-id="36874-259">51 PO Direct</span></span>
    3. <span data-ttu-id="36874-260">51 QMS</span><span class="sxs-lookup"><span data-stu-id="36874-260">51 QMS</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="36874-261">Mobiililaitteen valikkovaihtoehdot</span><span class="sxs-lookup"><span data-stu-id="36874-261">Mobile device menu items</span></span>

<span data-ttu-id="36874-262">Määritä valikkonimike niin, että mobiililaitteet voivat suorittaa **Laaduntarkistus**-toiminnon.</span><span class="sxs-lookup"><span data-stu-id="36874-262">Configure a menu item so that mobile devices can perform the **Quality Check** function.</span></span>

#### <a name="purchase-putaway"></a><span data-ttu-id="36874-263">Oston hyllytys</span><span class="sxs-lookup"><span data-stu-id="36874-263">Purchase putaway</span></span>

1. <span data-ttu-id="36874-264">Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.</span><span class="sxs-lookup"><span data-stu-id="36874-264">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="36874-265">Valitse luettelosta e **Oston hyllytys** -mobiililaitevalikkovaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="36874-265">In the list, select the **Purchase put-away** menu item.</span></span>
1. <span data-ttu-id="36874-266">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="36874-266">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="36874-267">Lisää uusi rivi ruudukkoon **Työluokat**-osassa valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="36874-267">In the **Work classes** section, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="36874-268">Aseta uudelle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="36874-268">In the new row, set the following values:</span></span>

    - <span data-ttu-id="36874-269">**Työluokan tunnus:** *QC-tarkistus*</span><span class="sxs-lookup"><span data-stu-id="36874-269">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="36874-270">Anna aiemmin laadunvalvontatyölle luodun [työluokan](#work-class) nimi.</span><span class="sxs-lookup"><span data-stu-id="36874-270">Enter the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

    - <span data-ttu-id="36874-271">**Työtilauksen tyyppi:** *Laaduntarkistuksen laatu*</span><span class="sxs-lookup"><span data-stu-id="36874-271">**Work order type:** *Quality in quality check*</span></span>

1. <span data-ttu-id="36874-272">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="36874-272">On the Action Pane, select **Save**.</span></span>

#### <a name="purchase-order-line-receiving"></a><span data-ttu-id="36874-273">Ostotilausrivin vastaanotto</span><span class="sxs-lookup"><span data-stu-id="36874-273">Purchase order line receiving</span></span>

1. <span data-ttu-id="36874-274">Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.</span><span class="sxs-lookup"><span data-stu-id="36874-274">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="36874-275">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="36874-275">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="36874-276">Aseta otsikkorivillä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="36874-276">In the header, set the following values:</span></span>

    - <span data-ttu-id="36874-277">**Valikkokohteen nimi:** *Ostotilausrivien vastaanotto*</span><span class="sxs-lookup"><span data-stu-id="36874-277">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="36874-278">**Otsikko:** *Ostotilausrivien vastaanotto*</span><span class="sxs-lookup"><span data-stu-id="36874-278">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="36874-279">**Tila:** *Työ*</span><span class="sxs-lookup"><span data-stu-id="36874-279">**Mode:** *Work*</span></span>
    - <span data-ttu-id="36874-280">**Käytä aiemmin luotua työtä:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="36874-280">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="36874-281">Määritä **Yleiset**-pikavälilehdessä seuraavat arvot.</span><span class="sxs-lookup"><span data-stu-id="36874-281">On the **General** FastTab, set the following values.</span></span> <span data-ttu-id="36874-282">Hyväksy jäljellä olevien kenttien oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="36874-282">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="36874-283">**Työn luomisprosessi:** *Ostotilausrivien vastaanotto ja hyllytys*</span><span class="sxs-lookup"><span data-stu-id="36874-283">**Work creation process:** *Purchase order line receiving and put away*</span></span>
    - <span data-ttu-id="36874-284">**Luo rekisterikilpi:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="36874-284">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="36874-285">**Työmalli:** *51 - ostotilauksen vastaanotto*</span><span class="sxs-lookup"><span data-stu-id="36874-285">**Work template:** *51 PO Receipt*</span></span>

1. <span data-ttu-id="36874-286">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="36874-286">On the Action Pane, select **Save**.</span></span>

#### <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="36874-287">Lisää valikkovaihtoehto mobiililaitteen valikkoon</span><span class="sxs-lookup"><span data-stu-id="36874-287">Add the menu item to a mobile device menu</span></span>

1. <span data-ttu-id="36874-288">Siirry kohtaan **Varastonhallinta \> Asetukset \> Mobiililaite \> Mobiililaitteen valikko**.</span><span class="sxs-lookup"><span data-stu-id="36874-288">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="36874-289">Valitse vasemmanpuoleisessa ruudussa **Saapuvat**-valikko.</span><span class="sxs-lookup"><span data-stu-id="36874-289">In the left pane, select the **Inbound** menu.</span></span>
1. <span data-ttu-id="36874-290">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="36874-290">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="36874-291">Valitse **Käytettävissä olevat valikot ja valikon vaihtoehdot** -sarakkeessa uusi **Ostotilausrivien vastaanotto** -valikon vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="36874-291">In the **Available menus and menu items** column, select the new **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="36874-292">Siirrä **Ostotilausrivin vastaanotto** oikealla nuolipainikkeella **Valikon rakenne** -sarakkeeseen.</span><span class="sxs-lookup"><span data-stu-id="36874-292">Select the right arrow button to move **PO line receiving** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="36874-293">Valitse **Valikon rakenne** -sarakkeessa **Ostotilausrivien vastaanotto** ja valitse sitten ylös- tai alasnuolipainike ja siirrä valikon vaihtoehto haluttuun kohtaan mobiililaitteen valikossa.</span><span class="sxs-lookup"><span data-stu-id="36874-293">In the **Menu structure** column, select **PO line receiving**, and then select the up arrow or down arrow button to move the menu item to the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="36874-294">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="36874-294">On the Action Pane, select **Save**.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="36874-295">Esimerkkiskenaario</span><span class="sxs-lookup"><span data-stu-id="36874-295">Example scenario</span></span>

<span data-ttu-id="36874-296">Kun olet tehnyt kaikki edellä mainitut näytetiedot käytettäviksi ja määrittänyt ne, voit käyttää tätä skenaariota ja kokeilla *Laaduntarkistus*-toimintoa.</span><span class="sxs-lookup"><span data-stu-id="36874-296">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Quality check* feature.</span></span> <span data-ttu-id="36874-297">Tämän skenaarion arvoissa oletetaan, että käsittelet vakionäytetietoja, valittuna on **USMF**-yritys ja että aiemmin tässä ohjeaiheessa kuvatut näytetietueet on valmisteltu.</span><span class="sxs-lookup"><span data-stu-id="36874-297">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="36874-298">Tämä skenaario on myös esimerkki siitä, miten ominaisuutta voidaan käyttää tuotannon määrityksessä.</span><span class="sxs-lookup"><span data-stu-id="36874-298">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="36874-299">Ostotilauksen luominen</span><span class="sxs-lookup"><span data-stu-id="36874-299">Create a purchase order</span></span>

1. <span data-ttu-id="36874-300">Siirry kohtaan **Hankinta ja alihankinta \> Ostotilaukset \> Kaikki ostotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="36874-300">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="36874-301">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="36874-301">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="36874-302">Aseta **Luo ostotilaus** -valintaikkunassa seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="36874-302">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="36874-303">**Toimittajan tili:** *104*</span><span class="sxs-lookup"><span data-stu-id="36874-303">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="36874-304">**Varasto**: *51*</span><span class="sxs-lookup"><span data-stu-id="36874-304">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="36874-305">Valitse **OK**, jos haluat sulkea valintaikkunan ja avata uuden ostotilauksen.</span><span class="sxs-lookup"><span data-stu-id="36874-305">Select **OK** to close the dialog box and open the new purchase order.</span></span>
1. <span data-ttu-id="36874-306">**Ostotilausrivit**-pikavälilehden ruudukko sisältää uuden, tyhjän rivin.</span><span class="sxs-lookup"><span data-stu-id="36874-306">On the **Purchase order lines** FastTab, the grid contains a new, blank line.</span></span> <span data-ttu-id="36874-307">Määritä tälle riville seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="36874-307">On this line, set the following values:</span></span>

    - <span data-ttu-id="36874-308">**Nimiketunnus:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="36874-308">**Item number:** *M9203*</span></span>
    - <span data-ttu-id="36874-309">**Määrä** *3*</span><span class="sxs-lookup"><span data-stu-id="36874-309">**Quantity:** *3*</span></span>
    - <span data-ttu-id="36874-310">**Yksikkö:** *PL*</span><span class="sxs-lookup"><span data-stu-id="36874-310">**Unit:** *PL*</span></span>

1. <span data-ttu-id="36874-311">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="36874-311">On the Action Pane, select **Save**.</span></span>

### <a name="process-quality-check-receiving"></a><span data-ttu-id="36874-312">Käsittele vastaanoton laaduntarkistus</span><span class="sxs-lookup"><span data-stu-id="36874-312">Process quality check receiving</span></span>

<span data-ttu-id="36874-313">Kun ostotilaus on luotu, se voidaan vastaanottaa käyttämällä **Ostotilausrivin vastaanotto** -valikon vaihtoehtoa ja *Laaduntarkistus*-ominaisuuden toimintoja.</span><span class="sxs-lookup"><span data-stu-id="36874-313">After the purchase order has been created, it can be received by using the **PO line receiving** menu item and the functionality of the *Quality check* feature.</span></span>

#### <a name="receive-pallet-1"></a><span data-ttu-id="36874-314">Vastaanota kuormalava 1</span><span class="sxs-lookup"><span data-stu-id="36874-314">Receive pallet 1</span></span>

1. <span data-ttu-id="36874-315">Kirjaudu varastosovellukseen käyttäjänä varastossa *51*.</span><span class="sxs-lookup"><span data-stu-id="36874-315">Sign in to the warehouse app as a user for warehouse *51*.</span></span> <span data-ttu-id="36874-316">(Anna käyttäjätunnukseksi *51* ja salasanaksi *1*.)</span><span class="sxs-lookup"><span data-stu-id="36874-316">(Enter *51* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="36874-317">Siirry kohtaan **Saapuvat \> Ostotilausrivin vastaanotto**.</span><span class="sxs-lookup"><span data-stu-id="36874-317">Go to **Inbound \> PO line receiving**.</span></span>
1. <span data-ttu-id="36874-318">Syötä **PONUM**-kenttään ostotilauksen numero.</span><span class="sxs-lookup"><span data-stu-id="36874-318">In the **PONUM** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="36874-319">Vahvista ostotilausnumero.</span><span class="sxs-lookup"><span data-stu-id="36874-319">Confirm the purchase order number.</span></span>
1. <span data-ttu-id="36874-320">Anna **LINENUM**-kenttään vastaanotettavan ostotilausrivin numero.</span><span class="sxs-lookup"><span data-stu-id="36874-320">In the **LINENUM** field, enter the number of the purchase order line that is being received.</span></span> <span data-ttu-id="36874-321">Koska tilauksella on tässä skenaariossa vain yksi rivi, anna **LINENUM**-kenttään arvo *1* jokaisessa vastaanottovaiheessa.</span><span class="sxs-lookup"><span data-stu-id="36874-321">Because the order has only one line in this scenario, you will enter *1* in the **LINENUM** field for each receiving step.</span></span>
1. <span data-ttu-id="36874-322">Vahvista rivinumero.</span><span class="sxs-lookup"><span data-stu-id="36874-322">Confirm the line number.</span></span>
1. <span data-ttu-id="36874-323">Syötä vastaanottomäärä **MÄÄRÄ**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="36874-323">In the **QTY** field, enter the quantity to receive.</span></span> <span data-ttu-id="36874-324">Koska ostotilaus koskee kolmea kuormalavaa (*PL*) tässä skenaariossa ja vastaanottovaiheita on kolme, jokaisessa vastaanottovaiheessa annetaan **MÄÄRÄ**-kentän arvoksi *1*.</span><span class="sxs-lookup"><span data-stu-id="36874-324">Because the purchase order is for three pallets (*PL*) in this scenario, and there are three receiving steps, you will enter *1* in the **QTY** field for each receiving step.</span></span>
1. <span data-ttu-id="36874-325">Vahvista määrä.</span><span class="sxs-lookup"><span data-stu-id="36874-325">Confirm the quantity.</span></span>

    <span data-ttu-id="36874-326">Näkyviin tulevalla **Laaduntarkistus**-sivulla ei ole syöttökenttiä.</span><span class="sxs-lookup"><span data-stu-id="36874-326">The **Quality check** page that appears has no entry fields.</span></span> <span data-ttu-id="36874-327">Se sisältää vain vahvistuksen (valintamerkin) painikkeen sivun alaosassa ja valikkopainikkeen (**≡**) sivun yläosassa.</span><span class="sxs-lookup"><span data-stu-id="36874-327">It has only the confirmation (check mark) button at the bottom and the Menu button (**≡**) at the top.</span></span> <span data-ttu-id="36874-328">(Valikkopainiketta kutsutaan joskus neljän viivan painikkeeksi tai hampurilaispainikkeeksi.) Laaduntarkistusprosessin nopeuttamiseksi käyttäjä voi vahvistaa **Laaduntarkistus**-sivun kuormalavan läpäistyä laaduntarkistuksen.</span><span class="sxs-lookup"><span data-stu-id="36874-328">(The Menu button is sometimes referred to as the hamburger or the hamburger button.) To expedite the quality check process, when the pallet passes the quality check, the user just confirms the **Quality check** page.</span></span>

    <span data-ttu-id="36874-329">![Laaduntarkistus-sivu](media/quality-check.png "Laaduntarkistus-sivu")</span><span class="sxs-lookup"><span data-stu-id="36874-329">![Quality check page](media/quality-check.png "Quality check page")</span></span>

1. <span data-ttu-id="36874-330">Valitse vahvistuspainike, jos haluat hyväksyä rivin 1 kuormalavan 1 laaduntarkistuksen.</span><span class="sxs-lookup"><span data-stu-id="36874-330">Select the confirmation button to pass the quality check for pallet 1 from line 1.</span></span>

    <span data-ttu-id="36874-331">Näkyviin tulevalla **Ostotilaukset: Hyllytys** -sivulla ovat seuraavat hyllytystyön tiedot:</span><span class="sxs-lookup"><span data-stu-id="36874-331">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="36874-332">**SIJAINTI:** Järjestelmän määrittämä sijainti</span><span class="sxs-lookup"><span data-stu-id="36874-332">**LOC:** The system determined location</span></span>

        <span data-ttu-id="36874-333">Tämä sijainti on ostotilauksen vastaanotolle määritetty hyllytyssijainti.</span><span class="sxs-lookup"><span data-stu-id="36874-333">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="36874-334">**RK:** Järjestelmän luoma rekisterikilpitunnus</span><span class="sxs-lookup"><span data-stu-id="36874-334">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="36874-335">**Nimike:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="36874-335">**Item:** *M9203*</span></span>
    - <span data-ttu-id="36874-336">**Määrä:** *1 KL: 100 kpl*</span><span class="sxs-lookup"><span data-stu-id="36874-336">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="36874-337">Nimikkeen kuvaus näytetään myös.</span><span class="sxs-lookup"><span data-stu-id="36874-337">The item description is also shown.</span></span>

1. <span data-ttu-id="36874-338">Vahvista hyllytystyö.</span><span class="sxs-lookup"><span data-stu-id="36874-338">Confirm the putaway work.</span></span>

    <span data-ttu-id="36874-339">Ostotilausrivin vastaanoton **Tehtävä**-sivulla on Työ valmis -sanoma.</span><span class="sxs-lookup"><span data-stu-id="36874-339">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="36874-340">**LINENUM**-kenttä on käytettävissä, joten voit aloittaa seuraavan kuormalavan vastaanoton.</span><span class="sxs-lookup"><span data-stu-id="36874-340">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

#### <a name="receive-pallet-2"></a><span data-ttu-id="36874-341">Vastaanota kuormalava 2</span><span class="sxs-lookup"><span data-stu-id="36874-341">Receive pallet 2</span></span>

<span data-ttu-id="36874-342">Tässä skenaariossa kuormalava 2 hylätään.</span><span class="sxs-lookup"><span data-stu-id="36874-342">For this scenario, pallet 2 will be rejected.</span></span>

1. <span data-ttu-id="36874-343">Anna **LINENUM**-kenttään *1* ja vahvista rivinumero.</span><span class="sxs-lookup"><span data-stu-id="36874-343">In the **LINENUM** field, enter *1*, and confirm the line number.</span></span>
1. <span data-ttu-id="36874-344">**MÄÄRÄ**-kenttä on nyt käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="36874-344">The **QTY** field is now available.</span></span> <span data-ttu-id="36874-345">Anna arvo *1* ja vahvista määrä.</span><span class="sxs-lookup"><span data-stu-id="36874-345">Enter *1*, and confirm the quantity.</span></span>

    <span data-ttu-id="36874-346">**Laaduntarkistus**-sivu tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="36874-346">The **Quality check** page appears.</span></span> <span data-ttu-id="36874-347">Tässä vastaanotossa kuormalava hylätään laadun osalta. Kuormalava asetetaan *QMS*-laatusijaintiin.</span><span class="sxs-lookup"><span data-stu-id="36874-347">For this receipt, the pallet will be rejected for quality, and it will be put into the *QMS* quality location.</span></span>

1. <span data-ttu-id="36874-348">Valitse valikkopainike (**≡**) sivun yläosassa ja valitse sitten valikosta **Hylkää**.</span><span class="sxs-lookup"><span data-stu-id="36874-348">Select the Menu button (**≡**) at the top of the page, and then, on the menu, select **Reject**.</span></span>
1. <span data-ttu-id="36874-349">Anna näkyviin tulevalla **Tehtävä**-sivulla **QMS** *hyllytyssijainniksi* ja lähetä kuormalava lisätarkastukseen.</span><span class="sxs-lookup"><span data-stu-id="36874-349">On the **Task** page that appears, enter **QMS** as the *Put* location to send the pallet to for further inspection.</span></span>

    <span data-ttu-id="36874-350">Näkyviin tulevalla **Laaduntarkistuksen laatu: Hyllytys** -sivulla ovat seuraavat hyllytystyön tiedot:</span><span class="sxs-lookup"><span data-stu-id="36874-350">The **Quality in quality check: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="36874-351">**SIJAINTI:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="36874-351">**LOC:** *QMS*</span></span>

        <span data-ttu-id="36874-352">Tämä sijainti on hylätyn laadun vastaanotolle määritetty hyllytyssijainti.</span><span class="sxs-lookup"><span data-stu-id="36874-352">This location is the designated putaway location for rejected quality receiving.</span></span>

    - <span data-ttu-id="36874-353">**RK:** Järjestelmän luoma rekisterikilpitunnus</span><span class="sxs-lookup"><span data-stu-id="36874-353">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="36874-354">**Nimike:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="36874-354">**Item:** *M9203*</span></span>
    - <span data-ttu-id="36874-355">**Määrä:** *1 KL: 100 kpl*</span><span class="sxs-lookup"><span data-stu-id="36874-355">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="36874-356">Nimikkeen kuvaus näytetään myös.</span><span class="sxs-lookup"><span data-stu-id="36874-356">The item description is also shown.</span></span>

1. <span data-ttu-id="36874-357">Vahvista hyllytystyö.</span><span class="sxs-lookup"><span data-stu-id="36874-357">Confirm the putaway work.</span></span>

    <span data-ttu-id="36874-358">Ostotilausrivin vastaanoton **Tehtävä**-sivulla on Työ valmis -sanoma.</span><span class="sxs-lookup"><span data-stu-id="36874-358">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="36874-359">**LINENUM**-kenttä on käytettävissä, joten voit aloittaa seuraavan kuormalavan vastaanoton.</span><span class="sxs-lookup"><span data-stu-id="36874-359">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

<span data-ttu-id="36874-360">Olet nyt tehnyt laatutarkistuksen ja luonut hylätyn kuormalavan laatutilauksen.</span><span class="sxs-lookup"><span data-stu-id="36874-360">You've now completed the quality check and created a quality order for the rejected pallet.</span></span> <span data-ttu-id="36874-361">Jos haluat tarkastella luotua laatutilausta, siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Laadunhallinta \> Laatutilaukset**.</span><span class="sxs-lookup"><span data-stu-id="36874-361">To view the order that was created, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="36874-362">Laatutilauksen testausta voidaan nyt käsitellä.</span><span class="sxs-lookup"><span data-stu-id="36874-362">Quality order testing can now be processed.</span></span> <span data-ttu-id="36874-363">Tässä ohjeaiheessa ei käsitellä laatutestausta.</span><span class="sxs-lookup"><span data-stu-id="36874-363">Quality testing isn't covered in this topic.</span></span>

<span data-ttu-id="36874-364">Lisätietoja laadunhallinnasta on kohdassa [Laadunhallinnan yleiskuvaus](../inventory/enable-quality-management.md)</span><span class="sxs-lookup"><span data-stu-id="36874-364">For more information about quality management, see [Quality management overview](../inventory/enable-quality-management.md)</span></span>

#### <a name="receive-pallet-3"></a><span data-ttu-id="36874-365">Vastaanota kuormalava 3</span><span class="sxs-lookup"><span data-stu-id="36874-365">Receive pallet 3</span></span>

<span data-ttu-id="36874-366">Tässä skenaariossa kuormalava 3 hyväksytään.</span><span class="sxs-lookup"><span data-stu-id="36874-366">For this scenario, pallet 3 will be accepted.</span></span>

1. <span data-ttu-id="36874-367">Anna **LINENUM**-kenttään *1* ja vahvista rivinumero.</span><span class="sxs-lookup"><span data-stu-id="36874-367">In the **LINENUM** field, enter *1*, and confirm the line number.</span></span>
1. <span data-ttu-id="36874-368">**MÄÄRÄ**-kenttä on nyt käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="36874-368">The **QTY** field is now available.</span></span> <span data-ttu-id="36874-369">Anna arvo *1* ja vahvista määrä.</span><span class="sxs-lookup"><span data-stu-id="36874-369">Enter *1*, and confirm the quantity.</span></span>

    <span data-ttu-id="36874-370">**Laaduntarkistus**-sivu tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="36874-370">The **Quality check** page appears.</span></span> <span data-ttu-id="36874-371">Tässä vastaanotossa kuormalava hyväksytään laadun osalta. Kuormalava asetetaan joukkohyllytyssijaintiin.</span><span class="sxs-lookup"><span data-stu-id="36874-371">For this receipt, the pallet will be accepted for quality, and it will be put into a bulk putaway location.</span></span>

1. <span data-ttu-id="36874-372">Valitse vahvistuspainike, jos haluat hyväksyä laaduntarkistuksen.</span><span class="sxs-lookup"><span data-stu-id="36874-372">Select the confirmation button to pass the quality check.</span></span>

    <span data-ttu-id="36874-373">Näkyviin tulevalla **Ostotilaukset: Hyllytys** -sivulla ovat seuraavat hyllytystyön tiedot:</span><span class="sxs-lookup"><span data-stu-id="36874-373">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="36874-374">**SIJAINTI:** Järjestelmän määrittämä sijainti</span><span class="sxs-lookup"><span data-stu-id="36874-374">**LOC:** The system determined location</span></span>

        <span data-ttu-id="36874-375">Tämä sijainti on ostotilauksen vastaanotolle määritetty hyllytyssijainti.</span><span class="sxs-lookup"><span data-stu-id="36874-375">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="36874-376">**RK:** Järjestelmän luoma rekisterikilpitunnus</span><span class="sxs-lookup"><span data-stu-id="36874-376">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="36874-377">**Nimike:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="36874-377">**Item:** *M9203*</span></span>
    - <span data-ttu-id="36874-378">**Määrä:** *1 KL: 100 kpl*</span><span class="sxs-lookup"><span data-stu-id="36874-378">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="36874-379">Nimikkeen kuvaus näytetään myös.</span><span class="sxs-lookup"><span data-stu-id="36874-379">The item description is also shown.</span></span>

1. <span data-ttu-id="36874-380">Vahvista hyllytystyö.</span><span class="sxs-lookup"><span data-stu-id="36874-380">Confirm the putaway work.</span></span>

    <span data-ttu-id="36874-381">Ostotilausrivin vastaanoton **Tehtävä**-sivulla on Työ valmis -sanoma.</span><span class="sxs-lookup"><span data-stu-id="36874-381">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="36874-382">**LINENUM**-kenttä on käytettävissä, joten voit aloittaa seuraavan kuormalavan vastaanoton.</span><span class="sxs-lookup"><span data-stu-id="36874-382">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

1. <span data-ttu-id="36874-383">Valitse valikkopainike (**≡**) sivun yläosassa ja valitse sitten valikosta **Peruuta**, jos haluat palata valikkoon.</span><span class="sxs-lookup"><span data-stu-id="36874-383">Select the Menu button (**≡**) at the top of the page, and then, on the menu, select **Cancel** to return to the menu.</span></span>

<span data-ttu-id="36874-384">Voit nyt sulkea mobiilisovelluksen.</span><span class="sxs-lookup"><span data-stu-id="36874-384">You can now close the mobile app.</span></span>
