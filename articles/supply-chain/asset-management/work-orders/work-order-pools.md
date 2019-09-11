---
title: Työtilauspoolit
description: Tässä ohjeaiheessa kerrotaan työtilauspoolien käsittelystä resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 069fa02073808fd7bbaac9bc1603e49ce4d450eb
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875631"
---
# <a name="work-order-pools"></a><span data-ttu-id="cd879-103">Työtilauspoolit</span><span class="sxs-lookup"><span data-stu-id="cd879-103">Work order pools</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="cd879-104">Voit käyttää työtilauspooleja sellaisten työtilausten ryhmittelyyn, joilla on jotain yhteistä.</span><span class="sxs-lookup"><span data-stu-id="cd879-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="cd879-105">Voit esimerkiksi luoda työtilauspooleja seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="cd879-105">For example, you can create work order pools for</span></span>

- <span data-ttu-id="cd879-106">työnjoukkueille, esimerkiksi huoltomiehistö A, huoltomiehistö B</span><span class="sxs-lookup"><span data-stu-id="cd879-106">work crews, for example, Maintenance Crew A, Maintenance Crew B</span></span>  

- <span data-ttu-id="cd879-107">osaamisille, esimerkiksi sähköasentajat tai putkimiehet</span><span class="sxs-lookup"><span data-stu-id="cd879-107">professional skills, for example, electricians or plumbers</span></span>  

- <span data-ttu-id="cd879-108">fyysinen sijainti</span><span class="sxs-lookup"><span data-stu-id="cd879-108">physical locations</span></span>  

- <span data-ttu-id="cd879-109">aikatauluille, esimerkiksi viikot tai muut kaudet</span><span class="sxs-lookup"><span data-stu-id="cd879-109">time schedules, for example, weeks or other periods</span></span>  


<span data-ttu-id="cd879-110">Jos tarpeen, yksi työtilaus voidaan sijoittaa moniin työtilauspooleihin.</span><span class="sxs-lookup"><span data-stu-id="cd879-110">If required, one work order can be placed in many work order pools.</span></span>


## <a name="create-work-order-pool"></a><span data-ttu-id="cd879-111">Luo työtilauspooli</span><span class="sxs-lookup"><span data-stu-id="cd879-111">Create work order pool</span></span>

<span data-ttu-id="cd879-112">**Kaikki työtilauspoolit**- tai **Aktiiviset työtilauspoolit**- kodissa saat yleiskuvan työtilauspooleista ja voit luoda uusia pooleja.</span><span class="sxs-lookup"><span data-stu-id="cd879-112">In **All work order pools** or **Active work order pools**, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="cd879-113">Valitse **Resurssien hallinta** >  **yhteiset** >  **Työtilauspoolit** >  **Kaikki työtilauspoolit** tai **Aktiiviset työtilauspoolit**.</span><span class="sxs-lookup"><span data-stu-id="cd879-113">Click **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="cd879-114">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="cd879-114">Click **New**.</span></span>

3. <span data-ttu-id="cd879-115">Lisää työtilauspoolin tunnus **pooli**-kenttään ja nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="cd879-115">Insert a work order pool ID in the **Pool** field and a name in the **Name** field.</span></span>

4. <span data-ttu-id="cd879-116">Valitse "kyllä" **Aktiivinen**-vaihtopainikkeen avulla osoittamaan, että työtilauspooli on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="cd879-116">Select "Yes" on the **Active** toggle button to indicate that the work order pool is active.</span></span>

5. <span data-ttu-id="cd879-117">Valitse **Poista työtilauksen suhteet** -vaihtopainikkeessa "kyllä", jos haluat, että työtilaukset poistetaan automaattisesti työtilauspoolista.</span><span class="sxs-lookup"><span data-stu-id="cd879-117">Select "Yes" on the **Delete work order relations** toggle button if you want work orders to be automatically removed from the work order pool.</span></span>

6. <span data-ttu-id="cd879-118">Valitse **Poista elinkaaren tila** -kentässä työtilauksen elinkaaritila.</span><span class="sxs-lookup"><span data-stu-id="cd879-118">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="cd879-119">Esimerkiksi työtilauksen suorittamisen elinkaaritila voidaan määrittää poistamaan automaattisesti suhteet työtilauspooleihin.</span><span class="sxs-lookup"><span data-stu-id="cd879-119">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

