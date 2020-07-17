---
title: Prosessien automatisointi
description: Tässä ohjeaiheessa on tietoja siitä, miten prosessien automatisointi mahdollistaa eräpalvelimen käyttämien prosessien yksinkertaisen aikatauluttamisen.
author: RyanCCarlson2
manager: tonyafehr
ms.date: 06/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 2ab4e7510ff98b9fbf0223096b905e9de47f52e1
ms.sourcegitcommit: 1833c1e07a32c8ad41e4a1516e78100ae04a2156
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/26/2020
ms.locfileid: "3508182"
---
# <a name="process-automation"></a>Prosessien automatisointi

[!include[banner](../includes/banner.md)]

Prosessien automatisointi mahdollistaa eräpalvelimen käyttämien prosessien yksinkertaisen aikatauluttamisen. Ajoitetun työmäärän päivitetyn kalenterinäkymän avulla peruskäyttäjät voivat tarkastella ajoitettuja ja valmiita töitä sekä tehdä niihin liittyviä toimia.

## <a name="administration"></a>Hallinto

Kaikkien prosessien automatisointien keskitetty hallintasivu löytyy **Asetukset**-valikon Järjestelmänhallinta-moduulista. Tällä sivulla luetellaan kaikki järjestelmään määritetyt automaattiset prosessit (sarjat). Sen avulla voit myös lisätä uusia prosessiautomaatioita suoraan tältä sivulta. Kun sarja on määritetty, voit hallita kutakin sarjaa tästä luettelosta. Voit halutessasi muokata koko sarjaa, poistaa sen, tarkastella kaikkia luettelonäkymän esiintymiä tai poistaa sarjan käytöstä, jos haluat keskeyttää ajoitetun työn tietyn ajanjakson ajaksi. 

## <a name="calendar-view"></a>Kalenterinäkymä 
Yksi prosessin automaation tärkeimmistä eduista on mahdollisuus tarkastella ajoitettua työtä yksinkertaisessa kalenterinäkymässä.  Tämän näkymän avulla voit tarkastella töitä viikon kerrallaan. Tämä näkymä näkyy **Prosessin automatisointi** -sivun oikealla puolella. Valitun sarjan ajoitettu työmäärä täytetään. 

[![Prosessin automatisointikalenteri](./media/CalendarView2.png)](./media/CalendarView2.png)

## <a name="occurrence-changes"></a>Esiintymän muutokset
Kutakin esiintymää voi muokata muuttamatta niiden sarjojen määrittämiä esiintymiä, jotka ovat peräisin niistä. Ajoitettujen töiden esiintymiä voi muokata kalenterinäkymästä valitsemalla **Näytä/Muokkaa**-painike ja valitsemalla sitten **Esiintymä**. Näin voit käyttää kaikkia asetuksia, jotka on alun perin määritetty ohjatussa sarjan asennuksessa, ja antaa mahdollisuuden tehdä kertaluonteinen muutos valitulle esiintymälle. Ajoitettujen töiden esiintyminen voidaan poistaa käytöstä myös valitsemalla **Poista käytöstä** -painike kalenterinäkymästä. 

## <a name="developer-documentation"></a>Kehitysdokumentaatio 
Kehittäjien ohjeita kirjoitetaan parhaillaan, jotta kehittäjät voivat laajentaa prosessin automaatiokehystä. Näissä ohjeissa on tietoja siitä, miten voit luoda mukautettuja prosesseja, joita eräpalvelin suorittaa ajoitettuna ohjatun prosessin automatisoinnin avulla, ja tuoda ne näkyviin kalenterinäkymään automaattisesti.
