---
title: Ylläpitokierrokset
description: Tässä ohjeaiheessa kerrotaan ylläpitokierroksista resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRoundTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 63cb2614b2037fac1129c7d2f82a26dac41a3490
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889958"
---
# <a name="maintenance-rounds"></a><span data-ttu-id="87117-103">Ylläpitokierrokset</span><span class="sxs-lookup"><span data-stu-id="87117-103">Maintenance rounds</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="87117-104">**Resurssien hallinnassa** huoltokierroksia voidaan luoda eri resursseille, joihin on suoritettava samanlainen tehtävä säännöllisin väliajoin.</span><span class="sxs-lookup"><span data-stu-id="87117-104">In **Asset Management**, you can create maintenance rounds for various assets, on which you need to carry out a similar task at regular intervals.</span></span> <span data-ttu-id="87117-105">Esimerkiksi voitelutyöt tai turvatarkastustyöt, jotka on suoritettava useilla koneilla samalla aikavälillä.</span><span class="sxs-lookup"><span data-stu-id="87117-105">For example, lubrication jobs or safety inspection jobs that need to be carried out on a number of machines within the same intervals.</span></span> <span data-ttu-id="87117-106">Ensimmäinen vaihe on huoltokierroksen luominen, mukaan lukien käyttökohteet, jotka edellyttävät samaa kunnossapitotyötä.</span><span class="sxs-lookup"><span data-stu-id="87117-106">First step is to create a maintenance round, including assets that require the same form of maintenance job.</span></span> <span data-ttu-id="87117-107">Seuraavaksi ajoitat huoltokierrokset.</span><span class="sxs-lookup"><span data-stu-id="87117-107">Next, you schedule the maintenance rounds.</span></span> <span data-ttu-id="87117-108">Kun kunnossapitokierrosten aikataulu on tehty, kaikki kierrokseen liittyvät työtietueet näkyvät kohdassa **Kaikki huoltoaikataulu** ja **Avoimet ylläpitoaikataulurivit**.</span><span class="sxs-lookup"><span data-stu-id="87117-108">When you have completed the maintenance rounds schedule, you can see all the job records relating to the round in the **All maintenance schedule** and **Open maintenance schedule lines**.</span></span>

>[!NOTE]
><span data-ttu-id="87117-109">Kunnossapitokierroksia voidaan määrittää myös toiminnallisissa sijainneissa, jotka on tarkoitus suorittaa toiminnallisessa sijainnissa asennettuihin käyttöomaisuuksiin kierrospohjaista työtilausta luotaessa.</span><span class="sxs-lookup"><span data-stu-id="87117-109">Maintenance rounds can also be set up on functional locations to be completed on the assets installed on the functional location at the time of creation of the round-based work order.</span></span> <span data-ttu-id="87117-110">Lisätietoja toiminnallisten sijaintien ylläpitohuoltokierrosten asetuksista toiminnallisissa sijainneissa on kohdassa [Luo toiminnalliset sijainnit](../functional-locations/create-functional-locations.md).</span><span class="sxs-lookup"><span data-stu-id="87117-110">Refer to [Create functional locations](../functional-locations/create-functional-locations.md) for more information on the setup of maintenance rounds on functional locations.</span></span>

## <a name="set-up-a-maintenance-round"></a><span data-ttu-id="87117-111">Ylläpitokierroksen määritys</span><span class="sxs-lookup"><span data-stu-id="87117-111">Set up a maintenance round</span></span>

1. <span data-ttu-id="87117-112">Valitse **Resurssien hallinta** > **Asetukset** > **Ennalta ehkäisevä ylläpito** > **Ylläpitokierrokset**.</span><span class="sxs-lookup"><span data-stu-id="87117-112">Click **Asset management** > **Setup** > **Preventive maintenance** > **Maintenance rounds**.</span></span>

2. <span data-ttu-id="87117-113">Luo uusi ylläpitokierros valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="87117-113">Click **New** to create a new maintenance round.</span></span>

3. <span data-ttu-id="87117-114">Lisää tunniste **ylläpitokierros**-kentässä ja ylläpitokierroksen nimi **Nimi**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="87117-114">Insert and ID in the **Maintenance round** field, and a name for the maintenance round in the **Name** field.</span></span>

4. <span data-ttu-id="87117-115">Valitse kierroksen aloituspäivä **Alkamispäivä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="87117-115">Select a start date for the round in the **Start date** field.</span></span>

