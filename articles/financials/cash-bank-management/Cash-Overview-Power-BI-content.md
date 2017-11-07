---
title: "Kassayhteenveto – Power BI -sisältö"
description: "Tässä ohjeaiheessa käsitellään kassayhteenvetoa ja Power BI -sisältöä. Siinä selitetään, miten sisältöön sisältyvät raportit avataan, sekä kerrotaan sisällön muodostamisessa käytetyistä tietomallista ja yksiköistä."
author: saraschi2
manager: AnnBe
ms.date: 06/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: e891f501727842e176741953df5ef9dd0336a2d5
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="cash-overview-power-bi-content"></a>Kassayhteenveto – Power BI -sisältö

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään **kassayhteenvetoa** ja Microsoft Power BI -sisältöä. Siinä selitetään, miten sisältöön sisältyvät raportit avataan, sekä kerrotaan sisällön muodostamisessa käytetyistä tietomallista ja yksiköistä.

## <a name="overview"></a>Yleiskuvaus

**Kassayhteenveto** – Power BI -sisältö luotiin henkilöille, jotka vastaavat organisaatiossa käteisvaroista. **Kassayhteenveto** – Power BI -sisältö tuo näkyvyyttä kassavirtaan. Se sisältää myös ennusteita, jotka parantavat päätöksentekoa ja siten myös kassavirran tilaa. Voit analysoida käteisvaroja yrityksen, valuutan ja pankkitilin perusteella. Saat tällä tavoin paremman käsityksen ylijäämistä ja vajeista.

## <a name="accessing-the-power-bi-content"></a>Power BI -sisällön käyttö

Jos käytössä on Dynamics 365 for Finance and Operations, Enterprise Editionin heinäkuun 2017 päivitys, **Kassayhteenveto** – Power BI -sisällön raportit näkyvät **Kassayhteenveto**- ja **Maksuliikenne**-työtiloissa.

Jos haluat tarkastella tietoja sisältäviä kassavirtaennusteita, ennustelaskelmaprosessi on tehtävä maksuliikenteen hallinta-alueen **Laske kassavirtaennusteet** -toiminnolla.  Tämä on suoritettava jokaiselle ennusteeseen sisältyvälle yritykselle.  Seuraavaksi on päivitettävä LedgerCovLiquidityMeasurement-koostemitta **Yksikkösäilö**-sivulla.  

Voit lisätä esimerkinomaisesti kassavirtaennusteen esittelytietoja esittelytietomoduulin **Luo tiedot** -sivulla.  Komentosarja lisää tiedot kassavirtaennusteen taulukoihin. Tällä tavoin raporttien tarvitsemat tiedot saadaan nopeasti esille.  Tämä moduuli on käytettävissä vain, jos esittelytietopakettimalli on otettu käyttöön ympäristössä. 

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Raportit, jotka sisältyvät Power BI -sisältöön
Seuraavassa taulukossa on tietoja mittareista, jotka löytyvät **Kassayhteenveto** – Power BI -sisällön kultakin raporttisivulta.

