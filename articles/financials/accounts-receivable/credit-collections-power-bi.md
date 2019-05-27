---
title: Luotonvalvonnan hallinnan Power BI-sisältö
description: Tässä ohjeaiheessa kerrotaan, mitä luotonvalvonnan hallinnan Power BI -sisältö sisältää. Siinä selitetään, miten sisältyvät Power BI -raportit avataan, sekä kerrotaan sisällön muodostamisessa käytettävistä tietomallista ja yksiköistä.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a80a180623d1cca77c633f12bcd92a088e089ee5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547229"
---
# <a name="credit-and-collections-management-power-bi-content"></a>Luotonvalvonnan hallinnan Power BI-sisältö

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, mitä **luotonvalvonnan hallinnan** Microsoft Power BI -sisältö sisältää. Siinä selitetään, miten sisältyvät Power BI -raportit avataan, sekä kerrotaan sisällön muodostamisessa käytetyistä tietomallista ja yksiköistä.

## <a name="overview"></a>Yleiskuvaus

**Luotonvalvonnan hallinnan** Power BI -sisältö luotiin luotonvalvonnan esimiehille ja perimisasiamiehille. Se sisältää keskeiset luotonvalvonnan mittarit, kuten selvittämätön päivämyynti, erääntynyt saldo, luottoriski ja luottorajan ylittävät asiakkaat. Se käyttää tapahtumatietoja ja siinä on kaikkien yritysten luotonvalvonnan koostenäkymät. Siinä on myös yritys-, asiakasryhmä- ja asiakaskohtainen erittely.

Tässä Power BI -sisällössä on 10 raporttisivua:

- kaksi yhteenvetosivua (yksi luoton yhteenvetosivu ja yksi perinnän yhteenvetosivu)
- kahdeksan tietosivua, jossa luotonvalvonnan mittaritiedot, jotka käsittävät kattavasti eri dimensiot.

Kaikki summat näytetään järjestelmän valuuttana. Järjestelmän valuutta määritetään **Järjestelmän parametrit** -sivulla.

Oletusarvoisesti näytetään nykyisen yrityksen luotonvalvonnan tiedot. Voit tarkastella kaikkien yritysten tietoja määrittämällä roolille **CustCollectionsBICrossCompany**-tehtävän.

## <a name="accessing-the-power-bi-content"></a>Power BI -sisällön käyttäminen
**Luotonvalvonnan hallinnan** Power BI -sisältö näkyy **Asiakkaan luotonvalvonta** -työtilassa.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Raportit, jotka sisältyvät Power BI -sisältöön

Power BI -sisältö **CustCollectionsBICrossCompany** sisältää raportin, jossa on mittarijoukko. Nämä mittarit visualisoidaan kaavioina, ruutuina ja taulukoina. Seuraavassa taulukossa on yleiskatsaus visualisoinneista **CustCollectionsBICrossCompany** Power BI -sisällössä.

