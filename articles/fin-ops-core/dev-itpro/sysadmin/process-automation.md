---
title: Prosessien automatisointi
description: Tässä artikkelissa on tietoja siitä, miten prosessien automatisointi mahdollistaa eräpalvelimen käyttämien prosessien yksinkertaisen aikatauluttamisen.
author: RyanCCarlson2
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 1a1d152a01e0ebe6a20e2e6b31f12ed7b8deb024
ms.sourcegitcommit: 07ed6f04dcf92a2154777333651fefe3206a817a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2022
ms.locfileid: "9423956"
---
# <a name="process-automation"></a>Prosessien automatisointi

[!include[banner](../includes/banner.md)]

Prosessien automatisointi mahdollistaa eräpalvelimen käyttämien prosessien yksinkertaisen aikatauluttamisen. Ajoitetun työmäärän päivitetyn kalenterinäkymän avulla peruskäyttäjät voivat tarkastella ajoitettuja ja valmiita töitä sekä tehdä niihin liittyviä toimia.

## <a name="administration"></a>Hallinto

Kaikkien prosessien automatisointien keskitetty hallintasivu löytyy **Asetukset**-valikon Järjestelmänhallinta-moduulista. Tällä sivulla luetellaan kaikki järjestelmään määritetyt automaattiset prosessit (sarjat). Sen avulla voit myös lisätä uusia prosessiautomaatioita suoraan tältä sivulta. Kun sarja on määritetty, voit hallita kutakin sarjaa tästä luettelosta. Voit halutessasi muokata koko sarjaa, poistaa sen, tarkastella kaikkia luettelonäkymän esiintymiä tai poistaa sarjan käytöstä, jos haluat keskeyttää ajoitetun työn tietyksi aikaa. 

Käytä tämän sivun **Taustaprosessit**-välilehteä, jos haluat hallinnoida jotain ympäristössä suoritettavaa taustaprosessia. Valitse **Muokkaa**, jos haluat ajoittaa taustaprosessiin muutoksia. Muutoksia voivat olla lepotilajakso, jonka aikana prosessi "lepää", tai tauko suorituksessa tiettynä jaksona joka päivä. Valitse **Tarkastele viimeisimpiä tuloksia**, jos haluat tarkastella kunkin taustaprosessin suorituksen tuloksia.

Kaikki ominaisuuksien hallinnassa käytöstä poistetut prosessit eivät näy, kun toiminto on poistettu käytöstä. Lisäksi prosessiautomaation ajoitusmoduuli ei ajoita esiintymiä tai taustaprosesseja käytöstä poistetun ominaisuuden osalta. Kun ominaisuus otetaan uudelleen käyttöön, kaikki ajoitetut esiintymät tai taustaprosessit suoritetaan heti. Prosessin automatisoinnin ajoitusmoduuli käyttää suorituksessa järjestelmän erätyötä, **Prosessin automatisoinnin kyselyjärjestelmän työ**. Työtä ei saa muuttaa eikä peukaloida missään vaiheessa. Jos tätä erätyötä ei suoriteta tai sillä on virheellinen tila, valitse **Alusta prosessien automatisoinnit** ja nollaa erätyö. Nollaus varmistaa, että sovelluksen uudemmissa versioissa julkaistut uudet automaatiot alustetaan. 

## <a name="calendar-view"></a>Kalenterinäkymä

Yksi prosessin automaation tärkeimmistä eduista on mahdollisuus tarkastella ajoitettua työtä yksinkertaisessa kalenterinäkymässä.  Tämän näkymän avulla voit tarkastella töitä viikon kerrallaan. Tämä näkymä näkyy **Prosessin automatisointi** -sivun oikealla puolella. Valitun sarjan ajoitettu työmäärä täytetään. 

[![Prosessin automatisointikalenteri.](./media/CalendarView2.png)](./media/CalendarView2.png)

## <a name="occurrence-changes"></a>Esiintymän muutokset

Kutakin esiintymää voi muokata muuttamatta niiden sarjojen määrittämiä esiintymiä, jotka ovat peräisin niistä. Ajoitettujen töiden esiintymiä voi muokata kalenterinäkymästä valitsemalla **Näytä/Muokkaa**-painike ja valitsemalla sitten **Esiintymä**. Tämän sivun avulla voit käyttää kaikkia asetuksia, jotka on alun perin määritetty ohjatussa sarjan asennuksessa, ja antaa mahdollisuuden tehdä kertaluonteinen muutos valitulle esiintymälle. Ajoitettujen töiden esiintyminen voidaan poistaa käytöstä myös valitsemalla **Poista käytöstä** -painike kalenterinäkymästä.

## <a name="developer-documentation"></a>Kehitysdokumentaatio

Prosessin automaatiokehyksen avulla kehittäjät voivat laajentaa prosessin automaatiokehystä. [Prosessin automaatiokehys](../process-automation/process-automation-framework.md) -dokumentaatio sisältää tietoja siitä, miten voit luoda mukautettuja prosesseja, joita eräpalvelin suorittaa ajoitettuna ohjatun prosessin automatisoinnin avulla, ja tuoda ne näkyviin kalenterinäkymään automaattisesti.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
