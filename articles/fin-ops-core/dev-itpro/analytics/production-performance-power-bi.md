---
title: Tuotannon suorituskyvyn Power BI -sisältö
description: Tässä artikkelissa kerrotaan, mitä tuotannon suorituskyvyn Power BI -sisältö sisältää.
author: AndersGirke
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.search.form: ProductionPerformancePowerBI
ms.openlocfilehash: 010b351023c8dee2f1242442c5846098374f18ca
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280801"
---
# <a name="production-performance-power-bi-content"></a>Tuotannon suorituskyvyn Power BI -sisältö

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, mitä **tuotannon suorituskyvyn** Microsoft Power BI -sisältöön kuuluu. Siinä selitetään, miten sisältyvät Power BI -raportit avataan, sekä kerrotaan sisällön muodostamisessa käytetyistä tietomallista ja yksiköistä.

## <a name="overview"></a>Yleiskuvaus

**Tuotannon suorituskyvyn** Power BI -sisältö on suunnattu tuotannon esimiehille ja henkilöille, jotka vastaavat organisaatiossa tuotannonhallinnasta.

Voit käyttää sisällytetyissä raporteissa Power BI:tä tuotannon työvaiheiden valvontaan ja seurata niiden avulla tuotannon aikarajojen noudattamista, laatua ja kustannuksia. Raportit käyttävät tuotanto- ja erätilausten tapahtumatietoja, ja niissä on koostenäkymä koko yrityksen tuotantomittareista sekä tuote- ja resurssikohtaiset mittareiden erittelyt.

Power BI -sisältö nostaa esille organisaation kyvyn valmistaa tuotteet ajoissa ja täysimääräisenä. Tuleva suorituskyky projisoidaan tuotantosuunnitelmien perusteella. Kattavissa raporteissa on tarkkoja tietoja tuotannosta johtuvista tuotevioista sekä resurssien ja työvaiheiden virheellisyysasteet.

Voit myös analysoida tuotannon variansseja Power BI -sisällön avulla. Tuotannon varianssit lasketaan arvioitujen kustannusten ja toteutuneiden kustannusten välisenä erona. Tuotannon varianssit lasketaan, kun tuotanto- tai erätilaukset siirtyvät **Päättynyt**-tilaan.

**Tuotannon suorituskyvyn** Power BI -sisältö sisältää tuotanto- ja erätilauksista peräisin olevia tietoja. Raporteissa ei ole kanban-tuotantoihin liittyviä tietoja.

