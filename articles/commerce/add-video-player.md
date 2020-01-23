---
title: Videotoistinmoduuli
description: Tässä ohjeaiheessa on tietoja videotoistinmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 12/02/2019
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
ms.openlocfilehash: 1c78583f39dbacdc7b38e89c33e67ae23731bf8a
ms.sourcegitcommit: 96bfc20eb748f4090a2b5e1ff9f54997d5a5d359
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/04/2019
ms.locfileid: "2885898"
---
# <a name="video-player-module"></a>Videotoistinmoduuli

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja videotoistinmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

## <a name="overview"></a>Yleiskatsaus

Videotoistinmoduuleja käytetään videoiden toistamisen tukemiseen. Myymälän aloituspaketissa on kaksi videotoistinmoduulia: ympäristön videotoistinmoduuli ja videotoistinmoduuli. Molemmat toistimet tukevat .mp4-mediatyyppiä.

## <a name="ambient-video-player-module"></a>Ympäristön videotoistinmoduuli

Ympäristön videotoistinmoduuli tukee lyhyitä tiedottavia videoita. Sitä tulisi käyttää videoissa, joiden pituus on alle viisi sekuntia. Tämä toistin tukee rajoitettuja videontoisto-ominaisuuksia, esimerkiksi toisto- ja pysäytystoimintoja.

### <a name="examples-of-ambient-video-player-modules-in-e-commerce"></a>Esimerkkejä ympäristön videotoistinmoduuleista sähköisessä kaupankäynnissä

- Lyhyet tiedottavat videot, joissa kerrotaan uusista tuotteista aloitussivulla
- Lyhyet tiedottavat videot, joissa kerrotaan tuoteominaisuuksista tuotetietosivulla

### <a name="ambient-video-player-module-properties"></a>Ympäristön videotoistinmoduulin ominaisuudet

| Ominaisuuden nimi     | Arvo                 | Kuvaus |
|-------------------|-----------------------|-------------|
| Automaattinen toisto          | **Tosi** vai **Epätosi** | Kun arvoksi on määritetty **Tosi**, videota toistetaan automaattisesti. |
| Vaimenna              | **Tosi** vai **Epätosi** | Kun arvoksi on määritetty **Tosi**, ääni on vaimennettu. Tämän toistimen oletusarvo on **Tosi**. Google Chrome -selaimessa automaattisen toiston videot vaimennetaan oletusarvoisesti. Ääni toistetaan vain, jos käyttäjä toistaa videon manuaalisesti. |
| Silmukka              | **Tosi** vai **Epätosi** | Kun arvoksi on määritetty **Tosi**, video toistetaan silmukassa. |
| Mediat             |  Videotiedostopolku ja -nimi | Videotiedosto, jota videotoistin toistaa. |
| Toiston säätimet | **Tosi** vai **Epätosi** | Kun arvoksi on asetettu **Tosi**, videossa näkyy toisto/pysäytys-painike. Jos arvoksi on määritetty **Epätosi**, toisto/pysäytys-painike ei näy, mutta käyttäjät voivat edelleen pysäyttää videon ja jatkaa sitä näppäimistön avulla. |

## <a name="video-player-module"></a>Videotoistinmoduuli

Videotoistinmoduulin avulla voit esitellä videoita sähköisen kaupankäynnin sivustossa. Se tukee kaikkia toisto-ominaisuuksia, kuten toistoa, pysäytystä, koko näytön tilaa ja tekstityksiä. Videotoistinmoduuli tukee myös tekstitysten mukauttamista Microsoftin helppokäyttötoimintojen standardien mukaisesti. Voit esimerkiksi mukauttaa fontin kokoa ja taustaväriä.

Videosoitinmoduuli tukee myös toissijaisia ääniraitoja. Kun video ladataan, myös toissijainen ääniraita voidaan ladata. Videosoitinmoduuli voi sitten toistaa toissijaisen ääniraidan, jos käyttäjä valitsee sen.

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
| Toiston säätimet     | **Tosi** vai **Epätosi**               | Kun arvoksi on asetettu **Tosi**, videossa näkyy toisto/pysäytys-painike. Jos arvoksi on määritetty **Epätosi**, toisto/pysäytys-painike ei näy, mutta käyttäjät voivat edelleen pysäyttää videon ja jatkaa sitä näppäimistön avulla. |
| Toista koko näyttössä       | **Tosi** vai **Epätosi**               | Kun arvoksi on määritetty **Tosi**, videota toistetaan koko näytön tilassa. |
| Ohjausobjektit              | **Tosi** vai **Epätosi**               | Kun arvoksi on määritetty **Tosi**, kaikki ohjausobjektit näkyvät. Näitä ohjausobjekteja ovat toisto- ja pysäytyspainikkeet, tilanneilmaisin ja tekstitykset. |
| Piilota julistekehys     | **Tosi** vai **Epätosi**               | Videossa voi olla julistekehys. Kun tämän ominaisuuden arvoksi määritetään **Tosi**, julistekehys piilotetaan. |
| Peitteen taso            | Numero väliltä **0**–**100** | Muoto, jota käytetään videon muotoiluun. |
| Koko näyttä -kuvakkeen tyyli | **Neliö** tai **nuoli**             | Videotoistimessa näkyvän Koko näyttö -kuvakkeen tyyli. |

## <a name="add-a-video-player-module-to-a-page"></a>Videotoistinmoduulin lisääminen sivulle

Voit lisätä videotoistinmoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Luo sivumalli, jonka nimi on **Videotoistinmalli**.
1. Lisää säilömoduuli oletussivun **pääpaikkaan**.
1. Lisää säilömoduulissa videotoistinmoduuli ja ympäristön videotoistinmoduuli.
1. Kirjaa malli sisään ja julkaise se.
1. Käytä juuri luotua videotoistinmallia, kun haluat luoda sivun nimeltä **Videotoistimen sivu**.
1. Lisää ympäristön videotoistinmoduuli uuden sivun **pääpaikkaan**.
1. Siirry ympäristön videotoistinmoduulin asetuksissa **Media**-kohtaan ja lataa videotiedosto. Voit muuttaa **Automaattinen toisto**-, **Silmukka**- ja muiden ominaisuuksien arvoa halutessasi.
1. Tallenna ja esikatsele sivu.
1. Lisää videotoistinmoduuli uuden sivun **pääpaikkaan**.
1. Siirry videotoistinmoduulin asetuksissa **Media**-kohtaan ja lataa videotiedosto.
1. Tallenna ja esikatsele sivu. Sivulla tulisi näkyä molemmat videomoduulit. Voit muokata kunkin moduulin toimintaa muuttamalla lisäasetuksia.
1. Kirjaa sivu sisään ja julkaise se.

## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Hälytysmoduuli](add-alert.md)

[Karusellimoduuli](add-carousel.md)

[Sisällöntäyteinen lohkomoduuli](add-content-rich-block.md)

[Sisällönsijoittelumoduuli](add-content-placement-modules.md)

[Omaisuusmoduuli](add-feature-module.md)

[Hero-moduuli](add-hero-module.md)
