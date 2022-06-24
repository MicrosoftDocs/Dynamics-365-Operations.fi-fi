---
title: Integroitu vero
description: Tässä artikkelissa käsitellään verotietojen integraatiota Finance and Operationsin ja Dataversen välillä.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8864a9567d57739aa72fa1859f5cfce6df33e8f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864540"
---
# <a name="integrated-tax"></a>Integroitu vero

[!include [banner](../../includes/banner.md)]



Veron asetustiedot määrittävät sekä välillisten verojen (ALV, GST-vero) ja ennakonpidätyksen asetukset Siinä käsitellään veron laskentasääntö, veroprosentti, verokirjanpito, tilitys ja muut käsitteet.

## <a name="templates"></a>Mallit

Verotiedot sisältävät taulukarttojen kokoelman, joita käytetään yhdessä tietojen vuorovaikutuksen aikana seuraavan taulukon mukaisesti.

| Taloushallinnon ja toimintojen sovellukset | Asiakkaiden aktivointisovellukset | Kuvaus |
|-----------------------------|-----------------------------------|-------------|
[Nimikkeen arvonlisäveroryhmä](mapping-reference.md#196) | msdyn_taxitemgroups | |
[Alv-viranomaiset](mapping-reference.md#193) | msdyn_taxauthorities | |
[Arvonlisäveron verovapauskoodin yksikkö CDS:lle](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[Arvonlisäveroryhmät](mapping-reference.md#195) | msdyn_taxgroups | |
[Arvonlisäveron kirjanpidon kirjausryhmät V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[Ennakonpidätyskoodit](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[Ennakonpidätysryhmät](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
