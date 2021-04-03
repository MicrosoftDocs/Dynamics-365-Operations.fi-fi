---
title: Työtilauksien luonti
description: Tässä ohjeaiheessa selitetään, miten työtilaukset luodaan käyttöomaisuuden hallinnassa.
author: johanhoffmann
manager: tfehr
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePoolsOpen
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 76306fb31e7e5297e6a5d64b97b5bd09b64349ee
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500571"
---
# <a name="creating-work-orders"></a><span data-ttu-id="6957f-103">Työtilauksien luonti</span><span class="sxs-lookup"><span data-stu-id="6957f-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6957f-104">Kun ennaltaehkäisevät ylläpitotyöt on aikataulutettu, seuraava vaihe on niiden työtilausten luominen.</span><span class="sxs-lookup"><span data-stu-id="6957f-104">After you've scheduled preventive maintenance jobs, the next step is to create work orders for them.</span></span> <span data-ttu-id="6957f-105">Tämä vaihe voidaan suorittaa käyttämällä jotakin ylläpitoaikataulua.</span><span class="sxs-lookup"><span data-stu-id="6957f-105">You can complete this step by using one of the maintenance schedules.</span></span> <span data-ttu-id="6957f-106">Ylläpitoaikataulun aikataulutettujen töiden viitetyypit voivat olla erilaiset, ja niitä käsitellään seuraavassa taulukossa.</span><span class="sxs-lookup"><span data-stu-id="6957f-106">The scheduled jobs in a maintenance schedule can have different reference types, as described in the following table.</span></span>

| <span data-ttu-id="6957f-107">Viitetyyppi</span><span class="sxs-lookup"><span data-stu-id="6957f-107">Reference type</span></span> | <span data-ttu-id="6957f-108">kuvaus</span><span class="sxs-lookup"><span data-stu-id="6957f-108">Description</span></span> |
|---|---|
| <span data-ttu-id="6957f-109">Ylläpitosuunnitelmat</span><span class="sxs-lookup"><span data-stu-id="6957f-109">Maintenance plans</span></span> | <span data-ttu-id="6957f-110">*Aika*- tai *Laskuri*-ylläpitosuunnitelmatyyppiin perustuvat ennaltaehkäisevät ylläpitotyöt.</span><span class="sxs-lookup"><span data-stu-id="6957f-110">Preventive maintenance jobs that are based on the *Time* or *Counter* maintenance plan type.</span></span> |
| <span data-ttu-id="6957f-111">Ylläpitokierrokset</span><span class="sxs-lookup"><span data-stu-id="6957f-111">Maintenance rounds</span></span> | <span data-ttu-id="6957f-112">Useita saman tyyppistä ylläpitoa edellyttäviä resursseja sisältävät ennaltaehkäisevät ylläpitotyöt.</span><span class="sxs-lookup"><span data-stu-id="6957f-112">Preventive maintenance jobs that contain several assets that require a similar type of maintenance.</span></span> |
| <span data-ttu-id="6957f-113">Ylläpitopyyntö</span><span class="sxs-lookup"><span data-stu-id="6957f-113">Maintenance request</span></span> | <span data-ttu-id="6957f-114">Resurssin manuaalisesti luotu ylläpito- tai korjauspyyntö.</span><span class="sxs-lookup"><span data-stu-id="6957f-114">A manually created request for maintenance or repair of an asset.</span></span> <span data-ttu-id="6957f-115">Tämä pyyntö voidaan muuntaa työtilaukseksi.</span><span class="sxs-lookup"><span data-stu-id="6957f-115">This request can be converted to a work order.</span></span> |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a><span data-ttu-id="6957f-116">Työtilausten luominen ylläpitoaikataulun perusteella</span><span class="sxs-lookup"><span data-stu-id="6957f-116">Create work orders based on your maintenance schedule</span></span>

<span data-ttu-id="6957f-117">Ylläpitoaikatauluun perustuvia työtilauksia luodaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6957f-117">To create work orders that are based on your maintenance schedule, follow these steps.</span></span>

