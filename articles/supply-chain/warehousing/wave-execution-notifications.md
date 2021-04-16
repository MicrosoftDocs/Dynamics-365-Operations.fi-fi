---
title: Aallon suoritusilmoitukset
description: Tässä ohjeaiheessa käsitellään aallon suoritusilmoituksia ja niiden määrittämistä.
author: mirzaab
ms.date: 04/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2022-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 0a61aff10234f40f14d603852be30fec3ba83647
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838079"
---
# <a name="wave-execution-notifications"></a><span data-ttu-id="34f01-103">Aallon suoritusilmoitukset</span><span class="sxs-lookup"><span data-stu-id="34f01-103">Wave execution notifications</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="34f01-104">*Aallon suoritusilmoitukset* -ominaisuus käyttää liiketoimintatapahtumia ja toimintokeskusta aaltojen suorittamiseen liittyvien ilmoitusten toimittamiseen.</span><span class="sxs-lookup"><span data-stu-id="34f01-104">The *Wave execution notifications* feature uses business events and the Action center to deliver notifications that are related to wave execution.</span></span> <span data-ttu-id="34f01-105">Sen avulla voit määrittää ilmoituksia tuottavien tapahtumien tyypit, niitä luovat varastot ja ne vastaanottavat käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="34f01-105">It lets you specify the types of events that generate notifications, the warehouses that generate them, and the users who receive them.</span></span>

<span data-ttu-id="34f01-106">Siirtymispalkin oikeassa sivussa oleva **Näytä viestit** -painike (kellosymboli) ilmaisee, milloin toimintokeskussanoma on nykyisen käyttäjän käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="34f01-106">The **Show messages** button (bell symbol) on the right side of the navigation bar indicates when an Action center message is available for the current user.</span></span> <span data-ttu-id="34f01-107">Käyttäjä voi avata toimintokeskuksen ja tarkastella viestejä valitsemalla **Näytä viestit** -painikkeen.</span><span class="sxs-lookup"><span data-stu-id="34f01-107">The user can select the **Show messages** button to open the Action center and review the messages.</span></span>

