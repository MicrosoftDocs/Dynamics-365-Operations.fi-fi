---
title: Kokeen esikatselu ja julkaisu
description: Tässä ohjeaiheessa käsitellään kokeen esikatselua ja julkaisua Dynamics 365 Commercessa.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: f1a565917ab7a048d4d455bc0a0fbd9316237aeb
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/22/2020
ms.locfileid: "4412109"
---
# <a name="preview-and-publish-an-experiment"></a>Kokeen esikatselu ja julkaisu

Tässä ohjeaiheessa käsitellään kokeen esikatselua ja julkaisua Dynamics 365 Commercessa sen jälkeen, kun [koe on yhdistetty ja variaatiot muokattu](experimentation-connect-edit.md). Seuraavassa kaaviossa on kaikki vaiheet, jotka sisältyvät kokeen määrittämiseen ja suorittamiseen sähköisessä kaupankäyntisivustossa Dynamics 365 Commercessa. Muut vaiheet käsitellään erillisissä ohjeaiheissa.

[ ![Kokeilun käyttäjän siirtymä – esikatselu ja julkaisu](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)

## <a name="preview-your-experiment-variations"></a>Kokeen variaatioiden esikatselu
Voit esikatsella variaatioita ja jatkaa niiden muokkausta, kunnes olet tyytyväinen niiden ulkoasuun.

Koevariaatioita voi esikatsella Commercen sivustonmuodostimessa seuraavasti:

1. Valitse komentopalkin alapuolella olevassa avattavassa variaatiovalikossa esikatseltava sisältö. 
1. Valitse komentopalkissa **Esikatsele**. Esikatselussa nähdään, miltä sisältö näyttää julkaistuna.
1. Jos haluat esikatsella toisen variaation, valitse se avattavasta variaatiovalikosta ja valitse sitten **Esikatselu** uudelleen.

## <a name="publish-your-experiment"></a>Kokeen julkaiseminen
Jos et käytä julkaisuryhmää aikatauluttamiseen, kun koe siirtyy live-tilaan ja haluat julkaista heti, valitse komentopalkissa **Julkaisu**. Kaikki kokeeseen kuuluvat variaatiot julkaistaan.
    
> [!IMPORTANT]
> Jos sivulla on julkaisematon URL-osoite, URL-osoite on ensin julkaistava tai se ei näy sivuston käyttäjille. Lisätietoja kohdassa [Sivun tallentaminen, esikatseleminen ja julkaiseminen](save-preview-publish-page.md).
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a>Kokeen live-tilaan siirtämisen aikatauluttaminen julkaisuryhmien avulla
Sivustonmuodostimessa luodut variaatiot voidaan aikatauluttaa julkaistaviksi käyttämällä julkaisuryhmää. Sivun tai osan voi yhdistää julkaisuryhmässä kokeeseen valitsemalla vasemmassa siirtymisruudussa **Kokeet**. Se on mahdollista myös valitsemalla **Sivut** tai **Osat** ja noudattamalla ohjeita kohdassa [Kokeen yhdistäminen ja variaatioiden muokkaaminen](experimentation-connect-edit.md). Lisätietoja julkaisuryhmistä on kohdassa [Julkaisuryhmien kanssa työskenteleminen](publish-groups.md).

Kun julkaisuryhmiä käytetään kokeissa, tietyt tärkeät seikat on otettava huomioon.
- Kun sivu tai osa, jossa koe on käynnissä, lisätään julkaisuryhmään, koe poistetaan julkaisuryhmän sivulta tai osasta.
- Live-sivuston sivuihin yhdistetyt kokeet eivät ole käytettävissä julkaisuryhmien sivulla ja päin vastoin. Vastaavasti sivut, joissa on live-sivustossa käytössä olevia kokeita, eivät ole muiden kokeiden käytettävissä julkaisuryhmissä ja päin vastoin.
- Kun julkaiset tai aikataulutat julkaisuryhmän, koko julkaisuryhmän sisältö julkaistaan riippumatta siitä, onko julkaisuryhmään liitetty koe vai ei.
- Koska julkaisuryhmä jää pysyväksi, kun se on julkaistu live-sivustoon, myös julkaisuryhmässä olevat kokeet jäävät pysyviksi. Tämän vuoksi muita kokeita voi liittää samalla sivulla tai samassa ryhmässä. Tämä rajoitus voidaan välttää poistamalla kaikki julkaisuryhmät, joissa on pysyviä kokeita. Jos vastaavasti poista kokeen live-sivustossa, joka on myös julkaisuryhmässä, poista se ensin julkaisuryhmästä.

## <a name="previous-step"></a>Edellinen vaihe
[Kokeilun yhdistäminen ja muokkaaminen](experimentation-connect-edit.md)

## <a name="next-step"></a>Seuraava vaihe
[Kokeen suorittaminen ja seuranta](experimentation-run-monitor.md)
