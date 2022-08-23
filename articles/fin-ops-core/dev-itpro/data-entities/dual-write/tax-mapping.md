---
title: Integroitu vero
description: Tässä artikkelissa käsitellään verotietojen integraatiota talous- ja toimintosovellusten sekä Dataversen välillä.
author: josaw
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8f148b710e2294edf1e402b9b8b22cb24e60a1f2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288791"
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

