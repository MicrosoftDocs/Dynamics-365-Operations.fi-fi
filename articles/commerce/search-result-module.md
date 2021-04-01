---
title: Hakutulosmoduuli
description: Tässä ohjeaiheessa on tietoja hakutulosmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5d852fe1a81b1e42484bc49ae136ef8613a2d3a5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254766"
---
# <a name="search-results-module"></a>Hakutulosmoduuli

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä ohjeaiheessa on tietoja hakutulosmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

Hakutulosmoduuli palauttaa tuotehaun tulokset ja luettelon tuotteisiin käytettävistä tarkennuksista. Dynamics 365 Commerce -sivustojen hakutulosmoduulien avulla voit muodostaa sivuja seuraavissa tilanteissa:

- Käyttäjähaun käynnistämät hakutulokset
- Hakutulokset, jotka näyttävät tietyn tuotejoukon, kuten "Ota samankaltaisia tuotteita"
- Luettelo tuotteista, jotka kuuluvat luokkaan

Lisätietoja luokka- ja hakutulossivuista on ohjeessa [Luokan oletussaapumis- ja oletushakutulossivun yleiskatsaus](category-search-page-overview.md).

Seuraavassa kuvassa näkyy esimerkki Fabrikam-sivuston luokan hakutulossivusta.

![Esimerkki hakutulossivusta Fabrikam-sivustolla](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a>Hakutulosmoduulin ominaisuudet

Seuraavassa taulukossa luetellaan hakutulosmoduulien ominaisuudet sekä niiden arvot ja kuvaukset.

| Ominaisuus | Arvot | kuvaus |
|----------|--------|-------------|
| Tuotteita sivulla | Kokonaisluku | Kullakin sivulla näkyvien nimikkeiden määrä. |
| Salli varmuuskopiointi PDP-kohteessa | **Tosi** vai **Epätosi** | Jos tämän ominaisuuden arvoksi määritetään **Tosi**, kun käyttäjä valitsee tuotteen hakutulossivulta, avautuvan tuotetietosivun (PDP) siirtymispolku näyttää Takaisin tuloksiin -linkin. |
| Laajenna tarkennukset | **Kaikki**, **1**, **2**, **3** tai **4** | Tärkeimpien tarkentajien määrä, jotka tulisi laajentaa, kun sivu ladataan. Jos ominaisuuden arvoksi määritetään esimerkiksi **3**, sivun ensimmäiset kolme tarkentajaa laajennetaan. |
| Piilota luokkahierarkian näyttö | **Tosi** vai **Epätosi** | Jos ominaisuuden arvoksi määritetään **Tosi**, sivulla näkyvä luokkahierarkia piilotetaan. Tämän ominaisuuden arvoksi tulee määrittää **Tosi**, jos luokkahierarkian näyttämiseen käytetään [siirtymispolkumoduulia](add-breadcrumb.md).|
| Sisällytä tuotemääritteet hakutuloksiin | **Tosi** vai **Epätosi** | Jos ominaisuuden arvoksi määritetään **Tosi**, tuotteiden määritteet palautetaan hakutuloksissa. Vaikka nämä määritteet voidaankin näyttää Commerce-sivustossa, laajennus on pakollinen.|
| Näytä liitoksen hinnat | **Tosi** vai **Epätosi** | Jos tämän ominaisuuden arvoksi määritetään **Tosi**, tuotteiden liittyvät hinnat näkyvät tuloksissa, kun kirjautunut käyttäjä selaa sivua. |

> [!IMPORTANT]
> Dynamics 365 Commerce -julkaisussa 10.0.16 ja sitä myöhemmissä versioissa **Näytä liittyvät hinnat** -konfiguraatiota voidaan käyttää liittyvien hintojen näyttämiseen sivulla.

## <a name="supported-modules"></a>Tuetut moduulit

Hakutulosmoduuli tukee [pikanäkymämoduulia](quick-view-module.md), jonka avulla käyttäjät voivat tarkastella tuotetietoja ja lisätä nimikkeitä ostoskoriin hakutulossivulta.

## <a name="add-a-search-results-module-to-a-category-page"></a>Hakutulosmoduulin lisääminen luokkasivulle

Voit lisätä luokkasivulle hakutulosmoduulin seuraavasti.

1. Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.
1. Kirjoita **Uusi malli** -valintaikkunassa nimi **Hakutulokset** ja valitse sitten **OK**.
1. Valitse kolme pistettä (...) **Tekstiosa**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Oletussivu**-moduuli ja valitse sitten **OK**.
1. Valitse **Oletussivu**-moduulin **Pää**-paikka. Valitse kolmen pisteen painike (...) ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.
1. Valitse kolme pistettä (...) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Linkkipolku**-moduuli ja valitse sitten **OK**.
1. Anna sitten **Navigointipolku**-omiansiuusruudussa arvo **1** kentälle **Toistojen vähimmäismäärä**.
1. Valitse kolme pistettä (...) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Hakutulokset**-moduuli ja valitse sitten **OK**.
1. Kirjoita **Hakutulokset**-ominaisuusruudussa arvo **1** kentälle **Toistojen vähimmäismäärä** ja määritä sitten muut hakutulosmoduulin pakolliset ominaisuudet. Kun määrität nämä ominaisuudet malliin, varmistat, että tietyn luokkasivun mukautukset sisältävät nämä asetukset automaattisesti.
1. Valitse **Lopeta muokkaus** ja valitse sitten **Julkaise** julkaistaksesi mallin.
1. Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.
1. Valitse **Valitse malli** -valintaikkunassa luomasi **Hakutulokset**-malli, kirjoita **sivun nimeksi** **Luokkasivu** ja valitse sitten **OK**. Koska kaikki arvot on määritetty mallissa, sivu on valmis julkaistavaksi.
1. Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.

## <a name="additional-resources"></a>Lisäresurssit

[Luokan oletussaapumis- ja oletushakutulossivun yleiskatsaus](category-search-page-overview.md)

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Pikanäkymämoduuli](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]