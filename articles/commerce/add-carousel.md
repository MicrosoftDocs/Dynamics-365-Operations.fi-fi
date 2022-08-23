---
title: Karusellimoduuli
description: Tässä artikkelissa on tietoja karusellimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 8bf9f7294dfbb4e16814dbdfb27bf646fcb5f4b1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275824"
---
# <a name="carousel-module"></a>Karusellimoduuli

[!include [banner](includes/banner.md)]

Tässä artikkelissa on tietoja karusellimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

Karusellimoduulia käytetään useiden kampanjanimikkeiden (mukaan lukien kuvat) sijoittamisessa kiertävään karusellibanneriin, jota asiakkaat voivat selata. Esimerkiksi jälleenmyyjä voi käyttää aloitussivulla karusellimoduulia useiden uusien tuotteiden tai kampanjoiden esittelyyn.

Voit lisätä sisältölohkomoduuleja karusellimoduulin sisälle. Karusellimoduulin ominaisuudet määrittävät, miten moduulit hahmonnetaan.

## <a name="examples-of-carousel-modules-in-e-commerce"></a>Esimerkkejä sähköisen kaupankäynnin karusellimoduuleista

- Karusellia, jossa on useita kampanjamoduuleja sisällä, voidaan käyttää aloitussivulla.
- Karusellia, jossa on useita kampanjamoduuleja sisällä, voidaan käyttää tuotetietosivulla.
- Karusellia voidaan käyttää millä tahansa markkinointisivulla useiden kampanjoiden tai tuotteiden markkinointia varten.

Seuraavassa kuvassa näkyy esimerkki karusellimoduulista, jota käytetään kotisivulla. Tämä karusellimoduuli sisältää useita sisältölohkon kohteita.

![Esimerkki karusellimoduulista.](./media/Hero.PNG)

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
