---
title: Karttamoduuli
description: Tässä ohjeaiheessa on tietoja karttamoduuleista ja niiden määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
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
ms.openlocfilehash: a0f5d902289c5867095e34a135c50d342f3c4f13
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/31/2020
ms.locfileid: "3646920"
---
# <a name="map-module"></a>Karttamoduuli

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä ohjeaiheessa on tietoja karttamoduuleista ja niiden määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.

## <a name="overview"></a>Yleiskuvaus

Karttamoduuli, jossa näkyvät myymälöiden sijainnit [Bing Maps V8 -verkko-ohjausobjektin](https://docs.microsoft.com/bingmaps/v8-web-control/) avulla hahmonnetussa interaktiivisessa kartassa. Bing Maps -ohjelmointirajapinnan avain on pakollinen, ja se on lisättävä Commercen pääkonttorisovelluksen jaettuihin parametreihin. Karttamoduulit tarjoavat erilaisia näkymiä, kuten maantie-, ilma- ja katunäkymät. Niiden avulla käyttäjät voivat tarkastella karttasijainteja. Ne mahdollistavat myös vuorovaikutuksen, kuten zoomauksen ja käyttäjän sijainnin käyttämisen.

Karttamoduuli toimii yhdessä myymälän valitsinmoduulin kanssa ja määrittää kartalla muodostettujen myymälöiden maantieteelliset sijainnit. Myymälän valitsin ja karttamoduulit ovat vuorovaikutuksessa, kun käyttäjä valitsee myymälän jollakin sivustosivulla olevista moduuleista. Karttamoduuleja voidaan laajentaa muihin skenaarioihin myymälän valitsinmoduulien vuorovaikutuksen lisäksi. Moduulin mukautus on kuitenkin pakollinen.

Karttamoduuli esiteltiin Commercen versiossa 10.0.13.

Seuraavassa kuvassa näkyy esimerkki karttsmoduulista, jota käytetään myymälän sijaintien sivulla.

![Esimerkki myymälän valitsinmoduulista](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a>Moduulin ominaisuudet

| Ominaisuuden nimi             | Arvo                 | kuvaus |
|---------------------------|-----------------------|-------------|
| Otsikko | Teksti | Moduulin otsikko. |
| Nuppineula-asetukset: Oletuskuvake | Kuva | Nuppineulasymbolin kuva, jota käytetään kartalla näkyvissä myymälöissä. |
| Nuppineula-asetukset: Aktiivinen-kuvake | Kuva | Nuppineulasymbolin kuva, jota käytetään kartalla valitussa myymälässä. |
| Nuppineula-asetukset: Oletuskuvakkeen väri | Merkkijono | Kartan nuppineulasymboleiden värin teksti- tai heksadesimaaliarvo. |
| Nuppineula-asetukset: Aktiivinen-kuvakkeen väri | Merkkijono | Kartan valittujen nuppineulasymboleiden värin teksti- tai heksadesimaaliarvo. |
| Näytä indeksi | **Tosi** vai **Epätosi** | Jos tämän ominaisuuden arvoksi on määritetty **Tosi**, jokainen myymälän osoittava nuppineulasymboli näyttää indeksin. Tämä indeksi vastaa sellaisen luettelonäkymän indeksiä, jonka myymälän valitsinmoduuli näyttää. |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a>Sallittujen yhdistämismääritysten URL-osoitteiden lisääminen sivuston sisällön suojauskäytännön direktiiveihin

Jotta karttamoduuli voi toimia yhdessä Bing Mapsin kanssa, varmista, että seuraavat yhdistämismääritysten URL-osoitteet ovat sallittuja (sallittujen luettelo) sivuston sisällön suojauskäytännön mukaan. Tämä asetus tehdään Commercen sivustonmuodostimessa lisäämällä sallitut URL-osoitteet eri sivustojen CSP-direktiiveihin (esimerkiksi **img-src**). Lisätietoja on kohdassa [Sisällön suojauskäytäntö](manage-csp.md). 

- Lisää **connect-src**-direktiiviin **&#42;.bing.com**.
- Lisää **img-src**-direktiiviin **&#42;.virtualearth.net**.
- Lisää **script-src**-direktiiviin **&#42;.bing.com, &#42;.virtualearth.net**.
- Lisää **skriptin style-src** -direktiiviin **&#42;.bing.com**.

## <a name="add-a-map-module-to-a-page"></a>Karttamoduulin lisääminen sivulle

Lisätietoja karttamoduulin määrittämisestä sivulla on kohdassa [Myymälän valitsinmoduuli](store-selector.md). 
 
## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Ostoruutumoduuli](add-buy-box.md)

[Ostoskorimoduuli](add-cart-module.md)

[Myymälän valitsinmoduuli](store-selector.md)

[Bing Maps -karttapalvelun hallinta organisaatiossa](./dev-itpro/manage-bing-maps.md)

[Bing Maps V8 -verkko-ohjausobjekti](https://docs.microsoft.com/bingmaps/v8-web-control/)