---
title: Adventure Works -teeman yleiskatsaus
description: Tässä artikkelissa on yleiskatsaus Adventure Works -teemasta ja sen käyttämisestä sivuston sivuilla Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
ms.date: 12/03/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4f13d6c1c4b0e2764c22dc3d7311c726fac7989d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874984"
---
# <a name="adventure-works-theme-overview"></a>Adventure Works -teeman yleiskatsaus

[!include [banner](includes/banner.md)]

Tässä artikkelissa on yleiskatsaus Adventure Works -teemasta ja sen käyttämisestä sivuston sivuilla Microsoft Dynamics 365 Commercessa.

Dynamics 365 Commerce sisältää sähköisen kaupankäynnin teeman, jonka nimi on Adventure Works. Adventure Works -teema esittelee urheilutuotteita ja vapaa-ajan tuotteita, ja se on optimoitu monipuolista ja paranneltua tarinoidenkerrontaa varten. Se tarjoaa modernin ulkoasun, uusia asetteluita ja animaatiotehosteita, joiden avulla voit luoda sähköisen kaupan asiakkaille houkuttelevan ja mukaansatempaavan verkko-ostoskokemuksen.

## <a name="trial-environments-in-commerce"></a>Commerce-kokeiluympäristöt

Jos haluat nähdä, miltä Adventure Works -teema näyttää, kun se otetaan kuluttajakaupan ja yritystenvälisen kaupan sivustoilla, vieraile seuraavilla kokeilusivustoilla:

- [Adventure Works -kuluttajakaupan sivusto](https://www.adventure-works.com/)
- [Adventure Works -yritysten välisen kaupan sivusto](https://www.adventure-works.com/business)

## <a name="theme-capabilities"></a>Teeman ominaisuudet

Adventure Works -teema tarjoaa seuraavat uudet ominaisuudet:

- Videotoistinmoduuli tukee nyt otsikoita, kappaleita ja linkitystä parempaa tarinankerrontaa varten.
- Sisältöjen siirtymät ovat parempia animaatioiden ansiosta.
- "Lisää ostoskoriin" -toiminto avaa pienoiskorin ilmoituksen näyttämisen sijaan.
- Pikanäkymämoduuli on ruutu, joka liukuu sekä tietokoneen että mobiililaitteen näytöllä.
- Sivuston sivuilla on uusia asetteluita. 
- Markkinointisisällön voi konfiguroida kärryä ja minikärryä varten, kun ne ovat tyhjiä.
- Minikärryssä voi näkyä kampanjasanomia, kuten "Ilmainen toimitus yli $50 arvoisille tilauksille".
- Kuvauskortit hahmonnetaan haku- ja luokkasivuilla.

Adventure Works -teema sisältää nyt seuraavat tarinankerrontamoduulit Commerce-moduulikirjastossa:

- [Ruutuluettelomoduuli](tile-list-module.md)
- [Vuorovaikutteinen ominaisuusmoduuli](interactive-feature-module.md)
- [Aktiivinen kuvamoduuli](active-image-module.md)
- [Allekirjoitusmoduuli](subscribe-module.md)
- [Kuvaluettelomoduuli](image-list-module.md)

Adventure Works -teema on täysin responsiivinen, ja se tarjoaa optimoidun käyttökokemuksen tietokoneiden, mobiililaitteiden ja tablettien näytöille.

> [!IMPORTANT]
> Adventure Works -teema ja uudet moduulit ovat käytettävissä Dynamics 365 Commerce -versiosta 10.0.20 eteenpäin.

Seuraavassa kuvassa on esimerkki aloitussivusta, joka käyttää Adventure Works -teemaa.

![Esimerkki aloitussivusta, joka käyttää Adventure Works -teemaa](./media/aw_b2c.PNG)

Seuraavassa kuvassa on esimerkki luettelosivusta, joka käyttää Adventure Works -teemaa.

![Esimerkki luettelosivusta, joka käyttää Adventure Works -teemaa](./media/Aw_list.PNG)

Seuraavassa kuvassa on esimerkki tuotetietosivusta (PDP), joka käyttää Adventure Works -teemaa.

![Esimerkki tuotetietosivusta (PDP), joka käyttää Adventure Works -teemaa](./media/aw_pdp.PNG)

## <a name="use-the-adventure-works-theme-for-b2b-sites"></a>Adventure Works -teeman käyttäminen B2B-sivustoille

Adventure Works -teema on myös yritystenvälisen yhteistyön (B2B) sivustojen viiteteema. Kaikki B2B-moduulit ja työnkulut esitellään Adventure Works -teemassa. Lisätietoja B2B-sivuston määrittämisestä on kohdassa [B2B-sivuston määritys](./b2b/set-up-b2b-site.md).

Seuraavassa kuvassa on esimerkki B2B-aloitussivusta, joka käyttää Adventure Works -teemaa.

![Esimerkki B2B-aloitussivusta, joka käyttää Adventure Works -teemaa](./media/aw_b2b.PNG)

## <a name="theme-extensions"></a>Teemalaajennukset

Adventure Works -teema sisältää useita teemalaajennuksia, kuten **näkymälaajennukset** ja **moduulimääritelmän** laajennukset. Adventure Works -teemaa voidaan käyttää viiteteemana samankaltaisen laajennusten luomiseen. Esimerkiksi Adventure Works -teeman luettelosivu on toteutettu näkymälaajennuksena, jolla on vaakasuora tarkentajana. (Sen sijaan vasemman ruudun tarkentajaa käytetään Fabrikam-teemassa).

Muut moduulit sisältävät myös moduulimääritelmän laajennuksia. Esimerkiksi [ostoskorikuvakemoduuli](cart-icon-module.md) sisältää kaksi ylimääräistä **Tyhjä ostoskori**- ja **Kampanjasisältö**-paikkaa, jotka on toteutettu käyttämällä moduulimääritelmän laajennuksia. Lisäksi otsikkomoduuliin on lisätty uusi **Mobiililogo**-ominaisuus, joka tukee logoa mobiililaitteiden näytöillä. Tämä ominaisuus on toteutettu otsikkomoduulin määritelmän laajennuksena.

Lisätietoja teemalaajennuksista on kohdassa [Teemalaajennukset](e-commerce-extensibility/theme-module-extensions.md).

## <a name="install-the-adventure-works-theme"></a>Adventure Works -teeman asentaminen

Lisätietoja Adventure Works -teeman asentamisesta on [Adventure Works -teeman asennuksessa](install-adventure-works.md).

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Ruutuluettelomoduuli](tile-list-module.md)

[Interaktiivinen ominaisuusmoduuli](interactive-feature-module.md)

[Aktiivinen kuvamoduuli](active-image-module.md)

[Tilausmoduuli](subscribe-module.md)

[Kuvaluettelomoduuli](image-list-module.md)

[Teemalaajennukset](e-commerce-extensibility/theme-module-extensions.md)

[Ostoskorikuvakemoduuli](cart-icon-module.md)

[Yritystenvälisen yhteistyön sähköisen kaupankäynnin sivuston määrittäminen](./b2b/set-up-b2b-site.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
