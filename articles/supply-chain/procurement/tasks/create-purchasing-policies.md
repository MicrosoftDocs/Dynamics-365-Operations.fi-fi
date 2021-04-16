---
title: Luo ostokäytännöt
description: Tässä aiheessa kuvataan, miten luot ostokäytäntöjä, jotka vastaavat ostojen liiketoimintaprosessejasi.
author: kamaybac
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2cc64d0b9492a7bfcf0076ea74ca36a9a26ee6c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812203"
---
# <a name="create-purchasing-policies"></a><span data-ttu-id="8757e-103">Luo ostokäytännöt</span><span class="sxs-lookup"><span data-stu-id="8757e-103">Create purchasing policies</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8757e-104">Tässä aiheessa kuvataan, miten luot ostokäytäntöjä, jotka vastaavat ostojen liiketoimintaprosessejasi.</span><span class="sxs-lookup"><span data-stu-id="8757e-104">This topic shows you how to create purchasing policies to align with your business processes for purchasing.</span></span> <span data-ttu-id="8757e-105">Ennen kuin voit luoda ostokäytäntöjä, sinun täytyy määrittää ostokäytäntöparametrit.</span><span class="sxs-lookup"><span data-stu-id="8757e-105">Before you can create purchasing policies, you must set up the purchasing policy parameters.</span></span> <span data-ttu-id="8757e-106">Voit luoda, muokata ja keskeyttää ostokäytännön, mutta et voi poistaa ostokäytäntöä.</span><span class="sxs-lookup"><span data-stu-id="8757e-106">It's possible to create, modify, and retire a purchasing policy, but you can't delete a purchasing policy.</span></span> <span data-ttu-id="8757e-107">Yleensä ostopäällikkö tekee tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="8757e-107">This procedure would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="8757e-108">Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoilla tai omilla tiedoillasi.</span><span class="sxs-lookup"><span data-stu-id="8757e-108">You can use this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-policy-parameters"></a><span data-ttu-id="8757e-109">Aseta käytäntöparametri</span><span class="sxs-lookup"><span data-stu-id="8757e-109">Set up policy parameters</span></span>
1. <span data-ttu-id="8757e-110">Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Asetukset > Käytännöt > Ostokäytännöt**.</span><span class="sxs-lookup"><span data-stu-id="8757e-110">In the navigation pane, go to **Modules > Procurement and sourcing > Setup > Policies > Purchasing policies**.</span></span>
2. <span data-ttu-id="8757e-111">Valitse toimintoruudussa **Parametrit**.</span><span class="sxs-lookup"><span data-stu-id="8757e-111">On the Action Pane, select **Parameters**.</span></span>
- <span data-ttu-id="8757e-112">Käytännön ohitussäännöt koskevat eri tasoja organisaatiossasi.</span><span class="sxs-lookup"><span data-stu-id="8757e-112">Policy precedence rules apply to different levels in your organization.</span></span> <span data-ttu-id="8757e-113">Näkyvissä olevat organisaatioyksiköt määräytyvät organisaatiohierarkian mukaan ja mille hierarkian tasoille on määritetty tarkoitukseksi hankinnan sisäinen tarkistus.</span><span class="sxs-lookup"><span data-stu-id="8757e-113">The organizational units that are shown depend on your organizational hierarchy, and on which levels in the hierarchy have been assigned the purpose of Procurement internal control.</span></span> <span data-ttu-id="8757e-114">Organisaatiossa voi olla yrityksiä, kustannuspaikkoja, alueita ja osastoja, mutta voi olla, että vain joillain näistä on hierarkian tarkoituksena hankinnan sisäinen tarkastus.</span><span class="sxs-lookup"><span data-stu-id="8757e-114">For example, your organization might have legal entities, cost centers, regions, and departments, but it may be that only some of these have a hierarchy purpose of Procurement internal control.</span></span> <span data-ttu-id="8757e-115">Oletuksena käytettävä organisaation tyyppi on Yritys.</span><span class="sxs-lookup"><span data-stu-id="8757e-115">As a default, the organization of type Company is available.</span></span>  
3. <span data-ttu-id="8757e-116">Napsauta **Käytäntösäännön tyyppiparametrit** -välilehteä.</span><span class="sxs-lookup"><span data-stu-id="8757e-116">Select the **Policy rule type parameters** tab.</span></span>
4. <span data-ttu-id="8757e-117">Valitse puurakenteessa **Ostokäytäntö > Ostoehdotuksen hallintasääntö**.</span><span class="sxs-lookup"><span data-stu-id="8757e-117">In the tree, go to **Purchasing policy > Purchase requisition control rule**.</span></span>
- <span data-ttu-id="8757e-118">Voit määrittää käytännön ratkaisun käsittelyjärjestyksen käytännön tasolla.</span><span class="sxs-lookup"><span data-stu-id="8757e-118">You define the order of precedence for policy resolution at the policy level.</span></span> <span data-ttu-id="8757e-119">Kuitenkin tiettyjen käytäntötyyppien käsittelyjärjestyksen voi ohittaa yksittäisissä käytäntösääntötyypeissä.</span><span class="sxs-lookup"><span data-stu-id="8757e-119">However, for some policy types, you can override the order of precedence for individual policy rule types.</span></span> <span data-ttu-id="8757e-120">Voit esimerkiksi määrittää ostokäytäntöjen ensisijaisuuden tässä järjestyksessä: kustannuskeskus, osasto, yritys.</span><span class="sxs-lookup"><span data-stu-id="8757e-120">For example, you might define the order of precedence for purchasing policies to be: cost center, department, company.</span></span> <span data-ttu-id="8757e-121">Voit haluta luettelon käytäntösäännön ensisijaisuusjärjestyksen olevan tässä järjestyksessä: osasto, kustannuspaikka, yritys.</span><span class="sxs-lookup"><span data-stu-id="8757e-121">For the catalog policy rule, you might want the order of precedence to be: department, cost center, company.</span></span> <span data-ttu-id="8757e-122">Voit muuttaa luettelon käytäntösäännön käsittelyjärjestystä.</span><span class="sxs-lookup"><span data-stu-id="8757e-122">You can change the order of precedence for the Catalog policy rule.</span></span> <span data-ttu-id="8757e-123">Kun työntekijä luo varasto-ottoehdotuksen, näytettävä luettelo määräytyy järjestyksessä niiden käytäntöjen perusteella, jotka on liitetty työntekijän osastoon, sitten kustannuspaikkaan ja viimeiseksi yritykseen.</span><span class="sxs-lookup"><span data-stu-id="8757e-123">When a worker creates a requisition, the catalog that is displayed is determined by the policies that are associated with the worker's department, then their cost center, and then their company.</span></span>  
- <span data-ttu-id="8757e-124">Jos luettelossa on useampi organisaatiotaso, voit määrittää järjestyssäännön ylä-/alanuolilla Ostoehdotuksen ohjaussäännölle.</span><span class="sxs-lookup"><span data-stu-id="8757e-124">If there's more than one organizational level listed, you can use the Up/Down arrows to set the order of precedence for the Purchase requisition control rule.</span></span>  
5. <span data-ttu-id="8757e-125">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8757e-125">Close the page.</span></span>

