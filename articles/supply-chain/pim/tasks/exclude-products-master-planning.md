---
title: Tuotteen elinkaaren tason luonti jättämään tuotteita pääsuunnittelun ulkopuolelle
description: Tässä menettelyssä kuvataan, miten luodaan uuden tuotteen elinkaaren tila, joka sulkee pois tuotteet pääsuunnittelusta ja tuoterakennetason laskennasta.
author: cvocph
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cadf1d812e737309dbe8ca26d04ffb1ee88ef16a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818034"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a>Tuotteen elinkaaren tason luonti jättämään tuotteita pääsuunnittelun ulkopuolelle

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]