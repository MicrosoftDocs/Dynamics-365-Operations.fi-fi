---
title: Sivuston valitsinmoduuli
description: Tässä ohjeaiheessa käsitellään sivuston valitsinmoduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: a5f6f6e3ff459447aa4b3c0058b5526c9e8d1038a5d2629eefbed197012aebf0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772225"
---
# <a name="site-selector-module"></a>Toimipaikan valitsinmoduuli

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään sivuston valitsinmoduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.

Jos yrityksellä on useita sivustoja eri markkinoilla, alueilla ja kielialueilla, sivuston käyttäjät tarvitsevat kätevän tavan vaihdella sivustoja ja valitse ensisijaisen ostossivuston. Tätä skenaariota varten käyttäjät voivat selata useita sivustoja sivuston valitsinmoduulin ansiosta.

Sivuston valitsinmoduuli on määritettävä käyttämällä sivustoluetteloa (markkinat, alueet tai kielialueet), jota sivuston käyttäjät voivat selata.

> [!NOTE]
> Sivuston valitsinmoduuli on käytettävissä Dynamics 365 Commercen versiossa 10.0.14.

Seuraavassa kuvassa on esimerkki sivuston sivun otsikossa olevasta sivuston valitsinmoduulista.

![Esimerkki sivuston valitsinmoduulista sivuston sivun otsikossa.](./media/ecommerce-sitepicker.PNG)

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]