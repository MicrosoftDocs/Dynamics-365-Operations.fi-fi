---
title: Karttamoduuli
description: Tässä ohjeaiheessa on tietoja karttamoduuleista ja niiden määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.
author: anupamar-ms
ms.date: 09/15/2020
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
ms.openlocfilehash: 659211f3a74c38389f991cd2385366d175b0c7c0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020256"
---
# <a name="map-module"></a>Karttamoduuli

[!include [banner](includes/banner.md)]


Tässä ohjeaiheessa on tietoja karttamoduuleista ja niiden määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.

Karttamoduuli, jossa näkyvät myymälöiden sijainnit [Bing Maps V8 -verkko-ohjausobjektin](/bingmaps/v8-web-control/) avulla hahmonnetussa interaktiivisessa kartassa. Bing Maps -ohjelmointirajapinnan avain on pakollinen, ja se on lisättävä Commercen pääkonttorisovelluksen jaettuihin parametreihin. Karttamoduulit tarjoavat erilaisia näkymiä, kuten maantie-, ilma- ja katunäkymät. Niiden avulla käyttäjät voivat tarkastella karttasijainteja. Ne mahdollistavat myös vuorovaikutuksen, kuten zoomauksen ja käyttäjän sijainnin käyttämisen.

Karttamoduuli toimii yhdessä myymälän valitsinmoduulin kanssa ja määrittää kartalla muodostettujen myymälöiden maantieteelliset sijainnit. Myymälän valitsin ja karttamoduulit ovat vuorovaikutuksessa, kun käyttäjä valitsee myymälän jollakin sivustosivulla olevista moduuleista. Karttamoduuleja voidaan laajentaa muihin skenaarioihin myymälän valitsinmoduulien vuorovaikutuksen lisäksi. Moduulin mukautus on kuitenkin pakollinen.

> [!NOTE]
> Karttamoduuli on käytettävissä Dynamics 365 Commercen versiossa 10.0.13.

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

Jotta karttamoduuli voi toimia yhdessä Bing Mapsin kanssa, varmista, että seuraavat yhdistämismääritysten URL-osoitteet ovat sallittuja sivuston sisällön suojauskäytännön mukaan. Tämä asetus tehdään Commercen sivustonmuodostimessa lisäämällä sallitut URL-osoitteet eri sivustojen CSP-direktiiveihin (esimerkiksi **img-src**). Lisätietoja on kohdassa [Sisällön suojauskäytäntö](manage-csp.md). 

- Lisää **connect-src**-direktiiviin **&#42;.bing.com**.
- Lisää **img-src**-direktiiviin **&#42;.virtualearth.net**.
- Lisää **script-src**-direktiiviin **&#42;.bing.com, &#42;.virtualearth.net**.
- Lisää **skriptin style-src** -direktiiviin **&#42;.bing.com**.

## <a name="add-a-map-module-to-a-page"></a>Karttamoduulin lisääminen sivulle

Lisätietoja karttamoduulin määrittämisestä sivulla on kohdassa [Myymälän valitsinmoduuli](store-selector.md). 
 
## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Ostoruutumoduuli](add-buy-box.md)

[Ostoskorimoduuli](add-cart-module.md)

[Myymälän valitsinmoduuli](store-selector.md)

[Bing Maps -karttapalvelun hallinta organisaatiossa](./dev-itpro/manage-bing-maps.md)

[Bing Maps V8 -verkko-ohjausobjekti](/bingmaps/v8-web-control/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]