1. <span data-ttu-id="6957f-118">Avaa jokin seuraavista sivuista sen mukaan, miten työtilausten aikataulutusnimikkeet valitaan:</span><span class="sxs-lookup"><span data-stu-id="6957f-118">Open one of the following pages, depending on how you want to select schedule items for your work orders:</span></span>

    - <span data-ttu-id="6957f-119">Kaikki ylläpitoaikataulut (**Resurssien hallinta \> Hallinta-aikataulu \>Kaikki ylläpitoaikataulut**)</span><span class="sxs-lookup"><span data-stu-id="6957f-119">All maintenance schedule (**Asset management \> Management schedule \> All maintenance schedule**)</span></span>
    - <span data-ttu-id="6957f-120">Avoimet ylläpitoaikataulurivit (**Resurssien hallinta \> Hallinta-aikataulu \> Avoimet ylläpitoaikataulurivit**)</span><span class="sxs-lookup"><span data-stu-id="6957f-120">Open maintenance schedule lines (**Asset management \> Management schedule \> Open maintenance schedule lines**)</span></span>
    - <span data-ttu-id="6957f-121">Avoimet ylläpitoaikataulupoolit (**Resurssien hallinta \> Hallinta-aikataulu \> Avoimet ylläpitoaikataulupoolit**)</span><span class="sxs-lookup"><span data-stu-id="6957f-121">Open maintenance schedule pools (**Asset management \> Management schedule \> Open maintenance schedule pools**)</span></span>

1. <span data-ttu-id="6957f-122">Valitse ruudukossa niiden aikataulutettujen ylläpitotöiden valintaruutu, joille haluat luoda työtilauksen.</span><span class="sxs-lookup"><span data-stu-id="6957f-122">In the grid, select the check box for every scheduled maintenance job that you want to create a work order for.</span></span> <span data-ttu-id="6957f-123">Valitse sitten toimintoruudussa **Työtilaus**.</span><span class="sxs-lookup"><span data-stu-id="6957f-123">Then, on the Action Pane, select **Work order**.</span></span>

    <span data-ttu-id="6957f-124">**Luo työtilaukset** -valintaikkuna avautuu.</span><span class="sxs-lookup"><span data-stu-id="6957f-124">The **Create work orders** dialog box appears.</span></span> <span data-ttu-id="6957f-125">Valittujen rivien ennustetuntien kokonaismäärä näkyy **Ylläpitoennusteen tunnit** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="6957f-125">The **Maintenance forecast hours** field shows the total number of forecast hours for the selected lines.</span></span>

    ![Luo työtilaukset -valintaikkuna](media/18-preventive-maintenance.png)

1. <span data-ttu-id="6957f-127">Määritä **Parametrit**-osassa luotavien työtilausten määrä.</span><span class="sxs-lookup"><span data-stu-id="6957f-127">In the **Parameters** section, specify the number of work orders that should be created.</span></span> <span data-ttu-id="6957f-128">Valitse jompikumpi seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="6957f-128">Select one of the following options:</span></span>

    - <span data-ttu-id="6957f-129">**Yksi rivikohtainen työtilaus** – yksi työtilaus luodaan kullekin ylläpitoaikatauluriville.</span><span class="sxs-lookup"><span data-stu-id="6957f-129">**One work order per line** – Create one work order per maintenance schedule line.</span></span>
    - <span data-ttu-id="6957f-130">**Yksi työtilaus perustuu** – Luotavat työtilaukset ryhmitellään muiden asetusten vaihtoehtojen mukaan. Nämä vaihtoehdot ovat käytettävissä, kun tämä vaihtoehto valitaan.</span><span class="sxs-lookup"><span data-stu-id="6957f-130">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="6957f-131">Valitse **Työtilaustyyppi**-kentässä työtilaustyyppi, jotka käytetään kaikissa luotavissa työtilauksissa.</span><span class="sxs-lookup"><span data-stu-id="6957f-131">In the **Work order type** field, select the work order type to use for all the work orders that you create.</span></span>
