---
title: Integroitu vero
description: Tässä aiheessa kuvataan verotietojen integraatiota Finance and Operationsin ja Dataversen välillä.
author: robinarh
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: rhaertle
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: c7e76294944196670ed4b02ebf785c1bed7b5106f73d4b66a15a19c9a4235cbf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738549"
---
# <a name="integrated-tax"></a>Integroitu vero

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Veron asetustiedot määrittävät sekä välillisten verojen (ALV, GST-vero) ja ennakonpidätyksen asetukset Siinä käsitellään veron laskentasääntö, veroprosentti, verokirjanpito, tilitys ja muut käsitteet.

## <a name="templates"></a>Mallit

Verotiedot sisältävät taulukarttojen kokoelman, joita käytetään yhdessä tietojen vuorovaikutuksen aikana seuraavan taulukon mukaisesti.

| Finance and Operations -sovellukset | Asiakkaiden aktivointisovellukset | kuvaus |
|-----------------------------|-----------------------------------|-------------|
[Nimikkeen arvonlisäveroryhmä](mapping-reference.md#196) | msdyn_taxitemgroups | |
[Alv-viranomaiset](mapping-reference.md#193) | msdyn_taxauthorities | |
[Arvonlisäveron verovapauskoodin yksikkö CDS:lle](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[Arvonlisäveroryhmät](mapping-reference.md#195) | msdyn_taxgroups | |
[Arvonlisäveron kirjanpidon kirjausryhmät V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[Ennakonpidätyskoodit](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[Ennakonpidätysryhmät](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
