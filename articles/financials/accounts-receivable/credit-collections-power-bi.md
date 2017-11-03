---
title: "Luotonvalvonnan hallinta – Power BI -sisältö"
description: "Tässä ohjeaiheessa kerrotaan, mitä luotonvalvonnan hallinnan Power BI -sisältö sisältää. Siinä kuvataan, miten avaat Power BI -raportit. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations. Core
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 7aec3d81fca86abdab4f5fcee54f832f917ffe92
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="credit-and-collections-management-power-bi-content"></a>Luotonvalvonnan hallinta – Power BI -sisältö

Tässä ohjeaiheessa kerrotaan, mitä **Luotonvalvonnan hallinta** – Power BI -sisältö sisältää. Siinä kuvataan, miten avaat Power BI -raportit. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä.

## <a name="overview"></a>Yleiskuvaus

**Luotonvalvonnan hallinta** – Power BI -sisältö luotiin luotonvalvonnan esimiehille ja perimisasiamiehille. Se sisältää keskeiset luotonvalvonnan mittarit, kuten selvittämätön päivämyynti, erääntynyt saldo, luottoriski ja luottorajan ylittävät asiakkaat. Se käyttää tapahtumatietoja ja siinä on kaikkien yritysten luotonvalvonnan koostenäkymät. Siinä on myös yritys-, asiakasryhmä- ja asiakaskohtainen erittely.

Tässä Power BI -sisällössä on 10 raporttisivua:

- kaksi yhteenvetosivua (yksi luoton yhteenvetosivu ja yksi perinnän yhteenvetosivu)
- kahdeksan tietosivua, jossa luotonvalvonnan mittaritiedot, jotka käsittävät kattavasti eri dimensiot.

Kaikki summat näytetään järjestelmän valuuttana. Järjestelmän valuutta määritetään **Järjestelmän parametrit** -sivulla.

Oletusarvoisesti näytetään nykyisen yrityksen luotonvalvonnan tiedot. Voit tarkastella kaikkien yritysten tietoja määrittämällä roolille **CustCollectionsBICrossCompany**-tehtävän.

## <a name="accessing-the-power-bi-content"></a>Power BI -sisällön käyttö
Jos käytössä on Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin heinäkuun 2017 päivitystä, **Luotonvalvonnan hallinta** – Power BI -sisältö näkyy **Asiakkaan luotonvalvonta** -työtilassa.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Raportit, jotka sisältyvät Power BI -sisältöön

Power BI -sisältö **CustCollectionsBICrossCompany** sisältää raportin, jossa on mittarijoukko. Nämä mittarit visualisoidaan kaavioina, ruutuina ja taulukoina. Seuraavassa taulukossa on yleiskatsaus visualisoinneista Power BI -sisällössä **CustCollectionsBICrossCompany**.

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