1. <span data-ttu-id="6957f-132">Luo asetusten mukaisia työtilauksia valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="6957f-132">Select **OK** to create the work orders according to your settings.</span></span>

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a><span data-ttu-id="6957f-133">Ylläpitosuunnitelman suorittamisen aikana automaattisesti luotavien työtilausrivien ryhmitteleminen</span><span class="sxs-lookup"><span data-stu-id="6957f-133">Group work order lines that are automatically created while a maintenance plan runs</span></span>

[!INCLUDE [preview-banner-section](../../../includes/preview-banner-section.md)]

<span data-ttu-id="6957f-134">Tällä toiminnolla voidaan määrittää ylläpitosuunnitelman perusteella säännöt, joilla työtilausrivit ryhmitellään yhteen työtilaukseen, kun järjestelmä on määritetty luomaan työtilauksia automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="6957f-134">This feature lets you define rules for grouping work order lines under a single work order when the system is set up to generate work orders automatically, based on a maintenance plan.</span></span> <span data-ttu-id="6957f-135">Aiemmin automaattisesti luoduissa työtilauksissa saattoi olla vain yksi rivi.</span><span class="sxs-lookup"><span data-stu-id="6957f-135">Previously, automatically generated work orders could contain only one line.</span></span> <span data-ttu-id="6957f-136">Työtilaukset voidaan kuitenkin nyt ryhmitellä esimerkiksi resurssin, resurssin tyypin tai toiminnallisen sijainnin perusteella.</span><span class="sxs-lookup"><span data-stu-id="6957f-136">However, you can now group work orders by, for example, asset, asset type, or functional location.</span></span> <span data-ttu-id="6957f-137">(Tällainen ryhmittely oli jo mahdollisesti manuaalisesti luoduissa työtilauksissa tämän aiheen edellisessä osassa kuvatulla tavalla.)</span><span class="sxs-lookup"><span data-stu-id="6957f-137">(Manually generated work orders could already be grouped in this way, as described in the previous section of this topic.)</span></span>

### <a name="enable-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="6957f-138">Automaattisesti luotujen työtilausten ryhmittelyn ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="6957f-138">Enable grouping for automatically generated work orders</span></span>

<span data-ttu-id="6957f-139">Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi.</span><span class="sxs-lookup"><span data-stu-id="6957f-139">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="6957f-140">Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="6957f-140">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="6957f-141">**Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="6957f-141">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="6957f-142">**Moduuli:** *Resurssien hallinta*</span><span class="sxs-lookup"><span data-stu-id="6957f-142">**Module:** *Asset Management*</span></span>
- <span data-ttu-id="6957f-143">**Toiminnon nimi:** *(Esiversio) Työtilausten ryhmittelysääntöjen käyttäminen ylläpitosuunnitelmaa suoritettaessa*</span><span class="sxs-lookup"><span data-stu-id="6957f-143">**Feature name:** *(Preview) Apply rules for grouping work orders while running a maintenance plan*</span></span>

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="6957f-144">Automaattisesti luotujen työtilausten ryhmittelyn määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6957f-144">Set up grouping for automatically generated work orders</span></span>

<span data-ttu-id="6957f-145">Automaattisesti luotujen työtilausten ryhmittely määritetään seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6957f-145">To set up grouping for automatically generated work orders, follow these steps.</span></span>

1. <span data-ttu-id="6957f-146">Valitse **Resurssien hallinta \> Asetukset \> Ennalta ehkäisevä ylläpito \>Ylläpitosuunnitelmat**.</span><span class="sxs-lookup"><span data-stu-id="6957f-146">Go to **Asset management \> Setup \> Preventative maintenance \> Maintenance plans**.</span></span>
1. <span data-ttu-id="6957f-147">Toimi seuraavasti jokaisessa suunnitelmassa, jossa halutaan luoda ryhmiteltyjä työtilauksia:</span><span class="sxs-lookup"><span data-stu-id="6957f-147">For each plan where you want to generate grouped work orders, follow these steps:</span></span>

    1. <span data-ttu-id="6957f-148">Valitse suunnitelma luetteloruudussa.</span><span class="sxs-lookup"><span data-stu-id="6957f-148">Select the plan in the list pane.</span></span>
    1. <span data-ttu-id="6957f-149">Varmista **Rivit**-pikavälilehdessä, että jokaisen rivin **Luo automaattisesti** -valintaruutu on valittu.</span><span class="sxs-lookup"><span data-stu-id="6957f-149">On the **Lines** FastTab, make sure that the **Auto create** check box is selected on every line.</span></span>