## <a name="accessing-the-power-bi-content"></a>Power BI -sisällön käyttäminen
**Tuotannon suorituskyvyn** Power BI -sisältö näkyy **Tuotannon suorituskyky** -sivulla (**Tuotannonhallinta** \> **Kyselyt ja raportit** \> **Tuotannon suorituskyvyn analyysi** \> **Tuotannon suorituskyky**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mittarit, jotka sisältyvät Power BI -sisältöön

**Tuotannon suorituskyvyn** Power BI -sisältö sisältää raporttisivujoukon. Jokainen sivu koostuu joukosta mittareita, jotka ovat visualisoitu kaavioiden, ruutujen ja taulukoiden muodossa.

Seuraavassa taulukossa on sisältyvien visualisointien yhteenveto.

| Raporttisivu                                | Kaaviot | Ruudut |
|--------------------------------------------|--------|-------|
| Tuotannon suorituskyky                     | <ul><li>Tuotannon määrä päivämäärän mukaan</li><li>Tuotantojen määrä tuote-ja nimikeryhmän mukaan</li><li>Suunniteltujen tuotantojen määrä päivämäärän mukaan</li><li>10 alinta tuotetta ajallaan olon &amp; kokonaisuuden mukaan</li></ul> | <ul><li>Tilauksia yhteensä</li><li>Ajallaan &amp; kokonaisuudessaan</li><li>Kesken – %</li><li>Etuajassa – %</li><li>Myöhässä – %</li></ul> |
| Viat tuotteen mukaan                         | <ul><li>Virheellisten osuus (ppm) päivämäärän mukaan</li><li>Virheellisten osuus (ppm) tuote- ja nimikeryhmän mukaan</li><li>Tuotettu määrä päivämäärän mukaan</li><li>10 merkittävintä tuotetta virheellisten osuuden mukaan</li></ul> | <ul><li>Virheellisten osuus (ppm)</li><li>Virheellisten määrä</li><li>Kokonaismäärä</li></ul> |
| Viallisten trendi tuotteen mukaan                   | Viallisten osuus (ppm) tuotetun määrän mukaan | Viallisten osuus (ppm) |
| Vialliset resurssien mukaan                        | <ul><li>Viallisten osuus (ppm) päivämäärän mukaan</li><li>Viallisten osuus (ppm) resurssin ja toimipaikan mukaan</li><li>Viallisten osuus (ppm) toimenpiteen mukaan</li><li>10 merkittävintä resurssia viallisten osuuden mukaan</li></ul> | Virheellisten määrä |
| Viallisten trendi resurssin mukaan                  | Viallisten osuus (ppm) käsitellyn määrän mukaan | |
| Työtilausten kustannuslaskennan tuotannon varianssit | <ul><li>Tuotannon varianssi päivämäärän ja kustannusryhmän tyypin mukaan</li><li>Tuotannon varianssi toimipaikan ja kustannusryhmän tyypin mukaan</li><li>10 merkittävintä tuotetta, jolla on kielteinen tuotannon varianssi</li><li>10 merkittävintä kielteistä tuotannon varianssia resurssin mukaan</li></ul> | <ul><li>Toteutunut kustannus</li><li>Tuotannon varianssi</li><li>Tuotannon varianssi – %</li></ul> |


## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot

Seuraavia tietoja käytetään **tuotannon suorituskyvyn** Power BI -sisällön raporteissa. Nämä tiedot esitetään koottuina mittauksina, joka vaiheistetaan yksikkösäilössä. Yksikkösäilö on analytiikkaa varten optimoitu Microsoft SQL Server -tietokanta. Lisätietoja yksikkösäilöstä on kohdassa [Power BI:n ja yksikkösäilön integrointi](power-bi-integration-entity-store.md).

Seuraavassa taulukossa on tärkeät koostemitat, joita käytetään Power BI -sisällön perustana.

| Yksikkö                   | Tärkeät koostemitat  | Talous- ja toimintosovellusten tietolähde | Kenttä              |
|--------------------------|-----------------------------|----------------------------------------|--------------------|
| CostCalculation          | CostAmount                  | ProdCalcTransExpanded                  | CostAmount         |
| CostCalculation          | CostMarkup                  | ProdCalcTransExpanded                  | CostMarkup         |
| CostCalculation          | ActualCostAmount            | ProdCalcTransExpanded                  | RealCostAmount     |
| CostCalculation          | RealCostAdjustment          | ProdCalcTransExpanded                  | RealCostAdjustment |
| RouteTransactions        | ErrorQuantity               | ProdRouteTransExpanded                 | QtyError           |
| RouteTransactions        | GoodQuantity                | ProdRouteTransExpanded                 | QtyGood            |
| ProductionOrder          | DaysDelayed                 | ProdTableExpanded                      | DaysDelayed        |
| ProductionOrder          | LeadTime                    | ProdTableExpanded                      | LeadTime           |
| ProductionOrder          | PlannedLeadTime             | ProdTableExpanded                      | PlannedLeadTime    |
| ProductionOrder          | ProductionOrderCount        | ProdTableExpanded                      |                    |
| CoproductCostCalculation | CoproductCostAmount         | PmfCoByProdCalcTransExpanded           | CostAmount         |
| CoproductCostCalculation | CoproductCostMarkup         | PmfCoByProdCalcTransExpanded           | CostMarkup         |
| CoproductCostCalculation | CoproductRealCostAdjustment | PmfCoByProdCalcTransExpanded           | RealCostAdjustment |
| CoproductCostCalculation | CoproductActualCostAmount   | PmfCoByProdCalcTransExpanded           | RealCostAmount     |

Seuraavassa taulukossa on esitetty, miten tärkeitä koostemittoja käytetään luomaan useita laskettuja mittoja sisällön tietojoukossa.

| Mitta                  | Miten mitta on laskettu |
|--------------------------|-------------------------------|
| Tuotannon varianssi, %   | SUM('Tuotannon varianssi'\[Tuotannon varianssi\]) / SUM('Tuotannon varianssi'\[Arvioitu kustannus\]) |
| Kaikki suunnitellut tilaukset       | COUNTROWS('Suunniteltu tuotantotilaus') |
| Etuajassa                    | COUNTROWS(FILTER('Suunniteltu tuotantotilaus', 'Suunniteltu tuotantotilaus'\[Suunniteltu päättymispäivä\] \< 'Suunniteltu tuotantotilaus'\[Tarvepäivä\])) |
| Myöhässä                     | COUNTROWS(FILTER('Suunniteltu tuotantotilaus', 'Suunniteltu tuotantotilaus'\[Suunniteltu päättymispäivä\] \> 'Suunniteltu tuotantotilaus'\[Tarvepäivä\])) |
| Ajallaan                  | COUNTROWS(FILTER('Suunniteltu tuotantotilaus', 'Suunniteltu tuotantotilaus'\[Suunniteltu päättymispäivä\] = 'Suunniteltu tuotantotilaus'\[Tarvepäivä\])) |
| Ajallaan – %                | IF ( 'Suunniteltu tuotantotilaus'\[Ajallaan\] \<\> 0, 'Suunniteltu tuotantotilaus'\[Ajallaan\], IF ('Suunniteltu tuotantotilaus'\[Kaikki suunnitellut tilaukset\] \<\> 0, 0, BLANK()) ) / 'Suunniteltu tuotantotilaus'\[Kaikki suunnitellut tilaukset\] |
| Päätetty                | COUNTROWS(FILTER('Tuotantotilaus', 'Tuotantotilaus'\[On ilmoitettu valmiiksi\] = TRUE)) |
| Virheellisten osuus (ppm)     | IF( 'Tuotantotilaus'\[Kokonaismäärä\] = 0, BLANK(), (SUM('Tuotantotilaus'\[Virheellisten määrä\]) / 'Tuotantotilaus'\[Kokonaismäärä\]) \* 1000000) |
| Viivästyneen tuotannon osuus  | 'Tuotantotilaus'\[Myöhässä \#\] / 'Tuotantotilaus'\[Valmis\] |
| Etuajassa ja kokonaisuudessaan          | COUNTROWS(FILTER('Tuotantotilaus', 'Tuotantotilaus'\[On kokonaisuudessaan\] = TRUE && 'Tuotantotilaus'\[On etuajassa\] = TRUE)) |
| Etuajassa \#                 | COUNTROWS(FILTER('Tuotantotilaus', 'Tuotantotilaus'\[On etuajassa\] = TRUE)) |
| Etuajassa – %                  | IFERROR( IF('Tuotantotilaus'\[Etuajassa \#\] \<\> 0, 'Tuotantotilaus'\[Etuajassa \#\], IF('Tuotantotilaus'\[Tilauksia yhteensä\] = 0, BLANK(), 0)) / 'Tuotantotilaus'\[Tilauksia yhteensä\], BLANK()) |
| Keskeneräinen               | COUNTROWS(FILTER('Tuotantotilaus', 'Tuotantotilaus'\[On kokonaisuudessaan\] = FALSE && 'Tuotantotilaus'\[On ilmoitettu valmiiksi\] = TRUE)) |
| Kesken – %             | IFERROR( IF('Tuotantotilaus'\[Kesken\] \<\> 0, 'Tuotantotilaus'\[Kesken\], IF('Tuotantotilaus'\[Tilauksia yhteensä\] = 0, BLANK(), 0)) / 'Tuotantotilaus'\[Tilauksia yhteensä\], BLANK()) |
| On viivästynyt               | 'Tuotantotilaus'\[On ilmoitettu valmiiksi\] = TRUE && 'Tuotantotilaus'\[Viivästynyt arvo\] = 1 |
| On etuajassa                 | 'Tuotantotilaus'\[On ilmoitettu valmiiksi\] = TRUE && 'Tuotantotilaus'\[Viivästymispäivät\] \< 0 |
| On kokonaisuudessaan               | 'Tuotantotilaus'\[Hyväksytty määrä\] \>= 'Tuotantotilaus'\[Ajoitettu määrä\] |
| On ilmoitettu valmiiksi                | 'Tuotantotilaus'\[Tuotantotilauksen arvo\] = 5 \|\| 'Tuotantotilaus'\[Tuotantotilauksen arvo\] = 7 |
| Myöhässä ja kokonaisuudessaan           | COUNTROWS(FILTER('Tuotantotilaus', 'Tuotantotilaus'\[On kokonaisuudessaan\] = TRUE && 'Tuotantotilaus'\[On viivästynyt\] = TRUE)) |
| Myöhässä \#                  | COUNTROWS(FILTER('Tuotantotilaus', 'Tuotantotilaus'\[On viivästynyt\] = TRUE)) |
| Myöhässä – %                   | IFERROR( IF('Tuotantotilaus'\[Myöhässä \#\] \<\> 0, 'Tuotantotilaus'\[Myöhässä \#\], IF('Tuotantotilaus'\[Tilauksia yhteensä\] = 0, BLANK(), 0)) / 'Tuotantotilaus'\[Tilauksia yhteensä\], BLANK()) |
| Ajallaan ja kokonaisuudessaan        | COUNTROWS(FILTER('Tuotantotilaus', 'Tuotantotilaus'\[On kokonaisuudessaan\] = TRUE && 'Tuotantotilaus'\[On viivästynyt\] = FALSE && 'Tuotantotilaus'\[On etuajassa\] = FALSE)) |
| Ajallaan ja kokonaisuudessaan – %      | IFERROR( IF('Tuotantotilaus'\[Ajallaan ja kokonaisuudessaan\] \<\> 0, 'Tuotantotilaus'\[Ajallaan ja kokonaisuudessaan\], IF('Tuotantotilaus'\[Valmis\] = 0, BLANK(), 0)) / 'Tuotantotilaus'\[Valmis\], BLANK()) |
| Tilauksia yhteensä             | COUNTROWS('Tuotantotilaus') |
| Kokonaismäärä           | SUM('Tuotantotilaus'\[Hyväksytty määrä\]) +('Tuotantotilaus'\[Viallinen määrä\]) |
| Viallisten osuus (ppm)        | IF( 'Reititystapahtumat'\[Käsitelty määrä\] = 0, BLANK(), (SUM('Reititystapahtumat'\[Viallinen määrä\]) / 'Reititystapahtumat'\[Käsitelty määrä\]) \* 1000000) |
| Yhdistetty virheellisten osuus (ppm) | IF( 'Reititystapahtumat'\[Yhdistetty kokonaismäärä\] = 0, BLANK(), (SUM('Reititystapahtumat'\[Viallinen määrä\]) / 'Reititystapahtumat'\[Yhdistetty kokonaismäärä\]) \* 1000000) |
| Käsitelty määrä       | SUM('Reititystapahtumat'\[Hyväksytty määrä\]) + SUM('Reititystapahtumat'\[Viallisten määrä\]) |
| Yhdistetty kokonaismäärä     | SUM('Tuotantotilaus'\[Hyväksytty määrä\]) + SUM('Reititystapahtumat'\[Viallisten määrä\]) |

Seuraavassa taulukossa on tärkeimmät koostemittojen osittamisen suodattimina käytetyt dimensiot, joiden avulla saavutetaan suurempi rakeisuus ja paremmat analyysitiedot.

| Kokonaisuus                    | Esimerkkejä määritteistä                                        |
|---------------------------|---------------------------------------------------------------|
| Ilmoitettu valmiiksi -päivämäärä | Valmistumisen (valmiiksi ilmoittamisen) päivämäärän, kuukauden ja vuoden poikkeama                 |
| Päättymispäivä                | Päättäneen kuukauden poikkeama ja kuukausi                                  |
| Tarvepäivä          | Tarvepäivän kuukauden poikkeama ja tarvepäivä            |
| Reititystapahtuman päivämäärä    | Reititystapahtuman kuukauden poikkeama ja päivämäärä                       |
| Toimipaikat                     | Toimipaikkojen tunnus, toimipaikan nimi, osavaltio ja paikkakunta                          |
| Yksiköt                  | Tunnus ja nimi                                                   |
| Resurssit                 | Resurssin tunnus, resurssin nimi, resurssin tyyppi ja resurssiryhmä |
| Tuotteet                  | Tuotenumero, tuotteen nimi, nimiketunnus ja nimikeryhmä         |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
