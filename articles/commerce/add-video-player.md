---
title: Videotoistinmoduuli
description: Tässä ohjeaiheessa on tietoja videotoistinmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: aa1efa6ce959439c49983553edfaf247c8e8dcd5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797404"
---
# <a name="video-player-module"></a>Videotoistinmoduuli

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja videotoistinmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

Videotoistinmoduulia käytetään tukemaan videotoistoa. Se voidaan lisätä mille tahansa sivulle, kunhan videosisältö on ladattu ja käytettävissä sisällönhallintajärjestelmässä (CMS). Videotoistinmoduuli tukee .mp4-mediatyypin.

## <a name="video-player-module"></a>Videotoistinmoduuli

Videotoistinmoduulin avulla voit esitellä videoita sähköisen kaupankäynnin sivustossa. Se tukee kaikkia toisto-ominaisuuksia, kuten toistoa, pysäytystä, koko näytön tilaa, äänikuvauksia ja tekstityksiä. Videotoistinmoduuli tukee myös tekstitysten mukauttamista Microsoftin helppokäyttötoimintojen standardien mukaisesti. Voit esimerkiksi mukauttaa fontin kokoa ja taustaväriä.

Videosoitinmoduuli tukee myös toissijaisia ääniraitoja. Kun video ladataan CMS-järjestelmään, myös toissijainen ääniraita voidaan ladata. Videosoitinmoduuli voi sitten toistaa toissijaisen ääniraidan, jos käyttäjä valitsee sen.

### <a name="examples-of-video-player-modules-in-e-commerce"></a>Esimerkkejä videotoistinmoduuleista sähköisessä kaupankäynnissä

- Tuotetietosivujen tai markkinointisivujen ohjevideot
- Markkinointisivuilla olevat käytäntöjä koskevat kampanjavideot tai videot
- Markkinointivideot, joissa kerrotaan tuotteen ominaisuuksista tuotetietosivuilla tai markkinointisivuilla

Seuraavassa kuvassa on esimerkki videotoistinmoduulista kotisivulla.

![Esimerkki videotoistinmoduulista](./media/ecommerce-videoplayer.PNG)

### <a name="video-player-module-properties"></a>Videotoistinmoduulin ominaisuudet

| Ominaisuuden nimi         | Arvo                               | kuvaus |
|-----------------------|-------------------------------------|-------------|
| Automaattinen toisto             | **Tosi** vai **Epätosi**               | Kun arvoksi on määritetty **Tosi**, videota toistetaan automaattisesti. |
| Vaimenna                  | **Tosi** vai **Epätosi**               | Kun arvoksi on määritetty **Tosi**, ääni on vaimennettu. Tämän toistimen oletusarvo on **Epätosi**. Chrome-selaimessa automaattisen toiston videot vaimennetaan oletusarvoisesti. Ääni toistetaan vain, jos käyttäjä toistaa videon manuaalisesti. |
| Silmukka                  | **Tosi** vai **Epätosi**               | Kun arvoksi on määritetty **Tosi**, video toistetaan silmukassa. |
| Mediat                 | Videotiedostopolku ja -nimi | Videotiedosto, jota videotoistin toistaa. |
| Toista koko näyttössä       | **Tosi** vai **Epätosi**               | Kun arvoksi on määritetty **Tosi**, videota toistetaan koko näytön tilassa. |
| Toiston/keskeytyksen valitsin    | **Tosi** vai **Epätosi**               | Kun arvoksi on asetettu **Tosi**, videossa näkyy toisto/pysäytys-painike. |
| Videosoittimen säätimet | **Tosi** vai **Epätosi**               | Kun arvoksi on määritetty **Tosi**, kaikki videotoistimen ohjausobjektit näkyvät. Näitä ohjausobjekteja ovat toisto- ja pysäytyspainikkeet, tilanneilmaisin ja tekstitysvaihtoehdot. |
| Piilota julistekuva     | **Tosi** vai **Epätosi**               | Videossa voi olla julistekehys. Kun tämän ominaisuuden arvoksi määritetään **Tosi**, julistekehys piilotetaan. |
| Peitteen taso            | Numero väliltä **0**–**100** | Muoto, jota käytetään videon muotoiluun. |

## <a name="add-a-video-player-module-to-a-page"></a>Videotoistinmoduulin lisääminen sivulle

> [!NOTE] 
> Video on ennen videotoistinmoduulin luontia ladattava mediakirjastoon.

Voit lisätä videotoistinmoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.
1. Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan **Videotoistimen malli** ja valitse sitten **OK**.
1. Valitse kolme pistettä (**...**) **Tekstiosa**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Oletussivu**-moduuli ja valitse sitten **OK**.
1. Valitse **Oletussivu**-moduulin **Pää**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.
1. Valitse kolme pistettä (**...**) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Videotoistin**-moduuli ja valitse sitten **OK**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**. 
1. Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.
1. Valitse **Valitse malli** -valintaikkunassa luomasi videotoistimen malli. Kirjoita **Sivun nimi** -kohtaan **Videotoistinsivu** ja valitse sitten **OK**.
1. Valitse uudella sivulla **Pää**-paikka. Valitse kolmen pisteen painike (**…**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.
1. Valitse kolme pistettä (**...**) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Videotoistin**-moduuli ja valitse sitten **OK**.
1. Valitse videotoistinmoduulin ominaisuusruudussa **Lisää video**.
1. Valitse **Mediavalitsin**-valintaikkunassa video ja valitse sitten **Lataa uusi medianimike**.
1. Valitse Resurssienhallinnassa videotiedosto ja valitse sitten **Avaa**.
1. Kirjoita **Lataa mediakohde** -valintaikkunaan otsikko ja muut tarvittavat tiedot ja valitse sitten **OK**.
1. Valitse **Mediavalitsin**-valintaikkunassa **Sulje**.
1. Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**. Videomoduulin pitäisi näkyä sivulla. Voit muokata moduulin toimintaa muuttamalla lisäasetuksia.
1. Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen. 

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Promopalkkimoduuli](add-alert.md)

[Karusellimoduuli](add-carousel.md)

[Tekstilohkomoduuli](add-content-rich-block.md)

[Sisältölohkomoduuli](add-hero-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]