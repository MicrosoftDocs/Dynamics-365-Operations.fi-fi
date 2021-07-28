---
title: Kokeilut Dynamics 365 Commercessa
description: Kokeilujen avulla voidaan luoda, muokata ja hallita sivun asettelua ja sisältökäsittelyjä sivustonmuodostimessa. Kattava kokeilutuki on otettu käyttöön sähköisissä kaupankäyntisivuissa ja sivulla olevissa kohteissa.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 658396e87b3007216f6fa11c6ad3923daeb8a67d
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349325"
---
# <a name="experimentation-in-dynamics-365-commerce"></a>Kokeilut Dynamics 365 Commercessa
Dynamics 365 Commercen kokeilujen avulla voi vahvistaa sähköisten kaupankäyntisivujen tehokkuutta koskevia hypoteeseja ja tehdä tietoihin perustuvia päätöksiä. Commerce tukee sivujen, moduulien ja osien A/B-testausta sekä antaa mahdollisuuden mitata sivustoon ehdotettujen muutosten vaikutusta.

Voit luoda, muokata ja hallita käsiteltyä sivua ja sisältöä eli **variaatioita** Commercen sivustonmuodostimessa. Commerce integroituu kolmannen osapuolen palveluihin, joilla voidaan luoda kokeita ja käsittelytehtäviä. Commercen tallentamien reaaliaikaisten tapahtumavirtojen avulla voidaan käyttää analytiikkaa, joka määrittää koetulokset kolmannen osapuolen palvelussa. Voit sitten käyttää näitä analyyseja hypoteesiin tukena tai sen kumoamiseen.

## <a name="set-up-prerequisites"></a>Määritä edellytykset
1. **Hanki Commercen oikea versio** – Päivitä moduulikirjasto, verkkokanavan laajennettavuuden SDK ja Commerce Scale Unit Commercen versioon 10.0.13 tai sitä uudempaan versioon.
1. **Määritä kokeilun yhdistin** – Commercen voi muodostaa yhteyden kokeilun yhdistimen avulla kolmannen osapuolen palveluun, jossa se noutaa koeluettelon ja määrittää, milloin koe näytetään käyttäjälle. Voit ostaa kolmannen osapuolen yhdistimen [AppSourcesta](https://appsource.microsoft.com). Noudata julkaisijan asennusohjeita. Vaihtoehtoisesti voit käyttää Commercen näytetestiyhdistintä kokeilutyönkalun testaamiseen ilman ulkoisen palvelun määrittämistä. Lisätietoja on kohdassa [Yhdistimien määrittäminen ja ottaminen käyttöön](e-commerce-extensibility/connectors.md). 
1. **Ota kokeilutoiminnon merkinnät käyttöön Commercessa** – Voit ottaa kokeilun käyttöön vuokraajatasolla valitsemalla **Vuokraajan asetukset > Ominaisuudet** tai sivustotasolla valitsemalla **Sivuston asetukset > Ominaisuudet**.
    - Ottamalla **Kokeilu**-merkinnän käyttöön voit luoda sivulle moduulin kokeiluvariaatioita ilman, että se vaikuttaa sisältöön, joka ei ole kokeilun osan, tai että kyseinen sisältö olisi kopioitava. Näin varmistetaan, että kokeilun ulkopuolella tehtävät sisältöpäivitykset pysyvät synkronoituna kokeilun elinkaaren aikana. Jos tämä merkintä poistetaan käytöstä, käyttäjät eivät näe mitään kokeiluja ja kaikki muokkaustoiminnot poistetaan sivustonmuodostimessa.
    - Ottamalla **Kokeilu sivuilla tai osilla** -merkinnän käyttöön voit suorittaa kokeiluja sivulla tai osassa. Näin luodaan täydellinen esiintymäkopio kaikkien sivulla tai osassa olevien moduulien koko sivusta tai osasta. Käytä tätä tilaa, kun haluat testata kattavia sisältömuutoksia, tai silloin, kun sisältömuutosten synkronoinnilla esiintymien välillä ei ole merkitystä. Tämän merkinnän poistaminen käytöstä estää uusien kokeiden luonnin tai muokkauksen sivuilla tai osissa.
    > [!NOTE]
    > **Kokeilu**-merkintä on lisäksi oltava käytössä, jotta **Koe sivulla tai osissa** -toimi toimisi.
    
## <a name="experimentation-lifecycle"></a>Kokeilun elinkaari
Kokeen määrittäminen, variaatioiden luominen ja kokeen suorittaminen on iteratiivinen prosessi. Seuraavassa kaaviossa näkyy kokeilun elinkaari Commercessa ja kolmannen osapuolen palvelussa. 

[ ![Kokeilun elinkaari.](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)

Lisätietoja kokeiluprosessin kustakin vaiheesta on seuraavissa ohjeaiheissa:
- [Kokeilun hypoteesin ja mittarien määrittäminen](experimentation-identify.md)
- [Kokeilun määrittäminen](experimentation-setup.md)
- [Kokeilun yhdistäminen ja muokkaaminen](experimentation-connect-edit.md)
- [Kokeilun esikatselu ja julkaisu](experimentation-preview-publish.md)
- [Kokeen suorittaminen ja seuranta](experimentation-run-monitor.md)
- [Muunnelman määrittäminen ja kokeilun viimeistely](experimentation-review-complete.md)

> [!NOTE]
> Kokeen elinkaaren vaiheen voi tarkistaa sivustonmuodostimen vasemman siirtymisruudun **Kokeet**-kohdassa. Kokeiluluettelossa on kunkin kokeen tila sekä Commercessa ja kolmannen osapuolen palvelussa. Lisätietoja on kohdassa [Kokeilun tilan tarkistaminen](experimentation-status.md).

## <a name="next-step"></a>Seuraava vaihe
[Hypoteesin ja kokeen onnistumismittareiden määrittäminen](experimentation-identify.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]