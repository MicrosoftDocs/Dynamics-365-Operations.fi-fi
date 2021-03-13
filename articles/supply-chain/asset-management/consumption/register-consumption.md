---
title: Kulutuksen rekisteröinti
description: Tässä ohjeaiheessa kerrotaan, kuinka kulutus rekisteröidään resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderJournal, EntAssetWorkOrderAddSparePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ea1522f8a8e4867d8d70fea59b493d139a1b01ef
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020777"
---
# <a name="register-consumption"></a><span data-ttu-id="c81d9-103">Kulutuksen rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="c81d9-103">Register consumption</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c81d9-104">Kun kunnossapitotyö on suoritettu työtilaukselle, seuraavaksi tehdään kulutusrekisteröinnit ja kirjataan kirjauskansiot.</span><span class="sxs-lookup"><span data-stu-id="c81d9-104">When a maintenance job has been completed on a work order, the next step is to make consumption registrations and post the journals.</span></span> <span data-ttu-id="c81d9-105">Voit tehdä rekisteröintejä seuraaville kulutustyypeille: tunnit, nimikkeet ja kulut.</span><span class="sxs-lookup"><span data-stu-id="c81d9-105">You can make registrations on the following consumption types: Hours, items, and expenses.</span></span> <span data-ttu-id="c81d9-106">Eri kulutustyypit rekisteröidään ja kirjataan **Työtilauksen kirjauskansiot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="c81d9-106">The different consumption types are registered and posted on the **Work order journals** page.</span></span> <span data-ttu-id="c81d9-107">**Resurssien hallinnan** kirjauskansion asetuksia käytetään luotaessa ja kirjattaessa erillisiä tunteja, nimikkeitä ja kuluja koskevia kirjauskansioita **Projektinhallinta ja kirjanpito** -moduulissa.</span><span class="sxs-lookup"><span data-stu-id="c81d9-107">The journal setup in **Asset Management** is used for creating and posting separate journals for hours, items, and expenses in the **Project management and accounting** module.</span></span>

