---
title: SEO-metatietojen hallinta
description: Tässä artikkelissa kerrotaan, miten hakukoneoptimoinnin metatietoja hallitaan Microsoft Dynamics 365 Commerce -sovelluksessa.
author: josaw1
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 4b04d675a903279e667e1f5fcee387f05d979e81
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276825"
---
# <a name="manage-seo-metadata"></a>SEO-metatietojen hallinta

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, miten hakukoneoptimoinnin metatietoja hallitaan Microsoft Dynamics 365 Commerce -sovelluksessa.

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
1. Valitse komentopalkissa **Muokkaa**.
1. Valitse sivueditorissa sivun jäsennyksen ohjausobjektin yläosasta vasemmalla **Ääriviivatila-vaihtoehto** (ratassymboli) ja valitse sitten **Ääriviivan lisäasetukset -näkymä**.
1. Laajenna ääriviivanäkymässä puuohjausobjekteja niin, että **HTML head** -paikan sisältö näkyy.
1. Valitse **HTML head** -paikkaan haluamasi SEO-moduuli (esimerkiksi **Sivun yhteenveto**, **Tuotesivun yhteenveto**, **Luokkasivun yhteenveto** tai **Metatunnisteet**).
1. Muokkaa oikealla olevassa ominaisuusruudussa valitun SEO-moduulin haluttuja SEO-tietoja (esimerkiksi **Otsikko**, **Kuvaus** tai **Kuvan jakaminen**).
1. Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.
1. Syötä **Kommentit**-kenttään **Päivitetyt SEO-tiedot** ja valitse **OK**.
1. Esikatsele sivua valitsemalla **Esikatsele**. Kun olet valmis, palaa muokkaustyökaluun sulkemalla Esikatselu-välilehti.
1. Valitse **Julkaise**.

> [!TIP]
> Tekijät voivat käyttää **Ääriviivatila-vaihtoehto** (ratassymboli) sivueditorin vasemman ääriviivaohjausobjektin yläosassa, kun hän vaihtaa **Perusääriviiva-näkymän** ja **Ääriviivan lisäasetukset -näkymän** välillä. **Perusääriviiva-näkymä** on oletusasetus ja suodattaa ääriviivat siten, että siinä näkyvät vain sivun **Body**-HTML -paikan moduulit. **Ääriviivan lisäasetukset -näkymä** näyttää koko sivun moduulin, mukaan lukien **HTML head**-, **body begin**- ja **body end** -paikat. Tämä näkymä on hyödyllinen, kun laatijat voivat muokata sivun tiettyjä SEO- tai komentosarjamoduuliasetuksia.

## <a name="additional-resources"></a>Lisäresurssit

[Aiemmin luodun sivuston sivun muokkaaminen](modify-existing-page.md)

[Uuden sivuston sivun lisääminen](add-new-page.md)

[Sivun asettelujen valitseminen](select-page-layouts.md)

[Sivun tallentaminen, esikatseleminen ja julkaiseminen](save-preview-publish-page.md)

[Tuotesivun täydentäminen](enrich-product-page.md)

[Luokan saapumissivun täydentäminen](enrich-category-page.md)

[Sivun sisällön helppokäyttöisyyden tarkistaminen](verify-accessibility.md)

[Dynaamisten verkkokauppasivujen luominen URL-parametrien perusteella](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
