---
title: "Kustannuslaskennan analyysin Power BI -sisältö"
description: "Tässä aiheessa kuvataan, mitä kuuluu kustannuslaskennan analyysin Power BI -sisältöön. Siinä kuvataan, miten avaat Power BI -raportit. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä."
author: YuyuScheller
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 1d19276331a4278f44ad14292ed434c49b74d727
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017

---

# <a name="cost-accounting-analysis-power-bi-content"></a>Kustannuslaskennan analyysin Power BI -sisältö

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, mitä **Kustannuslaskenta-analyysi** – Power BI -sisältöön sisältyy. Siinä kuvataan, miten avaat Power BI -raportit. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä.

## <a name="overview"></a>Yleiskuvaus

**Kustannuslaskenta-analyysi** – Microsoft Power BI -sisältö on tarkoitettu kustannuksista vastaaville henkilöille tai kenelle tahansa, joka on vastuussa organisaation kustannusseurannasta. Se sisältää tärkeitä mittareita, kuten kustannukset, suuruus ja kustannushinta budjetin kustannusten, todellisten kustannusten ja joustavan budjetin kustannusten mukaan. Se käyttää **Kustannuslaskentamoduulin** tapahtumatietoja ja tarjoaa koko organisaation kustannusten kokoomanäytön yhtenä raportointivaluuttana. Esimiehet voit suodattaa tietoja kustannusobjektien mukaan suorittaakseen kustannusseurantaa organisaatioyksiköille, vaikka organisaatiolla voi olla useita yrityksiä. 

Koska **Kustannuslaskenta-analyysi** – Power BI -sisältö korostaa toteutuneiden kustannusten ja suunniteltujen kustannusten eroja, johtajat voivat saada ilmoituksen positiivisista ja negatiivisista trendeistä omissa toiminnallisissa yksiköissään. Esimiehet voivat porautua kustannustasohierarkioihin tai yksittäisiin kustannustasoihin. Tällä tavoin esimiehet saat yksityiskohtaista tietoa tapahtuneista kustannuspoikkeamista, jonka perusteella he voivat toimia tehokkaasti. 

**Kustannuslaskenta-analyysi** -sisällön ansiosta kustannuslaskijat voivat analysoida, miten kustannukset kulkevat koko organisaation kustannusobjektien läpi. 

Katso lisätietoja kustannuslaskennasta ohjeaiheesta [Kustannuslaskennan aloitussivu](/dynamics365/unified-operations/financials/cost-accounting/cost-accounting-home-page). 

Määrittämällä käyttäjätason suojauksen kustannuslaskentaan ja yhdistämällä sen rivitason suojaukseen Power BI:ssä, voit myöntää kaikille kustannusobjektien omistajille pääsyn **Kustannuslaskennan analyysin** Power BI -sisältöön. Kaikki visualisoinnin data sitten suodatetaan sen käyttöoikeustason perusteella, jota ohjataan kustannuslaskennassa. Saat lisätietoja käyttöoikeustason suojauksesta ja rivitason suojauksesta ohjeaiheesta [Kustannuslaskennan Power BI -sisällön suojauksen määrittäminen](setup-security-cost-accounting-content-pack.md).

