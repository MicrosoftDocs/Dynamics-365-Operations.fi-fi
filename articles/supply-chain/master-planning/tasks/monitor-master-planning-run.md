---
title: Pääsuunnitteluajon valvonta
description: Tässä artikkelissa selvitetään, miten tuotannon suunnittelija näkee, käsitelläänkö pääsuunnitteluajoa.
author: t-benebo
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da04ef95f2f7e411ecea3fadf7ff31b3502d3d99
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860751"
---
# <a name="monitor-a-master-planning-run"></a>Pääsuunnitteluajon valvonta

[!include [banner](../../includes/banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a>Pääsuunnittelun edistymisen visualisointi Gantt-kaavion avulla

**Näytä pääsuunnittelun edistyminen** -sivulla pääsuunnitteluajoen historiatietoja Gantt-kaaviona. Tämän toiminnon avulla voi selvittää, kuinka kauan aikaa pääsuunnittelun eri vaiheisiin kului. Nykyisessä aktiivisessa suunnittelutyössä **Näytä pääsuunnittelun edistyminen** -sivun avulla voi seurata edistymistä ja näyttää arvioidun jäljellä olevan ajan.

### <a name="turn-the-master-plan-progress-visualization-feature-on-or-off"></a>Pääsuunnittelun etenemisen visualisointitoiminnon ottaminen käyttöön tai pois käytöstä

Supply Chain Managementin versiosta 10.0.21 alkaen tämä ominaisuus on poistettu oletusarvoisesti käytöstä. Supply Chain Managementin versiosta 10.0.25 alkaen tämä toiminto on pakollinen, eikä sitä voi poistaa käytöstä. Jos käytät vanhempaa versiota kuin 10.0.25, järjestelmänvalvojat voivat ottaa tämän toiminnon käyttöön tai pois käytöstä hakemalla *Aallon erätyön tiedot* -toimintoa [Toimintojen hallinta](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilassa.

### <a name="use-the-master-plan-progress-visualization-feature"></a>Pääsuunnittelun etenemisen visualisointitoiminnon käyttö

**Näytä pääsuunnittelun edistyminen** -sivulla voi olla näkyvissä sekä historiallisia että aktiivisia suunnittelutöitä. 

Historiallisten suunnittelutöiden näyttämiseen on kaksi vaihtoehtoa. 

1. Valitse ensin **Pääsuunnittelu \> Asetukset \> Suunnitelmat \> Pääsuunnitelmat** ja valitse sitten toimintoruudussa **Historia**. Kun sopiva työ on valittu, valitse ensin **Kyselyt** ja sitten **Näytä edistyminen**
1. Valitse ensin **Pääsuunnittelu \> Työtilat \> Pääsuunnittelu** ja valitse sitten Pääsuunnittelu-ruudussa **Historia**. Kun sopiva työ on valittu, valitse ensin **Kyselyt** ja sitten **Näytä edistyminen**

Aktiivisten suunnittelutöiden näyttämiseen on kaksi vaihtoehtoa. 
1. Valitse ensin **Pääsuunnittelu \> Työtilat \> Pääsuunnittelu** ja valitse sitten toimintoruudussa **Keskeneräiset suunnitteluprosessit**. Kun sopiva työ on valittu, valitse ensin **Kyselyt** ja sitten **Näytä edistyminen**.
1. Valitse ensin **Pääsuunnittelu \> Työtilat \> Pääsuunnittelu** ja valitse sitten Pääsuunnittelu-ruudussa **Näytä edistyminen**. Kun sopiva työ on valittu, valitse ensin **Kyselyt** ja sitten **Näytä edistyminen**

Huomaa, että voit tarkastella aktiivisia töitä vain silloin, kun suunnittelutyötä käsitellään.

### <a name="analyze-a-master-planning-job"></a>Pääsuunnittelun työn analysoiminen

Voit laajentaa Gantt-kaavion kunkin seuraavista suunnitteluprosesseista ja tarkastella ajankäyttöön liittyviä lisätietoja:

- Alustetaan
- Poistetaan ja lisätään tietoja
- Kattavuussuunnittelu
- Viiveet
- Toimintosanomat
- Viimeistely
- Automaattinen vahvistus

Gantt-kaavio on kätevä työkalu, jos haluat tarkastella toimenpidesanomien vaikutusta.

#### <a name="navigation-in-the-gantt-chart"></a>Siirtyminen Gantt-kaaviossa

- Voit laajentaa valittua ryhmää ja näyttää tiedot valitsemalla plus-merkin (**+**) puunäkymässä.
- Voit pienentää valitun ryhmän valitsemalla puunäkymässä miinus-merkin (**–**).
- Voit käyttää näppäimistöä siirtymiseen. Voit siirtyä riviltä toiselle **ylänuoli**- ja **alanuoli**-näppäimillä. Voit laajentaa ja tiivistää ryhmiä **oikealla** ja **vasemmalla nuolinäppäimellä**.
- Voit avata tai sulkea kaikki Gantt-kaavion tasot valitsemalla **Laajenna kaikki** tai **Tiivistä kaikki**.
- Voit tarkastella liittyvää käsittelyaikaa pitämällä hiiren osoitinta tehtävän päällä. (Tehtävät ovat Gantt-kaavion alin taso.)

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a>Töiden vertailu näyttämällä muu pääsuunnitteluajo

Valitsemalla pääsuunnittelutyön **Näytä muu pääsuunnitteluajo** -kentässä, voit tarkastella toista pääsuunnittelutyötä Gantt-kaaviossa ja vertailla töitä.

#### <a name="bom-level-display"></a>Tuoterakennetason näyttö

Tuoterakennetasot näytetään eri tavalla, kun kyse on kattavuuden suunnittelusta, viiveistä, toimenpiteistä ja vahvistuksesta.

- **Kattavuuden suunnittelu** – Tuoterakennetasot näytetään odotetusti. Ne lasketaan ylhäältä alaspäin.

    **Esimerkki:** tuoterakennetaso 0, 1, 2

- **Viiveet** – Tuoterakennetasot näytetään kattavuuden suunnittelun tuoterakennetasoina –1:llä kerrottuna. (Toisin sanoen niissä on negatiivinen merkki.)

    **Esimerkki:** tuoterakennetaso –2, –1, 0

- **Toimenpidesanoma** – Tuoterakennetasot näytetään odotetusti. Ne lasketaan ylhäältä alaspäin.

    **Esimerkki:** tuoterakennetaso 0, 1, 2

- **Automaattinen vahvistus** – tuoterakennetasot näytetään 999, josta on vähennetty kattavuuden suunnittelu tuoterakennetaso.

    **Esimerkki:** tuoterakennetaso 999, 998, 997

Seuraavassa taulukossa on edellisten yhteenveto.

| Näytettävä tuoterakennetaso | Loppunimike | Alikomponentti | Raaka-aine |
|---|---|---|---|
| Kattavuussuunnittelu | 0 | 1 | 2 |
| Viiveet | 0 | –1 | –2 |
| Toimenpidesanoma | 0 | 1 | 2 |
| Automaattinen vahvistus | 999 | 998 | 997 |

#### <a name="visualize-progress"></a>Edistymisen visualisointi

Jos tarkastelet käsittelyssä olevaa pääsuunnittelutyötä, edistyminen näytetään Gantt-kaaviossa värien avulla. Seuraava värien teema on sininen. Muiden väriteemojen värit ovat erilaiset.

- **Tummansininen** – valmistuneet suunnittelutehtävät.
- **Oranssi** – käsiteltävänä oleva tehtävä.
- **Vaaleansininen** – arvio jäljellä olevista tehtävistä.

Väri näkyy vain Gantt-kaavion alimmalla tasolla. Valitsemalla **Laajenna kaikki** voit tarkastella kaikkia pääsuunnittelutyön tehtäviä. Arvio jäljellä olevista tehtävistä perustuu historiallisiin pääsuunnittelutöihin.

## <a name="run-master-planning-and-track-processing-time"></a>Pääsuunnittelun suorittaminen ja käsittelyajan seuraaminen

1. Valitse oletuskoontinäytössä **Pääsuunnittelu**.
1. Anna tai valitse **Suunnitelma**-kentässä arvo.
1. Valitse **Suorita**.
1. Määritä **Seuraa käsittelyaikaa**-asetuksen arvoksi **Kyllä**.
1. Syötä **Säikeiden määrä** -kenttään numero.
1. Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodatus**.
1. Valitse ruudukossa rivi, jonka **Kenttä**-kentän arvona on **Nimiketunnus**.
1. Anna **Ehdot**-kenttään arvo.
1. Valitse **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]