5. <span data-ttu-id="87117-116">Voit lisätä **Päättyminen päivän sisällä**- ja **Päättyminen tunnin sisällä** -kenttiin suunnitellun päätymishetken päivinä tai tunteina.</span><span class="sxs-lookup"><span data-stu-id="87117-116">In the **Finish within days** and **Finish within hours** fields, you can insert expected end date in days or hours.</span></span> <span data-ttu-id="87117-117">Odotettu päättymispäivämäärä lasketaan suhteessa aloituspäivämäärään, joka lasketaan huoltoaikataulurivien luonnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="87117-117">The expected end date is calculated relative to the start date, which is calculated when maintenance schedule lines are created.</span></span> <span data-ttu-id="87117-118">Voit esimerkiksi lisätä **Päättyminen päivän sisällä** -kenttään arvon 7, joka ilmaisee, että liittyvä tehtävä on suoritettava viikon kuluessa aloituspäivämäärästä.</span><span class="sxs-lookup"><span data-stu-id="87117-118">For example, you can insert "7" in the **Finish within days** field to indicate that the related job should be completed within a week from the start date.</span></span>

6. <span data-ttu-id="87117-119">Valitse "kyllä" **Luo automaattisesti** -vaihtopainikkeesta, jos työtilaukset luodaan automaattisesti ylläpitoaikatauluriveistä, jotka on luotu tästä huoltokierroksesta.</span><span class="sxs-lookup"><span data-stu-id="87117-119">Select "Yes" on the **Auto create** toggle button if work orders should automatically be created from maintenance schedule lines that are created from this maintenance round.</span></span>

7. <span data-ttu-id="87117-120">Valitse **Työtilauksen tyyppi** -kentässä työtilaustyyppi, jota käytetään tästä ylläpitokierroksesta luoduissa työtilauksissa.</span><span class="sxs-lookup"><span data-stu-id="87117-120">In the **Work order type** field, select the work order type to be used on work orders created from this maintenance round.</span></span>

8. <span data-ttu-id="87117-121">Valitse **Palvelun taso** -kentässä työtilauksen palvelutaso, jota käytetään tästä ylläpitokierroksesta luoduissa työtilauksissa.</span><span class="sxs-lookup"><span data-stu-id="87117-121">In the **Service level** field, select the work order service level to be used on work orders created from this maintenance round.</span></span>

9. <span data-ttu-id="87117-122">Lisää resurssi ylläpitokirrokseen valitsemalla **Resurssirivit**-pikavälilehdessä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="87117-122">On the **Asset lines** FastTab, click **Add** to add an asset to the maintenance round.</span></span>

10. <span data-ttu-id="87117-123">**Rivinumero**- kenttään lisätään automaattisesti rivinumero, joka ilmaisee kunnossapitokierroksen käyttöomaisuuksien järjestyksen.</span><span class="sxs-lookup"><span data-stu-id="87117-123">A line number is automatically inserted in the **Line number** field to indicate the sequence of the assets in maintenance round.</span></span>

11. <span data-ttu-id="87117-124">Valitse resurssi **Resurssi**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="87117-124">Select the asset in the **Asset** field.</span></span>

12. <span data-ttu-id="87117-125">Valitse käyttöomaisuuden kunnossapitotöiden tyyppi **Ylläpitotyön tyyppi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="87117-125">Select the maintenance job type for the asset in the **Maintenance job type** field.</span></span>

13. <span data-ttu-id="87117-126">Valitse tarvittaessa **Ylläpitotyön tyypin variantti** ja **Kauppa**, jotka liittyvät kunnossapitotyön tyyppiin.</span><span class="sxs-lookup"><span data-stu-id="87117-126">If required, select **Maintenance job typ variant** and **Trade** related to the maintenance job type.</span></span>

14. <span data-ttu-id="87117-127">Valitse **Kauden tyyppi** -kentässä toistuvuus (päivä, viikko jne.).</span><span class="sxs-lookup"><span data-stu-id="87117-127">Select the recurrence (day, week, etc.) in the **Period type** field.</span></span>

