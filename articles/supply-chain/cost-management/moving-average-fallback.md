---
title: Liukuva keskiarvo, varalla oleva kustannusjärjestys
description: Tässä ohjeaiheessa on tietoja varakustannusjaksoista keskimääräisten muuttuvien laskelmien tekemiseksi Microsoft Dynamics 365 Supply Chain Managementissa.
author: AndersGirke
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: d91b3b4b8d49e59aa03d62f4dd101b5a1ec18c41
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568204"
---
# <a name="moving-average-fallback-cost-sequence"></a>Liukuva keskiarvo, varalla oleva kustannusjärjestys

[!include [banner](../includes/banner.md)]

Yksi tapa, jolla voit laskea varastosi kustannuksen, on _liukuva keskiarvo_. Kuhunkin varastonimikkeeseen voidaan liittää enintään kolme kustannusarvoa:

- **Viimeinen varasto-otto** – Viimeinen varasto-ottokustannus, joka määritettiin ennen kuin varasto muuttui negatiiviseksi
- **Aktiivinen kustannus** – Uusin kustannuslaskelmaversiossa aktivoitu hinta
- **Nimikehinta** – Vapautetusta tuotteesta määritetty kustannus

Määrittääkseen, mitä näistä kustannusarvoista käytetään liukuvissa keskiarvolaskelmissa, järjestelmä käyttää _varakustannussarjaa_ arvojen järjestyksen määrittämiseen. Jos ensisijainen kustannusarvo ei ole käytettävissä, järjestelmä käyttää seuraavaa ensisijaista arvoa ja niin edelleen.

Aiemmissa Microsoft Dynamics 365 Supply Chain Management -versioissa järjestelmä käytti vahvistettua varaukustannussarjaa (_viimeinen varasto-otto – aktiivinen kustannus – nimikehinta_). Versiossa 10.0.11 tämä järjestys on edelleen oletusjärjestys. Voit kuitenkin myös ottaa käyttöön toiminnon, jonka avulla voit valita kolmesta käytettävissä olevasta varakustannussekvenssistä. Tämä ominaisuus voi olla erityisen hyödyllinen organisaatioille, jotka käyttävät säännöllisesti negatiivisia varastoarvoja.

Jos haluat, että varakustannussarjavalitsin on käytettävissä, sinun (tai ylläpitäjän) on käytettävä [Ominaisuuksien hallintaa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), jotta voit ottaa käyttöön toiminnon, jonka nimi on _liukuva keskiarvo_.

Voit valita liukuvan keskiarvolaskennan varauksen kustannusjärjestyksen noudattamalla seuraavia vaiheita.

1. Avaa **Parametrit**-sivu.
2. Määritä **Varastokirjanpito**-välilehden **Liukuva keskiarvo** -osassa **Varakustannussarja**-kentän arvoksi jokin seuraavista arvoista:

    - **Viimeinen varasto-otto – aktiivinen kustannus – nimikkeen hinta** – Tämä järjestys on oletusjärjestys. Se on sama järjestys, jota käytetään, jos _liukuva keskiarvovarakustannussekvenssi_ -toiminto ei ole käytössä.
    - **Aktiivinen kustannus – viimeisin varasto-otto**
    - **Aktiivinen kustannus – nimike hinta** – Organisaatioissa saattaa ilmetä suorituskykyongelmia, jos ne käyttävät liiketoimintaprosesseja, joissa varasto säännöllisesti muuttuu negatiiviseksi ja samaan aikaan transaktion määrä on suuri. Tämän asetuksen avulla voit lieventää suorituskykyongelmia.

![Varastokirjanpitoparametrit.](media/inventory-accounting-parameters.png "Varastokirjanpitoparametrit")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]