---
title: Varaston suorituskyvyn Power BI -sisältö
description: Tässä artikkelissa kuvataan, mitä kuuluu varaston suorituskyvyn Power BI -sisältöön.
author: Mirzaab
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 272953
ms.assetid: 4e4d4323-78cf-4ffa-8d5a-05e856c33db6
ms.search.form: WHSWarehousePerformancePowerBI
ms.openlocfilehash: 82f43f45b43df864cbda8ba372dbed46d8f4c7e4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289843"
---
# <a name="warehouse-performance-power-bi-content"></a>Varaston suorituskyvyn Power BI -sisältö

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, mitä kuuluu **varaston suorituskyvyn** Microsoft Power BI -sisältöön. Siinä selitetään, miten sisältyvät Power BI -raportit avataan, sekä kerrotaan sisällön muodostamisessa käytettävistä tietomallista ja yksiköistä.

## <a name="overview"></a>Yleiskuvaus

**Varaston suorituskyvyn** Power BI -sisältöpaketti on luotu varaston ja toiminnoista vastaavien johtajien tärkeiden saapuvien, lähtevien ja varaston mittareiden seurantaan. Se käyttää varastonhallinta-, tuote- ja muita järjestelmäsi tapahtumatietoja tarjotakseen kootun näkymän varaston suorituskyvystä sekä erittelyn toimittajista, tuoteryhmistä ja tuotteista sekä sijainneista ja varastoista.

Varaston esimiehet voivat käyttää **varaston suorituskyvyn** Power BI -sisältöpakettia seuraavien kolmen alueen mittaamiseen:

- **Saapuvien suorituskyky** – Mittaa toimittajan suoritusta verrattuna asiakkaan vaatimuksiin (toisin sanoen toimitusten suorituskykyä) sekä poispanojen suorituskykyä, jotta voit tunnistaa työntekijöihin tai nimikkeisiin liittyviä tietyllä aikavälillä. On tärkeää, että tiedät toimittavatko toimittajat tuotteet ajallaan, etuajassa vai myöhässä, jotta voit määrittää, miten toimittajan suorituskyky vaikuttaa poispanojen suorituskykyyn. Toimittaja, joka toimittaa tuotteet sovittujen päivämäärien ulkopuolella, voi aiheuttaa varastolle ylimääräistä painetta odottamattoman työn vuoksi ja siten nostaa keskimääräistä hyllytysaikaa.
- **Lähetysten suorituskyky** – Mittaa, lähetetäänkö tuotteet varastostasi täydellisinä ja ajallaan asiakkaille (toisin sanoen lähtevien lähetysten ja toimitusten suorituskykyä), jotta voit tunnistaa tuotteisiin, sijainteihin, varastoihin tai kohdistettuihin asiakkaisiin liittyvät ongelmat. Jos huomaat, että lähetyksesi tietyille alueille tai tiettyihin kaupunkeihin ovat myöhässä, voi olla tarpeen kiinnittää tarkempaa huomiota kuljetusten tai tilien hallintaan.
- **Toimipaikkojen varastotarkkuus** – Varastotarkkuus on tärkeä sisäinen varaston liiketoimintatieto (BI). Laskennan yleisen tarkkuuden selvittäminen on hyvin tärkeää. Tärkeää on myös määrittää, kuinka tarkasti varastoit nimikkeitä oikeissa toimipaikoissa, ja jotta voit korostaa ristiriitatietoja löytääksesi nimikkeille paremmat paikat tai aloittaaksesi tietyille nimikkeille kokonaislaskennan. (Nimikepohjainen laskentatoiminta toimitetaan tällä hetkellä korjaustiedostona.) Jos käytät tätä Power BI -sisältöpakettia käytettävissä olevan varaston oikeellisuuden selvittämiseen toimipaikkakohtaisesti, voit myös tunnistaa varkaustapaukset liikkeissäsi. Voit myös määrittää, onko yhdessäkään toimipaikassasi käytettävissä olevia määriä, jotka poikkeavat yrityksen resurssien suunnittelutiedoista (ERP). Toimipaikat voivat olla liian suuria tai niiden laskenta voi olla mahdotonta. Fyysinen sijoittelu voi vaihtoehtoisesti olla huonoa, jonka vuoksi yksittäisen nimiketyypin synkronointi käytettävissä olevaan tietoon on vaikeaa.

