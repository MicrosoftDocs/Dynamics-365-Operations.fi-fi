---
title: Valmiiksi ilmoittaminen rekisterikilpiohjattuun sijaintiin työkorttilaitteelta
description: Tässä ohjeaiheessa käsitellään valmiiden tuotteiden viimeistelyprosessia, kun rekisterikilpi ohjaa sijaintia.
author: johanhoffmann
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: cb809e596fd6bf3030bcee460838798435512b95
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572126"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="38562-103">Valmiiksi ilmoittaminen rekisterikilpiohjattuun sijaintiin työkorttilaitteelta</span><span class="sxs-lookup"><span data-stu-id="38562-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="38562-104">Valmiiksi ilmoittamiseksi kutsuttu prosessi viimeistelee tuotantotilauksen valmiit tuotteet varastoon.</span><span class="sxs-lookup"><span data-stu-id="38562-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="38562-105">Jos valmis tuote on otettu käyttöön edistyksellisiä varastoprosesseja varten, se ilmoitetaan valmiiksi tuotannon tuotossijainniksi kutsuttuun sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="38562-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="38562-106">Lisätietoja tuotannon tuotossijainnin määrittämisestä on kohdassa [Tuotannon tuotossijainti](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location)</span><span class="sxs-lookup"><span data-stu-id="38562-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="38562-107">Sinun täytyy valita olemassa oleva rekisterinumero suorittaaksesi tehtävän.</span><span class="sxs-lookup"><span data-stu-id="38562-107">You must select an existing license plate number to complete this task.</span></span> <span data-ttu-id="38562-108">Jos tuotannon tuotossijainti on määritetty rekisterikilvellä seurattavaksi, rekisterinumero on sisällytettävä mukaan, kun tuotannon tuotossijainti ilmoitetaan valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="38562-108">If the production output location is set up to be tracked by license plate, then a license plate number must be included when reporting the production output location as finished.</span></span> <span data-ttu-id="38562-109">**Rekisterikilpi**-kenttä näytetään **Raportointi on meneillään** -kehotteessa **Työkorttilaite**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="38562-109">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="38562-110">Kenttä näytetään **Raportointi on meneillään** -kehotteessa vain, kun raportointia suoritetaan tuotantotilauksen viimeiselle toiminnolle.</span><span class="sxs-lookup"><span data-stu-id="38562-110">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order.</span></span> <span data-ttu-id="38562-111">Kenttä näytetään vain, jos tuotantotilauksen nimike on otettu käyttöön varastonhallintaprosessia varten.</span><span class="sxs-lookup"><span data-stu-id="38562-111">The field is only shown if the item for the production order is enabled for the warehouse management processes.</span></span> 
