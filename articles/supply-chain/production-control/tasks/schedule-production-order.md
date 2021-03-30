---
title: Ajoita tuotantotilaus
description: Tässä menettelyssä selvitetään, miten tuotantotilaus ajoitetaan.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum, ProdRouteJobSched, ProductionOrderScheduleDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 93ec5bd6984dd1a8f970834070fd77873078b3b0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237128"
---
# <a name="schedule-a-production-order"></a>Ajoita tuotantotilaus

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä selvitetään, miten tuotantotilaus ajoitetaan. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tämä on kolmas seitsemästä tuotantotilauksen elinkaaresta kertovasta menettelystä.


## <a name="schedule-a-production-order"></a>Ajoita tuotantotilaus
1. Siirry kohtaan Tuotannonhallinta > Tuotantotilaukset > Kaikki tuotantotilaukset.
    * Valitse tuotantotilaus, jonka tila on Arvioitu.  
2. Valitse toimintoruudussa Aikataulu.
3. Valitse Ajoita työt.
    * Ajoituksen parametrit määritetään tällä sivulla. Voit määrittää parametrit tietyille käyttäjille tai kaikille käyttäjille.  
4. Valitse Ajoituksen suunta -kentässä Tästä päivästä eteenpäin.
5. Anna Ajoituspäivämäärä-kentässä päivämäärä.
6. Valitse Rajallinen kapasiteetti -valintaruutu tai poista sen valinta.
7. Valitse Rajallinen materiaali -valintaruutu tai poista sen valinta.
8. Valitse OK.

## <a name="view-the-scheduling-results"></a>Näytä ajoituksen tulokset
1. Valitse toimintoruudussa Tuotantotilaus.
2. Valitse Kaikki työt.
    * Juuri luodut ajoitetut työt näkyvät tällä sivulla.  
3. Laajenna tai tiivistä Aikataulutus-osa.
    * Voit tarkastella ajoituksen pikavälilehdessä ajoitettua päivämäärää ja aikaa.  
4. Valitse Kyselyt.
5. Valitse Kapasiteetin kuormitus.
    * Kapasiteetin kuormitus -sivulla näkyy töiden ajoittamisella varattu kapasiteetti, resurssiin tällä hetkellä varattujen tuntien kokonaismäärä ja resurssissa jäljellä olevat tunnit, joille voidaan ajoittaa töitä.  
6. Sulje sivu.
7. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]