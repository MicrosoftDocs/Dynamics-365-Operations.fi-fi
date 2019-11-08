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

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>Valmiiksi ilmoittaminen rekisterikilpiohjattuun sijaintiin työkorttilaitteelta 

Valmiiksi ilmoittamiseksi kutsuttu prosessi viimeistelee tuotantotilauksen valmiit tuotteet varastoon. Jos valmis tuote on otettu käyttöön edistyksellisiä varastoprosesseja varten, se ilmoitetaan valmiiksi tuotannon tuotossijainniksi kutsuttuun sijaintiin. Lisätietoja tuotannon tuotossijainnin määrittämisestä on kohdassa [Tuotannon tuotossijainti](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location)

Sinun täytyy valita olemassa oleva rekisterinumero suorittaaksesi tehtävän. Jos tuotannon tuotossijainti on määritetty rekisterikilvellä seurattavaksi, rekisterinumero on sisällytettävä mukaan, kun tuotannon tuotossijainti ilmoitetaan valmiiksi. **Rekisterikilpi**-kenttä näytetään **Raportointi on meneillään** -kehotteessa **Työkorttilaite**-sivulla. Kenttä näytetään **Raportointi on meneillään** -kehotteessa vain, kun raportointia suoritetaan tuotantotilauksen viimeiselle toiminnolle. Kenttä näytetään vain, jos tuotantotilauksen nimike on otettu käyttöön varastonhallintaprosessia varten. 
