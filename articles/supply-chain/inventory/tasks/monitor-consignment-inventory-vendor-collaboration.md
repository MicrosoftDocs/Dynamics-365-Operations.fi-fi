---
title: "Tavaralähetysvaraston valvonta toimittajayhteistyön avulla"
description: "Tässä menettelyssä kuvataan, miten toimittajanyhteistyötä voi käyttää asiakkaan tavaralähetykseen asetetun tuotteen varastotasotietojen tarkasteluun."
author: mkirknel
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 567be29bd9989b3471b22d5a970ed0e51e4549ec
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a>Tavaralähetysvaraston valvonta toimittajayhteistyön avulla

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä kuvataan, miten toimittajanyhteistyötä voi käyttää asiakkaan tavaralähetykseen asetetun tuotteen varastotasotietojen tarkasteluun. Voit seurata varaston kulutusta, kun varaston omistajuuden siirtyy asiakkaalle. Voit käyttää tätä menettelyä USMF:n esittely-yrityksessä. Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.


## <a name="view-consumed-inventory"></a>Näytä käytetty varasto
1. Siirry kohtaan Toimittajayhteistyö > Tavaralähetysvarasto > Tavaralähetysvarastosta vastaanotetut tuotteet.
    * Luettelossa on tuotteen vastaanottorivit, jotka luotiin kun tavaranlähetysvaraston omistajuus muutettiin toimittajalta asiakkaalle. Joudut ehkä vierittämään näyttöä oikealle nähdäksesi määrät ja muut tiedot. Voit käyttää luettelon tietoja laskujen luonnissa asiakkaalle. Voit myös viedä tiedot Microsoft Exceliin.   
2. Valitse Näytä ostotilausrivit.
3. Laajenna Rivin erittely -osa.
    * Rivi on merkitty tavaralähetykseksi ja otsikko-osa näyttä, että ostotilauksen tila on Vastaanotettu.  
4. Sulje sivu.

## <a name="view-on-hand-inventory"></a>Näytetään käytettävissä oleva varasto
1. Siirry kohtaan Toimittajayhteistyö > Tavaralähetysvarasto > Käytettävissä oleva tavaralähetysvarasto.
    * Käytettävissä oleva tavaralähetysvarasto -sivulla näytetään asiakkaan varastossa omistamasi varasto. Voit näyttää muita dimensioita, kuten toimipaikan ja varaston, valitsemalla Näytä dimensiot -välilehden.   

