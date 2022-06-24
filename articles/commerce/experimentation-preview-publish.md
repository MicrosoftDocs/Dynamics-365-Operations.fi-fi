---
title: Kokeen esikatselu ja julkaisu
description: Tässä artikkelissa käsitellään kokeen esikatselua ja julkaisua Dynamics 365 Commercessa.
author: sushma-rao
ms.date: 06/08/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 5da7a4e3c17057278d02ebd45702d1de404f0dc6
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946129"
---
# <a name="preview-and-publish-an-experiment"></a>Kokeen esikatselu ja julkaisu

Tässä artikkelissa käsitellään kokeen esikatselua ja julkaisua Dynamics 365 Commercessa sen jälkeen, kun [koe on yhdistetty ja variaatiot muokattu](experimentation-connect-edit.md). Seuraavassa kaaviossa on kaikki vaiheet, jotka sisältyvät kokeen määrittämiseen ja suorittamiseen sähköisessä kaupankäyntisivustossa Dynamics 365 Commercessa. Muut vaiheet käsitellään erillisissä artikkeleissa.

[ ![Kokeilun käyttäjän siirtymä – esikatselu ja julkaisu.](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)

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

### <a name="force-variations-for-testing"></a>Testin variaatioiden pakotus

Kun kokeilu on live-tilassa, voit liittää koetunnuksen ja variaatiotunnuksen sivun oletus-URL-osoitteeseen ja pakottaa variaatiot testausta tai automaatiota varten. Jos sivun oletus-URL-osoite on esimerkiksi `https://fabrikam.com/modern/homepage`, voit pakottaa variaation URL-osoitteella kuten `https://fabrikam.com/modern/homepage?exp=18012910471|18024360464`. Voit saada kokeilutunnuksen ja variaatiotunnuksen edellä selitettyä esikatselukokemusta varten esiversio-URL-osoitteesta edellä selitetystä **Esiversio**-kokemuksesta.

## <a name="previous-step"></a>Edellinen vaihe
[Kokeilun yhdistäminen ja muokkaaminen](experimentation-connect-edit.md)

## <a name="next-step"></a>Seuraava vaihe
[Kokeilun suoritus ja seuranta](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
