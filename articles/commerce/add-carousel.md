---
title: Karusellimoduuli
description: Tässä ohjeaiheessa on tietoja karusellimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: c2c5adc8ab2e0330f7b07e5153fd8332ab0203e5
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785234"
---
# <a name="carousel-module"></a>Karusellimoduuli

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja karusellimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

## <a name="overview"></a>Yleiskatsaus

Karusellimoduulia käytetään useiden kampanjanimikkeiden sijoittamisessa karuselliin, jota asiakkaat voivat selata. Se on erityinen säilömoduuli, joka isännöi muita moduuleja. Esimerkiksi jälleenmyyjä voi käyttää aloitussivulla karusellimoduulia useiden uusien tuotteiden tai kampanjoiden esittelyyn.

Voit lisätä hero-ja ominaisuusmoduuleja karusellimoduulin sisälle. Karusellimoduulin ominaisuudet määrittävät, miten moduulit hahmonnetaan.

## <a name="examples-of-carousel-modules-in-e-commerce"></a>Esimerkkejä sähköisen kaupankäynnin karusellimoduuleista

- Karusellia, jossa on useita kampanjamoduuleja sisällä, voidaan käyttää aloitussivulla.
- Karusellia, jossa on useita kampanjamoduuleja sisällä, voidaan käyttää tuotetietosivulla.
- Karusellia voidaan käyttää millä tahansa markkinointisivulla useiden kampanjoiden tai tuotteiden markkinointia varten.

## <a name="carousel-module-properties"></a>Karusellimoduulin ominaisuudet

| Ominaisuuden nimi             | Arvo                                | Kuvaus |
|---------------------------|--------------------------------------|-------------|
| Automaattinen toisto                  | **Tosi** vai **Epätosi**                | Jos arvoksi on määritetty **Tosi**, karusellin nimikkeiden välinen siirtymä tapahtuu automaattisesti. Jos arvoksi on määritetty **Epätosi**, siirtyminen tapahtuu vain, jos asiakas siirtyy yhdestä nimikkeestä toiseen näppäimistön tai hiiren avulla. |
| Dian vaihtoväli | Arvo sekunteina                   | Nimikkeiden välisten siirtojen aikaväli. |
| Siirtymän animointi      | **Dia** tai **häivytys**                | Siirtymätehoste. |
| Leveys                     | **Sisällytä säilöön** tai **Täytä näyttö** | Jos arvoksi on määritetty **Sisällytä säilöön** karusellin sisällä olevat nimikkeet ovat korkeintaan karusellin levyisiä. Jos arvoksi on määritetty **Täytä näyttö**, karusellin leveys ei rajoita leveyttä, vaan nimikkeet voivat olla koko näytön levyisiä. Voit muuttaa arvoa halutun asettelun saavuttamiseksi. |

## <a name="add-a-carousel-module-to-a-page"></a>Karusellimoduulin lisääminen sivulle

Voit lisätä karusellimoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Luo sivumalli, jonka nimi on **Karusellimalli**.
1. Lisää karusellimoduuli oletussivun **pääpaikkaan**.
1. Lisää hero-moduuli karusellimoduuliin.
1. Lisää ominaisuusmoduuli karusellimoduuliin.
1. Kirjaa malli sisään ja julkaise se. 
1. Käytä juuri luotua karusellimallia, kun haluat luoda sivun nimeltä **Karusellisivu**.
1. Lisää karusellimoduuli uuden sivun **pääpaikkaan**.
1. Määritä karusellimoduulin **Leveys**-ominaisuudeksi **Täytä näyttö**. 
1. Määritä **Siirtymän animointi** -ominaisuuden arvoksi **Dia**.
1. Lisää hero-moduuli karusellimoduuliin.
1. Lisää hero-moduuliin kuva ja otsikko ja valitse **Tallenna**.
1. Lisää ominaisuusmoduuli karusellimoduuliin.
1. Lisää ominaisuusmoduuliin kuva, otsikko ja tekstikappale.
1. Tallenna ja esikatsele sivu. Sivulla pitäisi näkyä karuselli, jonka sisällä on kaksi moduulia (hero- ja ominaisuusmoduuli). Voit muuttaa karuselli-, hero- ja ominaisuusmoduulien lisäominaisuuksia halutun vaikutuksen aikaansaamiseksi.
1. Kirjaa sivu sisään ja julkaise se.

## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Hälytysmoduuli](add-alert.md)

[Sisällöntäyteinen lohkomoduuli](add-content-rich-block.md)

[Sisällönsijoittelumoduuli](add-content-placement-modules.md)

[Omaisuusmoduuli](add-feature-module.md)

[Hero-moduuli](add-hero-module.md)

[Videotoistinmoduuli](add-video-player.md)