Kaikkien raporttien kaavioita ja ruutuja voi suodattaa sekä kiinnittää koontinäyttöön. Lisätietoja suodattamisesta ja kiinnittämisestä Power BI -ohjelmassa löydät artikkelista [Koontinäytön luominen ja määrittäminen](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Voit viedä visualisoinnin kokoamat pohjana olevat tiedot pohjana olevien tietojen vientitoiminnolla.

## <a name="extending-the-power-bi-content"></a>Power BI -sisällön laajentaminen
Jos käytät Microsoft Dynamics Lifecycle Servicesin (LCS) sisältöpaketteja, voit tehdä erinomaisia analyyseja henkilöille, jotka eivät käytä Finance and Operationsia. Voit muokata näitä sisältöpaketit sisältämään muita raportteja ja visuaalisia tietoja ja julkaista sitten sisältöpaketit analysoitavaksi Power BI.com -vuokraajassa.

**Luotonvalvonnan hallinta** – Power BI -sisältö sijaitsee LCS:n Jaettu omaisuus -kirjastossa. Lisätietoja sisällön lataamisesta ja sen käyttöönottamisesta organisaatiossa on ohjeaiheessa [Microsoftin ja kumppaneiden Power BI -sisältö LCS-sovelluksessa](../../dev-itpro/analytics/power-bi-content-microsoft-partners.md). Katso Power BI -sisällön käyttöönotosta kertova esittely Office Mixin kohdassa [Microsoftin ja kumppaneiden Power BI -sisältö Dynamics Lifecycle Services -sovelluksessa](https://mix.office.com/watch/9puyb1b2xs1w).

Muista ladata käyttämääsi Finance and Operations -versiota vastaava **Luotonvalvonnan hallinta** – Power BI -sisältö.

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot

**Luotonvalvonnan hallinta** – Power BI -sisällön raportissa käytetään seuraavia tietoja. Nämä tiedot esitetään koottuina mittauksina, joka vaiheistetaan yksikkösäilössä. Yksikkösäilö on analytiikkaa varten optimoitu Microsoft SQL Server -tietokanta. Lisätietoja on ohjeaiheessa [yleiskatsaus Power BI:n integraatiosta yksikkökaupan kanssa](../../dev-itpro/analytics/power-bi-integration-entity-store.md).

| Kokonaisuus                                      | Tärkeät koostemitat           | Tietolähde                                 | Kenttä                                                      | kuvaus |
|---------------------------------------------|--------------------------------------|---------------------------------------------|------------------------------------------------------------|-------------|
| CustCollectionsBIActivitiesAverageCloseTime | NumOfActivities, AveragecClosedTime  | smmActivities                               | AverageOfChildren(AverageClosedTime) Count(ActivityNumber) | Suljettujen tehtävien määrä ja kyseisten tehtävien keskimääräinen sulkemisaika. |
| CustCollectionsBIActivitiesOpen             | ActivityNumber                       | smmActivities                               | Count(ActivityNumber)                                      | Avoimien tehtävien määrä. |
| CustCollectionsBIAgedBalances               | AgedBalances                         | CustCollectionsBIAgedBalancesView           | Sum(SystemCurrencyBalance)                                 | Erääntyneiden saldojen summa. |
| CustCollectionsBIBalancesDue                | SystemCurrencyAmount                 | CustCollectionsBIBalanceDueView             | Sum(SystemCurrencyAmount)                                  | Myöhässä olevat summat. |
| CustCollectionsBICaseAverageCloseTIme       | NumOfCases, CaseAverageClosedTime    | CustCollectionsCaseDetail                   | AverageOfChildren(CaseAverageClosedTime) Count(NumOfCases) | Suljettujen tapauksien määrä ja kyseisten tapauksien keskimääräinen sulkemisaika. |
| CustCollectionsBICasesOpen                  | CaseId                               | CustCollectionsCaseDetail                   | Count(CaseId)                                              | Avoimien tapauksien määrä. |
| CustCollectionsBICollectionLetter           | CollectionLetterNum                  | CustCollectionLetterJour                    | Count(CollectionLetterNum)                                 | Avoimien maksukehotusten määrä. |
| CustCollectionsBICollectionLetterAmount     | CollectionLetterAmounts              | CustCollectionsBIAccountsReceivables        | Sum(SystemCurrencyAmount)                                  | Kirjattujen maksukehotusten saldo. |
| CustCollectionsBICollectionStatus           | CollectionStatusAmounts              | CustCollectionsBIAccountsReceivables        | Sum(SystemCurrencyAmount)                                  | Niiden tapahtumien saldo, joilla on perintätila. |
| CustCollectionsBICredit                     | CreditExposed, AmountOverCreditLimit | CustCollectionsBICreditView                 | Sum(CreditExposed), Sum(AmountOverCreditLimit)             | Luottoriskien summa ja summa, jolla asiakkaat ovat ylittäneet luottorajansa. |
| CustCollectionsBICustOnHold                 | Estetty                              | CustCollectionsBICustTable                  | Count(Blocked)                                             | Pidossa olevien asiakkaiden määrä. |
| CustCollectionsBIDSO                        | DSO30                                | CustCollectionsBIDSOView                    | AverageOfChildren(DSO30)                                   | 30 päivän selvittämätön päivämyynti. |
| CustCollectionsBIExpectedPayment            | ExpectedPayment                      | CustCollectionsBIExpectedPaymentView        | Sum(SystemCurrencyAmounts)                                 | Seuraavan vuoden kuluessa odotettujen maksujen summa. |
| CustCollectionsBIInterestNote               | InterestNote                         | CustInterestJour                            | Count(InterestNote)                                        | Luotujen korkolaskujen määrä. |
| CustCollectionsBISalesOnHold                | SalesId                              | SalesTable                                  | Count(SalesId)                                             | Pidossa olevien myyntitilausten kokonaismäärä. |
| CustCollectionsBIWriteOff                   | WriteOffAmount                       | CustCollectionsBIWriteOffView               | Sum(SystemCurrencyAmount)                                  | Poistettujen tapahtumien summa. |

