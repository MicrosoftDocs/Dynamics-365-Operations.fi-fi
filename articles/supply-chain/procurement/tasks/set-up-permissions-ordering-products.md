---
title: Määritä käyttöoikeudet tuotteiden tilaamiseen jonkun muun puolesta
description: Tässä aiheessa kuvataan, miten myönnät työntekijöille oikeuden valmistella ostoehdotuksia muiden työntekijöiden puolesta.
author: mkirknel
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: baf39040bef2ccd0c643ce0d034348807ecdc50c
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914788"
---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a><span data-ttu-id="25cd6-103">Määritä käyttöoikeudet tuotteiden tilaamiseen jonkun muun puolesta</span><span class="sxs-lookup"><span data-stu-id="25cd6-103">Set up permissions for ordering products on behalf of someone else</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="25cd6-104">Tässä aiheessa kuvataan, miten myönnät työntekijöille oikeuden valmistella ostoehdotuksia muiden työntekijöiden puolesta.</span><span class="sxs-lookup"><span data-stu-id="25cd6-104">This topic explains how to grant workers permission to prepare purchase requisitions on behalf of other workers.</span></span> <span data-ttu-id="25cd6-105">Toisin sanoen ostoehdotuksen valmistelija voi luoda ostoehdotuksia toisen pyynnön lähettäjän puolesta.</span><span class="sxs-lookup"><span data-stu-id="25cd6-105">In other words, a purchase requisition “preparer” can create a requisition for another “requester.”</span></span> <span data-ttu-id="25cd6-106">Voit myös myöntää työntekijälle käyttöoikeudet kohteiden ja palveluiden tilaamiseen yhdessä tai useammassa yrityksessä tai toimintayksikössä.</span><span class="sxs-lookup"><span data-stu-id="25cd6-106">The procedure also shows how to grant a worker permission to order items and services in different legal entities or operating units.</span></span> <span data-ttu-id="25cd6-107">Ostopäällikkö tekee yleensä nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="25cd6-107">Typically, these tasks are performed by a purchasing manager.</span></span> <span data-ttu-id="25cd6-108">Voit käyttää tätä menettelyä joko USMF-demoyrityksen tiedoilla tai omilla tiedoillasi.</span><span class="sxs-lookup"><span data-stu-id="25cd6-108">You can use this procedure either on data for the USMF demo company or on your own data.</span></span>


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a><span data-ttu-id="25cd6-109">Myönnä käyttöoikeudet ostoehdotusten kirjoittamiseksi toisen työntekijän puolesta</span><span class="sxs-lookup"><span data-stu-id="25cd6-109">Grant permission to enter purchase requisitions on behalf of another worker</span></span>
1. <span data-ttu-id="25cd6-110">Siirry siirtymisruudussa kohtaan **Moduulit > Hankinta > Asetukset > Käytännöt > Ostoehdotuksen käyttöoikeudet**.</span><span class="sxs-lookup"><span data-stu-id="25cd6-110">In the navigation pane, go to **Modules > Procurement and sourcing > Setup > Policies > Purchase requisition permissions**.</span></span> <span data-ttu-id="25cd6-111">Varmista, että **Nykyinen näkymä** -kentän arvoksi on asetettu **Valmistelijan mukaan**.</span><span class="sxs-lookup"><span data-stu-id="25cd6-111">Make sure that the **Current view** field is set to **By preparer**.</span></span> <span data-ttu-id="25cd6-112">Vasemmassa ruudussa on luettelo henkilöistä, jotka voivat saada käyttöoikeuden valmistella ehdotuksia muiden käyttäjien puolesta.</span><span class="sxs-lookup"><span data-stu-id="25cd6-112">The list in the left pane shows the people who can be granted permission to prepare requisitions on behalf of other people.</span></span>  
2. <span data-ttu-id="25cd6-113">Valitse henkilö, jolle oikeudet myönnetään (valmistelija).</span><span class="sxs-lookup"><span data-stu-id="25cd6-113">Select the person to grant permission to (the preparer).</span></span>
3. <span data-ttu-id="25cd6-114">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="25cd6-114">Select **Add**.</span></span>
4. <span data-ttu-id="25cd6-115">Etsi ja lisää henkilö pyynnön lähettäjäksi.</span><span class="sxs-lookup"><span data-stu-id="25cd6-115">Find and select the person to add as a requester.</span></span>
    - <span data-ttu-id="25cd6-116">Ehdottaja on henkilö, jonka puolesta valmistelija voi luoda ostoehdotuksia.</span><span class="sxs-lookup"><span data-stu-id="25cd6-116">The requester is the person that the preparer can create requisitions on behalf of.</span></span>  
    - <span data-ttu-id="25cd6-117">Valitse **Valtuutus**-kentän arvoksi **Yksilöity**, jos valmistelija voi luoda ostoehdotuksia valitun työntekijän puolesta.</span><span class="sxs-lookup"><span data-stu-id="25cd6-117">In the **Authorization** field, select **Specific** if the preparer should be able to create purchase requisitions on behalf of the selected worker.</span></span> <span data-ttu-id="25cd6-118">Valitse arvoksi **Raportointi**, jos valmistelijan pitäisi myös luoda ostoehdotuksia kaikkien työntekijöiden puolesta, jotka raportoivat kyseiselle työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="25cd6-118">Select **Reporting** if the preparer should also be able to create purchase requisitions on behalf of all workers who report to that worker.</span></span>  
