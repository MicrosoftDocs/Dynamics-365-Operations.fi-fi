---
title: "Määritä tuoterakenneversio"
description: "Jos nimikkeen suunniteltuna oletustilaustyyppinä on kysynnän hajottamisen aikana Tuotanto, suunnitteluohjelma etsii kelvollisen tuoterakenneversion toimipaikan perusteella."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, InventItemOrderSetup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: ceeb82130a3ab214ef3e9eda09294c9bcc0c7cc0
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---

# <a name="determine-the-bom-version"></a><span data-ttu-id="14947-103">Määritä tuoterakenneversio</span><span class="sxs-lookup"><span data-stu-id="14947-103">Determine the BOM version</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="14947-104">Jos nimikkeen suunniteltuna oletustilaustyyppinä on kysynnän hajottamisen aikana Tuotanto, suunnitteluohjelma etsii kelvollisen tuoterakenneversion toimipaikan perusteella.</span><span class="sxs-lookup"><span data-stu-id="14947-104">During a demand explosion, if an item has a default order type of Production, the planning engine finds a valid BOM version based on the site.</span></span> 

<span data-ttu-id="14947-105">Toimipaikan dimensio on aina tiedossa. Se ilmoitetaan kysyntätapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="14947-105">The site dimension is always known and is stated on the demand transaction.</span></span> <span data-ttu-id="14947-106">Seuraavan prosessin avulla määritetään käytettävä tuoterakenneversio:</span><span class="sxs-lookup"><span data-stu-id="14947-106">The following process is used to determine the BOM version to use:</span></span>

-   <span data-ttu-id="14947-107">Jos nimikkeelle on määritetty tuoterakenneversio kysynnän toimipaikassa, käytössä on toimipaikkakohtainen tuoterakenne.</span><span class="sxs-lookup"><span data-stu-id="14947-107">If there is a BOM version defined for the item at the demand site, the site-specific BOM is used.</span></span>
-   <span data-ttu-id="14947-108">Jos nimikkeelle ei ole määritetty toimipaikkakohtaista tuoterakenneversiota kysynnän toimipaikassa, käytössä on yleinen tuoterakenne.</span><span class="sxs-lookup"><span data-stu-id="14947-108">If there is no site-specific BOM version defined for an item at the demand site, a general BOM is used.</span></span> <span data-ttu-id="14947-109">Yleinen tuoterakenne ei ilmaise toimipaikkaa, ja sitä voi käyttää useissa toimipaikoissa.</span><span class="sxs-lookup"><span data-stu-id="14947-109">A general BOM does not state a site, and it is valid for multiple sites.</span></span> <span data-ttu-id="14947-110">Jos yleinen tuoterakenne on käytettävissä, ohjelma käyttää sitä.</span><span class="sxs-lookup"><span data-stu-id="14947-110">If there is a general BOM, it is used.</span></span>
-   <span data-ttu-id="14947-111">Jos käytettävissä ei ole yleistä tuoterakenneversiota, kysynnän hajottaminen keskeytyy.</span><span class="sxs-lookup"><span data-stu-id="14947-111">If there is no general BOM version to use, the demand explosion stops at this point.</span></span>

<span data-ttu-id="14947-112">Kaikkien kelvollisten toimipaikkakohtaisten tai yleisten tuoterakenneversioiden on täytettävä tarvittavat päivämäärä- ja määräehdot.</span><span class="sxs-lookup"><span data-stu-id="14947-112">A valid BOM version, whether site-specific or general, must meet the required criteria for date and quantity.</span></span>






