---
title: Konsernin sisäinen pääajoitus
description: Tässä aiheessa käsitellään konsernin sisäistä pääajoitusta
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: e28051097905503e291e0c15a50e9363b39b2daa
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548240"
---
# <a name="intercompany-master-scheduling"></a>Konsernin sisäinen pääajoitus

[!include [banner](../../includes/banner.md)]

Konsernin sisäinen pääajoitus on keino, jolla voidaan laskea tarpeet ja luoda suunnitellut konsernin sisäiset tilaukset usean sisäisen yrityksen kesken. Konsernin sisäinen pääajoitus toistetaan niin monta kertaa kuin käyttäjä on määrittänyt. Microsoft Dynamics 365 Supply Chain Management voi suorittaa konsernin sisäisen pääajoituksen, kun pääajoituksen asetukset määritetään kullekin konsernin sisäiselle yritykselle. Pääajoitus käsittää useita toistoja, joiden aikana Microsoft Dynamics 365 Supply Chain Management luo automaattisesti konsernin sisäisen ostotilauksen, mikä puolestaan johtaa konsernin sisäisen myyntitilauksen automaattiseen luomiseen ja se taas uusiin tarpeisiin.

Konsernin sisäinen pääajoitus ja ajoitusjärjestys määritetään kunkin sisäisen yrityksen **Pääajoitus**-parametreissa.

Tarpeen eteneminen konsernin sisäisen ketjun läpi on varmistettava, että suunnitellut ostotilaukset vahvistetaan automaattisesti eli tilauksien aikaa eikä määrää ei voi muuttaa. **Vahvistuksena aikaraja** määritetään kattavuusryhmä tai **Vahvistuksen aikaraja** pääsuunnitelmassa. Jos **Vahvistuksen aikaraja** jätetään määrittämättä, konsernin sisäisiä ostotilauksia ei luoda automaattisesti. Suunnitellut tilaukset ovat tuloksena vain pääajoituksen ensimmäisellä suorituskerralla. Koska konsernin sisäistä ostotilausta ei luoda, myöskään konsernin sisäistä myyntitilausta ei luoda, joten konsernin sisäisiä ostotilauksia ei luoda lisää jne.

Kun konsernin sisäinen pääajoitus käynnistetään, Microsoft Dynamics 365 Supply Chain Management suorittaa yhden pääajoituksen kullekin konsernin sisäiselle yritykselle, sitten toisen pääajoituksen kullekin yritykselle ja niin edelleen, kunnes määritetty määrä toistoja saavutetaan. Toistoja voidaan määrittää 30; ajoitus kuitenkin kestää sitä kauemmin, mitä enemmän toistoja valitaan.

Konsernin sisäinen pääajoitus voidaan käynnistää mistä tahansa konsernin sisäisestä yrityksestä, sillä yritysten pääajoitus ohjaa konsernin sisäinen ajoitusjärjestys. Tämä on järjestys, jonka mukaan ohjelma priorisoi kunkin konsernin sisäisen yrityksen pääajoituksen. Koska ajoitusjärjestys määrää, missä järjestyksessä yritysten pääajoitus suoritetaan, ei ole väliä, mistä ajoitus käynnistetään. Jokaisessa toistossa nykyisen yrityksen ajoitus suoritetaan viimeisenä.

> [!NOTE]
> Paras käytäntö on sallia konsernin sisäisen pääajoitus käynnistys yhdestä Microsoft Dynamics 365 Supply Chain Management -yrityksestä.

**Konsernin sisäinen pääsuunnittelu** -sivulla voidaan käynnistää pääajoitussarja, jossa pääajoitus suoritetaan ensimmäisellä kerralla sillä periaatteella, että kaikille konsernin sisäisille yrityksille päivitetään ensimmäistä toistoa varten valittu tarvelaskenta. Tämän jälkeen käytetään seuraavalle toistolle valittua toissijaista periaatetta niin kauan, kunnes kaikki määritetyt toistokerrat on suoritettu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
