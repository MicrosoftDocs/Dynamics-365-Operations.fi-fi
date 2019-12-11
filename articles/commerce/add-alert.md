---
title: Hälytysmoduuli
description: Tässä ohjeaiheessa on tietoja hälytysmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
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
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785349"
---
# <a name="alert-module"></a>Hälytysmoduuli

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja hälytysmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

## <a name="overview"></a>Yleiskatsaus

Hälytysmoduulia käytetään sivun sisäisten tietosanomien näyttämisessä. Hälytysmoduulit tukevat tekstisanomaa ja linkkiä. Niiden avulla voidaan näyttää koko sivustoa koskevia kampanjoita, jotka näkyvät kaikilla sähköisen kaupankäynnin sivuston sivuilla. 

Hälytysmoduuleita ohjaavat sisällönhallintajärjestelmän (CMS) tiedot. Moduulit voidaan asettaa mille tahansa sivulle.

## <a name="examples-of-alert-modules-in-e-commerce"></a>Esimerkkejä sähköisen kaupankäynnin hälytysmoduuleista

Hälytysmoduuleja voidaan käyttää sivuston ylätunnisteessa osoittamaan koko sivustoa koskevia kampanjoita tai sanomia. Seuraavassa on muutamia esimerkkejä:

Vuosittainen alennusmyynti loppuu 10 päivän kuluttua

Alennusmyynnit ennen koulujen alkamista. Osta nyt.

## <a name="alert-module-properties"></a>Hälytysmoduulin ominaisuudet

| Ominaisuuden nimi  | Arvo                              | Kuvaus |
|----------------|------------------------------------|-------------|
| Teksti           | Teksti                               | Hälytysmoduulissa näkyvä tekstisanoma. |
| Tekstin tasaus | **Oikealla**, **vasemmalla** tai **keskellä** | Arvo, joka määrittää, miten teksti tasataan hälytysmoduulissa. |
| Hylkää hälytys  | **Tosi** vai **Epätosi**              | Jos arvoksi on määritetty **Tosi**, asiakas voi hylätä hälytyksen. |
| Linkitä           | URL-osoite                                | Vapaavalintaisen linkin URL-osoite. |

## <a name="add-an-alert-module-to-a-page"></a>Hälytysmoduulin lisääminen sivulle 

Voit lisätä hälytysmoduulin sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Luo sivumalli, jonka nimi on **Hälytysmalli**.
1. Lisää hälytysmoduuli oletussivun **pääpaikkaan**.
1. Kirjaa malli sisään ja julkaise se. 
1. Käytä juuri luotua hälytysmallia, kun haluat luoda sivun nimeltä **Hälytyssivu**. 
1. Lisää hälytysmoduuli uuden sivun **pääpaikkaan**.
1. Syötä hälytysteksti hälytysmoduulin asetuksiin. Voit muokata muita ominaisuuksia, jos haluat mukauttaa hälytysmoduulia lisää.
1. Tallenna ja esikatsele sivu. Sivun yläosassa pitäisi nyt olla hälytys, joka sisältää lisäämäsi tekstin.
1. Kirjaa sivu sisään ja julkaise se. 

## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Karusellimoduuli](add-carousel.md)

[Sisällöntäyteinen lohkomoduuli](add-content-rich-block.md)

[Sisällönsijoittelumoduuli](add-content-placement-modules.md)

[Omaisuusmoduuli](add-feature-module.md)

[Hero-moduuli](add-hero-module.md)

[Videotoistinmoduuli](add-video-player.md)
