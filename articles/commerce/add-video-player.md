---
title: Videotoistinmoduuli
description: Tässä ohjeaiheessa on tietoja videotoistinmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e94658eed12b12d6666e63d2c06b86646c81a120
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025642"
---
# <a name="video-player-module"></a>Videotoistinmoduuli


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja videotoistinmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

## <a name="overview"></a>Yleiskatsaus

Videotoistinmoduulia käytetään tukemaan videotoistoa. Se voidaan lisätä mille tahansa sivulle, kunhan videosisältö on ladattu ja käytettävissä sisällönhallintajärjestelmässä (CMS). Videotoistinmoduuli tukee .mp4-mediatyypin.

## <a name="video-player-module"></a>Videotoistinmoduuli

Videotoistinmoduulin avulla voit esitellä videoita sähköisen kaupankäynnin sivustossa. Se tukee kaikkia toisto-ominaisuuksia, kuten toistoa, pysäytystä, koko näytön tilaa, äänikuvauksia ja tekstityksiä. Videotoistinmoduuli tukee myös tekstitysten mukauttamista Microsoftin helppokäyttötoimintojen standardien mukaisesti. Voit esimerkiksi mukauttaa fontin kokoa ja taustaväriä.

Videosoitinmoduuli tukee myös toissijaisia ääniraitoja. Kun video ladataan CMS-järjestelmään, myös toissijainen ääniraita voidaan ladata. Videosoitinmoduuli voi sitten toistaa toissijaisen ääniraidan, jos käyttäjä valitsee sen.

### <a name="examples-of-video-player-modules-in-e-commerce"></a>Esimerkkejä videotoistinmoduuleista sähköisessä kaupankäynnissä

- Tuotetietosivujen tai markkinointisivujen ohjevideot
- Markkinointisivuilla olevat käytäntöjä koskevat kampanjavideot tai videot
- Markkinointivideot, joissa kerrotaan tuotteen ominaisuuksista tuotetietosivuilla tai markkinointisivuilla

### <a name="video-player-module-properties"></a>Videotoistinmoduulin ominaisuudet

| Ominaisuuden nimi         | Arvo                               | Kuvaus |
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

1. Luo sivumalli, jonka nimi on **Videotoistinmalli**.
1. Lisää säilömoduuli oletussivun **pääpaikkaan**.
1. Lisää säilömoduulissa videotoistinmoduuli ja ympäristön videotoistinmoduuli.
1. Kun mallin muokkaus on valmis, julkaise se.
1. Käytä luotua videotoistinmallia, kun haluat luoda sivun nimeltä **Videotoistimen sivu**.
1. Lisää videotoistinmoduuli uuden sivun **pääpaikkaan**.
1. Valitse videotoistinmoduulin ominaisuusruudussa **Lisää video**.
1. Valitse **Mediavalitsin**-valintaikkunassa video ja valitse sitten **Lataa uusi medianimike**.
1. Tallenna ja esikatsele sivu. Videomoduulin pitäisi näkyä sivulla. Voit muokata moduulin toimintaa muuttamalla lisäasetuksia.
1. Kun sivun muokkaus on valmis, julkaise se.

## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Kampanjabannerimoduuli](add-alert.md)

[Karusellimoduuli](add-carousel.md)

[Tekstilohkomoduuli](add-content-rich-block.md)

[Sisältölohkomoduuli](add-hero-module.md)
