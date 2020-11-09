---
title: Sivuston valitsinmoduuli
description: Tässä ohjeaiheessa käsitellään sivuston valitsinmoduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: bd54695f54b501631f916328c05bfd47e538d50d
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055827"
---
# <a name="site-selector-module"></a>Sivuston valitsinmoduuli

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä ohjeaiheessa käsitellään sivuston valitsinmoduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskuvaus

Jos yrityksellä on useita sivustoja eri markkinoilla, alueilla ja kielialueilla, sivuston käyttäjät tarvitsevat kätevän tavan vaihdella sivustoja ja valitse ensisijaisen ostossivuston. Tätä skenaariota varten käyttäjät voivat selata useita sivustoja sivuston valitsinmoduulin ansiosta.

Sivuston valitsinmoduuli on määritettävä käyttämällä sivustoluetteloa (markkinat, alueet tai kielialueet), jota sivuston käyttäjät voivat selata.

> [!NOTE]
> Sivuston valitsinmoduuli on käytettävissä Dynamics 365 Commercen versiossa 10.0.14.

Seuraavassa kuvassa on esimerkki sivuston sivun otsikossa olevasta sivuston valitsinmoduulista.

![Esimerkki sivuston valitsinmoduulista sivustonsivun otsikossa](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a>Sivuston valitsinmoduulin ominaisuudet

| Ominaisuuden nimi | Arvo                 | kuvaus |
|---------------|-----------------------|-------------|
| Otsikko       | Teksti                  | Moduulin otsikko. |
| Sivustoasetukset  | Nimi, kuva, URL      | Tämä ominaisuus määrittää nimen, linkin sivuston aloitussivulle ja valinnaisen kuvan, jonka jokainen moduuliin kuuluva sivusto näkee. Kuva voi olla lippu tai jotakin muuta, joka ilmaisee markkinan, alueen tai kielialueen. |

## <a name="add-a-site-selector-module-to-a-page"></a>Sivuston valitsinmoduulin lisääminen sivulle

Sivuston valitsinmoduuli voidaan lisätä [otsikkomoduuliin](author-header-module.md) sivuston valitsinpaikan alapuolelle. Kun moduuli on lisätty, voit määrittää sen otsikon ja sivustovaihtoehdot.

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Ylätunnistemoduuli](author-header-module.md)

[Navigointipolkumoduuli](add-breadcrumb.md)

[Siirtymisvalikkomoduulit](nav-menu-module.md)