| Raporttisivu                 | Visualisointi |
|-----------------------------|---------------|
| Perinnän yleiskatsaus        | <ul><li>Asiakkaiden erääntyneet</li><li>Luottorajan ylittäneet asiakkaat</li><li>DSO 30 päivää</li><li>Avoimet tapaukset</li><li>Päiviä tapauksen sulkemiseen keskimäärin</li><li>Avoimet tehtävät</li><li>Päiviä tehtävän sulkemiseen keskimäärin</li><li>Avoimet korkolaskut</li><li>Avoimet maksukehotukset</li><li>Asiakaspito</li><li>Myyntipito</li><li>Erääntyneet saldot</li><li>Perintätilan summat</li><li>Perintäkoodin summat</li><li>Poiskirjaus syyn mukaan</li><li>Erääntynyt saldo alueen mukaan</li><li>Odotetut maksut</li></ul> |
| Luoton yhteenveto             | <ul><li>Asiakkaiden erääntyneet</li><li>Luottorajan ja erääntyneen saldon vertailu</li><li>Luottorajan ylittäneiden asiakkaiden ruudukko</li><li>Luottorajan ylittäneet asiakkaat yrityksen mukaan</li><li>Luottorajan ja kokonaisluottorajan vertailu</li><li>Luottorajan ja aluekohtaisen käytetyn luoton vertailu</li><li>Asiakkaat luottokelpoisuusluokituksen mukaan</li></ul> |
| Luottoraja                | <ul><li>Luottoraja</li><li>Luottorajan tiedot</li><li>Asiakaskohtainen luottoraja</li><li>Luottoraja asiakasryhmän mukaan</li><li>Luottoraja luottokelpoisuusluokituksen ja yrityksen mukaan</li><li>Luottoraja vs. alueella käytetty luotto</li></ul> |
| Luottorajan ylittäneet asiakkaat | <ul><li>Luottorajan ylittäneet asiakkaat</li><li>Tiedot luottorajan ylittäneistä asiakkaista</li><li>Luottorajan ylittäneet asiakkaat yrityksen mukaan</li><li>Luottorajan ylittäneet asiakkaat asiakasryhmän mukaan</li><li>Luottorajan ylittäneet asiakkaat alueen mukaan</li></ul> |
| Asiakkaiden erääntyneet          | <ul><li>Asiakkaiden erääntyneet</li><li>Asiakkaan erääntyneiden tiedot</li><li>Asiakkaan erääntyneet yrityksen mukaan</li><li>Asiakkaan erääntyneet asiakasryhmän mukaan</li><li>Asiakkaan erääntyneet alueen mukaan</li></ul> |
| Erääntyneet saldot               | <ul><li>Erääntyneet saldot</li><li>Erääntyneiden saldojen tiedot</li><li>Erääntyneet saldot yrityksen mukaan</li><li>Erääntyneet saldot asiakasryhmän mukaan</li></ul> |
| Odotetut maksut           | <ul><li>Odotetut maksut</li><li>Odotettujen maksujen tiedot</li><li>Odotetut maksut yrityksen mukaan</li><li>Odotetut maksut asiakasryhmän mukaan</li><li>Odotetut maksut alueen mukaan</li></ul> |
| Poistot                  | <ul><li>Poistot alueen mukaan</li><li>Poistojen tiedot.</li><li>Poistot päätilin mukaan</li><li>Poistot yrityksen mukaan</li><li>Poistot asiakasryhmän mukaan</li><li>Poistot alueen mukaan</li></ul> |
| Koron ja maksukehotuksen tila          | <ul><li>Riidanalainen</li><li>Maksulupaus rikottu</li><li>Maksulupaus</li><li>Perinnän tilatiedot</li><li>Perintätilan summat</li><li>Avoimet tapaukset</li><li>Avoimet tehtävät</li></ul> |
| Maksukehotukset         | <ul><li>Perintäkoodin summat</li><li>Perintäkoodin summan tiedot</li><li>Maksukehotuksen summa yrityksen mukaan</li><li>Maksukehotuksen summa asiakasryhmän mukaan</li><li>Maksukehotuksen summa alueen mukaan</li></ul> |

