---
title: Suoratoimitus ei voi käsitellä WMS-yhteensopivaa varastoa
description: Jos varastossa on WMS käytössä, se ei tue suoratoimitusta. Suoratoimituksen käyttämistä varten on valittava muu kuin varastonhallintanimike ja varasto.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 090e17091e9fb92c2065679bb9b04637214e2eea
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476280"
---
# <a name="direct-delivery-not-able-to-process-for-wms-enabled-warehouse"></a>Suoratoimitus ei voi käsitellä WMS-yhteensopivaa varastoa

## <a name="symptoms"></a>Oireet

Jos nimike lisätään myyntiriville suoratoimitusta varten varastosta, johon sovelletaan varastonhallintaa, saat seuraavan virhesanoman, kun myyntirivi päivitetään.

> Suoratoimitus ei voi käsitellä varastoa 1%, koska varastonhallinta on otettu siinä käyttöön. Määritä toinen varasto, jossa varastonhallintaa ei ole otettu käyttöön.

## <a name="resolution"></a>Ratkaisu

Microsoft on arvioinut ongelman ja määrittänyt, että se on ominaisuuden rajoitus. Varastonhallinta ei tue tällä hetkellä suoratoimitusta. Suoratoimituksen käyttämistä varten on sen vuoksi valittava muu kuin varastonhallintanimike ja varasto.
