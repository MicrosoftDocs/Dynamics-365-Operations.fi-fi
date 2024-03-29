---
title: Viiveet
description: Tässä artikkelissa on tietoja pääsuunnittelun viivästyspäivistä. Viivästyspäivä on realistinen eräpäivä, jonka tapahtuma saa, jos pääsuunnittelun laskema aikaisin toimituspäivä on myöhempi kuin pyydetty päivämäärä.
author: t-benebo
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e7e0150e40193f2f799677ad19cae2ea589afc0
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740627"
---
# <a name="delays"></a>Viiveet

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja pääsuunnittelun viivästyspäivistä. Viivästyspäivä on realistinen eräpäivä, jonka tapahtuma saa, jos pääsuunnittelun laskema aikaisin toimituspäivä on myöhempi kuin pyydetty päivämäärä.

Pääsuunnittelu voi laskea tapahtumalle aikaisimman täyttymispäivämäärän läpimenoaikojen, materiaalin saatavuuden ja suunnittelun erilaisten parametrien perusteella. 

Jos pääsuunnittelu laskee tilauspäivämäärän, joka on aiempi kuin kuluva päivämäärä, tilausta ei voi täyttää ajoissa. Tämän vuoksi tilaus viivästyy. Tässä tapauksessa pääsuunnittelu suunnittelee tilauksen edelleen kuluvasta päivämäärästä ja sisällyttää läpimenoajat. Läpimenoajat lasketaan alatason osanimikkeistä alkaen. Tämän jälkeen tilaukselle määritetään viivästyspäivä. Viivästyspäivä on nykyisiin tietoihin perustuva realistinen eräpäivä. Pääsuunnittelu laskee myös viivästymispäivien määrän. 

Joissakin tilanteissa viivästyspäivää ei välttämättä käytetä. Näin voi käydä esimerkiksi silloin, kun käyttäjät tietävät voivansa jouduttaa läpimenoaikoja valitsemalla vaihtoehtoisen toimitustavan. 

Voit määrittää kattavuusryhmän viivästysten laskentatavat. Voit liittää kattavuusryhmän nimikkeeseen myöhemmin. 

**Pääsuunnittelun parametrit** -sivulla voit määrittää viivästymisten laskennan aloitusajan. Jos tilaus täyttyy tämän jälkeen, tilauksen viivästyspäivään lisätään yksi päivä. 

> [!NOTE]
> Aiemmissa versioissa laskettuja viiveitä kutsuttiin *viivästyssanomiksi*, viivästyspäivää *viivästyspäiväksi* ja viivästynyttä tapahtumaa *tulevaisuuteen määritetyksi tapahtumaksi*.

## <a name="limited-delays-in-production-setup-with-multiple-bom-levels"></a>Tuotantoasetusten rajoitetut viiveet useilla tuoterakennetasoilla
Kun käsittelet useita tuoterakennetasoja sisältävien tuotantomääritysten viiveitä, on tärkeää huomata, että vain suoraan nimikkeen yläpuolella (tuoterakennerakenteessa) olevat nimikkeet, jotka aiheuttavat viivästyksen, päivitetään viiveellä osana pääsuunnittelun ajoaikaa. Muut tuoterakennerakenteen nimikkeet eivät saa sitä viivettä, jota käytetään, ennen kuin ensimmäinen pääsuunnittelu suoritetaan, kun ylimmän tason suunniteltu tilaus hyväksytään tai vahvistetaan. 

Voit välttää tämän tunnetun rajoituksen valitsemalla tuoterakennerakenteen yläosassa olevat tuotantotilaukset, joiden viiveet on hyväksytty (tai vahvistettu) ennen seuraavaa pääsuunnitteluajoa. Näin viivästyneen hyväksytyn suunnitellun tuotantotilauksen viivästyminen säilytetään ja kaikki pohjana olevat komponentit päivitetään vastaavasti.
Toimenpidesanomien avulla voidaan myös tunnistaa suunnitellut tilaukset, jotka voidaan siirtää myöhempään päivään tuoterakennerakenteen muiden viivästysten vuoksi.

## <a name="desired-date"></a>Haluttu päivämäärä

**Suunniteltu tilaus** -sivulta **Viiveitä** -välilehdeltä löytyy **Haluttu päivämäärä** suunnitellulle tilaukselle. Suunnitellun tilauksen haluttu päivämäärä on viivästysten peruspäivä, joka on laskettu päivämäärä, joka vastaa **Vaadittua päivämäärää**, joka on laskettu kohteesta **Nettotarve**. Jos suunniteltu tilaus on Tuoterakenteen tuotantorivi tai kanban-rivi, kyseinen päivämäärä perustuu **Tarvepäivään** ja haluttua päivää ei näytetä **suunnitellun tilauksen** sivulla.

## <a name="additional-resources"></a>Lisäresurssit

- [Kattavuusasetukset](coverage-settings.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]