---
title: Toimittajan laskun yksiköt
description: Tässä aiheessa on tietoja toimittajan laskun yksiköistä, joiden avulla kustannustyyppikoodit voidaan konfiguroida sisäisille kustannuksille tai ulkoisille kustannuksille.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 4bbe0fdbf95050ebfa707224f602e5e71ddb3a8f
ms.sourcegitcommit: 611202adaa080250636efabb3b3b32b850d92d04
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/28/2022
ms.locfileid: "8813080"
---
# <a name="vendor-invoice-entities"></a>Toimittajan laskun yksiköt

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

**Aiheutunut kustannus** -moduulin avulla kustannustyyppikoodit voidaan konfiguroida sisäisille kustannuksille tai ulkoisille kustannuksille. Jos kustannus on yrityksen ulkoinen, palveluntarjoajalta odotetaan laskua. Tämä lasku käsitellään laskukirjauskansiona, joka voidaan liittää matkaan, ja laskun arvon voi jakaa yhdelle tai usealle matkan kustannukselle.

Toimittajan laskun yksiköt sallivat kirjauskansiorivin arvon kohdistamisen yhdelle tai useammalle matkan kustannukselle, jolla on sama kustannustyyppikoodi.

Kustannus voidaan kohdistaa vain, jos laskukirjauskansion otsikko ja laskukirjauskansiorivit ovat olemassa.

## <a name="vendor-voyage-cost-allocations-itmledgerjournalcostlinesvoyagesentity"></a>Toimittajan matkan kustannusten kohdistukset (ITMLedgerJournalCostLinesVoyagesEntity)

Toimittajan matkan kustannusten kohdistusten tietoyksikön avulla toimittajan laskun rivin voi kohdistaa yhdelle tai usealle kustannukselle, jota käytetään matkan kustannusalueella. Tätä toimintoa tukee `ITMLedgerJournalCostLinesVoyagesEntity`-entiteetti. Seuraavassa taulukossa luetellaan kentät ja määritykset, jotka muodostavat tämän yksikön.

| Nimi | Yhdistämismääritys | Tietotyyppi | Avain | Pakollinen |
|---|---|---|---|---|
| Varattu summa | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | En | En |
| Kustannustapahtumarivin numero | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Kyllä** | En |
| Kirjauskansion rivinumero | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Kyllä** | En |
| Kirjauskansion numero | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Kyllä** | En |
| Matka | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Kyllä** | En |

## <a name="vendor-shipping-container-cost-allocations-itmledgerjournalcostlinescontainersentity"></a>Toimittajan lähetyskontin kustannusten kohdistukset (ITMLedgerJournalCostLinesContainersEntity)

Toimittajan lähetyskontin kustannusten kohdistusten tietoyksikön avulla toimittajan laskun rivin voi kohdistaa yhdelle tai usealle kustannukselle, jota käytetään lähetyskontin kustannusalueella. Tätä toimintoa tukee `ITMLedgerJournalCostLinesContainersEntity`-entiteetti. Seuraavassa taulukossa luetellaan kentät ja määritykset, jotka muodostavat tämän yksikön.

| Nimi | Yhdistämismääritys | Tietotyyppi | Avain | Pakollinen |
|---|---|---|---|---|
| Varattu summa | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | En | En |
| Lähetyskontti | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Kyllä** | En |
| Kustannustapahtumarivin numero | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Kyllä** | En |
| Kirjauskansion rivinumero | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Kyllä** | En |
| Kirjauskansion numero | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Kyllä** | En |
| Matka | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Kyllä** | En |

## <a name="vendor-folio-cost-allocations-itmledgerjournalcostlinesfoliosentity"></a>Toimittajan pakkauksen kustannusten kohdistukset (ITMLedgerJournalCostLinesFoliosEntity)

Toimittajan pakkauksen kustannusten kohdistusten tietoyksikön avulla toimittajan laskun rivin voi kohdistaa yhdelle tai usealle kustannukselle, jota käytetään pakkauksen kustannusalueella. Tätä toimintoa tukee `ITMLedgerJournalCostLinesFoliosEntity`-entiteetti. Seuraavassa taulukossa luetellaan kentät ja määritykset, jotka muodostavat tämän yksikön.