## <a name="create-a-new-policy"></a><span data-ttu-id="8757e-126">Luo uusi käytäntö</span><span class="sxs-lookup"><span data-stu-id="8757e-126">Create a new policy</span></span>
1. <span data-ttu-id="8757e-127">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="8757e-127">Select **New**.</span></span>
2. <span data-ttu-id="8757e-128">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8757e-128">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="8757e-129">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="8757e-129">In the **Description** field, type a value.</span></span>
- <span data-ttu-id="8757e-130">Yksi ostokäytäntö voi koskea vain yhtä organisaatiohierarkiaa.</span><span class="sxs-lookup"><span data-stu-id="8757e-130">A single purchasing policy can only apply to one organization hierarchy.</span></span> <span data-ttu-id="8757e-131">Yksi hierarkia voi olla esimerkiksi "Maantieteellinen" ja toinen "Osasto", ja molemmilla voi olla erillinen ostokäytäntö.</span><span class="sxs-lookup"><span data-stu-id="8757e-131">For example, you could have one hierarchy called "Geographic" and one called "Department", and have a different purchasing policy for each.</span></span>  
- <span data-ttu-id="8757e-132">Valitse organisaatio, jota käytäntö koskee.</span><span class="sxs-lookup"><span data-stu-id="8757e-132">Select an organization that the policy should apply to.</span></span>  
4. <span data-ttu-id="8757e-133">Valitse haluttu organisaatio napsauttamalla nuolta.</span><span class="sxs-lookup"><span data-stu-id="8757e-133">Select the arrow to add the selected organization.</span></span>
- <span data-ttu-id="8757e-134">Voit toistaa prosessin lisätäksesi useita organisaatioita.</span><span class="sxs-lookup"><span data-stu-id="8757e-134">You can repeat this process to add more organizations.</span></span>  

## <a name="add-a-policy-rule"></a><span data-ttu-id="8757e-135">Lisää käytäntösääntö</span><span class="sxs-lookup"><span data-stu-id="8757e-135">Add a policy rule</span></span>
1. <span data-ttu-id="8757e-136">Valitse **Käytäntösäännön tyyppi** -luettelossa **Ehdotuksen tarkoitussääntö**.</span><span class="sxs-lookup"><span data-stu-id="8757e-136">In the **Policy rule type** list, select **Requisition purpose rule**.</span></span>
- <span data-ttu-id="8757e-137">Luot säännön, joka määrittää ostoehdotuksen oletustarkoitukseksi kulutuksen, mutta sallii myös täydennyksen valinnan sen sijaan.</span><span class="sxs-lookup"><span data-stu-id="8757e-137">You'll create a rule that sets the default requisition purpose to type Consumption but allows the Replenishment type to be selected instead.</span></span>  
2. <span data-ttu-id="8757e-138">Valitse **Luo käytäntösääntö**.</span><span class="sxs-lookup"><span data-stu-id="8757e-138">Select **Create policy rule**.</span></span>
3. <span data-ttu-id="8757e-139">Valitse **Salli manuaalinen ohitus** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="8757e-139">Select **Yes** in the **Allow manual override** field.</span></span>
4. <span data-ttu-id="8757e-140">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="8757e-140">Select **Close**.</span></span>
- <span data-ttu-id="8757e-141">Voit nyt määrittää muut ostokäytännön käytäntösäännöt.</span><span class="sxs-lookup"><span data-stu-id="8757e-141">Now you can set up other policy rules for the purchasing policy.</span></span> <span data-ttu-id="8757e-142">Huomaa, että käytäntösääntötyyppi ei voi sisältää päällekkäisiä sääntöjä, jotka ovat aktiivisia samaan aikaan yhdessä hankintasäännössä.</span><span class="sxs-lookup"><span data-stu-id="8757e-142">Note that a Policy rule type cannot have overlapping rules that are active at the same time within a single procurement policy.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]