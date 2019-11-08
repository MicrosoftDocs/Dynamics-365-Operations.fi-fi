---
title: Luo ylläpitopyyntöjä
description: Tässä ohjeaiheessa kerrotaan, kuinka ylläpitopyynnöt luodaan resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7fc9ec2f6a9a8a11d824e4b5c13d5aa173541454
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571918"
---
# <a name="create-maintenance-requests"></a><span data-ttu-id="7b7ac-103">Luo ylläpitopyyntöjä</span><span class="sxs-lookup"><span data-stu-id="7b7ac-103">Create maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="7b7ac-104">Ylläpitopyyntöjä voidaan käyttää, jos huoltotyöntekijät tai tuotannon työntekijät saavat selville, että laitteet vaativat korjausta, mutta korjaustyötä ei voi tehdä heti.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-104">Maintenance requests can be used if maintenance workers or production workers discover that equipment requires repair, but the repair job can't be done right away.</span></span>

<span data-ttu-id="7b7ac-105">**Esimerkki:** Kun kunnossapitotyöntekijä tekee korjauksen, hän havaitsee, että samassa sijainnissa on huollettava toinenkin resurssi.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-105">**Example:** While a maintenance worker is making a repair, she discovers that another asset at the same location must be serviced.</span></span> <span data-ttu-id="7b7ac-106">Huoltotyöntekijällä ei kuitenkaan ole aikaa tai tarvittavia varaosia korjaustyön tekemistä varten.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-106">However, the maintenance worker doesn't have the time or the required spare parts to do the repair job.</span></span> <span data-ttu-id="7b7ac-107">Tämän vuoksi hän luo resurssille ylläpitopyynnön ja kirjoittaa ongelmasta lyhyen kuvauksen.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-107">Therefore, she creates a maintenance request on the asset and enters a short description of the issue.</span></span>

<span data-ttu-id="7b7ac-108">**Aktiiviset ylläpitopyynnöt** -osa **Aiheeseen liittyviä tietoja** -ruudussa **Kaikki resurssit**- tai **Aktiiviset resurssit** -sivulla (**Resurssien hallinta** \> **Yhteiset** \> **Resurssit** \> **Kaikki resurssit** tai **Aktiiviset resurssit**) näyttää aktiiviset ylläpitopyynnöt, jotka on liitetty valittuuun resurssiin.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-108">The **Active maintenance requests** section of the **Related information** pane on the right side of the **All assets** or **Active assets** page (**Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**) shows the active maintenance requests that are attached to the selected asset.</span></span>

1. <span data-ttu-id="7b7ac-109">Valitse **Resurssien hallinta** \> **yhteiset** \> **Ylläpitopyynnöt** \> **Kaikki ylläpitopyynnöt** ta **Aktiiviset ylläpitopyynnöt**.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="7b7ac-110">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-110">Select **New**.</span></span>
3. <span data-ttu-id="7b7ac-111">Valitse **Luo pyyntö** -valintaikkunan **Ylläpitopyynnön tyyppi** -kentässä ylläpitopyynnön tyyppi.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-111">In the **Create request** dialog box, in the **Maintenance request type** field, select the type of maintenance request.</span></span> <span data-ttu-id="7b7ac-112">Ehdotetaan oletustyyppiä.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-112">A default type is suggested.</span></span>
4. <span data-ttu-id="7b7ac-113">Kirjoita **kuvaus**-kenttään nimi tai otsikko, joka kuvaa lyhyesti ylläpitopyyntöä.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-113">In the **Description** field, enter a name or title that briefly describes the maintenance request.</span></span>
5. <span data-ttu-id="7b7ac-114">Valitse **toiminnallinen sijainti**- ja **resurssi**-kentissä toiminnallinen sijainti tai resurssi tai toiminnallisen sijainnin ja resurssin yhdistelmä, kuten tarvitset.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-114">In the **Functional location** and **Asset** fields, select a functional location or an asset, or a combination of a functional location and an asset, as you require.</span></span> <span data-ttu-id="7b7ac-115">Voit luoda ylläpitopyynnön valitsematta resurssia, ja resurssi voidaan lisätä ylläpitopyyntöön myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-115">You can create a maintenance request without selecting an asset, and the asset can be added to the maintenance request later.</span></span> <span data-ttu-id="7b7ac-116">Jos kirjautunut kunnossapitotyöntekijä liittyy resurssiin liittyvään resurssiin **Resurssi**-kenttä määritetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-116">If the maintenance worker who is signed in is related to a resource that is related to an asset, the **Asset** field is automatically set.</span></span>

    <span data-ttu-id="7b7ac-117">Jos valittuun resurssiin on jo liitetty ylläpitopyyntö, **Luo pyyntö** -valintaikkunan yläosassa näkyy sanomapalkki, joka ilmoittaa olemassa olevan ylläpitopyynnön tunnuksesta.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-117">If a maintenance request is already attached to the selected asset, a message bar appears at the top of the **Create request** dialog box to notify you about the ID of the existing maintenance request.</span></span> <span data-ttu-id="7b7ac-118">Sanomapalkki ilmoittaa myös, jos resurssi kuuluu takuusopimuksen piiriin.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-118">A message bar also notifies you if the asset is covered by a warranty agreement.</span></span>

