---
title: Varaston omistaja ei ole sallittu siirtoja käsiteltäessä
description: Virhe "Varaston omistaja %1 ei ole sallittu" saattaa ilmetä. Varastonhallintaprosessit tukevat vain varastoa, jonka omistaja on yritys.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4ee29cfc7bad990cd1ee5deaa98fca217af772ed
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476204"
---
# <a name="inventory-owner-not-allowed-when-processing-movements-in-the-warehouse-app"></a>Varaston omistaja ei saa osallistua varastosovelluksen siirtojen käsittelyyn

## <a name="symptoms"></a>Oireet

Kun käsittelet siirtoja Warehouse Managementin mobiilisovelluksessa, seuraava virhesanoma saattaa avautua:

> Varaston omistaja %1 ei ole sallittu tässä prosessissa.

## <a name="cause"></a>Syy

Tämä tapahtuu, koska **Omistaja** seurantadimensio puuttuu, kun Warehouse Managementin mobiilisovellusta käytetään siirtojen tekemiseen. Supply Chain Management -asiakasohjelman säännöllinen varastosiirtokirjauskansio näyttää toimivan odotetusti ja voidaan kirjat vain, jos **Omistaja**-dimensio on täytetty.

## <a name="resolution"></a>Ratkaisu

Microsoft on arvioinut ongelman ja määrittänyt, että se on ominaisuuden rajoitus. Tällä hetkellä varastonhallintaprosessit tukevat vain varastoa, jonka omistaja on yritys.
