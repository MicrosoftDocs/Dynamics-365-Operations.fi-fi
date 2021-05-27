---
title: Varaston erä- ja sarjavaraushierarkioiden vianmääritys
description: Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun käytetään varaushierarkioita, jotka käyttävät erä- tai sarjadimensioita.
author: perlynne
ms.date: 3/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 3/12/2021
ms.openlocfilehash: 1cd4883cdd95a97f821e0103da910e2c0346a08d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022543"
---
# <a name="troubleshoot-warehouse-batch-and-serial-reservation-hierarchies"></a><span data-ttu-id="9ab1a-103">Varaston erä- ja sarjavaraushierarkioiden vianmääritys</span><span class="sxs-lookup"><span data-stu-id="9ab1a-103">Troubleshoot warehouse batch and serial reservation hierarchies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ab1a-104">Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun käytetään varaushierarkioita, jotka käyttävät erä- tai sarjadimensioita.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-104">This topic describes how to fix common issues that you might encounter while you work with reservation hierarchies that use batch or serial dimensions.</span></span>

<span data-ttu-id="9ab1a-105">Lisätietoja on kohdassa [Joustava varastotason dimensioiden varauskäytäntö](flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="9ab1a-105">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>

<span data-ttu-id="9ab1a-106">Nimikkeen varaushierarkia määrittää tarpeen varastodimensioille, jotka on täytettävä, jotta sijainti voidaan liittää kysyntätilaukseen.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-106">The reservation hierarchy of an item dictates the requirement of storage dimensions that must be fulfilled to assign a location to a demand order.</span></span> <span data-ttu-id="9ab1a-107">Näitä dimensioita voidaan kuvata *sijainnin yläpuolella oleviksi dimensioiksi* kaikille niille dimensioille, jotka on täytettävä ennen sijainnin määrittämistä, ja *dimensioiksi sijainnin alapuolella* niille dimensioille, jotka voidaan kohdistaa sen jälkeen, kun sijainti on liitetty kysyntätilaukseen.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-107">These dimensions can be described as *dimensions above location*, for all the dimensions that must be fulfilled before a location is assigned, and *dimensions below location*, for dimensions that can be allocated after a location has been assigned to the demand order.</span></span> <span data-ttu-id="9ab1a-108">Näitä varaushierarkioita kutsutaan myös *erä-yllä*- ja *erä-alla*-varaushierarkioiksi tai *sarja-yllä*- ja *sarja-alla*-varaushierarkioiksi.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-108">These reservation hierarchies are also known as *batch-above* and *batch-below* reservation hierarchies, or *serial-above* and *serial-below* reservation hierarchies.</span></span>

<span data-ttu-id="9ab1a-109">Varasto voidaan kohdistaa onnistuneesti vain, jos sijainnin yläpuolella olevissa dimensioissa ei ole aukkoja.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-109">Inventory can be successfully allocated only if there are no gaps in the dimensions above location.</span></span> <span data-ttu-id="9ab1a-110">Esimerkiksi *erä-yllä*-varaushierarkiassa odotat, että **Toimipaikka**-, **Varasto**- ja **Eränumero**-dimensiot määritetään kysyntätilauksessa.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-110">For example, in a *batch-above* reservation hierarchy, you expect **Site,** **Warehouse,** and **Batch number** dimensions to be specified on the demand order.</span></span> <span data-ttu-id="9ab1a-111">Jos jokin näistä dimensioista puuttuu, kohdistusprosessi epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-111">If any of these dimensions are missing, the allocation process will fail.</span></span> <span data-ttu-id="9ab1a-112">Sen sijaan alla *erä-alla* tai *sarja-alla*-varaushierarkiassa erä- tai sarjanumero voidaan määrittää kysyntätilauksessa, mutta kohdistusprosessi ei edellytä sitä.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-112">By contrast, in a *batch-below* or *serial-below* reservation hierarchy, a batch or serial number might be specified on the demand order, but the allocation process doesn't require it.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="9ab1a-113">Seuraava virhesanoma avautuu: Jotta kuormituksen rivit voidaan määrittää aaltoon, niiden on määritettävä dimensiot sijainnin yläpuolelle.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-113">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="9ab1a-114">Voit määrittää nämä dimensiot varaamalla kuormituksen rivin ja luomalla sen uudelleen.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-114">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="9ab1a-115">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="9ab1a-115">Issue description</span></span>

<span data-ttu-id="9ab1a-116">Jos käytät nimikettä, jossa käytetään *erä-yllä*-varaushierarkiaa osittaisen määrän **Kuormasuunnittelun työtila** -sivun **Vapauta varastoon** -komento ei toimi, jos yrität vapauttaa kuorman.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-116">When you use an item that has a *batch-above* reservation hierarchy, the **Release to warehouse** command on the **Load planning workbench** page doesn't work if you try to release a load for a partial quantity.</span></span> <span data-ttu-id="9ab1a-117">Sait tämän virhesanoma eikä osittaiselle määrälle luoda yhtään työtä.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-117">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="9ab1a-118">Jos käytät kuitenkin nimikettä, jossa käytetään *erä-alla*-varaushierarkiaa, voit vapauttaa kuorman osittaisen määrän **Kuormasuunnittelun työtila** -sivulta.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-118">However, when you use an item that has a *batch-below* reservation hierarchy, you can release a load for a partial quantity from the **Load planning workbench** page.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="9ab1a-119">Ongelman syy</span><span class="sxs-lookup"><span data-stu-id="9ab1a-119">Issue cause</span></span>

<span data-ttu-id="9ab1a-120">Jos dimensio on **Sijainti**-dimension yläpuolella varaushierarkiassa, se on määritettävä ennen vapautusta varastoon.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-120">When a dimension is above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="9ab1a-121">Osittaisia määriä ei voi vapauttaa, jos vähintään yhtä **Sijainti**-dimension yläpuolella olevaa dimensiota ei ole määritetty.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-121">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

## <a name="the-auto-reservation-prompt-for-a-batch-number-is-triggered-even-though-there-is-available-inventory"></a><span data-ttu-id="9ab1a-122">Eränumeron automaattinen varauskehote käynnistyy, vaikka varastoa on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-122">The auto-reservation prompt for a batch number is triggered even though there is available inventory.</span></span>

### <a name="issue-description"></a><span data-ttu-id="9ab1a-123">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="9ab1a-123">Issue description</span></span>

<span data-ttu-id="9ab1a-124">Kun käytät nimikettä, jolla on *erä-yllä*-varaushierarkia varastossa, joka ei ole ottanut fyysisen varastoinnin prosesseja käyttöön, ja automaattinen varaus on käytössä, eränumeron automaattinen varauskehote tulee näyttöön, vaikka keräilyyn olisi käytettävissä vain yksi erä.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-124">When you use an item that has a *batch-above* reservation hierarchy in a warehouse that hasn't enabled warehouse processes, and automatic reservation is enabled, the auto-reservation prompt for a batch number is shown even if only one batch is available for picking.</span></span>

<span data-ttu-id="9ab1a-125">Kun käytät samaa nimikettä varastossa, jossa fyysisen varastoinnin prosessit ovat käytössä, automaattista varauskehotetta ei näytetä.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-125">However, when you use the same item in a warehouse where warehouse processes are enabled, the auto-reservation prompt isn't shown.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="9ab1a-126">Ongelman syy</span><span class="sxs-lookup"><span data-stu-id="9ab1a-126">Issue cause</span></span>

<span data-ttu-id="9ab1a-127">Jos varaushierarkiaksi on määritetty *erä-yllä* tai *sarja-yllä*, viitattu dimensio (**Eränumero** tai **Sarjanumero**) on aina määritettävä kysyntätilauksissa.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-127">If a reservation hierarchy is defined as *batch-above* or *serial-above*, the referenced dimension (**Batch number** or **Serial number**) must always be specified on demand orders.</span></span> <span data-ttu-id="9ab1a-128">Fyysisen varastoinnin prosessit voivat ehkä täydentää tietoja, jos käytettävissä on yksi erä- tai sarjanumero.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-128">Warehouse processes might be able to complete the information if a single batch or serial number is available.</span></span> <span data-ttu-id="9ab1a-129">Koska varastolle ei kuitenkaan ole otettu käyttöön fyysisen varastoinnin prosesseja, käyttäjän on aina määritettävä kaikki **Sijainti**-kentän yläpuolella olevat dimensiot.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-129">However, because the warehouse isn't enabled for warehouse processes, the user must always specify all the dimensions above **Location**.</span></span>

## <a name="slotting-templates-that-have-the-consider-on-hand-slot-criterion-dont-consider-current-on-hand-inventory-for-batch-enabled-items"></a><span data-ttu-id="9ab1a-130">Paikannusmallit, joilla on Ota huomioon käytettävissä oleva varasto -paikkaehto, eivät ota huomioon nykyistä käytettävissä olevaa varastoa nimikkeille, joille erä on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-130">Slotting templates that have the Consider on-hand slot criterion don't consider current on-hand inventory for batch-enabled items.</span></span>

<span data-ttu-id="9ab1a-131">Lisätietoja on kohdassa [Varastopaikoitus](warehouse-slotting.md).</span><span class="sxs-lookup"><span data-stu-id="9ab1a-131">For more information, see [Warehouse slotting](warehouse-slotting.md).</span></span>

### <a name="issue-description"></a><span data-ttu-id="9ab1a-132">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="9ab1a-132">Issue description</span></span>

<span data-ttu-id="9ab1a-133">Paikannusmallit, joilla on *Ota huomioon käytettävissä oleva varasto* -paikkaehto, eivät ota huomioon nykyistä käytettävissä olevaa varastoa *erä-yllä*-nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-133">Slotting templates that have the *Consider on-hand* slot criterion don't consider current on-hand inventory for *batch-above* items.</span></span> <span data-ttu-id="9ab1a-134">Ne ottavat se huomioon vain, jos eränumero on määritetty myyntitilausrivillä.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-134">They consider it only if the batch number is specified on the sales order line.</span></span>

<span data-ttu-id="9ab1a-135">Kun käytät alla *erä-alla*-nimikkeitä, nykyistä käytettävissä olevaa varastoa pidetään oletettuna.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-135">However, when you use *batch-below* items, the current on-hand inventory is considered as expected.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="9ab1a-136">Ongelman syy</span><span class="sxs-lookup"><span data-stu-id="9ab1a-136">Issue cause</span></span>

<span data-ttu-id="9ab1a-137">Paikannusmallin otsikko voidaan määrittää *Tilattu*-, *Varattu*- tai *Vapautettu*-kysyntästrategialle.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-137">The slotting template header can be defined for the *Ordered,* *Reserved*, or *Released* demand strategy.</span></span> <span data-ttu-id="9ab1a-138">*Tilattu*-kysyntästrategiassa käytetään samoja varaushierarkian vaatimuksia, jotka koskevat varauksen tai varastoon vapautuksen prosesseja.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-138">For the *Ordered* demand strategy, the same reservation hierarchy requirements apply that apply to reservation or release to warehouse processes.</span></span> <span data-ttu-id="9ab1a-139">Siksi erä- tai sarjanumero on määritettävä kysyntätilaukseen (myynti- tai siirtotilaus) niiden nimikkeiden osalta, joissa on *erä-yllä*- tai *erä-alla*-varaushierarkia.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-139">Therefore, for items that have *batch-above* and *serial-below* reservation hierarchies, the batch or serial number must be specified on the demand order (sales or transfer).</span></span> <span data-ttu-id="9ab1a-140">Vaihtoehtoisesti *Varattu*-kysyntästrategian avulla voidaan valita erä- tai sarjanumero, ennen kuin varaston paikannustarve luodaan.</span><span class="sxs-lookup"><span data-stu-id="9ab1a-140">Alternatively, the *Reserved* demand strategy can be used to select the batch or serial number before the warehouse slotting demand is generated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