6. <span data-ttu-id="7b7ac-119">Valitse **Palvelutaso**-kentässä palvelutasto, joka ilmaisee pyynnön kiireellisyyden.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-119">In the **Service level** field, select a service level that indicates the urgency of the request.</span></span>
7. <span data-ttu-id="7b7ac-120">Jos valitsit resurssin vaiheessa 5, voit luoda vikarekisteröinnin käyttämällä kenttiä **Vian oire**, **Vika-alue** ja **Vikatyyppi**.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-120">If you selected an asset in step 5, you can use the **Fault symptom**, **Fault area**, and **Fault type** fields to create a fault registration.</span></span>
8. <span data-ttu-id="7b7ac-121">Jos huoltopyyntö on aiheuttanut huoltokatkoksia, anna seisonta-ajan alkamispäivä ja -aika.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-121">If the maintenance request has caused maintenance downtime, enter the start date and time of the downtime.</span></span>

    <span data-ttu-id="7b7ac-122">**Aloittanut** -kentän arvoksi määritetään automaattisesti nimesi.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-122">The **Started by** field is automatically set to your name.</span></span>

10. <span data-ttu-id="7b7ac-123">**Toteutunut aloitus** -kenttään valitaan automaattisesti nykyinen päivämäärä ja aika.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-123">The **Actual start** field is automatically set to the current date and time.</span></span> <span data-ttu-id="7b7ac-124">Voit kuitenkin muuttaa arvoa tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-124">However, you can change the value as you require.</span></span>
11. <span data-ttu-id="7b7ac-125">Kirjoita **Huomautukset**-kenttään tarvittavat lisähuomautukset.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-125">In the **Notes** field, enter any additional notes that are required.</span></span>
12. <span data-ttu-id="7b7ac-126">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-126">Select **OK**.</span></span>

![Luo ylläpitopyyntö](media/03-manage-maintenance-requests.png)

## <a name="subsequent-processing-of-maintenance-requests"></a><span data-ttu-id="7b7ac-128">Kunnossapitopyyntöjen myöhempi käsittely</span><span class="sxs-lookup"><span data-stu-id="7b7ac-128">Subsequent processing of maintenance requests</span></span>

<span data-ttu-id="7b7ac-129">Kun ylläpitopyyntö on luotu, mutta ennen kuin se muunnetaan työtilaukseksi, siihen tulee päivittää erilaisia tietoja.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-129">After a maintenance request is created, but before it's converted to a work order, various information should be updated on it.</span></span> <span data-ttu-id="7b7ac-130">Yleensä suunnittelija tai muu hallinnollinen työntekijä suorittaa tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-130">Typically, a planner or another administrative employee completes this task.</span></span>

- <span data-ttu-id="7b7ac-131">Valitse **Kaikki ylläpitopyynnöt**- tai **Aktiiviset ylläpitopyynnöt** -sivulla haluamasi pyyntö ja valitse sitten **Muokkaa** .</span><span class="sxs-lookup"><span data-stu-id="7b7ac-131">On the **All maintenance requests** or **Active maintenance requests** page, select the request to work with, and then select **Edit**.</span></span>

<span data-ttu-id="7b7ac-132">Tiedot-näkymässä voit päivittää erilaisia tietoja.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-132">In the details view, you can update various information.</span></span> <span data-ttu-id="7b7ac-133">Seuraavassa on muutamia esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="7b7ac-133">Here are some examples:</span></span>

- <span data-ttu-id="7b7ac-134">Valitse ja vahvista resurssi.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-134">Select and verify the asset.</span></span> <span data-ttu-id="7b7ac-135">Jos sinun on valittava toinen resurssi myöhemmin, voit määrittää **Resurssi vahvistettu** -asetukseksi **Ei**.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-135">If you must select a different asset later, you can set the **Asset verified** option to **No**.</span></span>
- <span data-ttu-id="7b7ac-136">Valitse vastuullinen kunnossapitotyöntekijäryhmä ja/tai vastuullinen huoltotyöntekijä.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-136">Select a responsible maintenance worker group and/or a responsible maintenance worker.</span></span> <span data-ttu-id="7b7ac-137">Lisätietoja vaadittavista asetuksista on kohdassa [Vastuulliset kunnossapitotyöntekijät](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="7b7ac-137">For more information about the required setup, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>
- <span data-ttu-id="7b7ac-138">Valitse kunnossapitotyön tyyppi ja, jos nämä tiedot ovat merkityksellisiä, liittyvä kunnossapitotyön variantti ja työn toimiala.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-138">Select a maintenance job type and, if this information is relevant, a related maintenance job variant and a job trade.</span></span>
- <span data-ttu-id="7b7ac-139">Kirjoita **Leveysaste**- ja **Pituusaste**-kenttiin maantieteelliset koordinaatit.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-139">In the **Latitude** and **Longitude** fields, enter geographic coordinates.</span></span> <span data-ttu-id="7b7ac-140">Kaikki ylläpitopyyntöön lisätyt koordinaatit siirretään automaattisesti liittyvään työtilaukseen.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-140">Any coordinates that are added to a maintenance request are automatically transferred to a related work order.</span></span> 

![Ylläpitopyynnön päivitys](media/04-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="7b7ac-142">Jos valitset resurssin, kun luot ylläpitopyynnön, voit lisätä resurssiin yhden virheen.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-142">If you select an asset when you create a maintenance request, you can add one fault to the asset.</span></span> <span data-ttu-id="7b7ac-143">Kun kunnossapitopyyntö on luotu, voit lisätä vikoja, kuten tarvitset.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-143">After the maintenance request has been created, you can add more faults, as you require.</span></span> <span data-ttu-id="7b7ac-144">Jos haluat lisätä vikoja, valitse **Resurssin vika** **Kaikki ylläpito pyynnöt** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="7b7ac-144">To add faults, select **Asset fault** on the **All maintenance requests** page.</span></span>