7. <span data-ttu-id="cd879-120">Voit aloittaa työtilausten lisäämisen työtilauspooliin heti.</span><span class="sxs-lookup"><span data-stu-id="cd879-120">You can start adding work orders to your work order pool right away.</span></span> <span data-ttu-id="cd879-121">Valitse **Työtilaukset** -pikavälilehdessä **Lisää rivi**.</span><span class="sxs-lookup"><span data-stu-id="cd879-121">On the **Work orders** FastTab, click **Add line**.</span></span>

8. <span data-ttu-id="cd879-122">Valitse **Työtilaus**-kentässä työtilaus.</span><span class="sxs-lookup"><span data-stu-id="cd879-122">Select a work order in the **Work order** field.</span></span> <span data-ttu-id="cd879-123">Liittyvät kentät päivittyvät automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="cd879-123">The related fields are automatically updated.</span></span>

9. <span data-ttu-id="cd879-124">Toista vaiheet 7-8, jos haluat lisätä uusia työtilauksia.</span><span class="sxs-lookup"><span data-stu-id="cd879-124">Repeat steps 7-8 if you want to add more work orders.</span></span>

10. <span data-ttu-id="cd879-125">**Lajittelujärjestys**-kentässä voit määrittää, suoritetaanko työtilaukset tietyssä järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="cd879-125">In the **Sort order** field, you can indicate if the work orders should be carried out in a certain order.</span></span> <span data-ttu-id="cd879-126">Voit määrittää valittujen työtilausten tietyn järjestyksen lisäämällä luvut 1, 2, 3 ja niin edelleen.</span><span class="sxs-lookup"><span data-stu-id="cd879-126">Insert numbers 1, 2, 3, and so on to indicate a specific sequence for the selected work orders.</span></span>

11. <span data-ttu-id="cd879-127">Napsauttamalla **Työtilaukset**-painiketta saat näkyviin luettelon kaikista työtilauspooliin sisältyvistä työtilauksista.</span><span class="sxs-lookup"><span data-stu-id="cd879-127">Click the **Work orders** button to see a list of all the work orders included in the work order pool.</span></span>

12. <span data-ttu-id="cd879-128">Valitsemalla **kapasiteetin kuormitus** -painikkeen voit avata **Kapasiteetin kuormitus** -kohdan, joka laskee ja näyttää ylläpitoaikataulun, ei-ajoitettujen työtilausten ja ajoitettujen työtilausten kapasiteetin kuormituksen.</span><span class="sxs-lookup"><span data-stu-id="cd879-128">Click the **Capacity load** button to open **Capacity load** to calculate and view capacity load for maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

13. <span data-ttu-id="cd879-129">Valitse **Nimike-ennuste**-painike, kun avata **Nimike-ennusteen** laskeaksesi ja tarkastellaksesi nimikkeiden (varaosien ja muiden tarvittavien nimikkeiden) ennusteita, jotka liittyvät kunnossapitoaikatauluun, ei-ajoitettuihin työtilauksiin ja ajoitettuihin työtilauksiin.</span><span class="sxs-lookup"><span data-stu-id="cd879-129">Click the **Item forecast** button to open **Item forecast** to calculate and view forecasts for items (spare parts and other required items) related to maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

14. <span data-ttu-id="cd879-130">Avaa **Työtilauksen ostoehdotus** -luettelo napsauttamalla **Työtilauksen ostoehdotus** -painiketta, niin saat näkyviin luettelon työtilauspoolin työtilauksiin liittyvistä ostoehdotuksista.</span><span class="sxs-lookup"><span data-stu-id="cd879-130">Click the **Work order purchase requisition** button to open the **Work order purchase requisition** list to see a list of purchase requisitions related to the work orders in the work order pool.</span></span>

15. <span data-ttu-id="cd879-131">Avaa **Työtilauksen osto** -luettelo napsauttamalla **Työtilauksen osto** -painiketta, niin saat näkyviin luettelon työtilauspoolin työtilauksiin liittyvistä ostotilauksista.</span><span class="sxs-lookup"><span data-stu-id="cd879-131">Click the **Work order purchase** button to open the **Work order purchase** list to see a list of purchase orders related to the work orders in the work order pool.</span></span>

