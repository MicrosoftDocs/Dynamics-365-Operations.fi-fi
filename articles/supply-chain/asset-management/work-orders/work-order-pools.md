---
title: Työtilauspoolit
description: Tässä ohjeaiheessa kerrotaan työtilauspoolien käsittelystä resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: debff2d6ec9c9e3ba711f62ffefab0546dbd2346
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208866"
---
# <a name="work-order-pools"></a><span data-ttu-id="d0106-103">Työtilauspoolit</span><span class="sxs-lookup"><span data-stu-id="d0106-103">Work order pools</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="d0106-104">Voit käyttää työtilauspooleja sellaisten työtilausten ryhmittelyyn, joilla on jotain yhteistä.</span><span class="sxs-lookup"><span data-stu-id="d0106-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="d0106-105">Tässä on esimerkkejä asioista, joita varten voit luoda työtilauspooleja:</span><span class="sxs-lookup"><span data-stu-id="d0106-105">Here are some examples of things that you can create  work order pools for:</span></span>

- <span data-ttu-id="d0106-106">Työvuorot, kuten Ylläpitovuoro A tai Ylläpitovuoro B</span><span class="sxs-lookup"><span data-stu-id="d0106-106">Work crews, for example, Maintenance Crew A or Maintenance Crew B</span></span>  

- <span data-ttu-id="d0106-107">Osaaminen, kuten sähköasentajat tai putkimiehet</span><span class="sxs-lookup"><span data-stu-id="d0106-107">Professional skills, such as electricians or plumbers</span></span>  

- <span data-ttu-id="d0106-108">Fyysiset sijainnit</span><span class="sxs-lookup"><span data-stu-id="d0106-108">Physical locations</span></span>  

- <span data-ttu-id="d0106-109">Aikataulut, kuten viikot tai muut ajanjaksot</span><span class="sxs-lookup"><span data-stu-id="d0106-109">Time schedules, such as weeks or other periods</span></span>  

<span data-ttu-id="d0106-110">Tarvittaessa voit laittaa yhden työtilauksen useaan työtilauspooliin.</span><span class="sxs-lookup"><span data-stu-id="d0106-110">As you require, you can put one work order in multiple work order pools.</span></span>


## <a name="create-a-work-order-pool"></a><span data-ttu-id="d0106-111">Työtilauspoolin luominen</span><span class="sxs-lookup"><span data-stu-id="d0106-111">Create a work order pool</span></span>

<span data-ttu-id="d0106-112">Luettelosivulla **Kaikki työtilauspoolit** tai **Aktiiviset työtilauspoolit** saat yleiskuvan työtilauspooleista ja voit luoda uusia pooleja.</span><span class="sxs-lookup"><span data-stu-id="d0106-112">On the **All work order pools** or **Active work order pools** list page, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="d0106-113">Valitse **Resurssien hallinta** > **yhteiset** > **Työtilauspoolit** > **Kaikki työtilauspoolit** tai **Aktiiviset työtilauspoolit**.</span><span class="sxs-lookup"><span data-stu-id="d0106-113">Select **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="d0106-114">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="d0106-114">Select **New**.</span></span>

3. <span data-ttu-id="d0106-115">Kirjoita **Pooli**-kenttään työtilauspoolin tunnus.</span><span class="sxs-lookup"><span data-stu-id="d0106-115">In the **Pool** field, enter an ID for the work order pool.</span></span>

4. <span data-ttu-id="d0106-116">Anna nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="d0106-116">the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="d0106-117">Aseta **Aktiivinen**-asetuksen arvoksi **Kyllä** ilmaisemaan, että työtilauspooli on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="d0106-117">Set the **Active** option to **Yes** to indicate that the work order pool is active.</span></span>

6. <span data-ttu-id="d0106-118">Aseta **Poista työtilauksen suhteet** -asetuksen arvoksi **Kyllä**, jos työtilaukset on tarkoitus poistaa automaattisesti työtilauspoolista.</span><span class="sxs-lookup"><span data-stu-id="d0106-118">Set the **Delete work order relations** option to **Yes** if work orders should automatically be removed from the work order pool.</span></span>

7. <span data-ttu-id="d0106-119">Valitse **Poista elinkaaren tila** -kentässä työtilauksen elinkaaritila.</span><span class="sxs-lookup"><span data-stu-id="d0106-119">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="d0106-120">Esimerkiksi työtilauksen suorittamisen elinkaaritila voidaan määrittää poistamaan automaattisesti suhteet työtilauspooleihin.</span><span class="sxs-lookup"><span data-stu-id="d0106-120">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

    <span data-ttu-id="d0106-121">Voit aloittaa työtilausten lisäämisen työtilauspooliin heti.</span><span class="sxs-lookup"><span data-stu-id="d0106-121">You can start adding work orders to your work order pool right away.</span></span>