| Raportti                                | Sisältö |
|---------------------------------------|----------|
| Kassayhteenveto – kaikki yritykset         | <ul><li>Saapuvat ja lähtevät kassavirrat järjestelmän valuuttana</li><li>Ennakoidut valuuttasaldot</li><li>Pankkitilin kokonaissaldo järjestelmän valuuttana</li><li>Saldo yrityksen mukaan</li><li>Kuluvan päivän toteutuneen ja ennustetun saldon vertailu pankkitilin valuuttana</li></ul> |
| Kassayhteenveto – nykyinen yritys       | <ul><li>Saapuvat ja lähtevät kassavirrat kirjanpitovaluuttana</li><li>Ennakoidut valuuttasaldot</li><li>Pankkitilin kokonaissaldo kirjanpitovaluuttana</li><li>Kuluvan päivän toteutuneen ja ennustetun saldon vertailu pankkitilin valuuttana</li></ul> |
| Kassavirtaennuste – kaikki yritykset    | <ul><li>Saapuvat ja lähtevät kassavirrat järjestelmän valuuttana</li><li>Päivittäisen ennusteen yhteenveto</li><li>Ennusteen tiedot</li></ul> |
| Kassavirtaennuste – nykyinen yritys | <ul><li>Saapuvat ja lähtevät kassavirrat kirjanpitovaluuttana</li><li>Päivittäisen ennusteen yhteenveto</li><li>Ennusteen tiedot</li></ul> |
| Valuuttaennuste                     | <ul><li>Ennakoidut valuuttasaldot</li><li>Päivittäinen valuutan yhteenveto</li><li>Ennusteen tiedot</li></ul> |
| Pankkitilin saldot                         | <ul><li>Pankkitilin kokonaissaldo järjestelmän valuuttana</li><li>Saldo yrityksen mukaan</li><li>Kuluvan päivän toteutuneen ja ennustetun saldon vertailu pankkitilin valuuttana</li><li>Saldo pankkitilin mukaan</li><li>Saldo valuutan mukaan</li></ul> |

## <a name="extending-the-power-bi-content"></a>Power BI -sisällön laajentaminen
Voit tehdä hyviä analyyseja henkilöille, jotka eivät käytä Dynamics 365:tä, Lifecycle Servicesin (LCS) sisältöpakettien avulla. Nämä sisältöpaketit voidaan muokata sisältämään muita raportteja ja visuaalisia tietoja, ja ne voidaan sitten julkaista analysoitavaksi Power BI.com -vuokraajassa. 

**Kassayhteenveto** – Power BI -sisältö sijaitsee LCS:n Jaettu omaisuus -kirjastossa. Lisätietoja sisällön lataamisesta ja sen käyttöönottamisesta organisaatiossa on ohjeaiheessa [Microsoftin ja kumppaneiden Power BI -sisältö LCS-sovelluksessa](../../dev-itpro/analytics/power-bi-content-microsoft-partners.md). Katso Power BI -sisällön käyttöönotosta kertova esittely Office Mixin kohdassa [Microsoftin ja kumppaneiden Power BI -sisältö Dynamics Lifecycle Services -sovelluksessa](https://mix.office.com/watch/9puyb1b2xs1w).

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot

Seuraavassa taulukossa on esitetty yksiköt, joihin **Kassayhteenveto** – Power BI -sisältö perustuu.

| Kokonaisuus                                                                          | Sisältö |
|---------------------------------------------------------------------------------|----------|
| LedgerCovLiquidityMeasurement\_Company                                          | Yritykset, joiden mukaan raportit suodatetaan |
| LedgerCovLiquidityMeasurement\_Date                                             | Päivämäärät, joiden mukaan raportit suodatetaan |
| LedgerCovLiquidityMeasurement\_LedgerCovForecastActual                          | Todellinen pankkitilin saldo verrattuna viimeisimpään ennustettuun pankkitilin saldoon |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidity                               | Ennustetun tapahtuman tiedot |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany    | Yhteenveto saapuvasta ja lähtevästä kassavirrasta sekä saldo kunkin yrityksen kirjanpitovaluuttana |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise | Yhteenveto saapuvasta ja lähtevästä kassavirrasta sekä saldo kaikkien yritysten järjestelmän valuuttana |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency            | Yhteenveto tapahtuman nettosummasta ja valuuttojen saldosta tapahtuman valuuttana |

Näitä yksikköjä käytettiin luomaan laskettuja mittoja tietomallissa. Näillä laskennallisilla mitoilla lasketaan sitten **Kassayhteenveto** – Power BI -sisällön kaavioissa ja raporteissa. Voit sisällyttää lisälaskutoimitukset raportteihin ja koontinäyttöön lataamalla Power BI -tiedoston LCS:stä ja muokkaamalla sitä. Tämä tiedosto on sisällön luomisessa käytetty oletustietomalli. Kun olet tehnyt haluamasi muutokset, voit luoda organisaation sisällön ja koontinäytöt, jotka sisältävät lisäämäsi tiedot.