>[!NOTE]
><span data-ttu-id="cd879-132">Kun työtilauspooli ei ole enää tarpeen työsuunnitelmasi osalta, määritä kyseisen varannon **Aktiivinen**-valintaruutuun Ei **Työtilauspooli**-luettelonäkymässä.</span><span class="sxs-lookup"><span data-stu-id="cd879-132">When a work order pool is no longer relevant for your work planning, set the **Active** check box for that pool to "No" in the **Work order pool** list view.</span></span>

<span data-ttu-id="cd879-133">Valitse **Poista työtilaussuhteet** -valintaruutu, jos haluat poistaa kaikki työtilausrivit, esimerkiksi luodaksesi tyhjän varannon, jota voit myöhemmin käyttää muissa työtilauksissa.</span><span class="sxs-lookup"><span data-stu-id="cd879-133">Select the **Delete work order relations** check box if you want to delete all work order lines, for example to create an empty pool that you can later use for other work orders.</span></span> <span data-ttu-id="cd879-134">Muista tyhjentää **Poista työtilauksen suhteet** -valintaruutu, jos haluat käyttää työtilauspoolia uusien työtilaussuhteiden luomiseen myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="cd879-134">Remember to clear the **Delete work order relations** check box if you want to use the work order pool to create new work order relations later.</span></span>


![Kuva 1](media/22-work-orders.png)


## <a name="add-work-order-to-a-work-order-pool"></a><span data-ttu-id="cd879-136">Työtilauksen lisääminen työtilauspooliin</span><span class="sxs-lookup"><span data-stu-id="cd879-136">Add work order to a work order pool</span></span>

<span data-ttu-id="cd879-137">Kuten yllä olevassa osassa on kuvattu, voit lisätä työtilauksia työtilauspooliin, kun luot poolin.</span><span class="sxs-lookup"><span data-stu-id="cd879-137">As described in the section above, you can add work orders to a work order pool when you create the pool.</span></span> <span data-ttu-id="cd879-138">Voit myös lisätä työtilauksen työtilauspooliin jostakin **Kaikki työtilaukset** -luettelosta.</span><span class="sxs-lookup"><span data-stu-id="cd879-138">You can also add a work order to a work order pool from one of the **All work orders** list.</span></span>

1. <span data-ttu-id="cd879-139">Valitse **Resurssien hallinta** >  **yhteiset** >  **työtilaukset** >  **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="cd879-139">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="cd879-140">Valitse työtilaus luettelosta ja valitse sitten **Työtilauspooli.**</span><span class="sxs-lookup"><span data-stu-id="cd879-140">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="cd879-141">Valitse **Lisää/poista** -kentässä Lisää.</span><span class="sxs-lookup"><span data-stu-id="cd879-141">Select "Add" in the **Add/remove** field.</span></span>

4. <span data-ttu-id="cd879-142">Valitse työtilauspooli **Pooli**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="cd879-142">Select the work order pool in the **Pool** field.</span></span>

5. <span data-ttu-id="cd879-143">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="cd879-143">Click **OK**.</span></span>

6. <span data-ttu-id="cd879-144">Kun olet lisännyt työtilauksen työtilauspooliin ja haluat sijoittaa työtilauksen poolin tiettyyn kohtaan: Avaa jokin työtilauspooli luettelosivulta, valitse pooli ja valitse **Muokkaa**ja säädä poolin työtilausten lajittelujärjestystä kohdassa **Työtilauspooli** -lomake > > **Työtilaukset**- pikavälilehti > **Lajittelujärjestys**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="cd879-144">After you have added a work order to a work order pool, if you want to place the work order in a specific sequence in the pool: Open one of the work order pools list pages, select the pool and click **Edit**, and adjust the sort order of the work orders included in pool in the **Work order pool** form > **Work orders** FastTab > **Sort order** field.</span></span>

<span data-ttu-id="cd879-145">Jos haluat poistaa valitun työtilauksen työtilauspoolista, valitse Poista vaiheessa 3.</span><span class="sxs-lookup"><span data-stu-id="cd879-145">If you want to remove the selected work order from a work order pool, select "Remove" in step 3.</span></span>

