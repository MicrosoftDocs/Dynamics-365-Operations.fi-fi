---
title: SEO-metatietojen hallinta
description: Tässä ohjeaiheessa kerrotaan, miten hakukoneoptimoinnin metatietoja hallitaan Microsoft Dynamics 365 Commerce -sovelluksessa.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b69d9d2769023967e2b94fef1b8fcf6b5b3357c5
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698346"
---
# <a name="manage-seo-metadata"></a>SEO-metatietojen hallinta

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten hakukoneoptimoinnin metatietoja hallitaan Microsoft Dynamics 365 Commerce -sovelluksessa.

## <a name="overview"></a>Yleiskatsaus

Sivuston hakukoneoptimoinnin metatietoja voi hallita sivustokarttojen ja sivun metatietojen avulla.
    
## <a name="site-maps"></a>Sivustokartat

Sivustokartta on sivuston sivujen koneluettava luettelo, joka on XML-muodossa. Se on tarkoitettu hakuohjelmien käyttöön. Näin ne voivat tarjota parempia hakutuloksia sivustosta. Hakuohjelmat voivat käyttää sivustokarttoja manuaalisesti tai ne voidaan julkaista robots.txt-tiedostossa.

Dynamics 365 Commerce tukee sivustokarttojen automaattista luontia. Sivustokartat päivittyvät automaattisesti, kun sivut julkaistaan tai niiden julkaiseminen perutaan.

### <a name="turn-on-site-map-generation"></a>Sivustokartan luonnin ottaminen käyttöön

1. Kirjaudu sisään muokkaustyökaluun.
1. Valitse **Sivustot**-kohdassa **Fabrikam** (tai sivuston nimi).
1. Valitse vasemmanpuoleisessa siirtymisruudussa **Sivuston hallinta**.
1. Varmista, että **Sivustokartta käytössä** -asetus on käytössä.

## <a name="page-metadata"></a>Sivun metatiedot

Dynamics 365 Commercen avulla voit hallita yksittäisten sivujen hakukoneoptimoinnin metatietoja. Voit tarkastella ja muokata näitä tietoja sivusäilön **Hakukoneoptimoinnin ominaisuudet** -osassa. Seuraavia hakukoneoptimoinnin metatietojen ominaisuuksia tuetaan:

- Titteli
- Kuvaus
- Hakukoneoptimoinnin avainsanat
- Aria-otsikot
- noindex
- nofollow
- noarchive
- nocache
- noOpenDirectoryProject
- nosnippet
- noImageIndex
- unavailableAfter

### <a name="modify-page-metadata"></a>Sivun metatietojen muokkaaminen

Voit muokata sivun metatietoja seuraavasti.

1. Valitse **Sivustot**-kohdassa **Fabrikam** (tai sivuston nimi).
1. Valitse vasemmanpuoleisessa siirtymisruudussa **Sivut**.
1. Valitse aloitussivu, joka avataan sivueditorissa.
1. Valitse toimintoruudussa **Kuittaa ulos**.
1. Laajenna oikeanpuoleisessa ominaisuusruudussa **Oletusmetatunnukset**-kohta.
1. Jos haluat lisätä uuden metatunnuksen, valitse **Lisää**ja kirjoita sitten tunnus kenttään.

    Jos haluat poistaa olemassa olevan metatunnuksen, valitse sen oikealla puolella oleva roskakorisymboli.

1. Valitse ensin **Tallenna** ja sitten **Kirjaa sisään**.
1. Syötä **Kommentit**-kenttään **Päivitetyt metatunnukset** ja valitse **OK**.
1. Esikatsele sivua valitsemalla **Esikatsele**. Kun olet valmis, palaa muokkaustyökaluun sulkemalla Esikatselu-välilehti.
1. Valitse **Julkaise**.

## <a name="additional-resources"></a>Lisäresurssit

[Aiemmin luodun sivuston sivun muokkaaminen](modify-existing-page.md)

[Uuden sivuston sivun lisääminen](add-new-page.md)

[Sivun asettelujen valitseminen](select-page-layouts.md)

[Sivun tallentaminen, esikatseleminen ja julkaiseminen](save-preview-publish-page.md)

[Tuotesivun täydentäminen](enrich-product-page.md)

[Luokan saapumissivun täydentäminen](enrich-category-page.md)
