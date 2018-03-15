--- 
title: "Tuotteen elinkaaren tason luonti jättämään tuotteita pääsuunnittelun ulkopuolelle"
description: "Tässä menettelyssä kuvataan, miten luodaan uuden tuotteen elinkaaren tila, joka sulkee pois tuotteet pääsuunnittelusta ja tuoterakennetason laskennasta."
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 74606b1378e94e8a6945a408520c8b68648970d8
ms.openlocfilehash: 1685e8eb706e29ef5b195e9163bf19345fee78b6
ms.contentlocale: fi-fi
ms.lasthandoff: 02/07/2018

---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a>Tuotteen elinkaaren tason luonti jättämään tuotteita pääsuunnittelun ulkopuolelle

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tässä menettelyssä kuvataan, miten luodaan uuden tuotteen elinkaaren tila, joka sulkee pois tuotteet pääsuunnittelusta ja tuoterakennetason laskennasta.


## <a name="create-an-obsolete-state"></a>Vanhentuneen tilan luominen
1. Valitse Tuotetietojen hallinta > Asetukset > Tuotteen elinkaaren tila.
2. Valitse Uusi.
3. Kirjoita arvo Tila-kenttään.
4. Valitse On käytettävissä suunnitteluun -kentässä Ei.
5. Kirjoita arvo Kuvaus-kenttään.

## <a name="associate-the-obsolete-state-to-a-released-product"></a>Vanhentuneen tilan liittäminen julkaistuun tuotteeseen
1. Sulje sivu.
2. Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.
3. Käytä pikasuodatinta tietueiden etsimiseen. Suodata esimerkiksi Haun nimi -kenttä arvolla M00.
4. Valitse Muokkaa.
5. Merkitse valittu rivi luettelossa.
6. Syötä tai valitse arvo Tuotteen elinkaaren tila -kenttään.