Kaikkien raporttien kaavioita ja ruutuja voi suodattaa sekä kiinnittää koontinäyttöön. Lisätietoja suodattamisesta ja kiinnittämisestä Power BI:ssä on kohdassa [Koontinäytön luominen ja määrittäminen](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Voit viedä visualisoinnin kokoamat pohjana olevat tiedot pohjana olevien tietojen vientitoiminnolla.

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot

**Luotonvalvonnan hallinnan** Power BI -sisällön raportissa käytetään seuraavia tietoja. Nämä tiedot esitetään koottuina mittauksina, joka vaiheistetaan yksikkösäilössä. Yksikkösäilö on analytiikkaa varten optimoitu Microsoft SQL Server -tietokanta. Lisätietoja on kohdassa [Power BI:n ja yksikkösäilön integroinnin yleiskatsaus](../../dev-itpro/analytics/power-bi-integration-entity-store.md).


|                   Kokonaisuus                    |      Tärkeät koostemitat      |             Tietolähde              |                           Kenttä                            |                                    kuvaus                                     |
|---------------------------------------------|--------------------------------------|--------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------------|
| CustCollectionsBIActivitiesAverageCloseTime | NumOfActivities, AveragecClosedTime  |            smmActivities             | AverageOfChildren(AverageClosedTime) Count(ActivityNumber) |     Suljettujen tehtävien määrä ja kyseisten tehtävien keskimääräinen sulkemisaika.     |
|       CustCollectionsBIActivitiesOpen       |            ActivityNumber            |            smmActivities             |                   Count(ActivityNumber)                    |                           Avoimien tehtävien määrä.                            |
|        CustCollectionsBIAgedBalances        |             AgedBalances             |  CustCollectionsBIAgedBalancesView   |                 Sum(SystemCurrencyBalance)                 |                             Erääntyneiden saldojen summa.                              |
|        CustCollectionsBIBalancesDue         |         SystemCurrencyAmount         |   CustCollectionsBIBalanceDueView    |                 Sum(SystemCurrencyAmount)                  |                           Myöhässä olevat summat.                            |
|    CustCollectionsBICaseAverageCloseTIme    |  NumOfCases, CaseAverageClosedTime   |      CustCollectionsCaseDetail       | AverageOfChildren(CaseAverageClosedTime) Count(NumOfCases) |        Suljettujen tapauksien määrä ja kyseisten tapauksien keskimääräinen sulkemisaika.        |
|         CustCollectionsBICasesOpen          |                CaseId                |      CustCollectionsCaseDetail       |                       Count(CaseId)                        |                              Avoimien tapauksien määrä.                              |
|      CustCollectionsBICollectionLetter      |         CollectionLetterNum          |       CustCollectionLetterJour       |                 Count(CollectionLetterNum)                 |                       Avoimien maksukehotusten määrä.                        |
|   CustCollectionsBICollectionLetterAmount   |       CollectionLetterAmounts        | CustCollectionsBIAccountsReceivables |                 Sum(SystemCurrencyAmount)                  |                     Kirjattujen maksukehotusten saldo.                      |
|      CustCollectionsBICollectionStatus      |       CollectionStatusAmounts        | CustCollectionsBIAccountsReceivables |                 Sum(SystemCurrencyAmount)                  |                Niiden tapahtumien saldo, joilla on perintätila.                 |
|           CustCollectionsBICredit           | CreditExposed, AmountOverCreditLimit |     CustCollectionsBICreditView      |       Sum(CreditExposed), Sum(AmountOverCreditLimit)       | Luottoriskien summa ja summa, jolla asiakkaat ovat ylittäneet luottorajansa. |
|         CustCollectionsBICustOnHold         |               Estetty                |      CustCollectionsBICustTable      |                       Count(Blocked)                       |                     Pidossa olevien asiakkaiden määrä.                      |
|            CustCollectionsBIDSO             |                DSO30                 |       CustCollectionsBIDSOView       |                  AverageOfChildren(DSO30)                  |                        30 päivän selvittämätön päivämyynti.                         |
|      CustCollectionsBIExpectedPayment       |           ExpectedPayment            | CustCollectionsBIExpectedPaymentView |                 Sum(SystemCurrencyAmounts)                 |                 Seuraavan vuoden kuluessa odotettujen maksujen summa.                 |
|        CustCollectionsBIInterestNote        |             InterestNote             |           CustInterestJour           |                    Count(InterestNote)                     |                Luotujen korkolaskujen määrä.                |
|        CustCollectionsBISalesOnHold         |               SalesId                |              SalesTable              |                       Count(SalesId)                       |                 Pidossa olevien myyntitilausten kokonaismäärä.                 |
|          CustCollectionsBIWriteOff          |            WriteOffAmount            |    CustCollectionsBIWriteOffView     |                 Sum(SystemCurrencyAmount)                  |                Poistettujen tapahtumien summa.                 |