15. <span data-ttu-id="87117-128">Lisää **Jakson frekvenssi** -kenttään ylläpitokierroksen toistumismäärä.</span><span class="sxs-lookup"><span data-stu-id="87117-128">In the **Period frequency** field, insert the number of recurrences for the maintenance round.</span></span> <span data-ttu-id="87117-129">Esimerkki: Jos **Kauden tyyppi** -kentässä on valittu "päivä" ja lisäät tähän kenttään numeron "7", uudet kunnossapitokierroksen rivit luodaan ennaltaehkäisevän huollon ajoituksessa kerran viikossa.</span><span class="sxs-lookup"><span data-stu-id="87117-129">Example: If you have selected "Day" in the **Period type** field, and you insert the number "7" in this field, new maintenance round lines are created during preventive maintenance scheduling once a week.</span></span>

16. <span data-ttu-id="87117-130">Valitse kunnossapitokierrokseen sisällytettävän käyttöomaisuuden alkamispäivämäärä **Alkamispäivämäärä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="87117-130">Select a start date for the asset to be included in the maintenance round in the **Start date** field.</span></span> <span data-ttu-id="87117-131">Tämä päivämäärä voi olla eri kuin ylläpitokierrokselle määritetty aloituspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="87117-131">This date may differ from the start date set on the maintenance round.</span></span>

17. <span data-ttu-id="87117-132">Lisää ylläpitokierrokseen lisää resursseja toistamalla vaiheita 9-16.</span><span class="sxs-lookup"><span data-stu-id="87117-132">Repeat steps 9-16 to add more assets to the maintenance round.</span></span>

18. <span data-ttu-id="87117-133">Lisää toiminnallinen sijainti ylläpitokirrokseen valitsemalla **Toiminnallisen sijainnin rivit**-pikavälilehdessä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="87117-133">On the **Functional location lines** FastTab, click **Add** to add a functional location to the maintenance round.</span></span> <span data-ttu-id="87117-134">Lisätietoja on yllä olevien liittyvien kenttien kuvauksessa.</span><span class="sxs-lookup"><span data-stu-id="87117-134">Refer to the description of the related fields above.</span></span> <span data-ttu-id="87117-135">Samat kentät ovat käytettävissä käyttöomaisuusrivin luomisessa, mutta voit tarvittaessa myös valita **valmistajan**- ja **mallin** toiminnalliselle sijainnille.</span><span class="sxs-lookup"><span data-stu-id="87117-135">The same fields are available as for creating an asset line, but you can also select **Manufacturer** and **Model** for a functional location, if required.</span></span> <span data-ttu-id="87117-136">Jos valitset vain rivin toiminnallisen sijainnin, mutta et tee valintoja **Resurssityyppi**, **Valmistaja**, **Malli**, **Ylläpitotyön tyyppi**, **Ylläpitotyön tyypin variantti** ja **Kauppa** -kohdissa, kaikki kyseiseen toiminnalliseen sijaintiin liittyvät käyttökohteet huoltoaikataulutuksen yhteydessä sisällytetään huoltokierrokseen.</span><span class="sxs-lookup"><span data-stu-id="87117-136">If you only select a functional location on a line, but make no selections in **Asset type**, **Manufacturer**, **Model**, **Maintenance job type**, **Maintenance job type variant** and **Trade**, all assets related to that functional location at the time of maintenance scheduling will be included in the maintenance round.</span></span>

19. <span data-ttu-id="87117-137">Valitse huoltokierrokseen sisällytettävä työtilauspooli valitsemalla**Poolit**-pikavälilehdessä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="87117-137">On the **Pools** FastTab, click **Add** to select a work order pool to be included in the maintenance round.</span></span> <span data-ttu-id="87117-138">Useita työtilauspooleja voidaan liittää yhteen huoltokierrokseen.</span><span class="sxs-lookup"><span data-stu-id="87117-138">Several work order pools can be connected to one maintenance round.</span></span>

20. <span data-ttu-id="87117-139">Tallenna asetukset.</span><span class="sxs-lookup"><span data-stu-id="87117-139">Save your setup.</span></span>

>[!NOTE]
><span data-ttu-id="87117-140">**Resurssit**- ja **Rivit**-kentissä (**Otsikko**-pikavälilehden **Tiedot**-ryhmässä) näkyy valittuun huoltokierrokseen liittyvien käyttöomaisuuksien ja rivien kokonaismäärä.</span><span class="sxs-lookup"><span data-stu-id="87117-140">The **Assets** and **Lines** fields located in the **Details** group on the **Header** FastTab show the total number of assets and lines related to the selected maintenance round.</span></span>