## <a name="accessing-the-power-bi-content"></a>Power BI -sisällön käyttö
Löydät **Kustannuslaskennan analyysin** Power BI -sisällön Microsoft Dynamics Lifecycle Services (LCS):n jaettujen resurssien kirjastosta. Lisätietoja sisällön lataamisesta ja sen käyttöönottamisesta organisaatiossa on ohjeaiheessa [Microsoftin ja kumppaneiden Power BI -sisältö LCS-sovelluksessa](power-bi-content-microsoft-partners.md). Katso Power BI -sisällön käyttöönotosta kertova esittely Office Mixin kohdassa [Microsoftin ja kumppaneiden Power BI -sisältö Dynamics Lifecycle Services -sovelluksessa](https://mix.office.com/watch/9puyb1b2xs1w).

Muista ladata käyttämääsi Microsoft Dynamics 365 -versiota vastaava **Kustannuslaskenta-analyysi** -sisältö.

> [!NOTE]
> KB 4011327 on edellytys tämän Power BI -sisällön käytölle. Kun olet kirjautunut LCS:ään, voit avata KB-artikkelin osoitteessa <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>.

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mittareita, jotka sisältyvät Power BI -sisältöön
Sisältö sisältää joukon raporttisivuja. Jokainen sivu koostuu joukosta mittareita, jotka ovat visualisoitu kaavioiden, ruutujen ja taulukoiden muodossa. Seuraavassa taulukossa on yleiskatsaus visualisoinneista **kustannuslaskennan analyysin** Power BI -sisällössä.

| Raporttisivu                      | Kaavio                                                                                                                         | Ruutu                                          |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Kustannusseuranta tilikauden mukaan    | Todelliset kustannukset ja budjetin kustannukset kustannuselementin hierarkiatason mukaan                                                                   | Todellinen kustannus vs. budjettikustannus                    |
|                                  | Budjetin varianssi kustannuselementin hierarkiatason mukaan                                                                               | Todellinen kustannushinta vs. budjetin kustannushinta          |
|                                  | Top 10 budjettivarianssi prosentteina kustannustekijän mukaan                                                                          | Todellinen suuruus vs budjetin suuruus          |
| Kustannusseuranta vuoden alusta     | Todelliset kustannukset ja budjetin kustannukset kalenterivuoden ajanjakson mukaan                                                                           | Todellinen kustannus vs. budjettikustannus                    |
|                                  | Budjetin varianssi kalenterivuoden ajanjakson mukaan                                                                                       | Todellinen kustannushinta vs. budjetin kustannushinta          |
|                                  | Top 10 budjettivarianssi prosentteina kustannustekijän mukaan                                                                          | Todellinen suuruus vs budjetin suuruus          |
| Kustannushinta tilikauden mukaan         | Todellinen kustannushinta kustannustoiminnan mukaan                                                                                             | Todellinen kustannushinta vs. budjetin kustannushinta          |
|                                  | Toteutunut kustannushinta, budjetin kustannushinnan varianssi, budjetin kustannushinnan prosentti ja budjetin kustannushinta kustannuselementin hierarkiatason mukaan | Todellinen suuruus vs budjetin suuruus          |
|                                  | Budjetin varianssi kustannuselementin hierarkiatason mukaan                                                                               |                                               |
|                                  | Top 10 budjettivarianssi prosentteina kustannustekijän mukaan                                                                          |                                               |
| Joustava budjetti kirjanpitokauden mukaan | Todelliset kustannukset , budjetin kustannukset ja joustava budjetin kustannus kustannuselementin hierarkiatason mukaan                                             | Todellinen suuruus vs budjetin suuruus          |
|                                  | Budjetin varianssi ja joustavan budjetin varianssi kustannuselementin hierarkiatason mukaan                                                  | Todellinen kustannus vs. joustavan budjetin kustannus           |
|                                  | Todelliset kustannukset , budjetin kustannukset ja joustavan budjetin kustannus kustannustoiminnan ja kustannuselementin hierarkiatason mukaan                                  | Todellinen kustannushinta vs. joustavan budjetin kustannushinta |
| Kustannusraportti tilikauden mukaan  | Todelliset kustannukset kustannuselementin hierarkiatason mukaan ja kustannusobjektin dimension jäsenen nimen mukaan                                             |                                               |
|                                  | Todelliset kustannukset kustannusobjektin dimension jäsenen nimen mukaan ja kustannustason dimension jäsenen nimen mukaan                                       |                                               |

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot
Seuraavilla tiedoilla täytetään **Kustannuslaskenta-analyysi** – Power BI -sisällön raporttisivut. Nämä tiedot esitetään koottuina mittauksina, joka vaiheistetaan yksikkösäilössä. Yksikkösäilö on analytiikkaa varten optimoitu Microsoft SQL Server -tietokanta. Lisätietoja on ohjeaiheessa [yleiskatsaus Power BI:n integraatiosta yksikkökaupan kanssa](power-bi-integration-entity-store.md). 

Seuraavia tärkeitä koostettuja mittoja käytetään sisällön perustana.

| Kokonaisuus                  | Tärkeät koostemitat | Dynamics 365:n tietolähde      | Kenttä     | kuvaus                                        |
|-------------------------|---------------------------|-----------------------------------|-----------|----------------------------------------------------|
| Kustannuslaskennan tapahtumat | SUM(Summa)               | CAMDATAAggregatedCostEntry        | Summa    | Summa kustannuslaskennan kirjanpitovaluuttana. |
| Tilastomerkinnät     | SUM(Suuruus)            | CAMDATAAggregatedStatisctialEntry | Suuruus |                                                    |

Seuraavassa taulukossa on esitetty, miten tärkeitä koostemittoja käytetään luomaan useita laskettuja mittoja sisällön tietojoukossa.

| Mitta                                       | Miten mitta on laskettu                                                                                          |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Toteutunut kustannus                                   | CALCULATE('Cost accounting entries'\[Measure\], 'Transaction versions'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 0)            |
| Budjetoitu kustannus                                   | CALCULATE('Cost accounting entries'\[Measure\], 'Transaction versions'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 1)            |
| Budjetin kustannusten varianssi                          | \[Budget cost\] - \[Actual cost\]                                                                                      |
| Budjettivarianssin prosentti                    | IF(\[Budget cost\] = 0, blank(), \[Budget variance\] / \[Budget cost\])                                                |
| Todellinen suuruus                              | CALCULATE('Statistical entries'\[FullMagnitude\], 'Transaction versions'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 0)          |
| Budjetin suuruus                              | CALCULATE(\[FullMagnitude\], 'Transaction versions'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 1)                               |
| Tilastollinen budjetin varianssi                   | \[Budget magnitude\] - \[Actual magnitude\]                                                                            |
| Tilastollinen budjettivarianssin prosentti        | IF(\[Budget magnitude\] = 0, blank(), \[Statistical budget variance\] / \[Budget magnitude\])                          |
| Toteutunut kustannushinta                              | IF(\[Actual magnitude\] = 0, BLANK(), \[Actual cost\] / \[Actual magnitude\])                                          |
| Budjetin kustannushinta                              | IF(\[Budget magnitude\] = 0, BLANK(), \[Budget cost\] / \[Budget magnitude\])                                          |
| Budjettikustannushinnan varianssi                     | \[Budget cost rate\] - \[Actual cost rate\]                                                                            |
| Budjettikustannushinnan varianssin prosentti          | IF(\[Budget cost\] = 0, blank(), \[Budget cost rate variance\] / \[Budget cost rate\])                                 |
| Kiinteä budjettikustannus                             | CALCULATE(\[Budget cost\], 'Cost accounting entries'\[COSTBEHAVIOR\] = 1)                                              |
| Muuttuva budjetin kustannus                          | CALCULATE(\[Budget cost\], 'Cost accounting entries'\[COSTBEHAVIOR\] = 2)                                              |
| Kiinteä joustava budjettikustannus                    | \[Fixed budget cost\]                                                                                                  |
| Muuttuva joustava budjettikustannus                 | IF(\[Budget magnitude\] = 0, BLANK(), (\[Variable budget cost\] / \[Budget magnitude\]) \* \[Actual magnitude\])       |
| Joustava budjettikustannus                          | \[Fixed flexible budget cost\] + \[Variable flexible budget cost\]                                                     |
| Joustava budjetin varianssi                      | \[Flexible budget cost\] - \[Actual cost\]                                                                             |
| Joustavan budjettivarianssin prosentti           | IF(\[Flexible budget cost\] = 0, BLANK(), \[Flexible budget variance\] / \[Flexible budget cost\])                     |
| Joustava budjettikustannushinta                     | IF(\[Actual magnitude\] = 0, BLANK(), \[Flexible budget cost\] / \[Actual magnitude\])                                 |
| Joustavan budjetin kustannushinnan varianssi            | \[Flexible budget cost rate\] - \[Actual cost rate\]                                                                   |
| Joustava budjettikustannushinnan varianssin prosentti | IF(\[Flexible budget cost rate\] = 0, BLANK(), \[Flexible budget cost rate variance\] / \[Flexible budget cost rate\]) |

Suodattimina käytetään seuraavia tärkeimpiä dimensioita osittamaan koostemitat, jotta saavutetaan suurempi rakeisuus ja saadaan syvempiä analyyttisiä näkemyksiä.

| Kokonaisuus                             | Esimerkkejä määritteistä                                                                                               |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Kustannuslaskennan kirjanpidot            | Kustannuslaskennan kirjanpito                                                                                               |
| Kustannusseurantayksiköt                 | Kustannusseurannan nimi                                                                                               |
| Kustannustason dimensiot            | Kustannustason dimension nimi, kustannustason dimension jäsenen nimi, kustannustason dimension jäsenen nimi          |
| Kustannusobjektin dimensiot             | Kustannusobjektin dimension nimi, kustannusobjektin dimension jäsenen nimi, kustannusobjektin dimension jäsenen nimi              |
| Tilastodimensiot             | Tilastollinen dimension nimi, Tilastollinen dimension jäsenen nimi, Tilastollinen dimension jäsenen nimi              |
| Kustannusobjektin dimensiohierarkiat  | Kustannusobjektin dimension hierarkian nimi, Kustannusobjektin dimension hierarkiataso, Kustannusobjektin dimension hierarkiapuu    |
| Kustannustason dimensiohierarkiat | Kustannustason dimension hierarkian nimi, Kustannustason dimension hierarkiataso, Kustannustason dimension hierarkiapuu |
| Tilastodimension hierarkiat  | Tilastodimension hierarkian nimi, Tilastodimension hierarkiataso, Tilastodimension hierarkiapuu    |
| Tapahtuman versiot               | Version nimi                                                                                                         |
| Kirjanpidon kalenterit                   | Kalenteri, kalenterin kuvaus                                                                                       |
| Tilikaudet                       | Kalenterivuosi                                                                                                        |
| Tilikaudet                     | Kalenterivuoden kausi                                                                                                 |