8. <span data-ttu-id="d0106-122">Valitse **Työtilaukset** -pikavälilehdessä **Lisää rivi**.</span><span class="sxs-lookup"><span data-stu-id="d0106-122">On the **Work orders** FastTab, select **Add line**.</span></span>

9. <span data-ttu-id="d0106-123">Valitse **Työtilaus**-kentässä työtilaus.</span><span class="sxs-lookup"><span data-stu-id="d0106-123">In the **Work order** field, select a work order.</span></span> <span data-ttu-id="d0106-124">Liittyvät kentät päivittyvät automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="d0106-124">The related fields are automatically updated.</span></span>

10. <span data-ttu-id="d0106-125">Voit lisätä muita työtilauksia tekemällä kohtien 8–9 toimet uudelleen.</span><span class="sxs-lookup"><span data-stu-id="d0106-125">Repeat steps 8 through 9 to add more work orders.</span></span>

11. <span data-ttu-id="d0106-126">Jos lisäämäsi työtilaukset on tarkoitus suorittaa tietyssä järjestyksessä, voit määrittää järjestyksen syöttämällä **Lajittelujärjestys**-kenttään numerot **1**, **2**, **3** jne.</span><span class="sxs-lookup"><span data-stu-id="d0106-126">If the work orders that you added should be done in a specific order, in the **Sort order** field, you can enter the numbers **1**, **2**, **3**, and so on, to specify that order.</span></span>

12. <span data-ttu-id="d0106-127">Voit tarkastella luetteloa kaikista työtilauspooliin kuuluvista työtilauksista valitsemalla **Työtilaukset** toimintoruudun **Työtilauspooli**-välilehden **Näytä työtilauspooliin liittyvät** -ryhmässä, jolloin **Kaikki työtilaukset** -luettelosivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="d0106-127">To view a list of all the work orders that are included in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Work orders** to open the **All work orders** list page.</span></span>

13. <span data-ttu-id="d0106-128">Voit laskea ylläpitoaikataulun, ajoittamattomien työtilausten ja ajoitettujen työtilausten kapasiteetin kuormituksen ja tarkastella sitä valitsemalla **Kapasiteetin kuormitus** toimintoruudun **Työtilauspooli**-välilehden **Näytä työtilauspooliin liittyvät** -ryhmässä, jolloin avautuu **Laske kapasiteetin kuormitus** -valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="d0106-128">To calculate and view capacity load for the maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Capacity load** to open the **Calculate capacity load** dialog.</span></span>

14. <span data-ttu-id="d0106-129">Voit laskea ylläpitoaikatauluun, ajoittamattomiin työtilauksiin ja ajoitettuihin työtilauksiin liittyvien nimikkeiden (varaosien ja muiden tarvittavien nimikkeiden) ennusteita ja tarkastella niitä valitsemalla **Nimike-ennuste** **Työtilauspooli**-välilehden **Näytä työtilauspooliin liittyvät** -ryhmässä, jolloin avautuu **Laske nimike-ennuste** -valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="d0106-129">To calculate and view forecasts for items (spare parts and other required items) that are related to maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Item forecast** to open the **Calculate item forecast** dialog.</span></span>

15. <span data-ttu-id="d0106-130">Voit tarkastella työtilauspoolin työtilauksiin liittyvien ostoehdotusten luetteloa valitsemalla **Työtilauksen ostoehdotus** toimintoruudun **Työtilauspooli**-välilehden **Hankinta**-ryhmässä, jolloin **Työtilauksen ostoehdotus** -luettelosivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="d0106-130">To view a list of purchase requisitions that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase requisition** to open the **Work order purchase requisition** list page.</span></span>

16. <span data-ttu-id="d0106-131">Voit tarkastella työtilauspoolin työtilauksiin liittyvien ostotilausten luetteloa valitsemalla **Työtilauksen osto** toimintoruudun **Työtilauspooli**-välilehden **Hankinta**-ryhmässä, jolloin **Työtilauksen osto** -luettelosivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="d0106-131">To view a list of purchase orders that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase** to open the **Work order purchase** list page.</span></span>

>[!NOTE]
><span data-ttu-id="d0106-132">Kun työtilauspooli ei ole enää tarpeen työsuunnitelmasi osalta, määritä kyseisen poolin **Aktiivinen**-asetuksen arvoksi **Ei** **Työtilauspooli**-sivun luettelonäkymässä.</span><span class="sxs-lookup"><span data-stu-id="d0106-132">When a work order pool is no longer relevant to your work planning, set the **Active** option for that pool to **No** in the list view of the **Work order pool** page.</span></span>

