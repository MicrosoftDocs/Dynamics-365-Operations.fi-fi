---
title: "Varaston suorituskyvyn Power BI -sisältö"
description: "Tässä aiheessa kuvataan, mitä kuuluu varaston suorituskyvyn Power BI -sisältöön. Siinä kuvataan, miten avaat Power BI -raportit. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä."
author: Mirzaab
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272953
ms.assetid: 4e4d4323-78cf-4ffa-8d5a-05e856c33db6
ms.search.region: Global
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: b4963c11f0cf3fb05e1905b265d4156323407e84
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="warehouse-performance-power-bi-content"></a>Varaston suorituskyvyn Power BI -sisältö

[!include[banner](../includes/banner.md)]

Tässä aiheessa kuvataan, mitä kuuluu **Varaston suorituskyvyn** Microsoft Power BI -sisältöön. Siinä kuvataan, miten avaat Power BI -raportit. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä.

## <a name="overview"></a>Yleiskuvaus

**Varaston suorituskyvyn** Power BI -sisältöpaketti on luotu varaston ja toiminnoista vastaavien johtajien tärkeiden saapuvien, lähtevien ja varaston mittareiden seurantaan. Se käyttää varastonhallinta-, tuote- ja muita järjestelmäsi tapahtumatietoja tarjotakseen kootun näkymän varaston suorituskyvystä sekä erittelyn toimittajista, tuoteryhmistä ja tuotteista sekä sijainneista ja varastoista. 

Varaston esimiehet voivat käyttää **Varaston suorituskyvyn** Power BI -sisältöpakettia seuraavien kolmen alueen mittaamiseen:

-   **Saapuvien suorituskyky** – Mittaa toimittajan suoritusta verrattuna asiakkaan vaatimuksiin (toisin sanoen toimitusten suorituskykyä) sekä poispanojen suorituskykyä, jotta voit tunnistaa työntekijöihin tai nimikkeisiin liittyviä tietyllä aikavälillä. On tärkeää, että tiedät toimittavatko toimittajat tuotteet ajallaan, etuajassa vai myöhässä, jotta voit määrittää, miten toimittajan suorituskyky vaikuttaa poispanojen suorituskykyyn. Toimittaja, joka toimittaa tuotteet sovittujen päivämäärien ulkopuolella, voi aiheuttaa varastolle ylimääräistä painetta odottamattoman työn vuoksi ja siten nostaa keskimääräistä hyllytysaikaa.
-   **Lähetysten suorituskyky** – Mittaa, lähetetäänkö tuotteet varastostasi täydellisinä ja ajallaan asiakkaille (toisin sanoen lähtevien lähetysten ja toimitusten suorituskykyä), jotta voit tunnistaa tuotteisiin, sijainteihin, varastoihin tai kohdistettuihin asiakkaisiin liittyvät ongelmat. Jos huomaat, että lähetyksesi tietyille alueille tai tiettyihin kaupunkeihin ovat myöhässä, voi olla tarpeen kiinnittää tarkempaa huomiota kuljetusten tai tilien hallintaan.
-   **Toimipaikkojen varastotarkkuus** – Varastotarkkuus on tärkeä sisäinen varaston liiketoimintatieto (BI). Laskennan yleisen tarkkuuden selvittäminen on hyvin tärkeää. Tärkeää on myös määrittää, kuinka tarkasti varastoit nimikkeitä oikeissa toimipaikoissa, ja jotta voit korostaa ristiriitatietoja löytääksesi nimikkeille paremmat paikat tai aloittaaksesi tietyille nimikkeille kokonaislaskennan. (Nimikepohjainen laskentatoiminta toimitetaan tällä hetkellä korjaustiedostona.) Jos käytät tätä Power BI -sisältöpakettia käytettävissä olevan varaston oikeellisuuden selvittämiseen toimipaikkakohtaisesti, voit myös tunnistaa varkaustapaukset liikkeissäsi. Voit myös määrittää, onko yhdessäkään toimipaikassasi käytettävissä olevia määriä, jotka poikkeavat yrityksen resurssien suunnittelutiedoista (ERP). Toimipaikat voivat olla liian suuria tai niiden laskenta voi olla mahdotonta. Fyysinen sijoittelu voi vaihtoehtoisesti olla huonoa, jonka vuoksi yksittäisen nimiketyypin synkronointi käytettävissä olevaan tietoon on vaikeaa.

