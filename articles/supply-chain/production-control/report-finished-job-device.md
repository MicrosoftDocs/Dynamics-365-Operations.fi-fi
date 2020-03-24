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

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>Valmiiksi ilmoittaminen rekisterikilpiohjattuun sijaintiin työkorttilaitteelta 

Valmiiksi ilmoittamiseksi kutsuttu prosessi viimeistelee tuotantotilauksen valmiit tuotteet varastoon. Jos valmis tuote on otettu käyttöön edistyksellisiä varastoprosesseja varten, se ilmoitetaan valmiiksi tuotannon tuotossijainniksi kutsuttuun sijaintiin. Lisätietoja tuotannon tuotossijainnin määrittämisestä on kohdassa [Tuotannon tuotossijainti](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location)

Jos tuotannon tuotossijainti on rekisterikilpiohjattu, niin rekisterikilpi on annettava, kun raportoidaan valmiiksi. **Rekisterikilpi**-kenttä näytetään **Raportointi on meneillään** -kehotteessa **Työkorttilaite**-sivulla. Kenttä näkyy vain **Raportin edistyminen** -kehotteessa, kun tuotantotilauksen viimeinen työvaihe raportoidaan ja tuotantotilauksen nimike on otettu käyttöön varastonhallintaprosesseille. 

Rekisterikilven tarjoamiseen on kaksi vaihtoehtoa
- Käyttäjä valitsee olemassa olevan rekisterikilven rekisterikilpikentässä.
- Rekisterikilpi luodaan automaattisesti numerosarjasta, ja se on oletusarvoisesti rekisterikilpikentässä.

Vaihtoehto, jonka mukaan rekisterikilpi luodaan automaattisesti, määritetään valitsemalla vaihtoehto **Luo rekisterikilpi** **Määritä työkortti laitteille** -sivulla.
