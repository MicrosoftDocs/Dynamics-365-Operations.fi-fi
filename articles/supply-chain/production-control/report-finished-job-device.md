---
title: Valmiiksi ilmoittaminen rekisterikilpiohjattuun sijaintiin työkorttilaitteelta
description: Tässä ohjeaiheessa käsitellään valmiiden tuotteiden viimeistelyprosessia, kun rekisterikilpi ohjaa sijaintia.
author: johanhoffmann
manager: AnnBe
ms.date: 01/06/2020
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
ms.openlocfilehash: 5f61c1abfb115f02e6ff314f6a3e42bb1d3b543f
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092565"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="af0a8-103">Valmiiksi ilmoittaminen rekisterikilpiohjattuun sijaintiin työkorttilaitteelta</span><span class="sxs-lookup"><span data-stu-id="af0a8-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="af0a8-104">Valmiiksi ilmoittamiseksi kutsuttu prosessi viimeistelee tuotantotilauksen valmiit tuotteet varastoon.</span><span class="sxs-lookup"><span data-stu-id="af0a8-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="af0a8-105">Jos valmis tuote on otettu käyttöön edistyksellisiä varastoprosesseja varten, se ilmoitetaan valmiiksi tuotannon tuotossijainniksi kutsuttuun sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="af0a8-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="af0a8-106">Lisätietoja tuotannon tuotossijainnin määrittämisestä on kohdassa [Tuotannon tuotossijainti](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location)</span><span class="sxs-lookup"><span data-stu-id="af0a8-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="af0a8-107">Jos tuotannon tuotossijainti on rekisterikilpiohjattu, niin rekisterikilpi on annettava, kun raportoidaan valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="af0a8-107">If the production output location is license plate controlled, then a license plate must be provided when reporting as finished.</span></span> <span data-ttu-id="af0a8-108">**Rekisterikilpi**-kenttä näytetään **Raportointi on meneillään** -kehotteessa **Työkorttilaite**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="af0a8-108">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="af0a8-109">Kenttä näkyy vain **Raportin edistyminen** -kehotteessa, kun tuotantotilauksen viimeinen työvaihe raportoidaan ja tuotantotilauksen nimike on otettu käyttöön varastonhallintaprosesseille.</span><span class="sxs-lookup"><span data-stu-id="af0a8-109">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order and the item for the production order is enabled for the warehouse management processes.</span></span> 

<span data-ttu-id="af0a8-110">Rekisterikilven tarjoamiseen on kaksi vaihtoehtoa</span><span class="sxs-lookup"><span data-stu-id="af0a8-110">There are two options for providing the license plate</span></span>
- <span data-ttu-id="af0a8-111">Käyttäjä valitsee olemassa olevan rekisterikilven rekisterikilpikentässä.</span><span class="sxs-lookup"><span data-stu-id="af0a8-111">The user is selecting an existing license plate in the license plate field.</span></span>
- <span data-ttu-id="af0a8-112">Rekisterikilpi luodaan automaattisesti numerosarjasta, ja se on oletusarvoisesti rekisterikilpikentässä.</span><span class="sxs-lookup"><span data-stu-id="af0a8-112">The license plate is automatically generated from a number sequence and defaulted to the license plate field.</span></span>

<span data-ttu-id="af0a8-113">Vaihtoehto, jonka mukaan rekisterikilpi luodaan automaattisesti, määritetään valitsemalla vaihtoehto **Luo rekisterikilpi** **Määritä työkortti laitteille** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="af0a8-113">The option to have the license plate generated automatically is configured by selecting the option **Generate license plate** on the **Configure job card for devices** page.</span></span>
