---
title: Toiminnalliset sijainnit ja resurssit
description: Tässä ohjeaiheessa kerrotaan toiminnallisista sijainneista ja resursseista resurssien hallinnassa. Resurssien hallinta on kehittynyt moduuli resurssien ja kunnossapitotöiden hallintaan Dynamics 365 Supply Chain Managementissa.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3a42d36fd137aa780886276a4235f1b8f3a3680
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653344"
---
# <a name="functional-locations-and-assets"></a><span data-ttu-id="49e39-104">Toiminnalliset sijainnit ja resurssit</span><span class="sxs-lookup"><span data-stu-id="49e39-104">Functional locations and assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="49e39-105">Tässä ohjeaiheessa kerrotaan toiminnallisista sijainneista ja resursseista resurssien hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="49e39-105">This topic describes functional locations and assets in Asset Management.</span></span> <span data-ttu-id="49e39-106">Resurssien hallinta on kehittynyt moduuli resurssien ja kunnossapitotöiden hallintaan Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="49e39-106">Asset Management is an advanced module for managing assets and maintenance jobs in Dynamics 365 Supply Chain Management.</span></span>

## <a name="overview"></a><span data-ttu-id="49e39-107">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="49e39-107">Overview</span></span>

<span data-ttu-id="49e39-108">Resurssien hallinta on integroitu saumattomasti useisiin moduuleihin muiden Finance and Operations -sovellusten kanssa.</span><span class="sxs-lookup"><span data-stu-id="49e39-108">Asset Management is integrated seamlessly with several modules with other Finance and Operations apps.</span></span> <span data-ttu-id="49e39-109">Seuraavassa kuvassa näkyvät liittymät muiden moduulien kanssa.</span><span class="sxs-lookup"><span data-stu-id="49e39-109">The following illustration shows the interfaces with other modules.</span></span>

![Kaavio, jossa näkyvät resurssienhallinnan rajapinnat muihin moduuleihin](media/01-overview-image.png)

<span data-ttu-id="49e39-111">Resurssien hallinnan avulla voit tehokkaasti hallita ja suorittaa kaikkia tehtäviä, jotka liittyvät yrityksen monentyyppisten laitteiden hallintaan ja huoltoon.</span><span class="sxs-lookup"><span data-stu-id="49e39-111">Asset Management lets you efficiently manage and perform all tasks that are related to managing and servicing many types of equipment in your company.</span></span> <span data-ttu-id="49e39-112">Näihin laitteisiin kuuluvat koneet, tuotantolaitteet ja ajoneuvot.</span><span class="sxs-lookup"><span data-stu-id="49e39-112">This equipment includes machines, production equipment, and vehicles.</span></span> <span data-ttu-id="49e39-113">Resurssien hallinta tukee myös ratkaisuja monilla eri aloilla.</span><span class="sxs-lookup"><span data-stu-id="49e39-113">Asset Management also supports solutions across numerous industries.</span></span>

<span data-ttu-id="49e39-114">Seuraavassa kuvassa on yleiskuvaus päätoiminnoista, jotka kuuluvat resurssien hallintaan.</span><span class="sxs-lookup"><span data-stu-id="49e39-114">The following illustration shows an overview of the main functionality that is covered by Asset Management.</span></span>