## <a name="accessing-the-power-bi-content-pack"></a>Power BI -sisältöpaketin avaaminen
**Varaston suorituskyvyn** Power BI -sisältö näkyy **Varaston suorituskyky** -sivulla (**Varastonhallinta** \> **Kyselyt ja raportit** \> **Varaston suorituskykyanalyysi** \> **Varaston suorituskyky**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mittarit, jotka sisältyvät Power BI -sisältöön
**Varaston suorituskyvyn** Power BI -sisältö sisältää raportin. Tämä raportti koostuu joukosta mittareita, jotka ovat visualisoitu kaavioiden, ruutujen ja taulukoiden muodossa. Seuraavassa taulukossa on yleiskatsaus visualisoinneista **varaston suorituskyvyn** Power BI -sisällössä.

| Raporttisivu                 | Kaaviot                                   | kuvaus |
|-----------------------------|------------------------------------------|-------------|
| Saapuvien suorituskyky         | Poispanot yhteensä                          | Tiettynä aikana käsiteltävien poispanotyörivien määrä. |
| Saapuvien suorituskyky         | Keskimääräinen poispanoaika                    | Keskimääräinen aika tunteina kaikille ostotilausten poispanoriveille, jotka on käsitelty, nimikkeiden rekisteröinnistä viimeisen panon käsittelyyn. |
| Saapuvien suorituskyky         | Vastaanotettu etuajassa                           | Etuajassa vastaanotettujen ostotilausrivien määrä. |
| Saapuvien suorituskyky         | Vastaanotettu ajallaan                         | Ajallaan vastaanotettujen ostotilausrivien määrä. |
| Saapuvien suorituskyky         | Vastaanotettu myöhässä                            | Myöhässä vastaanotettujen ostotilausrivien määrä. |
| Saapuvien suorituskyky         | Ajallaan toimittajan mukaan                        | Näkymä ostotilausrivien osuuksista, jotka on vastaanotettu toimittajalta tai toimittajaryhmältä etuajassa, ajallaan tai myöhässä. |
| Saapuvien suorituskyky         | Keskimääräinen laiturilta varastoon panon aika (tuntia) | Keskimääräinen laiturilta varastoon poispanon aika tunteina. |
| Saapuvien suorituskyky         | Keskimääräinen poispano työntekijän mukaan               | Keskimääräinen aika tunteina, jonka työntekijä on käyttänyt ostotilausrivien poispanokäsittelyyn. |
| Saapuvien suorituskyky         | Keskimääräinen poispanoaika toimittajan mukaan          | Keskimääräinen poispanoaika tunteina toimittajan tai toimittajaryhmän mukaan. |
| Saapuvien suorituskyky         | Keskimääräinen poispanoaika tuotteen mukaan         | Keskimääräinen poispanoaika tunteina nimikkeen tai nimikeryhmän mukaan. |
| Toimipaikan tarkkuuden seuranta | Määrä yhteensä                              | Tiettynä kautena käsiteltävien laskentatyörivien määrä. |
| Toimipaikan tarkkuuden seuranta | Poikkeama-aste                         | Yhteenlaskettu poikkeama-aste prosenttiosuutena kaikista kauden lasketuista riveistä. |
| Toimipaikan tarkkuuden seuranta | Laskenta ilman poikkeamaa                | Poikkeuksetta käsiteltyjen rivien määrä käsiteltyjen laskentatyörivien kokonaismäärästä. |
| Toimipaikan tarkkuuden seuranta | Jakson aikana lasketut nimikkeet                  | Laskettujen nimikkeiden osuus poikkeuksin ja poikkeuksitta tiettynä aikana. |
| Toimipaikan tarkkuuden seuranta | Nimikkeen määräpoikkeama suurempi kuin % | Taulukkonäkymä laskentariveistä, joilla on poikkeamia, jotka ylittävät tietyn osuuden. Taulukko sisältää seuraavat tiedot: toimipaikat, nimikkeet, keskimääräinen poikkeama, laskettujen laskentatyörivien kokonaismäärä, toimipaikan poikkeamia sisältävien rivien määrä, keskimääräinen laskettu määrä, laskettavaksi odotettu kokonaismäärä ja todellinen laskettu nimikemäärä. |
| Toimipaikan tarkkuuden seuranta | Nimikkeiden laskenta työntekijän mukaan                     | Työntekijöiden laskennan suorituskyky. Suorituskyky ilmaistaan prosenttiosuutena laskentatyöriveistä, joilla on ja ei ole poikkeamia. |
| Toimipaikan tarkkuuden seuranta | Nimikkeen laskenta sijainnin/varaston mukaan           | Laskennan suorituskyky sijainnin tai varaston mukaan käsiteltyjen laskentatyörivien määrän mukaisesti, sekä poikkeamin että ilman poikkeamia. |
| Toimipaikan tarkkuuden seuranta | Poikkeamien osuus tuotteen mukaan              | Laskennan suorituskyvyn poikkeamien osuus. Osuus ilmoitetaan prosenttiosuutena käsitellyistä laskentatyöriveistä nimikkeen tai nimikeryhmän mukaan. |
| Lähetysten suorituskyky        | Lähetetyt rivit                            | Tiettynä kautena lähetettyjen lähetysrivien kokonaismäärä. |
| Lähetysten suorituskyky        | Etuajassa                                    | Etuajassa lähetettyjen lähetysrivien osuus. |
| Lähetysten suorituskyky        | Ajallaan                                  | Ajallaan lähetettyjen lähetysrivien osuus. |
| Lähetysten suorituskyky        | Myöhässä                                     | Myöhässä lähetettyjen lähetysrivien osuus. |
| Lähetysten suorituskyky        | Lähetykset tiettynä aikana                      | Osuudet etuajassa, ajallaan tai myöhässä lähetetyistä lähetysriveistä. Trendirivi näyttää ajallaan toimitettujen rivien trendin. |
| Lähetysten suorituskyky        | Myöhästyneet lähetykset kaupungin mukaan                     | Karttavisualisointi kaupungeista ja alueista, joihin myöhästyneet lähetykset vaikuttavat. |
| Lähetysten suorituskyky        | Lähetetyt tuotteen mukaan                       | Etuajassa, ajallaan tai myöhässä lähetettyjen tuotteiden osuus nimikkeen tai nimikeryhmän mukaan. |
| Lähetysten suorituskyky        | Lähetetyt asiakkaan mukaan                      | Etuajassa, ajallaan tai myöhässä lähetettyjen tuotteiden osuus asiakkaan tai asiakasryhmän mukaan. |
| Lähetysten suorituskyky        | Lähetetyt sijainnin/varaston mukaan              | Etuajassa, ajallaan tai myöhässä lähetettyjen tuotteiden osuus sijainnin tai varaston mukaan. |

## <a name="understanding-the-data-model-and-calculations"></a>Tietomallin ja laskelmien tiedot
Seuraavia tietoja käytetään **varaston suorituskyvyn** Power BI -sisällön raporttisivujen täyttämiseen. Nämä tiedot esitetään koottuina mittauksina, joka vaiheistetaan yksikkösäilössä. Yksikkösäilö on analytiikkaa varten optimoitu Microsoft SQL Server -tietokanta. Lisätietoja on kohdassa [Power BI:n ja yksikkösäilön integraatio](power-bi-integration-entity-store.md).

Seuraavia tärkeitä koostettuja mittoja käytetään sisällön perustana.

| Raporttisivu                 | Kaaviot                                   | Taulut                                | Laskelmien kuvaukset |
|-----------------------------|------------------------------------------|---------------------------------------|--------------------------|
| Saapuvien suorituskyky         | Poispanot yhteensä                          | WHSWorkLine                           | Työrivien laskenta, kun työn tyyppi on **poispano**. |
| Saapuvien suorituskyky         | Keskimääräinen poispanoaika                    | WHSWorkLine                           | Työrivien enimmäisajan summa jaettuna työrivien enimmäisajan laskennalla, jossa työrivien enimmäisaika on suurin väli työn luontipäivämäärän ja sulkemispäivämäärän välillä. |
| Saapuvien suorituskyky         | Vastaanotettu etuajassa                           | WHSWorkLine                           | Laskenta työriveistä, joiden työn luontipäivämäärä on aiempi kuin käytetty toimituspäivämäärä. Jos toimituksen vahvistuspäivämäärää ei ole asetettu, käytä oletustoimituspäivämäärää. |
| Saapuvien suorituskyky         | Vastaanotettu ajallaan                         | WHSWorkLine                           | Laskenta työriveistä, joiden työn luontipäivämäärä on sama kuin käytetty toimituspäivämäärä. Jos toimituksen vahvistuspäivämäärää ei ole asetettu, käytä oletustoimituspäivämäärää. |
| Saapuvien suorituskyky         | Vastaanotettu myöhässä                            | WHSWorkLine                           | Laskenta työriveistä, joiden työn luontipäivämäärä on myöhempi kuin käytetty toimituspäivämäärä. Jos toimituksen vahvistuspäivämäärää ei ole asetettu, käytä oletustoimituspäivämäärää. |
| Saapuvien suorituskyky         | Ajallaan toimittajan mukaan                        | WHSWorkLine                           | Vastaanotettu ajoissa, Vastaanotettu etuajassa ja Vastaanotettu myöhässä (kuvaukset aiempana tässä taulukossa.) |
| Saapuvien suorituskyky         | Keskimääräinen laiturilta varastoon panon aika (tuntia)   | WHSWorkLine                           | Keskimääräinen hyllytysaika (kuvaus aiemmin tässä taulukossa.) |
| Saapuvien suorituskyky         | Keskimääräinen poispano työntekijän mukaan               | WHSWorkLine                           | Keskimääräinen hyllytysaika (kuvaus aiemmin tässä taulukossa.) |
| Saapuvien suorituskyky         | Keskimääräinen poispanoaika toimittajan mukaan          | WHSWorkLine                           | Keskimääräinen hyllytysaika (kuvaus aiemmin tässä taulukossa.) |
| Saapuvien suorituskyky         | Keskimääräinen poispanoaika tuotteen mukaan         | WHSWorkLine                           | Keskimääräinen hyllytysaika (kuvaus aiemmin tässä taulukossa.) |
| Toimipaikan tarkkuuden seuranta | Määrä yhteensä                              | WHSWorkLineCycleCount                 | Inventoinnit, joissa absoluuttisen poikkeaman määrä on yhtä suuri tai suurempi kuin 0 (nolla). |
| Toimipaikan tarkkuuden seuranta | Poikkeama-aste                         | WHSWorkLineCycleCount                 | Inventoinnit, joilla on poikkeamia jaettuna kokonaislaskennalla. Inventoinnilla on poikkeamia silloin, kun absoluuttinen poikkeamien määrä on suurempi kuin 0 (nolla). |
| Toimipaikan tarkkuuden seuranta | Laskenta ilman poikkeamaa                | WHSWorkLineCycleCount                 | Inventoinnit, joissa absoluuttisen poikkeaman määrä on suurempi kuin 0 (nolla). |
| Toimipaikan tarkkuuden seuranta | Laskenta poikkeamin                   | WHSWorkLineCycleCount                 | Inventoinnit, joissa absoluuttisen poikkeaman määrä on yhtä suuri kuin 0 (nolla). |
| Toimipaikan tarkkuuden seuranta | Jakson aikana lasketut nimikkeet                  | WHSWorkLineCycleCount                 | Laskenta ilman poikkeamia ja Laskenta poikkeamin (Kuvaukset aiempana tässä taulukossa.) |
| Toimipaikan tarkkuuden seuranta | Nimikkeen määräpoikkeama suurempi kuin % | WHSWorkLineCycleCount                 | Keskimääräinen poikkeama on absoluuttinen poikkeamien määrä jaettuna odotetulla määrällä, jossa absoluuttinen poikkeamien määrä on suurempi kuin 0 (nolla). Keskimääräinen poikkeaman määrä on keskimääräinen absoluuttisten poikkeamien määrä jaettuna odotetulla määrällä, jossa absoluuttinen poikkeamien määrä on suurempi kuin 0 (nolla). Laskenta poikkeamin, Kokonaislaskenta, Odotettu määrä, ja Laskettu määrä, jossa kokonaismäärä on ryhmitelty nimikkeen ja toimipaikan mukaan (kuvaukset aiempana tässä taulukossa). |
| Toimipaikan tarkkuuden seuranta | Nimikkeiden laskenta työntekijän mukaan                     | WHSWorkLineCycleCount                 | Laskenta ilman poikkeamia ja Laskenta poikkeamin (kuvaukset aiempana tässä taulukossa.) |
| Toimipaikan tarkkuuden seuranta | Nimikkeen laskenta sijainnin/varaston mukaan           | WHSWorkLineCycleCount                 | Laskenta ilman poikkeamia ja Laskenta poikkeamin (kuvaukset aiempana tässä taulukossa.) |
| Toimipaikan tarkkuuden seuranta | Poikkeamien osuus tuotteen mukaan              | WHSWorkLineCycleCount                 | Poikkeamien osuus (kuvaus aiempana tässä taulukossa.) |
| Lähetysten suorituskyky        | Lähetetyt rivit                            | SalesLine               | Myyntirivien laskenta, jossa myyntirivit on lähetetty. |
| Lähetysten suorituskyky        | Etuajassa                                    | CustPackingSlipOnTimeStatus           | Myyntirivit, joiden lähetyspäivä-tila on **1 (Etuajassa)**. Etuajassa tarkoittaa sitä, että pakkausluettelon lähetyspäivä on aikaisempi kuin myyntirivin vahvistettu lähetyspäivämäärä. Jos vahvistettua lähetyspäivämäärää ei ole asetettu, käytä pyydettyä lähetyspäivämäärää. |
| Lähetysten suorituskyky        | Ajallaan                                  | CustPackingSlipOnTimeStatus           | Myyntirivit, joiden lähetyspäivä-tila on **2 (Ajallaan)**. Ajallaan tarkoittaa sitä, että pakkausluettelon lähetyspäivä on sama kuin myyntirivin vahvistettu lähetyspäivämäärä. Jos vahvistettua lähetyspäivämäärää ei ole asetettu, käytä pyydettyä lähetyspäivämäärää. |
| Lähetysten suorituskyky        | Myöhässä                                     | CustPackingSlipOnTimeStatus           | Myyntirivit, joiden lähetyspäivä-tila on **3 (Myöhässä)**. Myöhässä tarkoittaa sitä, että pakkausluettelon lähetyspäivä on myöhäisempi kuin myyntirivin vahvistettu lähetyspäivämäärä. Jos vahvistettua lähetyspäivämäärää ei ole asetettu, käytä pyydettyä lähetyspäivämäärää. |
| Lähetysten suorituskyky        | Lähetykset tiettynä aikana                      | SalesLine CustPackingSlipOnTimeStatus | Tilaukset, jotka on lähetetty täysin, joissa myyntirivin koko määrä on lähetetty, ja lisäksi Etuajassa, Ajallaan ja Myöhässä (Kuvaukset aiempana tässä taulukossa). |
| Lähetysten suorituskyky        | Myöhästyneet lähetykset kaupungin mukaan                     | CustPackingSlipOnTimeStatus           | Myöhässä (kuvaus aiempana tässä taulukossa.) |
| Lähetysten suorituskyky        | Lähetetyt tuotteen mukaan                       | CustPackingSlipOnTimeStatus           | Etuajassa, Ajoissa ja Myöhässä (kuvaukset aiempana tässä taulukossa). |
| Lähetysten suorituskyky        | Lähetetyt asiakkaan mukaan                      | CustPackingSlipOnTimeStatus           | Etuajassa, Ajoissa ja Myöhässä (kuvaukset aiempana tässä taulukossa). |
| Lähetysten suorituskyky        | Lähetetyt sijainnin/varaston mukaan              | CustPackingSlipOnTimeStatus           | Etuajassa, Ajoissa ja Myöhässä (kuvaukset aiempana tässä taulukossa). |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