| Nimi | Yhdistämismääritys | Tietotyyppi | Avain | Pakollinen |
|---|---|---|---|---|
| Varattu summa | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | En | En |
| Kustannustapahtumarivin numero | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Kyllä** | En |
| Lasku | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Kyllä** | En |
| Kirjauskansion rivinumero | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Kyllä** | En |
| Kirjauskansion numero | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Kyllä** | En |

## <a name="vendor-purchase-order-cost-allocations-itmledgerjournalcostlinespurchtableentity"></a>Toimittajan ostotilauksen kustannusten kohdistukset (ITMLedgerJournalCostLinesPurchTableEntity)

Toimittajan ostotilauksen kustannusten kohdistusten tietoyksikön avulla toimittajan laskun rivin voi kohdistaa yhdelle tai usealle kustannukselle, jota käytetään ostotilauksen kustannusalueella. Tätä toimintoa tukee `ITMLedgerJournalCostLinesPurchTableEntity`-entiteetti. Seuraavassa taulukossa luetellaan kentät ja määritykset, jotka muodostavat tämän yksikön.

| Nimi | Yhdistämismääritys | Tietotyyppi | Avain | Pakollinen |
|---|---|---|---|---|
| Varattu summa | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | En | En |
| Kustannustapahtumarivin numero | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Kyllä** | En |
| Kirjauskansion rivinumero | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Kyllä** | En |
| Kirjauskansion numero | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Kyllä** | En |
| Ostotilaus | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Kyllä** | En |

## <a name="vendor-item-cost-allocations-itmledgerjournalcostlinespurchlineentity"></a>Toimittajan nimikkeen kustannusten kohdistukset (ITMLedgerJournalCostLinesPurchLineEntity)

Toimittajan nimikkeen kustannusten kohdistusten tietoyksikön avulla toimittajan laskun rivin voi kohdistaa yhdelle tai usealle kustannukselle, jota käytetään nimikkeen kustannusalueella. Nimikkeen kustannusalue kattaa kustannukset ostotilausrivillä. Tätä toimintoa tukee `ITMLedgerJournalCostLinesPurchLineEntity`-entiteetti. Seuraavassa taulukossa luetellaan kentät ja määritykset, jotka muodostavat tämän yksikön.

| Nimi | Yhdistämismääritys | Tietotyyppi | Avain | Pakollinen |
|---|---|---|---|---|
| Varattu summa | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | En | En |
| Kustannustapahtumarivin numero | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Kyllä** | En |
| Kirjauskansion rivinumero | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Kyllä** | En |
| Kirjauskansion numero | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Kyllä** | En |
| Ostotilaus | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Kyllä** | En |
| Ostotilausrivin numero | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Kyllä** | En |

## <a name="vendor-transfer-order-line-cost-allocations-itmledgerjournalcostlinestransferlineentity"></a>Toimittajan siirtotilausrivin kustannusten kohdistukset (ITMLedgerJournalCostLinesTransferLineEntity)

Toimittajan siirtotilausrivin kustannusten kohdistusten tietoyksikön avulla toimittajan laskun rivin voi kohdistaa yhdelle tai usealle kustannukselle, jota käytetään siirtotilauksen kustannusalueella. Tätä toimintoa tukee `ITMLedgerJournalCostLinesTransferLineEntity`-entiteetti. Seuraavassa taulukossa luetellaan kentät ja määritykset, jotka muodostavat tämän yksikön.

| Nimi | Yhdistämismääritys | Tietotyyppi | Avain | Pakollinen |
|---|---|---|---|---|
| Varattu summa | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | En | En |
| Kustannustapahtumarivin numero | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Kyllä** | En |
| Kirjauskansion rivinumero | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Kyllä** | En |
| Kirjauskansion numero | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Kyllä** | En |
| Siirtotilaus | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Kyllä** | En |
| Siirtotilausrivin numero | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Kyllä** | En |