![Kaavio, jossa näkyy resurssienhallinnan päätoiminto](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a><span data-ttu-id="49e39-116">Toiminnalliset sijainnit ja resurssit</span><span class="sxs-lookup"><span data-stu-id="49e39-116">Functional locations and assets</span></span>

<span data-ttu-id="49e39-117">Toiminnallisia sijainteja käytetään resurssien hallintaan sijainneissa.</span><span class="sxs-lookup"><span data-stu-id="49e39-117">Functional locations are used to manage assets on locations.</span></span> <span data-ttu-id="49e39-118">Tämä hallinta sisältää resurssien kustannusten seurannan toiminnallisissa sijainneissa.</span><span class="sxs-lookup"><span data-stu-id="49e39-118">This management includes tracking of asset costs on functional locations.</span></span> <span data-ttu-id="49e39-119">Toiminnalliset sijainnit on jäsennelty hierarkkisesti, ja sijainneissa voi olla alisijainteja.</span><span class="sxs-lookup"><span data-stu-id="49e39-119">Functional locations are structured hierarchically, and locations can have sub-locations.</span></span> <span data-ttu-id="49e39-120">Toiminnallisten sijaintien rakenne on staattinen.</span><span class="sxs-lookup"><span data-stu-id="49e39-120">The structure of functional locations is static.</span></span> <span data-ttu-id="49e39-121">Toisin sanoen sijainnit eivät voi muuttaa paikkaa.</span><span class="sxs-lookup"><span data-stu-id="49e39-121">In other words, locations can't change place.</span></span> <span data-ttu-id="49e39-122">Resurssit voidaan asentaa toiminnallisiin sijainteihin, ja ne voidaan tarvittaessa asentaa muihin toiminnallisiin sijainteihin myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="49e39-122">Assets can be installed on functional locations and, as required, can be installed on other functional locations later.</span></span>

<span data-ttu-id="49e39-123">Resurssien kustannukset noudattavat aina resurssin sijaintia.</span><span class="sxs-lookup"><span data-stu-id="49e39-123">Asset costs always follow the location of the asset.</span></span> <span data-ttu-id="49e39-124">Toisin sanoen, jos asennat resurssin uuteen toiminnalliseen sijaintiin, resurssi käyttää automaattisesti taloushallinnon dimensioita, jotka liittyvät uuteen toiminnalliseen sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="49e39-124">In other words, if you install an asset on a new functional location, the asset automatically uses the financial dimensions that are related to the new functional location.</span></span> <span data-ttu-id="49e39-125">Tämän vuoksi resurssien kustannukset liittyvät aina siihen toiminnalliseen sijaintiin, johon resurssi on tällä hetkellä asennettu.</span><span class="sxs-lookup"><span data-stu-id="49e39-125">Therefore, asset costs are always related to the functional location that the asset is  currently installed on.</span></span> <span data-ttu-id="49e39-126">Tämä taloushallinnon dimensioiden automaattinen käsittely auttaa takaamaan kustannusten täydellisen seurannan, kun yrityksesi tekee projektien hallinnan ja raportoinnin toiminnallisista sijainneista.</span><span class="sxs-lookup"><span data-stu-id="49e39-126">This automatic handling of financial dimensions helps guarantee complete tracking of costs when your company does project controlling and reporting on functional locations.</span></span>

<span data-ttu-id="49e39-127">Toiminnallisten sijaintien hierarkian koontitapa riippuu yrityksesi vaatimuksista, jotka koskevat sisäisten laitteiden ylläpitoa tai asiakaslaitteiden huoltoa.</span><span class="sxs-lookup"><span data-stu-id="49e39-127">The way that you build your hierarchy of functional locations depends on your company's requirements for maintaining internal equipment or servicing customer equipment.</span></span> <span data-ttu-id="49e39-128">Seuraavassa kuvassa on esimerkki toiminnallisista sijainneista, jotka perustuvat maantieteellisiin sijainteihin.</span><span class="sxs-lookup"><span data-stu-id="49e39-128">The following figure shows an example of functional locations that are based on geographical locations.</span></span>

![Kaavio, jossa näkyy toiminnallisia sijainteja maantieteellisten sijaintien perusteella](media/03-overview-image.png)

<span data-ttu-id="49e39-130">Seuraavassa kuvassa on esimerkki toiminnallisista sijainneista, jotka perustuvat asiakkaisiin.</span><span class="sxs-lookup"><span data-stu-id="49e39-130">The following figure shows an example of functional locations that are based on customers.</span></span>

![Kaavio, jossa näkyy toiminnallisia sijainteja asiakkaiden perusteella](media/04-overview-image.png)