## <a name="accessing-the-power-bi-content-pack"></a>Power BI -sisätöpaketin käyttö
Jos käytössä on Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin heinäkuun 2017 -päivitys, **Varaston suorituskyvyn** Power BI -sisältö näytetään **Varaston suorituskyky** -sivulla (**Varastonhallinta** > **Kyselyt ja raportit** > **Varaston suorituskyvyn analyysi** > **Varaston suorituskyky**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mittareita, jotka sisältyvät Power BI -sisältöön
**Varastoinnin suorituskyvyn** Power BI -sisältöpaketti sisältää raportin. Tämä raportti koostuu joukosta mittareita, jotka ovat visualisoitu kaavioiden, ruutujen ja taulukoiden muodossa. Seuraavassa taulukossa on yleiskatsaus visualisoinneista **varastoinnin suorituskyvyn** Power BI -sisällössä.

| Raporttisivu                 | Kaaviot                                   | kuvaus                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Saapuvien suorituskyky         | Poispanot yhteensä                          | Tiettynä aikana käsiteltävien poispanotyörivien määrä.                                                                                                                                                                                                                                                                                                                                       |
| Saapuvien suorituskyky         | Keskimääräinen poispanoaika                    | Keskimääräinen aika tunteina kaikille ostotilausten poispanoriveille, jotka on käsitelty, nimikkeiden rekisteröinnistä viimeisen panon käsittelyyn.                                                                                                                                                                                                                                                           |
| Saapuvien suorituskyky         | Vastaanotettu etuajassa                           | Etuajassa vastaanotettujen ostotilausrivien määrä.                                                                                                                                                                                                                                                                                                                                                     |
| Saapuvien suorituskyky         | Vastaanotettu ajallaan                         | Ajallaan vastaanotettujen ostotilausrivien määrä.                                                                                                                                                                                                                                                                                                                                                   |
| Saapuvien suorituskyky         | Vastaanotettu myöhässä                            | Myöhässä vastaanotettujen ostotilausrivien määrä.                                                                                                                                                                                                                                                                                                                                                      |
| Saapuvien suorituskyky         | Ajallaan toimittajan mukaan                        | Näkymä ostotilausrivien osuuksista, jotka on vastaanotettu toimittajalta tai toimittajaryhmältä etuajassa, ajallaan tai myöhässä.                                                                                                                                                                                                                                                                                      |
| Saapuvien suorituskyky         | Keskimääräinen laiturilta varastoon panon aika (tuntia) | Keskimääräinen laiturilta varastoon poispanon aika tunteina.                                                                                                                                                                                                                                                                                                                                                     |
| Saapuvien suorituskyky         | Keskimääräinen poispano työntekijän mukaan               | Keskimääräinen aika tunteina, jonka työntekijä on käyttänyt ostotilausrivien poispanokäsittelyyn.                                                                                                                                                                                                                                                                                                      |
| Saapuvien suorituskyky         | Keskimääräinen poispanoaika toimittajan mukaan          | Keskimääräinen poispanoaika tunteina toimittajan tai toimittajaryhmän mukaan.                                                                                                                                                                                                                                                                                                                                                   |
| Saapuvien suorituskyky         | Keskimääräinen poispanoaika tuotteen mukaan         | Keskimääräinen poispanoaika tunteina nimikkeen tai nimikeryhmän mukaan.                                                                                                                                                                                                                                                                                                                                                       |
| Toimipaikan tarkkuuden seuranta | Määrä yhteensä                              | Tiettynä kautena käsiteltävien laskentatyörivien määrä.                                                                                                                                                                                                                                                                                                                                        |
| Toimipaikan tarkkuuden seuranta | Poikkeama-aste                         | Yhteenlaskettu poikkeama-aste prosenttiosuutena kaikista kauden lasketuista riveistä.                                                                                                                                                                                                                                                                                                                    |
| Toimipaikan tarkkuuden seuranta | Laskenta ilman poikkeamaa                | Poikkeuksetta käsiteltyjen rivien määrä käsiteltyjen laskentatyörivien kokonaismäärästä.                                                                                                                                                                                                                                                                                  |
| Toimipaikan tarkkuuden seuranta | Jakson aikana lasketut nimikkeet                  | Laskettujen nimikkeiden osuus poikkeuksin ja poikkeuksitta tiettynä aikana.                                                                                                                                                                                                                                                                                                                                |
| Toimipaikan tarkkuuden seuranta | Nimikkeen määräpoikkeama suurempi kuin % | Taulukkonäkymä laskentariveistä, joilla on poikkeamia, jotka ylittävät tietyn osuuden. Taulukko sisältää seuraavat tiedot: toimipaikat, nimikkeet, keskimääräinen poikkeama, laskettujen laskentatyörivien kokonaismäärä, toimipaikan poikkeamia sisältävien rivien määrä, keskimääräinen laskettu määrä, laskettavaksi odotettu kokonaismäärä ja todellinen laskettu nimikemäärä. |
| Toimipaikan tarkkuuden seuranta | Nimikkeiden laskenta työntekijän mukaan                     | Työntekijöiden laskennan suorituskyky. Suorituskyky ilmaistaan prosenttiosuutena laskentatyöriveistä, joilla on ja ei ole poikkeamia.                                                                                                                                                                                                                                                                    |
| Toimipaikan tarkkuuden seuranta | Nimikkeen laskenta sijainnin/varaston mukaan           | Laskennan suorituskyky sijainnin tai varaston mukaan käsiteltyjen laskentatyörivien määrän mukaisesti, sekä poikkeamin että ilman poikkeamia.                                                                                                                                                                                                                                                                                |
| Toimipaikan tarkkuuden seuranta | Poikkeamien osuus tuotteen mukaan              | Laskennan suorituskyvyn poikkeamien osuus. Osuus ilmoitetaan prosenttiosuutena käsitellyistä laskentatyöriveistä nimikkeen tai nimikeryhmän mukaan.                                                                                                                                                                                                                                                                    |
| Lähetysten suorituskyky        | Lähetetyt rivit                            | Tiettynä kautena lähetettyjen lähetysrivien kokonaismäärä.                                                                                                                                                                                                                                                                                                                                        |
| Lähetysten suorituskyky        | Etuajassa                                    | Etuajassa lähetettyjen lähetysrivien osuus.                                                                                                                                                                                                                                                                                                                                                        |
| Lähetysten suorituskyky        | Ajallaan                                  | Ajallaan lähetettyjen lähetysrivien osuus.                                                                                                                                                                                                                                                                                                                                                      |
| Lähetysten suorituskyky        | Myöhässä                                     | Myöhässä lähetettyjen lähetysrivien osuus.                                                                                                                                                                                                                                                                                                                                                         |
| Lähetysten suorituskyky        | Lähetykset tiettynä aikana                      | Osuudet etuajassa, ajallaan tai myöhässä lähetetyistä lähetysriveistä. Trendirivi näyttää ajallaan toimitettujen rivien trendin.                                                                                                                                                                                                                                                 |
| Lähetysten suorituskyky        | Myöhästyneet lähetykset kaupungin mukaan                     | Karttavisualisointi kaupungeista ja alueista, joihin myöhästyneet lähetykset vaikuttavat.                                                                                                                                                                                                                                                                                                                                    |
| Lähetysten suorituskyky        | Lähetetyt tuotteen mukaan                       | Etuajassa, ajallaan tai myöhässä lähetettyjen tuotteiden osuus nimikkeen tai nimikeryhmän mukaan.                                                                                                                                                                                                                                                                                                                                   |
| Lähetysten suorituskyky        | Lähetetyt asiakkaan mukaan                      | Etuajassa, ajallaan tai myöhässä lähetettyjen tuotteiden osuus asiakkaan tai asiakasryhmän mukaan.                                                                                                                                                                                                                                                                                                                           |
| Lähetysten suorituskyky        | Lähetetyt sijainnin/varaston mukaan              | Etuajassa, ajallaan tai myöhässä lähetettyjen tuotteiden osuus sijainnin tai varaston mukaan.                                                                                                                                                                                                                                                                                                                                    |
## <a name="extending-the-power-bi-content"></a>Power BI -sisällön laajentaminen
Jos käytät Microsoft Dynamics Lifecycle Servicesin (LCS) sisältöpaketteja, voit tehdä erinomaisia analyyseja henkilöille, jotka eivät käytä Microsoft Dynamics 365:tä. Voit muokata näitä sisältöpaketit sisältämään muita raportteja ja visuaalisia tietoja ja julkaista sitten sisältöpaketit analysoitavaksi Power BI.com -vuokraajassa. 

**Varaston suorituskyvyn** Power BI -sisältö sijaitsee LCS:n Jaettu omaisuus -kirjastossa. Lisätietoja sisällön lataamisesta ja sen käyttöönottamisesta organisaatiossa on ohjeaiheessa [Microsoftin ja kumppaneiden Power BI -sisältö LCS-sovelluksessa](power-bi-content-microsoft-partners.md). Katso Power BI -sisällön käyttöönotosta kertova esittely Office Mixin kohdassa [Microsoftin ja kumppaneiden Power BI -sisältö Dynamics Lifecycle Services -sovelluksessa](https://mix.office.com/watch/9puyb1b2xs1w).

Muista ladata käyttämääsi Dynamics 365 -versiota vastaava **Varaston suorituskyvyn** sisältö.

> [!NOTE]
> Jos käytössä on Microsoft Dynamics 365 for Operations versio 1611, Power BI -sisällön edellytyksenä on KB 4011327. Kun olet kirjautunut LCS:ään, voit siirtyä tietämyskantaan osoitteessa https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.

## <a name="understanding-the-data-model-and-calculations"></a>Tietomallin ja laskelmien tiedot
Seuraavia tietoja käytetään **Varaston suorituskyvyn** Power BI -sisällön raporttisivujen täyttämiseen. Nämä tiedot esitetään koottuina mittauksina, joka vaiheistetaan yksikkösäilössä. Yksikkösäilö on analytiikkaa varten optimoitu Microsoft SQL Server -tietokanta. Lisätietoja on ohjeaiheessa [yleiskatsaus Power BI:n integraatiosta yksikkökaupan kanssa](power-bi-integration-entity-store.md). 

Seuraavia tärkeitä koostettuja mittoja käytetään sisällön perustana.

| Raporttisivu                 | Kaaviot                                   | Taulut                                | Laskelmien kuvaukset                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------|------------------------------------------|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Saapuvien suorituskyky         | Poispanot yhteensä                          | WHSWorkLine                           | Työrivien laskenta, kun työn tyyppi on **poispano**.                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Saapuvien suorituskyky         | Keskimääräinen poispanoaika                    | WHSWorkLine                           | Työrivien enimmäisajan summa jaettuna työrivien enimmäisajan laskennalla, jossa työrivien enimmäisaika on suurin väli työn luontipäivämäärän ja sulkemispäivämäärän välillä.                                                                                                                                                                                                                                                                                                                |
| Saapuvien suorituskyky         | Vastaanotettu etuajassa                           | WHSWorkLine                           | Laskenta työriveistä, joiden työn luontipäivämäärä on aiempi kuin käytetty toimituspäivämäärä. Jos toimituksen vahvistuspäivämäärää ei ole asetettu, käytä oletustoimituspäivämäärää.                                                                                                                                                                                                                                                                                                                  |
| Saapuvien suorituskyky         | Vastaanotettu ajallaan                         | WHSWorkLine                           | Laskenta työriveistä, joiden työn luontipäivämäärä on sama kuin käytetty toimituspäivämäärä. Jos toimituksen vahvistuspäivämäärää ei ole asetettu, käytä oletustoimituspäivämäärää.                                                                                                                                                                                                                                                                                                                      |
| Saapuvien suorituskyky         | Vastaanotettu myöhässä                            | WHSWorkLine                           | Laskenta työriveistä, joiden työn luontipäivämäärä on myöhempi kuin käytetty toimituspäivämäärä. Jos toimituksen vahvistuspäivämäärää ei ole asetettu, käytä oletustoimituspäivämäärää.                                                                                                                                                                                                                                                                                                                    |
| Saapuvien suorituskyky         | Ajallaan toimittajan mukaan                        | WHSWorkLine                           | Vastaanotettu ajoissa, Vastaanotettu etuajassa ja Vastaanotettu myöhässä (kuvaukset aiempana tässä taulukossa.)                                                                                                                                                                                                                                                                                                                                                                                             |
| Saapuvien suorituskyky         | Keskimääräinen laiturilta varastoon panon aika (tuntia) | WHSWorkLine                           | Keskimääräinen hyllytysaika (kuvaus aiemmin tässä taulukossa.)                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Saapuvien suorituskyky         | Keskimääräinen poispano työntekijän mukaan               | WHSWorkLine                           | Keskimääräinen hyllytysaika (kuvaus aiemmin tässä taulukossa.)                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Saapuvien suorituskyky         | Keskimääräinen poispanoaika toimittajan mukaan          | WHSWorkLine                           | Keskimääräinen hyllytysaika (kuvaus aiemmin tässä taulukossa.)                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Saapuvien suorituskyky         | Keskimääräinen poispanoaika tuotteen mukaan         | WHSWorkLine                           | Keskimääräinen hyllytysaika (kuvaus aiemmin tässä taulukossa.)                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Toimipaikan tarkkuuden seuranta | Määrä yhteensä                              | WHSWorkLineCycleCount                 | Inventoinnit, joissa absoluuttisen poikkeaman määrä on yhtä suuri tai suurempi kuin 0 (nolla).                                                                                                                                                                                                                                                                                                                                                                                                       |
| Toimipaikan tarkkuuden seuranta | Poikkeama-aste                         | WHSWorkLineCycleCount                 | Inventoinnit, joilla on poikkeamia jaettuna kokonaislaskennalla. Inventoinnilla on poikkeamia silloin, kun absoluuttinen poikkeamien määrä on suurempi kuin 0 (nolla).                                                                                                                                                                                                                                                                                                               |
| Toimipaikan tarkkuuden seuranta | Laskenta ilman poikkeamaa                | WHSWorkLineCycleCount                 | Inventoinnit, joissa absoluuttisen poikkeaman määrä on suurempi kuin 0 (nolla).                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Toimipaikan tarkkuuden seuranta | Laskenta poikkeamin                   | WHSWorkLineCycleCount                 | Inventoinnit, joissa absoluuttisen poikkeaman määrä on yhtä suuri kuin 0 (nolla).                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Toimipaikan tarkkuuden seuranta | Jakson aikana lasketut nimikkeet                  | WHSWorkLineCycleCount                 | Laskenta ilman poikkeamia ja Laskenta poikkeamin (Kuvaukset aiempana tässä taulukossa.)                                                                                                                                                                                                                                                                                                                                                                                            |
| Toimipaikan tarkkuuden seuranta | Nimikkeen määräpoikkeama suurempi kuin % | WHSWorkLineCycleCount                 | Keskimääräinen poikkeama on absoluuttinen poikkeamien määrä jaettuna odotetulla määrällä, jossa absoluuttinen poikkeamien määrä on suurempi kuin 0 (nolla). Keskimääräinen poikkeaman määrä on keskimääräinen absoluuttisten poikkeamien määrä jaettuna odotetulla määrällä, jossa absoluuttinen poikkeamien määrä on suurempi kuin 0 (nolla). Laskenta poikkeamin, Kokonaislaskenta, Odotettu määrä, ja Laskettu määrä, jossa kokonaismäärä on ryhmitelty nimikkeen ja toimipaikan mukaan (kuvaukset aiempana tässä taulukossa). |
| Toimipaikan tarkkuuden seuranta | Nimikkeiden laskenta työntekijän mukaan                     | WHSWorkLineCycleCount                 | Laskenta ilman poikkeamia ja Laskenta poikkeamin (kuvaukset aiempana tässä taulukossa.)                                                                                                                                                                                                                                                                                                                                                                                            |
| Toimipaikan tarkkuuden seuranta | Nimikkeen laskenta sijainnin/varaston mukaan           | WHSWorkLineCycleCount                 | Laskenta ilman poikkeamia ja Laskenta poikkeamin (kuvaukset aiempana tässä taulukossa.)                                                                                                                                                                                                                                                                                                                                                                                            |
| Toimipaikan tarkkuuden seuranta | Poikkeamien osuus tuotteen mukaan              | WHSWorkLineCycleCount                 | Poikkeamien osuus (kuvaus aiempana tässä taulukossa.)                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Lähetysten suorituskyky        | Lähetetyt rivit                            | SalesLine                             | Myyntirivien laskenta, jossa myyntirivit on lähetetty.                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Lähetysten suorituskyky        | Etuajassa                                    | CustPackingSlipOnTimeStatus           | Myyntirivit, joiden lähetyspäivä-tila on **1 (Etuajassa)**. Etuajassa tarkoittaa sitä, että pakkausluettelon lähetyspäivä on aikaisempi kuin myyntirivin vahvistettu lähetyspäivämäärä. Jos vahvistettua lähetyspäivämäärää ei ole asetettu, käytä pyydettyä lähetyspäivämäärää.                                                                                                                                                                                                                                                     |
| Lähetysten suorituskyky        | Ajallaan                                  | CustPackingSlipOnTimeStatus           | Myyntirivit, joiden lähetyspäivä-tila on **2 (Ajallaan)**. Ajallaan tarkoittaa sitä, että pakkausluettelon lähetyspäivä on sama kuin myyntirivin vahvistettu lähetyspäivämäärä. Jos vahvistettua lähetyspäivämäärää ei ole asetettu, käytä pyydettyä lähetyspäivämäärää.                                                                                                                                                                                                                                                     |
| Lähetysten suorituskyky        | Myöhässä                                     | CustPackingSlipOnTimeStatus           | Myyntirivit, joiden lähetyspäivä-tila on **3 (Myöhässä)**. Myöhässä tarkoittaa sitä, että pakkausluettelon lähetyspäivä on myöhäisempi kuin myyntirivin vahvistettu lähetyspäivämäärä. Jos vahvistettua lähetyspäivämäärää ei ole asetettu, käytä pyydettyä lähetyspäivämäärää.                                                                                                                                                                                                                                                         |
| Lähetysten suorituskyky        | Lähetykset tiettynä aikana                      | SalesLine CustPackingSlipOnTimeStatus | Tilaukset, jotka on lähetetty täysin, joissa myyntirivin koko määrä on lähetetty, ja lisäksi Etuajassa, Ajallaan ja Myöhässä (Kuvaukset aiempana tässä taulukossa).                                                                                                                                                                                                                                                                                                                             |
| Lähetysten suorituskyky        | Myöhästyneet lähetykset kaupungin mukaan                     | CustPackingSlipOnTimeStatus           | Myöhässä (kuvaus aiempana tässä taulukossa.)                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Lähetysten suorituskyky        | Lähetetyt tuotteen mukaan                       | CustPackingSlipOnTimeStatus           | Etuajassa, Ajoissa ja Myöhässä (kuvaukset aiempana tässä taulukossa).                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Lähetysten suorituskyky        | Lähetetyt asiakkaan mukaan                      | CustPackingSlipOnTimeStatus           | Etuajassa, Ajoissa ja Myöhässä (kuvaukset aiempana tässä taulukossa).                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Lähetysten suorituskyky        | Lähetetyt sijainnin/varaston mukaan              | CustPackingSlipOnTimeStatus           | Etuajassa, Ajoissa ja Myöhässä (kuvaukset aiempana tässä taulukossa).                                                                                                                                                                                                                                                                                                                                                                                                                        |
