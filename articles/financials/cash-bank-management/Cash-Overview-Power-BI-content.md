---
title: Käteisvarojen yleiskatsauksen Power BI -sisältö
description: Tässä ohjeaiheessa käsitellään käteisvarojen yhteenvetoa ja Power BI -sisältöä. Siinä selitetään, miten sisältöön sisältyvät raportit avataan, sekä kerrotaan sisällön muodostamisessa käytetyistä tietomallista ja yksiköistä.
author: saraschi2
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 5dccb5c5c6c336607603dfc7a935c039e5ac4aa5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568914"
---
# <a name="cash-overview-power-bi-content"></a>Käteisvarojen yleiskatsauksen Power BI -sisältö

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään **käteisvarojen yhteenvetoa** ja Microsoft Power BI -sisältöä. Siinä selitetään, miten sisältöön sisältyvät raportit avataan, sekä kerrotaan sisällön muodostamisessa käytetyistä tietomallista ja yksiköistä.

## <a name="overview"></a>Yleiskuvaus

**Käteisvarojen yhteenvedon** Power BI -sisältö luotiin henkilöille, jotka vastaavat organisaatiossa käteisvaroista. **Käteisvarojen vedon** Power BI -sisältö tuo näkyvyyttä kassavirtaan. Se sisältää myös ennusteita, jotka parantavat päätöksentekoa ja siten myös kassavirran tilaa. Voit analysoida käteisvaroja yrityksen, valuutan ja pankkitilin perusteella. Saat tällä tavoin paremman käsityksen ylijäämistä ja vajeista.

## <a name="accessing-the-power-bi-content"></a>Power BI -sisällön käyttäminen

**Käteisvarojen yhteenvedon** Power BI -sisällön raportit näytetään **Käteisvarojen yleiskatsaus**- ja **Maksuliikenne**-työtiloissa.

Jos haluat tarkastella tietoja sisältäviä kassavirtaennusteita, ennustelaskelmaprosessi on tehtävä maksuliikenteen hallinta-alueen **Laske kassavirtaennusteet** -toiminnolla.  Tämä on suoritettava jokaiselle ennusteeseen sisältyvälle yritykselle.  Seuraavaksi on päivitettävä LedgerCovLiquidityMeasurement-koostemitta **Yksikkösäilö**-sivulla.  

Voit lisätä esimerkinomaisesti kassavirtaennusteen esittelytietoja esittelytietomoduulin **Luo tiedot** -sivulla.  Komentosarja lisää tiedot kassavirtaennusteen taulukoihin. Tällä tavoin raporttien tarvitsemat tiedot saadaan nopeasti esille.  Tämä moduuli on käytettävissä vain, jos esittelytietopakettimalli on otettu käyttöön ympäristössä. 

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Raportit, jotka sisältyvät Power BI -sisältöön
Seuraavassa taulukossa on tietoja mittareista, jotka löytyvät **käteisvarojen yhteenvedon** Power BI -sisällön kultakin raporttisivulta.

| Raportti                                | Sisältö |
|---------------------------------------|----------|
| Kassayhteenveto – kaikki yritykset         | <ul><li>Saapuvat ja lähtevät kassavirrat järjestelmän valuuttana</li><li>Ennakoidut valuuttasaldot</li><li>Pankkitilin kokonaissaldo järjestelmän valuuttana</li><li>Saldo yrityksen mukaan</li><li>Kuluvan päivän toteutuneen ja ennustetun saldon vertailu pankkitilin valuuttana</li></ul> |
| Kassayhteenveto – nykyinen yritys       | <ul><li>Saapuvat ja lähtevät kassavirrat kirjanpitovaluuttana</li><li>Ennakoidut valuuttasaldot</li><li>Pankkitilin kokonaissaldo kirjanpitovaluuttana</li><li>Kuluvan päivän toteutuneen ja ennustetun saldon vertailu pankkitilin valuuttana</li></ul> |
| Kassavirtaennuste – kaikki yritykset    | <ul><li>Saapuvat ja lähtevät kassavirrat järjestelmän valuuttana</li><li>Päivittäisen ennusteen yhteenveto</li><li>Ennusteen tiedot</li></ul> |
| Kassavirtaennuste – nykyinen yritys | <ul><li>Saapuvat ja lähtevät kassavirrat kirjanpitovaluuttana</li><li>Päivittäisen ennusteen yhteenveto</li><li>Ennusteen tiedot</li></ul> |
| Valuuttaennuste                     | <ul><li>Ennakoidut valuuttasaldot</li><li>Päivittäinen valuutan yhteenveto</li><li>Ennusteen tiedot</li></ul> |
| Pankkitilin saldot                         | <ul><li>Pankkitilin kokonaissaldo järjestelmän valuuttana</li><li>Saldo yrityksen mukaan</li><li>Kuluvan päivän toteutuneen ja ennustetun saldon vertailu pankkitilin valuuttana</li><li>Saldo pankkitilin mukaan</li><li>Saldo valuutan mukaan</li></ul> |


## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot

Seuraavassa taulukossa on esitetty yksiköt, joihin **käteisvarojen yhteenvedon** Power BI -sisältö perustuu.

| Kokonaisuus                                                                          | Sisältö |
|---------------------------------------------------------------------------------|----------|
| LedgerCovLiquidityMeasurement\_Company                                          | Yritykset, joiden mukaan raportit suodatetaan |
| LedgerCovLiquidityMeasurement\_Date                                             | Päivämäärät, joiden mukaan raportit suodatetaan |
| LedgerCovLiquidityMeasurement\_LedgerCovForecastActual                          | Todellinen pankkitilin saldo verrattuna viimeisimpään ennustettuun pankkitilin saldoon |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidity                               | Ennustetun tapahtuman tiedot |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany    | Yhteenveto saapuvasta ja lähtevästä kassavirrasta sekä saldo kunkin yrityksen kirjanpitovaluuttana |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise | Yhteenveto saapuvasta ja lähtevästä kassavirrasta sekä saldo kaikkien yritysten järjestelmän valuuttana |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency            | Yhteenveto tapahtuman nettosummasta ja valuuttojen saldosta tapahtuman valuuttana |


