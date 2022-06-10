---
title: Kampanjabannerimoduuli
description: Tässä ohjeaiheessa käsitellään kampanjabannerimoduuleja ja niiden lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
ms.date: 05/18/2022
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1b7e7a8324c6460473e52543caf1484f9cf876a9
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780650"
---
# <a name="promo-banner-module"></a>Promopalkkimoduuli

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään kampanjabannerimoduuleja ja niiden lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.

Kampanjabannerimoduuleja käytetään sivun sisäisten tietosanomien näyttämisessä. Niiden avulla voidaan näyttää koko sivustoa koskevia kampanjoita, jotka näkyvät kaikilla sähköisen kaupankäynnin sivuston sivuilla. 

Kampanjamoduulitmoduulit tukevat tekstisanomaa ja linkkiä. Jos kampanjabannerimoduuliin lisätään useita sanomia, siitä tulee kiertävä karusellibanneri, jossa asiakkaat voidaan kierrättää kaikki sanomat. 

Kampanjabannerimoduuleita ohjaavat sisällönhallintajärjestelmän (CMS) tiedot. Moduulit voidaan asettaa mille tahansa sivulle.

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a>Esimerkkejä kampanjabannerien käytöstä sähköisessä kaupankäynnissä

Kampanjabannereita voidaan käyttää sivuston ylätunnisteissa, jossa niissä voidaan näyttää koko sivustoa koskevia kampanjoita tai sanomia, kuten seuraavissa esimerkeissä.

Vuosittainen alennusmyynti loppuu 10 päivän kuluttua

Alennusmyynnit ennen koulujen alkamista. Osta nyt.

"Osta Kiitospäivän ALENNUSMYYNNISTÄ!" 

Seuraavassa kuvassa on esimerkki kampanjabannerista.

![Esimerkki kampanjabannerimoduulista.](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a>Kampanjabannerimoduulin ominaisuudet

| Ominaisuuden nimi             | Arvo                              | kuvaus |
|---------------------------|------------------------------------|-------------|
| Banneriviestit           | Teksti ja linkit                     | Teksti-ja linkkitaulukko |
| Automaattinen toisto                  | **Tosi** vai **Epätosi**              | Arvo, joka ilmaisee kierrätetäänkö sanomia automaattisesti, jos useita sanomia on määritetty. |
| Dian vaihtoväli | Millisekuntien (ms) määrä      | Aikaväli, jota käytetään sanomien kierrättämiseen. |
| Salli ohittaminen             | **Tosi** vai **Epätosi**              | Jos arvoksi on määritetty **Tosi**, asiakkaat voivat hylätä hälytyksen. |
| Näytä karusellin valitsin     | **Tosi** vai **Epätosi**              | Arvo, joka ilmaisee, näytetäänkö karusellin valitsimet, jotta asiakkaan voivat kierrättää useita bannerikohteita manuaalisesti. |
| Tekstin tasaus            | **Oikealla**, **vasemmalla** tai **keskellä** | Tekstin kohdistus kampanjabannerimoduulissa. |
| Linkitä                      | URL-osoite                              | Vapaavalintaisen linkin URL-osoite. |
|Tekstin tasaus             | **Oikealla**, **vasemmalla** tai **keskellä** | Tämä ominaisuus on käytettävissä teemalaajennuksena Adventure Works -teemassa. Sen avulla käyttäjä voi määrittää kampanjabannerin tekstin tasauksen. |

> [!IMPORTANT]
> Adventure Works -teema on käytettävissä Dynamics 365 Commerce -versiosta 10.0.20 eteenpäin.

## <a name="add-a-promo-banner-module-to-a-page"></a>Kampanjabannerimoduulin lisääminen sivulle 

Voit lisätä kampanjabannerimoduulin sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.
1. Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan **Mainosnauhan malli** ja valitse sitten **OK**.
1. Lisää **Oletussivu**-moduuli **Tekstiosa**-paikkaan **Sivun jäsennys** -kohdassa. 
1. Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen. 
1. Luo **Kampanjabannerisivu**-niminen sivu käyttämällä juuri luotua mallia. 
1. Lisää säilömoduuli uuden sivun **pääpaikkaan**. 
1. Määritä oikeassa ruudussa **Leveys**-arvoksi **Täytä säilö**.
1. Lisää kampanjabannerimoduuli säilömoduuliin **Sivun jäsennys** -kohdassa.
1. Lisää vähintään yksi bannerisanoma bannerimoduulin asetuksissa. Kussakin sanomassa voi olla tekstiä ja linkki. Voit mukauttaa moduulia entisestään muokkaamalla muita ominaisuuksia.
1. Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**. Sivun yläosassa pitäisi nyt olla hälytys, joka näyttää lisäämäsi tekstin.
1. Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.

> [!NOTE]
> Kampanjabanneria käytetään yleensä sivun ylätunniste- ja alaotsikkopaikassa.

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Karusellimoduuli](add-carousel.md)

[Tekstilohkomoduuli](add-content-rich-block.md)

[Sisältölohkomoduuli](add-hero-module.md)

[Videotoistinmoduuli](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