<span data-ttu-id="87117-141">Alla oleva kuva osoittaa esimerkin huoltokierroksesta, joka sisältää kolme käyttöomaisuuserää.</span><span class="sxs-lookup"><span data-stu-id="87117-141">The illustration below shows and example of a maintenance round containing three assets.</span></span>

![Kuva 1](media/13-preventive-maintenance.png)


## <a name="schedule-maintenance-rounds"></a><span data-ttu-id="87117-143">Ajoita ylläpitokierroksia</span><span class="sxs-lookup"><span data-stu-id="87117-143">Schedule maintenance rounds</span></span>

<span data-ttu-id="87117-144">Kun olet määrittänyt kunnossapitokierroksen, voit ajoittaa kaikki huoltokierrokseen liittyvät työt suorittamalla ajoitustyön.</span><span class="sxs-lookup"><span data-stu-id="87117-144">When you've set up a maintenance round, you run a schedule job to schedule all the jobs related to the maintenance round.</span></span>

1. <span data-ttu-id="87117-145">Valitse **Resurssien hallinta** > **Kausittainen** > **Ennalta ehkäisevä ylläpito** > **Ajoita ylläpitokierrokset** tai **Resurssien hallinta** > **Yhteiset** > **Ylläpitoaikataulu** > **Kaikki ylläpitoaikataulut** tai **Avoimet ylläpitoaikataulurivit** tai **Avoimet ylläpitoaikataulupoolit** > valitse ylläpitoaikataulurivi luettelosta > **Ylläpitokierrokset** -painike.</span><span class="sxs-lookup"><span data-stu-id="87117-145">Click **Asset management** > **Periodic** > **Preventive maintenance** > **Schedule maintenance rounds**, or **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** > select maintenance schedule line in the list > **Maintenance rounds** button.</span></span>

2. <span data-ttu-id="87117-146">Valitse **Kausi**-kentässä kausityyppi, jota käytetään aikataulutuksessa.</span><span class="sxs-lookup"><span data-stu-id="87117-146">In the **Period** field, select the period type to be used for the scheduling job.</span></span>

3. <span data-ttu-id="87117-147">Lisää **Jakson frekvenssi** -kenttään niiden kausien määrä, jotka sisällytetään ajoitustyöhön.</span><span class="sxs-lookup"><span data-stu-id="87117-147">In the **Period frequency** field, insert the number of periods to be included in the scheduling job.</span></span> <span data-ttu-id="87117-148">Aikataulun alku on kuluva päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="87117-148">The start of the scheduling is the current date.</span></span>

4. <span data-ttu-id="87117-149">Valitse "kyllä" **Luo automaattisesti**- vaihtopainikkeesta, jos työtilaus luodaan automaattisesti huoltokierroksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="87117-149">Select "Yes" on the **Auto create** toggle button if a work order should automatically be created on the basis of a maintenance round.</span></span>

>[!NOTE]
><span data-ttu-id="87117-150">Jos tämän vaihtopainikkeen arvoksi on määritetty "kyllä" ja **Luo automaattisesti** -vaihtopainikkeessa on Kyllä valittuna **Ylläpitokierrokset** -lomakkeessa, työtilaukset luodaan huoltokierrosrivien perusteella ja myös ylläpitosuunnitelmarivit, joiden tila on "Työtilaus luotu", luodaan.</span><span class="sxs-lookup"><span data-stu-id="87117-150">If this toggle button is set to "Yes", and the **Auto create** toggle button is also set to "Yes" on the maintenance round in **Maintenance rounds** form, work orders are created based on the maintenance round lines, and maintenance schedule lines with status "Work order created" are also created.</span></span> <span data-ttu-id="87117-151">Jos vain yksi **Luo automaattisesti** -vaihtopainikkeista on määritetty Kyllä-arvoon, tässä avattavassa valikossa tai **Ylläpitokierrokset** -kohdassa luodaan vain huoltoaikataulurivit tilassa Luotu.</span><span class="sxs-lookup"><span data-stu-id="87117-151">If only one of the **Auto create** toggle buttons is set to "Yes", in this drop-down or in **Maintenance rounds**, only maintenance schedule lines are created with status "Created".</span></span> <span data-ttu-id="87117-152">Tässä tapauksessa työtilauksia ei luoda.</span><span class="sxs-lookup"><span data-stu-id="87117-152">In that case, no work orders are created.</span></span>

