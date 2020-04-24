---
title: Tuotannon tuotossijainti
description: Tässä ohjeaiheessa käsitellään hierarkiaa, jolla tuotannon tuotossijainti tunnistetaan.
author: johanhoffmann
manager: tfehr
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e4002bf7dddb196edf306268ecc16e1bfa5d6d1e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211304"
---
# <a name="production-output-location"></a><span data-ttu-id="3d6f2-103">Tuotannon tuotossijainti</span><span class="sxs-lookup"><span data-stu-id="3d6f2-103">Production output location</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d6f2-104">Tässä ohjeaiheessa käsitellään hierarkiaa, jolla tuotannon tuotossijainti tunnistetaan.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-104">This topic describes the hierarchy that is used to identify the production output location.</span></span>

<span data-ttu-id="3d6f2-105">Tuotannon tuotossijainti on sijainti, jossa valmista tavaraa säilytetään heti valmistuksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-105">The production output location is the location where a finished good is first stored after it's produced.</span></span> <span data-ttu-id="3d6f2-106">Yleensä tämä sijainti on valmiin tavaran tuottavan tuotantoprosessin lähellä.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-106">Usually, this location is close to the production process that produces the finished good.</span></span> <span data-ttu-id="3d6f2-107">Tuotannon tuotossijaintia käytetään materiaalin välivarastona, ennen kuin se esimerkiksi siirretään lähetysalueelle, varastosijaintiin, tuotantovirran tuotantoprosessin tuotannon tuotossijaintiin.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-107">The production output location is used as intermediate storage for the material before it's moved on to the shipment area, a storage location, a production input location for a downstream production process, and so on.</span></span> 

<span data-ttu-id="3d6f2-108">Tuotannon oletustuotossijainti määritetään, kun valmiit tuotteet ilmoitetaan tuotantotilauksessa tai erätilauksessa.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-108">A default production output location is set when finished goods are reported on a production order or batch order.</span></span> <span data-ttu-id="3d6f2-109">Tämä tuotossijainti ilmoitetaan seuraavan hierarkian avulla:</span><span class="sxs-lookup"><span data-stu-id="3d6f2-109">The following hierarchy is used to identify this output location:</span></span>

1. <span data-ttu-id="3d6f2-110">Käytä tuotanto- tai erätilauksen otsikossa määritettyä tuotossijaintia.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-110">Use the output location that is defined on the production order or batch order header.</span></span>
2. <span data-ttu-id="3d6f2-111">Jos sijainti ei ole siellä, käytä siinä resurssissa määritettyä tuotossijaintia, jota tuotantoreitissä määritetty viimeisin toiminto käyttää.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-111">If no location is found there, use the output location that is defined on the resource that is used by the last operation that is defined in the production route.</span></span>
3. <span data-ttu-id="3d6f2-112">Jos sijainti ei ole siellä, käytä siinä resurssiryhmässä määritettyä tuotossijaintia, jota tuotantoreitissä määritetyn viimeisimmän toiminnon resurssi käyttää.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-112">If no location is found there, use the output location that is defined on the resource group that is used by the resource for the last operation that is defined in the production route.</span></span>
4. <span data-ttu-id="3d6f2-113">Jos sijainti ei ole siellä, käytä sitä tuotossijaintia, joka on määritetty tuotantotilaukselle määritetyssä varastossa.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-113">If no location is found there, use the output location that is defined on the warehouse that is defined for the production order.</span></span>

<span data-ttu-id="3d6f2-114">Tuotannon oletustuotossijainti määritetään vain tuotteille, jotka on määritetty edistyksellisellä varastoprosessilla.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-114">A default production output location is set only for products that are set up by using advanced warehouse processes.</span></span> <span data-ttu-id="3d6f2-115">Kun tämän tyyppinen nimike määritetään valmiiksi, **Valmiiden tuotteiden poispano**- tai **Rinnakkaistuotteen ja sivutuotteen poispano** -tyyppinen varastotyö luodaan.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-115">When this type of item is reported as finished, warehouse work of the **Finished goods put away** or **Co-product and by-product put away** type is created.</span></span> <span data-ttu-id="3d6f2-116">Tämän tyyppinen työ käyttää tuotannon tuotossijaintia keräyssijaintia.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-116">This type of work uses the production output location as the pick location.</span></span> <span data-ttu-id="3d6f2-117">Sijaintidirektiivi määrittää poispanosijainnin.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-117">The put-away location is determined by the location directives.</span></span>