5. <span data-ttu-id="25cd6-119">Kirjoita päivämäärä **Voimassa**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="25cd6-119">In the **Effective** field, enter a date.</span></span>
6. <span data-ttu-id="25cd6-120">Syötä päivämäärä **Päättyminen**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="25cd6-120">In the **Expiration** field, enter a date.</span></span>

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a><span data-ttu-id="25cd6-121">Tarkastele valmistelijoita, joilla on oikeus luoda ostoehdotuksia valitulle työntekijälle</span><span class="sxs-lookup"><span data-stu-id="25cd6-121">View preparers who have permission to create purchase requisitions for a selected worker</span></span>
1. <span data-ttu-id="25cd6-122">Valitse **Nykyinen näkymä** -kentän arvoksi **Pyytäjän mukaan**.</span><span class="sxs-lookup"><span data-stu-id="25cd6-122">In the **Current view** field, select **By requester**.</span></span> <span data-ttu-id="25cd6-123">Tässä näkymässä on luettelo valmistelijoista joille on myönnetty oikeudet luoda ostoehdotuksia valitun työntekijän puolesta.</span><span class="sxs-lookup"><span data-stu-id="25cd6-123">This view shows a list of preparers who have been granted permission to create purchase requisitions on behalf of a selected worker.</span></span>  
2. <span data-ttu-id="25cd6-124">Etsi pyynnön lähettäjäksi lisäämäsi työntekijä pikasuodattimen avulla.</span><span class="sxs-lookup"><span data-stu-id="25cd6-124">Use the Quick Filter to find the worker that you just added as the requester.</span></span>
3. <span data-ttu-id="25cd6-125">Valitse pyynnön lähettäjä.</span><span class="sxs-lookup"><span data-stu-id="25cd6-125">Select the requester.</span></span> <span data-ttu-id="25cd6-126">Valmistelijaluettelossa ovat käyttäjät, joilla on oikeus tilata nimikkeitä vasemmassa ruudussa valitun pyynnön lähettäjän puolesta.</span><span class="sxs-lookup"><span data-stu-id="25cd6-126">The Preparer list shows the people who have permission to order items on behalf of the requester who is selected in the left pane.</span></span>  <span data-ttu-id="25cd6-127">Voit lisätä muita valmistelijoita tässä.</span><span class="sxs-lookup"><span data-stu-id="25cd6-127">You can add additional preparers here.</span></span> <span data-ttu-id="25cd6-128">Näkymän avulla voit myös antaa pyynnön lähettäjälle oikeuden luoda ostoehdotuksia yrityksissä toimintayksiköissä, jotka eivät ole tämän ensisijainen yritys tai toimintayksikkö.</span><span class="sxs-lookup"><span data-stu-id="25cd6-128">This view also lets you grant the requester permission to create requisitions in legal entities and operating units that aren't that person's primary legal entity or operating unit.</span></span>  

