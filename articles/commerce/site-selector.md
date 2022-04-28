---
title: Sivuston valitsinmoduuli
description: Tässä ohjeaiheessa käsitellään sivuston valitsinmoduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
ms.date: 04/06/2022
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
ms.openlocfilehash: ad4d4d5f950d0631059d8f509e9e808a9106eb98
ms.sourcegitcommit: 4861ec2d3ae24cc9dd4ad3ac748fd05be3d80c70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/06/2022
ms.locfileid: "8551691"
---
# <a name="site-picker-module"></a>Sivuston valitsinmoduuli

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään sivuston valitsinmoduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.

Jos yrityksellä on useita sivustoja eri markkinoilla, alueilla ja kielialueilla, sivuston käyttäjät tarvitsevat kätevän tavan vaihdella sivustoja ja valitse ensisijaisen ostossivuston. Tätä skenaariota varten käyttäjät voivat selata useita sivustoja sivuston valitsinmoduulin ansiosta. Sivuston valitsinta suositellaan myös silloin, kun sähköpostiosoitteessa on otettu käyttöön [Sivuston tunnistus ja uudelleenohjaus](geo-detection-redirection.md), jotta asiakkaat voivat ohittaa [maan tai alueen valinta](country-region-picker-module.md) -moduulin avulla ilmaisemiaan toimipaikka-asetusta. 

Sivuston valitsinmoduuli on määritettävä käyttämällä sivustoluetteloa (markkinat, alueet tai kielialueet), jota sivuston käyttäjät voivat selata. Seuraavassa kuvassa on esimerkki sivuston sivun otsikossa olevasta sivuston valitsinmoduulista.

![Esimerkki sivuston valitsinmoduulista sivuston sivun otsikossa.](./media/ecommerce-sitepicker.PNG)

## <a name="site-picker-module-properties"></a>Sivuston valitsinmoduulin ominaisuudet

| Ominaisuuden nimi | Arvo                 | Kuvaus |
|---------------|-----------------------|-------------|
| Otsikko       | Teksti                  | Moduulin otsikko. |
| Sivustoasetukset  | Nimi, kuva, URL      | Tämä ominaisuus määrittää nimen, linkin sivuston aloitussivulle ja valinnaisen kuvan, jonka jokainen moduuliin kuuluva sivusto näkee. Kuva voi olla lippu tai jotakin muuta, joka ilmaisee markkinan, alueen tai kielialueen. |

## <a name="add-a-site-picker-module-to-a-page"></a>Sivuston valitsinmoduulin lisääminen sivulle

Sivuston valitsinmoduuli voidaan lisätä [otsikkomoduulin](author-header-module.md) **Sivustonvalitsin**-kohtaan. Kun sivuston valitsinmoduuli on lisätty, voit määrittää sen otsikon ja sivustovaihtoehdot. Yleensä otsikkomoduuli sisältyy otsikko-osaan, joka voidaan jakaa sivuston eri verkkokauppasivuille. Seuraavassa esimerkissä sivuston valitsinmoduuli on lisätty sellaisen otsikkomoduulin **Sivustonvalitsin**-paikkaan, joka sisältyy **HeaderContainer**-nimiseen otsikko-osaan.

![Esimerkki sivuston valitsinmoduulista otsikko-osassa.](./media/ecommerce-sitepicker-2.png)

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Ylätunnistemoduuli](author-header-module.md)

[Navigointipolkumoduuli](add-breadcrumb.md)

[Siirtymisvalikkomoduulit](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
