---
title: Integroitu vero
description: Tässä ohjeaiheessa käsitellään verotietojen integraatiota Finance and Operationsin ja Dataversen välillä.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 532e6603b74ad0293d65684d2d6858ef31fbc496
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063184"
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