### <a name="reference-table"></a>Viitetaulu

Matkan kustannusrivit liittyvät suoraan kustannustapahtumatietueeseen. Tietueeseen sisältyy **Viitetaulun tunnus** -arvo. Tämä arvo on yksilöllinen kullakin kustannusalueella (esim. matka, lähetyskontti). Kun tiettyihin taulukkonumeroihin viitataan tietoyksikköjä käyttämällä luotuja tietoja varten, yksiköt jaetaan **Viitetaulun tunnus** -arvojen perusteella.

Viitetaulukon (`RefTableId`) arvot ja tapahtuman tyyppi (`TransType`) ovat implisiittisiä joko aiheutuneiden kustannusten ostorivin tai aiheutuneiden kustannusten siirtoriviyksikön valinnassa.

## <a name="vendor-invoice-journal-lines-vendorinvoicejournallineentity"></a>Toimittajan laskun kirjauskansiorivit (VendorInvoiceJournalLineEntity)

Ennen kuin kirjauskansiorivin arvon voi kohdistaa yhdelle tai useammalle kustannukselle **Aiheutunut kustannus** -moduulissa, kirjauskansiorivi on liitettävä kustannusalueeseen. Tämän toiminnan tukemiseksi **Aiheutunut kustannus** -moduuli lisää uusia kenttiä kirjauskansiorivien taulukkoon (`LedgerJournalTrans`).

### <a name="fields-added-to-the-vendor-invoice-journal-line-entity"></a>Toimittajan laskun kirjauskansiorivien yksikköön lisättävät kentät

Seuraavassa taulukossa näkyvät kentät, jotka **Aiheutunut kustannus** -moduuli lisää toimittajan laskun kirjauskansiorivien yksikköön (`VendorInvoiceJournalLineEntity`). Näiden kenttien avulla järjestelmä voi luoda kirjauskansion rivejä ja kohdistaa kustannuksia niihin.

| Nimi | Yhdistämismääritys | Tietotyyppi | Avain | Pakollinen |
|---|---|---|---|---|
| Kustannusalue | LedgerJournalTrans.ITMCostArea | Int | En | En |
| Kustannustyypin koodi | LedgerJournalTrans.ITMCostTypeId | Nvarchar(20) | En | En |

### <a name="mainoffset-account"></a>Pää-/vastatili

Aiheutuneen kustannuksen matkaan liittyvän laskun kirjauskansiorivin pää-/vastatilin määrittelee kustannustyyppikoodi. Kun kustannustyyppikoodi sisältyy laskun kirjauskansioriviin, koodin selvitystiliä käytetään joko päätilinä tai vastatilinä skenaarion mukaan:

- **Yhden rivin kirjauskansio** – Jos päätili (toisin sanoen toimittajan tili) on määritetty ja kustannustyyppikoodi on määritetty, tämän kustannustyyppikoodin selvitystilin arvo syötetään vastatilille.
- **Usean rivin kirjauskansio** – Jos päätiliä ei ole määritetty, mutta kustannustyyppikoodi on määritetty, tämän kustannustyyppikoodin selvitystilin arvo syötetään päätilille. Toimittajaa hyvittävä kirjauskansiorivi ei viittaa kustannustyyppikoodiin.

## <a name="sequencing"></a>Järjestys

Kirjauskansioiden ja kirjauskansiorivitaulukoiden välisten riippuvuuksien vuoksi matkatietue on luotava ensin. Matkarivit voi luoda vasta sitten, kun matka, lähetyskontti ja pakkaukset on luotu.

Jos haluat kohdistaa matkan laskun, järjestelmän on käsiteltävä yksiköt seuraavassa järjestyksessä:

1. Laskukirjauskansion otsikko (`VendInvoiceJournalHeaderEntity`)
1. Laskukirjauskansion rivi (`VendInvoiceJournalLineEntity`)
1. Aiheutuneiden kustannusten kohdistukset (`ITMLedgerJournalEntities`)