1. <span data-ttu-id="6957f-150">Valitse **Resurssien hallinta \> Kausittainen \> Ennalta ehkäisevä ylläpito \> Aikatauluta ylläpitosuunnitelmat**.</span><span class="sxs-lookup"><span data-stu-id="6957f-150">Go to **Asset management \> Periodic \> Preventive maintenance \> Schedule maintenance plans**.</span></span>
1. <span data-ttu-id="6957f-151">Määritä **Aikatauluta ylläpitosuunnitelmat** -valintaikkunan **Kausi**-osassa suunnitelman aikajakso (kuinka pitkältä tulevaisuudesta etsitään aikataulutettuja ylläpitotöitä, joille työ luodaan).</span><span class="sxs-lookup"><span data-stu-id="6957f-151">In the **Schedule maintenance plans** dialog box, in the **Period** section, specify the time horizon for the plan (how far to look ahead when finding scheduled maintenance jobs to generate work for).</span></span>
1. <span data-ttu-id="6957f-152">Määritä **Luo työtilaus automaattisesti aikataulusta** -asetukseksi *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="6957f-152">Set the **Automatically create work order from schedule** option to *Yes*.</span></span>
1. <span data-ttu-id="6957f-153">Valitse **Työtilaus**-osasta jokin seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="6957f-153">In the **Work order** section, select one of the following options:</span></span>

    - <span data-ttu-id="6957f-154">**Yksi rivikohtainen työtilaus** – yksi työtilaus luodaan kullekin ylläpitoaikatauluriville.</span><span class="sxs-lookup"><span data-stu-id="6957f-154">**One work order per line** – Create one work order per maintenance schedule line.</span></span> <span data-ttu-id="6957f-155">(Tämä vaihtoehto sisältää saman toiminnon, joka oli käytettävissä, kun *Työtilausten ryhmittelysääntöjen käyttäminen ylläpitosuunnitelmaa suoritettaessa* -toiminto oli poistettu käytöstä.)</span><span class="sxs-lookup"><span data-stu-id="6957f-155">(This option provides the same functionality that is available when the *Apply rules for grouping work orders while running a maintenance plan* feature is turned off.)</span></span>
    - <span data-ttu-id="6957f-156">**Yksi työtilaus perustuu** – Luotavat työtilaukset ryhmitellään muiden asetusten vaihtoehtojen mukaan. Nämä vaihtoehdot ovat käytettävissä, kun tämä vaihtoehto valitaan.</span><span class="sxs-lookup"><span data-stu-id="6957f-156">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="6957f-157">Jos vaihtoehtoja halutaan käyttää, kun vain osa ylläpitosuunnitelmista suoritetaan, lisää **Sisällytettävät tietueet** -pikavälilehdessä sopivat suodattimet aivan kuten muissakin Microsoft Dynamics 365 Supply Chain Managementin erätöissä.</span><span class="sxs-lookup"><span data-stu-id="6957f-157">If you want the options to apply when you run only some of your maintenance plans, on the **Records to include** FastTab, add filters as you require, just as you might do for other batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="6957f-158">Määritä **Suorita taustalla** -pikavälilehdessä tarvittavat erä- ja aikataulutusvaihtoehdot aivan kuten muissakin Supply Chain Managementin erätöissä.</span><span class="sxs-lookup"><span data-stu-id="6957f-158">On the **Run in the background** FastTab, set up batch and scheduling options as you require, just as you might do for other batch jobs in Supply Chain Management.</span></span>
1. <span data-ttu-id="6957f-159">Suorita ja/tai aikatauluta valitut ylläpitosuunnitelmat valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="6957f-159">Select **OK** to run and/or schedule the selected maintenance plans.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]