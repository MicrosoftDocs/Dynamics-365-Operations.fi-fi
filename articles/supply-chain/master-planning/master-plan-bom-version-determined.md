---
title: Määritä tuoterakenneversio
description: Jos nimikkeen suunniteltuna oletustilaustyyppinä on kysynnän hajottamisen aikana Tuotanto, suunnitteluohjelma etsii kelvollisen tuoterakenneversion toimipaikan perusteella.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 766c857cca603f84bb7fcef2c7eea3bc76620c19
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427312"
---
# <a name="determine-the-bom-version"></a><span data-ttu-id="8dea4-103">Määritä tuoterakenneversio</span><span class="sxs-lookup"><span data-stu-id="8dea4-103">Determine the BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8dea4-104">Jos nimikkeen suunniteltuna oletustilaustyyppinä on kysynnän hajottamisen aikana Tuotanto, suunnitteluohjelma etsii kelvollisen tuoterakenneversion toimipaikan perusteella.</span><span class="sxs-lookup"><span data-stu-id="8dea4-104">During a demand explosion, if an item has a default order type of Production, the planning engine finds a valid BOM version based on the site.</span></span> 

<span data-ttu-id="8dea4-105">Toimipaikan dimensio on aina tiedossa. Se ilmoitetaan kysyntätapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="8dea4-105">The site dimension is always known and is stated on the demand transaction.</span></span> <span data-ttu-id="8dea4-106">Seuraavan prosessin avulla määritetään käytettävä tuoterakenneversio:</span><span class="sxs-lookup"><span data-stu-id="8dea4-106">The following process is used to determine the BOM version to use:</span></span>

-   <span data-ttu-id="8dea4-107">Jos nimikkeelle on määritetty tuoterakenneversio kysynnän toimipaikassa, käytössä on toimipaikkakohtainen tuoterakenne.</span><span class="sxs-lookup"><span data-stu-id="8dea4-107">If there is a BOM version defined for the item at the demand site, the site-specific BOM is used.</span></span>
-   <span data-ttu-id="8dea4-108">Jos nimikkeelle ei ole määritetty toimipaikkakohtaista tuoterakenneversiota kysynnän toimipaikassa, käytössä on yleinen tuoterakenne.</span><span class="sxs-lookup"><span data-stu-id="8dea4-108">If there is no site-specific BOM version defined for an item at the demand site, a general BOM is used.</span></span> <span data-ttu-id="8dea4-109">Yleinen tuoterakenne ei ilmaise toimipaikkaa, ja sitä voi käyttää useissa toimipaikoissa.</span><span class="sxs-lookup"><span data-stu-id="8dea4-109">A general BOM does not state a site, and it is valid for multiple sites.</span></span> <span data-ttu-id="8dea4-110">Jos yleinen tuoterakenne on käytettävissä, ohjelma käyttää sitä.</span><span class="sxs-lookup"><span data-stu-id="8dea4-110">If there is a general BOM, it is used.</span></span>
-   <span data-ttu-id="8dea4-111">Jos käytettävissä ei ole yleistä tuoterakenneversiota, kysynnän hajottaminen keskeytyy.</span><span class="sxs-lookup"><span data-stu-id="8dea4-111">If there is no general BOM version to use, the demand explosion stops at this point.</span></span>

<span data-ttu-id="8dea4-112">Kaikkien kelvollisten toimipaikkakohtaisten tai yleisten tuoterakenneversioiden on täytettävä tarvittavat päivämäärä- ja määräehdot.</span><span class="sxs-lookup"><span data-stu-id="8dea4-112">A valid BOM version, whether site-specific or general, must meet the required criteria for date and quantity.</span></span>





