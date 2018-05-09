--- 
title: "Julkaistun päätuotteen perusmääritysten päättäminen"
description: "Tässä menettelyssä selvitetään, mitkä asetukset on ainakin määritettävä, ennen kuin päätuotetta voi käyttää tuoterakenneversioissa."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 35ca13f157537087346a5bcf9c6ccdd659a0d772
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="361a7-103">Julkaistun päätuotteen perusmääritysten päättäminen</span><span class="sxs-lookup"><span data-stu-id="361a7-103">Complete basic setup of a released product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="361a7-104">Tässä menettelyssä selvitetään, mitkä asetukset on ainakin määritettävä, ennen kuin päätuotetta voi käyttää tuoterakenneversioissa.</span><span class="sxs-lookup"><span data-stu-id="361a7-104">This procedure shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="361a7-105">Tämä on kolmas kahdeksasta menettelystä, joissa selitetään, miten dimensioihin perustuvia konfiguraatioyhdistelmiä luodaan.</span><span class="sxs-lookup"><span data-stu-id="361a7-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="361a7-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="361a7-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="361a7-107">Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="361a7-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="361a7-108">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="361a7-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="361a7-109">Valitse toisessa menettelyssä vapautettu päätuote.</span><span class="sxs-lookup"><span data-stu-id="361a7-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="361a7-110">Tämä päätuote on luotu dimensioihin perustuvalla konfiguraatiomenetelmällä.</span><span class="sxs-lookup"><span data-stu-id="361a7-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="361a7-111">Valitse toimintoruudussa Tuote.</span><span class="sxs-lookup"><span data-stu-id="361a7-111">On the Action Pane, click Product.</span></span>
4. <span data-ttu-id="361a7-112">Avaa valintaikkunalomake valitsemalla Dimensioryhmät.</span><span class="sxs-lookup"><span data-stu-id="361a7-112">Click Dimension groups to open the drop dialog.</span></span>
5. <span data-ttu-id="361a7-113">Avaa haku valitsemalla Varastodimensioryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="361a7-113">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="361a7-114">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="361a7-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="361a7-115">Varastodimensioryhmä määrittää, mitä varastodimensioita käytetään tuotetapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="361a7-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="361a7-116">Valitse Toimipaikka tässä menettelyssä.</span><span class="sxs-lookup"><span data-stu-id="361a7-116">Select Site for this procedure.</span></span>  
7. <span data-ttu-id="361a7-117">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="361a7-117">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="361a7-118">Avaa haku valitsemalla Seurantadimensioryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="361a7-118">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="361a7-119">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="361a7-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="361a7-120">Seurantadimensioryhmä määrittää, mitä seurantadimensioita käytetään tuotetapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="361a7-120">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="361a7-121">Valitse tässä menettelyssä Ei mitään.</span><span class="sxs-lookup"><span data-stu-id="361a7-121">Select None for this procedure.</span></span>  
10. <span data-ttu-id="361a7-122">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="361a7-122">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="361a7-123">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="361a7-123">Click OK.</span></span>
12. <span data-ttu-id="361a7-124">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="361a7-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="361a7-125">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="361a7-125">Click Edit.</span></span>
    * <span data-ttu-id="361a7-126">Jatka asennustehtävää avaamalla vapautetun tuotteen tietolomake.</span><span class="sxs-lookup"><span data-stu-id="361a7-126">Open the Released product details form to continue the setup task.</span></span>  
14. <span data-ttu-id="361a7-127">Avaa haku valitsemalla Nimikemalliryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="361a7-127">In the Item model group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="361a7-128">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="361a7-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="361a7-129">Nimikemalliryhmien sisältämät asetukset määrittävät, kuinka nimikkeitä hallitaan ja käsitellään nimikkeiden vastaanotoissa ja varasto-otoissa.</span><span class="sxs-lookup"><span data-stu-id="361a7-129">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="361a7-130">Ne määrittävät myös, millä tavalla nimikkeiden kulutus lasketaan.</span><span class="sxs-lookup"><span data-stu-id="361a7-130">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="361a7-131">Valitse tähän menettelyyn FIFO.</span><span class="sxs-lookup"><span data-stu-id="361a7-131">Select   FIFO for this procedure.</span></span>  
16. <span data-ttu-id="361a7-132">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="361a7-132">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="361a7-133">Laajenna tai tiivistä Kustannusten hallinta -osa.</span><span class="sxs-lookup"><span data-stu-id="361a7-133">Expand or collapse the Manage costs section.</span></span>
18. <span data-ttu-id="361a7-134">Avaa haku valitsemalla Nimikeryhmä-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="361a7-134">In the Item group field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="361a7-135">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="361a7-135">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="361a7-136">Nimikeryhmiä käytetään varaston hallintaan jakamalla varastonimikkeet ryhmiin.</span><span class="sxs-lookup"><span data-stu-id="361a7-136">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="361a7-137">Valitse CarAudio tähän menettelyyn.</span><span class="sxs-lookup"><span data-stu-id="361a7-137">Select   CarAudio for this procedure.</span></span>  
20. <span data-ttu-id="361a7-138">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="361a7-138">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="361a7-139">Valitse toimintoruudussa Suunnitelma.</span><span class="sxs-lookup"><span data-stu-id="361a7-139">On the Action Pane, click Plan.</span></span>
22. <span data-ttu-id="361a7-140">Valitse Tilauksen oletusasetukset.</span><span class="sxs-lookup"><span data-stu-id="361a7-140">Click Default order settings.</span></span>
23. <span data-ttu-id="361a7-141">Valitse Oletusarvoinen tilaustyyppi -kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="361a7-141">In the Default order type field, select an option.</span></span>
    * <span data-ttu-id="361a7-142">Valitsemalla Tuotanto voit määrittää, että tämän päätuotteen oletustoimitusvalinta on sen tuottaminen.</span><span class="sxs-lookup"><span data-stu-id="361a7-142">Select Production to specify that the default supply option for this product master is to produce it.</span></span>  
24. <span data-ttu-id="361a7-143">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="361a7-143">Close the page.</span></span>
25. <span data-ttu-id="361a7-144">Sulje Vapautetun tuotteen tiedot -lomake.</span><span class="sxs-lookup"><span data-stu-id="361a7-144">Close the Released product details form.</span></span>


