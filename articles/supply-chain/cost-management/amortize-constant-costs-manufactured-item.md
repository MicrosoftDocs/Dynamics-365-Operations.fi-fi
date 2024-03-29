---
title: Valmistetun nimikkeen vakiokustannusten kuolettaminen
description: Valmistetun nimikkeen vakiokustannukset kuvastavat toimintojen asetusaikoja sekä komponentteja, joilla on vakiomäärä tai hävikin vakiomäärä.
author: JennySong-SH
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: d466395859e19874183691e697c8aca3a774d359
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675400"
---
# <a name="amortize-constant-costs-for-a-manufactured-item"></a>Valmistetun nimikkeen vakiokustannusten kuolettaminen

[!include [banner](../includes/banner.md)]

Valmistetun nimikkeen vakiokustannukset kuvastavat toimintojen asetusaikoja sekä komponentteja, joilla on vakiomäärä tai hävikin vakiomäärä. 

Kustannuslaskelman eräkoon käsitettä käytetään kuoletettaessa näitä valmistetun nimikkeen laskettujen kustannusten vakiokustannuksia. Tällä käsitteellä on useita synonyymeja, kuten kirjanpidon eräkoko. Myös vakiokustannusten kuoletuksen käsitteellä on useita synonyymeja, kuten suhteelliset vakiokustannukset.

Valmistetun nimikkeen kustannuslaskelman eräkokoa käytetään tuoterakennelaskelmassa. Alla oleva kuva osoittaa, miten tuoterakennelaskelman käynnistys- ja suoritustapa vaikuttavat määrään:

-   Nimikkeen tuoterakennelaskelman laskelman oletusmäärä: Nimikkeen varaston vakiotilausmäärä toimii nimikkeen kustannuslaskelman eräkoon oletusmääränä, mutta oletusmäärä voi olla suurempi, jolloin se kuvastaa nimikkeen tilausmäärän kerrannaisia Nimikkeen vakiotilausmäärä ja kerrannaiset voidaan määrittää nimikkeen oletustilausasetuksissa tai toimipaikkakohtaisissa tilausasetuksissa.
-   Nimikkeen tuoterakennelaskelman määritetty laskelman määrä: Määritetty laskelman määrä toimii nimikkeen kustannuslaskelman eräkokona. Laskelman oletusmääränä käytetään alun perin nimikkeen vakiotilausmäärää, mutta se voidaan ohittaa manuaalisesti. Määritetty laskelman määrä edustaa määritetyn nimikkeen kustannuslaskelman eräkokoa. Se edustaa myös tuotannon tuoterakennerivityypin valmistettujen komponenttien kustannuslaskelman eräkokoa. Tämä johtuu siitä, että oletettavasti komponentteja valmistetaan täsmälleen sama määrä. Muiden valmistettujen komponenttien (joiden tuoterakennerivityyppi on nimike) kustannuslaskelman eräkoko vastaa kyseisten komponenttien oletustilausmäärää.
-   Nimikkeen tuoterakennelaskelman määritetty valmistus myyntitilaukselle -määrä: Määritetty laskelman määrä toimii nimikkeen ja sen valmistettujen komponenttien kustannuslaskelman eräkokona, kun tuoterakennelaskelmat käyttävät valmistus myyntitilaukselle -hajotustilaa. Järjestelmä olettaa, että valmistettavia komponentteja tuotetaan täsmälleen sama määrä, aivan kuten valmistettavia komponentteja, joiden tuoterakennerivin tyyppi on tuotanto.
-   Tilauskohtaisen tuoterakennelaskelman määritetty laskelman määrä: Tilauskohtainen tuoterakennelaskelma voidaan suorittaa myyntitilauksen, myyntitarjouksen tai huoltotilauksen rivinimikkeelle. Määritetyn laskelman määrän oletusmääränä käytetään alkuperäisen rivinimikkeen määrää, mutta se voidaan ohittaa manuaalisesti. Voit valita, käyttääkö tilauskohtainen tuoterakennelaskelma valmistus myyntitilaukselle -hajotustilaa vai monirivistä hajotustilaa.

Valmistetun nimikkeen kuoletettujen vakiokustannusten laskettu summa sisältyy kuluihin.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]