<span data-ttu-id="34f01-108">Liiketoimintatapahtumat tapahtuvat, kun liiketoimintaprosesseja suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="34f01-108">Business events occur when business processes are run.</span></span> <span data-ttu-id="34f01-109">Liiketoimintaprosessit koostuvat tehtävistä.</span><span class="sxs-lookup"><span data-stu-id="34f01-109">Business processes are made up of tasks.</span></span> <span data-ttu-id="34f01-110">Liiketoimintaprosessin aikana siihen osallistuvat käyttäjät suorittavat liiketoimintatoimintoja näiden tehtävien suorittamiseksi.</span><span class="sxs-lookup"><span data-stu-id="34f01-110">During a business process, the users who participate in it perform business actions to complete those tasks.</span></span> <span data-ttu-id="34f01-111">Liiketoimintatapahtumat tarjoavat mekanismin, jonka avulla ulkoiset järjestelmät saavat ilmoituksia Finance and Operations -sovelluksista.</span><span class="sxs-lookup"><span data-stu-id="34f01-111">Business events provide a mechanism that lets external systems receive notifications from Finance and Operations applications.</span></span> <span data-ttu-id="34f01-112">Tällä tavoin järjestelmät voivat suorittaa liiketoimintatoimintoja vastauksena liiketoimintatapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="34f01-112">In this way, the systems can perform business actions in response to the business events.</span></span> <span data-ttu-id="34f01-113">Lisätietoja on kohdassa [Liiketoimintatapahtumien yleiskatsaus](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span><span class="sxs-lookup"><span data-stu-id="34f01-113">For more information, see [Business events overview](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span></span>

## <a name="turn-on-the-wave-execution-notifications-feature"></a><span data-ttu-id="34f01-114">Aallon suoritusilmoitukset -toiminnon ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="34f01-114">Turn on the Wave execution notifications feature</span></span>

<span data-ttu-id="34f01-115">Ennen kuin voit käyttää *Aallon suoritusilmoitukset* -toimintoa, sen pitää olla otettu käyttöön järjestelmässäsi.</span><span class="sxs-lookup"><span data-stu-id="34f01-115">Before you can use the *Wave execution notifications* feature, it must be turned on in your system.</span></span> <span data-ttu-id="34f01-116">Järjestelmänvalvojat voivat käyttää [Toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) työtilaa tarkistaakseen toiminnon tilan sekä laittaa sen päälle, jos sitä vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="34f01-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="34f01-117">Tässä tapauksessa toiminto näkyy seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="34f01-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="34f01-118">**Moduuli:** *Varastonhallinta*</span><span class="sxs-lookup"><span data-stu-id="34f01-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="34f01-119">**Ominaisuuden nimi:** *Aallon suoritusilmoitukset*</span><span class="sxs-lookup"><span data-stu-id="34f01-119">**Feature name:** *Wave execution notifications*</span></span>

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a><span data-ttu-id="34f01-120">Skenaario: Aallon eräsuorituksen ilmoitusten lähettäminen toimintokeskukseen</span><span class="sxs-lookup"><span data-stu-id="34f01-120">Scenario: Send wave batch execution notifications to the Action center</span></span>

<span data-ttu-id="34f01-121">Tässä skenaariossa näkyy päästä päähän -työnkulku ilmoitusten lähettämiseen aallon eräsuorituksen virheist tietylle roolille toimintokeskuksen kautta.</span><span class="sxs-lookup"><span data-stu-id="34f01-121">This scenario shows the end-to-end flow for sending notifications about wave batch execution errors to a specific role via the Action center.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="34f01-122">Demotietojen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="34f01-122">Make demo data available</span></span>

<span data-ttu-id="34f01-123">Tämän skenaarion käyttäminen edellyttää, että demotiedot on asennettu ja että **USMF**-yritys on valittu.</span><span class="sxs-lookup"><span data-stu-id="34f01-123">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a><span data-ttu-id="34f01-124">Varmista, että aallot suoritetaan erätilassa</span><span class="sxs-lookup"><span data-stu-id="34f01-124">Make sure that waves are run in batch mode</span></span>

1. <span data-ttu-id="34f01-125">Siirry kohtaan **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**.</span><span class="sxs-lookup"><span data-stu-id="34f01-125">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="34f01-126">Määritä **Aallon käsittely** -pikavälilehdessä **Aallon käsittelyn eräryhmä** -arvoksi *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="34f01-126">On the **Wave processing** FastTab, set the **Process waves in batch** option to *Yes*.</span></span>

> [!NOTE]
> <span data-ttu-id="34f01-127">Jos haluat poistaa aallon eräsuorituksen ilmoitukset käytöstä, määritä **Poista aallon käsittelyn eräilmoitukset käytöstä** -asetuksen arvoksi *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="34f01-127">If you want to disable wave batch execution notifications, set the **Disable wave processing batch notifications** option to *Yes*.</span></span>

### <a name="configure-a-wave-notification-policy"></a><span data-ttu-id="34f01-128">Aallon ilmoituskäytännön määrittäminen</span><span class="sxs-lookup"><span data-stu-id="34f01-128">Configure a wave notification policy</span></span>

<span data-ttu-id="34f01-129">Aallon ilmoituskäytännöt määrittävät lähetetyt ilmoitustyypit ja käyttäjät, joille ilmoitetaan.</span><span class="sxs-lookup"><span data-stu-id="34f01-129">Wave notification policies define the types of notifications that are sent and the users who are notified.</span></span>

1. <span data-ttu-id="34f01-130">Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aallon ilmoituskäytännöt**.</span><span class="sxs-lookup"><span data-stu-id="34f01-130">Go to **Warehouse management \> Setup \> Waves \> Wave notification policies**.</span></span>
1. <span data-ttu-id="34f01-131">Luo tietue, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="34f01-131">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="34f01-132">**Aallon ilmoituskäytäntö:** *24BatchError*</span><span class="sxs-lookup"><span data-stu-id="34f01-132">**Wave notification policy:** *24BatchError*</span></span>
    - <span data-ttu-id="34f01-133">**Kuvaus:** *Varaston 24 aallon erävirhe*</span><span class="sxs-lookup"><span data-stu-id="34f01-133">**Description:** *Warehouse 24 wave batch error*</span></span>
    - <span data-ttu-id="34f01-134">**Lähetä ilmoitus:** *Vain virhe*</span><span class="sxs-lookup"><span data-stu-id="34f01-134">**Send notification on:** *Error only*</span></span>
    - <span data-ttu-id="34f01-135">**Roolille:** *Järjestelmänvalvojan*</span><span class="sxs-lookup"><span data-stu-id="34f01-135">**To role:** *System administrator*</span></span>

        > [!NOTE]
        > <span data-ttu-id="34f01-136">Koska tässä skenaariossa käytetään esittelytietoja, *Järjestelmänvalvoja*-rooli valitaan yksinkertaisuuden vuoksi.</span><span class="sxs-lookup"><span data-stu-id="34f01-136">Because this scenario uses demo data, the *System administrator* role is selected for the sake of simplicity.</span></span> <span data-ttu-id="34f01-137">Koska olet kirjautuneena järjestelmänvalvojana, saat ilmoitukset.</span><span class="sxs-lookup"><span data-stu-id="34f01-137">Therefore, because you're signed in as a system administrator user, you will receive the notifications.</span></span> <span data-ttu-id="34f01-138">Käytännössä kannattaa kuitenkin yleensä valita tarkempi rooli, jos haluat ilmoittaa aallon eräsuorituksen virheistä, kuten *Varaston esimies* -rooli.</span><span class="sxs-lookup"><span data-stu-id="34f01-138">However, in practice, you should usually select a more specific role to notify about wave batch execution errors, such as *Warehouse manager*.</span></span>

1. <span data-ttu-id="34f01-139">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="34f01-139">On the Action Pane, select **Save**.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="34f01-140">Aaltomallin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="34f01-140">Configure a wave template</span></span>

<span data-ttu-id="34f01-141">Aaltomallin avulla tietyt aaltomenetelmien esiintymät voidaan linkittää vastaavaan aallon etikettimalleihin.</span><span class="sxs-lookup"><span data-stu-id="34f01-141">Wave templates let you link specific instances of wave methods to corresponding wave label templates.</span></span>

1. <span data-ttu-id="34f01-142">Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aaltomallit**.</span><span class="sxs-lookup"><span data-stu-id="34f01-142">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="34f01-143">Määritä luetteloruudussa **Aaltomallin tyyppi** -kentän arvoksi *Toimitus* ja valitse sitten varastolle 24 *24 Shipping Default* -aaltomalli.</span><span class="sxs-lookup"><span data-stu-id="34f01-143">In the list pane, set the **Wave template type** field to *Shipping*, and then select the *24 Shipping Default* wave template for warehouse 24.</span></span>
1. <span data-ttu-id="34f01-144">Määritä **Yleiset**-pikavälilehden **Aallon ilmoituskäytäntö** -kentän arvoksi *24BatchError*.</span><span class="sxs-lookup"><span data-stu-id="34f01-144">On the **General** FastTab, set the **Wave notification policy** field to *24BatchError*.</span></span>

### <a name="configure-a-work-template"></a><span data-ttu-id="34f01-145">Työmallin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="34f01-145">Configure a work template</span></span>

<span data-ttu-id="34f01-146">Työmalleja käytetään aaltojen suorittamisen aikana työn luomiseen.</span><span class="sxs-lookup"><span data-stu-id="34f01-146">Work templates are used during wave execution to generate work.</span></span> <span data-ttu-id="34f01-147">Tässä skenaariossa aallon suorittamisen pitäisi aiheuttaa virhe.</span><span class="sxs-lookup"><span data-stu-id="34f01-147">For this scenario, wave execution should trigger an error.</span></span> <span data-ttu-id="34f01-148">Määrittämällä työmallikyselyn käyttämään olematonta varastoa varmistat, että aaltojen suorittaminen epäonnistuu, ja siksi ilmoitus lähetetään.</span><span class="sxs-lookup"><span data-stu-id="34f01-148">By setting the work template query to use a nonexistent warehouse, you will ensure that wave execution fails and therefore sends a notification.</span></span>

1. <span data-ttu-id="34f01-149">Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työmallit**.</span><span class="sxs-lookup"><span data-stu-id="34f01-149">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="34f01-150">Määritä luetteloruudussa **Työmallin tyyppi** -kentän arvoksi *Myyntitilaukset* ja valitse sitten varastolle 24 *24 SO Stage* -työmalli.</span><span class="sxs-lookup"><span data-stu-id="34f01-150">In the list pane, set the **Work template type** field to *Sales orders* and then select the *24 SO Stage* work template for warehouse 24.</span></span>
1. <span data-ttu-id="34f01-151">Valitse toimintoruudussa **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="34f01-151">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="34f01-152">Muokkaa kyselyeditorin valintaikkunan **Alue**-välilehdessä seuraavaa riviä (tai lisää se, jos sitä ei ole):</span><span class="sxs-lookup"><span data-stu-id="34f01-152">In the query editor dialog box, on the **Range** tab, edit the following row (or add it if it doesn't exist):</span></span>

    - <span data-ttu-id="34f01-153">**Taulukko:** *Väliaikaiset työtapahtumat*</span><span class="sxs-lookup"><span data-stu-id="34f01-153">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="34f01-154">**Johdettu taulukko:** *Väliaikaiset työtapahtumat*</span><span class="sxs-lookup"><span data-stu-id="34f01-154">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="34f01-155">**Kenttä:** *Varasto*</span><span class="sxs-lookup"><span data-stu-id="34f01-155">**Field:** *Warehouse*</span></span>
    - <span data-ttu-id="34f01-156">**Ehdot:** Muuta arvosta *24* arvoon *Virhe*.</span><span class="sxs-lookup"><span data-stu-id="34f01-156">**Criteria:** Change the value from *24* to *Error*.</span></span>

1. <span data-ttu-id="34f01-157">Valitse **OK** ja vahvista muutos.</span><span class="sxs-lookup"><span data-stu-id="34f01-157">Select **OK**, and confirm the change.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="34f01-158">Myyntitilauksen luominen ja sen vapauttaminen varastoon</span><span class="sxs-lookup"><span data-stu-id="34f01-158">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="34f01-159">Valitse **Myynti ja markkinointi \> Myyntitilaus \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="34f01-159">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="34f01-160">Luo myyntitilaus, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="34f01-160">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="34f01-161">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="34f01-161">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="34f01-162">**Varasto**: *24*</span><span class="sxs-lookup"><span data-stu-id="34f01-162">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="34f01-163">Lisää **Myyntitilausrivit**-pikavälilehdessä myyntitilausrivi, jonka asetukset ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="34f01-163">On the **Sales order lines** FastTab, add a sales order line that has the following settings:</span></span>

    - <span data-ttu-id="34f01-164">**Nimiketunnus:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="34f01-164">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="34f01-165">**Määrä** *10*</span><span class="sxs-lookup"><span data-stu-id="34f01-165">**Quantity:** *10*</span></span>

    > [!NOTE]
    > <span data-ttu-id="34f01-166">Nämä nimikkeet ja määrät ovat vain esimerkkejä.</span><span class="sxs-lookup"><span data-stu-id="34f01-166">These items and quantities are only examples.</span></span> <span data-ttu-id="34f01-167">Määritetyssä varastossa on oltava riittävästi saldoa.</span><span class="sxs-lookup"><span data-stu-id="34f01-167">The specified warehouse must contain enough stock.</span></span>

1. <span data-ttu-id="34f01-168">Kun uusi rivi on edelleen valittuna **Myyntitilausrivit**-pikavälilehdessä, valitse työnkalurivillä **Varasto \> Varaus**.</span><span class="sxs-lookup"><span data-stu-id="34f01-168">While the new line is still selected on the **Sales order lines** FastTab, select **Inventory \> Reservation** on the toolbar.</span></span>
1. <span data-ttu-id="34f01-169">Valitse **Varaus**-sivun toimintoruudussa kohta **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="34f01-169">On the **Reservation** page, on the Action Pane, select **Reserve lot**.</span></span> <span data-ttu-id="34f01-170">Sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="34f01-170">Then close the page.</span></span>
1. <span data-ttu-id="34f01-171">Valitse toimintoruudussa **Varasto**-välilehdellä **Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="34f01-171">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

### <a name="notifications-from-wave-batch-job-execution"></a><span data-ttu-id="34f01-172">Ilmoitukset aallon erätyön suorituksesta</span><span class="sxs-lookup"><span data-stu-id="34f01-172">Notifications from wave batch job execution</span></span>

<span data-ttu-id="34f01-173">Liiketoimintatapahtumien määritysten mukaan saat lopulta ilmoituksen aallon suorittamisen epäonnistumisesta.</span><span class="sxs-lookup"><span data-stu-id="34f01-173">Depending on the setup of your business events, you will eventually receive a notification about wave execution failure.</span></span> <span data-ttu-id="34f01-174">Toimintokeskuksen sanoma muistuttaa seuraavaa esimerkkiä ja sisältää linkin epäonnistuneeseen aaltoon.</span><span class="sxs-lookup"><span data-stu-id="34f01-174">The Action center message will resemble the following example and will include a link to the wave that failed.</span></span>

> <span data-ttu-id="34f01-175">**Virhe aallon suorituksen aikana**</span><span class="sxs-lookup"><span data-stu-id="34f01-175">**Error during wave execution**</span></span>  
> <span data-ttu-id="34f01-176">Virhe suoritettavissa aaltoa USMF-000000001.</span><span class="sxs-lookup"><span data-stu-id="34f01-176">An error occurred while executing wave USMF-000000001.</span></span>  
> <span data-ttu-id="34f01-177">Viimeiset viestit: Töitä ei luotu aallolle USMF-000000001.</span><span class="sxs-lookup"><span data-stu-id="34f01-177">Last messages: No Work was created for Wave USMF-000000001.</span></span>
>
> <span data-ttu-id="34f01-178">**TILA**</span><span class="sxs-lookup"><span data-stu-id="34f01-178">**STATUS**</span></span>  
> <span data-ttu-id="34f01-179">Käytössä</span><span class="sxs-lookup"><span data-stu-id="34f01-179">Active</span></span>
>
> <span data-ttu-id="34f01-180">Avoimen aallon tiedot</span><span class="sxs-lookup"><span data-stu-id="34f01-180">Open wave details</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
