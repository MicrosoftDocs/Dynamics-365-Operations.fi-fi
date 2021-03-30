---
title: Julkaistun päätuotteen perusmääritysten päättäminen
description: Tässä aiheessa selvitetään, mitkä asetukset on ainakin määritettävä, ennen kuin päätuotetta voi käyttää tuoterakenneversioissa.
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8c6de9fa9dd49cc32f87a6041a3639198db9f182
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218606"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="ba157-103">Julkaistun päätuotteen perusmääritysten päättäminen</span><span class="sxs-lookup"><span data-stu-id="ba157-103">Complete basic setup of a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ba157-104">Tässä aiheessa selvitetään, mitkä asetukset on ainakin määritettävä, ennen kuin päätuotetta voi käyttää tuoterakenneversioissa.</span><span class="sxs-lookup"><span data-stu-id="ba157-104">This topic shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="ba157-105">Tämä on kolmas kahdeksasta menettelystä, joissa selitetään, miten dimensioihin perustuvia konfiguraatioyhdistelmiä luodaan.</span><span class="sxs-lookup"><span data-stu-id="ba157-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="ba157-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="ba157-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="ba157-107">Valitse **Siirtymisruutu > Moduulit > Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="ba157-107">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="ba157-108">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ba157-108">In the list, find and select the desired record.</span></span> <span data-ttu-id="ba157-109">Valitse toisessa menettelyssä vapautettu päätuote.</span><span class="sxs-lookup"><span data-stu-id="ba157-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="ba157-110">Tämä päätuote on luotu dimensioihin perustuvalla konfiguraatiomenetelmällä.</span><span class="sxs-lookup"><span data-stu-id="ba157-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="ba157-111">Valitse toimintoruudussa **Tuote**.</span><span class="sxs-lookup"><span data-stu-id="ba157-111">On the Action Pane, select **Product**.</span></span>
4. <span data-ttu-id="ba157-112">Avaa valintaikkunalomake valitsemalla **Dimensioryhmät**.</span><span class="sxs-lookup"><span data-stu-id="ba157-112">Select **Dimension groups** to open the drop dialog.</span></span>
5. <span data-ttu-id="ba157-113">Avaa haku valitsemalla **Varastodimensioryhmä**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="ba157-113">In the **Storage dimension group** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ba157-114">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ba157-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="ba157-115">Varastodimensioryhmä määrittää, mitä varastodimensioita käytetään tuotetapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="ba157-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="ba157-116">Valitse **Toimipaikka** tässä menettelyssä.</span><span class="sxs-lookup"><span data-stu-id="ba157-116">Select **Site** for this procedure.</span></span>  
7. <span data-ttu-id="ba157-117">Avaa haku valitsemalla **Seurantadimensioryhmä**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="ba157-117">In the **Tracking dimension group** field, select the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="ba157-118">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ba157-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="ba157-119">Seurantadimensioryhmä määrittää, mitä seurantadimensioita käytetään tuotetapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="ba157-119">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="ba157-120">Valitse tässä menettelyssä **Ei mitään**.</span><span class="sxs-lookup"><span data-stu-id="ba157-120">Select **None** for this procedure.</span></span>  
9. <span data-ttu-id="ba157-121">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="ba157-121">Click **OK**.</span></span>
10. <span data-ttu-id="ba157-122">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="ba157-122">Click **Edit**.</span></span>
11. <span data-ttu-id="ba157-123">Avaa haku valitsemalla **Nimikemalliryhmä**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="ba157-123">In the **Item model group** field, select the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="ba157-124">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ba157-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="ba157-125">Nimikemalliryhmien sisältämät asetukset määrittävät, kuinka nimikkeitä hallitaan ja käsitellään nimikkeiden vastaanotoissa ja varasto-otoissa.</span><span class="sxs-lookup"><span data-stu-id="ba157-125">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="ba157-126">Ne määrittävät myös, millä tavalla nimikkeiden kulutus lasketaan.</span><span class="sxs-lookup"><span data-stu-id="ba157-126">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="ba157-127">Valitse tähän menettelyyn **FIFO**.</span><span class="sxs-lookup"><span data-stu-id="ba157-127">Select **FIFO** for this procedure.</span></span>  
13. <span data-ttu-id="ba157-128">Laajenna **Kustannusten hallinta** -osa.</span><span class="sxs-lookup"><span data-stu-id="ba157-128">Expand the **Manage costs** section.</span></span>
14. <span data-ttu-id="ba157-129">Avaa haku valitsemalla **Nimikeryhmä**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="ba157-129">In the **Item group** field, select the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="ba157-130">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ba157-130">In the list, find and select the desired record.</span></span> <span data-ttu-id="ba157-131">Nimikeryhmiä käytetään varaston hallintaan jakamalla varastonimikkeet ryhmiin.</span><span class="sxs-lookup"><span data-stu-id="ba157-131">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="ba157-132">Valitse **CarAudio** tähän menettelyyn.</span><span class="sxs-lookup"><span data-stu-id="ba157-132">Select **CarAudio** for this procedure.</span></span>  
16. <span data-ttu-id="ba157-133">Valitse toimintoruudussa **Suunnitelma**.</span><span class="sxs-lookup"><span data-stu-id="ba157-133">On the Action Pane, select **Plan**.</span></span>
17. <span data-ttu-id="ba157-134">Valitse **Tilauksen oletusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="ba157-134">Select **Default order settings**.</span></span>
18. <span data-ttu-id="ba157-135">Valitse **Oletusarvoinen tilaustyyppi** -kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="ba157-135">In the **Default order type field**, select an option.</span></span> <span data-ttu-id="ba157-136">Valitsemalla **Tuotanto** voit määrittää, että tämän päätuotteen oletustoimitusvalinta on sen tuottaminen.</span><span class="sxs-lookup"><span data-stu-id="ba157-136">Select **Production** to specify that the default supply option for this product master is to produce it.</span></span>  
19. <span data-ttu-id="ba157-137">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ba157-137">Select **Save**.</span></span>
20. <span data-ttu-id="ba157-138">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ba157-138">Close the page.</span></span>
21. <span data-ttu-id="ba157-139">Sulje **Vapautetun tuotteen tiedot** -lomake.</span><span class="sxs-lookup"><span data-stu-id="ba157-139">Close the **Released product details** form.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]