5. <span data-ttu-id="87117-153">Voit tarvittaessa valita aikataulun työlle tietyt kierrokset tai toisen alkamispäivämäärän.</span><span class="sxs-lookup"><span data-stu-id="87117-153">If required, you can select specific rounds or another start date for the schedule job.</span></span> <span data-ttu-id="87117-154">Valitse **Suodata**ja lisää sisällytettävät kierrokset.</span><span class="sxs-lookup"><span data-stu-id="87117-154">Click **Filter**, and add the rounds to be included.</span></span>

6. <span data-ttu-id="87117-155">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="87117-155">Click **OK**.</span></span>

7. <span data-ttu-id="87117-156">Näet nyt ylläpitokierroksen työt kohdassa **Resurssien hallinta** > **Yhteiset** > **Ylläpitoaikataulu** > **Kaikki ylläpitoaikataulut** tai **Avoimet ylläpitoaikataulurivit**.</span><span class="sxs-lookup"><span data-stu-id="87117-156">You are now able to see the maintenance rounds jobs in **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines**.</span></span> <span data-ttu-id="87117-157">Jos ajoitetut kierrokset on liitetty työtilauspooliin, huoltoaikataulurivit näkyvät myös kohdassa **Avoimet ylläpitoaikataulupoolit**.</span><span class="sxs-lookup"><span data-stu-id="87117-157">If the scheduled rounds are connected to a work order pool, you also see maintenance schedule lines in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="87117-158">Kierroksesta luoduilla ylläpitoaikatauluriveillä on viitetyyppi "Ylläpitokierrokset".</span><span class="sxs-lookup"><span data-stu-id="87117-158">Maintenance schedule lines created from a round have the reference type "Maintenance rounds".</span></span>

<span data-ttu-id="87117-159">Alla olevat kaksi kuvitusta näyttävät työn aikataulutuksen **Ajoita ylläpitokierroksia** -valintaikkunassa ja huoltoaikataulu rivit, jotka on luotu **Kaikki ylläpitoaikataulut** -kohdassa kyseisen ajoitustyön perusteella.</span><span class="sxs-lookup"><span data-stu-id="87117-159">The two illustrations below show a schedule job in the **Schedule maintenance rounds** dialog, and the maintenance schedule lines created in **All maintenance schedule** based on that schedule job.</span></span>

![Kuva 2](media/14-preventive-maintenance.png)

![Kuva 3](media/15-preventive-maintenance.png)

- <span data-ttu-id="87117-162">Kun työtilaukset luodaan manuaalisesti toimittajan takuun kattamille resursseille, näyttöön tulee valintaikkuna, jonka avulla käyttäjä saa tietää takuun.</span><span class="sxs-lookup"><span data-stu-id="87117-162">When work orders are manually created on assets that are covered by a vendor warranty, a dialog box is shown to make the user aware of the warranty.</span></span> <span data-ttu-id="87117-163">Työtilauksen luonti voidaan sitten peruuttaa.</span><span class="sxs-lookup"><span data-stu-id="87117-163">The creation of the work order can then be canceled.</span></span> <span data-ttu-id="87117-164">Takuusuhdetta koskeva tarkistus jätetään pois automaattisesti luoduissa työtilauksissa.</span><span class="sxs-lookup"><span data-stu-id="87117-164">The check for a warranty relation is omitted for work orders that are automatically created.</span></span>  
- <span data-ttu-id="87117-165">Voit määrittää eräajon **Suorita taustalla** -pikavälilehdessä, jolloin kierrokset ajoitetaan säännöllisin väliajoin.</span><span class="sxs-lookup"><span data-stu-id="87117-165">You can set up a batch job on the **Run in the background** FastTab to schedule rounds at regular intervals.</span></span>  
- <span data-ttu-id="87117-166">Jos kierros sisältyy useisiin työtilauspooleihin (lisätietoja on kohdassa [Työtilauspoolit](../work-orders/work-order-pools.md)), kullekin poolille näytetään yksi tietue kohdassa **Avaa ylläpitoaikataulupoolit**.</span><span class="sxs-lookup"><span data-stu-id="87117-166">If a round is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="87117-167">Tämä tehdään työtilauspoolien suodatusasetusten optimoimiseksi.</span><span class="sxs-lookup"><span data-stu-id="87117-167">This is done to optimize the filtering options for work order pools.</span></span>

