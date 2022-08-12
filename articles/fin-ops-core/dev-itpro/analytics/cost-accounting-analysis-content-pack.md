---
title: Kustannuslaskenta-analyysin Power BI -sisältö
description: Tässä artikkelissa kuvataan, mitä kuuluu kustannuslaskennan analyysin Power BI -sisältöön.
author: AndersGirke
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom:
- "270274"
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.openlocfilehash: 19dd250141894d1551fc4e54257f05ab5008d110
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/28/2022
ms.locfileid: "9205963"
---
# <a name="cost-accounting-analysis-power-bi-content"></a>Kustannuslaskenta-analyysin Power BI -sisältö

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, mitä kuuluu **kustannuslaskennan analyysin** Microsoft Power BI -sisältöön. Siinä selitetään, miten sisältyvät Power BI -raportit avataan, sekä kerrotaan sisällön muodostamisessa käytetyistä tietomallista ja yksiköistä.

## <a name="overview"></a>Yleiskuvaus

**Kustannuslaskenta-analyysin** Power BI -sisältö on tarkoitettu kustannuksista vastaaville henkilöille tai kenelle tahansa, joka on vastuussa organisaation kustannusseurannasta. Se sisältää tärkeitä mittareita, kuten kustannukset, suuruus ja kustannushinta budjetin kustannusten, todellisten kustannusten ja joustavan budjetin kustannusten mukaan. Se käyttää **Kustannuslaskentamoduulin** tapahtumatietoja ja tarjoaa koko organisaation kustannusten kokoomanäytön yhtenä raportointivaluuttana. Esimiehet voit suodattaa tietoja kustannusobjektien mukaan suorittaakseen kustannusseurantaa organisaatioyksiköille, vaikka organisaatiolla voi olla useita yrityksiä.

Koska **Cost accounting analysis** –sisältö korostaa toteutuneiden kustannusten ja suunniteltujen kustannusten eroja, johtajat voivat saada ilmoituksen positiivisista ja negatiivisista trendeistä omissa toiminnallisissa yksiköissään. Esimiehet voivat porautua kustannustasohierarkioihin tai yksittäisiin kustannustasoihin. Tällä tavoin esimiehet saat yksityiskohtaista tietoa tapahtuneista kustannuspoikkeamista, jonka perusteella he voivat toimia tehokkaasti.

**Kustannuslaskenta-analyysi** -sisällön ansiosta kustannuslaskijat voivat analysoida, miten kustannukset kulkevat koko organisaation kustannusobjektien läpi.

Katso lisätietoja kustannuslaskennasta ohjeaiheesta [Kustannuslaskennan aloitussivu](../../../finance/cost-accounting/cost-accounting-home-page.md).

Määrittämällä käyttäjätason suojauksen kustannuslaskentaan ja yhdistämällä sen rivitason suojaukseen Power BI:ssä, voit myöntää kaikille kustannusobjektien omistajille pääsyn **kustannuslaskennan analyysin** Power BI -sisältöön. Kaikki visualisoinnin data sitten suodatetaan sen käyttöoikeustason perusteella, jota ohjataan kustannuslaskennassa. Lisätietoja käyttöoikeustason suojauksesta ja rivitason suojauksesta on kohdassa [Kustannuslaskenta-analyysin Power BI -sisällön suojauksen määrittäminen](setup-security-cost-accounting-content-pack.md).

## <a name="accessing-the-power-bi-content"></a>Power BI -sisällön käyttäminen
Löydät **kustannuslaskennan analyysin** Power BI -sisällön Microsoft Dynamics Lifecycle Services (LCS):n jaettujen resurssien kirjastosta. Lisätietoja sisällön lataamisesta ja sen käyttöönottamisesta organisaatiossa on kohdassa [Microsoftin ja kumppaneiden Power BI -sisältö LCS-sovelluksessa](/archive/blogs/dynamicsaxbi/power-bi-content-from-microsoft-and-your-partners).

Muista ladata käyttämääsi Microsoft Dynamics 365 -versiota vastaava **Kustannuslaskenta-analyysi** -sisältö.

> [!NOTE]
> KB 4011327 on edellytys tämän Power BI -sisällön käytölle. Kun kirjaudut LCS:ään, voit siirtyä KB-artikkeliin <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>.

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mittarit, jotka sisältyvät Power BI -sisältöön
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
Seuraavilla tiedoilla täytetään **kustannuslaskennan analyysin** Power BI -sisällön raporttisivut. Nämä tiedot esitetään koottuina mittauksina, joka vaiheistetaan yksikkösäilössä. Yksikkösäilö on analytiikkaa varten optimoitu Microsoft SQL Server -tietokanta. Lisätietoja on kohdassa [Power BI:n ja yksikkösäilön integraatio](power-bi-integration-entity-store.md).

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
