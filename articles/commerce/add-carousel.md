---
title: Karusellimoduuli
description: Tässä ohjeaiheessa on tietoja karusellimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: f09f3f98d174f965a75e27ee6a5c2ed8599042fc
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411898"
---
# <a name="carousel-module"></a>Karusellimoduuli

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja karusellimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

## <a name="overview"></a>Yleiskatsaus

Karusellimoduulia käytetään useiden kampanjanimikkeiden (mukaan lukien kuvat) sijoittamisessa kiertävään karusellibanneriin, jota asiakkaat voivat selata. Esimerkiksi jälleenmyyjä voi käyttää aloitussivulla karusellimoduulia useiden uusien tuotteiden tai kampanjoiden esittelyyn.

Voit lisätä sisältölohkomoduuleja karusellimoduulin sisälle. Karusellimoduulin ominaisuudet määrittävät, miten moduulit hahmonnetaan.

## <a name="examples-of-carousel-modules-in-e-commerce"></a>Esimerkkejä sähköisen kaupankäynnin karusellimoduuleista

- Karusellia, jossa on useita kampanjamoduuleja sisällä, voidaan käyttää aloitussivulla.
- Karusellia, jossa on useita kampanjamoduuleja sisällä, voidaan käyttää tuotetietosivulla.
- Karusellia voidaan käyttää millä tahansa markkinointisivulla useiden kampanjoiden tai tuotteiden markkinointia varten.

Seuraavassa kuvassa näkyy esimerkki karusellimoduulista, jota käytetään kotisivulla. Tämä karusellimoduuli sisältää useita sisältölohkon kohteita.

![Esimerkki karusellimoduulista](./media/Hero.PNG)

## <a name="carousel-module-properties"></a>Karusellimoduulin ominaisuudet

| Ominaisuuden nimi             | Arvo                 | kuvaus |
|---------------------------|-----------------------|-------------|
| Automaattinen toisto                  | **Tosi** vai **Epätosi** | Jos arvoksi on määritetty **Tosi**, karusellin nimikkeiden välinen siirtymä tapahtuu automaattisesti. Jos arvoksi on määritetty **Epätosi**, siirtyminen tapahtuu vain, jos asiakas siirtyy yhdestä nimikkeestä toiseen näppäimistön tai hiiren avulla. |
| Dian vaihtoväli | Arvo sekunteina    | Nimikkeiden välisten siirtojen aikaväli. |
| Siirtymätyyppi           | **Dia** tai **häivytys** | Nimikkeiden välinen siirtymistehoste. |
| Piilota karusellin valitsin     | **Tosi** vai **Epätosi** | Jos arvoksi on määritetty **Tosi**, karusellin valitsin ja järjestyksen osoitin piilotetaan. |
| Salli karusellin ohittaminen    | **Tosi** vai **Epätosi** | Jos arvoksi on määritetty **Tosi**, käyttäjät voivat ohittaa karusellin. |

## <a name="add-a-carousel-module-to-a-page"></a>Karusellimoduulin lisääminen sivulle

Voit lisätä karusellimoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.
1. Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan **Karusellimalli** ja valitse sitten **OK**.
1. Lisää **Teksti**-paikkaan **Oletussivu**-moduuli.
1. Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen.  
1. Käytä juuri luotua karusellimallia, kun haluat luoda sivun nimeltä **Karusellisivu**.
1. Lisää säilömoduuli uuden sivun **pääpaikkaan**. 
1. Määritä oikeassa ruudussa **Leveys**-arvoksi **Täytä näyttö**.
1. Lisää karusellimoduuli säilömoduuliin **Sivun jäsennys** -kohdassa.
1. Lisää sisältölohko karusellimoduuliin. Määritä sisältölohkomoduuliin ominaisuudet antamalla **Otsikko**-, **Linkki**-, **Asettelu**- ja muut ominaisuudet.
1. Lisää ja määritä toinen sisältölohkomoduuli.
1. Määritä karusellimoduulin lisäominaisuudet tarpeen mukaan.
1. Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**. Sivulla pitäisi näkyä karuselli, jonka sisällä on kaksi moduulia (hero- ja ominaisuusmoduuli). Voit muuttaa karuselli-, hero- ja ominaisuusmoduulien lisäominaisuuksia halutun vaikutuksen aikaansaamiseksi.
1. Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Promopalkkimoduuli](add-alert.md)

[Tekstilohkomoduuli](add-content-rich-block.md)

[Sisältölohkomoduuli](add-hero-module.md)

[Videotoistinmoduuli](add-video-player.md)