<span data-ttu-id="d0106-133">Voit poistaa kaikki työtilausrivit asettamalla **Poista työtilaussuhteet**-asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="d0106-133">To delete all worker order lines, set the **Delete work order relations** option to **Yes**.</span></span> <span data-ttu-id="d0106-134">Tämä asetus on hyödyllinen, jos esimerkiksi haluat luoda tyhjän poolin, jota voit käyttää myöhemmin muita työtilauksia varten.</span><span class="sxs-lookup"><span data-stu-id="d0106-134">This option is useful if, for example, you want to create an empty pool that you can use later for other work orders.</span></span> <span data-ttu-id="d0106-135">Kun myöhemmin olet valmis käyttämään työtilauspoolia uusien työtilaussuhteiden luomiseen, muista asettaa **Poista työtilaussuhteet** -asetuksen arvoksi **Ei**.</span><span class="sxs-lookup"><span data-stu-id="d0106-135">When you're ready to use the work order pool to create new work order relations later, remember to set the **Delete work order relations** option to **No**.</span></span>

<span data-ttu-id="d0106-136">Seuraavassa kuvassa on esimerkki **Työtilauspooli** -luettelosivusta.</span><span class="sxs-lookup"><span data-stu-id="d0106-136">The illustration below shows an example of the **Work order pool** list page.</span></span>

![Kuva 1](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a><span data-ttu-id="d0106-138">Työtilauksen lisääminen työtilauspooliin</span><span class="sxs-lookup"><span data-stu-id="d0106-138">Add a work order to a work order pool</span></span>

<span data-ttu-id="d0106-139">Kuten edellisessä osassa on kuvattu, voit lisätä työtilauksia työtilauspooliin, kun luot poolin.</span><span class="sxs-lookup"><span data-stu-id="d0106-139">As described in the previous section, you can add work orders to a work order pool when you create that pool.</span></span> <span data-ttu-id="d0106-140">Voit myös lisätä työtilauksia työtilauspooliin luettelosivulla **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="d0106-140">You can also add work orders to a work order pool on the **All work orders** or **Active work orders** list page.</span></span>

1. <span data-ttu-id="d0106-141">Valitse työtilaus luettelosta ja sitten toimintoruudun **Työtilaus**-välilehden **Ylläpidä**-ryhmässä **Työtilauspooli**.</span><span class="sxs-lookup"><span data-stu-id="d0106-141">Select the work order, and then, on the Action Pane, on the **Work order** tab, in the **Maintain** group, select **Work order pool**.</span></span>

2. <span data-ttu-id="d0106-142">Valitse työtilaus luettelosta ja valitse sitten **Työtilauspooli.**</span><span class="sxs-lookup"><span data-stu-id="d0106-142">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="d0106-143">Valitse **Ylläpidä työtilauspoolia** -valintaikkunan **Lisää/poista**-kentässä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="d0106-143">In the **Maintain work order pool** dialog, in the **Add/remove** field, select **Add**.</span></span>

4. <span data-ttu-id="d0106-144">Valitse työtilauspooli **Pooli**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="d0106-144">In the **Pool** field, select the work order pool.</span></span>

5. <span data-ttu-id="d0106-145">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0106-145">Select **OK**.</span></span>

6. <span data-ttu-id="d0106-146">Jos haluat asettaa lisäämäsi työtilaukset tiettyyn järjestykseen työtilauspoolissa, valitse pooli luettelosivulla **Kaikki työtilauspoolit** tai **Aktiiviset työtilauspoolit** ja valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="d0106-146">To put the work order that you added in a specific order in the work order pool, on the **All work order pools** or **Active work order pools** list page, select the pool, and then select **Edit**.</span></span> <span data-ttu-id="d0106-147">Käytä sitten **Työtilauspooli**-sivun **Työtilaukset**-pikavälilehden **Lajittelujärjestys**-kenttää muuttaaksesi pooliin kuuluvien työtilausten lajittelujärjestystä.</span><span class="sxs-lookup"><span data-stu-id="d0106-147">Then, on the **Work order pool** page, on the **Work orders** FastTab, use the **Sort order** field to adjust the sort order of the work orders that are included in pool.</span></span>

<span data-ttu-id="d0106-148">Voit poistaa työtilauksen työtilauspoolista toistamalla nämä vaiheet, mutta valitsemalla **Poista** vaiheessa 3.</span><span class="sxs-lookup"><span data-stu-id="d0106-148">To remove a work order from a work order pool, repeat these steps, but select **Remove** in step 3.</span></span>

