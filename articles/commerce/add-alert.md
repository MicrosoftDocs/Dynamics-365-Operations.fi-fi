---
title: Kampanjabannerimoduuli
description: Tässä ohjeaiheessa käsitellään kampanjabannerimoduuleja ja niiden lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
manager: annbe
ms.date: 04/14/2020
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 12cabbf0b8d9f337f15a8cd6cb1f2a85100b75f7
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269771"
---
# <a name="promo-banner-module"></a>Kampanjabannerimoduuli


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään kampanjabannerimoduuleja ja niiden lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskatsaus

Kampanjabannerimoduuleja käytetään sivun sisäisten tietosanomien näyttämisessä. Niiden avulla voidaan näyttää koko sivustoa koskevia kampanjoita, jotka näkyvät kaikilla sähköisen kaupankäynnin sivuston sivuilla. 

Kampanjamoduulitmoduulit tukevat tekstisanomaa ja linkkiä. Jos kampanjabannerimoduuliin lisätään useita sanomia, siitä tulee kiertävä karusellibanneri, jossa asiakkaat voidaan kierrättää kaikki sanomat. 

Kampanjabannerimoduuleita ohjaavat sisällönhallintajärjestelmän (CMS) tiedot. Moduulit voidaan asettaa mille tahansa sivulle.

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a>Esimerkkejä kampanjabannerien käytöstä sähköisessä kaupankäynnissä

Kampanjabannereita voidaan käyttää sivuston ylätunnisteissa, jossa niissä voidaan näyttää koko sivustoa koskevia kampanjoita tai sanomia, kuten seuraavissa esimerkeissä.

Vuosittainen alennusmyynti loppuu 10 päivän kuluttua

Alennusmyynnit ennen koulujen alkamista. Osta nyt.

## <a name="promo-banner-module-properties"></a>Kampanjabannerimoduulin ominaisuudet

| Ominaisuuden nimi             | Value                              | Kuvaus |
|---------------------------|------------------------------------|-------------|
| Banneriviestit           | Teksti ja linkit                     | Teksti-ja linkkitaulukko |
| Automaattinen toisto                  | **Tosi** vai **Epätosi**              | Arvo, joka ilmaisee kierrätetäänkö sanomia automaattisesti, jos useita sanomia on määritetty. |
| Dian vaihtoväli | Millisekuntien (ms) määrä      | Aikaväli, jota käytetään sanomien kierrättämiseen. |
| Salli ohittaminen             | **Tosi** vai **Epätosi**              | Jos arvoksi on määritetty **Tosi**, asiakkaat voivat hylätä hälytyksen. |
| Näytä karusellin valitsin     | **Tosi** vai **Epätosi**              | Arvo, joka ilmaisee, näytetäänkö karusellin valitsimet, jotta asiakkaan voivat kierrättää useita bannerikohteita manuaalisesti. |
| Tekstin tasaus            | **Oikealla**, **vasemmalla** tai **keskellä** | Tekstin kohdistus kampanjabannerimoduulissa. |
| Linkitä                      | URL-osoite                              | Vapaavalintaisen linkin URL-osoite. |

## <a name="add-a-promo-banner-module-to-a-page"></a>Kampanjabannerimoduulin lisääminen sivulle 

Voit lisätä kampanjabannerimoduulin sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Luo sivumalli valitsemalla **Uusi**.
1. Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan **Mainosnauhan malli** ja valitse sitten **OK**.
1. Lisää **Oletussivu**-moduuli **Tekstiosa**-paikkaan **Sivun jäsennys** -kohdassa. 
1. Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen. 
1. Luo **Kampanjabannerisivu**-niminen sivu käyttämällä juuri luotua mallia. 
1. Lisää säilömoduuli uuden sivun **pääpaikkaan**. 
1. Määritä oikeassa ruudussa **Leveys**-arvoksi **Täytä säilö**.
1. Lisää kampanjabannerimoduuli säilömoduuliin **Sivun jäsennys** -kohdassa.
1. Lisää vähintään yksi bannerisanoma bannerimoduulin asetuksissa. Kussakin sanomassa voi olla tekstiä ja linkki. Voit mukauttaa moduulia entisestään muokkaamalla muita ominaisuuksia.
1. Valitse **Tallenna**ja esikatsele sitten sivua valitsemalla **Esikatselu**. Sivun yläosassa pitäisi nyt olla hälytys, joka näyttää lisäämäsi tekstin.
1. Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen. 

> [!NOTE]
> Kampanjabanneria käytetään yleensä sivun ylätunniste- ja alaotsikkopaikassa.


## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Karusellimoduuli](add-carousel.md)

[Tekstilohkomoduuli](add-content-rich-block.md)

[Sisältölohkomoduuli](add-hero-module.md)

[Videotoistinmoduuli](add-video-player.md)
