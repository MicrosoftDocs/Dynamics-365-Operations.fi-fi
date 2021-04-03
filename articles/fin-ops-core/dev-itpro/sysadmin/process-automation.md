---
title: Prosessien automatisointi
description: Tässä ohjeaiheessa on tietoja siitä, miten prosessien automatisointi mahdollistaa eräpalvelimen käyttämien prosessien yksinkertaisen aikatauluttamisen.
author: RyanCCarlson2
manager: tonyafehr
ms.date: 08/12/2020
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
ms.openlocfilehash: e3babed18caefff16105f70a0b15b8b8cf0f08eb
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568207"
---
# <a name="process-automation"></a>Prosessien automatisointi

[!include[banner](../includes/banner.md)]

Prosessien automatisointi mahdollistaa eräpalvelimen käyttämien prosessien yksinkertaisen aikatauluttamisen. Ajoitetun työmäärän päivitetyn kalenterinäkymän avulla peruskäyttäjät voivat tarkastella ajoitettuja ja valmiita töitä sekä tehdä niihin liittyviä toimia.

## <a name="administration"></a>Hallinto

Kaikkien prosessien automatisointien keskitetty hallintasivu löytyy **Asetukset**-valikon Järjestelmänhallinta-moduulista. Tällä sivulla luetellaan kaikki järjestelmään määritetyt automaattiset prosessit (sarjat). Sen avulla voit myös lisätä uusia prosessiautomaatioita suoraan tältä sivulta. Kun sarja on määritetty, voit hallita kutakin sarjaa tästä luettelosta. Voit halutessasi muokata koko sarjaa, poistaa sen, tarkastella kaikkia luettelonäkymän esiintymiä tai poistaa sarjan käytöstä, jos haluat keskeyttää ajoitetun työn tietyksi aikaa. 

Kaikki ominaisuuksien hallinnassa käytöstä poistetut prosessit eivät näy, kun toiminto on poistettu käytöstä. Lisäksi prosessiautomaation ajoitusmoduuli ei ajoita esiintymiä tai taustaprosesseja käytöstä poistetun ominaisuuden osalta. Kun ominaisuus otetaan uudelleen käyttöön, kaikki ajoitetut esiintymät tai taustaprosessit suoritetaan heti.

## <a name="calendar-view"></a>Kalenterinäkymä

Yksi prosessin automaation tärkeimmistä eduista on mahdollisuus tarkastella ajoitettua työtä yksinkertaisessa kalenterinäkymässä.  Tämän näkymän avulla voit tarkastella töitä viikon kerrallaan. Tämä näkymä näkyy **Prosessin automatisointi** -sivun oikealla puolella. Valitun sarjan ajoitettu työmäärä täytetään. 

[![Prosessin automatisointikalenteri](./media/CalendarView2.png)](./media/CalendarView2.png)

## <a name="occurrence-changes"></a>Esiintymän muutokset

Kutakin esiintymää voi muokata muuttamatta niiden sarjojen määrittämiä esiintymiä, jotka ovat peräisin niistä. Ajoitettujen töiden esiintymiä voi muokata kalenterinäkymästä valitsemalla **Näytä/Muokkaa**-painike ja valitsemalla sitten **Esiintymä**. Tämän sivun avulla voit käyttää kaikkia asetuksia, jotka on alun perin määritetty ohjatussa sarjan asennuksessa, ja antaa mahdollisuuden tehdä kertaluonteinen muutos valitulle esiintymälle. Ajoitettujen töiden esiintyminen voidaan poistaa käytöstä myös valitsemalla **Poista käytöstä** -painike kalenterinäkymästä.

## <a name="developer-documentation"></a>Kehitysdokumentaatio

Prosessin automaatiokehyksen avulla kehittäjät voivat laajentaa prosessin automaatiokehystä. [Prosessin automaatiokehys](../process-automation/process-automation-framework.md) -dokumentaatio sisältää tietoja siitä, miten voit luoda mukautettuja prosesseja, joita eräpalvelin suorittaa ajoitettuna ohjatun prosessin automatisoinnin avulla, ja tuoda ne näkyviin kalenterinäkymään automaattisesti.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]