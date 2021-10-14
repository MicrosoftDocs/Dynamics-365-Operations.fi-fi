---
title: Tavaralähetysvaraston valvonta toimittajayhteistyön avulla
description: Tässä menettelyssä kuvataan, miten toimittajanyhteistyötä voi käyttää asiakkaan tavaralähetykseen asetetun tuotteen varastotasotietojen tarkasteluun.
author: yufeihuang
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0d194728805cd1eee741069538352b497867981
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571830"
---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a>Tavaralähetysvaraston valvonta toimittajayhteistyön avulla

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä kuvataan, miten toimittajanyhteistyötä voi käyttää asiakkaan tavaralähetykseen asetetun tuotteen varastotasotietojen tarkasteluun. Voit seurata varaston kulutusta, kun varaston omistajuuden siirtyy asiakkaalle. Voit käyttää tätä menettelyä USMF:n esittely-yrityksessä. Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.


## <a name="view-consumed-inventory"></a>Näytä käytetty varasto
1. Siirry kohtaan Toimittajayhteistyö > Tavaralähetysvarasto > Tavaralähetysvarastosta vastaanotetut tuotteet.
    * Luettelossa on tuotteen vastaanottorivit, jotka luotiin kun tavaranlähetysvaraston omistajuus muutettiin toimittajalta asiakkaalle. Joudut ehkä vierittämään näyttöä oikealle nähdäksesi määrät ja muut tiedot. Voit käyttää luettelon tietoja laskujen luonnissa asiakkaalle. Voit viedä tiedot myös Microsoft Exceliin.   
2. Valitse Näytä ostotilausrivit.
3. Laajenna Rivin erittely -osa.
    * Rivi on merkitty tavaralähetykseksi ja otsikko-osa näyttä, että ostotilauksen tila on Vastaanotettu.  
4. Sulje sivu.

## <a name="view-on-hand-inventory"></a>Näytetään käytettävissä oleva varasto
1. Siirry kohtaan Toimittajayhteistyö > Tavaralähetysvarasto > Käytettävissä oleva tavaralähetysvarasto.
    * Käytettävissä oleva tavaralähetysvarasto -sivulla näytetään asiakkaan varastossa omistamasi varasto. Voit näyttää muita dimensioita, kuten toimipaikan ja varaston, valitsemalla Näytä dimensiot -välilehden.   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]