<span data-ttu-id="c81d9-108">Joissakin tapauksissa voit lisätä tai poistaa työtilauksen ennusterivejä.</span><span class="sxs-lookup"><span data-stu-id="c81d9-108">In some cases, you may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="c81d9-109">Työtilauksen elinkaaritilan, siihen liittyvän projektityypin ja projektityyppiin liittyvien vaihesääntöjen määrittäminen määrittää, voitko lisätä tai muokata kirjauskansiorivejä.</span><span class="sxs-lookup"><span data-stu-id="c81d9-109">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determine if you are able to add or edit journal lines.</span></span> <span data-ttu-id="c81d9-110">Lisätietoja työtilausten elinkaaritiloista ja niihin liittyvistä projektin vaiheista on kohdassa [Ennusteet, työtilaukset ja projektit](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="c81d9-110">Read more about work order lifecycle states and related project stages in [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

>[!NOTE]
><span data-ttu-id="c81d9-111">Kirjauskansioiden automaattisen kirjauksen voi määrittää työtilauksen elinkaaritilalle.</span><span class="sxs-lookup"><span data-stu-id="c81d9-111">It is possible to set up automatic posting of journals on a work order lifecycle state.</span></span> <span data-ttu-id="c81d9-112">Lisätietoja on kohdassa [Työtilauksen elinkaaren tilat](../setup-for-work-orders/work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="c81d9-112">Refer to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) for more information.</span></span>

1. <span data-ttu-id="c81d9-113">Valitse **Resurssien hallinta** >  **yhteiset** >  **työtilaukset** >  **kaikki työtilaukset** tai **Aktiiviset työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="c81d9-113">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="c81d9-114">Valitse työtilaus ja valitse **Kirjauskansiot**.</span><span class="sxs-lookup"><span data-stu-id="c81d9-114">Select the work order, and click **Journals**.</span></span>

3. <span data-ttu-id="c81d9-115">Siirrä kaikki työtilaukseen mahdollisesti liitetyt ennusterivit valitsemalla **Kopioi ennusteesta**.</span><span class="sxs-lookup"><span data-stu-id="c81d9-115">Click **Copy from forecast** to transfer any forecast lines that may be connected to the work order.</span></span> <span data-ttu-id="c81d9-116">Voit valita, mitkä kulutustyypit haluat siirtää.</span><span class="sxs-lookup"><span data-stu-id="c81d9-116">You can select which consumption types you want to transfer.</span></span>

4. <span data-ttu-id="c81d9-117">Tarvittaessa voit lisätä kulutusrivejä asianmukaiseen pikavälilehteen valitsemalla **Lisää rivi** ja täyttämällä rivin tiedot.</span><span class="sxs-lookup"><span data-stu-id="c81d9-117">If necessary, you can add more consumption lines on the relevant FastTab by clicking **Add line** and filling out data on the line.</span></span>

5. <span data-ttu-id="c81d9-118">Valitse **Vahvista kirjauskansiot** vahvistaaksesi kirjauskansiorivit ennen kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="c81d9-118">Click **Validate journals** to validate the journal lines before posting.</span></span>

6. <span data-ttu-id="c81d9-119">Kirjaa kirjauskansion rivit valitsemalla **Kirjaa kirjauskansiot**.</span><span class="sxs-lookup"><span data-stu-id="c81d9-119">Click **Post journals** to post the journal lines.</span></span>

7. <span data-ttu-id="c81d9-120">Kun olet kirjannut kulutuksen kirjauskansiot, voit päivittää työtilauksen elinkaaren tilan.</span><span class="sxs-lookup"><span data-stu-id="c81d9-120">After you've posted the consumption journals, you can update the work order lifecycle state.</span></span> <span data-ttu-id="c81d9-121">Voit esimerkiksi päivittää työtilauksen elinkaaren tilaksi "Päättynyt", kun se on suoritettu loppuun.</span><span class="sxs-lookup"><span data-stu-id="c81d9-121">For example, to indicate that the work order has been completed, you can update the lifecycle state to "Ended".</span></span>

    - <span data-ttu-id="c81d9-122">Valitse **Työtilauksen kirjauskansiot** -sivun yläosassa olevasta **Näytä**-kentästä, mitä kirjauskansiorivejä haluat tarkastella: **Kaikki**, **Ei kirjattu** tai **Kirjattu**.</span><span class="sxs-lookup"><span data-stu-id="c81d9-122">In the **Show** field at the top of the **Work order journals** page, select which journal lines you want to see: **All**, **Not posted**, or **Posted**.</span></span> <span data-ttu-id="c81d9-123">Kirjatuilla kirjauskansiolla on rasti **Kirjattu**-valintaruudussa.</span><span class="sxs-lookup"><span data-stu-id="c81d9-123">Posted journals have a check mark in the **Posted** check box.</span></span>  
    - <span data-ttu-id="c81d9-124">Kun nimikerivit luodaan työtilauskirjauskansiossa, nimikkeeseen liittyvät tuotedimensiot ja seurantadimensiot siirretään automaattisesti kirjauskansion riville.</span><span class="sxs-lookup"><span data-stu-id="c81d9-124">When item lines are created in the work order journal, product dimensions and tracking dimensions related to the item are automatically transferred to the journal line.</span></span>  

<span data-ttu-id="c81d9-125">Alla oleva kuvakaappaus näyttää esimerkin tunti- ja nimikerekisteröinneistä työtilaukselle kohdassa **Työtilauksen kirjauskansiot**.</span><span class="sxs-lookup"><span data-stu-id="c81d9-125">The screenshot below shows an example of hour and item registrations on a work order in **Work order journals**.</span></span>

![Kuva 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a><span data-ttu-id="c81d9-127">Jaa työtilausten tunnit useisiin työtilaustöihin</span><span class="sxs-lookup"><span data-stu-id="c81d9-127">Split hours on work orders with several work order jobs</span></span>

<span data-ttu-id="c81d9-128">Jos työtilaus sisältää useita työtilaustöitä, voit rekisteröidä työtunnit käyttämällä **Jaa tunnit** -toimintoa eli yksi tuntien rekisteröintirivi voidaan jakaa tasaisesti kullekin työtilaustyölle.</span><span class="sxs-lookup"><span data-stu-id="c81d9-128">If a work order contains several work order jobs, you can register work hours using the **Split hours** functionality, meaning one hour registration line can be distributed evenly on each work order job.</span></span>

1. <span data-ttu-id="c81d9-129">Valitse **Resurssien hallinta** >  **yhteiset** >  **työtilaukset** >  **kaikki työtilaukset** tai **Aktiiviset työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="c81d9-129">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="c81d9-130">Valitse työtilaus ja valitse **Kirjauskansiot**.</span><span class="sxs-lookup"><span data-stu-id="c81d9-130">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="c81d9-131">Valitse jaettava tuntikirjausrivi ja valitse sitten **Jaa tunnit.**</span><span class="sxs-lookup"><span data-stu-id="c81d9-131">Select the hour registration line you want to split, and click **Split hours**.</span></span>

4. <span data-ttu-id="c81d9-132">**Jaa työtilauksen ylläpitotöiden tunnit** -valintaikkunassa näkyy automaattisesti **Työntekijä**-kentässä sisäänkirjautuneen työntekijän nimi.</span><span class="sxs-lookup"><span data-stu-id="c81d9-132">In the **Split hours on work order maintenance jobs** dialog, the name of the worker who is logged in is automatically shown in the **Worker** field.</span></span> <span data-ttu-id="c81d9-133">Voit valita toisen työntekijän tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="c81d9-133">If required, you can select another worker.</span></span>

5. <span data-ttu-id="c81d9-134">Valitse tuntirekisteröintien luokka **Luokka** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="c81d9-134">Select a category for the hour registration in the **Category** field.</span></span>

6. <span data-ttu-id="c81d9-135">Lisää jaettavat työtunnit **Tunnit** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="c81d9-135">Insert number of work hours to be split in the **Hours** field.</span></span>

    ![Kuva 2](media/02-consumption.png)

7. <span data-ttu-id="c81d9-137">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="c81d9-137">Click **OK**.</span></span>

<span data-ttu-id="c81d9-138">*Esimerkki:* Alla olevassa kuvakaappauksessa näytetään kolme työtilaustyötä sisältävän työtilauksen kirjauskansiorivit.</span><span class="sxs-lookup"><span data-stu-id="c81d9-138">*Example:* In the screenshot below, journal lines for a work order containing three work order jobs are shown.</span></span> <span data-ttu-id="c81d9-139">Ensimmäinen rivi, joka sisältää kolme työtuntia, on jaettu, ja kullekin työtilaustyölle rekisteröidään yksi työtunti.</span><span class="sxs-lookup"><span data-stu-id="c81d9-139">The first line, containing three work hours, has been split, and one work hour is registered on each work order job.</span></span> <span data-ttu-id="c81d9-140">Kun kolmen tunnin kirjausrivit on luotu, voit päättää, mitä haluat tehdä alkuperäiselle tuntikirjausriville (esimerkin ensimmäinen rivi).</span><span class="sxs-lookup"><span data-stu-id="c81d9-140">After the three hour registration lines have been created, you decide what to do with the original hour registration line (the first line in the example).</span></span> <span data-ttu-id="c81d9-141">Voit pitää sen sellaisena kuin se on tai poistaa sen.</span><span class="sxs-lookup"><span data-stu-id="c81d9-141">You can keep it as is or delete it.</span></span> 

![Kuva 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a><span data-ttu-id="c81d9-143">Kulutusrekisteröintien taloushallinnon dimensiot</span><span class="sxs-lookup"><span data-stu-id="c81d9-143">Financial dimensions on consumption registrations</span></span>

<span data-ttu-id="c81d9-144">Kun teet kulutusmerkintöjä, eri rekisteröintityyppeihin liittyvät taloushallinnon dimensiot lisätään rekisteröinteihin tietyssä järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="c81d9-144">When you make consumption registrations, financial dimensions related to the different registration types are added to the registrations in a specific sequence.</span></span> 

- <span data-ttu-id="c81d9-145">*Tunti- ja kulurekisteröinnit* : Ensin lisätään kirjauskansion otsikon taloushallinnon dimensiot, jos sellaisia on.</span><span class="sxs-lookup"><span data-stu-id="c81d9-145">*Hour and Expense registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="c81d9-146">Seuraavaksi lisätään liittyvän työtilausprojektin taloushallinnon dimensiot.</span><span class="sxs-lookup"><span data-stu-id="c81d9-146">Next, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="c81d9-147">Lopuksi lisätään resurssin (työntekijän) taloushallinnon dimensiot.</span><span class="sxs-lookup"><span data-stu-id="c81d9-147">Finally, financial dimensions from the resource (worker) are added.</span></span>

- <span data-ttu-id="c81d9-148">*Nimikerekisteröinnit* : Ensin lisätään kirjauskansion otsikon taloushallinnon dimensiot, jos sellaisia on.</span><span class="sxs-lookup"><span data-stu-id="c81d9-148">*Item registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="c81d9-149">Sitten lisätään liittyvän työtilausprojektin taloushallinnon dimensiot.</span><span class="sxs-lookup"><span data-stu-id="c81d9-149">Then, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="c81d9-150">Seuraavaksi lisätään toimipaikan taloushallinnon dimensiot.</span><span class="sxs-lookup"><span data-stu-id="c81d9-150">Next, financial dimensions from the site are added.</span></span> <span data-ttu-id="c81d9-151">Lopuksi lisätään nimikkeen taloushallinnon dimensiot.</span><span class="sxs-lookup"><span data-stu-id="c81d9-151">Finally, financial dimensions from the item are added.</span></span>

>[!NOTE]
><span data-ttu-id="c81d9-152">Kaikkien kolmen kirjaustyypin osalta taloushallinnon dimensioyhdistelmä tarkistetaan ja virheelliset yhdistelmät poistetaan.</span><span class="sxs-lookup"><span data-stu-id="c81d9-152">For all three registration types, the financial dimension combination is validated, and invalid combinations are blanked.</span></span> <span data-ttu-id="c81d9-153">Tämä on vakioasetus muiden Finance and Operations -sovellusten kanssa.</span><span class="sxs-lookup"><span data-stu-id="c81d9-153">This is standard setup with other Finance and Operations apps.</span></span>

